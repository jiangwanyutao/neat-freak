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
| OpenAI Codex / OpenCode / OpenClaw | 参考各自的 skills 目录约定 |

详细路径与同步矩阵见 `references/agent-paths.md` 与 `references/sync-matrix.md`。

## 目录

```
.
├── SKILL.md                    # Skill 主体（含触发规则与执行流程）
├── README.md                   # 本文件
└── references/
    ├── agent-paths.md          # 各平台 skills 目录路径
    └── sync-matrix.md          # 跨 Agent 知识同步矩阵
```

## License

按使用方约定。
