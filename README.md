<div align="center">

# Echo@55

**独立开发者 · 把 AI 的能力落到本机**

MCP Server ｜ 桌面工具 ｜ 自动化流水线

<img src="https://img.shields.io/badge/focus-AI%20Agent%20tooling-8957e5?style=flat-square" />
<img src="https://img.shields.io/badge/platform-Windows%20%2F%20Web-1f6feb?style=flat-square" />
<img src="https://img.shields.io/badge/license-MIT%20%2F%20Apache--2.0-2ea44f?style=flat-square" />

</div>

---

我不太写「又一个 demo」。更在意一件事能不能在自己机器上天天跑：AI 要能真的执行命令、桌面工具断网也要能用、重复点 20 次的操作应该收成一条命令。

### 在做的事

- **给 Agent 装上手脚** — 用 MCP 把真实系统的能力接进去，而不只是聊天
- **本地优先的工具** — 数据留在本机，密钥本地加密，不做云端依赖
- **把流程变成命令** — 手工流程 → 可复用脚本 → 可分发 CLI

---

### 精选项目

#### [ssh-licco](https://github.com/Echoqili/ssh-licco)

<img src="https://img.shields.io/github/languages/top/Echoqili/ssh-licco?style=flat-square" /> <img src="https://img.shields.io/github/license/Echoqili/ssh-licco?style=flat-square" /> <img src="https://img.shields.io/github/stars/Echoqili/ssh-licco?style=flat-square" />

给 AI 客户端一副能登录服务器的手。SSH 能力封装成标准 MCP 工具，Claude Code / Qoder / Cursor 等客户端一处配置、多处复用，不用每个工具各写一套胶水代码。

#### [shiying · 拾影](https://github.com/Echoqili/shiying)

<img src="https://img.shields.io/github/languages/top/Echoqili/shiying?style=flat-square" /> <img src="https://img.shields.io/github/license/Echoqili/shiying?style=flat-square" /> <img src="https://img.shields.io/github/v/release/Echoqili/shiying?style=flat-square&label=release" />

Windows 桌面应用（PySide6 + yt-dlp）：批量下载视频/MP3，缺字幕时本地 FFmpeg 分段转写，再用 Qoder 或任意 OpenAI 兼容接口生成中文笔记（摘要 / 关键观点 / 时间线 / 行动建议）。

工程细节上做了几件容易被忽略的事：密钥走 Windows DPAPI 加密、转写失败可断点续传避免重复计费、不兼容封装自动转 H.264 兼容 MP4、发版由 GitHub Actions 全自动打包并校验安装包。

#### [skills-manager](https://github.com/Echoqili/skills-manager)

<img src="https://img.shields.io/github/languages/top/Echoqili/skills-manager?style=flat-square" /> <img src="https://img.shields.io/github/license/Echoqili/skills-manager?style=flat-square" />

Skills 的注册表、分发链路和质检闸门，Web + Electron + CLI 三端同一套数据：239 个技能、零依赖 TF-IDF 中文语义检索、199+ 项安全审计、信任分三维评估。

关键在于**不照单全收**：从外部导入的技能先过「规范校验 + 风险扫描 + 声明与行为一致性」，不通过就进隔离区，不入库。私有 Registry 的发布门禁与导入链路同源，避免「发布一套标准、CI 另一套标准」。

#### [douyin-favorites-organizer](https://github.com/Echoqili/douyin-favorites-organizer)

<img src="https://img.shields.io/github/languages/top/Echoqili/douyin-favorites-organizer?style=flat-square" /> <img src="https://img.shields.io/github/stars/Echoqili/douyin-favorites-organizer?style=flat-square" />

抖音收藏夹批量整理：采集 → 语义分类 → 浏览器自动化写回。附带流程文档与可复用的 WorkBuddy Skill，把一次性脚本沉淀成可重复执行的流程。

---

### 其他

| 项目 | 说明 |
| --- | --- |
| [openclaw-feishu-deploy](https://github.com/Echoqili/openclaw-feishu-deploy) | 飞书新闻机器人：AI 抓取、分类并推送到飞书，含 Docker / Render 部署链路 |
| [wedding-live](https://github.com/Echoqili/wedding-live) | 婚礼现场互动系统：签到墙、祝福弹幕、抽奖、摇一摇，H5 大屏 + 手机端 + 主持控台走 WebSocket 实时同步 |
| [learning-open-source](https://github.com/Echoqili/learning-open-source) | AI Agent Skills 合集与学习沉淀 |

---

### 技术栈

<img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" /> <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black" /> <img src="https://img.shields.io/badge/PySide6-41CD52?style=flat-square&logo=qt&logoColor=white" /> <img src="https://img.shields.io/badge/Flask-000000?style=flat-square&logo=flask&logoColor=white" /> <img src="https://img.shields.io/badge/Electron-47848F?style=flat-square&logo=electron&logoColor=white" /> <img src="https://img.shields.io/badge/MCP-8957E5?style=flat-square" /> <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" /> <img src="https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white" />

<div align="center">
<sub>项目均以 MIT / Apache-2.0 开源，欢迎 Issue 与 PR。</sub>
</div>
