# dsh-superagent

[English](README.md) | 简体中文

> **仅供研究参考的原型，并非 DeepSeek 官方产品。** 本代码源于我们团队的日常开发工作，其中大量工程由编码智能体完成。请将其视为研究代码，而非可直接投入生产的软件。它可能仍包含缺陷，编码风格与工程实践也可能并不统一。在你自己的环境中使用之前，请先审阅并酌情调整。
>
> 为公开发布，我们对其进行了改编，因此它与我们的内部版本，以及 *Exploring Super-agent Design: Towards a More Autonomous Agent System* 一文所描述的实现并不完全一致。文章中讨论的部分设计属于未来发展方向，本原型尚未实现。

dsh-superagent 是一个面向单个 GitHub 仓库的主动式编码智能体，以 [DeepSeek Harness](https://www.deepseek.com/en/harness/) 插件包（bundle）的形式提供。它监听 GitHub，也可选择监听飞书。当获得许可的人请求智能体处理某项工作时，它会创建一个工作项，在专属的智能体会话和目录中推进，并在原会话中回复，例如通过一个拉取请求（pull request）来答复。网页面板会显示哪些事项需要人来处理。

它同时也是一种与智能体协作的方式：**尽可能少占用人的注意力，尽可能多地创造价值。** 一个能够为整个团队行动的智能体，也可能浪费整个团队的注意力；因此，它只在被请求时行动，或只在团队书面规则允许时行动，并且只在有人需要行动或能够使用结果时才发言。[docs/000-philosophy.md](docs/000-philosophy.md) 阐述了这一原则，以及它对运维者的要求。

## 安装

安装步骤较多，因此由智能体陪你一起完成。请对你的编码智能体说：

> 请阅读本仓库中的 SETUP.md，和我一起安装配置 dsh-superagent。

它会一次只问一个简短的问题，然后一次性展示完整计划，接着完成安装与配置。它遵循的正是 [SETUP.md](SETUP.md)。

## 文档

请按编号顺序阅读文档；每篇只建立在前面已介绍的概念之上。以下文档目前仍以英文撰写。

- [000 理念（Philosophy）](docs/000-philosophy.md)
- [001 领域模型（Domain model）](docs/001-domain.md)
- [002 授权（Authorization）](docs/002-authorization.md)
- [003 执行（Execution）](docs/003-execution.md)
- [004 提示词（Prompts）](docs/004-prompts.md)
- [005 面板（Panel）](docs/005-panel.md)
- [006 部署（Deployment）](docs/006-deployment.md)：手动安装、配置、升级与故障排除
- [007 架构（Architecture）](docs/007-architecture.md)
- [008 实践手册（Cookbook）](docs/008-cookbook.md)：新增一个 Source

## 开发

`pnpm check` 会运行类型检查、测试和构建。

## 许可证

[MIT](LICENSE)
