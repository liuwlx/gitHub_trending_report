# GitHub Trending 日报内容底稿

## Meta

- Report Date: 2026-07-30
- Generated At: 2026-07-30 21:03:00 JST
- Output Markdown: `md/github_trending_report_2026-07-30.md`
- Planned HTML: `html/github_trending_report_2026-07-30.html`
- Fixed Base Template: `.codex/skills/skill-github-trending-report/reference/fixedBaseTemplate_2026-03-16.html`
- User Rules: `.codex/skills/skill-github-trending-report/reference/user-rules.md`
- Sources:
  - GitHub Trending：Repositories / Any language / Today，当日抓取快照
  - GitHub Explore：当日公开页面，仅作补充，不参与排名
  - 项目 README、许可证、依赖清单、官方文档与公开源码

## Page Intent

- 今日主线：AI 项目继续从“单个模型”向可运行的语音管线、编码代理、桌面工作台和角色交互系统扩张；同时，GIS、IT 资产管理和数据采集等传统软件仍有稳定吸引力。
- 适合谁阅读：希望快速判断项目价值、技术边界、部署成本和源码阅读优先级的开发者、架构师与技术负责人。
- 页面重点：严格保留 GitHub 原始 Top 12 排名；累计 Stars、Forks 与 Stars Today 分栏呈现；所有性能、生产规模和效果数字均标明为项目方公开主张。
- 需要诚实降级说明的地方：Explore 与 Trending 高度重合；动态榜单会继续变化；本报告未独立复测性能、安全性、模型质量或平台兼容性。

## Stats

- Trending 项目数：12
- 今日累计新增 Stars：5,301
- 编程语言数：7
- AI 相关项目数：9（编辑分类，不是 GitHub 官方标签）

## Editorial Insights

### Insight 1
- Title: Agent 工程开始抢过模型的麦克风
- Body: ECC、jcode、OpenWork 与 Superpowers 都在解决“如何让代理稳定做事”，重点从一次回答转向计划、执行、测试、权限、会话恢复和可复用能力。热度不只追模型大小，也追工程闭环。

### Insight 2
- Title: 语音 AI 正在拆成可替换的流水线
- Body: speech-to-speech 明确采用 VAD → STT → LLM → TTS 的模块化线程与队列，VibeVoice覆盖 ASR、实时 TTS 和长音频模型，AIRI再把语音输入接到虚拟角色交互。三者分别站在管线、模型和产品层。

### Insight 3
- Title: 老牌业务软件照样能回到前排
- Body: Snipe-IT、faceswap 与 MediaCrawler 都不是刚搭的演示壳。它们分别具备成熟业务流程、完整训练转换链路或多平台采集架构，说明 Trending 并不只奖励新概念，也会把长期维护的系统重新推到台前。

### Insight 4
- Title: License 和运行门槛比宣传语更值得先看
- Body: OpenWork存在 MIT 与 `/ee` Fair Source 的混合边界，MediaCrawler明确限制非商业学习用途，FlashKDA要求 SM90+ 与 CUDA 12.9+，VibeVoice也明确不建议未经进一步测试直接用于商业或现实场景。先看边界，再谈落地，省得项目跑起来了，法务和显卡一起冒烟。

## Top Projects

### Rank 01 - opengeos/GeoLibre
- Repo URL: https://github.com/opengeos/GeoLibre
- Tagline: 可在浏览器、桌面、移动端和 Jupyter 运行的轻量云原生 GIS。
- Stars: 4,266
- Stars Today: 671
- Forks: 444
- Language: TypeScript
- License: MIT
- Homepage: https://geolibre.app/
- Topics: geospatial, duckdb, tauri, maplibre, data-science
- 技术栈: Tauri v2、React、TypeScript、MapLibre GL JS、DuckDB-WASM Spatial、deck.gl
- Why It Matters Today: 以本地优先和跨端统一工作区，把 GIS 浏览、分析与分享压进更轻的交付形态。
- 项目摘要: GeoLibre 将地图渲染、空间 SQL、矢量分析、3D 图层和项目分享整合在同一工作区，核心卖点是数据尽量留在用户设备上，并覆盖 Web、桌面、Android 与 Notebook。
- 核心特性:
  1. 浏览器内通过 DuckDB-WASM Spatial 执行空间查询和分析。
  2. 同一代码工作区适配 Web、Tauri 桌面、Android 和 Jupyter。
  3. 支持 MapLibre、deck.gl、插件 API、项目格式和分享服务。
- 适用场景: 轻量 GIS 工作台、教育演示、离线或隐私敏感的空间分析、跨端地图应用原型。
- 一句话推荐: 想把传统桌面 GIS 的一部分能力搬进浏览器，又不愿先搭一整套后端，可以先看它。
- Evidence Notes: README 明确列出跨端形态、核心技术栈、架构文档、插件 API 与 MIT 许可证。
- Honest Caveat: 浏览器内大规模空间数据性能、移动端资源占用和复杂桌面 GIS 的功能等价性未独立验证。

### Rank 02 - moeru-ai/airi
- Repo URL: https://github.com/moeru-ai/airi
- Tagline: 自托管、用户拥有的实时 AI 虚拟角色与数字伴侣平台。
- Stars: 45,578
- Stars Today: 682
- Forks: 4,501
- Language: TypeScript
- License: MIT
- Homepage: https://airi.moeru.ai/
- Topics: ai-companion, live2d, vrm, vtuber, realtime-voice
- 技术栈: TypeScript、Vue/Pinia、pnpm monorepo、Turbo、Web/Electron/移动端应用、可插拔转写提供方
- Why It Matters Today: 它不止做聊天框，而是把语音输入、角色表现、跨端运行和游戏交互放进一个长期运行的数字角色容器。
- 项目摘要: AIRI 由多个 apps、packages、services 和 engines 组成，提供 Web、桌面与移动形态，并围绕 Hearing、Provider、Stage UI、角色渲染和服务运行时组织能力。
- 核心特性:
  1. 支持实时语音输入、转写提供方选择、自动发送和角色交互。
  2. Monorepo 同时维护 Stage Web、桌面 Tamagotchi、Pocket 移动端和服务端运行时。
  3. 面向 Live2D/VRM、游戏互动、记忆与 RAG 等扩展方向。
- 适用场景: 自托管数字伴侣、AI VTuber、语音角色应用、游戏辅助角色实验。
- 一句话推荐: 想研究“AI 角色如何从一个回答器变成持续在线的应用系统”，AIRI 的工程面比宣传图更值得看。
- Evidence Notes: 根 package.json 明确列出各端应用、测试和构建任务；Hearing store 与 use-transcriptions 展示了提供方选择、麦克风权限、流式转写、自动发送和错误分支。
- Honest Caveat: README 中的游戏能力、角色体验和性能属于项目方能力描述；完整 LLM 回复到 TTS/动作驱动链路未在本次逐函数跑通。

### Rank 03 - affaan-m/ECC
- Repo URL: https://github.com/affaan-m/ECC
- Tagline: 为多种编码代理提供计划、测试、评审、记忆与安全能力的工程系统。
- Stars: 235,802
- Stars Today: 857
- Forks: 35,893
- Language: JavaScript
- License: MIT
- Homepage: https://ecc.tools/
- Topics: coding-agents, skills, memory, security, developer-workflow
- 技术栈: Shell、TypeScript、Python、Go、Java、Perl、Markdown、插件与 Hook
- Why It Matters Today: 今日新增 Stars 最高，说明开发者对“代理工作流治理”和跨工具复用的需求仍在放大。
- 项目摘要: ECC 将 agents、skills、commands、hooks、rules、memory 和 AgentShield 组合为可安装的代理工程环境，覆盖 Claude Code、Codex、Cursor、OpenCode 等多种 harness。
- 核心特性:
  1. 以 plan → test → implement → review → verify → remember → improve 组织开发循环。
  2. 提供规划、架构、安全、构建修复和领域任务的 agents 与 skills。
  3. 支持多种编码代理的插件、同步和规则安装路径。
- 适用场景: 团队统一编码代理工作流、个人代理能力库、代码代理安全扫描和持续学习实验。
- 一句话推荐: 需要的不是“再写一条神奇提示词”，而是一套能约束代理干活方式的工具箱时，可以研究 ECC。
- Evidence Notes: README 给出公开组件数量、安装路径、支持范围和 MIT 许可；数量和效果均按项目方口径记录。
- Honest Caveat: 代理、skills 和命令数量以及效率收益未独立盘点；部分能力更接近流程资产和配置生态，而非单一运行时系统。

### Rank 04 - huggingface/speech-to-speech
- Repo URL: https://github.com/huggingface/speech-to-speech
- Tagline: 通过开放模型构建低延迟模块化语音代理。
- Stars: 8,070
- Stars Today: 827
- Forks: 1,020
- Language: Python
- License: Apache-2.0
- Homepage: https://github.com/huggingface/speech-to-speech
- Topics: voice-agent, vad, stt, llm, tts, websocket
- 技术栈: Python、线程与队列、Silero VAD、可替换 STT/LLM/TTS、OpenAI Realtime WebSocket
- Why It Matters Today: 它把语音代理的关键阶段拆成清晰接口，并兼容本地模型、托管提供商和标准客户端。
- 项目摘要: 项目采用 VAD → STT → LLM → TTS 的级联管线，各阶段独立在线程中运行并通过队列连接，默认暴露 OpenAI Realtime 兼容 WebSocket API。
- 核心特性:
  1. VAD、STT、LLM、TTS 后端均可替换。
  2. 支持 realtime、local 和原始 PCM WebSocket 三种运行模式。
  3. LLM 可指向 OpenAI 兼容服务、Hugging Face Providers、vLLM 或 llama.cpp。
- 适用场景: 机器人语音后端、客服语音代理、全本地语音助手、Realtime API 兼容服务。
- 一句话推荐: 需要一条能换零件的语音流水线，而不是把模型绑死在一锅里，这个仓库很合适。
- Evidence Notes: README 明确描述线程、队列、协议、默认组件、运行模式及依赖冲突说明。
- Honest Caveat: “用于数千台 Reachy Mini”是项目方生产声明；端到端延迟受模型、硬件、网络和音频设备共同影响。

### Rank 05 - 1jehuang/jcode
- Repo URL: https://github.com/1jehuang/jcode
- Tagline: 以低内存和多会话效率为卖点的 Rust 编码代理 harness。
- Stars: 13,652
- Stars Today: 640
- Forks: 1,498
- Language: Rust
- License: MIT
- Homepage: https://jcode.sh/
- Topics: coding-agent, cli, rust, agent-harness
- 技术栈: Rust、跨平台 CLI、代理会话、可选本地嵌入
- Why It Matters Today: 在代理工具越来越重的背景下，jcode 把资源占用本身当作产品指标。
- 项目摘要: jcode 面向 Linux、macOS 和 Windows，强调快速启动、低内存与多会话工作流，并提供文档、基准和安装脚本。
- 核心特性:
  1. Rust 实现的跨平台代理 harness。
  2. 面向多会话运行优化内存与启动开销。
  3. 提供本地嵌入开关、安装器和公开基准页面。
- 适用场景: 资源敏感的编码代理终端、多并发本地会话、希望研究 Rust Agent Runtime 的开发者。
- 一句话推荐: 代理开十个窗口，电脑先替你辞职时，可以看看它怎么压资源。
- Evidence Notes: README 给出安装方式、平台、资源对比和 MIT 许可。
- Honest Caveat: 内存排名和“最智能”属于项目自述；基准环境、版本和公平性需要单独复核。

### Rank 06 - grokability/snipe-it
- Repo URL: https://github.com/grokability/snipe-it
- Tagline: 面向 IT 运维的开源资产、许可证和领用管理系统。
- Stars: 14,548
- Stars Today: 164
- Forks: 3,906
- Language: PHP
- License: AGPL-3.0-or-later
- Homepage: https://snipeitapp.com/
- Topics: asset-management, inventory, it-operations, laravel
- 技术栈: PHP 8.2、Laravel 12、Eloquent、Passport、Livewire、REST API、Docker
- Why It Matters Today: 它代表的是明确、刚需、可审计的业务系统：谁领了哪台设备、何时归还、许可证如何分配。
- 项目摘要: Snipe-IT 是成熟的 Web 资产管理系统，覆盖硬件、软件许可证、配件、耗材、用户、位置、签收与通知等业务对象。
- 核心特性:
  1. 资产领用、归还、审计、折旧与状态管理。
  2. JSON REST API、OAuth/Passport、SCIM 与多种通知集成。
  3. Web 部署、Docker 镜像、数据库迁移和完整 PHPUnit 测试体系。
- 适用场景: 企业 IT 资产台账、设备领用审计、许可证席位管理、学校或组织设备管理。
- 一句话推荐: 不想再用一张“设备去哪儿了.xlsx”撑起整个 IT 运维，可以从它开始。
- Evidence Notes: README、composer.json、硬件路由、AssetCheckoutController 和 AssetCheckoutRequest 可验证领用主链路与 AGPL 许可。
- Honest Caveat: 生产部署需要数据库、邮件、身份权限与备份策略；AGPL 网络交互义务应由团队自行评估。

### Rank 07 - deepfakes/faceswap
- Repo URL: https://github.com/deepfakes/faceswap
- Tagline: 面向图片和视频的人脸提取、训练与转换工具。
- Stars: 56,508
- Stars Today: 166
- Forks: 13,445
- Language: Python
- License: GPL-3.0
- Homepage: https://faceswap.dev/
- Topics: deep-learning, face-swap, computer-vision, gpu
- 技术栈: Python、深度学习、OpenCV、CUDA/ROCm、GUI、FFmpeg 工具链
- Why It Matters Today: 它是较成熟的深度伪造工具链，也持续提醒技术能力和使用伦理不能分家。
- 项目摘要: FaceSwap 以 Extract → Train → Convert 为主流程，同时提供 GUI、视频转换辅助工具和跨平台安装说明。
- 核心特性:
  1. 从图片或视频中检测、对齐并提取人脸。
  2. 训练换脸模型并将结果转换回图片或视频。
  3. 支持 GUI、CUDA 和部分 AMD ROCm 环境。
- 适用场景: 经授权的影视特效、计算机视觉研究、教育实验和合成媒体检测对照。
- 一句话推荐: 只适合在明确授权和合规边界内研究，技术门槛能降，责任门槛不能降。
- Evidence Notes: README 明确给出三阶段流程、GPU 需求和伦理声明；LICENSE 为 GPL v3。
- Honest Caveat: 存在冒用、欺诈、隐私和肖像权风险；不得把“能运行”理解为“可以随便用”。

### Rank 08 - microsoft/VibeVoice
- Repo URL: https://github.com/microsoft/VibeVoice
- Tagline: 微软开源的 ASR、长音频与实时 TTS 语音模型家族。
- Stars: 51,476
- Stars Today: 336
- Forks: 5,721
- Language: Python
- License: MIT（代码；模型权重需分别核对模型卡）
- Homepage: https://microsoft.github.io/VibeVoice
- Topics: speech-recognition, text-to-speech, streaming, voice-ai
- 技术栈: Python、Transformers、vLLM、连续语音 tokenizer、扩散生成、Hugging Face 模型
- Why It Matters Today: 项目把长音频识别、说话人/时间戳结构化输出和实时语音合成放在同一系列中。
- 项目摘要: VibeVoice 包含长音频 ASR、实时 TTS 与相关研究实现，强调低帧率连续语音 tokenizer 和长上下文处理。
- 核心特性:
  1. ASR 面向长音频并输出 Who、When、What 结构。
  2. 实时 TTS 支持流式文本输入和长段语音生成。
  3. 提供 Hugging Face 权重、Colab、vLLM 推理与微调材料。
- 适用场景: 会议转写、长音频结构化、语音研究、实时合成原型。
- 一句话推荐: 做长音频和实时语音研究值得跟，但上线前别把 README 当验收报告。
- Evidence Notes: README 给出模型范围、论文、权重、推理方式、风险限制；代码许可证为 MIT。
- Honest Caveat: 项目曾因不当使用移除部分 TTS 代码，并明确不建议未经进一步测试直接用于商业或真实应用；模型权重条款需单独核验。

### Rank 09 - different-ai/openwork
- Repo URL: https://github.com/different-ai/openwork
- Tagline: 基于 OpenCode 的开源 AI 工作桌面与团队能力分发平台。
- Stars: 18,174
- Stars Today: 97
- Forks: 1,865
- Language: TypeScript
- License: 核心代码 MIT；`/ee` 为 Fair Source
- Homepage: https://openworklabs.com/
- Topics: desktop-agent, opencode, mcp, workflow, electron
- 技术栈: TypeScript、React 19、Vite、Electron、OpenCode SDK、MCP、TanStack Query、Zustand、可选 Den 服务
- Why It Matters Today: 它将聊天会话、工作区、文件工具、能力分发和团队控制面放进同一产品，而不是只提供一个命令行壳。
- 项目摘要: OpenWork 的 UI 同时服务 Electron 和 Web，通过 HTTP 连接 openwork-server、OpenCode 与 Den；核心层、Kernel、Shell 和领域模块有明确依赖规则。
- 核心特性:
  1. 桌面工作区和 Web UI 共用 React/Vite 应用。
  2. 使用 OpenCode SDK 处理代理会话、工具结果、事件和错误恢复。
  3. 通过 MCP 暴露 `search_capabilities` 与 `execute_capability`，并提供组织级能力管理。
- 适用场景: AI 桌面工作台、团队技能与 MCP 分发、多工作区编码/办公代理、企业控制面实验。
- 一句话推荐: 想研究“代理桌面产品”如何从聊天框长出工作区、控制面和恢复机制，OpenWork 很有代表性。
- Evidence Notes: README、根与 app package.json、React Architecture 文档、usechat-adapter 和 Docker/测试脚本提供公开证据。
- Honest Caveat: `/ee` 不是 MIT；部分云、组织和托管能力依赖 OpenWork Den 或官方服务，不能把整个仓库简单归为纯本地单体应用。

### Rank 10 - obra/superpowers
- Repo URL: https://github.com/obra/superpowers
- Tagline: 为编码代理提供可组合技能和强制软件开发方法论。
- Stars: 263,525
- Stars Today: 616
- Forks: 23,530
- Language: Shell
- License: MIT
- Homepage: https://github.com/obra/superpowers
- Topics: agent-skills, tdd, worktrees, code-review, sdlc
- 技术栈: Shell、Markdown skills、插件适配、Git worktree、测试与评审流程
- Why It Matters Today: 高热度说明开发者希望代理遵循可检查的工程流程，而不是一路“凭感觉生成”。
- 项目摘要: Superpowers 用 brainstorming、worktrees、writing-plans、TDD、subagent development、code review 和 branch finishing 组成强制工作流。
- 核心特性:
  1. 多种编码代理和插件市场的安装适配。
  2. 设计确认、细粒度计划、红绿重构和双阶段评审。
  3. 通过 skills 在任务开始前自动触发对应方法。
- 适用场景: 编码代理流程规范、TDD 教学、个人或团队 Agent SDLC 模板。
- 一句话推荐: 它更像给代理请了个严厉项目经理，不一定写代码，但会盯着流程别跑偏。
- Evidence Notes: README 给出完整基本工作流、安装方式和 MIT 许可证。
- Honest Caveat: 仓库主要价值在方法、skills 和适配层，不是具备复杂运行时架构的独立业务系统。

### Rank 11 - MoonshotAI/FlashKDA
- Repo URL: https://github.com/MoonshotAI/FlashKDA
- Tagline: 基于 CUTLASS 的高性能 Kimi Delta Attention CUDA Kernel。
- Stars: 1,054
- Stars Today: 91
- Forks: 101
- Language: Cuda
- License: MIT
- Homepage: https://github.com/MoonshotAI/FlashKDA
- Topics: cuda, cutlass, attention, pytorch, kernel
- 技术栈: CUDA/C++、CUTLASS、PyTorch、flash-linear-attention、Python 扩展
- Why It Matters Today: 它把注意力优化落到明确的 Kernel API、调度条件、状态布局和正确性测试，而非只发布论文描述。
- 项目摘要: FlashKDA 提供 KDA 前向 Kernel，可被 flash-linear-attention 的 `chunk_kda` 自动调度，支持状态输入输出和变长序列。
- 核心特性:
  1. 面向 SM90+ 的 CUTLASS Kernel 实现。
  2. 与 flash-linear-attention 自动调度并支持回退 Triton 路径。
  3. 提供 Torch 参考实现精确匹配测试与公开基准文档。
- 适用场景: KDA 模型推理优化、CUDA Kernel 研究、Hopper/Blackwell 平台性能实验。
- 一句话推荐: 有合适显卡和 Kernel 胃口再进，普通笔记本看一眼需求就可以礼貌告辞。
- Evidence Notes: README 明确列出 SM90、CUDA 12.9、PyTorch 2.4、Kernel API、测试与调度方式；LICENSE 为 MIT。
- Honest Caveat: 硬件门槛高，当前 K/V 维度有固定限制；性能数据未在独立环境复测。

### Rank 12 - NanmiCoder/MediaCrawler
- Repo URL: https://github.com/NanmiCoder/MediaCrawler
- Tagline: 基于浏览器登录态的多平台公开内容与评论采集工具。
- Stars: 59,274
- Stars Today: 154
- Forks: 11,695
- Language: Python
- License: Non-Commercial Learning License 1.1
- Homepage: https://github.com/NanmiCoder/MediaCrawler
- Topics: crawler, playwright, xiaohongshu, douyin, bilibili, webui
- 技术栈: Python、Playwright/CDP、FastAPI、Vite WebUI、Node.js、平台适配器
- Why It Matters Today: 它把多平台登录态、搜索、详情、评论、代理和可视化操作统一到一套工程里。
- 项目摘要: MediaCrawler 支持小红书、抖音、快手、B 站、微博、贴吧和知乎等平台，通过 Playwright 或 CDP 复用浏览器登录状态并采集公开信息。
- 核心特性:
  1. 多平台关键词、详情、创作者和多级评论采集。
  2. 默认 CDP 连接已有 Chrome，也可切换标准 Playwright。
  3. 提供 FastAPI 后端和 Vite WebUI，用于配置、日志、预览与导出。
- 适用场景: 非商业学习、爬虫架构研究、经授权的小规模公开数据采集实验。
- 一句话推荐: 架构能学，数据不能乱拿；先读许可证和平台规则，再敲运行命令。
- Evidence Notes: README、运行命令、WebUI 说明和 LICENSE 明确了技术路径及非商业限制。
- Honest Caveat: 仅限非商业学习与研究，不得大规模抓取或影响平台运行；登录、验证码、平台协议、隐私和当地法律均需自行合规。

## Language Distribution

- Python:
  - Count: 4
  - Percent: 33.3%
  - Color Hint: #3572A5
- TypeScript:
  - Count: 3
  - Percent: 25.0%
  - Color Hint: #3178C6
- JavaScript:
  - Count: 1
  - Percent: 8.3%
  - Color Hint: #F1E05A
- Rust:
  - Count: 1
  - Percent: 8.3%
  - Color Hint: #DEA584
- PHP:
  - Count: 1
  - Percent: 8.3%
  - Color Hint: #4F5D95
- Shell:
  - Count: 1
  - Percent: 8.3%
  - Color Hint: #89E051
- Cuda:
  - Count: 1
  - Percent: 8.3%
  - Color Hint: #3A4E3A

## Explore Highlights

### Explore 1
- Title: GeoLibre
- URL: https://github.com/opengeos/GeoLibre
- Kind: Trending repository
- Meta: Updated Jul 30, 2026 · TypeScript
- Short Reason: GitHub Explore 首屏推荐，跨端本地优先 GIS 代表。

### Explore 2
- Title: AIRI
- URL: https://github.com/moeru-ai/airi
- Kind: Trending repository
- Meta: Updated Jul 30, 2026 · TypeScript
- Short Reason: 自托管实时 AI 角色项目，与今日 Agent/语音主线一致。

### Explore 3
- Title: ECC
- URL: https://github.com/affaan-m/ECC
- Kind: Trending repository
- Meta: Agent harness ecosystem
- Short Reason: 今日 Stars Today 最高，展示代理工程治理的强需求。

### Explore 4
- Title: speech-to-speech
- URL: https://github.com/huggingface/speech-to-speech
- Kind: Trending repository
- Meta: Python · OpenAI Realtime-compatible
- Short Reason: 模块化语音代理管线，适合与模型型项目区分阅读。

### Explore 5
- Title: Pixel Art Tools
- URL: https://github.com/collections/pixel-art-tools
- Kind: GitHub Collection
- Meta: 17 items
- Short Reason: Explore 中少数不与 Trending 重合的编辑精选，补充创意工具视角。

### Explore 6
- Title: Notebook Reviews Done Right
- URL: https://gitnotebooks.com/
- Kind: GitHub Staff Recommendation
- Meta: Notebook review workflow
- Short Reason: GitHub Staff 推荐的 Notebook 评审工具，补充代码审查之外的数据科学协作场景。

## Rendering Notes

- Hero 主标题建议：GitHub 热榜日报 · 2026-07-30
- Hero 副标题建议：今天的热度从 Agent 工程、语音流水线一路铺到 GIS 与资产管理；先分清 Stars Today 和累计 Stars，再决定哪个仓库值得下班后点开。
- Top 3 高亮原因：按 GitHub 原始排名高亮 GeoLibre、AIRI、ECC，不以编辑偏好重新排序。
- 需要在 HTML 中诚实提示的降级点：Explore 与 Trending 高度重合；Stars Today 为抓取时动态快照；性能、效果和生产规模未独立复测。
- 不允许省略的区块：Meta、Stats、四条洞察、Top 12、语言分布、Explore、Evidence/Honest Caveat。
- 必须保留的固定模板结构：
  - Header / Hero
  - 4 张 Stats Cards
  - 今日洞察
  - 今日热门 Top 12
  - 编程语言分布
  - GitHub Explore 精选
  - Footer
- Top 详情固定顺序：
  1. 项目摘要
  2. 核心特性
  3. 技术栈
  4. 适用场景
  5. 一句话推荐

## Validation

- 8 个页面区块数据：PASS
- Top 12 完整字段：PASS
- 原始排名保留：PASS
- 累计 Stars / Stars Today 分离：PASS
- 项目摘要 / 核心特性 / 技术栈 / 适用场景 / 一句话推荐：PASS
- Evidence Notes / Honest Caveat：PASS
- Explore 抓取：PASS（与 Trending 高度重合，已说明）
- Markdown Gate: PASS
