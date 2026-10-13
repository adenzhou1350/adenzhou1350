# 周栩丞 · Aden Zhou

**AI Infra · 具身 Agent**

主要做模型推理和具身 Agent。这里放我的量化实验、动作决策教学，以及给推理框架和 GPU 编译器提交的修复。

[个人网站](https://adenzhou1350.github.io/) · [技术博客](https://adenzhou1350.github.io/blog/) · [动手教学](https://adenzhou1350.github.io/learn/) · [工作联系](mailto:aden1350@outlook.com)

## 从这里开始

| 想看什么 | 项目 | 可以做什么 |
|---|---|---|
| 低比特训练与压缩推理 | [Bonsai 风格量化教学](https://github.com/adenzhou1350/bonsai-qat-teaching) | 先在[浏览器里试三值打包](https://adenzhou1350.github.io/learn/bonsai-low-bit/#ternary-demo)，再看 CPU 检查、QAT 和单卡 MoE 实验；仓库未发布模型权重 |
| 小模型如何选择动作 | [Jev 决策模型实战](https://github.com/adenzhou1350/jev-decision-teaching) | 先在 CPU 上试玩推箱子，再学习候选打分、训练与页面按钮选择；独立 Jev-style 教学实现 |
| 用代码理解生成模型 | [minimind-diffusion](https://github.com/adenzhou1350/minimind-diffusion) | 用 PyTorch 学习掩码扩散，从小模型测试走到训练与采样；生成质量仍在探索 |
| 定制自己的助手 | [soul-generator](https://github.com/adenzhou1350/soul-generator) | 把表达方式和工作习惯整理成可编辑的 SOUL.md |

## 开源贡献

给 vLLM、SGLang、TileLang、Triton 等项目提交过已合并的修复，涉及多模态输入、GPU 同步、资源清理和数值计算。

[按项目查看贡献](https://adenzhou1350.github.io/contributions/)：点进对应项目，可以看到我在该仓库已合并的 PR。

## 两篇具体的记录

- [TileLang 同步修复：一个 block 报到了两次](https://adenzhou1350.github.io/blog/tilelang-grid-barrier/)：从两个 block 的复现，到修复线程选择和回归测试；[PR #3400](https://github.com/tile-ai/tilelang/pull/3400) 已合并。
- [单张 5090 跑 122B MoE](https://adenzhou1350.github.io/blog/bonsai-5090-experiment/)：记录显存、配对评测，以及一次没有带来整模型收益的解包优化。质量未达原定门槛。

更多[实验与故障复盘](https://adenzhou1350.github.io/blog/)。项目里的教学实现、个人实验和 fork 分别标明来源与验证范围。

有模型部署、量化或 Agent 工程中的具体问题，可以写信到 [aden1350@outlook.com](mailto:aden1350@outlook.com)，附上环境、复现步骤和预期结果。

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="images/github-snake-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="images/github-snake.svg" />
  <img src="images/github-snake.svg" alt="根据 GitHub 贡献记录生成的动态小蛇" width="100%" />
</picture>
