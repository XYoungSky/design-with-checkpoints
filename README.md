# Design with Checkpoints

[English](#design-with-checkpoints) · [简体中文](#简体中文)

Design with Checkpoints is a frontend design skill for building websites, redesigning interfaces, and reviewing existing designs. It involves you in key decisions through focused questions and sample reviews, then guides implementation and testing in stages.

## Installation

### Using the skills CLI

Requires Node.js and npm. Run from your project directory:

```bash
npx skills@latest add XYoungSky/design-with-checkpoints --skill design-with-checkpoints
```

Select your target agent in the installer. Add `--global` to install across projects, or `--agent codex` / `--agent claude-code` to choose an agent directly. See the [skills CLI documentation](https://github.com/vercel-labs/skills#install-a-skill) for other supported agents and options.

### Manual installation

Download and extract the repository, then copy the `skills/design-with-checkpoints/` folder to one of these locations:

| Agent | This project | All your projects |
| --- | --- | --- |
| [Codex](https://developers.openai.com/codex/skills#where-to-save-skills) | `.agents/skills/design-with-checkpoints/` | `~/.agents/skills/design-with-checkpoints/` |
| [Claude Code](https://code.claude.com/docs/en/skills#choose-where-skills-load) | `.claude/skills/design-with-checkpoints/` | `~/.claude/skills/design-with-checkpoints/` |

Keep `SKILL.md`, `references/`, `agents/`, and `LICENSE` together, with `SKILL.md` directly inside the installed folder. Open or reload your agent to load the skill.

## Quick start

In Codex CLI or the IDE extension:

```text
$design-with-checkpoints Improve the current website.
Audit it first and recommend changes. Let me choose the main direction;
handle the details yourself.
```

In Claude Code:

```text
/design-with-checkpoints Review the current website and recommend improvements.
```

In other tools, select the skill using the tool's skill picker or ask an agent with local file access to read `/path/to/design-with-checkpoints/SKILL.md`, replacing the path with its actual location.

## Use cases

| Task | Approach |
| --- | --- |
| New website | Establish goals, content, and design direction, then build in stages |
| Redesign | Inspect the interface, preserve effective design, and address the main problems |
| Plan or review | Analyze problems, recommend design changes, and outline validation |
| Focused improvement | Identify and fix a specific issue, then retest related functionality |

## Key Features

- **Focused checkpoints.** Discuss direction and key details using concrete options tied to the interface.
- **Sample reviews.** Review representative layouts and interactions before extending them across the site.
- **Project continuity.** Work with the existing stack, design conventions, and agreed decisions.
- **Practical verification.** Check responsive layouts, interactions, and accessibility, and document the results.

## Files

- [SKILL.md](skills/design-with-checkpoints/SKILL.md): agent instructions and workflow.
- [Interview and decisions](skills/design-with-checkpoints/references/interview-and-decisions.md): options, decision records, and feedback.
- [Reference evidence](skills/design-with-checkpoints/references/reference-evidence.md): research, prototype comparisons, and evidence quality.
- [Motion and QA](skills/design-with-checkpoints/references/motion-and-qa.md): interaction, responsive behavior, accessibility, and performance checks.
- [Project templates](skills/design-with-checkpoints/references/project-templates.md): briefs, specifications, handoffs, and regression scenarios.
- [Sources](skills/design-with-checkpoints/references/sources.md): background and references for the workflow.

## License

Licensed under the [MIT License](LICENSE).

## 简体中文

Design with Checkpoints 是一个用于网站新建、界面改版和设计审查的前端设计 skill。它通过具体提问和样例审阅，让你参与关键设计决策，再分阶段推进实现与测试。

### 安装

#### 使用 skills CLI

需要 Node.js 和 npm。在项目目录中运行：

```bash
npx skills@latest add XYoungSky/design-with-checkpoints --skill design-with-checkpoints
```

按提示选择目标 agent。添加 `--global` 可跨项目使用；添加 `--agent codex` 或 `--agent claude-code` 可直接指定 agent。其他支持的工具与选项见 [skills CLI 文档](https://github.com/vercel-labs/skills#install-a-skill)。

#### 手动安装

下载并解压仓库，将其中的 `skills/design-with-checkpoints/` 文件夹复制到以下一个位置：

| Agent | 当前项目 | 所有项目 |
| --- | --- | --- |
| [Codex](https://developers.openai.com/codex/skills#where-to-save-skills) | `.agents/skills/design-with-checkpoints/` | `~/.agents/skills/design-with-checkpoints/` |
| [Claude Code](https://code.claude.com/docs/en/skills#choose-where-skills-load) | `.claude/skills/design-with-checkpoints/` | `~/.claude/skills/design-with-checkpoints/` |

保留文件夹内的 `SKILL.md`、`references/`、`agents/` 和 `LICENSE`，将 `SKILL.md` 放在该文件夹根目录。随后打开或重新加载 agent。

### 快速开始

在 Codex CLI 或 IDE 扩展中：

```text
$design-with-checkpoints 改进当前网站。
先审查现状，给出建议；重要方向由我选择，细节由你处理。
```

在 Claude Code 中：

```text
/design-with-checkpoints 审查当前网站并提出改进建议。
```

在其他工具中，通过技能选择器选中此 skill；也可以让具备本地文件访问能力的 agent 读取 `/path/to/design-with-checkpoints/SKILL.md`，将路径替换为实际位置。

### 适用场景

| 任务 | 工作方式 |
| --- | --- |
| 新建网站 | 明确目标、内容与设计方向，逐步完成实现 |
| 界面改版 | 检查现有界面，保留有效设计，改善主要问题 |
| 方案与审查 | 分析问题，提供设计建议和验证思路 |
| 局部优化 | 定位并修改具体问题，复测相关功能 |

### 核心特点

- **关键决策提问。** 结合实际界面提供具体选项，讨论设计方向和关键细节。
- **阶段样例审阅。** 通过典型布局和交互样例确认效果，再扩展到整个网站。
- **保持项目一致性。** 沿用现有技术栈、设计约定和已确定的决策。
- **实际效果验证。** 检查响应式布局、交互和可访问性，并记录测试结果。

### 文件导航

- [SKILL.md](skills/design-with-checkpoints/SKILL.md)：技能说明与工作流程。
- [提问与决策](skills/design-with-checkpoints/references/interview-and-decisions.md)：设计选项、决策记录与反馈处理。
- [参考与证据](skills/design-with-checkpoints/references/reference-evidence.md)：案例研究、原型比较与证据评估。
- [动效与质量检查](skills/design-with-checkpoints/references/motion-and-qa.md)：交互、响应式、可访问性与性能检查。
- [项目模板](skills/design-with-checkpoints/references/project-templates.md)：简报、设计规格、交付记录和回归场景。
- [参考来源](skills/design-with-checkpoints/references/sources.md)：工作方法的背景与参考资料。

### 许可证

本项目采用 [MIT License](LICENSE)。
