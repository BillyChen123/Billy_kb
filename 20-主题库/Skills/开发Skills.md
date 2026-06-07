---
title: 开发 Skills
type: reference
status: draft
domain: skills
maintainer: Billy
updated: 2026-06-07
tags:
  - skills
  - development
agent_reading: cautious
---

# 开发 Skills

这里放面向开发、产品、前端、视频和工程流程的 skills。

## Superpowers

GitHub：

- https://github.com/obra/superpowers

它有什么用：

- 给 coding agent 加一套工程方法论和可组合 skills。
- 典型流程包括头脑风暴、设计确认、实施计划、TDD、代码审查、系统化调试等。
- 适合把“直接让 Agent 写代码”变成“先澄清目标、写计划、再执行和验收”。

适合场景：

- 复杂功能设计。
- 需要先讨论再实现的任务。
- 需要强制 Agent 不跳过计划、测试和 review 的开发流程。

在本库中的定位：

- 作为开发类 Agent 协作的底层范式参考。
- 可以和 OpenSpec 配合：Superpowers 管协作流程，OpenSpec 管规格和变更 artifact。

## ui-ux-pro-max

GitHub：

- https://github.com/nextlevelbuilder/ui-ux-pro-max-skill

它有什么用：

- 给 Agent 提供 UI/UX 设计智能层。
- 包含 UI 风格、配色、字体、UX 规则、图表类型、技术栈建议等可检索知识。
- 适合在前端页面、组件、dashboard、landing page、SaaS、移动端等设计任务中使用。

适合场景：

- 生成前端设计系统。
- 审查页面是否专业、可用、响应式、可访问。
- 给 Agent 生成 `design.md` 作为前端实现前的设计约束。

在本库中的定位：

- 开发类前端设计 skill。
- 后续可以沉淀团队自己的 `design.md` 模板和 UI 验收清单。

## Remotion

GitHub：

- https://github.com/remotion-dev/skills
- Skill 文件：https://github.com/remotion-dev/skills/blob/main/skills/remotion/SKILL.md

它有什么用：

- 给 Agent 提供 Remotion 视频生成的领域知识。
- Remotion 本身是用 React 编程式生成视频的框架。
- skill 覆盖动画、素材、音频、字幕、composition、timing、transition、Tailwind、charts、3D 等规则。

适合场景：

- 产品介绍视频。
- 组会或项目展示中的动态解释视频。
- 可复现的 motion graphics。
- 从已有网页、dashboard 或科研结果生成短视频说明。

在本库中的定位：

- 开发类视频制作 skill。
- 后续可以沉淀视频项目模板、分镜结构、渲染排错经验。
