---
title: OpenSpec
type: explanation
status: draft
domain: method
maintainer: Billy
updated: 2026-06-07
tags:
  - method
  - openspec
  - sdd
  - spec-driven-development
agent_reading: cautious
---

# OpenSpec

GitHub：

- https://github.com/Fission-AI/OpenSpec

官网：

- https://openspec.dev/

## 一句话定位

OpenSpec 是面向 AI coding assistants 的 Spec-Driven Development 范式：先把“要改什么、为什么改、验收什么”写成可审查的规格，再让 Agent 实现。

它解决的问题不是“让 Agent 更会写代码”，而是“让人和 Agent 在写代码前先对齐意图”。

## 它为什么重要

AI 写代码最大的问题之一是需求常常只存在聊天上下文里。聊天上下文会漂移，也不方便审查。OpenSpec 把需求、设计、任务拆成文件，让一次变更变成可读、可追踪、可验证的 artifact。

OpenSpec 的价值在于：

- 把用户意图从聊天里拉出来。
- 让每次变更都有 proposal、spec、design、tasks。
- 让代码实现前先通过规格对齐。
- 让 reviewer 可以审查“变更意图”，而不是只审查代码 diff。
- 让项目长期留下可追踪的需求历史。

## 核心工作流

OpenSpec 的典型流程：

```text
/opsx:propose  提出变更，生成 proposal/spec/design/tasks
/opsx:apply    按任务实现
/opsx:archive  完成后归档变更，并更新 specs
```

项目中通常会出现：

```text
openspec/
  specs/                 # 当前系统规格
  changes/               # 进行中的变更
    add-dark-mode/
      proposal.md
      design.md
      tasks.md
      specs/
```

## 适合什么任务

适合：

- 软件功能开发。
- 复杂重构。
- 多文件、多模块改动。
- 需要人审查需求和验收标准的任务。
- 需要避免 Agent “边想边写、越写越偏”的任务。

不适合：

- 一两行小修。
- 临时探索性问题。
- 还没有明确目标的科研探索。
- 纯知识整理任务。

## 和本知识库的关系

OpenSpec 更适合管理“开发项目的变更”。Billy_kb 更适合沉淀“项目记忆和可复用经验”。

建议映射：

```text
OpenSpec proposal/design/tasks  -> 开发项目的变更计划
Billy_kb project memory.md      -> 项目当前状态和关键判断
Billy_kb lessons/               -> 做完之后沉淀的经验
20-主题库/方法范式/OpenSpec.md    -> OpenSpec 方法本身的解释
```

如果一个开发项目使用 OpenSpec，同时也在 Billy_kb 里建项目，那么 Agent 应该：

1. 先读 `10-项目/项目名/memory.md` 理解当前状态。
2. 再读项目里的 `openspec/` 理解当前变更规格。
3. 完成实质推进后，同步 `memory.md`。
4. 做完后用 `/capture_lesson` 沉淀 OpenSpec 使用经验。

## 和 QDD 的区别

OpenSpec 适合“要把一个系统改成什么样”。它关注需求、设计、任务和实现。

QDD 适合“科研探索中下一步应该问什么”。它关注问题、边界、study、artifact 和探索记忆。

简单说：

```text
OpenSpec：需求驱动开发
QDD：问题驱动科研探索
```

## 待沉淀

- OpenSpec 在 Codex / Claude Code 中的实际使用步骤。
- OpenSpec 和本库 `/sync_memory` 的配合方式。
- OpenSpec 变更完成后如何自动生成 lesson。
- 一个真实开发项目的 OpenSpec 示例。
