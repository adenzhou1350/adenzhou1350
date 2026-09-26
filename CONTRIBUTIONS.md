# Selected contribution case studies

These are merged upstream changes. Each case links to the original PR for the diff, review discussion, and full test record.

## Mooncake: bound waiting TCP payloads by bytes

[Merged PR #4063](https://github.com/kvcache-ai/Mooncake/pull/4063)

**Problem.** Classic TCP limited a peer's waiting requests by item count, but each waiting request retained its source payload. Large transfers could therefore hold much more memory than the queue length suggested.

**Change.** I added an opt-in per-peer byte limit that counts queued work and pending admissions. A request over the limit gets the existing `QUEUE_FULL` result. Moving work between those two waiting containers does not change its charge; starting, timing out, or removing it releases the charge. Leaving the setting unset or at zero preserves existing behavior.

**Evidence and limit.** The PR reports 49/49 CPU test cases passing, 100 repeats of the new queued-byte cases, and 15/15 related ASan/UBSan cases passing. It does **not** claim measured throughput or RSS improvement. A nonzero production default still needs representative slow-peer and recovery measurements.

## vLLM: preserve DeepSeek V4 multimodal block boundaries

[Merged PR #56882](https://github.com/vllm-project/vllm/pull/56882)

**Problem.** The renderer flattened OpenAI-format content before the tokenizer could insert the expected blank-line separation between text and image blocks. That changed prompt bytes and image offsets.

**Change.** The synchronous and asynchronous renderers keep structured content until the DeepSeek V4 tokenizer joins blocks with two newlines. Text-only string behavior stays the same.

**Evidence and limit.** The PR reports 40 focused CPU tests passing, plus an official two-image request using real DeepSeek V4 weights on eight A800 GPUs. That full-stack run included the patch, but was not an exact-current-main qualification. The responses were semantically correct but not bit-identical; this is a formatting fix, not a performance claim.

## LMDeploy: restore a process-global function on parser errors

[Merged PR #5000](https://github.com/InternLM/lmdeploy/pull/5000)

**Problem.** `set_envs()` temporarily replaced `os.getenv`. An exception while parsing an invalid environment value skipped the normal restoration and left the process-global function patched.

**Change.** I moved restoration into a `finally` block. The production diff is small and keeps the success path unchanged.

**Evidence and review.** An exception-path probe failed on the original main branch and passed with the fix. The dedicated test file was removed during review at the maintainer's request; the final merged PR contains the production fix.
