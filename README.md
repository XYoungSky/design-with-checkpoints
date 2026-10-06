# Design with Checkpoints

[English](#design-with-checkpoints) · [简体中文](#简体中文)

A frontend design skill that guides research, direction selection, prototyping, implementation, and verification, with user input at key decisions.

Use it for new websites, redesigns, interface reviews, and focused improvements. The workflow scales to the task and follows the project's existing stack and design conventions.

## Installation

### Using the skills CLI

Requires Node.js and npm. Run from your project directory:

```bash
npx skills@latest add XYoungSky/design-with-checkpoints --skill design-with-checkpoints
```

Select your target agent in the installer. Add `--global` to install across projects, or `--agent codex` / `--agent claude-code` to choose an agent directly. See the [skills CLI documentation](https://github.com/vercel-labs/skills#install-a-skill) for other supported agents and options.

### Manual installation

Download and extract the repository, then place its contents in a folder named `design-with-checkpoints` at one of these locations:

| Agent | This project | All your projects |
| --- | --- | --- |
| [Codex](https://developers.openai.com/codex/skills#where-to-save-skills) | `.agents/skills/design-with-checkpoints/` | `~/.agents/skills/design-with-checkpoints/` |
| [Claude Code](https://code.claude.com/docs/en/skills#choose-where-skills-load) | `.claude/skills/design-with-checkpoints/` | `~/.claude/skills/design-with-checkpoints/` |

Keep `SKILL.md`, `references/`, and `agents/` together, with `SKILL.md` directly inside that folder. No build step is required. Open or reload your agent and confirm the skill is available.

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

Preview, testing, and deployment capabilities come from your agent and project tools.

## When to use it

| Task | Approach |
| --- | --- |
| New website | Establish goals, content, and direction; test uncertain choices and build incrementally |
| Redesign | Audit the existing interface, identify what to preserve, and propose improvements |
| Plan or review only | Deliver recommendations, supporting evidence, and open checks; stop there |
| Focused fix | Reproduce, change, and retest while preserving the existing direction |

## How collaboration works

Inspect the relevant interface, complete a verifiable batch, check its effects, and use feedback to guide the next step. Research, comparisons, prototypes, and separate specifications are used when the task needs them.

- **Ask at meaningful decisions.** Discuss navigation, core flows, or changes in direction. Handle spacing, type sizes, and similar details within the chosen direction.
- **Respect delegation.** Let the agent choose a direction, or ask to review a sample first. Preserve settled decisions and revisit them only when relevant conditions change.
- **Verify the result.** Check real content, responsive layouts, interactions, and accessibility. Distinguish verified results from untested behavior.
- **Follow the project.** UI language follows your explicit instructions, then project language and audience requirements, with the conversation language as a fallback.

Set your preferred involvement in ordinary language:

```text
Show me two distinct directions. Start implementation after I choose one.
```

```text
Keep the current design. Choose the details yourself;
ask me only if the scope changes.
```

```text
Build the homepage's first screen and a mobile sample.
Wait for my review before expanding to the rest of the site.
```

Delivery explains what changed, what was tested, and what remains unverified. Publishing follows existing authorization and the tool's permission requirements.

## Files

- [SKILL.md](SKILL.md): agent instructions and workflow.
- [Interview and decisions](references/interview-and-decisions.md): options, decision records, and feedback.
- [Reference evidence](references/reference-evidence.md): research, prototype comparisons, and evidence quality.
- [Motion and QA](references/motion-and-qa.md): interaction, responsive behavior, accessibility, and performance checks.
- [Project templates](references/project-templates.md): briefs, specifications, handoffs, and regression scenarios.
- [Sources and evidence limits](references/sources.md): method sources and their applicability.

## License

Licensed under the [MIT License](LICENSE).

## 简体中文

一个面向前端设计的 skill，涵盖调研、方向选择、原型、实现与验证，让用户参与关键决策。

适用于网站新建、改版、界面审查和局部优化。根据任务大小调整流程，沿用项目已有的技术栈和设计约定。

### 安装

#### 使用 skills CLI

需要 Node.js 和 npm。在项目目录中运行：

```bash
npx skills@latest add XYoungSky/design-with-checkpoints --skill design-with-checkpoints
```

按提示选择目标 agent。添加 `--global` 可跨项目使用；添加 `--agent codex` 或 `--agent claude-code` 可直接指定 agent。其他支持的工具与选项见 [skills CLI 文档](https://github.com/vercel-labs/skills#install-a-skill)。

#### 手动安装

下载并解压仓库，将内容放入名为 `design-with-checkpoints` 的文件夹，选择以下一个位置：

| Agent | 当前项目 | 所有项目 |
| --- | --- | --- |
| [Codex](https://developers.openai.com/codex/skills#where-to-save-skills) | `.agents/skills/design-with-checkpoints/` | `~/.agents/skills/design-with-checkpoints/` |
| [Claude Code](https://code.claude.com/docs/en/skills#choose-where-skills-load) | `.claude/skills/design-with-checkpoints/` | `~/.claude/skills/design-with-checkpoints/` |

完整保留 `SKILL.md`、`references/` 和 `agents/`，确保 `SKILL.md` 直接位于该文件夹中。无需构建。打开或重新加载 agent，确认它能识别此 skill。

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

实际预览、测试和发布能力由所用 agent 与项目工具提供。

### 适合哪些任务

| 任务 | 工作方式 |
| --- | --- |
| 新建网站 | 明确目标、内容与方向，验证不确定的选择后逐步实现 |
| 改版现有页面 | 先审查，识别值得保留的设计，再提出改进 |
| 只要方案或审查 | 交付建议、依据和待验证项，到此结束 |
| 局部修复 | 定位问题、修改、复测，保持已有方向 |

### 如何协作

检查相关界面，完成一批可验证的工作，检查影响，再根据反馈决定下一步。调研、方案比较、原型和独立规格文档按任务需要使用。

- **关键选择再提问。** 导航结构、核心流程或方向变化需要讨论；已选方向内的间距、字号等细节通常直接处理。
- **尊重你的委托。** 可以让 agent 自行选择方向，也可以指定“先给我看样例”。已有决定会被保留，只有相关条件变化时才重新讨论。
- **用结果验证。** 检查真实内容、响应式布局、交互和可访问性；区分已验证结果与待验证内容。
- **保持项目一致性。** 界面语言优先遵循你的指定，其次是项目语言与受众要求，最后才以聊天语言作为默认值。

你可以这样约定参与方式：

```text
先给我两个有明显区别的方向，我选定后再实现。
```

```text
沿用当前设计，细节由你决定；只有范围变化时再问我。
```

```text
先完成首页第一屏和移动端样例，等我确认后再扩展。
```

交付会说明改了什么、验证了什么，以及尚未确认的部分。发布遵循已有授权和当前工具的权限要求。

### 文件导航

- [SKILL.md](SKILL.md)：agent 的入口规则与工作流程。
- [提问与决策](references/interview-and-decisions.md)：如何提出选项、记录选择和处理反馈。
- [参考与证据](references/reference-evidence.md)：如何研究案例、比较原型和判断证据。
- [动效与质量检查](references/motion-and-qa.md)：交互、响应式、可访问性与性能检查。
- [项目模板](references/project-templates.md)：简报、设计规格、交付记录和回归场景。
- [来源与适用边界](references/sources.md)：方法来源及其使用限制。

### 许可证

本项目采用 [MIT License](LICENSE)。
