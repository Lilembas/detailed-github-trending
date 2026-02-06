# 🌟 GitHub Trending 概览

> 数据更新于：2026-02-06

---

## 🔍 项目详情

### 1. [anomalyco/opencode](https://github.com/anomalyco/opencode)
- 📅 **创建日期**：2025-04-30  
- 🔄 **最近更新**：2026-02-06  
- ⭐ **Stars**：176,230（日 +906｜周 +6364｜月 +73328）  
- 📝 **描述**：The open source coding agent.  

<details>
<summary><b>📈 Star 与 Commit 历史趋势</b></summary>

![opencode Star and Commit Trend](charts/anomalyco_opencode_trend.png)

> *蓝色：累计 Stars｜橙色：累计 Commits（次 Y 轴）*

</details>

<details>
<summary><b>📄 README 摘要</b></summary>

1. **该项目的功能**  
OpenCode 是一个开源的 AI 编程智能体（AI coding agent），旨在为开发者提供终端原生（TUI）、轻量高效、可扩展的 AI 辅助编程体验。它支持在本地终端中直接与 AI 协作完成代码编写、调试、重构、文档生成、代码库分析等任务，无需依赖特定云服务或闭源平台。其核心目标是成为开发者日常开发流程中“始终在线”的终端内 AI 助手，强调隐私性、离线可用性（配合本地模型）、跨平台一致性及对开发者工作流（如 LSP、Neovim 风格交互）的深度适配。

2. **关键特性**  
- **双模式智能体切换**：内置 `build`（全权限开发代理，支持文件编辑与命令执行）和 `plan`（只读分析代理，禁止自动修改文件，执行 shell 命令前强制确认），按 Tab 键即时切换，兼顾生产力与安全性；  
- **通用子代理（`@general`）**：支持复杂多步推理、跨文件语义搜索与抽象任务规划，可显式调用；  
- **终端优先架构（TUI-first）**：深度优化终端交互体验（类 Neovim 操作习惯），支持纯 CLI 使用，同时提供可选的桌面应用（Electron 或原生打包）；  
- **完全解耦的模型后端**：不绑定任何厂商 API，原生支持 Claude、OpenAI、Google Gemini、Ollama 本地模型等多种 LLM 接入方式，并推荐配套的开源模型分发平台 OpenCode Zen；  
- **开箱即用的 LSP 支持**：内置语言服务器协议集成，实现智能补全、跳转、诊断等 IDE 级功能；  
- **客户端/服务器分离架构**：核心引擎可独立运行于本地或远程服务器，支持通过不同前端（如 TUI、移动 App、Web）连接控制，提升部署灵活性；  
- **多平台一键安装**：覆盖 macOS/Linux（Homebrew、Nix、Mise）、Windows（Scoop、Chocolatey）、Arch（AUR）等主流包管理器，支持自定义安装路径与多版本共存。

3. **技术栈**  
- **核心语言与运行时**：TypeScript（主逻辑）、Rust（高性能组件，如部分 CLI 工具链与底层通信模块，虽未明写但由项目结构及维护者背景可推断）；  
- **前端框架**：TUI 层基于终端原生渲染（可能使用 `blessed` / `ink` / 自研轻量渲染器），桌面版采用 Electron（.dmg/.exe/.deb 等分发格式佐证）；  
- **协议与集成**：原生支持 LSP（Language Server Protocol）、STDIO 进程通信、HTTP API（供外部客户端调用）；  
- **构建与发布**：GitHub Actions CI/CD（`publish.yml`），多平台交叉构建（darwin-aarch64/x64、win-x64、linux-x64/arm64），支持 Nix、Homebrew、Scoop 等现代包管理生态；  
- **基础设施**：依赖 Ollama、Claude、OpenAI 等外部模型服务（运行时可插拔），自身不托管模型，强调“AI 引擎”而非“AI 服务”。

</details>

---

### 2. [anthropics/claude-code](https://github.com/anthropics/claude-code)
- 📅 **创建日期**：2025-02-22  
- 🔄 **最近更新**：2026-02-06  
- ⭐ **Stars**：119,523（日 +407｜周 +1723｜月 +15255）  
- 📝 **描述**：Claude Code is an agentic coding tool that lives in your terminal, understands your codebase, and helps you code faster by executing routine tasks, explaining complex code, and handling git workflows - all through natural language commands.  

<details>
<summary><b>📈 Star 与 Commit 历史趋势</b></summary>

![claude-code Star and Commit Trend](charts/anthropics_claude-code_trend.png)

> *蓝色：累计 Stars｜橙色：累计 Commits（次 Y 轴）*

</details>

<details>
<summary><b>📄 README 摘要</b></summary>

1. **该项目的功能**  
Claude Code 是一款终端原生的智能编程助手，能够深度理解用户当前代码库，通过自然语言指令自动执行常规开发任务（如代码生成、重构、调试）、解释复杂代码逻辑、自动化 Git 工作流（如提交、分支管理、冲突分析），并支持在终端、IDE 或 GitHub 中（通过 `@claude` 提及）调用，实现无缝集成的“代理式”编码体验。

2. **核心特性**  
- **上下文感知的代码理解**：基于项目目录结构和文件内容实时构建代码知识图谱，提供精准的语义级响应；  
- **自然语言驱动的开发操作**：支持纯中文/英文指令完成编码、注释、测试、文档生成等任务；  
- **Git 智能工作流支持**：自动解析 Git 状态、生成提交信息、建议分支策略、解释差异（diff）与冲突；  
- **多环境部署能力**：提供 macOS/Linux 一键脚本、Homebrew、Windows PowerShell 脚本、WinGet 四种主流安装方式，弃用 npm 全局安装；  
- **插件化扩展架构**：内置可扩展插件系统（位于 `plugins/` 目录），支持自定义命令与专用代理功能；  
- **内建反馈与诊断机制**：通过 `/bug` 命令直接上报问题，集成会话数据与操作反馈用于质量改进（受隐私策略严格约束）。

3. **技术栈**  
- **运行时环境**：Node.js 18+（作为基础运行时，但安装方式已脱离 npm 依赖）；  
- **客户端架构**：终端原生 CLI 工具（非 Web 应用），跨平台原生二进制分发（通过 shell 脚本、Homebrew Cask、PowerShell、WinGet 分发）；  
- **后端服务**：依托 Anthropic 的 Claude 大模型 API（未公开具体模型版本，但强调针对代码场景优化）；  
- **安全与合规**：采用最小化数据收集策略，敏感数据限时保留，禁止将用户代码或对话用于模型训练，符合商业服务条款与隐私政策要求。

</details>

---

### 3. [anthropics/skills](https://github.com/anthropics/skills)
- 📅 **创建日期**：2025-09-22  
- 🔄 **最近更新**：2026-02-06  
- ⭐ **Stars**：104,100（日 +909｜周 +5994｜月 +35293）  
- 📝 **描述**：Public repository for Agent Skills  

<details>
<summary><b>📈 Star 与 Commit 历史趋势</b></summary>

![skills Star and Commit Trend](charts/anthropics_skills_trend.png)

> *蓝色：累计 Stars｜橙色：累计 Commits（次 Y 轴）*

</details>

<details>
<summary><b>📄 README 摘要</b></summary>

1. **该项目的作用**  
该项目是 Anthropic 官方提供的 Claude 技能（Skills）参考实现仓库，旨在展示如何通过结构化技能包扩展 Claude 的能力。每个“技能”是一个独立文件夹，内含 `SKILL.md`（含 YAML 元数据和自然语言指令），使 Claude 能动态加载并执行特定领域任务，如按企业品牌规范生成文档、按组织流程分析数据、自动化个人事务等。它不提供独立运行的软件，而是为开发者和企业构建可复用、可插拔的 AI 能力模块提供权威范例与实践基准。

2. **核心功能**  
- **模块化技能封装**：每个技能自包含于独立文件夹，通过标准化 `SKILL.md`（含 `name`/`description` 前置元数据 + 指令正文 + 示例 + 指南）定义行为，支持即插即用；  
- **多场景技能覆盖**：涵盖创意设计（艺术/音乐/设计）、技术开发（Web 应用测试、MCP 服务器生成）、企业应用（通信模板、品牌合规）及文档处理（DOCX/PDF/PPTX/XLSX 创建与编辑）四大类；  
- **生产级参考实现**：公开 `skills/docx`、`skills/pdf` 等子目录中支撑 Claude 实际文档能力的源可用（source-available）技能代码，供开发者学习复杂技能工程实践；  
- **跨平台集成支持**：支持在 Claude Code（插件市场安装）、Claude.ai（付费版直接启用）、Claude API（上传自定义技能）三端部署与调用，实现“提及即用”（如：“用 PDF 技能提取 `xxx.pdf` 的表单字段”）；  
- **开放规范与模板**：内置 [Agent Skills 规范](./spec) 和 [技能模板](./template)，降低开发者创建符合标准技能的门槛。

3. **技术栈**  
- **核心格式**：纯文本 Markdown（`SKILL.md`）+ YAML 前置元数据，无运行时依赖，强调人类可读性与模型可解析性；  
- **协议标准**：基于开源的 [Agent Skills 规范](http://agentskills.io)，定义技能发现、加载、执行与元数据交互的通用接口；  
- **交付形态**：静态文件仓库（GitHub），技能以文件系统目录结构组织，依赖 Anthropic 运行时环境（Claude Code / Claude.ai / Claude API）进行动态解析与执行；  
- **许可证**：多数示例技能采用 Apache 2.0 开源许可，文档类技能为源可用（source-available，非开源），明确区分可自由修改与仅作参考的组件。

</details>

---

### 4. [DataTalksClub/data-engineering-zoomcamp](https://github.com/DataTalksClub/data-engineering-zoomcamp)
- 📅 **创建日期**：2021-10-21  
- 🔄 **最近更新**：2026-02-06  
- ⭐ **Stars**：74,641（日 +71｜周 +503｜月 +6062）  
- 📝 **描述**：Data Engineering Zoomcamp is a free 9-week course on building production-ready data pipelines. The next cohort starts in January 2026. Join the course here 👇🏼  

<details>
<summary><b>📈 Star 与 Commit 历史趋势</b></summary>

![data-engineering-zoomcamp Star and Commit Trend](charts/DataTalksClub_data-engineering-zoomcamp_trend.png)

> *蓝色：累计 Stars｜橙色：累计 Commits（次 Y 轴）*

</details>

<details>
<summary><b>📄 README 摘要</b></summary>

1. **该项目做什么？**  
该项目是“Data Engineering Zoomcamp”（数据工程训练营），一个为期9周、完全免费的实践型数据工程入门课程。其核心目标是带领学员从零开始构建端到端的数据工程流水线，覆盖数据采集、存储、处理、分析到部署的完整生命周期。课程以真实工业级场景为驱动，强调动手实操而非纯理论，最终通过综合项目整合所学知识，并提供社区支持与同行评审机制，助力学员掌握就业所需的核心能力。

2. **关键特性**  
- **结构化渐进式学习路径**：涵盖6大核心模块（容器化与基础设施即代码、工作流编排、数据湖/仓、分析工程、批处理、流处理）+ 2个专项工作坊（数据摄入、最终项目），逻辑清晰、层层递进；  
- **全栈工具链实战**：深度集成云平台（GCP）、容器（Docker/Docker Compose）、IaC（Terraform）、编排（Kestra）、数据湖/仓（BigQuery）、ETL/ELT（dlt）、建模与测试（dbt）、大数据计算（Spark）、流处理（Kafka/KSQL/Avro）等主流技术；  
- **强社区驱动与开放生态**：依托 DataTalks.Club 全球 Slack 社区提供实时答疑、协作与职业网络；所有课程资料（视频、笔记、代码、作业）永久免费开源，支持自主学习；  
- **真实项目导向**：包含多个动手实验、模块作业及综合性最终项目，强调工程规范（如测试、文档、CI/CD意识）与可交付成果；  
- **行业背书与持续更新**：由资深数据工程师联合授课，获 Kestra、Bruin、dltHub 等头部数据工具厂商赞助，内容紧贴业界最新实践。

3. **技术栈**  
- **云与基础设施**：Google Cloud Platform（GCP）、Terraform（基础设施即代码）、Docker / Docker Compose（容器化部署）；  
- **数据存储与查询**：PostgreSQL（本地开发）、BigQuery（云数仓，含分区/聚类/ML集成）、DuckDB（轻量分析）；  
- **数据编排与管道**：Kestra（现代工作流引擎）、dlt（声明式数据加载工具）；  
- **分析工程与建模**：dbt（data build tool），支持 DuckDB 和 BigQuery 后端，涵盖模型设计、测试、文档生成与部署；  
- **大数据处理**：Apache Spark（Scala/Python API）、Spark SQL、DataFrame 操作及底层执行原理（如 GroupBy/Join 机制）；  
- **实时流处理**：Apache Kafka（消息队列）、Kafka Streams、KSQL、Avro（Schema 管理）；  
- **辅助生态**：Airtable（报名管理）、Slack/Telegram（社区协作）、YouTube（课程视频）、GitHub（代码托管与文档）。

</details>

---

### 5. [obra/superpowers](https://github.com/obra/superpowers)
- 📅 **创建日期**：2025-10-09  
- 🔄 **最近更新**：2026-02-06  
- ⭐ **Stars**：74,227（日 +913｜周 +5608｜月 +46031）  
- 📝 **描述**：An agentic skills framework & software development methodology that works.  

<details>
<summary><b>📈 Star 与 Commit 历史趋势</b></summary>

![superpowers Star and Commit Trend](charts/obra_superpowers_trend.png)

> *蓝色：累计 Stars｜橙色：累计 Commits（次 Y 轴）*

</details>

<details>
<summary><b>📄 README 摘要</b></summary>

1. **项目功能**  
Superpowers 是一个面向编程智能体（coding agents）的完整软件开发工作流增强系统。它不直接替代编码代理，而是为其注入结构化、可复用的“能力技能”（skills），使其在真实开发场景中能自动执行专业级工程实践：从需求澄清、设计评审、TDD 实施、分支隔离开发，到子智能体协同执行、多阶段代码审查及分支收尾决策。整个流程由技能自动触发、强制执行，无需用户手动调用，目标是让 AI 编程代理具备接近资深工程师的系统性、纪律性和协作意识。

2. **核心特性**  
- **全流程自动化工程实践**：覆盖从头脑风暴（Socratic 设计引导）、Git 工作树隔离、原子化任务计划（每项 2–5 分钟）、子智能体驱动开发（Subagent-Driven Development）、严格红/绿/重构 TDD（含测试先行与无测试代码自动删除）、到分支完成决策的七阶段闭环。  
- **强制性技能触发机制**：所有技能均为上下文感知、自动激活的“硬性流程”，非可选建议；每个开发动作前均检查并应用匹配技能。  
- **深度协作支持**：内置代码评审请求/响应、并行子智能体调度、Git 工作树管理、PR/合并策略建议等，模拟真实团队协作范式。  
- **可扩展技能库**：开放技能架构（如 `writing-skills` 技能提供技能开发规范），支持社区贡献新技能，所有技能即代码（存于仓库），版本化、可测试、可更新。  
- **跨平台兼容性**：原生支持 Claude Code（插件市场一键安装）、Codex 与 OpenCode（通过远程配置脚本集成），具备统一技能语义与行为一致性。

3. **技术栈**  
- **运行时环境**：依赖大语言模型智能体平台（Claude Code、Codex、OpenCode），本身为**平台无关的技能协议层**，不绑定特定模型或推理引擎。  
- **核心实现形式**：以纯文本技能文档（`.md`）为主，辅以结构化指令模板与验证逻辑；技能通过自然语言指令+上下文规则触发，无二进制组件或运行时服务。  
- **基础设施**：基于 GitHub 托管（代码、文档、市场插件仓库），使用标准 Git 工作流；安装与更新通过平台原生命令（如 `/plugin install`）或 HTTP 远程拉取配置实现；许可证为 MIT。  
- **设计理念驱动栈**：技术实现完全服务于工程哲学——TDD、YAGNI、DRY、系统性调试、证据导向验证，所有技能均内嵌对应方法论（如 TDD 技能含反模式参考，调试技能含四阶段根因追踪框架）。

</details>

---

### 6. [ComposioHQ/awesome-claude-skills](https://github.com/ComposioHQ/awesome-claude-skills)
- 📅 **创建日期**：2025-10-17  
- 🔄 **最近更新**：2026-02-06  
- ⭐ **Stars**：52,467（日 +603｜周 +2967｜月 +21912）  
- 📝 **描述**：A curated list of awesome Claude Skills, resources, and tools for customizing Claude AI workflows  

<details>
<summary><b>📈 Star 与 Commit 历史趋势</b></summary>

![awesome-claude-skills Star and Commit Trend](charts/ComposioHQ_awesome-claude-skills_trend.png)

> *蓝色：累计 Stars｜橙色：累计 Commits（次 Y 轴）*

</details>

<details>
<summary><b>📄 README 摘要</b></summary>

1. **项目功能**  
该项目是一个面向 Anthropic Claude 系列模型（包括 Claude.ai、Claude Code 和 Claude API）的**可扩展技能（Skills）开源集合库**，旨在将 Claude 从纯文本生成模型升级为具备**真实世界操作能力的智能代理**。它不提供独立运行的应用，而是通过标准化的技能插件机制，使 Claude 能够执行具体、可复用的任务——如处理文档（Word/PDF/Excel/PPT）、调用外部 API、连接 1000+ 第三方应用（Gmail/Slack/GitHub/Notion 等）、自动化开发流程（Git 操作、测试生成、Changelog 编写）、数据分析（CSV/PostgreSQL）、安全分析（Sigma 规则威胁狩猎）、内容创作（品牌文案、会议洞察、简历定制）等，覆盖生产力、开发、商业、协作、安全等全场景工作流。

2. **核心特性**  
- **跨平台统一技能体系**：所有技能均兼容 Claude.ai（网页端）、Claude Code（本地 IDE 插件）及 Claude API（程序化调用），实现“一次编写、三端生效”。  
- **深度应用集成能力**：依托 Composio 框架，通过 `connect-apps` 插件实现免代码连接 500+ SaaS 应用，支持邮件发送、Slack 发帖、GitHub Issue 创建、数据库查询等**真实动作执行**（非仅模拟）。  
- **结构化技能规范**：采用基于 Markdown 的标准化技能格式（含 YAML 元数据、使用场景、指令逻辑、示例），支持脚本、模板、资源文件等扩展目录，便于复用与维护。  
- **垂直领域全覆盖**：按功能划分为 9 大类共 60+ 个精选技能，涵盖文档处理、开发工具链（Playwright 自动化、D3 可视化、LangSmith 调试）、数据科学（CSV 分析、PostgreSQL 查询）、商业营销（竞品广告提取、领英线索研究）、创意媒体（Canvas 设计、YouTube 转录）、安全系统（数字取证、Sigma 威胁检测）等。  
- **低门槛接入与协作生态**：提供一键式插件安装（`claude --plugin-dir`）、交互式配置向导（`/connect-apps:setup`），并鼓励社区贡献（PRs Welcome），集成 Discord 社区、X/LinkedIn 官方渠道及 Apache-2.0 开源协议。

3. **技术栈**  
- **核心框架**：基于 Anthropic 官方 [Claude Skills API](https://docs.claude.com/en/api/skills-guide) 构建，遵循其技能定义规范（`SKILL.md` + YAML 元数据）；底层应用连接依赖 [Composio](https://composio.dev/) 平台（提供跨应用认证、API 抽象与工具编排能力）。  
- **开发语言与工具**：技能本身以纯文本 Markdown 实现，但配套能力广泛使用 Python（如 `postgres` 技能的 SQL 执行、`n8n-skills` 的工作流集成）、TypeScript/JavaScript（`artifacts-builder` 中的 React/Tailwind 前端构建、`Playwright` 浏览器自动化）、Shell（Git 工作树管理）、SQL（PostgreSQL 只读查询）等；部分技能调用外部服务如 Gemini API（`imagen`, `deep-research`）、NotebookLM、FFUF 等。  
- **基础设施与部署**：无服务端组件，技能以本地文件形式加载（Claude Code 存于 `~/.config/claude-code/skills/`）；插件模式依赖 Claude 客户端原生支持；第三方集成通过 Composio 的云服务或自托管 SDK 实现 OAuth 与 API 通信。

</details>

---

### 7. [openclaw/openclaw](https://github.com/openclaw/openclaw)
- 📅 **创建日期**：2025-11-24  
- 🔄 **最近更新**：2026-02-06  
- ⭐ **Stars**：52,341（日 +4594｜周 +52341｜月 +52341）  
- 📝 **描述**：Your own personal AI assistant. Any OS. Any Platform. The lobster way. 🦞   

<details>
<summary><b>📈 Star 与 Commit 历史趋势</b></summary>

![openclaw Star and Commit Trend](charts/openclaw_openclaw_trend.png)

> *蓝色：累计 Stars｜橙色：累计 Commits（次 Y 轴）*

</details>

<details>
<summary><b>📄 README 摘要</b></summary>

1. **项目功能**  
OpenClaw 是一个**本地化、单用户、全栈自托管的个人AI助手系统**，核心目标是让用户在自有设备（macOS/iOS/Android/Linux）上完全掌控AI交互体验。它不依赖中心化云服务，而是通过轻量级本地网关（Gateway）统一调度：接收来自30+通讯渠道（WhatsApp、Telegram、Slack、Discord、Signal、iMessage、BlueBubbles、Microsoft Teams、Matrix、Zalo、WebChat等）的消息，调用本地或远程大模型（如Claude Opus、GPT系列），执行多模态工具操作（浏览器控制、Canvas可视化界面、语音唤醒与合成、摄像头/录屏、定位、系统命令等），并以低延迟、高隐私的方式将响应实时回传至原始通道。其本质是“你设备上的AI操作系统”，强调**始终在线、零数据外泄、深度设备集成**。

2. **关键特性**  
- **跨平台多通道统一收发**：原生支持主流IM及扩展渠道（含iMessage蓝泡泡、Zalo等区域平台），支持群组消息路由、提及激活、上下文隔离。  
- **本地优先架构**：单进程WebSocket网关作为控制平面，管理会话、通道、工具、定时任务、WebHook和远程调试接口；所有敏感操作（如文件读写、系统调用）默认运行于用户本地环境。  
- **多智能体工作区（Workspace）与会话隔离**：支持为不同场景（如工作/生活/开发）配置独立Agent，每个Agent拥有专属模型、技能、上下文策略与权限沙箱。  
- **全模态交互能力**：  
  • **语音**：macOS/iOS/Android端集成ElevenLabs实现“常驻唤醒（Voice Wake）”与连续对话（Talk Mode）；  
  • **视觉**：基于A2UI协议的“Live Canvas”动态画布，支持AI驱动的可视化操作、截图、快照与评估；  
  • **设备能力调用**：通过`node.invoke`安全调用相机、屏幕录制、位置、通知、系统命令（含TCC权限校验）。  
- **企业级安全与治理**：默认启用DM配对认证（防未授权消息）、模型故障转移（Model Failover）、会话自动剪枝、细粒度通道访问策略（`allowFrom`/`dmPolicy`）、密码/Tailscale双因子远程访问控制。  
- **开发者友好生态**：CLI向导（`openclaw onboard`）一键完成部署；支持Nix声明式配置、Docker容器化、Tailscale内网穿透/公网暴露；提供完整Web控制台（Control UI）、诊断工具（`openclaw doctor`）及详尽文档体系。

3. **技术栈**  
- **运行时**：Node.js ≥22（主程序），TypeScript（全栈开发），pnpm（首选包管理器），bun（可选TS直接执行）。  
- **核心框架**：自研轻量级WebSocket网关（事件驱动架构），Pi Agent RPC运行时（支持工具流式调用与块流式响应）。  
- **前端与UI**：WebChat基于Web技术栈；macOS/iOS/Android Companion App采用原生开发（Swift/Kotlin）；Canvas/A2UI为定制化渲染协议。  
- **通道集成**：复用成熟开源SDK——Baileys（WhatsApp）、grammY（Telegram）、discord.js（Discord）、@slack/bolt（Slack）、signal-cli（Signal）、matrix-js-sdk（Matrix）等。  
- **AI模型层**：抽象化模型适配器，官方推荐Anthropic Claude Opus 4.6（强长上下文与抗提示注入），兼容OpenAI、Ollama等任意兼容OpenAI API的后端。  
- **基础设施**：Tailscale（安全远程访问）、SSH隧道、systemd/launchd服务管理、Chrome DevTools Protocol（浏览器自动化）、FFmpeg（音视频处理）。

</details>

---

### 8. [bytedance/UI-TARS-desktop](https://github.com/bytedance/UI-TARS-desktop)
- 📅 **创建日期**：2025-01-19  
- 🔄 **最近更新**：2026-02-06  
- ⭐ **Stars**：51,030（日 +533｜周 +1731｜月 +10275）  
- 📝 **描述**：The Open-Source Multimodal AI Agent Stack: Connecting Cutting-Edge AI Models and Agent Infra  

<details>
<summary><b>📈 Star 与 Commit 历史趋势</b></summary>

![UI-TARS-desktop Star and Commit Trend](charts/bytedance_UI-TARS-desktop_trend.png)

> *蓝色：累计 Stars｜橙色：累计 Commits（次 Y 轴）*

</details>

<details>
<summary><b>📄 README 摘要</b></summary>

1. **项目功能**  
TARS 是一个开源的多模态 AI 智能体（Agent）技术栈，核心目标是实现类人化、端到端的任务自动化。它包含两大协同组件：  
- **Agent TARS**：通用多模态智能体框架，支持在终端（CLI）、Web 界面及产品中运行，可理解 GUI 界面、屏幕图像与自然语言指令，自主调用真实世界工具（如浏览器、Shell、文件系统等）完成复杂任务（例如“在 Booking.com 预订机场附近丽思卡尔顿酒店”或“生成杭州一个月天气图表”）。  
- **UI-TARS Desktop**：原生桌面应用，基于 UI-TARS 视觉语言模型（如 Seed-1.5-VL/1.6 系列），提供本地/远程计算机与浏览器的 GUI 自动化控制能力（如操作 VS Code 设置、浏览 GitHub 问题），全程离线处理，保障隐私安全。

2. **关键特性**  
- ✅ **多模态感知与执行**：融合视觉（截图识别）、语言、GUI 元素定位（Visual Grounding + DOM 解析）能力，实现跨界面精准交互；  
- ✅ **混合浏览器代理**：支持 GUI 视觉驱动、DOM 结构解析或二者协同的浏览器自动化策略；  
- ✅ **事件流驱动架构（Event Stream）**：基于协议化事件流实现上下文工程、实时数据流追踪与调试（含 Event Stream Viewer）；  
- ✅ **MCP（Model Control Protocol）深度集成**：以 MCP 为内核，可动态挂载各类 MCP Server，无缝连接 Shell、代码执行沙箱（AIO Sandbox）、浏览器、本地应用等现实工具；  
- ✅ **开箱即用的多形态部署**：提供 CLI（headless）、Web UI（headful）、桌面客户端（Windows/macOS）、远程控制（Remote Computer/Browser Operator）四种运行模式；  
- ✅ **全链路本地化与隐私保护**：UI-TARS Desktop 支持纯本地模型推理与操作，无数据上传；Agent TARS CLI/Web UI 亦支持私有化部署与本地工具集成。

3. **技术栈**  
- **前端/客户端**：Electron（UI-TARS Desktop）、React/Vite（Web UI）、TypeScript；  
- **核心运行时**：Node.js（≥ v22），CLI 基于 npm 包 `@agent-tars/cli`；  
- **AI 模型层**：  
  - 视觉语言模型：ByteDance 自研 **UI-TARS 系列**（如 UI-TARS-1.5-7B）、**Seed-1.5-VL / Seed-1.6**；  
  - 多模态大模型支持：兼容 VolcEngine（Doubao 系列）、Anthropic（Claude 3.7 Sonnet）等第三方 API；  
- **协议与标准**：基于开放协议 **MCP（Model Control Protocol）** 构建工具编排与通信；  
- **基础设施**：支持 ModelScope、Hugging Face 模型托管；提供 AIO Agent Sandbox 作为隔离化工具执行环境；  
- **部署与生态**：支持云部署（ModelScope 平台）、本地 SDK（UI TARS SDK）、飞书/DeepWiki/Discord 社区协作。

</details>

---

### 9. [remotion-dev/remotion](https://github.com/remotion-dev/remotion)
- 📅 **创建日期**：2020-06-23  
- 🔄 **最近更新**：2026-02-06  
- ⭐ **Stars**：35,189（日 +187｜周 +1556｜月 +10043）  
- 📝 **描述**：🎥      Make videos programmatically with React  

<details>
<summary><b>📈 Star 与 Commit 历史趋势</b></summary>

![remotion Star and Commit Trend](charts/remotion-dev_remotion_trend.png)

> *蓝色：累计 Stars｜橙色：累计 Commits（次 Y 轴）*

</details>

<details>
<summary><b>📄 README 摘要</b></summary>

1. **项目功能**  
Remotion 是一个基于 React 的视频生成框架，允许开发者使用 React 组件、JavaScript 逻辑和 Web 技术（如 CSS、SVG、Canvas、WebGL）**以编程方式动态创建高质量视频**。它将视频视为“可渲染的 React 应用”，支持时间轴控制、帧精确渲染、动态内容生成（如数据驱动动画、个性化视频），并可导出为 MP4、GIF 或 ProRes 等格式，适用于营销视频、数据可视化、年度回顾（如 GitHub Unwrapped）、教程动画等场景。

2. **核心特性**  
- ✅ **React 原生开发体验**：复用 React 组件、Hooks、状态管理、Context 和第三方库；支持 Fast Refresh 实时预览动画变化。  
- ✅ **时间轴与帧控制**：提供 `useCurrentFrame`、`interpolate`、`Sequence`、`Composition` 等 API，实现基于时间的精准动画逻辑与分段编排。  
- ✅ **多目标输出**：一键导出为 MP4（H.264/AV1）、GIF、ProRes、PNG 序列，并支持自定义编码参数与分辨率。  
- ✅ **服务端渲染支持**：可通过 Node.js（无头 Chromium）离线渲染视频，适配 CI/CD、Serverless（Vercel/Cloudflare）及动态视频生成（如用户定制化内容）。  
- ✅ **开发友好工具链**：内置本地预览服务器、帧调试器、性能分析面板、TypeScript 全面支持，以及丰富的 CLI（如 `npx create-video@latest` 快速初始化）。  

3. **技术栈**  
- **核心框架**：React（v18+，支持 Concurrent Features）、TypeScript  
- **渲染引擎**：基于 Chromium（Puppeteer / Playwright）进行 Headless 浏览器渲染，利用其对 CSS 动画、Canvas/WebGL 的完整支持  
- **构建与打包**：Vite（默认模板）、Webpack（兼容）；ESM 模块规范  
- **底层依赖**：FFmpeg（视频编码/封装）、@ffmpeg/ffmpeg（WASM 版本可选）、sharp（图像处理）  
- **部署与集成**：原生支持 Vercel、Netlify、Cloudflare Workers；提供 Remotion Cloud 托管服务（可选）  
- **生态配套**：npm 包管理（`remotion` 主包 + `@remotion/cli`、`@remotion/renderer` 等子包），Discord 社区与活跃开源维护

</details>

---

### 10. [asgeirtj/system_prompts_leaks](https://github.com/asgeirtj/system_prompts_leaks)
- 📅 **创建日期**：2025-05-03  
- 🔄 **最近更新**：2026-02-06  
- ⭐ **Stars**：30,291（日 +183｜周 +2674｜月 +5545）  
- 📝 **描述**：Collection of extracted System Prompts from popular chatbots like ChatGPT, Claude & Gemini  

<details>
<summary><b>📈 Star 与 Commit 历史趋势</b></summary>

![system_prompts_leaks Star and Commit Trend](charts/asgeirtj_system_prompts_leaks_trend.png)

> *蓝色：累计 Stars｜橙色：累计 Commits（次 Y 轴）*

</details>

---

### 11. [code-yeongyu/oh-my-opencode](https://github.com/code-yeongyu/oh-my-opencode)
- 📅 **创建日期**：2025-12-03  
- 🔄 **最近更新**：2026-02-06  
- ⭐ **Stars**：28,535（日 +387｜周 +2731｜月 +18915）  
- 📝 **描述**：The Best Agent Harness. Meet Sisyphus: The Batteries-Included Agent that codes like you.  

<details>
<summary><b>📈 Star 与 Commit 历史趋势</b></summary>

![oh-my-opencode Star and Commit Trend](charts/code-yeongyu_oh-my-opencode_trend.png)

> *蓝色：累计 Stars｜橙色：累计 Commits（次 Y 轴）*

</details>

<details>
<summary><b>📄 README 摘要</b></summary>

1. **项目功能**  
Oh My OpenCode 是一个面向开源代码编辑器 OpenCode（基于终端的 AI 编程环境）的**高性能、生产就绪型插件框架**，核心目标是将单个 LLM 代理升级为协同工作的「AI 工程师团队」。它不替代 OpenCode，而是深度增强其能力：通过多模型协同编排（orchestration），让不同专业角色的 AI 代理（如 Sisyphus 主协调员、Hephaestus 深度工匠、Oracle 架构师、Librarian 文档专家、Frontend Engineer 前端专家等）并行执行、自主分工、上下文共享与任务闭环，实现从需求理解、代码探索、重构调试到交付验证的**全自动、端到端工程化工作流**。本质是为 OpenCode 提供企业级 AI 团队协作操作系统。

2. **关键特性**  
- **多智能体协同架构**：预置 6+ 专业化角色代理（Sisyphus、Hephaestus、Oracle 等），支持按任务类型（`visual`/`business-logic`）、模型能力或成本自动路由；  
- **全自动背景任务调度**：支持异步并行执行探索、文档检索、代码搜索等前置任务，显著降低主代理上下文负担；  
- **工业级代码工具链集成**：原生支持 LSP（语义重命名、诊断）、AST-Grep（结构化代码搜索）、Refactor 工具，确保代码修改安全精准；  
- **Claude Code 兼容层**：完整实现命令（Command）、技能（Skill）、MCP（Model Calling Protocol）、钩子（Pre/PostToolUse 等 25+ 可配置钩子）；  
- **任务强保障机制**：Todo Continuation Enforcer（强制未完成任务续跑）、Comment Checker（抑制冗余注释）、Ralph Loop（迭代验证闭环）；  
- **开箱即用的 MCP 生态**：内置 Exa（Web 搜索）、Context7（官方文档）、grep.app（GitHub 代码搜索）等高价值工具；  
- **极简触发协议**：仅需在提示词中加入 `ultrawork`（或 `ulw`）关键词，即可激活全部高级能力，无需手动配置；  
- **全终端友好设计**：深度集成 Tmux，支持交互式终端操作，零屏幕闪烁，高响应性能。

3. **技术栈**  
- **运行时环境**：专为 [OpenCode](https://github.com/sst/opencode)（基于 Rust/Terminal 的开源 IDE）构建，依赖其插件系统与 LSP 协议；  
- **核心语言**：TypeScript（主要逻辑）、Rust（底层性能敏感模块，如 AST 工具集成）；  
- **AI 模型层**：多模型混合调度（非绑定单一供应商），实测支持 Claude Sonnet/Haiku/Opus、GPT-4.5/GPT-5.2 Codex、Gemini 3 Pro 等主流闭源模型，通过标准化 MCP 接口抽象调用；  
- **基础设施**：JSONC 配置（支持注释与灵活语法）、Tmux 会话管理、本地文件系统上下文注入（自动加载 `AGENTS.md`/`README.md` 等）；  
- **许可证**：采用 [SUL-1.0（Sisyphus License）](https://github.com/code-yeongyu/oh-my-opencode/blob/master/LICENSE.md) —— 一种强调“开源可审计、商用需授权”的定制许可，兼顾开放性与可持续性。

</details>

---

### 12. [microsoft/BitNet](https://github.com/microsoft/BitNet)
- 📅 **创建日期**：2024-08-05  
- 🔄 **最近更新**：2026-02-06  
- ⭐ **Stars**：27,962（日 +70｜周 +1456｜月 +2600）  
- 📝 **描述**：Official inference framework for 1-bit LLMs  

<details>
<summary><b>📈 Star 与 Commit 历史趋势</b></summary>

![BitNet Star and Commit Trend](charts/microsoft_BitNet_trend.png)

> *蓝色：累计 Stars｜橙色：累计 Commits（次 Y 轴）*

</details>

<details>
<summary><b>📄 README 摘要</b></summary>

1. **该项目的功能**  
bitnet.cpp 是微软推出的、专为 1-bit（实际为 1.58-bit）大语言模型（如 BitNet b1.58 系列）设计的**官方高性能推理框架**。其核心目标是实现**快速、无损（lossless）的本地化推理**，支持在资源受限的边缘设备（尤其是 CPU）上高效运行超大规模 1.58-bit LLM。它可单机部署 100B 参数级模型，在主流 CPU 上达到 5–7 token/s 的实时阅读级生成速度，并显著降低能耗（x86 平台节能达 71.9%–82.2%，ARM 平台达 55.4%–70.0%），使 1-bit LLM 真正具备端侧落地能力。

2. **关键特性**  
- ✅ **跨架构高性能 CPU 推理**：针对 x86 和 ARM 架构深度优化，实测加速比达 **2.37×–6.17×（x86）** 和 **1.37×–5.07×（ARM）**；最新并行核与分块（tiling）优化带来额外 **1.15×–2.1× 加速**；  
- ✅ **全模型规模支持**：已验证可运行 2.4B、3.3B、8B、10B 及至 **100B 参数级 BitNet b1.58 模型**于单颗 CPU；  
- ✅ **多量化内核支持**：提供三种底层计算核（I2_S、TL1、TL2），按硬件平台（x86/ARM）和模型结构自动适配，支持 embedding 量化（`--quant-embd`）；  
- ✅ **GPU/NPU 扩展就绪**：已发布官方 GPU 推理内核（CUDA），NPU 支持正在开发中；  
- ✅ **开箱即用生态集成**：兼容 Hugging Face 官方发布的多个 BitNet 模型（如 `microsoft/BitNet-b1.58-2B-4T`、`HF1BitLLM/Llama3-8B-1.58-100B-tokens`、Falcon3/E 系列等），支持 `.safetensors` → `.gguf` 转换；  
- ✅ **完整工具链**：提供模型下载、环境配置（`setup_env.py`）、推理（`run_inference.py`）、端到端基准测试（`e2e_benchmark.py`）、虚拟模型生成等全流程脚本，支持对话模式（`--conversation`）与温度控制等实用功能。

3. **技术栈**  
- **基础框架**：基于 `llama.cpp` 架构深度定制，复用其内存管理、上下文调度与 GGUF 模型格式生态；  
- **核心计算范式**：采用 **查找表（Lookup Table, LUT）加速方法论**，源自微软 T-MAC 项目，专为极低比特（1.58-bit weight + 4-bit activation）矩阵乘法优化；  
- **编程语言与编译工具链**：C/C++ 主体实现，依赖 **Clang ≥18**（Windows 需 VS2022 + Clang-LLVM 工具集）、**CMake ≥3.22**，构建系统高度适配跨平台原生编译；  
- **模型格式**：统一采用 **GGUF 格式**（含多种量化变体如 `i2_s.gguf`, `tl1.gguf`），支持量化权重加载与混合精度（如 f16 embedding）；  
- **运行时依赖**：Python 3.9+ 用于工具脚本（模型下载、转换、启动、评测），但**推理引擎本身为纯 C/C++，零 Python 运行时依赖**，保障最小化部署开销与最大性能。

</details>

---

### 13. [thedotmack/claude-mem](https://github.com/thedotmack/claude-mem)
- 📅 **创建日期**：2025-08-31  
- 🔄 **最近更新**：2026-02-06  
- ⭐ **Stars**：23,896（日 +1225｜周 +8423｜月 +12734）  
- 📝 **描述**：A Claude Code plugin that automatically captures everything Claude does during your coding sessions, compresses it with AI (using Claude's agent-sdk), and injects relevant context back into future sessions.  

<details>
<summary><b>📈 Star 与 Commit 历史趋势</b></summary>

![claude-mem Star and Commit Trend](charts/thedotmack_claude-mem_trend.png)

> *蓝色：累计 Stars｜橙色：累计 Commits（次 Y 轴）*

</details>

<details>
<summary><b>📄 README 摘要</b></summary>

1. **项目功能**  
Claude-Mem 是一个专为 Anthropic 的 **Claude Code（AI 编程代理）** 设计的**持久化记忆压缩系统**。它在用户每次会话结束后自动捕获工具调用行为、代码操作、错误修复等关键观测数据，生成语义化摘要，并将其结构化存储；在新会话启动时，智能检索并按需注入相关历史上下文，从而实现跨会话的**无缝知识延续**，显著提升 Claude Code 对项目背景的理解深度与连贯性。

2. **核心特性**  
- ✅ **持久记忆**：上下文自动跨会话保留，无需手动重载  
- ✅ **渐进式披露（Progressive Disclosure）**：分三层（索引→时间线→详情）按需加载记忆，实时显示 token 消耗，优化成本  
- ✅ **技能化搜索（mem-search）**：支持自然语言查询历史（如“认证相关 bug 修复”），结合类型/日期/项目过滤  
- ✅ **本地 Web 查看器**：`http://localhost:37777` 提供实时记忆流、API 接口（如 `/api/observation/{id}`）及可视化管理界面  
- ✅ **Claude Desktop 集成**：可在桌面版对话中直接调用记忆搜索技能  
- ✅ **隐私控制**：通过 `<private>` 标签自动排除敏感内容，不存入数据库  
- ✅ **全自动运行**：零配置即用，依赖生命周期钩子（SessionStart/PostToolUse/SessionEnd 等）静默工作  
- ✅ **引用溯源**：每条观测分配唯一 ID，支持精准回溯与交叉引用  
- ✅ **Beta 实验通道**：提供 Endless Mode（仿生长时记忆架构）等前沿功能，支持版本热切换  

3. **技术栈**  
- **运行时**：Node.js ≥18.0.0（主逻辑）、Bun（Worker 服务托管与 HTTP API）、uv（Python 包管理，用于向量搜索依赖）  
- **数据库**：SQLite 3（内置，含 FTS5 全文搜索） + ChromaDB（向量数据库，支撑混合语义+关键词检索）  
- **搜索架构**：Hybrid Search（FTS5 关键词索引 + Chroma 向量嵌入），实现高精度低延迟记忆检索  
- **后端服务**：基于 Bun 构建的轻量级 Worker Service（监听 `37777` 端口），提供 REST API 与 Web UI  
- **前端**：静态 Web Viewer（HTML/CSS/JS，适配深浅色模式）  
- **插件协议**：深度集成 Claude Agent SDK 与 MCP（Model Context Protocol）标准，实现 4 个标准化记忆搜索工具（`search`/`timeline`/`get_observations`/`__IMPORTANT`）  
- **开发语言**：TypeScript（主力）、Python（向量处理）、Shell/Bash（安装与自动化脚本）  
- **许可协议**：AGPL-3.0（主项目），`ragtime/` 子模块采用 PolyForm Noncommercial License

</details>

---

### 14. [lbjlaq/Antigravity-Manager](https://github.com/lbjlaq/Antigravity-Manager)
- 📅 **创建日期**：2025-11-26  
- 🔄 **最近更新**：2026-02-06  
- ⭐ **Stars**：21,440（日 +333｜周 +2121｜月 +12401）  
- 📝 **描述**：Professional Antigravity Account Manager & Switcher. One-click seamless account switching for Antigravity Tools. Built with Tauri v2 + React (Rust).专业的 Antigravity 账号管理与切换工具。为 Antigravity 提供一键无缝账号切换功能。  

<details>
<summary><b>📈 Star 与 Commit 历史趋势</b></summary>

![Antigravity-Manager Star and Commit Trend](charts/lbjlaq_Antigravity-Manager_trend.png)

> *蓝色：累计 Stars｜橙色：累计 Commits（次 Y 轴）*

</details>

<details>
<summary><b>📄 README 摘要</b></summary>

1. **项目功能**  
Antigravity Tools 是一个面向开发者与 AI 爱好者的**本地高性能 AI 调度网关与协议反代系统**，核心目标是构建稳定、极速、低成本的私有 AI 中转站。它并非简单账号管理工具，而是通过**多账号聚合、智能路由、协议标准化与自动容错**，打通 Google（Gemini）、Anthropic（Claude）等主流 Web 端 Session 与标准 API 接口之间的协议壁垒。用户可将浏览器登录态（如 Google OAuth 会话）转化为兼容 OpenAI/Claude/Gemini 原生协议的本地 API 服务（如 `http://localhost:8045/v1/chat/completions`），供各类 AI 客户端（Claude Code、Cherry Studio、Kilo Code、Python SDK 等）无缝接入，实现跨平台、跨协议、跨账号的统一调用。

2. **关键功能**  
- **智能账号仪表盘**：实时监控多账号（Gemini Pro/Flash、Claude 等）剩余配额，基于算法动态推荐“最佳可用账号”，支持一键切换与活跃账号快照。  
- **全模式账号管理**：支持 OAuth 2.0 自动/手动授权、JSON 批量导入、V1 版本热迁移；提供列表/网格双视图，集成 403 封禁自动检测与标注。  
- **多协议反向代理**：原生兼容 OpenAI（`/v1/chat/completions`）、Anthropic（`/v1/messages`）、Gemini 官方 SDK 三套协议；具备毫秒级自愈能力，对 `401`（Token 过期）和 `429`（限流）自动重试+静默轮换。  
- **高级模型路由中心**：支持模型家族映射（如所有 GPT-4 请求统一路由至 `gemini-3-pro-high`）、正则表达式级精准重定向、智能分级路由（按账号等级/配额重置周期优先调度）、后台请求静默降级（如自动将 Claude CLI 的标题生成任务导向 Flash 模型）。  
- **多模态与 Imagen 3 深度支持**：完整适配图像生成，支持 OpenAI 风格 `size`/`quality` 参数自动映射至 Imagen 3 规格；后端支持高达 100MB Payload，满足 4K 图像识别等高负载场景。  

3. **技术栈**  
- **前端**：React（TypeScript），基于 Tauri 框架构建跨平台桌面应用（macOS/Windows/Linux），UI 组件库集成 `@lobehub/icons`；Web 模式下通过 HTTP API 与后端通信，支持 Docker 容器化部署。  
- **后端**：Rust（Axum 框架），采用异步高性能架构，核心模块包括中间件（鉴权/限流/日志）、模型路由器、账号分发器、多协议请求/响应转换器（Mapper）。  
- **架构与部署**：Tauri（v2）作为桌面容器；Docker 原生支持（含 Headless 模式）；持久化数据存储于本地 `~/.antigravity_tools`；安全机制涵盖 `sessionStorage` 存储敏感密钥、路径遍历防护、IP 黑白名单、设备指纹绑定等。

</details>

---

### 15. [linshenkx/prompt-optimizer](https://github.com/linshenkx/prompt-optimizer)
- 📅 **创建日期**：2025-02-12  
- 🔄 **最近更新**：2026-02-06  
- ⭐ **Stars**：19,350（日 +150｜周 +417｜月 +1021）  
- 📝 **描述**：一款提示词优化器，助力于编写高质量的提示词  

<details>
<summary><b>📈 Star 与 Commit 历史趋势</b></summary>

![prompt-optimizer Star and Commit Trend](charts/linshenkx_prompt-optimizer_trend.png)

> *蓝色：累计 Stars｜橙色：累计 Commits（次 Y 轴）*

</details>

<details>
<summary><b>📄 README 摘要</b></summary>

1. **项目功能**  
Prompt Optimizer（提示词优化器）是一个面向开发者与AI从业者的专业级提示工程（Prompt Engineering）工具，核心目标是**系统性提升提示词质量与AI输出效果**。它不运行大模型，而是通过智能分析、结构化重构与多维度测试，辅助用户将模糊、低效或易失效的原始提示词，优化为高鲁棒性、高可控性、高可复用性的优质提示词。支持三大典型场景：① 角色扮演类提示（激发小模型角色一致性与沉浸感）；② 知识提取/结构化输出类提示（保障生产环境中格式稳定、结果可靠）；③ 创意生成类提示（将灵感精准转化为主题、意象、风格明确的定制化指令）。所有处理均在客户端完成，数据不经过任何中间服务器。

2. **关键特性**  
- **双模智能优化**：独立支持系统提示词（System Prompt）与用户提示词（User Prompt）的针对性优化，适配不同LLM交互范式；  
- **实时对比验证**：并排展示原始提示与优化后提示在相同模型、相同参数下的输出差异，直观量化优化效果；  
- **全栈模型兼容**：原生集成 OpenAI、Gemini、DeepSeek、智谱AI（Zhipu）、SiliconFlow 等主流文本模型，并支持任意 OpenAI 兼容接口（如 Ollama、vLLM）；  
- **图像生成一体化**：内置文生图（T2I）与图生图（I2I）模式，对接 Gemini、Seedream 等图像模型，支持尺寸、风格等细粒度参数调控；  
- **高级测试能力**：提供上下文变量管理（批量替换/预览）、多轮会话模拟、Function Calling 工具调用测试，覆盖真实生产调试需求；  
- **零信任安全架构**：纯前端实现，API密钥仅存于本地（浏览器/桌面应用），请求直连AI服务商，无代理、无日志、无数据留存；  
- **全形态部署支持**：开箱即用的 Web 版（在线/自托管）、跨平台桌面应用（自动更新、无CORS限制）、Chrome插件、Docker容器及 Docker Compose 编排方案；  
- **MCP协议深度集成**：内置符合 Model Context Protocol 标准的 MCP Server，可无缝对接 Claude Desktop 等MCP客户端，提供 `optimize-user-prompt`、`optimize-system-prompt`、`iterate-prompt` 等标准化工具调用能力；  
- **企业级访问控制**：支持密码保护（ACCESS_PASSWORD）与用户名配置，满足私有化部署安全合规要求。

3. **技术栈**  
- **前端框架**：基于 [Vue 3](https://vuejs.org/)（Composition API）构建，采用 [Vite](https://vitejs.dev/) 作为构建工具，[Pinia](https://pinia.vuejs.org/) 管理状态，[Tailwind CSS](https://tailwindcss.com/) 实现响应式UI；  
- **核心语言**：TypeScript（强类型保障复杂提示逻辑与模型参数配置可靠性）；  
- **包管理**：pnpm（高性能、磁盘空间友好）；  
- **桌面端**：使用 [Tauri](https://tauri.app/)（Rust + WebView2/WebKit），替代Electron，实现轻量、安全、原生性能的跨平台桌面应用；  
- **图像生成集成**：通过标准HTTP API对接 Gemini Vision、Seedream 等服务，支持二进制图片上传与Base64流式渲染；  
- **MCP服务层**：基于 Rust 或轻量Node.js HTTP服务（文档指向Docker中与Web同进程运行），遵循 [MCP v0.2+](https://modelcontextprotocol.io/) 规范，提供JSON-RPC 2.0 接口；  
- **部署生态**：全面支持 Vercel（Serverless静态托管）、Docker（多平台容器化）、Docker Compose（含.env配置管理），国内镜像源（阿里云）加速；  
- **开发规范**：遵循严格 LLM 参数抽象设计（`llmParams` 字段统一映射各模型特有参数），模块化架构支持多模型动态加载与热切换。

</details>

---

### 16. [VectifyAI/PageIndex](https://github.com/VectifyAI/PageIndex)
- 📅 **创建日期**：2025-04-01  
- 🔄 **最近更新**：2026-02-06  
- ⭐ **Stars**：18,366（日 +347｜周 +2993｜月 +8971）  
- 📝 **描述**：📑 PageIndex: Document Index for Vectorless, Reasoning-based RAG  

<details>
<summary><b>📈 Star 与 Commit 历史趋势</b></summary>

![PageIndex Star and Commit Trend](charts/VectifyAI_PageIndex_trend.png)

> *蓝色：累计 Stars｜橙色：累计 Commits（次 Y 轴）*

</details>

<details>
<summary><b>📄 README 摘要</b></summary>

1. **项目功能**  
PageIndex 是一个**无向量数据库（vectorless）、基于推理（reasoning-based）的检索增强生成（RAG）系统**，专为长篇专业文档（如财报、法律文件、技术手册、学术教材等）设计。它不依赖传统语义相似度搜索，而是通过构建文档的**分层树状索引（Tree Index）**，并利用大语言模型（LLM）在该索引上执行**类人、多步推理式检索**，实现高精度、可追溯、可解释的知识定位与提取。核心目标是解决传统向量RAG中“相似≠相关”的根本缺陷，以**推理驱动的相关性判断**替代黑箱式的向量近似匹配。

2. **关键特性**  
- **零向量数据库**：完全摒弃向量嵌入、向量存储与相似度检索，不依赖任何向量数据库（如FAISS、Pinecone等）。  
- **零人工分块（No Chunking）**：不将文档切分为固定长度的文本块，而是基于文档天然结构（标题层级、语义段落）自动构建逻辑连贯的节点（nodes），保留上下文完整性。  
- **类人检索能力**：模拟人类专家阅读文档的方式——先理解整体结构（生成类似目录的树索引），再通过推理逐步缩小范围、跳转至最相关章节，支持深度导航与跨节关联分析。  
- **高可解释性与可追溯性**：每次检索结果均附带明确的页面号、节点ID及路径引用，推理过程透明可审计，避免传统RAG中不可解释的“直觉检索”（vibe retrieval）。  
- **原生视觉支持（Vision-based RAG）**：提供OCR-Free方案，可直接对PDF页面图像进行推理式索引与检索，绕过易出错的文本提取环节，保持原始版式与结构语义。  
- **SOTA性能验证**：在金融领域权威基准FinanceBench上达成**98.7%准确率**，显著超越主流向量RAG方案，证实其在专业文档理解任务中的领先性。

3. **技术栈**  
- **核心范式**：Agentic RAG（代理式RAG）、In-context Tree Search（上下文内树搜索）、Reasoning-native Retrieval（推理原生检索）。  
- **模型层**：深度集成OpenAI大模型（默认使用 `gpt-4o-2024-11-20`），用于生成树结构索引、执行树遍历推理及答案合成；支持扩展至其他兼容API的闭源/开源LLM。  
- **文档处理**：基于PDF解析（PyPDF2等）与Markdown结构识别（按`#`层级解析）；配套自研**PageIndex OCR**（未开源但已商用），专为长文档全局结构保真而优化。  
- **部署架构**：提供开源Python CLI工具（`run_pageindex.py`），依赖标准Python生态（`pip`安装）；支持本地自托管、云服务（Chat平台/MCP/API）、企业级私有化部署。  
- **开发与交互**：提供Jupyter Notebook Cookbook（Colab一键运行）、MCP（Model Context Protocol）协议集成（兼容Claude、Cursor等Agent）、RESTful API及详细文档体系（Docs、Blog、Tutorials）。

</details>

---

### 17. [microsoft/agent-lightning](https://github.com/microsoft/agent-lightning)
- 📅 **创建日期**：2025-06-18  
- 🔄 **最近更新**：2026-02-06  
- ⭐ **Stars**：14,126（日 +142｜周 +2244｜月 +4053）  
- 📝 **描述**：The absolute trainer to light up AI agents.  

<details>
<summary><b>📈 Star 与 Commit 历史趋势</b></summary>

![agent-lightning Star and Commit Trend](charts/microsoft_agent-lightning_trend.png)

> *蓝色：累计 Stars｜橙色：累计 Commits（次 Y 轴）*

</details>

<details>
<summary><b>📄 README 摘要</b></summary>

1. **项目功能**  
Agent Lightning 是一个面向 AI 智能体（AI Agent）的通用训练框架，核心目标是**无需修改原有代理代码（近乎零代码改动）即可对任意 AI 代理系统进行高效、可插拔的优化训练**。它不替代用户现有的代理实现，而是以“轻量级注入”方式，在运行时捕获代理行为（如提示词、工具调用、奖励信号等），将其结构化为训练数据，并驱动各类算法（如强化学习、自动提示优化、监督微调等）持续改进代理性能。支持单代理及多代理系统的**选择性优化**（例如仅优化某几个关键角色），适用于从简单链式代理到复杂多智能体协作的全场景。

2. **关键特性**  
- ✅ **零代码/极低侵入性集成**：通过 `agl.emit_xxx()` 辅助函数或自动 tracer 即可接入，无需重构原有代理逻辑；  
- ✅ **框架无关性**：原生兼容 LangChain、OpenAI Agent SDK、AutoGen、CrewAI、Microsoft Agent Framework 等主流框架，也支持裸 Python + OpenAI API 等无框架实现；  
- ✅ **细粒度优化控制**：可在多代理系统中按需指定优化目标（如仅优化 planner 或 verifier），提升训练效率与资源利用率；  
- ✅ **多算法支持**：内置并可扩展集成强化学习（RL）、轨迹级聚合（Trajectory-Level Aggregation）、自动提示优化（APO）、监督微调（SFT）等前沿训练范式；  
- ✅ **统一可观测与数据流架构**：基于 LightningStore 中央存储统一管理任务、资源与行为追踪（spans），实现训练闭环——采集 → 存储 → 算法学习 → 资源更新 → 推理引擎热更新；  
- ✅ **工业级可扩展性验证**：已在腾讯云 Youtu-Agent 项目中实测支持 **128 GPU 规模的稳定 RL 训练**，覆盖数学、代码生成与搜索等复杂任务。

3. **技术栈**  
- **核心语言**：Python（3.9+）；  
- **依赖生态**：深度适配 OpenAI 兼容 API（含 token ID 精确返回）、vLLM 等高性能推理后端；  
- **架构设计**：采用轻量级事件驱动架构，核心组件包括 tracer（行为采集）、LightningStore（结构化数据中枢）、Trainer（训练调度与资源编排）、Algorithm（可插拔算法模块，支持自定义）；  
- **工程保障**：CI/CD 全覆盖（CPU/Full/UI/Examples/Dependency/Legacy 多维度测试），GitHub Actions 自动化验证；  
- **部署与分发**：PyPI 官方发布（`pip install agentlightning`），支持稳定版与 Test PyPI 夜间构建版；  
- **文档与生态**：基于 GitHub Pages 的完整文档站、丰富示例（`./examples`）、活跃 Discord 社区及跨平台博客（Medium / arXiv / Zhihu / vLLM Blog 等）。

</details>

---

### 18. [nvm-sh/nvm](https://github.com/nvm-sh/nvm)
- 📅 **创建日期**：2010-04-15  
- 🔄 **最近更新**：2026-02-06  
- ⭐ **Stars**：12,468（日 +123｜周 +324｜月 +785）  
- 📝 **描述**：Node Version Manager - POSIX-compliant bash script to manage multiple active node.js versions  

<details>
<summary><b>📈 Star 与 Commit 历史趋势</b></summary>

![nvm Star and Commit Trend](charts/nvm-sh_nvm_trend.png)

> *蓝色：累计 Stars｜橙色：累计 Commits（次 Y 轴）*

</details>

<details>
<summary><b>📄 README 摘要</b></summary>

1. **该项目的功能**  
nvm（Node Version Manager）是一个用于在 POSIX 兼容 Shell（如 bash、zsh、ksh、dash）环境下**按用户级管理多个 Node.js 版本**的命令行工具。它允许用户在同一台机器上快速安装、切换、卸载不同版本的 Node.js（包括官方 Node.js 和历史上的 io.js），无需 sudo 权限，且各版本及其全局 npm 包相互隔离。典型场景包括：项目依赖特定 Node 版本时快速切换、测试多版本兼容性、CI/CD 中精准控制运行时环境等。

2. **核心特性**  
- ✅ **多版本共存与即时切换**：支持 `nvm install <version>`、`nvm use <version>`、`nvm alias` 等命令，实现秒级版本切换；  
- ✅ **自动版本管理**：通过 `.nvmrc` 文件声明项目所需 Node 版本，配合 shell 集成（如 `cd` 时自动 `nvm use`）；  
- ✅ **LTS 与别名支持**：内置 `node`（最新稳定版）、`lts/*`（各类长期支持版本）、`iojs` 等语义化别名；  
- ✅ **全局包隔离**：每个 Node 版本拥有独立的 `npm global` 安装目录，避免跨版本冲突；  
- ✅ **镜像源与定制能力**：支持配置国内/私有 Node 二进制镜像（含 Authorization 头）、自定义颜色输出、PATH 恢复机制；  
- ✅ **跨平台兼容**：原生支持 Linux、macOS、WSL；对 Git Bash/Cygwin 提供有限支持；不支持原生 Windows 或 Fish Shell（但提供第三方适配方案）；  
- ✅ **Docker 友好**：提供专为容器（含 CI/CD）优化的安装与环境初始化方案（如 `BASH_ENV` 配置、非交互式 shell 支持）；  
- ✅ **Shell 深度集成**：支持 Bash 补全、Zsh 插件（如 `zsh-nvm`）、自动加载与默认版本设置。

3. **技术栈**  
- **实现语言**：纯 Bash 脚本（POSIX 兼容），无外部运行时依赖；  
- **依赖工具**：安装阶段依赖 `curl` / `wget` / `git`（三者选一即可）；编译安装 Node 时需系统 C++ 编译器（如 `build-essential`、Xcode CLT）及 `libssl-dev`；  
- **运行环境**：要求 POSIX 兼容 Shell（bash/zsh/ksh/dash/sh），不依赖 Node.js 自身（即“零 Node 启动”）；  
- **配置与存储**：所有版本二进制文件默认存放于 `$HOME/.nvm`（支持 XDG Base Directory 规范），配置通过 Shell profile 文件（`.bashrc`/`.zshrc` 等）注入；  
- **分发方式**：以 GitHub 仓库形式托管，通过 `install.sh` 脚本一键克隆部署，版本号（如 `v0.40.4`）严格对应 Git Tag。

</details>

---

### 19. [frankbria/ralph-claude-code](https://github.com/frankbria/ralph-claude-code)
- 📅 **创建日期**：2025-08-27  
- 🔄 **最近更新**：2026-02-06  
- ⭐ **Stars**：10,215（日 +78｜周 +430｜月 +9161）  
- 📝 **描述**：Autonomous AI development loop for Claude Code with intelligent exit detection  

<details>
<summary><b>📈 Star 与 Commit 历史趋势</b></summary>

![ralph-claude-code Star and Commit Trend](charts/frankbria_ralph-claude-code_trend.png)

> *蓝色：累计 Stars｜橙色：累计 Commits（次 Y 轴）*

</details>

<details>
<summary><b>📄 README 摘要</b></summary>

1. **项目功能**  
Ralph for Claude Code 是一个面向 Claude Code 的自主式 AI 软件开发闭环工具，实现“无人值守的迭代式项目构建”：它基于用户提供的需求（如 PRD、GitHub Issues 或任务清单），驱动 Claude Code 持续执行代码编写、修改、测试、构建等操作，直至项目达成完成状态。其核心价值在于将大模型开发流程自动化、结构化和可控化——不是单次调用 API，而是构建可持续、可中断、可恢复、带智能终止判断的完整开发循环。

2. **关键特性**  
- **双条件智能退出机制**：必须同时满足「自然语言完成信号 ≥2 次」+「Claude 显式输出 `EXIT_SIGNAL: true`」才终止循环，杜绝误判与过早退出；  
- **全生命周期会话管理**：支持 `--resume <session_id>` 断点续跑、24 小时（可配置）自动过期、防会话劫持保护；  
- **多重安全熔断机制**：含 API 调用频控（默认 100 次/小时，支持环境变量配置）、5 小时 Claude 使用上限自动检测与交互式等待、无进展循环（3 次）或重复错误（5 次）自动熔断；  
- **结构化任务驱动架构**：通过 `.ralph/PROMPT.md`（目标）、`.ralph/fix_plan.md`（优先级任务）、`.ralph/specs/`（技术细则）、`.ralph/AGENT.md`（构建命令）四层文件体系组织开发逻辑；  
- **开箱即用的工程化能力**：支持 `ralph-enable` 交互式向现有项目注入 Ralph（自动识别 TypeScript/Python/Rust/Go 等技术栈及 Next.js/FastAPI/Django 等框架）、`ralph-import` 多格式需求导入（MD/TXT/JSON/DOCX/PDF）、tmux 实时监控看板、JSON 输出自动降级为文本解析、CI/CD 集成（GitHub Actions）、一键卸载等；  
- **开发者友好体验**：全局 CLI 命令、`.ralphrc` 项目级配置、`--live` 实时流式输出、`--verbose` 进度追踪、`--monitor` 集成终端仪表盘、跨平台兼容（含 macOS Homebrew coreutils 适配）。

3. **技术栈**  
- **主体语言**：Bash Shell（核心逻辑全部基于 POSIX 兼容 Shell 脚本实现，轻量、可移植、无运行时依赖）；  
- **AI 接口层**：深度集成 Claude Code CLI（非通用 Anthropic API），专为 Claude Code 的输出格式（含 RALPH_STATUS 块、JSON 模式、多行错误匹配等）定制解析与响应分析；  
- **配置与数据格式**：Markdown（PROMPT/fix_plan/AGENT）、JSON（CLI 输出与错误处理）、Shell 变量语法（`.ralphrc`）；  
- **基础设施**：GitHub Actions（CI/CD 测试流水线）、tmux（实时监控终端复用）、Git（进度检测与防卡死）、jq（JSON 处理）、coreutils（跨平台日期/文本处理）；  
- **部署模型**：本地 CLI 工具（无服务器、无云依赖），所有状态与上下文持久化至项目内 `.ralph/` 目录，完全离线可控。

</details>

---

### 20. [fish-shell/fish-shell](https://github.com/fish-shell/fish-shell)
- 📅 **创建日期**：2012-05-10  
- 🔄 **最近更新**：2026-02-06  
- ⭐ **Stars**：8,796（日 +120｜周 +210｜月 +423）  
- 📝 **描述**：The user-friendly command line shell.  

<details>
<summary><b>📈 Star 与 Commit 历史趋势</b></summary>

![fish-shell Star and Commit Trend](charts/fish-shell_fish-shell_trend.png)

> *蓝色：累计 Stars｜橙色：累计 Commits（次 Y 轴）*

</details>

---

### 21. [NevaMind-AI/memU](https://github.com/NevaMind-AI/memU)
- 📅 **创建日期**：2025-07-29  
- 🔄 **最近更新**：2026-02-06  
- ⭐ **Stars**：7,884（日 +230｜周 +1847｜月 +4488）  
- 📝 **描述**：Memory for 24/7 proactive agents like openclaw (moltbot, clawdbot).  

<details>
<summary><b>📈 Star 与 Commit 历史趋势</b></summary>

![memU Star and Commit Trend](charts/NevaMind-AI_memU_trend.png)

> *蓝色：累计 Stars｜橙色：累计 Commits（次 Y 轴）*

</details>

<details>
<summary><b>📄 README 摘要</b></summary>

1. **该项目做什么？**  
memU 是一个专为 **7×24 小时持续运行的主动式 AI 代理（Proactive Agents）** 设计的记忆框架。它不依赖用户显式指令，而是持续监听、理解并记忆用户行为、对话、文档、邮件、交易等多模态交互数据，自动提取意图、偏好、技能、关系与知识，构建结构化、可演化的长期记忆。其核心目标是让 AI 代理真正“永不休眠、永不遗忘”，并在用户提出请求前就预判需求、主动执行任务（如推荐内容、起草邮件、触发交易警报），同时显著降低大语言模型（LLM）在长期在线场景下的 token 消耗。

2. **关键特性：**  
- **全天候主动记忆（24/7 Proactive Memory）**：后台持续监控输入/输出流，自动完成记忆采集、分类、关联与预测，无需人工触发；  
- **类文件系统记忆架构**：将记忆组织为 `categories`（目录）、`items`（文件）、`resources`（挂载源）和 `symlinks`（交叉引用），支持层级导航、即时挂载新知识、跨记忆图谱链接及文件级导出/迁移；  
- **双模态智能检索**：  
  - *RAG 模式*：毫秒级向量检索，适用于实时上下文组装与背景监控；  
  - *LLM 模式*：深度意图推理与查询演化，支持前瞻性任务预判与自动终止；  
- **成本优化机制**：通过缓存结构化洞察、避免重复 LLM 调用、优先使用轻量嵌入计算，大幅削减长周期 token 开销；  
- **多场景主动能力**：原生支持信息推荐（基于阅读/搜索历史）、智能邮件管理（自动生成回复、识别冲突、摘要线程）、金融交易监控（结合风险偏好与市场事件触发操作建议）等落地用例；  
- **全栈可定制性**：支持 OpenAI、阿里云 Qwen、Voyage AI、OpenRouter 等多 LLM/Embedding 提供商，兼容 in-memory、PostgreSQL+pgvector 等多种存储后端。

3. **技术栈：**  
- **编程语言**：Python 3.13+（强类型、异步优先）；  
- **核心依赖**：`asyncio`（异步流水线）、`pydantic`（Schema 验证）、`litellm` 或原生 SDK（LLM 抽象层）、`pgvector`（向量扩展，可选）、`httpx`（高性能 HTTP 客户端）；  
- **记忆存储**：支持内存（in-memory）、PostgreSQL（含 pgvector 向量索引）、未来可扩展至其他向量/图数据库；  
- **模型生态**：无缝集成 OpenAI（GPT / Embeddings）、Anthropic（Claude）、Qwen（通义千问）、Voyage AI、OpenRouter（统一接入 100+ 模型）；  
- **部署形态**：提供云服务（memu.so）、本地 Docker（PostgreSQL）、纯 Python 包（`pip install -e .`）三种部署方式，API 设计遵循 RESTful 规范（v3），支持细粒度作用域过滤（如 `user_id`、`agent_id`）。

</details>

---

### 22. [badlogic/pi-mono](https://github.com/badlogic/pi-mono)
- 📅 **创建日期**：2025-08-09  
- 🔄 **最近更新**：2026-02-06  
- ⭐ **Stars**：7,198（日 +506｜周 +3743｜月 +5959）  
- 📝 **描述**：AI agent toolkit: coding agent CLI, unified LLM API, TUI & web UI libraries, Slack bot, vLLM pods  

<details>
<summary><b>📈 Star 与 Commit 历史趋势</b></summary>

![pi-mono Star and Commit Trend](charts/badlogic_pi-mono_trend.png)

> *蓝色：累计 Stars｜橙色：累计 Commits（次 Y 轴）*

</details>

<details>
<summary><b>📄 README 摘要</b></summary>

1. **项目功能**  
该项目是一个面向AI智能体（Agent）开发与大语言模型（LLM）部署管理的工具型单体仓库（Monorepo），核心目标是提供一套模块化、可组合的基础设施，支持构建和运行各类AI代理系统——尤其是以编程为核心的交互式AI助手（如 `pi-coding-agent`）。它不直接提供终端用户产品，而是为开发者提供底层能力：统一调用多厂商LLM、运行时状态与工具调用管理、终端/Web界面渲染、GPU集群上的vLLM推理服务编排，以及企业协作场景（如Slack集成）的轻量级适配。

2. **关键特性**  
- **多厂商LLM统一抽象层**（`@mariozechner/pi-ai`）：屏蔽OpenAI、Anthropic、Google等不同API差异，提供一致接口与错误处理。  
- **可扩展的Agent运行时核心**（`@mariozechner/pi-agent-core`）：内置工具调用（function calling）、会话状态持久化、执行流程控制，支持自定义插件与行为策略。  
- **开箱即用的编程助手CLI**（`@mariozechner/pi-coding-agent`）：面向开发者的一站式终端编码代理，支持文件操作、代码生成、调试建议等。  
- **跨平台UI支持**：包含高性能终端UI库（`pi-tui`，支持差分渲染避免闪烁）和可复用Web组件（`pi-web-ui`），便于快速构建AI聊天界面。  
- **生产就绪的LLM部署工具**（`pi-pods`）：命令行工具，用于在GPU服务器/云Pod上一键部署、扩缩容及监控vLLM推理服务。  
- **企业协作集成**（`pi-mom`）：轻量Slack机器人，将用户消息自动路由至编码Agent并返回结果，实现“对话即服务”。

3. **技术栈**  
- **语言与运行时**：TypeScript（全栈主导）、Node.js（后端/CLI）、Rust（部分性能敏感模块可能预留扩展接口，但当前未显式声明；主仓库以TS为主）  
- **前端框架**：无重型框架依赖；`pi-tui` 基于ANSI转义序列实现原生终端渲染；`pi-web-ui` 提供标准Web Components（Custom Elements + Shadow DOM），兼容任意前端框架。  
- **构建与包管理**：npm Workspaces（单体仓库管理）、TypeScript（类型系统与编译）、ESBuild（推测用于快速构建，虽未明写但符合生态惯例）  
- **测试与质量**：Jest或Vitest（未明确，但`./test.sh`表明存在单元/集成测试）、ESLint + Prettier（`npm run check`含lint/format/type-check）  
- **部署与推理**：深度集成vLLM（作为首选开源推理引擎），面向GPU加速场景；支持通过CLI（`pi-pods`）进行容器化部署与生命周期管理。  
- **基础设施**：GitHub Actions（CI流水线）、Discord（社区协作）、MIT许可证。

</details>

---

### 23. [anthropics/claude-plugins-official](https://github.com/anthropics/claude-plugins-official)
- 📅 **创建日期**：2025-11-20  
- 🔄 **最近更新**：2026-02-06  
- ⭐ **Stars**：6,642（日 +142｜周 +1272｜月 +4855）  
- 📝 **描述**：Official, Anthropic-managed directory of high quality Claude Code Plugins.  

<details>
<summary><b>📈 Star 与 Commit 历史趋势</b></summary>

![claude-plugins-official Star and Commit Trend](charts/anthropics_claude-plugins-official_trend.png)

> *蓝色：累计 Stars｜橙色：累计 Commits（次 Y 轴）*

</details>

<details>
<summary><b>📄 README 摘要</b></summary>

1. **该项目的功能**  
该项目是一个为 Claude Code（Anthropic 推出的 AI 编程助手）提供插件支持的官方插件目录（市场），用于集中托管、分发和管理高质量插件。它本身不运行插件，而是作为权威的插件索引与分发平台，支持用户通过命令行（如 `/plugin install {plugin-name}@claude-plugin-directory`）或图形界面（`/plugin > Discover`）一键安装插件，并为插件开发者（包括 Anthropic 内部团队与经审核的第三方）提供标准化的提交与发布流程。

2. **核心特性**  
- **双源分类管理**：明确区分 `/plugins`（Anthropic 官方开发与维护的内部插件）和 `/external_plugins`（经安全与质量审核的第三方合作伙伴及社区插件）；  
- **标准化插件结构**：强制要求每个插件包含 `.claude-plugin/plugin.json`（必需元数据文件），并支持可选的 MCP 服务配置（`.mcp.json`）、Slash 命令（`commands/`）、智能体定义（`agents/`）和技能定义（`skills/`），确保兼容性与可扩展性；  
- **可信度优先机制**：显著强调安全警示，明确告知用户插件内容不受 Anthropic 控制，需自行评估风险，并引导用户查阅各插件主页获取详情；  
- **规范化贡献流程**：为内部团队提供参考实现（如 `/plugins/example-plugin`），为外部开发者提供标准化提交入口（在线表单）及明确的准入标准（质量与安全性）；  
- **开箱即用集成**：深度集成 Claude Code 原生插件系统，支持命令行快速安装与 UI 可视化发现，降低用户使用门槛。

3. **技术栈**  
- **协议与规范层**：基于 Anthropic 定义的 **Claude Plugin 协议** 和 **MCP（Model Control Protocol）标准**，其中 `.mcp.json` 文件用于声明模型交互能力与服务端点；  
- **元数据格式**：采用 JSON 格式定义插件核心信息（`plugin.json`），涵盖名称、版本、权限、功能描述等；  
- **组织结构**：纯静态目录结构（Git 仓库管理），无后端服务，依赖 Claude Code 客户端解析和执行插件清单；  
- **开发与分发基础设施**：依托 Anthropic 的插件运行时环境、Claude Code IDE 客户端、以及官方文档平台（`code.claude.com/docs/en/plugins`）提供完整开发支持。

</details>

---

### 24. [MoonshotAI/kimi-cli](https://github.com/MoonshotAI/kimi-cli)
- 📅 **创建日期**：2025-10-15  
- 🔄 **最近更新**：2026-02-06  
- ⭐ **Stars**：6,053（日 +93｜周 +1115｜月 +2306）  
- 📝 **描述**：Kimi Code CLI is your next CLI agent.  

<details>
<summary><b>📈 Star 与 Commit 历史趋势</b></summary>

![kimi-cli Star and Commit Trend](charts/MoonshotAI_kimi-cli_trend.png)

> *蓝色：累计 Stars｜橙色：累计 Commits（次 Y 轴）*

</details>

<details>
<summary><b>📄 README 摘要</b></summary>

1. **项目功能**  
Kimi Code CLI 是一个运行在终端中的 AI 智能体（AI agent），专为软件开发任务和终端操作而设计。它能够自主阅读与编辑代码文件、执行 Shell 命令、搜索并抓取网页内容，并在运行过程中动态规划、调整执行策略，实现端到端的自动化开发辅助。

2. **核心特性**  
- **Shell 命令模式**：通过 `Ctrl-X` 快捷键切换至原生 Shell 模式，直接执行任意外部命令（注：暂不支持内置命令如 `cd`）；  
- **VS Code 扩展集成**：提供官方 VS Code 插件，实现 IDE 内无缝调用 Kimi Code CLI；  
- **ACP（Agent Client Protocol）标准兼容**：开箱即支持 ACP 协议，可与 Zed、JetBrains 等 ACP 兼容 IDE 集成，通过配置 `kimi acp` 启动为代理服务器；  
- **Zsh 深度集成**：提供 `zsh-kimi-cli` 插件，将 AI 能力嵌入日常 Zsh 工作流，同样支持 `Ctrl-X` 切换智能体模式；  
- **MCP（Model Context Protocol）支持**：  
  - 提供 `kimi mcp` 子命令组，用于添加/删除/授权/管理 HTTP 或 stdio 类型的 MCP 工具服务器（如 Context7、Linear、Chrome DevTools）；  
  - 支持通过 `--mcp-config-file` 参数加载 JSON 格式的 MCP 配置文件，实现灵活、声明式的工具集成。

3. **技术栈**  
- **主语言**：Python（项目基于 Python 构建，使用 `uv` 作为现代 Python 包与环境管理工具）；  
- **协议标准**：原生支持 [Agent Client Protocol (ACP)](https://github.com/agentclientprotocol/agent-client-protocol) 和 [Model Context Protocol (MCP)](https://modelcontextprotocol.io/)；  
- **构建与发布**：使用 `make` 统一管理开发流程（含格式化、类型检查、多模块测试、Web UI 构建、Python 包打包及独立二进制文件生成）；Web UI 构建依赖 Node.js/npm；  
- **扩展生态**：与 Zsh（Oh My Zsh 插件）、VS Code（Marketplace 插件）、Zed、JetBrains IDE 等主流开发工具深度协同，体现跨平台、协议驱动的架构设计。

</details>

---

### 25. [j178/prek](https://github.com/j178/prek)
- 📅 **创建日期**：2024-10-07  
- 🔄 **最近更新**：2026-02-06  
- ⭐ **Stars**：5,514（日 +288｜周 +1503｜月 +2442）  
- 📝 **描述**：⚡ Better `pre-commit`, re-engineered in Rust  

<details>
<summary><b>📈 Star 与 Commit 历史趋势</b></summary>

![prek Star and Commit Trend](charts/j178_prek_trend.png)

> *蓝色：累计 Stars｜橙色：累计 Commits（次 Y 轴）*

</details>

<details>
<summary><b>📄 README 摘要</b></summary>

1. **项目功能**  
prek 是一个用 Rust 重写的 `pre-commit` 替代工具，专为运行代码检查、格式化等 Git 钩子（hooks）而设计。它完全兼容原生 `pre-commit` 的配置文件（如 `.pre-commit-config.yaml`）和钩子生态，可作为零修改迁移的“即插即用”替代方案；核心目标是取代 Python 编写的 `pre-commit`，提供更高性能、更低资源开销，并原生支持现代开发工作流（如单体仓库/monorepo、多语言工具链统一管理）。

2. **关键特性**  
- ✅ **零依赖单二进制**：无需预装 Python、Node.js 等运行时，下载即用；  
- ✅ **显著性能提升**：比 `pre-commit` 快数倍，磁盘占用减半，支持并行克隆/安装/执行钩子；  
- ✅ **全配置兼容**：无缝复用现有 `.pre-commit-config.yaml`，支持 `repo: local`、`repo: https://...` 等全部语法；  
- ✅ **原生 monorepo 支持**：内置 workspace 模式，允许多个子项目各自拥有独立配置；  
- ✅ **智能工具链管理**：统一缓存并共享 Python（通过 `uv`）、Node.js、Bun、Go、Rust、Ruby 等语言环境，避免重复安装；  
- ✅ **Rust 原生内置钩子**：提供 `trailing-whitespace`、`end-of-file-fixer` 等常用钩子的高性能 Rust 实现，支持离线 `repo: builtin`；  
- ✅ **增强 CLI 体验**：支持 `prek run --directory`、`--last-commit`、多钩子选择执行、`prek list` 可读性列表、`prek auto-update --cooldown-days` 防供应链攻击等实用功能；  
- ✅ **广泛分发支持**：提供 standalone 脚本、PyPI（`uv tool install`）、Homebrew、npm、Cargo、Nix、Conda、Scoop、MacPorts 等全平台安装方式，并支持 GitHub Actions。

3. **技术栈**  
- **主语言**：Rust（1.89+），强调内存安全、零成本抽象与高性能；  
- **核心依赖**：无外部运行时依赖（不依赖 Python/Node.js）；  
- **关键集成**：深度集成 [`uv`](https://github.com/astral-sh/uv)（用于极速 Python 虚拟环境创建与包安装）；  
- **构建与分发**：使用 `cargo` 构建，通过 `cargo-binstall`、GitHub Releases、Nixpkgs、conda-forge 等多渠道发布预编译二进制；  
- **跨平台支持**：原生支持 Linux、macOS、Windows（含 PowerShell 安装脚本及 Scoop）；  
- **生态兼容层**：解析 YAML 配置、调用各类语言钩子（Python/Shell/Node/Rust 等）、与 Git 深度交互，同时保持对 `pre-commit` 协议的严格兼容。

</details>

---

### 26. [aquasecurity/trivy](https://github.com/aquasecurity/trivy)
- 📅 **创建日期**：2019-04-11  
- 🔄 **最近更新**：2026-02-06  
- ⭐ **Stars**：4,678（日 +100｜周 +202｜月 +562）  
- 📝 **描述**：Find vulnerabilities, misconfigurations, secrets, SBOM in containers, Kubernetes, code repositories, clouds and more  

<details>
<summary><b>📈 Star 与 Commit 历史趋势</b></summary>

![trivy Star and Commit Trend](charts/aquasecurity_trivy_trend.png)

> *蓝色：累计 Stars｜橙色：累计 Commits（次 Y 轴）*

</details>

<details>
<summary><b>📄 README 摘要</b></summary>

1. **项目功能**  
Trivy 是一款全面、轻量且高可用的开源安全扫描工具，专注于在软件开发生命周期（SDLC）各阶段主动识别和报告安全风险。它能够对多种目标（如容器镜像、本地文件系统、远程 Git 仓库、虚拟机镜像、Kubernetes 集群）执行多维度安全检测，覆盖从底层操作系统组件到上层应用配置的全栈风险面。

2. **核心功能**  
- **多目标扫描支持**：原生支持容器镜像、本地文件系统（`fs`）、Git 远程仓库、VM 镜像（如 VMDK/OVA）及 Kubernetes 集群（通过 `k8s` 子命令）。  
- **多类型安全扫描器**：  
  - **SBOM 生成与分析**：自动识别 OS 包和语言级依赖（如 Python pip、Node.js npm、Java Maven 等），输出软件物料清单；  
  - **漏洞扫描（CVE）**：实时检测已知操作系统和应用依赖中的安全漏洞，支持 NVD、Red Hat、Alpine、Debian 等多个数据源；  
  - **IaC 安全与配置审计**：检查 Terraform、Kubernetes YAML、Dockerfile、CloudFormation 等基础设施即代码中的策略违规与误配置（基于 Rego 规则）；  
  - **敏感信息检测**：识别硬编码密钥、密码、API tokens、私钥等泄露风险；  
  - **许可证合规性分析**：检测第三方组件所用开源许可证，辅助合规审查。  
- **高度可集成**：提供 CLI、Docker 镜像、GitHub Actions 插件、Kubernetes Operator、VS Code 扩展等多种形态，无缝嵌入 CI/CD 和开发环境；  
- **快速启动与标准化使用**：命令行接口简洁统一（`trivy <target> [options] <subject>`），支持按需启用/禁用扫描器组合（如 `--scanners vuln,secret,misconfig`）。

3. **技术栈**  
- **编程语言**：Go（Golang），保障高性能、静态编译、跨平台二进制分发能力；  
- **依赖管理**：Go Modules；  
- **漏洞数据库**：集成并定期同步多个权威数据源（NVD、OSV、Alpine SecDB、Debian Security Tracker、RHEL/CentOS 等），支持离线模式与自定义数据库；  
- **IaC 扫描引擎**：基于 Open Policy Agent（OPA）的 Rego 策略语言实现灵活、可扩展的配置合规检查；  
- **构建与分发**：GitHub Actions 自动化测试与发布、Docker Hub / ECR / GitHub Container Registry 多渠道镜像托管、预编译二进制（Linux/macOS/Windows）；  
- **许可证**：Apache License 2.0。

</details>

---

### 27. [openai/skills](https://github.com/openai/skills)
- 📅 **创建日期**：2025-11-25  
- 🔄 **最近更新**：2026-02-06  
- ⭐ **Stars**：4,277（日 +593｜周 +2105｜月 +3033）  
- 📝 **描述**：Skills Catalog for Codex  

<details>
<summary><b>📈 Star 与 Commit 历史趋势</b></summary>

![skills Star and Commit Trend](charts/openai_skills_trend.png)

> *蓝色：累计 Stars｜橙色：累计 Commits（次 Y 轴）*

</details>

<details>
<summary><b>📄 README 摘要</b></summary>

1. **项目功能**  
该项目是一个面向 AI 代理（AI agents）的技能（Skills）标准化仓库，旨在为 Codex 平台提供可复用、可发现、可分发的任务能力包。每个“技能”是一组结构化文件（含指令、脚本、资源等），封装了完成特定任务所需的全部逻辑与上下文；用户“编写一次”，即可在支持 Agent Skills 标准的各类 AI 代理环境中跨平台复用。

2. **核心特性**  
- **标准化技能目录结构**：按用途划分为 `.system`（系统预置）、`.curated`（人工审核精选）、`.experimental`（实验性技能）三类，便于分类管理与可信度分级；  
- **一键式技能安装机制**：通过内置命令 `$skill-installer` 支持按名称、本地路径或 GitHub 直链安装技能，降低集成门槛；  
- **即插即用与热更新支持**：`.system` 技能自动加载；其他技能安装后仅需重启 Codex 即可生效；  
- **开放标准兼容性**：遵循 [Agent Skills 开放标准](https://agentskills.io)，确保跨平台互操作性与社区协作扩展性；  
- **细粒度版权管理**：每个技能目录内独立附带 `LICENSE.txt`，实现技能级许可证透明化。

3. **技术栈**  
- **运行平台**：深度集成于 OpenAI Codex（AI 编程与代理环境）；  
- **技能格式**：基于文件系统组织的纯文本/脚本资源（如 Markdown 指令、Shell/Python 脚本、JSON 配置等），无强制编程语言或框架依赖；  
- **分发与安装**：依托 GitHub 代码托管（支持直接解析 `tree/` URL 安装），配合 Codex 内置 CLI 工具 `$skill-installer` 实现技能生命周期管理；  
- **标准协议**：遵循 [Agent Skills 开放规范](https://agentskills.io)，属轻量级、协议无关的元数据与目录结构约定。

</details>

---

### 28. [topoteretes/cognee](https://github.com/topoteretes/cognee)
- 📅 **创建日期**：2023-08-16  
- 🔄 **最近更新**：2026-02-06  
- ⭐ **Stars**：4,107（日 +152｜周 +387｜月 +1075）  
- 📝 **描述**：Memory for AI Agents in 6 lines of code  

<details>
<summary><b>📈 Star 与 Commit 历史趋势</b></summary>

![cognee Star and Commit Trend](charts/topoteretes_cognee_trend.png)

> *蓝色：累计 Stars｜橙色：累计 Commits（次 Y 轴）*

</details>

<details>
<summary><b>📄 README 摘要</b></summary>

1. **项目功能**  
Cognee 是一个开源的 AI 记忆平台，旨在将用户原始数据（如文档、对话记录、文件、图像描述、音频转录等）转化为**持久化、可演化、语义化**的 AI 代理（AI Agents）记忆层。它不依赖传统 RAG（检索增强生成）范式，而是通过构建动态知识图谱（graph database）与向量索引（vector search）深度融合的记忆系统，使 AI 不仅能“按意义检索”，还能“按关系推理”，从而实现更准确、可追溯、可解释的长期记忆能力。

2. **核心特性**  
- **ECL 统一数据管道**：采用 Extract（抽取）、Cognify（认知建模/图谱构建）、Load（加载/索引）三阶段流程，替代碎片化 RAG 架构；  
- **多模态数据融合**：原生支持文本、PDF、Markdown、网页、音频转录、图像描述、聊天历史等多种数据类型；  
- **图+向量双引擎检索**：同时利用知识图谱的关系推理能力与向量嵌入的语义匹配能力，提升搜索精度与上下文连贯性；  
- **高度可定制化**：提供 Pythonic API、CLI 工具及模块化任务接口，支持用户自定义提取逻辑、图谱模式（schema）、记忆算法（memify）和搜索策略；  
- **开箱即用的轻量部署**：5 行代码即可完成数据注入、图谱构建与语义查询；支持本地 UI（`cognee-cli -ui`）与 Colab 快速验证；  
- **生态扩展友好**：通过社区插件仓库（cognee-community）支持第三方数据源接入、LLM 适配器（OpenAI/Ollama 等）及领域专用记忆模块。

3. **技术栈**  
- **语言与框架**：Python（3.10–3.13），基于异步编程（`asyncio`）设计；  
- **核心存储**：混合使用图数据库（如 Neo4j 或内置轻量图引擎）与向量数据库（如 Qdrant、Chroma 或 Weaviate）；  
- **AI 基础设施**：集成主流 LLM 接口（默认 OpenAI，支持 Ollama、Anthropic 等 via 配置），用于文本理解、实体识别、关系抽取与图谱生成；  
- **数据处理**：内置 30+ 数据源连接器（Web、Notion、Obsidian、RSS、本地文件等），基于 Pydantic 模型与 LangChain-style 模块化处理器；  
- **运维与部署**：支持 `.env` 环境配置、Poetry/UV 包管理、Docker 可选封装；前端 UI 基于简易 Web 框架（未明示但 CLI `-ui` 启动本地服务）；  
- **基础设施协议**：遵循开源许可（MIT），代码托管于 GitHub，文档托管于 docs.cognee.ai，社区协作通过 Discord、Reddit 和插件仓库推进。

</details>

---

### 29. [ThePrimeagen/99](https://github.com/ThePrimeagen/99)
- 📅 **创建日期**：2025-11-22  
- 🔄 **最近更新**：2026-02-06  
- ⭐ **Stars**：3,365（日 +92｜周 +2204｜月 +2411）  
- 📝 **描述**：Neovim AI agent done right  

<details>
<summary><b>📈 Star 与 Commit 历史趋势</b></summary>

![99 Star and Commit Trend](charts/ThePrimeagen_99_trend.png)

> *蓝色：累计 Stars｜橙色：累计 Commits（次 Y 轴）*

</details>

<details>
<summary><b>📄 README 摘要</b></summary>

1. **项目功能**  
该项目（`99`）是一个面向 Neovim 的轻量级 AI 编程代理框架，旨在为**已具备扎实编程技能的开发者**提供受控、可预测、上下文感知的 AI 辅助体验。它不替代通用 AI 编程工具（如 OpenCode），而是聚焦于**限定范围内的高信噪比操作**：例如根据当前函数签名自动补全函数体（`fill_in_function`）、基于视觉选区生成/修改代码（`visual`）、或通过自定义规则（`SKILL.md`）触发特定行为（如插入调试语句）。其核心设计哲学是“限制请求范围、强化意图表达”，要求用户显式以 `@` 符号触发技能补全，并依赖项目级 `AGENT.md` 和用户定义的 `SKILL.md` 文件来约束 AI 行为边界。

2. **关键特性**  
- **结构化技能系统（Skill-based Completion）**：支持从指定目录（如 `scratch/custom_rules/`）自动加载 `SKILL.md` 文件，每个文件定义一个可被 `@` 触发的原子能力（如 `@vim`、`@debug`），实现行为可插拔与场景化定制。  
- **上下文感知自动注入**：基于当前文件路径与工作目录（cwd），自动向上查找并注入同级/父级目录中的 `AGENT.md`，为 AI 请求提供项目专属上下文（如架构约束、编码规范）。  
- **Neovim 原生集成工作流**：提供开箱即用的键位绑定（如 `<leader>9f` 补全函数、`<leader>9v` 处理选区），支持日志追踪（`view_logs`/`prev_request_logs`）、请求中断（`stop_all_requests`）等调试能力。  
- **语言与规则双驱动**：当前原生支持 TypeScript 和 Lua，通过 Tree-sitter 解析代码结构以提升定位精度；同时预留扩展接口，未来计划融合 LSP 与 FIM（Fill-in-the-Middle）模型优化上下文提取效率。  
- **严格的安全与隐私意识**：日志系统明确警示需手动脱敏 `query` 字段，避免敏感信息泄露；所有 AI 请求均在本地配置约束下执行，无隐式云端调用。

3. **技术栈**  
- **运行时环境**：Neovim（≥0.9） + Lua 5.1+（主逻辑实现语言）  
- **前端框架**：Lazy.nvim（插件管理）、cmp（补全引擎，当前唯一支持的补全源）  
- **语言解析**：Tree-sitter（用于代码结构分析、选区内容提取、函数体定位）  
- **AI 接口层**：依赖外部工具 `opencode`（作为底层大模型调用入口，具体模型未指定，由用户自行配置）  
- **配置与规则系统**：纯文本 Markdown（`AGENT.md`、`SKILL.md`）定义行为契约，路径匹配逻辑基于 `vim.fs.basename` 和 `vim.uv.cwd()` 实现项目根目录推导  
- **日志与调试**：异步文件写入（`/tmp/xxx.99.debug`）、内置日志导航 API（`prev_request_logs`/`next_request_logs`）

</details>

---

### 30. [disler/claude-code-hooks-mastery](https://github.com/disler/claude-code-hooks-mastery)
- 📅 **创建日期**：2025-07-05  
- 🔄 **最近更新**：2026-02-06  
- ⭐ **Stars**：2,555（日 +194｜周 +431｜月 +534）  
- 📝 **描述**：Master Claude Code Hooks  

<details>
<summary><b>📈 Star 与 Commit 历史趋势</b></summary>

![claude-code-hooks-mastery Star and Commit Trend](charts/disler_claude-code-hooks-mastery_trend.png)

> *蓝色：累计 Stars｜橙色：累计 Commits（次 Y 轴）*

</details>

<details>
<summary><b>📄 README 摘要</b></summary>

1. **项目功能**  
该项目是一个面向 Anthropic Claude Code CLI 的深度定制化增强套件，专注于通过官方支持的 **Claude Code Hooks（钩子）机制**，对 AI 编程工作流实施**确定性、可编程、细粒度的行为控制**。它不依赖大模型自身决策，而是利用 13 类生命周期钩子，在用户输入、工具调用、子代理执行、会话管理等关键节点插入自定义逻辑，实现安全拦截、上下文注入、多模态反馈（TTS）、日志审计、代码质量验证、团队协作式构建/校验（Builder/Validator 模式）及智能状态可视化等功能，本质是为 Claude Code 构建一套可扩展、可维护、生产就绪的“操作系统级”控制层。

2. **核心特性**  
- **全生命周期钩子覆盖**：完整实现并验证全部 13 个 Claude Code 钩子（如 `UserPromptSubmit`、`PreToolUse`、`PostToolUse`、`SubagentStart/Stop`、`SessionStart/End` 等），支持拦截、阻断、修改、记录与增强；  
- **确定性安全控制**：在 `PreToolUse` 等钩子中实时阻断高危命令（如 `rm -rf`、`.env` 访问、`sudo`、写系统目录），支持正则匹配与结构化决策（`"decision": "block"`）；  
- **智能多模态交互**：集成 ElevenLabs / OpenAI / pyttsx3 的 TTS 系统，支持语音播报通知、完成提示与子代理状态，并通过 `tts_queue.py` 实现音频防重叠；  
- **团队化验证架构（Team-Based Validation）**：基于 Sub-Agents 实现 Builder（全权限执行）与 Validator（只读校验）分离的双角色工作流，配合 Ruff（Python linting）和类型检查（`ty_validator.py`）等钩子实现自动化代码质量门禁；  
- **元代理（Meta-Agent）与动态代理编排**：支持 `meta-agent.md` 自动创建/配置新子代理，并通过 `plan_w_team.md` 等自定义指令触发多代理协同；  
- **全栈可观测性**：自动将 JSONL 会话日志转为可读 `chat.json`，所有钩子事件以结构化 JSON 形式持久化至 `logs/` 目录；提供 9 代演进的终端状态行（`status_line_v1–v9`），支持 Git 状态、上下文窗口、Token 使用、缓存命中率、成本估算等实时指标；  
- **输出样式即服务（Output Styles Collection）**：预置 8 种响应格式模板（HTML、表格、YAML、极简文本、语义 HTML5 等），支持按需切换输出形态；  
- **UV 单文件脚本架构**：所有钩子均为独立 `.py` 脚本，内嵌依赖声明，由 Astral UV 自动解析与执行，实现零虚拟环境、强隔离、高便携性。

3. **技术栈**  
- **核心运行时**：`Astral UV`（作为 Python 包管理器与单文件脚本执行引擎） + `Claude Code CLI`（Anthropic 官方 CLI）；  
- **语言模型后端**：`OpenAI`（优先级最高）、`Anthropic`（原生兼容）、`Ollama`（本地 LLM）、`ElevenLabs`（TTS）；  
- **工具链与验证**：`Ruff`（Python 代码规范检查）、`ty`（Python 类型检查）、`Firecrawl MCP Server`（网页爬取）、`ElevenLabs MCP Server`（MCP 协议 TTS 集成）；  
- **开发与工程实践**：`Git`（上下文感知）、`ruff.toml` / `ty.toml`（配置驱动）、`Mermaid`（文档流程图）、`JSONL` → `JSON` 转换管道；  
- **架构范式**：基于 MCP（Model Context Protocol）的模块化代理系统、Hook 驱动的事件总线、队列化 TTS（`tts_queue.py`）、状态行版本化演进（v1–v9）、自定义 Slash 命令（`/prime`、`/plan_w_team` 等）。

</details>

---

### 31. [microsoft/playwright-cli](https://github.com/microsoft/playwright-cli)
- 📅 **创建日期**：2020-06-19  
- 🔄 **最近更新**：2026-02-06  
- ⭐ **Stars**：2,272（日 +68｜周 +598｜月 +1255）  
- 📝 **描述**：CLI for common Playwright actions. Record and generate Playwright code, inspect selectors and take screenshots.  

<details>
<summary><b>📈 Star 与 Commit 历史趋势</b></summary>

![playwright-cli Star and Commit Trend](charts/microsoft_playwright-cli_trend.png)

> *蓝色：累计 Stars｜橙色：累计 Commits（次 Y 轴）*

</details>

<details>
<summary><b>📄 README 摘要</b></summary>

1. **项目功能**  
该项目是一个专为**AI 编程代理（coding agents）**设计的命令行工具（CLI），提供对 Playwright 浏览器自动化能力的轻量级、低开销接口。它不依赖传统 MCP（Model Control Protocol）协议，而是通过简洁、语义明确的 CLI 命令（即“SKILLs”）让 LLM 驱动的编码代理直接操控浏览器，完成网页导航、交互、状态管理、网络拦截、截图/PDF 生成、会话持久化等端到端自动化任务。核心目标是**在有限上下文窗口内高效执行浏览器操作**，避免将冗长的页面结构、工具 Schema 或可访问性树注入大模型提示中，从而提升 token 利用率与执行吞吐量。

2. **关键特性**  
- **极致 Token 友好**：所有命令均无隐式数据回传，不强制将 DOM/页面状态注入 LLM 上下文，仅返回必要结果（如元素引用 `ref`、成功状态、文件路径等）。  
- **技能即 CLI 命令（SKILLs）**：内置超 60 个细粒度命令，覆盖核心交互（`click`/`type`/`fill`/`check`）、导航（`go-back`/`reload`）、键盘鼠标（`press`/`mousemove`）、存储（Cookie/LocalStorage/SessionStorage 管理）、网络（`route`/`unroute` 拦截）、媒体（`screenshot`/`pdf`/`video-start`）、开发调试（`console`/`network`/`tracing-start`）及会话管理（`session-list`/`session-stop`）等全场景能力。  
- **会话隔离与持久化**：默认使用独立持久化用户配置文件（profile），支持多会话（`--session=name`）并行运行，各会话拥有独立 Cookie、Storage 和浏览历史，适用于多项目/多账号场景。  
- **零配置技能发现（Skills-less operation）**：代理可直接解析 `playwright-cli --help` 动态获取可用命令，无需预装技能定义文件；亦支持手动安装 SKILL.md 或通过插件市场（如 `/plugin install playwright-cli`）集成。  
- **灵活部署模式**：支持 headless（默认）与 headed（`--headed`）模式；可通过 CDP 端点、远程 Playwright Server 或浏览器扩展连接现有实例；支持配置文件（`playwright-cli.json`）与丰富环境变量（`PLAYWRIGHT_MCP_*`）精细化控制行为。  

3. **技术栈**  
- **运行时**：Node.js ≥ 18（必需）  
- **核心依赖**：基于 [Playwright](https://playwright.dev/)（官方浏览器自动化库），深度封装其 API 为 CLI 命令，复用 Chromium/Firefox/WebKit 多引擎能力。  
- **集成生态**：面向 AI 编程代理优化，原生适配 Claude Code、GitHub Copilot 等主流 coding agent 工具链；遵循 MCP 协议设计理念但采用更轻量的 CLI + SKILL 范式。  
- **配置与扩展**：JSON 配置文件（`playwright-cli.json`）+ 全面环境变量体系（`PLAYWRIGHT_MCP_*`）；支持 TypeScript/JavaScript 初始化脚本（`initPage`/`initScript`）、自定义测试 ID 属性（`testIdAttribute`）、超时/视口/代理/权限等高级参数。

</details>

---

### 32. [pedramamini/Maestro](https://github.com/pedramamini/Maestro)
- 📅 **创建日期**：2025-11-23  
- 🔄 **最近更新**：2026-02-06  
- ⭐ **Stars**：1,822（日 +167｜周 +1093｜月 +1412）  
- 📝 **描述**：Agent Orchestration Command Center  

<details>
<summary><b>📈 Star 与 Commit 历史趋势</b></summary>

![Maestro Star and Commit Trend](charts/pedramamini_Maestro_trend.png)

> *蓝色：累计 Stars｜橙色：累计 Commits（次 Y 轴）*

</details>

<details>
<summary><b>📄 README 摘要</b></summary>

1. **项目功能**  
Maestro 是一款跨平台桌面应用，专为高效协同多个 AI 编程代理（AI agents）而设计，核心目标是帮助开发者（尤其是“键盘优先”的黑客型用户）在并行多项目场景下实现注意力聚焦与工作流自动化。它不替代底层 AI 工具，而是作为“智能调度中枢”，以非交互式、会话隔离的方式调用用户已配置好的本地 AI 编程代理（如 Claude Code、OpenAI Codex 等），执行任务、管理上下文、协调多智能体协作，并支持长时间无人值守运行（实测超 24 小时）。本质是将分散的 AI 编程能力整合为可编排、可监控、可复用的工程化工作流平台。

2. **关键特性**  
- **多智能体并行调度**：支持无限数量 AI 代理同时运行，每个拥有独立工作区、会话历史与干净上下文；支持 Git Worktrees 实现分支级隔离并行开发，一键生成 PR。  
- **自动化任务引擎（Auto Run & Playbooks）**：基于文件系统的 Markdown 清单驱动批量任务处理，支持循环执行、进度追踪与完整历史回溯，每项任务独占 AI 会话。  
- **智能协作范式**：提供 Group Chat 功能，由“主持人 AI”协调多个专业 AI 代理参与架构讨论、跨项目问答并合成结论。  
- **全栈开发集成**：深度 Git 支持（自动检测/分支显示/差异查看/提交日志）、文件浏览器（语法高亮/Markdown 预览/图像查看）、`@` 文件引用、Git-aware 补全。  
- **极致键盘操作体验**：全功能快捷键体系（`Cmd+K` 快速操作、`Cmd+J` 切换 AI/Shell 终端等），含键盘熟练度追踪与成就系统。  
- **远程与命令行控制**：内置 Web 服务 + QR 码实现手机远程监控；提供 `maestro-cli` 支持 Headless 运行、CI/CD 集成及脚本化调用。  
- **高级分析与可视化**：Usage Dashboard（多维度用量统计、热力图、CSV 导出）；Document Graph（自动生成 Markdown 文档知识图谱，支持双向链接发现与交互式导航）。  
- **增强生产力工具**：消息队列（防丢指令）、输出过滤（正则/包含/排除）、Slash 命令扩展、自动草稿保存、语音通知、12 种主题、实时 Token/成本追踪。

3. **技术栈**  
- **前端框架**：基于 Electron 构建跨平台桌面应用（隐含使用 Chromium 渲染引擎 + Node.js 运行时）；UI 层采用现代 Web 技术（推测为 React/Vue 类框架，文档中强调高度交互性与响应速度）。  
- **核心通信机制**：采用 MCP（Model Context Protocol）标准协议与本地 AI 代理（Claude Code、Codex、OpenCode、Factory Droid）对接，实现零侵入式集成——复用用户原有认证、权限与工具链配置。  
- **后端/服务层**：内置轻量 Web 服务器（支持本地网络与 Cloudflare Tunnel 远程访问）；CLI 工具（`maestro-cli`）提供命令行接口；消息队列与会话管理依赖本地持久化存储（推测为 SQLite 或文件系统）。  
- **构建与依赖**：使用 npm 进行包管理（`npm install`, `npm run dev`），源码公开，支持从源码构建；依赖 Git 作为可选但关键的基础设施（支撑 Worktrees、Diff、Commit 等功能）。

</details>

---

### 33. [modelcontextprotocol/ext-apps](https://github.com/modelcontextprotocol/ext-apps)
- 📅 **创建日期**：2025-11-21  
- 🔄 **最近更新**：2026-02-06  
- ⭐ **Stars**：1,377（日 +41｜周 +538｜月 +1047）  
- 📝 **描述**：Official repo for spec & SDK of MCP Apps protocol - standard for UIs embedded AI chatbots, served by MCP servers  

<details>
<summary><b>📈 Star 与 Commit 历史趋势</b></summary>

![ext-apps Star and Commit Trend](charts/modelcontextprotocol_ext-apps_trend.png)

> *蓝色：累计 Stars｜橙色：累计 Commits（次 Y 轴）*

</details>

<details>
<summary><b>📄 README 摘要</b></summary>

1. **项目功能**  
该项目实现了 **MCP（Model Context Protocol）Apps 扩展标准（SEP-1865）**，旨在为基于 MCP 的 AI 系统（如 LLM 驱动的聊天客户端/智能代理）提供标准化的**内联交互式 UI 能力**。它使 MCP 服务器能够向兼容的 MCP 客户端（如支持 MCP 的 IDE、桌面应用或聊天界面）动态提供可嵌入对话上下文中的富交互界面（例如图表、3D 场景、表单、视频播放器、实时监控面板等），突破传统 MCP 工具仅返回文本/结构化数据的限制，实现“工具调用即界面呈现”的无缝体验。

2. **核心特性**  
- ✅ **标准化 UI 声明机制**：通过 `ui://` 协议资源在工具定义中声明 HTML 界面地址，实现服务端驱动的 UI 注册；  
- ✅ **沙箱化安全渲染**：客户端在隔离的 iframe 中加载并渲染远程 UI，保障执行安全；  
- ✅ **双向上下文通信**：支持主机（Host）向 UI 传递工具输入数据（via notifications），UI 也可通过 Host 调用其他 MCP 工具（tool calling），形成闭环交互；  
- ✅ **跨框架 SDK 支持**：为应用开发者提供 React Hooks、Vanilla JS、Vue、Svelte、Preact、Solid 等多前端框架的开箱即用模板与 SDK；  
- ✅ **完整双角色支持**：分别提供 **App SDK**（供 UI 开发者构建交互组件）和 **App Bridge SDK**（供客户端/Host 开发者集成渲染与通信逻辑）；  
- ✅ **丰富开箱即用示例**：包含 20+ 生产级场景示例（如 CesiumJS 地球可视化、Three.js 3D 渲染、ShaderToy 实时着色器、PDF 查看器、客户分群散点图、预算分配器、维基知识图谱探索等），覆盖数据可视化、多媒体、系统监控、文档处理等多领域；  
- ✅ **Agent 技能集成**：提供 Agent Skills 插件（支持 Claude Code 等 AI 编程代理），简化 MCP Apps 的开发与部署流程。

3. **技术栈**  
- **协议层**：基于 [Model Context Protocol (MCP)](https://github.com/modelcontextprotocol/modelcontextprotocol) 标准扩展，采用 `ui://` 自定义 URI 方案；  
- **前端（App 侧）**：支持主流 JavaScript 框架 —— **React**（含专用 Hooks）、**Vue**、**Svelte**、**Preact**、**Solid**、**Vanilla JS**；依赖现代 Web API（如 `postMessage` 沙箱通信）、HTML/CSS/JS；部分示例集成 **CesiumJS**、**Three.js**、**ABCjs**（乐谱）、**GLSL**（着色器）等专业库；  
- **后端/服务端（Server）**：Node.js（TypeScript）为主，提供多种预构建 MCP 服务器包（如 `@modelcontextprotocol/server-basic-react`）；Python 示例（如 `qr-server`、`say-server`）使用 `uv` 运行时，体现多语言兼容性；  
- **通信机制**：基于 MCP stdio transport（标准输入输出）或自定义 HTTP 接口，通过 `postMessage` 实现 Host ↔ App iframe 的跨域安全通信；  
- **构建与生态**：npm 包管理（`@modelcontextprotocol/ext-apps` 及子包），TypeScript 类型定义完善，配套完整 API 文档与 Markdown 规范文档（apps.mdx），支持本地开发热更新与 MCP 客户端（如 Claude Desktop、VS Code MCP 扩展）深度集成。

</details>

---

### 34. [ZeroTworu/anet](https://github.com/ZeroTworu/anet)
- 📅 **创建日期**：2025-09-07  
- 🔄 **最近更新**：2026-02-06  
- ⭐ **Stars**：359（日 +128｜周 +357｜月 +358）  
- 📝 **描述**：Simple Rust VPN Client / Server  

<details>
<summary><b>📈 Star 与 Commit 历史趋势</b></summary>

![anet Star and Commit Trend](charts/ZeroTworu_anet_trend.png)

> *蓝色：累计 Stars｜橙色：累计 Commits（次 Y 轴）*

</details>

<details>
<summary><b>📄 README 摘要</b></summary>

1. **项目功能**  
ANet（“朋友网络”）是一个用于在互相信任的亲密个体之间构建私有、安全信息空间的去中心化通信技术。它不提供托管服务，而是提供一套可本地部署的端到端通信工具链，旨在绕过网络审查与封锁，在高丢包、连接不稳定甚至受监控的网络环境中（如受限地区）实现隐蔽、可靠的信息交换。

2. **核心特性**  
- 自研安全传输协议 **ASTP v1.0**：专为抗审查与强隐私设计；  
- **端到端加密**：采用 ChaCha20-Poly1305 对称加密 + X25519 密钥交换，保障通信内容不可窃听、不可篡改；  
- **抗网络干扰能力**：协议层优化适配高丢包率与抖动网络，维持会话稳定性；  
- **流量伪装（Mimicry）**：UDP 数据流呈现高熵随机噪声特征，难以被 DPI（深度包检测）识别或阻断；  
- **全平台支持**：提供 Linux/Windows 命令行与图形界面客户端、Android 移动端（含 JNI 绑定），满足多样化终端需求；  
- **离线密钥管理**：配套 `anet-keygen` 工具支持本地密钥对生成，无中心化身份认证依赖。

3. **技术栈**  
- **主语言**：Rust（v1.84+），强调内存安全、零成本抽象与并发性能；  
- **核心协议栈**：自定义 ASTP 协议实现在 `anet-common` 模块中，集成成熟密码学原语（via `ring` 或 `libsodium` 等 Rust 生态 crate）；  
- **架构分层**：模块化设计，包含协调节点（`anet-server`）、CLI 客户端（`anet-client-cli`）、GUI 客户端（`anet-client-gui`）、Android 库（`anet-mobile`）及通用协议/密码库（`anet-common`）；  
- **构建系统**：基于 Cargo 标准工作流，支持一键全组件编译（`cargo build --release`）。

</details>

---

