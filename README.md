# neat-freak

> 跨平台 Agent Skill — 会话结束后对项目文档和记忆进行洁癖级审查与同步。

## 简介

`neat-freak` 是一个跨平台 Agent Skill，遵循开放 Agent Skill 规范，可在 Claude Code / OpenAI Codex / OpenCode / OpenClaw 通用。

它把你当成**知识库编辑**而不是记录员：审查全局、合并重复、修正过期、删除废弃，让整个项目的文档（CLAUDE.md / README.md / docs/）和 Agent 记忆始终与代码保持一致。

## 触发

会话中出现下列措辞时自动触发：

- `sync up` / `tidy up docs` / `update memory` / `clean up docs`
- `/sync` / `/neat`
- `同步一下` / `整理文档` / `整理一下` / `更新记忆` / `梳理一下` / `收尾` / `这个阶段做完了` / `新人能直接上手`

## 安装

放进对应 Agent 的 skills 目录即可：

| 平台 | 路径 |
|------|------|
| Claude Code | `~/.claude/skills/neat-freak/` |
| OpenAI Codex | `~/.codex/skills/neat-freak/` |
| OpenClaw | `~/.openclaw/skills/neat-freak/` |
| OpenCode | 直接复用上面 Claude Code / Codex 的目录，无需另装 |

```bash
git clone https://github.com/jiangwanyutao/neat-freak.git ~/.claude/skills/neat-freak
```

详细路径与同步矩阵见 `references/agent-paths.md` 与 `references/sync-matrix.md`。

## 边界

- **整份文件的删除一定会先问你**；文件内部的过期段落由 skill 自行改写删除。
- 全局配置（`~/.claude/CLAUDE.md` 等）只在你明确提出跨项目原则时才动。

## 目录

```
.
├── SKILL.md                    # Skill 主体（含触发规则与执行流程）
├── README.md                   # 本文件
├── LICENSE                     # MIT
└── references/
    ├── agent-paths.md          # 各平台记忆与 skills 目录路径
    └── sync-matrix.md          # 跨 Agent 知识同步矩阵
```

## License

MIT，见 [LICENSE](LICENSE)。
