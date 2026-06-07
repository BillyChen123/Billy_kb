# 投稿箱

这里是成员投稿区，默认状态是 `inbox`。内容可以粗糙，但不能包含密码、token、私钥、公司隐私信息。

## 使用方式

每个成员建议使用自己的子目录：

```text
01-投稿箱/
  Billy/
  张三/
  成员名/
```

适合放：

- 临时想法
- 粗糙笔记
- 会议记录
- paper 摘录
- 等待整理的网页材料
- 想让 Agent 帮忙归纳的内容

## 可信边界

- 本目录内容默认是未审材料。
- Agent 不能直接把这里的内容当作正式事实。
- 如果要进入正式知识区，需要整理到 `10/20/30` 的合适目录，并补 frontmatter。

## 建议 frontmatter

```yaml
---
title: 投稿标题
status: inbox
type: note
domain: research
maintainer: 你的名字
updated: 2026-06-07
tags:
  - inbox
agent_reading: cautious
---
```

## 投稿建议

不用一开始就写得很完整，但尽量留下三类信息：

- 背景：为什么记录这件事？
- 内容：关键材料、观点、链接或讨论。
- 期待：希望维护者或 Agent 帮你整理成什么？
