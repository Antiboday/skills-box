# skills-box

个人技能箱：经过通用性验证的 AI agent 技能（SKILL.md 格式），可被 Claude Code / ZCode / DSH / Codex 等 agent 宿主直接使用。

## 内容与来源

来自 [mattpocock/skills](https://github.com/mattpocock/skills) @ `5beb35b`（MIT 许可）。原仓库 38 个技能中，经验证 **36 个为工具无关的通用技能**，已拍平为 `skills/<名称>/` 布局（去掉 engineering/productivity 等分类层级，宿主直接扫描即可发现）。

排除 2 个 Claude 专属技能：

| 排除项 | 原因 |
|---|---|
| `claude-handoff` | 正文硬编码 `claude --bg` 后台代理命令 |
| `git-guardrails-claude-code` | 依赖 Claude Code PreToolUse hooks（写 `.claude/settings.json`） |

## 技能清单（36）

- **工程（20）**：tdd, code-review, diagnosing-bugs, codebase-design, domain-modeling, research, prototype, wizard, setup-matt-pocock-skills, ask-matt, grill-with-docs, to-spec, to-tickets, implement, implement-spec, wayfinder, triage, improve-codebase-architecture, retro, pr
- **效率（7）**：grill-me, grilling, handoff, teach, to-questionnaire, wait-what, writing-for-agents
- **实验中（6）**：chief-of-staff, loop-me, setup-ts-deep-modules, writing-beats, writing-fragments, writing-shape
- **杂项（3）**：setup-pre-commit, scaffold-exercises, migrate-to-shoehorn

## 使用

- **ZCode**：拷入 `~\.zcode\skills\`（全局）或 `<repo>\.zcode\skills\`（单仓库）
- **DSH**：拷入 `~\.dsh\skills\`
- **skills.sh 通用安装器**：本仓库为私有，`npx skills add` 需要认证，建议 `git clone` 后本地拷贝
- 每个新仓库首次使用前跑一次 `setup-matt-pocock-skills`（配置 issue tracker、triage 标签、领域文档布局；其余工程技能依赖它的产出）
- 技能间存在互调（如 `implement-spec` 引用 `/to-spec`、`/to-tickets`），建议整包使用，不要拆单

## 许可

技能内容来自上游 mattpocock/skills，MIT 许可，见 [LICENSE](LICENSE)，版权归上游作者所有。
