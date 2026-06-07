# Billy_kb

这是一个 AI-native 的 Obsidian 协作知识库。

核心规则、目录结构、Agent 读写协议都在 [AGENTS.md](./AGENTS.md)。人和 Agent 都应该先读它。

## 快速开始

人类成员：

1. 接入 Obsidian：读 [00-使用说明/如何接入Obsidian.md](./00-%E4%BD%BF%E7%94%A8%E8%AF%B4%E6%98%8E/%E5%A6%82%E4%BD%95%E6%8E%A5%E5%85%A5Obsidian.md)。
2. 不知道放哪的内容，先放 `01-收件箱/`。
3. 推进课题时，让 Agent 进入 `10-项目/项目名/` 并同步 `memory.md`。
4. 不要把密码、token、私钥、cookie、公司隐私信息写进仓库。

Agent：

1. 必须先读 [AGENTS.md](./AGENTS.md)。
2. 处理项目时，必须先读该项目的 `README.md` 和 `memory.md`。
3. 每次实质推进后，判断是否需要运行 `/sync_memory`。

## 目录

```text
00-使用说明/      接入、同步、协作说明
01-收件箱/        临时输入、粗糙笔记、待整理材料
10-项目/          按课题或项目聚合当前工作和历史经验
20-主题库/        跨项目复用的主题知识
30-模板/          给 Agent 生成高质量文档用的轻模板
90-归档/          过期、废弃、历史材料
docs/             仓库设计和维护记录
```

这个仓库的重点不是让人手动维护一套复杂 wiki，而是让 Agent 在工作过程中自动沉淀 memory、lesson 和可复用知识。
