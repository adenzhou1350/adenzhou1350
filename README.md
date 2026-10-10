# 周栩丞 · Aden Zhou

**AI Infra & Embodied Agents — 让智能体真正跑起来。**

我做具身 Agent，也做它底下的推理系统。关注模型、工具与状态如何接成可以运行、检查和恢复的任务链；通过公开项目、技术复盘和上游贡献记录这些实践。

[个人网站](https://adenzhou1350.github.io/) · [技术博客](https://adenzhou1350.github.io/blog/) · [动手教学](https://adenzhou1350.github.io/learn/) · [工作联系](mailto:aden1350@outlook.com)

## 从这里开始

| 想看什么 | 项目 | 可以做什么 |
|---|---|---|
| 小模型如何选择动作 | [Jev 决策模型实战](https://github.com/adenzhou1350/jev-decision-teaching) | 先在 CPU 上试玩推箱子，再学习候选打分、训练与页面按钮选择；独立 Jev-style 教学实现 |
| 低比特训练与压缩推理 | [Bonsai 风格量化教学](https://github.com/adenzhou1350/bonsai-qat-teaching) | 从 CPU 方程读到 MoE 三值 QAT、恢复与单卡推理实验，逐项检查结果 |
| 用代码理解生成模型 | [minimind-diffusion](https://github.com/adenzhou1350/minimind-diffusion) | 用 PyTorch 学习掩码扩散，从小模型测试走到训练与采样；生成质量仍在探索 |
| 定制自己的助手 | [soul-generator](https://github.com/adenzhou1350/soul-generator) | 把表达方式和工作习惯整理成可编辑的 SOUL.md |

## 让改进回到上游

几个已合并的具体改动：

- [vLLM #56882](https://github.com/vllm-project/vllm/pull/56882)：保留 DeepSeek V4 多模态输入中图像块的结构边界。
- [Mooncake #4063](https://github.com/kvcache-ai/Mooncake/pull/4063)：让池化 TCP 的准入预算按排队字节数计算。
- [TIRx-harness #12](https://github.com/mlc-ai/TIRx-harness/pull/12)：限定 ptxas 资源统计的 kernel report 范围，避免串用数字。

[查看精选贡献与原始 PR](https://adenzhou1350.github.io/contributions/) · [阅读实验和故障复盘](https://adenzhou1350.github.io/blog/)

个人项目、基于他人工作的扩展和贡献用 fork 在仓库中分别标明来源。量化、生成模型与 Agent 都有各自的验证范围，具体结果以项目文档和实验记录为准。

欢迎交流 **Agent 工程、量化训练、推理部署与可复现的系统问题**。

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="images/github-snake-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="images/github-snake.svg" />
  <img src="images/github-snake.svg" alt="根据 GitHub 贡献记录生成的动态小蛇" width="100%" />
</picture>
