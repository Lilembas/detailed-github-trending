# 🌟 GitHub Trending 概览

> 数据更新于：2026-05-18

---

## 🔍 项目详情

### 1. [Anil-matcha/Open-Generative-AI](https://github.com/Anil-matcha/Open-Generative-AI)
- 📅 **创建日期**：2023-05-09  
- 🔄 **最近更新**：2026-05-18  
- ⭐ **Stars**：13,168（日 +500｜周 +500｜月 +8121）  
- 📝 **描述**：Open-source alternative to AI video platforms — Free AI image & video generation studio with 200+ models (Flux, Midjourney, Kling, Sora, Veo). No content filters. Self-hosted, MIT licensed.  

<details>
<summary><b>📄 README 摘要</b></summary>

1. **该项目做什么？**  
Open Generative AI 是一个免费、开源的 AI 多媒体生成平台，旨在替代封闭式商业 AI 视频/图像服务（如 Runway、Pika、Sora 等）。它提供一体化的本地与云端混合工作流，支持**文本/图像生成图像（T2I/I2I）、文本/图像生成视频（T2V/I2V）、音频驱动唇形同步（Lip Sync）、电影级摄影控制（Cinema）及可视化多步自动化管线（Workflow）**。用户可在浏览器中直接使用托管版，或下载跨平台桌面应用（macOS/Windows/Linux），完全离线运行部分模型。核心定位是赋予创作者**无内容审查、无提示拦截、无订阅费用、无厂商锁定**的绝对创作自由，并支持自托管与深度定制。

2. **关键特性**  
- ✅ **四大专业工作室**：Image（50+ T2I + 55+ I2I 模型）、Video（40+ T2V + 60+ I2V 模型）、Lip Sync（9 个专用唇动模型，支持人像/视频双输入模式）、Cinema（镜头参数级影视化控制）；  
- ✅ **智能双模自动切换**：Image/Video Studio 根据是否上传参考图自动切换 T2I↔I2I 或 T2V↔I2V 模型集；  
- ✅ **突破性多图输入能力**：最高支持 **14 张参考图**（如 Nano Banana 2 Edit），用于高保真风格迁移与复杂编辑；  
- ✅ **双引擎本地推理支持**（仅桌面端）：  
　• `sd.cpp`（内置）：Metal/CUDA/Vulkan/ROCm 加速，支持 SD1.5/SDXL/Z-Image 等图像模型；  
　• `Wan2GP`（BYO 服务器）：通过 HTTP 调用用户自建的 PyTorch GPU 服务，支持 Flux、Qwen-Image、Wan 2.2、Hunyuan、LTX 等前沿视频与大图模型；  
- ✅ **全流程自动化工作流（Workflow Studio）**：节点式可视化编排，支持图像→视频→音频→剪辑等跨模态链式生成，含社区模板与个人工作流管理；  
- ✅ **持久化资产系统**：上传历史（本地存储可复用）、生成历史（浏览器内持久化）、一键高清下载、API 密钥安全本地管理；  
- ✅ **开发者友好扩展性**：开放源码、可添加自定义模型、修改 UI、集成至自动化媒体管道（如配合 [Generative-Media-Skills](https://github.com/SamurAIGPT/Generative-Media-Skills) 实现 CLI 端 AI 编程代理驱动）；  
- ✅ **硬件自适应智能控制**：动态分辨率/画幅/时长/质量滑块，按模型能力实时启用或禁用；响应式玻璃拟态（glassmorphism）UI，适配桌面与移动端。

3. **技术栈**  
- **前端框架**：Electron（桌面端跨平台封装）、React（主界面交互）、TypeScript（类型安全开发）；  
- **后端/服务层**：托管版依赖云 API（[Muapi.ai](https://muapi.ai) 提供统一模型网关）；本地推理则通过 Electron 内置二进制（`sd-cli`）或 HTTP 客户端（对接 Wan2GP Gradio 服务）实现；  
- **本地推理引擎**：  
　• `sd.cpp`（C++ 实现，基于 [leejet/stable-diffusion.cpp](https://github.com/leejet/stable-diffusion.cpp)），支持 Metal（Apple Silicon）、CUDA/Vulkan/ROCm（Windows/Linux）；  
　• `Wan2GP`（Python + PyTorch），需用户自行部署，依赖 flash-attn、sageattention、AWQ/GGUF 等 CUDA 优化内核；  
- **模型生态**：集成超 **200 种 SOTA 模型**，涵盖 Flux、Kling、Sora、Veo、Wan 2.2、Hunyuan、LTX、Seedream、Nano Banana、Grok Imagine、MiniMax、Qwen-Image、Infinite Talk 等，覆盖图像、视频、唇动、编辑、超分全场景；  
- **构建与分发**：Electron Builder（打包 macOS `.dmg`、Windows `.exe`、Linux `.AppImage`/`.deb`），Hugging Face 作为部分模型权重源，GitHub Releases 托管全部二进制发布。

</details>

---

### 2. [ComposioHQ/awesome-codex-skills](https://github.com/ComposioHQ/awesome-codex-skills)
- 📅 **创建日期**：2026-01-12  
- 🔄 **最近更新**：2026-05-18  
- ⭐ **Stars**：10,298（日 +215｜周 +2297｜月 +9538）  
- 📝 **描述**：A curated list of practical Codex skills for automating workflows across the Codex CLI and API.  

<details>
<summary><b>📄 README 摘要</b></summary>

1. **该项目的作用**  
该项目是一个面向 Codex（Composio 推出的智能代理 CLI 工具）的**精选技能（Skills）集合库**，旨在扩展 Codex 的自动化能力，使其不仅能生成文本，还能执行真实世界操作——如发送邮件、创建 GitHub Issue、发布 Slack 消息、连接并操作 1000+ 第三方应用（Notion、Linear、Datadog、Stripe 等）。它不提供独立运行的软件，而是通过模块化、可插拔的“技能包”增强 Codex 的任务执行能力，覆盖开发、协作、通信、数据分析及元工具等全场景工作流。

2. **核心功能**  
- ✅ **开箱即用的实用技能库**：按领域分类（开发/生产力/写作/数据/元工具），包含超 50 个已验证技能，如 `meeting-notes-and-actions`（会议纪要与待办自动生成）、`spreadsheet-formula-helper`（公式编写与调试）、`sentry-triage`（Sentry 错误源码级诊断）、`pr-review-ci-fix`（PR 自动评审+CI 失败自动修复闭环）。  
- ✅ **多模态集成能力**：通过 Composio CLI 深度对接外部服务（Slack、GitHub、Notion、Jira、Datadog、LangSmith 等），实现跨应用动作编排；支持 MCP（Model Communication Protocol）标准，兼容 Claude Code、Cursor、VS Code 等多平台。  
- ✅ **灵活安装与触发机制**：支持命令行一键安装（`skill-installer` 脚本）或手动复制；技能通过 `SKILL.md` 中的 `description` 元数据被 Codex 自动匹配触发，支持自然语言调用或显式技能名引用；支持渐进式披露（progressive disclosure），仅在需要时加载长文档或脚本，保持上下文精简。  
- ✅ **开发者友好生态**：提供 `template-skill` 和 `skill-creator` 指南，标准化技能结构（含 `scripts/`、`references/`、`assets/`）；鼓励社区贡献，强调描述精准性、可复现性与上下文效率。

3. **技术栈**  
- **核心运行时**：依赖 [Codex CLI](https://composio.dev)（基于 Composio 构建的本地智能代理终端工具）作为执行引擎；所有技能以纯文本 Markdown（`SKILL.md`）为核心指令载体。  
- **集成协议**：深度采用 **MCP（Model Communication Protocol）** 标准，实现模型与工具间的结构化通信；通过 **Composio CLI** 统一桥接 1000+ 应用 API（OAuth、Webhook、CLI 插件等）。  
- **部署与运行环境**：纯本地化设计（如 `paperjsx` 本地生成 PPTX/DOCX/XLSX，`unslop` 本地去除 AI 痕迹），无需外部 API Key 或网络请求；技能脚本主要使用 **Python**（安装器、CLI 工具）和 **Shell/Bash**（Git、gh、curl 等系统交互）；部分技能集成前端技术栈（如 Emdash Skills 使用 Hono + Angular + Cloudflare Workers）。  
- **辅助工具链**：内置 `skill-installer`（Python）、`skill-creator`（指南）、`template-skill`（标准化骨架）；支持 Git 工作树隔离（Bernstein、Polywave）、CI 验证（`codebase-migrate`）、结构化日志（`raffle-winner-picker`）等工程化实践。

</details>

---

