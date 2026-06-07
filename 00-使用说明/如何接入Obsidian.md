# 如何接入 Obsidian

这份文档写给“懂一点 Git，但主要用 Obsidian 协作”的成员。

目标是让你完成下面这件事：

1. 把这个仓库克隆到本地
2. 用 Obsidian 打开成 vault
3. 安装并配置 `Obsidian Git`
4. 能完成日常 `pull -> 编辑 -> commit/push` 协作

## 先知道这几条

1. 平时主要在 `01-投稿箱/你的名字/` 下写内容。
2. 不要修改 `AGENTS.md`。
3. 不要把密码、token、SSH 私钥、公司隐私信息写进仓库。
4. `01-投稿箱/` 默认是未审材料，不是正式知识区。
5. 遇到冲突先不要硬覆盖，先保留现场再联系维护者。

## 仓库地址

当前仓库地址：

```text
https://github.com/BillyChen123/Billy_kb.git
```

如果后续仓库改成 private，只是认证方式会变化，本文的大部分步骤仍然一样。

## 首次接入总流程

### 第 1 步：安装 Git

Windows：

- 安装 Git for Windows
- 安装后在终端执行：

```bash
git --version
```

macOS：

- 任选一种：
  - 安装 Xcode Command Line Tools
  - 或通过 Homebrew 安装 Git
- 安装后执行：

```bash
git --version
```

如果这里没有版本号，先不要继续往下配 Obsidian。

### 第 2 步：确认 Git 身份

第一次在这台机器上用 Git 时，先确认用户名和邮箱：

```bash
git config --global user.name "你的名字"
git config --global user.email "你的邮箱"
```

检查：

```bash
git config --global --list
```

### 第 3 步：把仓库 clone 到本地

建议放到一个你长期不会随便移动的位置，例如：

- Windows：`D:\Obsidian\Billy_kb` 或 `C:\Users\你的用户名\Documents\Obsidian\Billy_kb`
- macOS：`~/Documents/Obsidian/Billy_kb`

克隆命令：

```bash
git clone https://github.com/BillyChen123/Billy_kb.git
```

如果你已经有这个文件夹，不要再 clone 到同一路径里。

### 第 4 步：用 Obsidian 打开 vault

1. 打开 Obsidian
2. 选择 `Open folder as vault`
3. 选中刚才 clone 下来的 `Billy_kb` 文件夹

打开后，你应该能看到仓库里的目录结构，例如：

- `00-使用说明`
- `01-投稿箱`
- `10-AI-Agent知识`
- `20-课题研究`
- `30-Skills-MCP-工具资源`

### 第 5 步：安装并启用 Obsidian Git

1. 打开 `设置 -> Community plugins`
2. 如果还没开社区插件，先启用
3. 进入 `Browse`
4. 搜索 `Git`
5. 安装 `Obsidian Git`
6. 安装后点击启用

启用后，左侧或命令面板里通常会出现 Git 相关命令。

### 第 6 步：配置 Obsidian Git

打开：

`设置 -> Community plugins -> Git`

建议先用下面这组配置。

#### 必配项

`Commit message`

```text
vault sync: {{date}}
```

`Auto commit message`

```text
vault sync: {{date}}
```

`Commit date format`

```text
YYYY-MM-DD HH:mm:ss
```

`Pull before push`

```text
开启
```

#### 推荐项

刚开始协作时，建议先以手动同步为主。

可以先保持下面这些自动项关闭或为 0：

- `Auto backup after file change`
- `Auto pull interval`
- `Auto push interval`

等你确认流程稳定后，再考虑：

- `Auto pull interval = 5`
- `Auto push interval = 5`

如果团队里经常多人同时编辑同一批文件，前期不建议把自动同步开得太激进。

### 第 7 步：做一次首次同步验证

先在仓库根目录确认状态：

```bash
git status
```

第一次建议用命令行验证一次，再回到 Obsidian 使用。

拉取远端：

```bash
git pull origin main
```

然后随便新建一条测试笔记，例如在 `01-投稿箱/你的名字/` 下写一个测试文件，再执行：

```bash
git add .
git commit -m "test: verify obsidian collaboration"
git push origin main
```

如果命令行能通，再用 Obsidian Git 做日常同步，心里会更有底。

## 日常协作流程

推荐日常流程固定成下面这样：

1. 打开 Obsidian 前，先 `pull`
2. 编辑你的笔记
3. 提交并推送
4. 确认远端成功

### 方式 A：命令行

进入仓库目录后：

```bash
git pull origin main
git status
```

编辑完成后：

```bash
git add .
git commit -m "notes: update personal draft"
git push origin main
```

### 方式 B：Obsidian Git

在 Obsidian 里：

1. 打开命令面板
2. 先执行 `Git: Pull`
3. 编辑内容
4. 执行 `Git: Commit all changes`
5. 执行 `Git: Push`

如果你已经开启自动同步，仍然建议在重要修改前手动 `Pull` 一次。

## 建议的写作位置

### 普通成员默认写这里

```text
01-投稿箱/你的名字/
```

例如：

```text
01-投稿箱/张三/
01-投稿箱/Billy/
```

### 不建议直接改这些区域

- `AGENTS.md`
- 你不熟悉的正式知识文档
- 别人的投稿目录

### 正式知识区

下面这些目录默认是正式知识区：

- `10-AI-Agent知识/`
- `20-课题研究/`
- `30-Skills-MCP-工具资源/`

如果你要改正式知识区，先确认自己是在整理、修订，而不是随手覆盖别人的内容。

## Windows 操作说明

### 安装建议

推荐使用：

- Git for Windows
- Obsidian Desktop

### 常用终端

任选一种：

- PowerShell
- Windows Terminal
- Git Bash

如果你使用代理软件，请确认它已经真的启动，不只是开了配置。

### 典型路径

```text
C:\Users\你的用户名\Documents\Obsidian\Billy_kb
```

或

```text
D:\Obsidian\Billy_kb
```

### Windows 常见注意点

1. 不要把仓库放进会自动同步的网盘目录里，再叠加 Git 同步，容易出冲突。
2. 文件夹路径不要太深。
3. 如果命令行提示认证，优先使用 Git Credential Manager 完成 GitHub 登录。

## macOS 操作说明

### 安装建议

推荐使用：

- Obsidian Desktop
- Git
- iTerm2 或系统终端

如果没装 Git，可以先执行：

```bash
git --version
```

系统通常会引导你安装开发工具。

如果你用 Homebrew，也可以：

```bash
brew install git
```

### 典型路径

```text
~/Documents/Obsidian/Billy_kb
```

### macOS 常见注意点

1. 第一次调用 Git 时，系统可能要求安装命令行工具。
2. 如果你使用代理工具，确认它对终端也生效，而不是只对浏览器生效。
3. 如果 Obsidian 没有读写权限，去系统隐私权限里检查。

## 认证说明

### 仓库是 public 时

只读操作通常不需要认证，但 `push` 仍然需要 GitHub 身份认证。

### 仓库改成 private 后

最常见的情况是：

- `clone` 需要登录
- `pull/push` 需要登录

推荐使用 GitHub 官方登录流程，或 Git Credential Manager 弹出的网页登录。

如果你被要求输入用户名和密码，不要再用 GitHub 账号密码硬试。GitHub 现在通常需要：

- 浏览器 OAuth 登录
- 或 Personal Access Token

## 常见问题

### 1. `git push` 报连不上 GitHub

先看报错里有没有这种字样：

```text
via 127.0.0.1
```

如果有，通常说明 Git 正在走本地代理。

检查代理配置：

```bash
git config --global --get-regexp "^(http|https)\\..*proxy$|^http\\.proxy$|^https\\.proxy$"
```

如果你确实要走代理，确认代理软件已经启动，并且端口真的在监听。  
如果你不需要代理，可以移除：

```bash
git config --global --unset http.proxy
git config --global --unset https.proxy
```

### 2. `git push` 报认证失败

一般是凭据没配好，不是仓库坏了。

先确认：

- 你对这个仓库有写权限
- 当前 GitHub 账号登录正确
- 凭据没有过期

### 3. `git pull` 后出现冲突

先不要直接删除冲突标记。

建议流程：

1. 先执行 `git status`
2. 看哪些文件冲突
3. 保留现场
4. 联系维护者一起处理

如果你明确知道怎么解冲突，再改；如果不确定，不要硬合。

### 4. Obsidian Git 没反应

按顺序检查：

1. Git 是否安装成功
2. 当前 vault 是否真的是一个 Git 仓库
3. 社区插件是否已启用
4. `Obsidian Git` 是否已安装并开启

仓库根目录里应当能看到 `.git/`。

### 5. 自动同步看起来“不稳定”

这通常不是插件坏了，而是多人协作下自动 `pull/push` 太频繁。

处理方式：

- 先改回手动同步
- 固定成 `pull -> 编辑 -> commit -> push`
- 确认稳定后再考虑开自动

## 推荐的最小工作流

如果你不想记太多，至少记住这套：

1. 打开库前先 `pull`
2. 主要在 `01-投稿箱/你的名字/` 写
3. 写完就 `commit + push`
4. 有冲突先停，不硬覆盖

这已经足够支持大部分日常协作。
