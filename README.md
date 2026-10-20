# Design with Checkpoints

[English](#design-with-checkpoints) · [简体中文](#简体中文)

Design with Checkpoints is a frontend design skill for building websites, redesigning interfaces, and reviewing existing designs. The agent aligns with you at three checkpoints, proposes opinionated layout, typography, and motion directions, and checks every layout and animation before delivery.

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
| Design review | Prioritized findings with concrete fixes and severity, without editing |
| Focused improvement | Identify and fix a specific issue, then retest related functionality |

## Key Features

- **Three checkpoints.** Confirm the brief, choose a direction from real-content samples, and review one slice before it is repeated across pages.
- **Opinionated proposals.** Each direction states its design idea, its layout, type, and motion moves, what it costs, and a recommendation.
- **Layout check.** Every changed page is checked at phone and desktop widths, in Chinese and English, against concrete type and spacing rules and a list of machine-made patterns.
- **Motion intensity and inventory.** Choose calm, lively, or expressive motion from samples. Every animation is listed with its job, duration, and reduced-motion fallback; you see the list at the direction check, the sample review, and in the final report.
- **Lightweight.** Small tweaks are fixed directly; reference files load only when needed.

## Files

- [SKILL.md](skills/design-with-checkpoints/SKILL.md): workflow and checkpoints.
- [Alignment](skills/design-with-checkpoints/references/alignment.md): restating the brief, asking questions, presenting directions, recording decisions, and interface copy.
- [Layout and type](skills/design-with-checkpoints/references/layout-and-type.md): composition, grid, spacing, Chinese and English typography, and the layout check.
- [Motion](skills/design-with-checkpoints/references/motion.md): animation jobs, intensity levels, techniques, starting values, reduced motion, and the motion inventory.
- [Verify](skills/design-with-checkpoints/references/verify.md): the basic review and the handoff report.
- [Regression cases](evals/cases.md): cases for revising the skill; not installed with it.

## Acknowledgements

The workflow draws on [Anthropic frontend-design](https://github.com/anthropics/skills/blob/main/skills/frontend-design/SKILL.md), [taste-skill](https://github.com/Leonxlnx/taste-skill), [Matt Pocock's grilling skill](https://github.com/mattpocock/skills/blob/main/skills/productivity/grilling/SKILL.md), [Superpowers](https://github.com/obra/superpowers), [Emil Kowalski's skills](https://github.com/emilkowalski/skills), [ibelick ui-skills](https://github.com/ibelick/ui-skills), [Impeccable](https://github.com/pbakaus/impeccable), the [Double Diamond](https://www.designcouncil.org.uk/resources/the-double-diamond/), [GOV.UK prototyping guidance](https://www.gov.uk/service-manual/design/making-prototypes), [WCAG 2.2](https://www.w3.org/TR/WCAG22/), the [WAI-ARIA Authoring Practices](https://www.w3.org/WAI/ARIA/apg/patterns/), and [web.dev on motion](https://web.dev/articles/prefers-reduced-motion).

## License

Licensed under the [MIT License](LICENSE).

## 简体中文

Design with Checkpoints 是一个用于网站新建、界面改版和设计审查的前端设计 skill。AI 在三个检查点与你对齐想法，提出有明确主张的排版、字体与动效方案，并在交付前逐项检查每个布局和每个动效。

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
| 设计审查 | 按优先级列出问题、具体修改方案和严重程度，不改动代码 |
| 局部优化 | 定位并修改具体问题，复测相关功能 |

### 核心特点

- **三个检查点。** 确认需求复述；用真实内容的小样选择方向；先审阅一个代表性片段，再扩展到其他页面。
- **有主张的方案。** 每个方向都说明设计想法、具体的排版、字体与动效做法、代价和推荐理由。
- **排版检查。** 每个改动的页面都在手机和桌面宽度、中英文两种语言下，按具体的字体与间距规则检查，并排除常见的 AI 模板特征。
- **动效强度与动效清单。** 通过样例在克制、生动、华丽三档中选择动效强度。每个动效都列出用途、时长和减弱动效时的替代方式；方向检查、样例审阅和最终报告中都会给你看这份清单。
- **轻量。** 小改动直接修改；参考文件只在需要时读取。

### 文件导航

- [SKILL.md](skills/design-with-checkpoints/SKILL.md)：工作流程与检查点。
- [对齐](skills/design-with-checkpoints/references/alignment.md)：复述需求、提问、呈现方向、记录决策和界面文案。
- [排版与字体](skills/design-with-checkpoints/references/layout-and-type.md)：构图、网格、间距、中英文排版和排版检查。
- [动效](skills/design-with-checkpoints/references/motion.md)：动效用途、强度分档、技法、起点数值、减弱动效和动效清单。
- [验证](skills/design-with-checkpoints/references/verify.md)：基础审阅和交付报告。
- [回归用例](evals/cases.md)：修订 skill 时使用，不随 skill 安装。

### 致谢

工作方法参考了上方英文部分 [Acknowledgements](#acknowledgements) 中列出的项目与标准。

### 许可证

本项目采用 [MIT License](LICENSE)。
