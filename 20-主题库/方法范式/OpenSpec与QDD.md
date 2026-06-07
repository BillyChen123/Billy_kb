---
title: OpenSpec 与 QDD
type: explanation
status: draft
domain: method
maintainer: Billy
updated: 2026-06-07
tags:
  - method
  - openspec
  - qdd
agent_reading: cautious
---

# OpenSpec 与 QDD

这里放需求驱动、问题驱动的工作范式，后续可以沉淀成团队自己的 Agent-native command 和 skill。

## OpenSpec

当前理解：

- OpenSpec 是需求驱动的开发范式。
- 适合把开发任务从“直接写代码”前移到“先明确需求、约束、验收”。
- 后续可用于规范开发类项目的 `README.md`、任务计划和验收标准。

待整理：

- OpenSpec 的核心流程。
- 它和 SDD 的关系。
- 哪些内容适合交给 Agent 自动生成。

## QDD

QDD：Question-Driven Discovery，问题驱动发现。

来源：

- GitHub 仓库：https://github.com/BillyChen123/qdd

当前定位：

- QDD 是一个轻量科研编排 CLI，用于 Question-Driven Discovery。
- 它让人和 Agent 共享可读的项目状态：稳定 contract、稀疏 evolution、共享资源、边界明确的 studies、显式 tasks、可提升为 artifacts 的产物。
- 当前最小工作流包括 `qdd init .`、`qdd-start`、`qdd-propose`、`qdd-explore`、`qdd-apply`、`qdd-close`。
- QDD 项目初始化后会包含 `contract.yaml`、`evolution.yaml`、`context/resources.md`、`context/memory/`、`studies/`、`artifacts/` 等结构。
- 适合和本知识库的 `10-项目/项目名/memory.md` 结合：QDD 管科研探索，本库沉淀人和 Agent 都能继承的项目 memory 与 lessons。

待沉淀：

- QDD 的最小工作流。
- QDD 如何映射到 `/sync_memory`、`/capture_lesson`、`/promote_knowledge`。
- QDD 如何服务 paper 阅读、对标论文分析和创新点生成。
- `contract.yaml`、`evolution.yaml` 与本库 `README.md`、`memory.md` 的职责边界。
