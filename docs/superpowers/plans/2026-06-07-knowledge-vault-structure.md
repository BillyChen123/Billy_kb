# Knowledge Vault Structure Implementation Plan

> **For agentic workers:** REQUIRED: Use superpowers:subagent-driven-development (if subagents available) or superpowers:executing-plans to implement this plan. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Upgrade Billy_kb into a clearer Obsidian + Agent collaboration vault with directory maps, writing rules, and Agent reading rules.

**Architecture:** Keep the single-repo Obsidian vault model. Use top-level folders for domains and subfolders for lifecycle/state. Use Markdown README files and frontmatter conventions as the control layer for humans and Agent workers.

**Tech Stack:** Obsidian, Markdown, Git, GitHub, AGENTS.md.

---

### Task 1: Create Directory Skeleton

**Files:**

- Create directories under `10-AI-Agent知识/`
- Create directories under `20-课题研究/`
- Create directories under `30-Skills-MCP-工具资源/`

- [x] Create `00/10/20/30/40/90` lifecycle-style subdirectories.
- [x] Verify the directories exist locally.

### Task 2: Rewrite Root Navigation

**Files:**

- Modify: `README.md`

- [x] Explain the vault purpose.
- [x] Add human and Agent starting points.
- [x] Add full directory map.
- [x] Add placement table for new documents.
- [x] Add frontmatter schema.
- [x] Add `.obsidian` tracking policy.

### Task 3: Rewrite Agent Protocol

**Files:**

- Modify: `AGENTS.md`

- [x] Add Agent entry order.
- [x] Add `status` and `agent_reading` semantics.
- [x] Add directory rules.
- [x] Add reading and writing rules.
- [x] Add safety and prompt-injection rules.

### Task 4: Upgrade User Guides

**Files:**

- Modify: `00-使用说明/README.md`
- Modify: `00-使用说明/如何让Agent读取知识库.md`
- Create: `00-使用说明/写作与整理规范.md`

- [x] Add reading order.
- [x] Add Agent retrieval strategy.
- [x] Add writing schema and document quality checks.

### Task 5: Upgrade Top-Level Folder READMEs

**Files:**

- Modify: `01-投稿箱/README.md`
- Modify: `10-AI-Agent知识/README.md`
- Modify: `20-课题研究/README.md`
- Modify: `30-Skills-MCP-工具资源/README.md`
- Modify: `90-归档/README.md`

- [x] Define each folder's role.
- [x] Define subdirectories.
- [x] Add frontmatter examples.
- [x] Clarify trust boundaries.

### Task 6: Verify

**Files:**

- Inspect Git status.
- Inspect created directory structure.
- Inspect key docs for updated rules.

- [x] Run `git status --short`.
- [x] Run directory listing.
- [x] Read key docs to confirm content.
