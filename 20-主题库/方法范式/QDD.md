---
title: QDD
type: explanation
status: draft
domain: method
maintainer: Billy
updated: 2026-06-07
tags:
  - method
  - qdd
  - research
  - question-driven-discovery
agent_reading: cautious
---

# QDD

GitHub：

- https://github.com/BillyChen123/qdd

## 一句话定位

QDD 是 Question-Driven Discovery，问题驱动发现。它是一个轻量科研编排 CLI，用来让人和 Agent 在科研探索中共享项目状态、研究边界、资源、study 记忆和可提升的 artifacts。

它解决的问题不是“快速写一篇论文”，而是“让科研探索过程可追踪、可恢复、可复利”。

## 它为什么重要

科研探索和普通开发不一样。很多时候我们并不知道最后要实现什么，只知道当前有一个问题、一个假设、一些线索和一堆不确定边界。

如果只靠聊天推进，下一轮 Agent 很容易忘记：

- 当前真正的问题是什么。
- 哪些方向已经试过。
- 哪些路线被证明不好走。
- 哪些材料是关键证据。
- 哪些产物已经可以提升为 artifact。

QDD 把这些状态放进项目结构里，让探索过程变成可读、可继续、可审计的工作流。

## 核心工作流

QDD README 中的最小流程：

```text
qdd init .
qdd-start
qdd-propose
qdd-explore
qdd-apply
qdd-close
```

这些命令对应的含义可以理解为：

- `qdd init .`：初始化科研探索项目。
- `qdd-start`：开始或恢复当前探索上下文。
- `qdd-propose`：提出可探索的问题、边界或 study。
- `qdd-explore`：围绕问题展开探索。
- `qdd-apply`：把探索中的有效结果应用到项目产物。
- `qdd-close`：关闭 study，并沉淀记忆。

## 项目结构

QDD 初始化后，项目大致结构是：

```text
project-root/
  contract.yaml
  evolution.yaml
  research-map.html
  context/
    resources.md
    memory/
  studies/
  artifacts/
    index.yaml
    data/
    code/
    figures/
    reports/
  .qdd/
```

关键文件：

- `contract.yaml`：稳定项目契约，记录主题、范围和模式。
- `evolution.yaml`：稀疏 study 历史，以及当前开放/已解决边界。
- `context/resources.md`：长期共享资源。
- `context/memory/STUDY-XXX.md`：study 关闭时写入的局部记忆。
- `research-map.html`：派生可视化，不是真实来源。
- `artifacts/`：被提升出来的数据、代码、图和报告。

## 适合什么任务

适合：

- 科研选题探索。
- paper reading 后的创新点生成。
- 多轮实验和分析。
- 单细胞、生信、医学 AI 等需要持续积累上下文的课题。
- 需要记录“哪些路走不通”的探索。

不适合：

- 已经完全明确需求的软件功能开发。
- 一次性问答。
- 不需要长期记忆的临时分析。

## 和本知识库的关系

QDD 管的是科研探索项目内部的执行结构。Billy_kb 管的是团队长期知识复利。

建议映射：

```text
QDD contract.yaml              -> 项目稳定边界
QDD evolution.yaml             -> study 历史和开放问题
QDD context/resources.md        -> 项目资源
QDD context/memory/STUDY.md     -> 单个 study 的关闭记忆
Billy_kb 10-项目/项目名/memory.md -> 给下一轮 Agent 必读的当前态势摘要
Billy_kb lessons/              -> 跨轮次复用的经验和失败路线
```

也就是说，QDD 可以比 Billy_kb 更“研究执行态”；Billy_kb 的 `memory.md` 应该更像当前态势摘要，不要复制所有 QDD 细节。

## 和 OpenSpec 的区别

QDD 是问题驱动，不是需求驱动。

OpenSpec 在开始前尽量明确“要做什么”；QDD 允许你承认“不知道答案”，然后通过一个个 study 把问题边界收窄。

简单说：

```text
OpenSpec：先定义需求，再实现。
QDD：先定义问题，再探索。
```

## 待沉淀

- QDD 在真实课题里的最小实践样例。
- QDD 和 `memory.md` 的同步规则。
- QDD 和 `/capture_lesson` 的连接方式。
- 哪些 QDD artifacts 值得提升到 Billy_kb 的主题库。
