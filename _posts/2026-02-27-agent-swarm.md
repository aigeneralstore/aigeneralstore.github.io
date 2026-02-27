---
layout: post
title: "Agent Swarm 实战：用 OpenClaw 编排 AI 开发团队"
date: 2026-02-27
categories: [AI, 自动化]
tags: [openclaw, agent, automation, github]
---

最近搭建了基于 [Elvis 的 Agent Swarm 架构](https://x.com/elvissun/status/2025920521871716562)，用 OpenClaw 作为编排层，让 Codex 和 Claude Code 协同工作。

## 为什么需要 Agent Swarm？

直接用 Codex 或 Claude Code 的问题：

1. **上下文有限** - 它们只看到代码，不了解业务背景
2. **单线程** - 一次只能处理一个任务
3. **缺乏记忆** - 每次对话都从零开始

解决方案：用一个"编排者"（OpenClaw）来管理多个 coding agents。

## 架构

```
┌─────────────────────────────────────┐
│         OpenClaw (编排者)            │
│  - 持有业务上下文                     │
│  - 分配任务给 agents                 │
│  - 监控进度，Telegram 通知            │
└──────────────┬──────────────────────┘
               │
     ┌─────────┼─────────┐
     ▼         ▼         ▼
  Agent 1   Agent 2   Agent 3
  (codex)   (claude)  (gemini)
```

每个 agent 有独立的 worktree，互不干扰。

## 核心组件

```bash
.clawdbot/
├── active-tasks.json    # 任务注册表
├── spawn-agent.sh       # 启动脚本
├── check-agents.sh      # 监控脚本 (cron)
└── agent-swarm.js       # Node.js 辅助工具
```

## 效果

- **94 commits in one day** - 个人最高记录
- **7 PRs in 30 minutes** - 从想法到上线
- **自动 code review** - Codex + Gemini + Claude 三重审查

## 下一步

- 配置 Sentry 自动修复 bug
- 接入会议笔记，自动提取 feature request
- 尝试更多 agent 并行

---

完整代码在我的 [workspace](https://github.com/aigeneralstore) 里，欢迎参考！
