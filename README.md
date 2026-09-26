# Hi, I'm Aden 👋

I build LLM inference and research tools, and contribute fixes to serving systems. Recent changes have been merged into Mooncake, vLLM, and LMDeploy. I care about reproducible bugs, measured performance, and changes that are useful upstream.

我关注大模型推理系统、GPU 性能与自动研究工具。Mooncake、vLLM 和 LMDeploy 已有合并贡献，也持续在 SGLang 等项目中提交修复。我重视真实瓶颈、正确性与可复现的实验。

## Selected upstream work

| Project | Contribution | What changed |
| --- | --- | --- |
| [Mooncake](https://github.com/kvcache-ai/Mooncake/pull/4063) | Bound pooled TCP admission by queued bytes · merged | Added an opt-in byte limit so queued transfers cannot retain unbounded payload memory behind an item-count limit. |
| [vLLM](https://github.com/vllm-project/vllm/pull/56882) | Preserve DeepSeek V4 image block spacing · merged | Fixed multimodal prompt formatting without changing the intended image content. |
| [LMDeploy](https://github.com/InternLM/lmdeploy/pull/5000) | Restore `getenv` after parsing errors · merged | Kept environment parsing from leaving process state modified on failure. |
| [PyTorch AO](https://github.com/pytorch/ao/pull/4948) | Handle scalar and vector transpose in PT2E x86 lowering · open | Preserved the identity behavior of `torch.t` below rank two and added regression cases. |

[Read three short case studies with validation evidence](CONTRIBUTIONS.md).

## Projects I build

| Project | What you can explore |
| --- | --- |
| [minimind-diffusion](https://github.com/adenzhou1350/minimind-diffusion) | A compact PyTorch path from training to evaluation for text and multimodal diffusion language models. The README explains the design and records limitations found in small-model experiments. |
| [soul-generator](https://github.com/adenzhou1350/soul-generator) | A reusable OpenClaw persona skill with presets and three ways to create a new persona: a public figure, a personality type, or a custom description. |

## Current focus

- **Inference and kernels:** inspect real workloads, establish correctness and matched baselines, then optimize memory traffic, scheduling, and kernel dispatch. [vLLM contributions](https://github.com/pulls?q=is%3Apr+author%3Aadenzhou1350+repo%3Avllm-project%2Fvllm) · [SGLang contributions](https://github.com/pulls?q=is%3Apr+author%3Aadenzhou1350+repo%3Asgl-project%2Fsglang)
- **KV transfer and distributed training:** reduce avoidable work while preserving concurrency and failure semantics. [Mooncake contributions](https://github.com/pulls?q=is%3Apr+author%3Aadenzhou1350+repo%3Akvcache-ai%2FMooncake) · [DeepSpeed contributions](https://github.com/pulls?q=is%3Apr+author%3Aadenzhou1350+repo%3Adeepspeedai%2FDeepSpeed)
- **Evidence-based research automation:** build a persistent public-source Scout that tracks evidence, counterexamples, verification cost, and human review. It is experimental; a research lead is not a validated fix or a PR. [Scout work](https://github.com/adenzhou1350/kernel_opt_agent/pulls?q=is%3Apr+is%3Amerged) · [upstream toolkit work](https://github.com/pulls?q=is%3Apr+author%3Aadenzhou1350+repo%3Adasikuzi2%2Fkernel_opt_agent)

## How I work

I try to keep every proposal small enough to review, reproduce the issue before fixing it, distinguish kernel timing from end-to-end impact, and describe validation limits plainly. I'm learning more about GPU architecture, numerical accuracy, distributed systems, and maintaining open-source changes through review.

欢迎交流：**aden1350@outlook.com**
