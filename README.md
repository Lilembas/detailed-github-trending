# 🌟 GitHub Trending 概览

> 数据更新于：2026-02-13

---

## 🔍 项目详情

### 1. [anomalyco/opencode](https://github.com/anomalyco/opencode)
- 📅 **创建日期**：2025-04-30  
- 🔄 **最近更新**：2026-02-13  
- ⭐ **Stars**：181,754（日 +723｜周 +5048｜月 +44500）  
- 📝 **描述**：The open source coding agent.  

<details>
<summary><b>📈 Star 与 Commit 历史趋势</b></summary>

![opencode Star and Commit Trend](charts/anomalyco_opencode_trend.png)

> *蓝色：累计 Stars｜橙色：累计 Commits（次 Y 轴）*

</details>

<details>
<summary><b>📄 README 摘要</b></summary>

1. **该项目做什么？**  
OpenCode 是一个开源的 AI 编程智能体（AI coding agent），旨在为开发者提供终端原生（TUI）、轻量高效且高度可扩展的 AI 辅助编程体验。它直接在本地终端中运行，支持代码理解、编辑、调试、重构、文档生成与多步任务规划等全流程开发辅助功能；同时采用客户端/服务器架构，允许远程控制（如通过移动 App 驱动本地运行的 OpenCode 实例），并原生集成语言服务器协议（LSP），实现深度 IDE 级语义支持。

2. **核心功能**  
- **双模式智能体切换**：内置 `build`（默认，全权限开发代理）和 `plan`（只读分析代理，禁止自动修改文件、执行命令前需显式授权），按 Tab 键即时切换；另含 `@general` 子代理处理复杂搜索与多步骤推理任务。  
- **跨平台终端优先设计**：深度优化 TUI 交互体验，面向 Neovim 用户及终端极客打造，强调“在终端中完成一切”。  
- **完全开源与厂商中立**：不绑定任何大模型供应商，原生兼容 Claude、OpenAI、Google Gemini、Ollama 本地模型等，支持自定义模型后端与 OpenCode Zen（官方推荐模型服务）。  
- **多形态部署支持**：提供命令行 CLI（支持 npm/brew/scoop/choco/paru/mise/nix 等多种安装方式）、桌面应用（macOS/Windows/Linux BETA 版）、以及可嵌入的 SDK（`opencode-ai` npm 包）。  
- **国际化与可定制安装路径**：支持 18 种语言文档；安装脚本遵循 XDG 规范，支持通过环境变量（`OPENCODE_INSTALL_DIR`/`XDG_BIN_DIR`）灵活指定安装目录。

3. **技术栈**  
- **核心语言与运行时**：TypeScript（主逻辑）、Rust（高性能组件，如底层通信或模型适配层，虽未明示但由项目结构与社区实践可推断）、Shell（安装脚本）  
- **架构模式**：Client/Server 架构，TUI 为默认客户端，支持未来 Web、移动端等多端接入  
- **协议与标准**：原生支持 LSP（Language Server Protocol），实现智能补全、跳转、诊断等 IDE 功能  
- **构建与分发**：GitHub Actions 自动化发布；多包管理器支持（npm、Homebrew、Scoop、Chocolatey、AUR/Paru、Mise、Nix）；桌面版基于现代跨平台框架（如 Tauri 或 Electron，结合其二进制分发形态推断）  
- **基础设施**：托管于 GitHub；文档站点 `opencode.ai` 基于静态生成；社区协作依托 Discord 和 GitHub 生态

</details>

---

### 2. [anthropics/skills](https://github.com/anthropics/skills)
- 📅 **创建日期**：2025-09-22  
- 🔄 **最近更新**：2026-02-13  
- ⭐ **Stars**：109,397（日 +587｜周 +4762｜月 +28823）  
- 📝 **描述**：Public repository for Agent Skills  

<details>
<summary><b>📈 Star 与 Commit 历史趋势</b></summary>

![skills Star and Commit Trend](charts/anthropics_skills_trend.png)

> *蓝色：累计 Stars｜橙色：累计 Commits（次 Y 轴）*

</details>

<details>
<summary><b>📄 README 摘要</b></summary>

1. **该项目做什么？**  
该项目是 Anthropic 官方维护的 Claude 技能（Skills）开源示例仓库，提供一系列可动态加载、即插即用的模块化能力单元。每个“技能”是一个独立文件夹，内含 `SKILL.md`（含 YAML 元数据与任务指令），用于指导 Claude 在特定场景下执行标准化、可复现的专业任务，例如：按企业品牌规范生成文档、按组织流程分析数据、自动化个人事务、解析/生成 PDF/DOCX/PPTX/XLSX 文件、测试 Web 应用、构建 MCP 服务器等。它不提供运行时引擎，而是为开发者和企业展示如何通过结构化提示工程与资源封装，扩展 Claude 的垂直领域能力。

2. **关键特性**  
- **模块化与自包含设计**：每个技能独立成 folder，含清晰元数据（`name`/`description`）与行为指令（Markdown 内容含示例、指南），支持即插即用；  
- **多场景覆盖**：涵盖创意设计（艺术/音乐/设计）、技术开发（Web 测试/MCP 服务生成）、企业协作（通讯/品牌管理）及全格式文档处理（DOCX/PDF/PPTX/XLSX）四大类技能；  
- **生产级参考实现**：`skills/docx` 等子目录公开了支撑 Claude 官方文档功能的真实源码（source-available，非开源），为复杂技能开发提供工业级范本；  
- **跨平台部署支持**：兼容 Claude Code（插件市场注册）、Claude.ai（付费用户开箱即用）、Claude API（支持上传自定义技能）三大使用路径；  
- **标准化规范与模板**：内置 `./spec`（Agent Skills 标准规范）与 `./template`（技能创建模板），降低开发门槛，确保互操作性。

3. **技术栈**  
- **核心格式**：YAML（元数据声明） + Markdown（指令、示例、指南的自然语言描述）——无代码依赖，纯文本驱动；  
- **协议标准**：遵循 [Agent Skills](https://agentskills.io) 开放规范，定义技能发现、加载、执行与元数据交互的统一接口；  
- **运行环境**：深度集成 Anthropic 生态，依赖 Claude 模型原生技能加载机制（非独立服务），通过 `claude-code` 插件系统、`claude.ai` 前端或 `Anthropic API` 调用；  
- **许可证**：多数示例技能采用 Apache 2.0 开源协议，文档类技能为 source-available（可查看/学习，但不可修改分发）。

</details>

---

### 3. [Shubhamsaboo/awesome-llm-apps](https://github.com/Shubhamsaboo/awesome-llm-apps)
- 📅 **创建日期**：2024-04-29  
- 🔄 **最近更新**：2026-02-13  
- ⭐ **Stars**：94,876（日 +483｜周 +2359｜月 +7088）  
- 📝 **描述**：Collection of awesome LLM apps with AI Agents and RAG using OpenAI, Anthropic, Gemini and opensource models.  

<details>
<summary><b>📈 Star 与 Commit 历史趋势</b></summary>

![awesome-llm-apps Star and Commit Trend](charts/Shubhamsaboo_awesome-llm-apps_trend.png)

> *蓝色：累计 Stars｜橙色：累计 Commits（次 Y 轴）*

</details>

<details>
<summary><b>📄 README 摘要</b></summary>

1. **该项目做什么？**  
该项目是一个高度结构化的、持续更新的开源精选集（curated collection），专注于**实际可运行的大型语言模型（LLM）应用项目**，而非理论或纯工具库。它系统性地归类并提供大量开箱即用（或易于本地部署）的LLM应用案例，覆盖从入门级单智能体到复杂多智能体协作、语音交互、RAG增强、MCP协议集成、记忆机制、跨平台数据源对话（如GitHub/Gmail/PDF/YouTube等）以及模型优化与微调等多个前沿实践方向。其核心目标是为开发者、研究人员和AI从业者提供一个“即学即用”的高质量LLM应用参考库与学习路径。

2. **关键特性**  
- **全栈式智能体覆盖**：包含数百个按难度与类型精细分类的AI智能体，涵盖 Starter（如AI旅行代理、AI医疗影像分析）、Advanced（如AI VC尽调团队、AI自我演化代理）、Multi-agent Teams（如AI法律/招聘/房地产代理团队）、Voice Agents（语音客服、音频导览）、MCP Agents（浏览器/GitHub/Notion等MCP协议集成代理）；  
- **深度RAG实战体系**：提供超20种RAG变体实现（如Corrective RAG、Hybrid Search RAG、Vision RAG、Local Llama3.1 RAG、RAG-as-a-Service），支持本地化部署与云服务混合架构；  
- **跨平台数据连接能力**：通过“Chat with X”系列教程，实现LLM与真实世界数据源的无缝对话（Gmail、GitHub、PDF、ArXiv论文、Substack、YouTube视频等）；  
- **工程化增强能力**：内置LLM成本优化工具（Toonify Token Optimization降本30–60%，Headroom Context Optimization降本50–90%）、持久化记忆（Stateful Chat、Shared Memory）、多模型协同（OpenAI/Claude/Gemini/Qwen/Llama混合调度）；  
- **框架实战教学**：提供Google ADK与OpenAI Agents SDK两大主流智能体框架的完整速成课程，涵盖工具集成、结构化输出、多智能体编排、Swarm路由、MCP插件及评估机制；  
- **国际化与社区驱动**：支持8种语言界面，由活跃社区维护，并获得TinyFish、Tiger Data、Speechmatics等机构赞助支持。

3. **技术栈**  
- **大模型层**：兼容闭源API（OpenAI GPT系列、Anthropic Claude、Google Gemini、xAI Grok）与主流开源模型（Llama 3.1/3.2、Qwen、Gemma 3、DeepSeek、Mixtral）；  
- **智能体框架**：Google ADK（Agent Development Kit）、OpenAI Agents SDK、CrewAI、LangChain、LlamaIndex；  
- **协议与标准**：Model Context Protocol（MCP）深度集成，支持标准化工具调用与上下文管理；  
- **RAG基础设施**：向量数据库（Chroma、FAISS、Qdrant等隐含依赖）、嵌入模型（Gemma Embedding、Cohere等）、混合检索、重排序、文档切分与多模态解析（PDF/视频/图像）；  
- **语音与多模态**：Speechmatics语音识别、Whisper、Gemini Multimodal、Vision RAG；  
- **开发与部署**：Python为主，依赖标准生态（Pydantic、FastAPI隐含）、本地运行优先（支持CPU/GPU推理）、要求明确的`requirements.txt`管理；  
- **辅助工具链**：Git版本控制、GitHub Actions（隐含CI/CD）、Star History指标看板、i18n多语言README自动化支持。

</details>

---

### 4. [obra/superpowers](https://github.com/obra/superpowers)
- 📅 **创建日期**：2025-10-09  
- 🔄 **最近更新**：2026-02-13  
- ⭐ **Stars**：79,814（日 +592｜周 +5033｜月 +36771）  
- 📝 **描述**：An agentic skills framework & software development methodology that works.  

<details>
<summary><b>📈 Star 与 Commit 历史趋势</b></summary>

![superpowers Star and Commit Trend](charts/obra_superpowers_trend.png)

> *蓝色：累计 Stars｜橙色：累计 Commits（次 Y 轴）*

</details>

<details>
<summary><b>📄 README 摘要</b></summary>

1. **该项目的作用**  
Superpowers 是一个面向编程智能体（coding agents）的完整软件开发工作流框架，旨在将原本零散、随意的代码生成行为，系统化为可验证、可协作、符合工程最佳实践的开发过程。它不直接生成代码，而是通过一系列自动触发的“技能”（skills），引导智能体完成从需求澄清、设计评审、计划制定、TDD 实施、子智能体协同开发、代码审查到分支收尾的全流程。其核心目标是让 AI 编程行为具备人类高级工程师的工程纪律性——强调实证（而非断言）、简化（而非过度设计）、自动化验证（而非主观判断）和人机协同控制（而非完全黑箱执行）。

2. **关键特性**  
- **全自动技能触发机制**：无需手动调用，智能体在每个开发阶段前自动识别并启用对应技能（如设计阶段触发 `brainstorming`，编码前强制 `test-driven-development`）。  
- **严格遵循工程原则**：强制实施红-绿-重构（RED-GREEN-REFACTOR）的 TDD 流程；贯彻 YAGNI（你不会需要它）与 DRY（不要重复自己）；杜绝无测试先行的代码编写（自动删除未经测试的代码）。  
- **结构化人机协作流程**：包括分块式设计确认、细粒度任务拆解（每项任务≤5分钟、含精确文件路径与验证步骤）、双阶段子智能体审查（先验规范符合性，再审代码质量）、基于严重等级的阻断式代码审查（critical 问题立即中止流程）。  
- **多环境兼容架构**：原生支持 Claude Code 插件市场，同时提供 Codex 和 OpenCode 的标准化接入方案（通过远程加载安装指令）。  
- **可扩展技能库**：内置 15+ 经过验证的模块化技能，覆盖测试、调试、协作、元能力（如 `writing-skills` 支持用户自主创建新技能），所有技能均自带最佳实践指南与测试方法论。  
- **Git 工作流深度集成**：自动使用 `git worktree` 创建隔离开发分支，确保环境干净、测试基线可靠，并在完成时提供合并/PR/丢弃等决策选项。

3. **技术栈**  
- **运行平台**：专为 LLM 编程智能体设计，非独立应用；当前主要适配 **Claude Code**（通过官方插件系统）、**Codex** 和 **OpenCode** 三类 AI 编程环境。  
- **核心范式**：基于“技能（Skill）”的声明式工作流引擎——每个技能是自包含的 Markdown 文档（如 `skills/test-driven-development/SKILL.md`），定义行为逻辑、触发条件、输入输出及验证规则；无传统后端服务或运行时框架。  
- **基础设施依赖**：零服务器依赖，纯客户端侧执行；技能资源托管于 GitHub 仓库（`obra/superpowers`），通过 HTTPS 直接拉取（如 Codex/OpenCode 的 `fetch and follow instructions` 机制）；更新通过插件命令（`/plugin update`）实现。  
- **协议与标准**：遵循 Git 分支管理规范（worktree）、TDD 标准流程、Socratic 提问法设计思维；所有技能文档采用统一结构化格式，支持机器解析与人工审计。

</details>

---

### 5. [openclaw/openclaw](https://github.com/openclaw/openclaw)
- 📅 **创建日期**：2025-11-24  
- 🔄 **最近更新**：2026-02-13  
- ⭐ **Stars**：76,116（日 +3159｜周 +21290｜月 +76116）  
- 📝 **描述**：Your own personal AI assistant. Any OS. Any Platform. The lobster way. 🦞   

<details>
<summary><b>📈 Star 与 Commit 历史趋势</b></summary>

![openclaw Star and Commit Trend](charts/openclaw_openclaw_trend.png)

> *蓝色：累计 Stars｜橙色：累计 Commits（次 Y 轴）*

</details>

<details>
<summary><b>📄 README 摘要</b></summary>

1. **项目功能**  
OpenClaw 是一个完全本地化、用户自托管的个人 AI 助手系统，核心目标是让用户在自有设备（macOS/iOS/Android/Linux/Windows）上运行一个响应迅速、始终在线、隐私优先的单用户 AI 助理。它不依赖中心化云服务，而是通过轻量级「网关（Gateway）」作为统一控制平面，将来自 14+ 主流通信渠道（WhatsApp、Telegram、Slack、Discord、Google Chat、Signal、iMessage、BlueBubbles、Microsoft Teams、Matrix、Zalo、Zalo Personal、WebChat 等）的消息实时接入，并交由本地运行的 AI 代理（Pi agent）处理；同时支持语音唤醒（Voice Wake）、实时对话（Talk Mode）、跨平台可视化工作区（Live Canvas/A2UI），以及设备级操作（如调用摄像头、屏幕录制、系统命令、通知等），真正实现“AI 在本地、动作在终端、控制在手中”。

2. **关键特性**  
- **多通道统一收件箱**：原生集成 WhatsApp（Baileys）、Telegram（grammY）、Slack（Bolt）、Discord（discord.js）等主流平台，含扩展支持（如 BlueBubbles 实现 iMessage 桥接、Zalo 个人版、Matrix 等）。  
- **本地优先架构**：网关（Gateway）为单一 WebSocket 控制平面，管理会话、通道、工具、事件、定时任务（cron）、Webhook 及远程调试界面（Control UI/WebChat）。  
- **多智能体路由与隔离**：支持按通道、账号、群组或用户粒度分发至独立工作区（workspace）和隔离会话（session），具备群组激活规则（mention/always）、上下文隔离、队列模式与回复回传机制。  
- **全栈语音交互**：基于 ElevenLabs 实现 macOS/iOS/Android 端常驻语音唤醒（Voice Wake）与连续对话模式（Talk Mode），支持 PTT 与语音转文字流水线。  
- **动态可视化工作区（Live Canvas）**：AI 代理可主动推送、重置或执行 A2UI 组件（按钮、表单、图表等），构建可编程的图形化交互界面，跨 macOS/iOS/Android 同步渲染。  
- **深度设备集成节点（Nodes）**：提供 `system.run`（执行命令）、`system.notify`（通知）、`camera.*`、`screen.record`、`location.get`、`canvas.*` 等原生能力，通过 `node.invoke` 安全调用，严格遵循 macOS TCC / iOS/Android 权限模型。  
- **安全默认策略**：DM 默认启用配对认证（pairing policy），未知发送者需输入一次性验证码方可加入白名单；支持显式开放（`dmPolicy="open"`）并配置细粒度 `allowFrom` 规则；内置 `openclaw doctor` 自动检测高危配置。  
- **自动化与扩展生态**：内置浏览器控制（专属 Chromium + CDP）、Cron 任务、Gmail Pub/Sub 集成、Webhook 触发器；支持技能平台（ClawHub 技能注册中心），提供捆绑技能（bundled）、托管技能（managed）与工作区技能（workspace）三级管理。  
- **灵活部署与远程访问**：支持 Tailscale Serve（内网穿透）/Funnel（公网暴露）、SSH 隧道、Nix 声明式配置、Docker 容器化部署；允许 Gateway 运行于远程 Linux 服务器，而设备节点（iOS/macOS/Android）仅负责本地敏感操作，实现安全解耦。

3. **技术栈**  
- **运行时**：Node.js ≥22（主运行环境），支持 npm/pnpm/bun；TypeScript 为主开发语言，使用 `tsx` 直接运行源码，`pnpm build` 生成 `dist/` 供生产部署。  
- **核心框架**：WebSocket 协议驱动的网关控制平面；RPC 模式 Pi agent 运行时；A2UI（Canvas 渲染协议）；CDP（Chrome DevTools Protocol）用于浏览器自动化。  
- **前端与 UI**：WebChat 内嵌于网关 HTTP 服务；macOS 菜单栏应用（Swift/Objective-C + WebView）；iOS/Android 原生节点（Swift/Kotlin）；Canvas 使用 Web 技术栈（HTML/CSS/JS）渲染。  
- **语音与媒体**：ElevenLabs 语音合成；FFmpeg（音视频处理）；Whisper（可选语音识别）；媒体管道支持图像/音频/视频上传、转录钩子、尺寸限制与临时文件生命周期管理。  
- **安全与权限**：OAuth（Anthropic/OpenAI 订阅）与 API Key 双模模型认证；模型故障转移（failover）与会话剪枝（session pruning）；Tailscale Identity Header 认证；密码/Token/SSH 多层远程访问鉴权。  
- **基础设施**：Tailscale（网络层穿透与身份）、Docker（容器化）、Nix（声明式配置与可复现构建）、launchd（macOS）/systemd（Linux）守护进程管理。

</details>

---

### 6. [google/langextract](https://github.com/google/langextract)
- 📅 **创建日期**：2025-07-08  
- 🔄 **最近更新**：2026-02-13  
- ⭐ **Stars**：54,056（日 +841｜周 +7839｜月 +12965）  
- 📝 **描述**：A Python library for extracting structured information from unstructured text using LLMs with precise source grounding and interactive visualization.  

<details>
<summary><b>📈 Star 与 Commit 历史趋势</b></summary>

![langextract Star and Commit Trend](charts/google_langextract_trend.png)

> *蓝色：累计 Stars｜橙色：累计 Commits（次 Y 轴）*

</details>

<details>
<summary><b>📄 README 摘要</b></summary>

1. **项目功能**  
LangExtract 是一个基于大语言模型（LLM）的 Python 库，专注于从**非结构化文本**（如临床病历、放射报告、文学作品等）中**高精度提取结构化信息**。其核心能力是依据用户提供的自然语言指令和少量示例（few-shot examples），自动识别并组织关键实体（如人物、情感、药物名称、剂量、关系等），同时严格保证所有提取结果均**可追溯至原文中的精确位置**（source grounding），支持端到端的验证与审计。

2. **关键特性**  
- ✅ **精准溯源定位**：为每个提取项标注原文起止字符偏移量，支持可视化高亮，确保结果完全可验证；  
- ✅ **强结构化输出保障**：通过受控生成机制（如 Gemini 的 schema 强约束）和示例驱动，强制输出严格符合预定义类目与属性格式的 JSON 结构；  
- ✅ **长文档优化处理**：采用智能分块（chunking）、多轮提取（extraction_passes）、并行处理（max_workers）及上下文缓冲（max_char_buffer）策略，高效应对数十万字符级文档（如整本《罗密欧与朱丽叶》）；  
- ✅ **交互式可视化审查**：一键生成自包含 HTML 文件，支持动态搜索、上下文展开、实体聚类与动画高亮，便于人工复核海量结果；  
- ✅ **多源模型灵活适配**：原生支持 Google Gemini（云）、OpenAI（需额外安装）、本地 Ollama 模型（如 gemma2:2b），并提供插件化接口扩展第三方模型；  
- ✅ **零微调领域泛化**：仅需 1–3 个高质量示例即可快速适配新领域（医疗、法律、文学等），无需训练或微调模型；  
- ✅ **生产就绪增强功能**：支持 Vertex AI 批处理降本、Docker 容器化部署、环境变量/.env 安全密钥管理、以及社区驱动的 Provider 插件生态。

3. **技术栈**  
- **编程语言**：Python 3.10+（核心实现）；  
- **核心依赖**：`google-generativeai`（Gemini）、`openai`（可选）、`ollama`（本地 LLM）、`pydantic`（数据校验）、`rich`（CLI 输出）、`jinja2`（HTML 模板）；  
- **构建与打包**：`pyproject.toml` + `setuptools`，支持 PEP 517/518 标准；  
- **开发工具链**：`pytest`（测试）、`tox`（多环境 CI 模拟）、`pylint`/`pyink`/`isort`（代码规范）、`pre-commit`（钩子自动化）；  
- **部署与集成**：Docker 支持、Vertex AI 服务账号认证、Hugging Face Spaces 在线 Demo（RadExtract）；  
- **协议与许可**：Apache 2.0 开源许可证，健康领域应用额外遵循 Google Health AI 开发者条款。

</details>

---

### 7. [remotion-dev/remotion](https://github.com/remotion-dev/remotion)
- 📅 **创建日期**：2020-06-23  
- 🔄 **最近更新**：2026-02-13  
- ⭐ **Stars**：36,465（日 +121｜周 +1158｜月 +11234）  
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
- ✅ **开发友好工具链**：内置本地预览服务器、帧调试器、性能分析面板、CLI 工具（`npx create-video@latest` 快速初始化）及 TypeScript 全面支持。  
- ✅ **扩展生态**：兼容 FFMPEG 高级处理、音频合成、字体加载、远程资源动态注入，并拥有活跃社区与官方 Showcase 案例库。

3. **技术栈**  
- **核心框架**：React（v18+，支持 Concurrent Features）、TypeScript（默认强类型支持）  
- **渲染引擎**：基于 Chromium（Puppeteer / Playwright）的 Headless 浏览器渲染，利用 Canvas/WebGL 加速图形合成  
- **构建与打包**：Vite（默认模板）、Webpack（兼容模式）；ESM + 动态导入支持  
- **视频处理层**：FFmpeg（用于编码/转封装）、WebCodecs（实验性浏览器原生编码）  
- **基础设施**：Node.js 运行时、npm/pnpm 包管理；CI/CD 友好（GitHub Actions 集成示例）  
- **配套工具**：自研 CLI（`remotion` CLI）、VS Code 插件（语法高亮/调试支持）、Discord 社区实时支持

</details>

---

### 8. [asgeirtj/system_prompts_leaks](https://github.com/asgeirtj/system_prompts_leaks)
- 📅 **创建日期**：2025-05-03  
- 🔄 **最近更新**：2026-02-13  
- ⭐ **Stars**：31,366（日 +137｜周 +992｜月 +6359）  
- 📝 **描述**：Collection of extracted System Prompts from popular chatbots like ChatGPT, Claude & Gemini  

<details>
<summary><b>📈 Star 与 Commit 历史趋势</b></summary>

![system_prompts_leaks Star and Commit Trend](charts/asgeirtj_system_prompts_leaks_trend.png)

> *蓝色：累计 Stars｜橙色：累计 Commits（次 Y 轴）*

</details>

---

### 9. [patchy631/ai-engineering-hub](https://github.com/patchy631/ai-engineering-hub)
- 📅 **创建日期**：2024-10-21  
- 🔄 **最近更新**：2026-02-13  
- ⭐ **Stars**：29,108（日 +104｜周 +1096｜月 +3126）  
- 📝 **描述**：In-depth tutorials on LLMs, RAGs and real-world AI agent applications.  

<details>
<summary><b>📈 Star 与 Commit 历史趋势</b></summary>

![ai-engineering-hub Star and Commit Trend](charts/patchy631_ai-engineering-hub_trend.png)

> *蓝色：累计 Stars｜橙色：累计 Commits（次 Y 轴）*

</details>

<details>
<summary><b>📄 README 摘要</b></summary>

1. **该项目做什么？**  
AI Engineering Hub 是一个面向 AI 工程实践的开源资源库，旨在为初学者、从业者和研究人员提供可直接上手的**生产级 AI 项目模板与实战教程**。它不侧重理论教学，而是聚焦于构建真实可用的 AI 系统，涵盖从单模块工具（如 OCR、本地聊天界面）到多智能体协作系统（如自动研报生成、品牌监控）、再到企业级部署方案（如私有化 Agentic RAG API、细调流水线、多模态文档处理）的全栈能力。所有项目均强调“开箱即用”，支持本地运行、轻量化部署，并鼓励用户复用、改编与规模化集成至自身工程体系中。

2. **核心功能**  
- **分层项目体系**：按难度分级（93+ 项目），含 22 个入门级（单组件、Streamlit/CLI 快速验证）、48 个中级（多智能体工作流、语音/视频 RAG、MCP 集成、模型对比评测）和 23 个高级项目（模型微调、推理架构实现、生产级文档管道、合规型对话代理等）；  
- **技术场景全覆盖**：深度覆盖 LLM 应用核心范式——基础 RAG、Agentic RAG（含 Web 回退、多源检索）、多模态 RAG（图像/视频/音频）、智能体编排（CrewAI/AutoGen/Motia）、MCP（Model Context Protocol）协议落地、语音交互（AssemblyAI/Cartesia）、结构化数据处理（Excel RAG、SQL 路由）、合成数据与评估观测（Opik/CometML）；  
- **工程就绪导向**：所有项目均提供可运行代码、明确依赖说明与部署指引（如 LitServe API、Docker 化、Ollama 本地模型集成），并包含大量前沿技术组合（如 Llama 4 + Qdrant、DeepSeek-Janus-Pro 多模态、FireCrawl 网页抓取 + MCP、Zep/Graphiti 持久化记忆）。

3. **技术栈**  
- **模型层**：主流开源模型全覆盖，包括 Llama 系列（Llama 3.2/3.3/4）、DeepSeek（R1、Janus-Pro）、Gemma-3、Qwen 系列（2.5 VL / 3 / 3-Coder）、GPT-OSS、ModernBERT、Sonnet 4、Claude Code、O3/O4 等；  
- **框架与工具链**：  
  - 智能体框架：CrewAI、AutoGen、Motia、Stagehand；  
  - RAG 栈：LlamaIndex、Qdrant、Milvus、SambaNova、Dockling（IBM）、Ragie；  
  - MCP 生态：Cursor Linkup、EyeLevel、LlamaIndex MCP 客户端、MindsDB MCP、Pixeltable MCP；  
  - UI/交互：Streamlit、Chainlit、React（前端）、Supabase（后端存储）；  
  - 语音/音视频：AssemblyAI、Cartesia、Gemini；  
  - 部署与运维：LitServe、Ollama、Unsloth（高效微调）、Docker；  
- **基础设施与服务**：BrightData（爬虫）、FireCrawl（网页转 API）、GroundX（文档处理）、Zep（记忆管理）、Opik（可观测性）、TensorLake（上下文工程）。

</details>

---

### 10. [thedotmack/claude-mem](https://github.com/thedotmack/claude-mem)
- 📅 **创建日期**：2025-08-31  
- 🔄 **最近更新**：2026-02-13  
- ⭐ **Stars**：28,009（日 +284｜周 +3723｜月 +14332）  
- 📝 **描述**：A Claude Code plugin that automatically captures everything Claude does during your coding sessions, compresses it with AI (using Claude's agent-sdk), and injects relevant context back into future sessions.  

<details>
<summary><b>📈 Star 与 Commit 历史趋势</b></summary>

![claude-mem Star and Commit Trend](charts/thedotmack_claude-mem_trend.png)

> *蓝色：累计 Stars｜橙色：累计 Commits（次 Y 轴）*

</details>

<details>
<summary><b>📄 README 摘要</b></summary>

1. **项目功能**  
Claude-Mem 是一个专为 Anthropic Claude Code（AI 编程助手）设计的**持久化记忆压缩系统**。它在用户每次会话中自动捕获工具调用、代码操作、错误信息等“观察数据”（observations），生成语义化摘要，并持久化存储于本地 SQLite 数据库中；在后续会话启动时，自动检索并按需注入相关上下文，从而实现跨会话的知识连续性——使 Claude 能“记住”项目历史、技术决策、调试过程和已修复问题，显著提升长周期开发任务中的上下文连贯性与推理准确性。

2. **核心特性**  
- ✅ **持久化记忆**：上下文不随会话关闭而丢失，支持长期项目知识沉淀；  
- ✅ **渐进式披露（Progressive Disclosure）**：分三层检索（`search` → `timeline` → `get_observations`），按需加载内容，节省 10 倍以上 token 消耗；  
- ✅ **技能化搜索（mem-search）**：通过自然语言查询历史（如 “authentication bug”），支持按类型、日期、项目名等多维过滤；  
- ✅ **实时 Web 查看器**：内置 HTTP 服务（`http://localhost:37777`），提供内存流可视化、观测详情查看、API 接口及设置面板；  
- ✅ **Claude Desktop 深度集成**：可在桌面版对话中直接调用 `mem-search` 技能检索记忆；  
- ✅ **隐私敏感控制**：支持 `<private>` 标签语法，自动排除敏感内容（如密钥、凭证）进入存储；  
- ✅ **全自动运行**：无需手动触发，依赖 6 个生命周期钩子（SessionStart/PostToolUse/SessionEnd 等）实现零干预记忆管理；  
- ✅ **混合搜索架构**：融合 SQLite FTS5 全文检索 + Chroma 向量数据库，兼顾关键词精度与语义相关性；  
- ✅ **可扩展 MCP 工具集**：提供 5 个标准化 MCP（Model Context Protocol）工具，符合 AI Agent 生态规范；  
- ✅ **Beta 实验通道**：支持 Endless Mode 等前沿特性（仿生长时记忆架构），可通过 Web UI 一键切换版本。

3. **技术栈**  
- **运行时**：Node.js ≥18.0.0（主逻辑）、Bun（Worker 服务托管与进程管理）、uv（Python 包管理器，用于 Chroma 向量库依赖）；  
- **数据库**：SQLite 3（嵌入式，含 FTS5 全文搜索支持）+ Chroma（轻量级向量数据库，用于语义检索）；  
- **前端**：静态 Web UI（HTML/CSS/JS），基于本地 HTTP 服务提供实时内存流与交互界面；  
- **协议与标准**：完全兼容 MCP（Model Context Protocol），深度适配 Claude Code 插件系统；  
- **开发与构建**：TypeScript（主力语言）、GitHub Actions（CI/CD）、AGPL-3.0 开源许可证（主体）；  
- **附加组件**：Ragtime 子模块（独立采用 PolyForm Noncommercial License）。

</details>

---

### 11. [ChromeDevTools/chrome-devtools-mcp](https://github.com/ChromeDevTools/chrome-devtools-mcp)
- 📅 **创建日期**：2025-09-11  
- 🔄 **最近更新**：2026-02-13  
- ⭐ **Stars**：24,690（日 +354｜周 +1212｜月 +3782）  
- 📝 **描述**：Chrome DevTools for coding agents  

<details>
<summary><b>📈 Star 与 Commit 历史趋势</b></summary>

![chrome-devtools-mcp Star and Commit Trend](charts/ChromeDevTools_chrome-devtools-mcp_trend.png)

> *蓝色：累计 Stars｜橙色：累计 Commits（次 Y 轴）*

</details>

<details>
<summary><b>📄 README 摘要</b></summary>

1. **项目功能**  
`chrome-devtools-mcp` 是一个 Model-Context-Protocol（MCP）标准兼容的服务端实现，旨在让 AI 编程助手（如 Gemini、Claude、Cursor、Copilot、Codex 等）通过标准化协议**安全、可靠地控制和深度观测运行中的 Chrome 浏览器实例**。它桥接大模型与 Chrome DevTools 原生能力，使 AI 能够执行真实浏览器自动化、全链路调试（网络/控制台/渲染）、性能分析（实验室+现场数据）等任务，而非仅依赖模拟或简化 API。

2. **核心特性**  
- **全栈性能洞察**：支持录制完整 DevTools 性能轨迹（trace），自动分析瓶颈，并可选集成 Google CrUX（Chrome 用户体验报告）API 获取真实用户性能字段数据，实现 lab + field 双维度评估；  
- **深度浏览器调试能力**：实时捕获带源码映射（source-mapped）的控制台日志、细粒度网络请求分析（含请求/响应详情）、全屏/区域截图、DOM 快照（snapshot）及任意脚本执行（`evaluate_script`）；  
- **高可靠性自动化**：基于 Puppeteer 实现语义化操作（点击、拖拽、表单填充、文件上传、对话框处理等），并内置智能等待机制（`wait_for`），确保操作在页面状态就绪后执行；  
- **灵活环境适配**：支持连接已运行的 Chrome 实例（通过 `--browser-url` 或 `--ws-endpoint`）、自动启动隔离/非隔离模式 Chrome（含多频道支持：stable/canary/beta/dev）、自定义代理、视口、证书策略及启动参数；  
- **模块化工具集**：按功能划分为输入自动化（8 项）、导航（6 项）、仿真（2 项）、性能（3 项）、网络（2 项）、调试（5 项）六大类共 26+ 个标准化 MCP 工具，支持按需禁用类别（如 `--category-network=false`）。

3. **技术栈**  
- **运行时**：Node.js（v20.19+ LTS）；  
- **浏览器引擎**：Google Chrome（当前稳定版或更新版本），通过 DevTools Protocol（CDP）通信；  
- **底层驱动**：Puppeteer（用于浏览器生命周期管理、页面操作与等待逻辑）；  
- **协议层**：严格遵循 [Model-Context-Protocol (MCP)](https://modelcontextprotocol.org/) 规范，提供标准 JSON-RPC over stdio / HTTP / WebSocket 的服务接口；  
- **DevTools 集成**：直接复用 Chromium 官方 [devtools-frontend](https://github.com/ChromeDevTools/devtools-frontend) 的性能分析与调试能力；  
- **部署与分发**：以 npm 包（`chrome-devtools-mcp`）形式发布，通过 `npx` 一键启动，零构建依赖。

</details>

---

### 12. [virattt/dexter](https://github.com/virattt/dexter)
- 📅 **创建日期**：2025-10-14  
- 🔄 **最近更新**：2026-02-13  
- ⭐ **Stars**：22,414（日 +265｜周 +4356｜月 +8481）  
- 📝 **描述**：An autonomous agent for deep financial research  

<details>
<summary><b>📈 Star 与 Commit 历史趋势</b></summary>

![dexter Star and Commit Trend](charts/virattt_dexter_trend.png)

> *蓝色：累计 Stars｜橙色：累计 Commits（次 Y 轴）*

</details>

<details>
<summary><b>📄 README 摘要</b></summary>

1. **项目功能**  
Dexter 是一个面向金融研究的自主式AI代理系统，能够对复杂金融问题进行端到端的自动分析：接收用户提问 → 自主规划多步研究任务 → 调用实时市场数据工具（如财报、资产负债表、现金流量表）执行查询 → 对中间结果进行自我验证与反思 → 迭代优化直至生成可信、数据支撑的最终结论。其核心目标是实现“无需人工干预的闭环金融调研”，适用于股票分析、公司基本面评估等专业场景。

2. **关键特性**  
- **智能任务规划**：将模糊或复杂的金融问题（如“对比苹果与英伟达的盈利质量与增长可持续性”）自动拆解为结构化、可执行的研究子任务（例如“获取AAPL/NVDA近5年收入与毛利率”→“计算ROIC趋势”→“分析现金流覆盖比率”）。  
- **自主工具执行与编排**：动态选择并调用适配的API工具（Financial Datasets API 获取结构化财报、Exa/Tavily 进行补充网络检索），支持多源数据融合。  
- **自省与迭代机制**：通过LLM驱动的自我验证（self-reflection）判断任务完成度，若结果不充分或存在矛盾，则自动修正计划、重试或扩展查询，内置循环检测与最大步数限制保障安全性。  
- **实时、机构级财务数据接入**：直连专业金融数据服务（如 Financial Datasets），免费支持主流标的（AAPL/NVDA/MSFT）的完整三张表（利润表、资产负债表、现金流量表）按年/季粒度查询。  
- **可追溯调试能力**：全程记录每一步推理（thinking）、工具调用（tool_result）及原始输入（init）至JSONL格式的本地scratchpad文件，支持完整行为回放与根因分析。

3. **技术栈**  
- **运行时**：Bun（v1.0+）—— 作为高性能JavaScript/TypeScript运行时，替代Node.js，提供极速依赖安装与启动。  
- **核心语言**：TypeScript —— 保障大型Agent系统的类型安全与可维护性。  
- **AI模型层**：支持多后端LLM接入，包括OpenAI（默认）、Anthropic、Google Gemini、xAI及OpenRouter，亦兼容本地Ollama模型（通过`OLLAMA_BASE_URL`配置）。  
- **数据服务**：  
  - 主要财务数据源：Financial Datasets API（机构级结构化财报）；  
  - 补充网络搜索：Exa API（首选）或Tavily API（备用）；  
- **评估与可观测性**：LangSmith —— 用于自动化评测（LLM-as-judge打分）、链路追踪、性能监控与结果分析；  
- **开发与部署友好性**：基于`.env`环境变量管理多API密钥，内置`bun dev`热重载开发模式，CLI驱动交互式运行（`bun start`）。

</details>

---

### 13. [iOfficeAI/AionUi](https://github.com/iOfficeAI/AionUi)
- 📅 **创建日期**：2025-08-07  
- 🔄 **最近更新**：2026-02-13  
- ⭐ **Stars**：21,603（日 +477｜周 +3323｜月 +14512）  
- 📝 **描述**：Free, local, open-source 24/7 Cowork and OpenClaw for Gemini CLI, Claude Code, Codex, OpenCode, Qwen Code, Goose CLI, Auggie, and more | 🌟 Star if you like it!  

<details>
<summary><b>📈 Star 与 Commit 历史趋势</b></summary>

![AionUi Star and Commit Trend](charts/iOfficeAI_AionUi_trend.png)

> *蓝色：累计 Stars｜橙色：累计 Commits（次 Y 轴）*

</details>

---

### 14. [eigent-ai/eigent](https://github.com/eigent-ai/eigent)
- 📅 **创建日期**：2025-07-29  
- 🔄 **最近更新**：2026-02-13  
- ⭐ **Stars**：21,214（日 +58｜周 +434｜月 +12313）  
- 📝 **描述**：Eigent: The Open Source Cowork Desktop to Unlock Your Exceptional Productivity.  

<details>
<summary><b>📈 Star 与 Commit 历史趋势</b></summary>

![eigent Star and Commit Trend](charts/eigent-ai_eigent_trend.png)

> *蓝色：累计 Stars｜橙色：累计 Commits（次 Y 轴）*

</details>

<details>
<summary><b>📄 README 摘要</b></summary>

1. **项目功能**  
Eigent 是一款开源的“协作办公桌面应用”（Cowork Desktop），旨在帮助用户构建、管理和部署定制化的 AI 多智能体工作团队（Multi-Agent Workforce），将复杂业务流程自动化。它支持本地化、私有化运行，无需依赖云端服务，可完全离线执行任务；同时提供云连接模式和企业级部署选项。核心价值在于：通过多个专业化 AI 智能体（如开发者、浏览器、文档、多模态代理）并行协作，动态拆解并执行端到端任务（例如生成旅行行程、分析财务数据、撰写市场研究报告、SEO 审计、PDF 签名等），全程支持人类介入（Human-in-the-Loop），确保结果可控可信。

2. **关键特性**  
- **多智能体工作队列（Workforce）**：预置多种角色代理（Developer/Browser/Document/Multi-modal Agent），支持任务自动分解与并行执行；  
- **全本地模型支持**：无缝集成 vLLM、Ollama、LM Studio 等本地大模型运行时，保障数据隐私与低延迟；  
- **Model Context Protocol（MCP）深度集成**：内置大量开箱即用工具（Web 浏览、代码执行、Notion/Google/Slack 等），并支持用户自定义安装内部 API 或函数工具；  
- **人类在环（Human-in-the-Loop）**：当任务遇阻或存在不确定性时，自动暂停并请求人工确认或输入；  
- **100% 开源 & 本地化部署**：全栈代码开放（Apache 2.0 许可），支持零外部依赖的纯本地部署，无强制账户注册或数据上传；  
- **企业就绪能力**：支持单点登录（SSO）、细粒度访问控制、专属定制开发及 SLA 服务；  
- **MCP 协议原生兼容**：作为 MCP 生态重要实现，强调工具标准化与跨平台互操作性。

3. **技术栈**  
- **后端**：基于 Python 构建，采用 **FastAPI** 作为 Web 框架，**Uvicorn** 异步服务器，**uv** 作为高性能包管理器；认证体系为 **OAuth 2.0 + Passlib**；多智能体编排底层依托 **CAMEL-AI** 框架；  
- **前端 & 桌面层**：使用 **React + TypeScript** 开发，通过 **Electron** 封装为跨平台桌面应用；UI 采用 **Tailwind CSS + Radix UI + Lucide React + Framer Motion**；状态管理使用 **Zustand**；流程可视化编辑器基于 **React Flow**。

</details>

---

### 15. [HandsOnLLM/Hands-On-Large-Language-Models](https://github.com/HandsOnLLM/Hands-On-Large-Language-Models)
- 📅 **创建日期**：2024-06-28  
- 🔄 **最近更新**：2026-02-13  
- ⭐ **Stars**：21,078（日 +305｜周 +827｜月 +1327）  
- 📝 **描述**：Official code repo for the O'Reilly Book - "Hands-On Large Language Models"  

<details>
<summary><b>📈 Star 与 Commit 历史趋势</b></summary>

![Hands-On-Large-Language-Models Star and Commit Trend](charts/HandsOnLLM_Hands-On-Large-Language-Models_trend.png)

> *蓝色：累计 Stars｜橙色：累计 Commits（次 Y 轴）*

</details>

<details>
<summary><b>📄 README 摘要</b></summary>

1. **项目功能**  
该项目是配套技术图书《Hands-On Large Language Models》（中文常译为《动手学大语言模型》）的官方代码仓库，提供全书12章内容所涉及的所有可运行示例代码。其核心目标是通过**交互式Jupyter Notebook**形式，将书中近300幅原创可视化图解转化为可实践、可验证的代码实验，帮助读者从零开始系统掌握大语言模型（LLM）的核心原理与工程应用，涵盖从基础概念（如分词、嵌入）、模型结构（Transformer内部机制）、下游任务（文本分类、聚类、语义搜索），到高级技术（提示工程、RAG、多模态LLM、模型微调与量化）等完整知识链。

2. **关键特性**  
- **全章节覆盖的可执行Notebook**：按章节组织（共12章），每章对应一个Colab Notebook，开箱即用，支持免费T4 GPU加速；  
- **深度可视化驱动学习**：所有代码均服务于书中“图解式教学”理念，强调直观理解（如注意力权重热力图、token嵌入空间投影、RAG流程拆解等）；  
- **端到端实践导向**：不仅演示API调用，更包含从数据预处理、模型加载、训练/微调（BERT、生成式模型）、评估到部署优化（量化、MoE、Mamba等）的完整工作流；  
- **扩展性强的补充资源**：提供独立于主书的“Bonus内容”，包括Mamba、量化、MoE、推理型LLM、Stable Diffusion、DeepSeek-R1等前沿主题的可视化指南与配套代码；  
- **跨平台兼容性设计**：虽推荐Google Colab，但提供本地环境搭建指南（含conda配置、PyTorch安装等），适配不同开发场景。

3. **技术栈**  
- **编程语言**：Python（主流版本，依赖明确）；  
- **核心框架**：PyTorch（模型构建与训练）、Hugging Face Transformers（预训练模型加载与推理）、Sentence-Transformers（文本嵌入）、scikit-learn（传统ML任务）；  
- **辅助库**：NumPy、Pandas、Matplotlib/Seaborn（数据处理与可视化）、UMAP/HDBSCAN（降维与聚类）、LlamaIndex（RAG构建）、LangChain（提示编排）；  
- **部署与优化**：支持模型量化（bitsandbytes等）、高效架构实现（如Mamba、MoE模块）；  
- **运行环境**：默认适配Google Colab（T4 GPU），同时提供conda环境配置方案，兼容Linux/macOS/Windows本地部署。

</details>

---

### 16. [linshenkx/prompt-optimizer](https://github.com/linshenkx/prompt-optimizer)
- 📅 **创建日期**：2025-02-12  
- 🔄 **最近更新**：2026-02-13  
- ⭐ **Stars**：20,893（日 +121｜周 +1312｜月 +2368）  
- 📝 **描述**：一款提示词优化器，助力于编写高质量的提示词  

<details>
<summary><b>📈 Star 与 Commit 历史趋势</b></summary>

![prompt-optimizer Star and Commit Trend](charts/linshenkx_prompt-optimizer_trend.png)

> *蓝色：累计 Stars｜橙色：累计 Commits（次 Y 轴）*

</details>

<details>
<summary><b>📄 README 摘要</b></summary>

1. **项目功能**  
Prompt Optimizer（提示词优化器）是一个面向AI提示工程的全栈式优化工具，核心目标是帮助用户系统性提升提示词质量，从而显著改善大语言模型（LLM）与多模态模型（如图像生成模型）的输出效果。它不替代AI模型，而是作为“提示词智能协作者”，支持从模糊创意（如“写首诗”）到结构化、可复现、高精度提示的转化；同时赋能生产级应用——通过优化提示词降低对模型能力的依赖，使小模型也能稳定输出指定格式（如知识图谱JSON）、保障服务可靠性与成本效益。

2. **关键特性**  
- **双轨智能优化**：独立支持系统提示词（System Prompt）与用户提示词（User Prompt）的针对性优化，并支持多轮迭代精调；  
- **实时对比验证**：内置并行测试面板，可同步运行原始提示与优化后提示，直观比对输出质量差异；  
- **全场景测试能力**：提供高级测试模式，涵盖上下文变量批量管理、多轮会话模拟、Function Calling（工具调用）集成（兼容OpenAI/Gemini）；  
- **多模态支持**：原生集成文生图（T2I）与图生图（I2I）能力，支持Gemini、Seedream等图像模型，并提供尺寸/风格等参数精细调控；  
- **隐私优先架构**：纯客户端执行（Web版/桌面版），所有提示处理、API密钥使用均在本地完成，数据不经过任何中间服务器；  
- **全平台交付**：提供在线Web版、跨平台桌面应用（自动更新）、Chrome浏览器插件、Docker容器化部署四种开箱即用形态；  
- **企业级扩展能力**：支持密码访问控制（ACCESS_PASSWORD）、Model Context Protocol（MCP）协议，可无缝对接Claude Desktop等MCP兼容AI客户端，提供`optimize-system-prompt`、`iterate-prompt`等标准化工具接口。

3. **技术栈**  
- **前端框架**：基于 Vue 3 + TypeScript 构建，采用 Vite 构建工具，UI 组件库为 Naive UI；  
- **桌面端**：使用 Tauri（Rust + WebView2/WebKit）实现轻量、安全、高性能的原生桌面应用，规避浏览器CORS限制；  
- **构建与包管理**：使用 pnpm 作为包管理器，支持 Monorepo 风格开发；  
- **部署方案**：支持 Vercel（Serverless静态托管）、Docker（标准镜像 `linshen/prompt-optimizer` 及阿里云国内镜像）、Docker Compose（含 MCP 服务一体化部署）；  
- **协议与集成**：深度支持 MCP（Model Context Protocol）标准，兼容 OpenAI 兼容 API、Gemini SDK、DeepSeek、智谱AI（Zhipu）、SiliconFlow、DashScope、ModelScope 等主流厂商接口；  
- **安全与配置**：通过环境变量（如 `VITE_OPENAI_API_KEY`）或前端界面动态注入模型凭证，支持 `llmParams` 字段精细化配置各模型专属参数（temperature、max_tokens等）。

</details>

---

### 17. [vercel-labs/agent-skills](https://github.com/vercel-labs/agent-skills)
- 📅 **创建日期**：2025-12-08  
- 🔄 **最近更新**：2026-02-13  
- ⭐ **Stars**：20,150（日 +156｜周 +932｜月 +19953）  
- 📝 **描述**：Vercel's official collection of agent skills  

<details>
<summary><b>📈 Star 与 Commit 历史趋势</b></summary>

![agent-skills Star and Commit Trend](charts/vercel-labs_agent-skills_trend.png)

> *蓝色：累计 Stars｜橙色：累计 Commits（次 Y 轴）*

</details>

<details>
<summary><b>📄 README 摘要</b></summary>

1. **项目功能**  
该项目是一个面向AI编程代理（AI coding agents）的可复用技能库（Agent Skills），提供结构化、即插即用的领域专业知识模块。每个“技能”本质上是一组标准化的指令文档（`SKILL.md`）、自动化脚本（`scripts/`）及参考材料（`references/`），用于指导AI代理在特定技术场景下执行高质量、符合最佳实践的任务，如代码审查、性能优化、UI合规审计、跨平台开发指导及一键部署等。技能本身不运行代码，而是为AI代理提供上下文感知的决策依据与操作规范，使其能更精准地响应用户自然语言指令（例如“优化这个Next.js页面”或“检查我的UI可访问性”）。

2. **核心特性**  
- **标准化格式兼容性**：严格遵循 [Agent Skills](https://agentskills.io/) 开放规范，确保跨平台AI代理（如Claude Desktop、claude.ai）可统一识别、加载与调用；  
- **场景驱动的垂直技能集**：涵盖五大高价值方向——  
  • `react-best-practices`：基于Vercel工程实践的40+条React/Next.js性能规则，按影响等级（Critical/High/Medium等）分类，覆盖水falls消除、Bundle优化、服务端渲染、重渲染控制等；  
  • `web-design-guidelines`：100+条Web UI综合审计规则，深度覆盖无障碍（a11y）、焦点管理、表单、动画、排版、图片、性能、导航状态、深色模式、触控交互及国际化（i18n）；  
  • `react-native-guidelines`：专为AI代理优化的16条React Native/Expo实践，聚焦移动端性能（FlashList）、布局安全区、Reanimated动画、图片缓存、Zustand状态管理及iOS/Android平台适配；  
  • `composition-patterns`：React组件架构技能，系统性解决布尔属性泛滥问题，提供复合组件、状态提升、内部组合、避免属性透传等可扩展设计模式；  
  • `vercel-deploy-claimable`：零配置Vercel部署能力，支持自动框架识别（40+）、静态HTML处理、`node_modules`/`.git`智能排除，并生成可移交所有权的“Claim URL”，实现对话内一键发布；  
- **开箱即用的集成体验**：通过一行命令（`npx skills add vercel-labs/agent-skills`）即可安装，技能由AI代理自动感知并触发，无需手动调用或参数配置；  
- **输出明确、结果可信**：部署类技能返回结构化结果（Preview URL + Claim URL），审查类技能提供带优先级分类的可操作建议，增强AI响应的可验证性与专业性。

3. **技术栈**  
- **核心协议/标准**：Agent Skills 规范（Markdown为主载体，含结构化元数据）；  
- **交付形态**：纯静态资源仓库（GitHub托管），包含 `SKILL.md`（主指令文档）、`scripts/`（Shell/Node.js等轻量脚本，用于自动化辅助）、`references/`（PDF/HTML等补充资料）；  
- **部署能力依赖**：`vercel-deploy-claimable` 技能底层调用 Vercel CLI 或其公开API，依赖 Node.js 运行时执行打包（tarball）、框架探测与上传逻辑；  
- **运行环境**：非独立应用，作为插件嵌入支持Agent Skills协议的AI代理平台（如Claude生态），无前端界面或后端服务；  
- **许可证**：MIT开源协议，允许自由使用、修改与分发。

</details>

---

### 18. [VectifyAI/PageIndex](https://github.com/VectifyAI/PageIndex)
- 📅 **创建日期**：2025-04-01  
- 🔄 **最近更新**：2026-02-13  
- ⭐ **Stars**：19,797（日 +98｜周 +1264｜月 +9719）  
- 📝 **描述**：📑 PageIndex: Document Index for Vectorless, Reasoning-based RAG  

<details>
<summary><b>📈 Star 与 Commit 历史趋势</b></summary>

![PageIndex Star and Commit Trend](charts/VectifyAI_PageIndex_trend.png)

> *蓝色：累计 Stars｜橙色：累计 Commits（次 Y 轴）*

</details>

<details>
<summary><b>📄 README 摘要</b></summary>

1. **该项目的功能**  
PageIndex 是一个面向长文档（如财务报告、法律文件、学术教材等）的新型检索增强生成（RAG）系统，其核心目标是**取代传统基于向量数据库（Vector DB）和文本分块（Chunking）的语义相似性检索范式**。它不依赖向量嵌入或近似匹配，而是通过构建文档的**语义层次化树索引（Tree Index）**，并利用大语言模型（LLM）进行**推理驱动的树搜索（reasoning-based tree search）**，实现精准、可解释、类人式的上下文相关检索。该系统直接作用于原始PDF或Markdown文档，支持端到端的“向量化无关”（vectorless）文档理解与问答。

2. **关键特性**  
- **零向量数据库（No Vector DB）**：完全摒弃嵌入计算与向量相似度搜索，避免“vibe retrieval”（凭感觉匹配）导致的相关性偏差；  
- **零人工分块（No Chunking）**：基于文档天然结构（标题层级、章节逻辑）组织内容，保留语义完整性与上下文连贯性；  
- **类人推理式检索（Human-like, Reasoning-based Retrieval）**：模拟专家阅读行为，通过LLM在树索引中执行多步推理（如“先定位章节→再聚焦子节→最终提取关键段落”），实现高精度定位；  
- **强可解释性与可追溯性**：每次检索结果附带明确的页面号、节点ID及路径引用，支持审计与调试，告别黑箱向量匹配；  
- **原生视觉支持（Vision-native）**：提供OCR-Free方案，可直接对PDF页面图像进行推理式RAG，绕过传统OCR误差与结构丢失问题；  
- **高性能实证验证**：驱动的金融分析系统 Mafin 2.5 在 FinanceBench 基准测试中达成 **98.7% 准确率**，显著超越主流向量RAG方案。

3. **技术栈**  
- **核心模型层**：依赖 OpenAI 系列大模型（默认 `gpt-4o-2024-11-20`）执行树索引构建与推理搜索；  
- **文档解析层**：支持 PDF（基于 PyPDF2 / pdfplumber 等库的文本提取）与 Markdown（按 `#` 标题层级解析）双输入格式；  
- **索引结构**：自研**分层树状索引（Tree Index）**，以 JSON 格式表达文档语义结构（含 `title`、`node_id`、`start/end_index`、`summary` 及嵌套 `nodes`）；  
- **部署与集成**：提供本地开源 CLI 工具（`run_pageindex.py`）、云服务（[chat.pageindex.ai](https://chat.pageindex.ai)）、MCP 协议插件（兼容 Claude/Cursor 等代理环境）及 RESTful API；  
- **开发与运行环境**：Python 3.x，依赖 `openai`, `pypdf`, `python-dotenv`, `tqdm` 等标准库，支持 Google Colab 快速实验。

</details>

---

### 19. [KeygraphHQ/shannon](https://github.com/KeygraphHQ/shannon)
- 📅 **创建日期**：2025-09-27  
- 🔄 **最近更新**：2026-02-13  
- ⭐ **Stars**：18,230（日 +455｜周 +14472｜月 +14551）  
- 📝 **描述**：Fully autonomous AI hacker to find actual exploits in your web apps. Shannon has achieved a 96.15% success rate on the hint-free, source-aware XBOW Benchmark.  

<details>
<summary><b>📈 Star 与 Commit 历史趋势</b></summary>

![shannon Star and Commit Trend](charts/KeygraphHQ_shannon_trend.png)

> *蓝色：累计 Stars｜橙色：累计 Commits（次 Y 轴）*

</details>

<details>
<summary><b>📄 README 摘要</b></summary>

1. **该项目做什么？**  
Shannon 是一个面向源码的全自动 AI 渗透测试工具，专为白盒（white-box）Web 应用安全测试设计。其核心目标是**在漏洞被真实攻击者利用前，自主发现并实际执行可复现的攻击链**，而非仅生成静态告警。它通过分析用户提供的源代码仓库（REPO），结合动态浏览器交互与命令行攻击，在运行中的目标应用（URL）上验证漏洞的真实可利用性，输出经实证的高置信度安全报告。项目定位为填补“高频开发”与“低频人工渗透测试”之间的安全缺口，实现按需、持续、自动化的真实渗透验证。

2. **关键特性**  
- **全自主渗透流程**：单命令启动，自动处理复杂认证（含 2FA/TOTP、Google 登录）、页面导航、多路径探索与结果聚合，全程无需人工干预；  
- **实证型报告与 PoC 驱动**：严格遵循“无 exploit，不报告”原则，仅输出经成功触发的漏洞，附带可一键复现的复制粘贴式 Proof-of-Concept（PoC），彻底消除误报；  
- **深度 OWASP 覆盖与验证**：当前支持 Injection、XSS、SSRF、Broken Authentication/Authorization 等关键漏洞类型的**源码感知识别 + 动态实操验证**；  
- **代码感知的动态测试（Code-Aware Dynamic Testing）**：融合静态源码分析（指导攻击策略）与动态黑盒执行（浏览器+CLI 实际攻击），确保风险真实存在；  
- **集成专业安全工具链**：内置调用 Nmap、Subfinder、WhatWeb、Schemathesis 等工具强化侦察与接口分析能力；  
- **并行化高效执行**：对 Recon、Vuln Analysis、Exploitation 等耗时阶段全面并行化，显著缩短测试周期；  
- **白盒专用架构**：明确要求访问源代码（`./repos/` 目录结构），不支持纯黑盒或远程扫描。

3. **技术栈**  
- **核心推理引擎**：基于 Anthropic Claude Agent SDK（主推 Anthropic API，实验性支持 OpenAI/Gemini via Router Mode）；  
- **运行时环境**：Docker 容器化部署，保障环境隔离与可移植性；  
- **工作流编排**：采用 Temporal（通过 `http://localhost:8233` Web UI 监控）实现多阶段、容错、可观测的分布式任务调度；  
- **安全工具集成**：Nmap（网络测绘）、Subfinder（子域发现）、WhatWeb（指纹识别）、Schemathesis（API 模糊测试）；  
- **自动化执行层**：浏览器自动化（用于登录、交互式攻击）、命令行工具调用（用于注入、SSRF 等 CLI 场景）；  
- **配置与扩展**：YAML 配置驱动（支持自定义登录流程、TOTP、测试范围规则等），模块化多智能体架构（Recon → Parallel Vuln Analysis → Parallel Exploitation → Reporting）。

</details>

---

### 20. [hsliuping/TradingAgents-CN](https://github.com/hsliuping/TradingAgents-CN)
- 📅 **创建日期**：2025-06-26  
- 🔄 **最近更新**：2026-02-13  
- ⭐ **Stars**：17,202（日 +110｜周 +1570｜月 +2473）  
- 📝 **描述**：基于多智能体LLM的中文金融交易框架 - TradingAgents中文增强版  

<details>
<summary><b>📈 Star 与 Commit 历史趋势</b></summary>

![TradingAgents-CN Star and Commit Trend](charts/hsliuping_TradingAgents-CN_trend.png)

> *蓝色：累计 Stars｜橙色：累计 Commits（次 Y 轴）*

</details>

<details>
<summary><b>📄 README 摘要</b></summary>

1. **项目功能**  
本项目是一个面向中文用户的**多智能体与大模型股票分析学习平台**，基于开源框架 `TradingAgents` 进行深度本地化增强。其核心定位为**合规、非实盘的教育与研究工具**，旨在帮助用户系统学习如何利用多智能体架构（Multi-Agent System）和大语言模型（LLM）开展股票基本面、技术面、新闻舆情等多维度分析，支持 A股、港股、美股市场，但**不生成或执行任何实盘交易指令**。

2. **关键特性**  
- **全栈中文化与本土适配**：完整中文界面、A股数据源（Tushare/AkShare/BaoStock）、国产大模型（通义千问、DeepSeek等）集成、符合中文金融语境的提示词与分析逻辑；  
- **企业级多智能体分析能力**：支持动态LLM供应商管理、任务驱动的智能模型自动选型（如新闻分析用Gemini、财报解读用Qwen）、多分析师协同（新闻/技术/基本面/情绪等角色分工）；  
- **专业研究工作流**：自选股管理、多股批量分析、智能股票筛选（多维指标排序）、虚拟模拟交易系统、Markdown/Word/PDF三格式专业分析报告导出；  
- **现代化工程架构**：FastAPI + Vue 3 全新前后端分离架构，MongoDB + Redis 双缓存数据库，SSE+WebSocket 实时进度推送，Docker 多架构（amd64/arm64）一键部署；  
- **生产就绪治理能力**：RBAC用户权限体系、可视化配置中心（模型/数据源/系统参数）、统一日志与操作审计、成本监控与缓存策略管理；  
- **强健性与准确性保障**：修复原版技术指标（MACD/RSI等）与财务数据（PE/PB）计算缺陷，杜绝死循环，确保多分析师数据源一致性。

3. **技术栈**  
- **后端**：Python 3.10+，FastAPI + Uvicorn（替代原Streamlit），MongoDB（主存储）、Redis（高速缓存与会话管理），Celery（异步任务调度）；  
- **前端**：Vue 3 + Vite + Element Plus（现代化响应式SPA），集成WebSocket/SSE实时通信；  
- **AI与数据层**：原生OpenAI API、Google Gemini、DeepSeek、通义千问等多LLM提供商SDK；Tushare、AkShare、BaoStock 等A股主流数据接口；新闻聚合与质量评估模块；  
- **基础设施**：Docker Compose 多容器编排（含app、frontend、mongo、redis、nginx），GitHub Actions 自动化CI/CD与镜像构建，支持x86_64及ARM64（Apple Silicon/树莓派/AWS Graviton）；  
- **许可证架构**：混合授权——核心算法与工具代码采用 **Apache 2.0 开源协议**；`app/`（FastAPI后端）与 `frontend/`（Vue前端）目录为**专有组件，商业使用需单独授权**。

</details>

---

### 21. [danielmiessler/Personal_AI_Infrastructure](https://github.com/danielmiessler/Personal_AI_Infrastructure)
- 📅 **创建日期**：2025-09-08  
- 🔄 **最近更新**：2026-02-13  
- ⭐ **Stars**：13,070（日 +581｜周 +1612｜月 +3919）  
- 📝 **描述**：Agentic AI Infrastructure for magnifying HUMAN capabilities.  

<details>
<summary><b>📈 Star 与 Commit 历史趋势</b></summary>

![Personal_AI_Infrastructure Star and Commit Trend](charts/danielmiessler_Personal_AI_Infrastructure_trend.png)

> *蓝色：累计 Stars｜橙色：累计 Commits（次 Y 轴）*

</details>

<details>
<summary><b>📄 README 摘要</b></summary>

1. **该项目的功能**  
PAI（Personal AI Infrastructure，个人AI基础设施）是一个开源的、面向用户的AI平台，旨在将大语言模型（LLM）转化为真正“懂你”的长期智能助手（Digital Assistant, DA）。它不局限于单次问答或工具调用，而是构建一个持续学习、目标驱动、深度个性化的AI系统：通过捕获用户反馈（如评分、修正、验证结果）、记忆个人目标与偏好（TELOS文档体系）、并基于科学方法论（观察→思考→计划→执行→验证→学习）闭环迭代，使AI随时间推移越来越精准地服务于个体的独特需求。其核心使命是“激活人类潜能”——帮助普通人系统性地发现自我、明确目标、提升高主动性，并让顶级AI能力摆脱技术或经济门槛，实现普惠可及。

2. **关键特性**  
- **目标导向（Goal-Oriented）**：以用户的人生使命、具体项目与长期目标（通过10份TELOS文档如`MISSION.md`、`GOALS.md`等结构化定义）为执行中心，而非仅响应临时任务。  
- **持续自主学习（Continuous Learning Loop）**：内置三层次记忆系统（热/温/冷），自动收集交互信号（成功率、用户修改、情感倾向等），驱动技能、工作流与系统行为的渐进式优化。  
- **模块化能力架构（Primitives）**：包含10+核心组件，如：  
  • **技能系统（Skill System）**：严格遵循“代码→CLI工具→提示词→技能”确定性链路，确保结果可复现；  
  • **钩子系统（Hook System）**：8类生命周期事件（如会话启动、任务完成）触发自动化响应（通知、安全校验、上下文加载）；  
  • **安全系统（Security System）**：默认启用权限策略，预检危险命令（如`rm -rf`），无需手动跳过安全检查；  
  • **AI驱动安装（AI-Based Installation）**：由AI助手解析Pack包、适配本地环境并全自动完成部署；  
  • **终端原生UI（Terminal-Based UI）**：动态状态栏、多窗格管理、实时显示学习信号与任务状态；  
  • **语音系统（Voice System）**：集成ElevenLabs TTS，支持自然语调的语音播报与交互；  
  • **用户/系统分离（User/System Separation）**：`USER/`目录存放所有个性化配置，升级时完全隔离，保障可移植性与稳定性。  

3. **技术栈**  
- **核心语言与运行时**：TypeScript（强类型保障系统可靠性） + Bun（超快JavaScript/TypeScript运行时，用于脚本执行与安装流程）；  
- **AI基础设施依赖**：深度集成Claude（Anthropic）生态，设计初衷即为增强Claude Code等客户端能力，非独立模型训练框架；  
- **架构范式**：严格遵循UNIX哲学（单一职责、文本接口、可组合性）与SRE工程实践（版本控制、自动化、可观测性）；  
- **辅助技术**：ElevenLabs（语音合成）、ntfy（跨平台推送通知）、Discord（社区协作）、Git（全生命周期版本管理）；  
- **设计理念支撑**：所有技术选型服务于16条PAI原则，尤其强调“确定性基础设施”（避免LLM随机性污染系统层）和“CLI优先”（命令行作为唯一可信交互界面）。

</details>

---

### 22. [badlogic/pi-mono](https://github.com/badlogic/pi-mono)
- 📅 **创建日期**：2025-08-09  
- 🔄 **最近更新**：2026-02-13  
- ⭐ **Stars**：11,519（日 +415｜周 +4024｜月 +9835）  
- 📝 **描述**：AI agent toolkit: coding agent CLI, unified LLM API, TUI & web UI libraries, Slack bot, vLLM pods  

<details>
<summary><b>📈 Star 与 Commit 历史趋势</b></summary>

![pi-mono Star and Commit Trend](charts/badlogic_pi-mono_trend.png)

> *蓝色：累计 Stars｜橙色：累计 Commits（次 Y 轴）*

</details>

<details>
<summary><b>📄 README 摘要</b></summary>

1. **项目功能**  
该项目是一个面向 AI 代理（AI Agents）开发与大语言模型（LLM）部署管理的开源单体仓库（monorepo），核心目标是提供一套模块化、可组合的工具链，用于构建、运行和部署智能编码与交互式 AI 代理系统。它不直接提供终端用户产品，而是为开发者和研究者提供底层基础设施——包括统一的多厂商 LLM 接口、轻量级代理运行时、终端/Web 界面库、GPU 推理服务编排工具，以及与 Slack 等协作平台集成的机器人能力。

2. **关键特性**  
- ✅ **多提供商 LLM 抽象层**：`@mariozechner/pi-ai` 封装 OpenAI、Anthropic、Google 等主流 API，屏蔽厂商差异，支持无缝切换与负载均衡。  
- ✅ **可扩展代理运行时**：`@mariozechner/pi-agent-core` 提供标准化工具调用（tool calling）、会话状态管理、记忆持久化与执行生命周期控制。  
- ✅ **开箱即用的交互式编码代理**：`@mariozechner/pi-coding-agent` 是命令行版 AI 编程助手，支持文件操作、代码生成与调试辅助。  
- ✅ **生产就绪部署工具**：`@mariozechner/pi-pods` 提供 CLI 管理基于 vLLM 的 GPU 推理服务集群（如 Kubernetes pod），简化本地/边缘 LLM 部署。  
- ✅ **跨平台 UI 支持**：`pi-tui`（终端界面，含差分渲染优化）与 `pi-web-ui`（Web 组件库）共同支撑多模态人机交互体验。  
- ✅ **企业级集成能力**：`pi-mom` 实现 Slack 消息自动路由至编码代理，打通团队协作工作流。  

3. **技术栈**  
- **语言与运行时**：TypeScript（全栈主导）、Node.js（v18+）  
- **构建与包管理**：npm（monorepo 管理）、Turborepo 或自定义 npm script 编排（隐含于 `npm run build/check` 流程）  
- **前端框架**：无重型框架依赖；`pi-web-ui` 基于标准 Web Components（Custom Elements + Shadow DOM），`pi-tui` 使用纯终端渲染（可能基于 `blessed` 或自研渲染器）  
- **AI/LLM 集成**：适配 OpenAI v1.x、Anthropic Messages API、Google Gemini 等现代 LLM 接口；推理后端支持 vLLM（通过 `pi-pods`）  
- **基础设施与部署**：面向 GPU 加速场景，深度集成 vLLM；CI/CD 使用 GitHub Actions（`ci.yml`）  
- **协作与生态**：Discord 社区支持；MIT 开源协议；域名与品牌资源由 exe.dev 等合作伙伴捐赠

</details>

---

### 23. [microsoft/RD-Agent](https://github.com/microsoft/RD-Agent)
- 📅 **创建日期**：2024-04-03  
- 🔄 **最近更新**：2026-02-13  
- ⭐ **Stars**：11,099（日 +28｜周 +293｜月 +885）  
- 📝 **描述**：Research and development (R&D) is crucial for the enhancement of industrial productivity, especially in the AI era, where the core aspects of R&D are mainly focused on data and models. We are committed to automating these high-value generic R&D processes through R&D-Agent, which lets AI drive data-driven AI. 🔗https://aka.ms/RD-Agent-Tech-Report  

<details>
<summary><b>📈 Star 与 Commit 历史趋势</b></summary>

![RD-Agent Star and Commit Trend](charts/microsoft_RD-Agent_trend.png)

> *蓝色：累计 Stars｜橙色：累计 Commits（次 Y 轴）*

</details>

<details>
<summary><b>📄 README 摘要</b></summary>

1. **项目功能**  
RD-Agent（R&D-Agent）是一个面向工业级研发（R&D）流程自动化的开源多智能体框架，核心目标是**自动化数据驱动场景下的机器学习工程全生命周期**。它不局限于单点任务（如调参或写代码），而是系统性地模拟人类研究员（Research）与开发工程师（Development）的协同闭环：从提出新想法（如新因子、新模型结构、新特征）、设计实验、生成可执行代码，到运行验证、分析结果、迭代优化，最终形成自主演进的研发循环。目前已在量化金融（因子-模型联合优化）、Kaggle数据科学竞赛、学术论文/财报驱动的模型构建、医疗预测建模等真实复杂场景中落地验证，并在权威ML工程基准 **MLE-Bench** 上取得当前最优性能（SOTA），成为首个被实证为“最佳机器学习工程智能体”的开源系统。

2. **关键特性**  
- **双角色协同架构（R+D）**：内置独立但紧密协作的“研究智能体”（负责假设生成、方案设计、知识推理）和“开发智能体”（负责代码实现、环境部署、实验执行），支持交替优化与反馈闭环。  
- **全栈量化金融自动化（RD-Agent(Q)）**：业界首个数据为中心的量化多智能体框架，实现因子挖掘、模型构建、回测验证、组合优化的端到端联合演化，在实盘级实验中以<10美元成本达成2倍于传统因子库的年化收益（ARR），且因子数量减少70%以上。  
- **多场景泛化能力**：原生支持四大核心场景——  
  • 量化金融（`fin_quant`/`fin_factor`/`fin_model`/`fin_factor_report`）；  
  • 学术/财报驱动的模型研发（`general_model`）；  
  • Kaggle竞赛全自动解题（特征工程+模型调优）；  
  • 通用数据科学工程（`data_science`，含医疗预测等垂直领域）。  
- **强鲁棒性与可复现性**：深度集成 **Qlib**（微软量化平台）、支持 **LiteLLM** 统一后端（兼容OpenAI/Azure/DeepSeek/SiliconFlow等20+ LLM提供商），提供完整配置化、容器化（Docker）部署方案及健康检查（`rdagent health_check`）；  
- **生产就绪工具链**：内置文档生成、UI可视化监控（Live Demo）、详细运行日志追踪、多种子实验统计（含均值±标准差）、与主流开发工具链（pre-commit/mypy/Ruff/Conda）深度集成。

3. **技术栈**  
- **编程语言**：Python 3.10/3.11（类型提示完善，mypy静态检查）；  
- **核心框架**：基于 **LiteLLM** 作为默认LLM抽象层（支持异构模型路由、fallback、负载均衡）；底层可插拔接入 OpenAI API、Azure OpenAI、DeepSeek 官方API、SiliconFlow 等；嵌入模型支持 BGE 系列（如 `bge-m3`, `bge-large-en-v1.5`）；  
- **基础设施**：Docker 容器化部署（强制依赖）、Conda 环境管理、Linux 平台专用（官方仅支持）；  
- **工程实践**：GitHub Actions 全流程CI/CD（测试/扫描/发布/文档构建）、pre-commit 钩子、Ruff 代码格式化、Read the Docs 文档系统；  
- **领域依赖**：深度集成 **Qlib**（量化策略研发）、Selenium（网页报告解析）、Chromedriver（Kaggle数据抓取）、Kaggle API；  
- **许可证**：MIT 开源协议。

</details>

---

### 24. [cheahjs/free-llm-api-resources](https://github.com/cheahjs/free-llm-api-resources)
- 📅 **创建日期**：2024-07-04  
- 🔄 **最近更新**：2026-02-13  
- ⭐ **Stars**：10,406（日 +441｜周 +2212｜月 +2617）  
- 📝 **描述**：A list of free LLM inference resources accessible via API.  

<details>
<summary><b>📈 Star 与 Commit 历史趋势</b></summary>

![free-llm-api-resources Star and Commit Trend](charts/cheahjs_free-llm-api-resources_trend.png)

> *蓝色：累计 Stars｜橙色：累计 Commits（次 Y 轴）*

</details>

<details>
<summary><b>📄 README 摘要</b></summary>

1. **项目功能**  
该项目是一个持续维护的、开源的免费大语言模型（LLM）API资源汇总清单，旨在为开发者、研究人员和普通用户提供当前可免费或通过试用额度调用的合法、合规的LLM服务入口。它不提供自有API或运行时服务，而是系统性地整理、分类并实时更新全球范围内支持免密钥/免付费注册即可使用的主流LLM API服务商及其具体模型、访问限制（如QPS、日请求量、Token配额）、使用条件（如是否需手机号验证、数据训练授权、地域限制等），并明确排除所有非官方、逆向工程类或存在法律风险的服务。

2. **核心特性**  
- **双层结构化分类**：严格划分为「完全免费提供商」（Free Providers）与「提供试用额度的提供商」（Providers with trial credits），便于用户按需快速筛选；  
- **细粒度限额透明化**：对每家服务商均明确标注关键限制参数（如每分钟请求数、每日/每月Token上限、单次上下文窗口约束等），部分含表格化对比，避免隐性超限；  
- **模型覆盖广且时效性强**：收录超100+主流模型（含Llama 3/4、Gemma 3、Qwen 3/3.5、Mistral系列、DeepSeek-R1/V3、GLM-4.5/4.6、Solar Pro、Kimi-K2、Grok、Phi-4等），并动态关联至各平台最新公开模型页；  
- **合规性与可用性警示**：显著标注数据隐私政策（如Google AI Studio在欧盟外使用即默认用于训练）、验证要求（手机号/支付方式）、地域限制及滥用警告，强调可持续使用伦理；  
- **自动化维护机制**：README文件由脚本`src/pull_available_models.py`自动生成，确保信息同步性与低人工维护成本。

3. **技术栈**  
该项目本质为静态文档型资源库，**无运行时代码或后端服务**，因此其“技术栈”体现为支撑信息组织、生成与协作的工具链：  
- **核心生成工具**：Python（含`requests`/`BeautifulSoup`等库）——用于自动抓取/解析各API平台公开的模型列表与配额文档；  
- **文档格式**：Markdown（GitHub Flavored）——作为唯一交付载体，支持渲染、锚点跳转与版本追溯；  
- **协作与发布基础设施**：GitHub平台（含Actions自动化流水线、PR审查流程）——保障多人协同更新与变更审计；  
- **辅助生态**：链接深度整合各服务商官方控制台、文档中心与模型Hub（如Hugging Face、NVIDIA NIM、Google Vertex AI Model Garden），依赖其公开API与网页结构化数据。

</details>

---

### 25. [EveryInc/compound-engineering-plugin](https://github.com/EveryInc/compound-engineering-plugin)
- 📅 **创建日期**：2025-10-09  
- 🔄 **最近更新**：2026-02-13  
- ⭐ **Stars**：8,772（日 +127｜周 +1452｜月 +4120）  
- 📝 **描述**：Official Claude Code compound engineering plugin  

<details>
<summary><b>📈 Star 与 Commit 历史趋势</b></summary>

![compound-engineering-plugin Star and Commit Trend](charts/EveryInc_compound-engineering-plugin_trend.png)

> *蓝色：累计 Stars｜橙色：累计 Commits（次 Y 轴）*

</details>

<details>
<summary><b>📄 README 摘要</b></summary>

1. **项目功能**  
该项目是一个面向 AI 编程助手的**跨平台插件适配与同步工具集**，核心目标是实现「复合式工程（Compound Engineering）」工作流。它将专为 Claude Code 设计的 `compound-engineering` 插件（含规划、执行、评审、知识沉淀等智能工作流能力）**自动转换并部署到多个主流 AI 编程环境**，包括 OpenCode、Codex、Factory Droid、Cursor 和 Pi；同时支持将用户在 Claude Code 中的个人配置（技能 Skills、MCP 服务器设置）**单向同步至其他平台**，确保工程知识和工作习惯在不同工具间复用，避免重复配置与知识孤岛。

2. **关键特性**  
- ✅ **多平台插件格式转换**：通过 CLI 命令（如 `bunx ... --to opencode`）一键将 Claude 插件转换为各平台原生格式（OpenCode 的 `opencode.json` + 目录结构、Codex 的 prompt/skill 双生成、Droid 的命令/代理映射、Cursor 的 `.mdc` 规则与 `mcp.json`、Pi 的 MCPorter 兼容结构）。  
- ✅ **智能配置同步**：支持 `sync` 命令将 `~/.claude/` 下的个人技能（符号链接，实时生效）和 MCP 服务器配置同步至目标平台，实现「一次配置，多端生效」。  
- ✅ **标准化复合工作流**：内置 `/workflows:plan` / `:work` / `:review` / `:compound` 四阶段命令，覆盖从需求拆解、任务执行、多智能体代码评审到经验沉淀的完整闭环，强调「每轮迭代都降低后续工作的难度」。  
- ✅ **语义化工具映射与兼容性处理**：针对不同平台能力差异进行适配（如 Codex 技能描述截断至 1024 字符、Droid 工具名标准化映射、Cursor 采用 `alwaysApply: false` 的按需触发规则），保障功能可用性。  
- ✅ **本地开发友好**：提供 `bun run src/index.ts` 直接运行转换逻辑，便于插件开发者调试与定制。

3. **技术栈**  
- **运行时**：Bun（作为默认 JavaScript 运行时与包管理器，主打高性能与极简 CLI 体验）  
- **语言**：TypeScript（强类型保障 CLI 工具可靠性与可维护性）  
- **核心依赖**：`@every-env/compound-plugin`（NPM 发布的 CLI 包，版本受 `npm` badge 管控）  
- **文件系统操作**：深度依赖 Unix 风格路径约定（`~/.config/opencode`, `~/.codex/`, `~/.cursor/`, `~/.pi/` 等），利用符号链接（symlinks）实现技能的实时同步  
- **架构模式**：CLI 驱动的格式转换器 + 配置同步器，无后端服务，纯客户端工具链

</details>

---

### 26. [openai/skills](https://github.com/openai/skills)
- 📅 **创建日期**：2025-11-25  
- 🔄 **最近更新**：2026-02-13  
- ⭐ **Stars**：8,320（日 +177｜周 +3699｜月 +6782）  
- 📝 **描述**：Skills Catalog for Codex  

<details>
<summary><b>📈 Star 与 Commit 历史趋势</b></summary>

![skills Star and Commit Trend](charts/openai_skills_trend.png)

> *蓝色：累计 Stars｜橙色：累计 Commits（次 Y 轴）*

</details>

<details>
<summary><b>📄 README 摘要</b></summary>

1. **项目功能**  
该项目定义并维护一套标准化的“Agent Skills”（智能体技能）规范与资源集合，旨在为AI智能体（特别是OpenAI Codex平台中的智能体）提供可发现、可复用、可分发的任务执行能力。每个Skill是一个独立的文件夹，内含指令（prompt）、脚本、配置及依赖资源，使AI能以结构化方式完成特定任务（如代码审查、计划生成、地址解析等）。核心价值是“一次编写，多处复用”，支持团队和个人沉淀和共享可重复使用的AI能力单元。

2. **关键特性**  
- **标准化技能格式**：遵循公开的[Agent Skills开放标准](https://agentskills.io)，确保跨平台兼容性与互操作性；  
- **分层技能管理**：按可信度与成熟度划分为三类——自动集成的`.system`技能（内置核心能力）、经人工审核的`.curated`技能（推荐使用）、以及需自行评估的`.experimental`技能（前沿探索）；  
- **便捷安装机制**：通过Codex内置命令`$skill-installer`支持按名称、本地路径或GitHub URL一键安装，安装后重启即可生效；  
- **细粒度授权控制**：每个Skill目录内含独立的`LICENSE.txt`文件，明确其开源协议与使用条款，便于合规分发与集成。

3. **技术栈**  
- **核心平台**：深度集成于OpenAI Codex（AI编程助手/智能体运行环境），依赖其技能加载、执行与上下文管理机制；  
- **组织结构**：纯文件系统驱动，采用Git版本控制的目录结构（`skills/.system/`, `skills/.curated/`, `skills/.experimental/`），无运行时服务或数据库；  
- **分发协议**：基于HTTPS和GitHub REST API实现远程技能拉取（支持直接解析GitHub Tree URL）；  
- **元数据与规范**：依赖约定式文件命名、目录结构及文档（如`LICENSE.txt`）支撑自动化识别与策略治理，不依赖特定编程语言或框架。

</details>

---

### 27. [tobi/qmd](https://github.com/tobi/qmd)
- 📅 **创建日期**：2025-12-08  
- 🔄 **最近更新**：2026-02-13  
- ⭐ **Stars**：8,249（日 +162｜周 +1522｜月 +6658）  
- 📝 **描述**：mini cli search engine for your docs, knowledge bases, meeting notes, whatever. Tracking current sota approaches while being all local  

<details>
<summary><b>📈 Star 与 Commit 历史趋势</b></summary>

![qmd Star and Commit Trend](charts/tobi_qmd_trend.png)

> *蓝色：累计 Stars｜橙色：累计 Commits（次 Y 轴）*

</details>

<details>
<summary><b>📄 README 摘要</b></summary>

1. **项目功能**  
QMD（Query Markup Documents）是一个**纯本地运行的设备端搜索引擎**，专为个人知识管理与智能体（agentic）工作流设计。它可对用户本地的 Markdown 笔记、会议记录、技术文档、知识库等文本内容进行统一索引与跨源检索。支持三种搜索模式：基于关键词的快速 BM25 全文搜索（`qmd search`）、基于语义相似度的向量搜索（`qmd vsearch`），以及融合查询扩展、多路并行检索与大语言模型（LLM）重排序的高质量混合搜索（`qmd query`）。所有处理（索引、嵌入、重排序、查询扩展）均在设备端完成，无需联网或依赖外部 API。

2. **核心特性**  
- ✅ **三重混合检索架构**：同步调用 BM25（SQLite FTS5）、向量语义搜索（sqlite-vec + GGUF 嵌入模型）与 LLM 重排序（Qwen3-Reranker），并通过改进的**位置感知加权融合策略**（Position-Aware Blending）整合结果，兼顾精确匹配与语义理解；  
- ✅ **全自动本地化处理**：自动解析 Markdown 标题、生成文档唯一 ID（6 字符哈希）、按 800 token/15% 重叠切块、批量嵌入与缓存，全程离线；  
- ✅ **上下文增强检索**：支持为集合（`qmd://notes`）或路径添加自然语言描述（`qmd context add`），提升搜索相关性与结果可解释性；  
- ✅ **面向 AI 智能体的深度集成**：提供标准化 JSON/CSV/Markdown 等结构化输出格式，原生支持 MCP（Model Context Protocol）协议，可作为 Claude Desktop / Claude Code 的插件，暴露 `qmd_search`、`qmd_deep_search` 等 6 个标准化工具；  
- ✅ **灵活部署模式**：支持 CLI 直接调用、stdio 子进程 MCP、或长期驻留的 HTTP MCP 服务器（端口可配，支持守护进程），LLM 模型常驻 VRAM，冷启动开销仅限首次请求；  
- ✅ **细粒度控制与运维能力**：支持按集合过滤、最小分数阈值（`--min-score`）、多文件通配符获取（`qmd multi-get`）、行号定位、全文提取、索引健康检查（`qmd status`）及缓存清理（`qmd cleanup`）。

3. **技术栈**  
- **运行时**：Bun（v1+）作为 JavaScript 运行时与包管理器；  
- **本地 LLM 推理引擎**：`node-llama-cpp`（C++ 绑定），全量加载并执行 GGUF 格式量化模型；  
- **核心模型（自动下载）**：  
  - `embeddinggemma-300M-Q8_0`（~300MB）：用于生成文档/查询嵌入；  
  - `qwen3-reranker-0.6b-q8_0`（~640MB）：交叉编码器重排序模型；  
  - `qmd-query-expansion-1.7B-q4_k_m`（~1.1GB）：微调版 Qwen3，用于生成多样化查询变体；  
- **索引存储**：SQLite（含 FTS5 全文索引扩展 + `sqlite-vec` 向量扩展），数据持久化于 `~/.cache/qmd/index.sqlite`；  
- **协议与集成**：MCP（Model Context Protocol）标准，支持 stdio 与 HTTP（`/mcp` 流式 JSON + `/health` 健康检查）两种传输方式；  
- **系统依赖**：macOS 需 Homebrew 安装 `sqlite`（启用 FTS5 扩展支持）；Linux/Windows 兼容性未明确说明，但底层依赖均为跨平台组件。

</details>

---

### 28. [THUDM/slime](https://github.com/THUDM/slime)
- 📅 **创建日期**：2025-06-18  
- 🔄 **最近更新**：2026-02-13  
- ⭐ **Stars**：4,012（日 +100｜周 +320｜月 +697）  
- 📝 **描述**：slime is an LLM post-training framework for RL Scaling.  

<details>
<summary><b>📈 Star 与 Commit 历史趋势</b></summary>

![slime Star and Commit Trend](charts/THUDM_slime_trend.png)

> *蓝色：累计 Stars｜橙色：累计 Commits（次 Y 轴）*

</details>

<details>
<summary><b>📄 README 摘要</b></summary>

1. **项目功能**  
slime 是一个面向大语言模型（LLM）强化学习（RL）规模化后训练的开源框架，核心目标是支撑高效、灵活且可扩展的 RLHF（基于人类反馈的强化学习）与更广义的智能体式强化学习（Agentic RL）训练。它不直接提供预训练模型，而是作为底层训练基础设施，驱动如 GLM-4.7/4.6/4.5、Qwen3/Qwen2.5、DeepSeek V3/R1、Llama 3 等主流模型的 RL 后训练阶段，并已成功应用于多个前沿研究项目（如 P1 物理推理模型、RLVE 可验证环境训练、TritonForge 内核生成、APRIL 加速 rollout、qqr 开放式智能体进化等）。

2. **关键特性**  
- **高性能混合训练架构**：深度集成 Megatron-LM（负责高效分布式参数更新）与 SGLang（负责高吞吐、低延迟的 rollout 推理与数据生成），通过统一的 Data Buffer 实现训练与 rollout 的异步解耦；  
- **灵活的数据生成能力**：支持自定义数据生成接口与服务化 rollout 引擎（如 SGLang Router），允许用户自由构建任意复杂度的数据生成流程（如多轮编译反馈、可验证环境采样、竞技场对战排名、MCP 工具调用等）；  
- **模块化与可扩展设计**：采用清晰分层架构（training / rollout / data buffer），各模块职责明确、松耦合，便于插拔式扩展（如 APRIL、qqr 等均为 slime 上层轻量扩展）；  
- **生产就绪的工程支持**：原生兼容 Megatron 和 SGLang 全量参数配置（分别通过标准参数和 `--sglang-` 前缀参数透传），提供完整的快速启动指南、调试文档、pre-commit 代码规范及开发者协作流程。

3. **技术栈**  
- **核心训练引擎**：Megatron-LM（用于分布式模型并行训练与参数同步）；  
- **推理与 rollout 引擎**：SGLang（提供高性能 LLM 推理服务、批处理、PagedAttention 及自定义前端逻辑支持）；  
- **系统集成层**：自研 Data Buffer 模块（桥接训练与 rollout，管理 prompt 初始化、自定义数据注入与 rollout 策略调度）；  
- **辅助生态**：深度依赖并兼容 mbridge、OpenRLHF、veRL、Pai-Megatron-Patch 等社区项目；支持与 Triton、CUDA 工具链及 MCP（Model Context Protocol）等协议/框架协同工作；开发流程采用 pre-commit 进行代码风格管控。

</details>

---

### 29. [ThePrimeagen/99](https://github.com/ThePrimeagen/99)
- 📅 **创建日期**：2025-11-22  
- 🔄 **最近更新**：2026-02-13  
- ⭐ **Stars**：3,770（日 +44｜周 +373｜月 +2762）  
- 📝 **描述**：Neovim AI agent done right  

<details>
<summary><b>📈 Star 与 Commit 历史趋势</b></summary>

![99 Star and Commit Trend](charts/ThePrimeagen_99_trend.png)

> *蓝色：累计 Stars｜橙色：累计 Commits（次 Y 轴）*

</details>

<details>
<summary><b>📄 README 摘要</b></summary>

1. **该项目做什么？**  
该项目是一个专为 Neovim 设计的轻量级、面向开发者的 AI 编程助手客户端（代号 `99`），旨在为“无技能瓶颈”的资深开发者提供受控、高效、上下文精准的 AI 协作体验。它不追求通用问答，而是将 AI 请求严格限定在代码编辑场景中（如视觉选区处理、规则注入、文件引用等），通过结构化提示（`#规则`、`@文件`）自动注入项目上下文，避免手动粘贴冗余信息。核心目标是将 AI 深度融入 Neovim 编辑流，而非替代开发者思考或覆盖通用聊天场景（明确建议“一般问题请直接用 opencode”）。

2. **关键特性**  
- **结构化上下文注入**：支持 `#` 前缀自动补全自定义技能规则（`SKILL.md`），`@` 前缀模糊搜索并注入项目内文件内容，自动拼接到 AI 请求上下文中；  
- **多模式 AI 操作接口**：已实现 `visual()`（基于可视选区生成/修改代码）、`search()`（规划中）、`debug()`（规划中）等 API；  
- **多后端 AI 提供商支持**：原生兼容 `opencode`、`claude`、`cursor-agent` 三类 CLI 工具，可自由切换 provider 与模型；  
- **项目感知型提示工程**：自动沿目录树向上查找 `AGENT.md` 等配置文件，动态注入项目专属指令与约束；  
- **深度 Neovim 集成**：强依赖 `cmp` 补全引擎实现智能触发，提供日志查看（`view_logs`/`prev_request_logs`）、请求中断（`stop_all_requests`）等调试能力；  
- **Alpha 阶段务实设计**：明确限制语言支持（TS/Lua 优先）、默认禁用不稳定功能（如 cursor_rules）、强调日志脱敏与问题复现规范。

3. **技术栈**  
- **宿主环境**：Neovim（要求 ≥ 0.9，依赖 Lua 配置）；  
- **核心语言**：Lua（插件主体逻辑、API 封装、配置驱动）；  
- **前端补全**：`cmp`（唯一当前支持的补全源，用于 `#`/`@` 触发）；  
- **AI 后端协议**：通过调用外部 CLI 工具通信（`opencode` / `claude` / `cursor-agent`），不内置大模型或 HTTP 客户端；  
- **依赖工具链**：`treesitter`（规划中用于优化选区提取）、`vim.uv`（跨平台路径/IO）、`vim.fs`（文件系统操作）；  
- **调试与日志**：基于文件的异步日志系统（支持 DEBUG 级别、自定义路径）、内置日志导航 API。

</details>

---

### 30. [likec4/likec4](https://github.com/likec4/likec4)
- 📅 **创建日期**：2023-03-24  
- 🔄 **最近更新**：2026-02-13  
- ⭐ **Stars**：2,598（日 +15｜周 +931｜月 +1466）  
- 📝 **描述**：Visualize, collaborate, and evolve the software architecture with always actual and live diagrams from your code  

<details>
<summary><b>📈 Star 与 Commit 历史趋势</b></summary>

![likec4 Star and Commit Trend](charts/likec4_likec4_trend.png)

> *蓝色：累计 Stars｜橙色：累计 Commits（次 Y 轴）*

</details>

<details>
<summary><b>📄 README 摘要</b></summary>

1. **该项目做什么？**  
LikeC4 是一个将软件架构“代码化”（Architecture as Code）的开源工具，旨在通过声明式建模语言自动、实时地从源码级架构描述中生成**始终最新、可交互、可协作的可视化架构图**。它支持在开发流程中嵌入架构设计，使架构图与代码同步演进，消除文档与实现脱节的问题；同时提供在线协作、预览、部署和集成能力，适用于团队协同建模、技术文档自动化及架构治理场景。

2. **核心功能**  
- ✅ **声明式架构建模语言**：基于类 DSL 的简洁语法，支持自定义元素类型、关系语义、视觉样式及任意深度的嵌套层级（如 System → Container → Component → Code），不强制绑定 C4 四层模型，灵活适配不同抽象需求；  
- ✅ **实时可视化与热重载**：通过 CLI（`npx likec4 start`）本地启动开发服务器，编辑模型文件后图表即时更新，支持缩放、搜索、聚焦、展开/折叠等交互操作；  
- ✅ **全栈集成生态**：提供官方 VS Code 扩展（含语法高亮、智能提示、错误校验、一键预览），支持 StackBlitz 在线编辑，兼容 GitHub Pages / Vercel 等静态托管平台一键部署可访问的交互式架构视图；  
- ✅ **开箱即用的协作工作流**：提供模板仓库（`likec4/template`）、在线 Playground 和 Demo 示例，支持导出为 PNG/SVG，集成 Discord 社区与 GitHub Discussions 用于快速反馈与协作。

3. **技术栈**  
- **建模语言**：自研轻量级领域特定语言（DSL），受 C4 Model 和 Structurizr DSL 启发，但具备更高扩展性；  
- **前端渲染**：基于 Web 技术栈构建交互式图表界面（推测使用 TypeScript + React/Vite + D3.js 或类似图形库实现动态布局与渲染）；  
- **工具链**：Node.js CLI 工具（`likec4` npm 包），支持跨平台运行；VS Code 插件（TypeScript + VS Code Extension API）；  
- **基础设施**：GitHub Actions 自动化构建与发布，OpenCollective / GitHub Sponsors 支持开源可持续发展；  
- **协议与许可**：MIT 开源许可证，完全免费且允许商用。

</details>

---

### 31. [github/gh-aw](https://github.com/github/gh-aw)
- 📅 **创建日期**：2025-08-12  
- 🔄 **最近更新**：2026-02-13  
- ⭐ **Stars**：2,124（日 +183｜周 +1757｜月 +1827）  
- 📝 **描述**：GitHub Agentic Workflows  

<details>
<summary><b>📈 Star 与 Commit 历史趋势</b></summary>

![gh-aw Star and Commit Trend](charts/github_gh-aw_trend.png)

> *蓝色：累计 Stars｜橙色：累计 Commits（次 Y 轴）*

</details>

<details>
<summary><b>📄 README 摘要</b></summary>

1. **该项目的功能**  
GitHub Agentic Workflows 是一个将自然语言编写的“智能体式工作流”（agentic workflows）集成到 GitHub Actions 中的框架。它允许用户以 Markdown 格式用自然语言描述复杂、多步骤、具备决策与反馈能力的自动化任务（例如：分析 PR 变更、生成摘要、调用工具、条件分支、循环重试等），系统将其解析、验证并安全地在 GitHub Actions 环境中执行，实现 AI 驱动的仓库级自动化。

2. **核心特性**  
- **自然语言工作流定义**：支持以人类可读的 Markdown 描述带逻辑（如 if/else、循环、工具调用、状态追踪）的智能体行为；  
- **强安全默认机制**：所有工作流默认仅具**只读权限**，写操作必须通过显式声明、沙箱化处理的 `safe-outputs` 显式授权；  
- **多层防护体系**：包括执行环境沙箱化、输入内容自动净化、网络完全隔离（无外网访问）、依赖项 SHA256 强校验（供应链安全）、工具白名单管控、编译时静态验证；  
- **精细化访问控制**：支持按团队成员粒度授权，关键操作强制配置人工审批门禁（human approval gates）；  
- **配套安全基础设施**：深度集成 Agent Workflow Firewall（基于域名的网络出口管控与日志审计）和 MCP Gateway（统一代理 Model Context Protocol 调用，实现集中鉴权与治理）；  
- **生产就绪设计**：强调“人在环路”（human-in-the-loop）原则，明确警示需谨慎使用并保持人工监督。

3. **技术栈**  
- **运行平台**：原生构建于 **GitHub Actions** 之上，复用其基础设施与事件驱动模型；  
- **工作流语言**：基于扩展的 **Markdown**（非 YAML），支持自然语言指令与结构化元数据混合；  
- **安全核心组件**：  
  - 自研沙箱执行引擎（隐含，用于隔离运行时）；  
  - **Agent Workflow Firewall (AWF)**（Rust/Go 实现，独立服务，提供网络策略控制）；  
  - **MCP Gateway**（HTTP 网关，用于标准化、安全化大模型上下文协议交互）；  
- **依赖管理**：采用 **SHA-pinned 依赖**（确定性构建，防供应链投毒）；  
- **部署与分发**：通过 GitHub 官方扩展机制安装，文档与配置托管于 GitHub Pages（`github.github.com/gh-aw/`）。

</details>

---

### 32. [Jeffallan/claude-skills](https://github.com/Jeffallan/claude-skills)
- 📅 **创建日期**：2025-10-20  
- 🔄 **最近更新**：2026-02-13  
- ⭐ **Stars**：2,032（日 +608｜周 +1724｜月 +2004）  
- 📝 **描述**：66 Specialized Skills for Full-Stack Developers. Transform Claude Code into your expert pair programmer.  

<details>
<summary><b>📈 Star 与 Commit 历史趋势</b></summary>

![claude-skills Star and Commit Trend](charts/Jeffallan_claude-skills_trend.png)

> *蓝色：累计 Stars｜橙色：累计 Commits（次 Y 轴）*

</details>

<details>
<summary><b>📄 README 摘要</b></summary>

1. **项目功能**  
该项目是一个专为 Anthropic Claude Code（Claude 编程插件）设计的开源技能增强框架，旨在将 Claude 转变为面向全栈开发者的智能协作伙伴。它通过预置的、上下文感知的“技能”（Skills）和结构化“工作流”（Workflows），使 Claude 能够深度理解并精准响应复杂工程任务（如 JWT 认证实现、React 服务端组件开发、安全加固等），自动加载对应技术栈的权威参考文档，并在多阶段任务中串联多个专家角色（如架构师→全栈守护者→测试大师→DevOps 工程师），实现从需求分析到交付落地的端到端辅助。

2. **核心特性**  
- **66 项精细化技能**：覆盖 12 类技术领域（含编程语言、前后端框架、基础设施、API 设计、测试、DevOps、安全、数据/ML、平台专项等），每项技能附带专属知识库（`references/*.md`）；  
- **9 大端到端项目工作流**：支持史诗级任务管理（如特性开发、缺陷排查、安全加固），深度集成 Jira 和 Confluence，需配合 Atlassian MCP 服务器运行；  
- **上下文感知激活机制**：基于用户自然语言指令自动识别技术场景（如“在 NestJS 中实现 JWT” → 触发 NestJS 专家技能并加载认证文档）；  
- **多技能协同工作流**：支持跨角色链式调用（如 Bug 调查 = 调试向导 + 框架专家 + 测试大师 + 代码评审员）；  
- **上下文工程能力**：提供 `/common-ground` 命令显式揭示并校准 Claude 对项目隐含假设（如技术选型、架构约束），提升响应准确性；  
- **渐进式信息披露（Progressive Disclosure）**：按需分层呈现技术细节，避免信息过载，兼顾新手引导与专家深度需求。

3. **技术栈**  
- **运行环境**：Anthropic Claude Code 插件平台（Claude 的 IDE 内嵌 AI 编程助手）；  
- **后端集成依赖**：Atlassian MCP（Model Control Protocol）服务器（用于 Jira/Confluence 工作流）；  
- **知识组织**：纯 Markdown 技能文档（`skills/*/SKILL.md`）与引用文件（`skills/*/references/`），共 365+ 参考文件；  
- **工程实践**：GitHub Actions CI/CD、MIT 开源协议、模块化技能目录结构、本地技能开发支持（见 `docs/local_skill_development.md`）；  
- **生态集成**：被多个权威精选列表收录（如 `awesome-claude-code`、`awesome-claude-skills`），支持插件市场一键安装（`/plugin marketplace add`）。

</details>

---

### 33. [chenyme/grok2api](https://github.com/chenyme/grok2api)
- 📅 **创建日期**：2025-10-10  
- 🔄 **最近更新**：2026-02-13  
- ⭐ **Stars**：1,397（日 +42｜周 +321｜月 +760）  
- 📝 **描述**：基于 FastAPI 重构的 Grok2API，全面适配最新 Web 调用格式，支持流/非流式对话、图像生成/编辑、深度思考，号池并发与自动负载均衡一体化。  

<details>
<summary><b>📈 Star 与 Commit 历史趋势</b></summary>

![grok2api Star and Commit Trend](charts/chenyme_grok2api_trend.png)

> *蓝色：累计 Stars｜橙色：累计 Commits（次 Y 轴）*

</details>

---

### 34. [DebugSwift/DebugSwift](https://github.com/DebugSwift/DebugSwift)
- 📅 **创建日期**：2023-12-14  
- 🔄 **最近更新**：2026-02-13  
- ⭐ **Stars**：1,297（日 +82｜周 +265｜月 +314）  
- 📝 **描述**：A toolkit to make debugging iOS applications easier 🚀  

<details>
<summary><b>📈 Star 与 Commit 历史趋势</b></summary>

![DebugSwift Star and Commit Trend](charts/DebugSwift_DebugSwift_trend.png)

> *蓝色：累计 Stars｜橙色：累计 Commits（次 Y 轴）*

</details>

<details>
<summary><b>📄 README 摘要</b></summary>

1. **项目功能**  
DebugSwift 是一个专为 Swift iOS 应用设计的**集成式调试工具包**，旨在深度增强开发阶段的调试能力。它在应用运行时提供一个可交互的悬浮调试面板（支持 Shake 手势触发），无需依赖外部工具或打断开发流程，即可实时监控、分析和干预应用行为，覆盖网络请求、性能指标、UI 层级、资源状态及崩溃诊断等全链路调试场景。

2. **核心特性**  
- **网络调试（Network Inspector）**：全自动捕获 HTTP/HTTPS 请求与响应（含 JSON 格式化高亮）、WebSocket 帧级监控；支持 URL 过滤、请求限流、AES-256/128 自动解密及自定义解密器注册。  
- **性能分析（Performance）**：实时显示 CPU、内存占用、FPS；自动检测 ViewController/View 内存泄漏；主线程违规检测（Main Thread Checker）；支持性能数据叠加 Widget。  
- **应用工具（App Tools）**：崩溃报告（附截图+完整堆栈）、实时控制台日志过滤、设备与 App 元信息查看、APNs Token 一键复制、支持自定义调试操作与动态信息面板。  
- **界面调试（Interface Tools）**：可调参网格对齐层、3D 交互式视图层级检查器、触摸反馈指示器、动画减速控制、视图边界高亮；**Beta 版 SwiftUI 渲染追踪**（可视化重绘区域、计数、持续叠加、控制台日志）。  
- **资源管理（Resources）**：沙盒与 App Group 文件浏览器、UserDefaults 运行时编辑、Keychain 条目查看、SQLite/Realm 数据库浏览器、模板化推送通知模拟。

3. **技术栈**  
- **平台与语言**：iOS 14.0+，Swift 6.0+，Xcode 16.0+  
- **架构支持**：原生 Apple Silicon（arm64 模拟器）与 Intel（x86_64）双架构兼容，全面弃用 `EXCLUDED_ARCHS` 适配方案  
- **分发方式**：主推 Swift Package Manager（SPM），同时支持 CocoaPods（含标准源码版与预编译 XCFramework 版以加速构建）  
- **底层机制**：基于 URLSessionConfiguration 协议注入实现无侵入网络监控；利用 Swift 的 Runtime 特性与 UIKit/SwiftUI 深度集成（如 View Hierarchy 遍历、SwiftUI 视图生命周期钩子）；采用轻量级单例 + 模块化设计（`.network`, `.performance`, `.swiftUIRender` 等命名空间明确分离关注点）

</details>

---

### 35. [TelegramMessenger/MTProxy](https://github.com/TelegramMessenger/MTProxy)
- 📅 **创建日期**：2018-05-29  
- 🔄 **最近更新**：2026-02-13  
- ⭐ **Stars**：1,100（日 +54｜周 +181｜月 +238）  
- 📝 **描述**：暂无描述  

<details>
<summary><b>📈 Star 与 Commit 历史趋势</b></summary>

![MTProxy Star and Commit Trend](charts/TelegramMessenger_MTProxy_trend.png)

> *蓝色：累计 Stars｜橙色：累计 Commits（次 Y 轴）*

</details>

<details>
<summary><b>📄 README 摘要</b></summary>

1. **项目功能**  
该项目是 Telegram 官方维护的 **MTProto 代理服务器（MTProxy）**，用于中继客户端与 Telegram 服务器之间的加密通信。它实现 MTProto 协议的代理层，允许用户通过自建代理绕过网络审查或优化连接，同时支持 Telegram 官方的代理发现与标签（tag）机制，可注册至 @MTProxybot 并被 Telegram 客户端自动识别和分发流量。

2. **核心特性**  
- **轻量高效**：C 语言编写，资源占用低，支持多工作进程（`-M` 参数配置），适合高并发部署；  
- **动态配置支持**：需定期拉取 Telegram 官方发布的 `proxy-secret`（密钥）和 `proxy-multi.conf`（服务器配置），确保与 Telegram 后端兼容；  
- **多密钥与多租户支持**：可通过多个 `-S` 参数配置不同用户密钥，实现单实例服务多个代理链接；  
- **防检测增强**：支持**随机填充（Random Padding）模式**——客户端在密钥前添加 `dd` 前缀即可启用，使流量包长随机化，有效对抗基于固定包长特征的 ISP 流量识别与封锁；  
- **安全加固机制**：启动时自动 `setuid` 降权（如指定 `-u nobody`），限制运行权限；本地统计端口（如 `:8888/stats`）仅限 loopback 访问，防止信息泄露；  
- **完整运维支持**：提供 systemd 服务模板、Docker 官方镜像（尽管已过时）、详细启动/注册/更新流程及错误处理指引（如 `make clean` 重试）。

3. **技术栈**  
- **编程语言**：C（高性能、低依赖、适合系统级网络代理）；  
- **核心依赖库**：OpenSSL（TLS/加密运算）、zlib（数据压缩）；  
- **构建工具**：GNU Make、GCC（标准 C 工具链）；  
- **运行环境**：Linux 系统（明确适配 Debian/Ubuntu、CentOS/RHEL 等发行版）；  
- **部署扩展**：支持 systemd 服务管理、Docker 容器化（官方镜像 `telegrammessenger/proxy`）；  
- **协议与标准**：严格遵循 Telegram 自研的 MTProto 2.0 代理协议，兼容 Telegram 客户端的 `tg://proxy?...` 链接格式及 Bot 注册生态。

</details>

---

### 36. [SynkraAI/aios-core](https://github.com/SynkraAI/aios-core)
- 📅 **创建日期**：2025-12-09  
- 🔄 **最近更新**：2026-02-13  
- ⭐ **Stars**：317（日 +140｜周 +169｜月 +303）  
- 📝 **描述**：Synkra AIOS: AI-Orchestrated System for Full Stack Development - Core Framework v4.0  

<details>
<summary><b>📈 Star 与 Commit 历史趋势</b></summary>

![aios-core Star and Commit Trend](charts/SynkraAI_aios-core_trend.png)

> *蓝色：累计 Stars｜橙色：累计 Commits（次 Y 轴）*

</details>

<details>
<summary><b>📄 README 摘要</b></summary>

1. **该项目做什么？**  
Synkra AIOS 是一个面向全栈软件开发的**自修改型 AI 代理框架**，核心目标是实现真正意义上的**AI 驱动的敏捷开发（Agentic Agile）**。它不局限于任务执行或代码补全，而是构建了一套由专业化 AI 代理（Agents）协同工作的“虚拟敏捷团队”，覆盖从需求分析、架构设计、用户故事拆解、编码实现到质量保障的完整研发闭环。其独特价值在于：将人类开发者置于“指挥官”角色，由 AI 代理团队（如 @analyst、@architect、@sm、@dev、@qa 等）基于上下文自动协作生成高一致性、强可追溯性的交付物（PRD、架构文档、带完整上下文的故事文件、可运行代码），彻底解决传统 AI 编程中普遍存在的**规划不一致**与**上下文丢失**两大痛点。该框架亦支持扩展至非技术领域（如创意写作、商业策略、健康教育等），通过“Squads”（专业代理团队）适配任意垂直场景。

2. **关键特性**  
- **双阶段智能工作流**：① **代理式规划（Agentic Planning）**——分析师、产品经理、架构师等代理协同生成结构化、可验证的 PRD 与架构文档；② **上下文驱动开发（Contextualized Engineering）**——Scrum Master 代理将规划成果转化为含完整技术上下文、实现细节与架构约束的“故事文件”，供 Dev 代理精准执行。  
- **CLI 优先架构（CLI First）**：命令行界面是唯一真相源（Source of Truth），所有智能决策、执行与自动化均发生于 CLI 层；UI 仅作为只读可观测性视图（Dashboard、Kanban），绝不参与控制逻辑。  
- **自主开发引擎（ADE, Autonomous Development Engine）**：v1.0 引入包含 7 大核心能力的自治系统，涵盖 Git 工作树隔离、规格管道（Spec Pipeline）、13 步自检执行引擎、故障自动恢复、10 阶段结构化 QA 审查及持久化记忆层（Memory Layer）。  
- **现代化交互体验**：内置受 Vite/Next.js 启发的交互式安装向导（支持彩色提示、实时校验、多组件选择、包管理器切换、取消退出、安装耗时统计等）；CLI 支持 `--help` 全局帮助、跨平台兼容、彩色日志、dry-run 模拟及健康诊断（`aios-core doctor`）。  
- **开箱即用的专业代理集群**：预置 11 个角色明确的 AI 代理，分为元代理（orchestrator/master）、规划代理（analyst/pm/architect/ux-expert）和开发代理（sm/dev/qa/po），并支持通过 Squads 扩展至软件开发以外的领域。  
- **零配置 IDE 集成**：提供 Windsurf/Cursor/Claude Code 的预设规则文件（`.windsurf/`, `.cursor/`, `.claude/`），自动启用代理命令识别、故事驱动工作流、复选框追踪、测试规范与 AIOS 专属编码标准。

3. **技术栈**  
- **运行时**：Node.js ≥18.0.0（推荐 v20+）  
- **包管理**：npm（默认）、yarn、pnpm（安装时可选）  
- **核心依赖**：  
  - CLI 框架：`commander`（命令解析）  
  - 交互式终端 UI：`@clack/prompts`（现代化安装向导）  
  - 进程执行：`execa`（安全调用子进程）  
  - 文件系统：`fs-extra`（增强文件操作）  
  - 跨平台工具：`picocolors`（轻量级终端着色）  
- **基础设施**：Git（工作树管理、版本控制）、GitHub CLI（可选，用于团队协作）  
- **架构范式**：事件驱动（SSE 实时可观测性）、文件即接口（Stories 作为代理间通信载体）、分层抽象（CLI → Observability → UI）  
- **部署与分发**：以 NPM 包（`aios-core`）形式发布，支持 `npx` 一键启动，无须全局安装。

</details>

---

### 37. [google-deepmind/superhuman](https://github.com/google-deepmind/superhuman)
- 📅 **创建日期**：2025-10-29  
- 🔄 **最近更新**：2026-02-13  
- ⭐ **Stars**：288（日 +73｜周 +140｜月 +209）  
- 📝 **描述**：暂无描述  

<details>
<summary><b>📈 Star 与 Commit 历史趋势</b></summary>

![superhuman Star and Commit Trend](charts/google-deepmind_superhuman_trend.png)

> *蓝色：累计 Stars｜橙色：累计 Commits（次 Y 轴）*

</details>

<details>
<summary><b>📄 README 摘要</b></summary>

1. **该项目做什么？**  
该项目由Google DeepMind“超人级推理”（Superhuman Reasoning）团队（负责人Thang Luong）主导，聚焦于推动人工智能在**高阶数学推理与形式化证明能力**上的突破，目标是实现媲美甚至超越人类顶尖数学竞赛选手（如IMO金牌得主）及专业数学研究者的推理水平。其核心工作包括：构建具备奥林匹克级别解题能力的AI系统（AlphaGeometry系列）、开发面向前沿数学研究的自主推理代理（Aletheia），以及发布权威、细粒度、可复现的数学推理评测基准套件（IMO Bench）。

2. **关键特性**  
- **AlphaGeometry 与 AlphaGeometry2**：专攻几何定理自动证明的符号+神经混合系统；AlphaGeometry2在2024年国际数学奥林匹克（IMO）测试中达到银牌水平，代表当前几何推理SOTA。  
- **IMO Bench 评测套件**：包含三大互补子集——*IMO-AnswerBench*（400道高难度短答案题）、*IMO-ProofBench*（60道经数学专家审核的证明题）、*IMO-GradingBench*（1000条真实人工评分数据），全面覆盖答案正确性、推理严谨性与自动评估能力。  
- **Aletheia 数学研究代理**：基于Gemini Deep Think构建的闭环研究型AI，支持“生成→形式验证→迭代修正”的完整科研流程，并开源实际运行提示词与输出结果，推动可验证数学AI研究。  

3. **技术栈**  
- **模型基础**：深度依赖Google自研大模型，特别是具备强链式推理与思维深化能力的**Gemini Deep Think**（用于Aletheia）；AlphaGeometry系列融合**神经语言模型（NLM）与符号推理引擎（如几何定理证明器）**，采用神经引导的搜索与演绎验证架构。  
- **工具与方法**：强调**形式化验证**（如Coq或定制化证明检查器）、**程序合成**（将自然语言问题转化为可执行代码/证明脚本）、**多阶段提示工程与自我反思机制**（Aletheia的核心循环）。  
- **开源协议**：代码遵循**Apache License 2.0**，数据集与文档等非代码材料采用**Creative Commons Attribution 4.0 International (CC-BY)** 许可。

</details>

---

