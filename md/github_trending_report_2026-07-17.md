# GitHub Trending 日报内容底稿

## Meta

- Report Date: 2026-07-17
- Generated At: 2026-07-17 21:10:44 Asia/Tokyo
- Output Markdown: `md/github_trending_report_2026-07-17.md`
- Planned HTML: `html/github_trending_report_2026-07-17.html`
- Fixed Base Template: `.codex/skills/skill-github-trending-report/reference/fixedBaseTemplate_2026-03-16.html`
- User Rules: `.codex/skills/skill-github-trending-report/reference/user-rules.md`
- Sources:
  - GitHub Trending — Repositories / Any language / Today
  - GitHub Explore
  - Repo README / About / Homepage / public repository files

## Page Intent

- 今日主线：开发者工具与 AI Agent 继续占据主场，但真正拉开差距的，不只是“接了个模型”，而是能否把模型、工具、数据和运行边界组织成可落地的工作流。
- 适合谁阅读：想快速筛选开源工具的开发者、技术负责人、AI 应用工程师、产品与数据团队。
- 页面重点：保留 GitHub 官方原始排名，突出当日 Stars 增量，并把项目的现实成熟度、许可证与采用门槛讲清楚。
- 需要诚实降级说明的地方：Stars Today 来自 GitHub Trending 页面快照，会随抓取时间变化；部分仓库处于重写、实验或模型演示阶段，不代表已经具备稳定生产能力。

## Stats

- Trending 项目数：12
- 今日累计新增 Stars：12,451
- 编程语言数：7
- AI 相关项目数：8

## Editorial Insights

### Insight 1
- Title: AI 编程工具开始比拼“运行底盘”
- Body: Open Interpreter、LobeHub、DeepTutor 和两套工程 Skills 都不再满足于给模型套一层聊天界面。它们在争夺的是会话状态、工具调用、权限、长期任务、知识库和多 Agent 编排。模型仍重要，但决定用户体验的越来越是 Agent harness 和运行时工程。

### Insight 2
- Title: 本地小模型从“能跑”走向“能做事”
- Body: Bonsai Demo 把 1-bit / ternary 模型、llama.cpp、MLX、视觉输入、OpenAI 风格工具调用和 MCP 放进一套安装脚本里。今日热度说明，开发者关心的不只是压缩率，而是普通设备能否真正跑起长上下文、视觉和工具链。

### Insight 3
- Title: 开源生产力工具一边爆发，一边重写地基
- Body: OpenCut 的当日增量最高之一，但当前主仓库明确处于从零重写阶段，经典版本才是现阶段更稳妥的使用入口。这类项目最容易让星标把成熟度遮住：关注度很高，不等于新架构已经交付完毕。

### Insight 4
- Title: 数据、规范与技能库也能成为基础设施
- Body: Apache Ossie 试图统一分析、AI 与 BI 的语义元数据；exercises-dataset 把健身数据、Schema 和前端浏览器打包；awesome-llm-apps 与 mattpocock/skills 则把可复用案例和工程方法做成分发单元。今天的基础设施，不一定是一台服务器，也可能是一套可验证的语义或工作流契约。

## Top Projects

### Rank 01 - apache/ossie
- Repo URL: https://github.com/apache/ossie
- Tagline: 为分析、AI 与 BI 平台定义厂商中立的语义元数据交换规范。
- Stars: 1,056
- Stars Today: 60
- Forks: 142
- Language: Python
- License: Apache-2.0
- Homepage: https://ossie.apache.org
- Topics: metadata, semantic
- 技术栈: JSON, YAML, JSON Schema, Python, semantic metadata
- Why It Matters Today: 生成式 AI 正在消费越来越多企业指标与语义层数据，跨工具共享“指标究竟是什么意思”比再造一套查询接口更难，Ossie 正面处理这个互操作问题。
- 项目摘要: Apache Ossie 是一套语义元数据交换规范及配套工具，目标是在分析、AI 和 BI 产品之间交换指标、维度、实体与关系定义，让同一业务口径不必在每个平台重新翻译。仓库包含核心规范、示例、转换器、校验与文档。
- 核心特性:
  1. 用 JSON/YAML 表达厂商中立的语义模型，并通过 Schema 约束结构。
  2. 提供示例、验证与转换工具，方便现有平台接入，而不是只发一份概念白皮书。
  3. 面向指标口径、语义层迁移和 AI 数据上下文共享，减少平台锁定。
- 适用场景: 多 BI/分析平台共存、企业语义层治理、需要向 AI Agent 提供可靠指标定义、语义模型迁移与审计。
- 一句话推荐: 如果你们的数据平台常为“同一个收入指标到底怎么算”开会，Ossie 想先把这门外语统一了。
- Evidence Notes: GitHub Trending 原始排名第 1；仓库 README、core-spec、converters、examples 与 validation 目录共同支持定位。
- Honest Caveat: 规范的价值取决于工具厂商和企业采纳度；仓库存在实现工具，不代表所有主流平台已经完成兼容。

### Rank 02 - Nutlope/hallmark
- Repo URL: https://github.com/Nutlope/hallmark
- Tagline: 面向 Claude Code、Cursor 和 Codex 的反 AI 套路化界面设计 Skill。
- Stars: 11,399
- Stars Today: 3,372
- Forks: 566
- Language: CSS
- License: MIT
- Homepage: https://usehallmark.com
- Topics: design-skill, claude-code, cursor, codex, anti-ai-slop
- 技术栈: Agent Skills, Markdown, CSS, design heuristics, automated design audit
- Why It Matters Today: AI 生成页面越来越多，但“渐变大标题、玻璃卡片、万能 dashboard”也越来越像批发市场。Hallmark 把设计批评与审校标准做成 Agent 可执行的技能。
- 项目摘要: Hallmark 是一套给编码 Agent 使用的设计技能，提供 build、audit、redesign、study 四类工作方式，并用主题知识和规则门禁约束常见的 AI 套路化设计。它更像设计审校手册与执行流程，而不是 UI 组件库。
- 核心特性:
  1. 覆盖从新建设计、现有页面审计到重设计和风格研究的完整流程。
  2. 提供多类视觉主题与反模式检查，要求 Agent 解释设计选择，而非只换配色。
  3. 可安装到主流编码 Agent，直接参与生成与评审过程。
- 适用场景: AI 辅助前端开发、设计系统审查、营销页与产品页去模板化、团队统一 AI 产出质量门槛。
- 一句话推荐: 它不是给页面化妆，是先把 AI 那套“紫色渐变加玻璃卡”从购物车里删了。
- Evidence Notes: README 明确列出四类动作、主题集合与审校门禁；About 指向 usehallmark.com。
- Honest Caveat: 设计判断仍带主观性；Skill 能改善过程，不能替代真实用户研究、品牌规范和专业设计评审。

### Rank 03 - OpenCut-app/OpenCut
- Repo URL: https://github.com/OpenCut-app/OpenCut
- Tagline: 面向 Web、桌面与移动端的开源视频编辑器，目标是成为 CapCut 的开放替代品。
- Stars: 74,363
- Stars Today: 3,537
- Forks: 7,512
- Language: TypeScript
- License: MIT
- Homepage: https://opencut.app
- Topics: editor, oss, videoeditor
- 技术栈: TypeScript, React 19, Vite 8, TanStack Router/Start, Cloudflare Workers, Rust, GPUI, Moonrepo
- Why It Matters Today: 视频生产工具的开放替代需求很强，3,500+ 当日新增 Stars 说明用户愿意押注；但项目正处于架构重写，热度和可用版本必须分开看。
- 项目摘要: OpenCut 是免费开源视频编辑器项目。当前主仓库正在从零重写，规划以 Rust core 支撑浏览器、桌面和移动端，并加入 Editor API、插件优先架构、MCP、无头模式和脚本能力。现阶段官方仍建议需要稳定使用的用户选择 classic 版本。
- 核心特性:
  1. 目标覆盖 Web、桌面与移动端，并用统一核心减少平台分叉。
  2. 规划 Editor API、第三方插件、无头批处理和 Agent/MCP 集成。
  3. 新仓库已经搭起 Web、Cloudflare API 与 GPUI 桌面工程，但编辑器核心仍在设计与迁移。
- 适用场景: 跟踪开源创作工具架构、参与早期视频编辑器生态、评估未来自动化剪辑和插件开发；当前生产剪辑优先 classic。
- 一句话推荐: 星星很亮，地基还在浇；想围观未来可以冲，今晚交片先别拿它赌命。
- Evidence Notes: README 明确说明重写状态、未来能力与 classic 推荐；apps/web、apps/api、apps/desktop 和 Cargo workspace 可验证当前工程边界。
- Honest Caveat: README 明确表示架构仍在设计且暂不接收外部贡献；规划能力不能当作已交付功能。

### Rank 04 - PostHog/posthog
- Repo URL: https://github.com/PostHog/posthog
- Tagline: 把产品分析、回放、Feature Flags、实验、错误、日志、AI 可观测性和数据管道放进同一平台。
- Stars: 35,981
- Stars Today: 77
- Forks: 2,999
- Language: Python
- License: MIT
- Homepage: https://posthog.com
- Topics: analytics, product-analytics, session-replay, feature-flags, experiments, ai-observability
- 技术栈: Python, Django, React/TypeScript, ClickHouse, Kafka, PostgreSQL, Rust, Docker, Terraform
- Why It Matters Today: 当产品数据、LLM trace、错误与发布动作散落在多套工具中，Agent 很难获得完整上下文。PostHog 正把这些数据收拢，进一步尝试让 Agent 主动诊断并提交修复。
- 项目摘要: PostHog 是开源产品工程平台，覆盖产品与 Web 分析、会话回放、Feature Flags、A/B 实验、错误跟踪、日志、数据仓库、数据管道、AI 可观测性和自动化工作流。仓库是大型多语言 monorepo，支持云服务与高级自托管部署。
- 核心特性:
  1. 从用户行为、LLM 调用、错误与日志中收集统一上下文。
  2. 把分析、实验、发布控制和数据外发放在一套产品中，减少工具间拼接。
  3. Self-driving mode 尝试把异常信号转成研究报告与可审查的代码变更。
- 适用场景: SaaS 产品分析、增长实验、会话诊断、LLM 应用 trace、Feature Flag 发布治理以及统一数据管道。
- 一句话推荐: 想少养几套互相不说话的数据工具，PostHog 是那只打算把桌子都搬到一起的刺猬。
- Evidence Notes: 官方 README 列出各产品能力，仓库目录可验证前端、后端、服务、Rust、Docker 与 Terraform 等实现。
- Honest Caveat: 完整自托管复杂度高；开源仓库、云端产品和付费功能边界需要按最新官方说明逐项确认。

### Rank 05 - openinterpreter/openinterpreter
- Repo URL: https://github.com/openinterpreter/openinterpreter
- Tagline: 为 Kimi、Qwen、DeepSeek 等低成本开放模型优化的 Rust 编码 Agent。
- Stars: 66,135
- Stars Today: 661
- Forks: 5,681
- Language: Rust
- License: Apache-2.0
- Homepage: https://openinterpreter.com
- Topics: rust, acp, kimi, qwen, deepseek, coding-agent
- 技术栈: Rust, Codex-derived agent runtime, TUI, ACP, MCP, sandboxing, tool calling
- Why It Matters Today: 开放模型能力在涨，但同一模型放进不同 harness，工程效果可能差一截。Open Interpreter 把“适配模型的 Agent 运行方式”作为核心产品，而不是只换 API 地址。
- 项目摘要: 新版 Open Interpreter 是基于 OpenAI Codex 代码演进的 Rust 编码 Agent，重点复刻和切换不同模型供应商推荐的 harness。它提供交互 TUI、非交互 exec、ACP、MCP、沙箱、权限、会话恢复、工具与本地状态管理。
- 核心特性:
  1. `/harness` 在 native、Claude Code、Kimi Code、Qwen Code、DeepSeek 等提示与工具范式间切换。
  2. 兼容 ACP 和 Codex exec 协议，可接编辑器或现有 SDK。
  3. 原生沙箱、权限审批、会话状态、工具调用和可恢复执行共同形成完整运行时。
- 适用场景: 使用低成本开放模型完成代码修改、终端任务、编辑器 Agent 接入、模型 harness 对比与本地自动化。
- 一句话推荐: 同一匹马换套鞍具就能跑出不同成绩，这个项目专门研究鞍具，还顺手把马厩也盖了。
- Evidence Notes: README、Rust workspace、CLI 入口、core/session、shell-command、sandboxing、exec 与 protocol 模块相互验证。
- Honest Caveat: 项目继承并扩展大型 Codex 代码基线，模块很多、迭代快；不同模型的效果主张仍需在真实任务集独立验证。

### Rank 06 - PrismML-Eng/Bonsai-demo
- Repo URL: https://github.com/PrismML-Eng/Bonsai-demo
- Tagline: 在消费级设备本地运行 1-bit 与 ternary Bonsai 模型的完整演示与安装工具链。
- Stars: 1,617
- Stars Today: 196
- Forks: 158
- Language: Shell
- License: Apache-2.0
- Homepage: https://prismml.com
- Topics: bonsai, mlx, llm, small-models, llamacpp, prism-ml
- 技术栈: Shell, Python/uv, llama.cpp, MLX, GGUF, Open WebUI, MCP, OpenAI-compatible API
- Why It Matters Today: 模型压缩是否有价值，最后要落到普通机器能否安装、加载、推理、处理视觉和调用工具。Bonsai Demo 把论文结果变成可执行路径。
- 项目摘要: Bonsai Demo 提供脚本、预编译二进制、模型下载和 UI 集成，让用户在 macOS、Linux、Windows、GPU 或 CPU 上运行 Bonsai 1-bit / Ternary-Bonsai 模型。27B 系列支持视觉、推理力度、长上下文、OpenAI 风格工具调用与 MCP。
- 核心特性:
  1. `setup.sh` / `setup.ps1` 负责依赖、虚拟环境、模型、二进制与可选 WebUI 安装。
  2. 支持 llama.cpp 和 Apple MLX，多种模型尺寸与硬件后端。
  3. 提供聊天服务器、视觉输入、工具调用、MCP、可选 speculative decoding 与 KV cache 优化。
- 适用场景: 本地模型评估、消费级硬件部署、量化格式测试、离线聊天、视觉问答与工具调用实验。
- 一句话推荐: 论文说模型瘦了不算数，能在你桌上的机器跑起来，才算真的减肥成功。
- Evidence Notes: README、setup 脚本、run/start 脚本、TOOLS/VISION/KV-CACHE 文档和测试目录形成直接证据。
- Honest Caveat: 性能与内存数字来自项目方及社区基准，硬件、上下文长度和后端会显著影响结果；27B 模型访问条件也可能变化。

### Rank 07 - hasaneyldrm/exercises-dataset
- Repo URL: https://github.com/hasaneyldrm/exercises-dataset
- Tagline: 带 Schema、缩略图、动作 GIF 和多语言步骤的 1,324 条健身动作数据集。
- Stars: 15,233
- Stars Today: 710
- Forks: 1,830
- Language: HTML
- License: MIT（代码、结构和文字）；媒体另有归属与复用限制
- Homepage: https://github.com/hasaneyldrm/exercises-dataset
- Topics: json, fitness, dataset, gym, exercises, workout, exercise-database
- 技术栈: JSON, JSON Schema 2020-12, static HTML, local media assets
- Why It Matters Today: 开发者需要的不是一张“动作名称表”，而是能直接导入、验证、检索和展示的数据层。这个仓库把 Schema、媒体与开发接入向导一起交付。
- 项目摘要: exercises-dataset 收录 1,324 个健身动作，包含目标肌群、器械、步骤、多语言指令、缩略图与动画 GIF。仓库自带纯前端浏览器、JSON Schema 和数据库/API 接入向导，不需要服务器即可检索查看。
- 核心特性:
  1. 结构化 JSON 数据配套正式 Schema，可验证字段和自定义扩展。
  2. 每个动作包含本地缩略图、GIF 和多语言说明。
  3. 静态浏览器支持搜索、筛选、无限滚动；setup 页面可生成数据库导入与 API 示例。
- 适用场景: 健身 App 原型、训练计划工具、动作搜索、教学演示、推荐与识别研究的数据准备。
- 一句话推荐: 这不是“健身动作大全.txt”，而是一箱拆开就能接后端的数据零件。
- Evidence Notes: README 给出文件结构、Schema、浏览器和使用示例；LICENSE 与 NOTICE 单独说明媒体授权。
- Honest Caveat: 图片和 GIF 并非普通 MIT 资产，复用前必须保留归属并核对 Gym visual 条款；健康产品还需专业内容审核。

### Rank 08 - Shubhamsaboo/awesome-llm-apps
- Repo URL: https://github.com/Shubhamsaboo/awesome-llm-apps
- Tagline: 100+ 可运行的 AI Agent、RAG 与多模态应用模板合集。
- Stars: 123,229
- Stars Today: 923
- Forks: 18,166
- Language: Python
- License: Apache-2.0
- Homepage: https://www.theunwindai.com
- Topics: python, agents, rag, llms
- 技术栈: Python, Streamlit, multiple LLM SDKs, vector stores, RAG, agents
- Why It Matters Today: 大量团队仍卡在“看完概念，不知道怎么拼成应用”。这个仓库用可克隆案例覆盖研究、金融、语音、多 Agent、RAG 与 MCP，降低第一步成本。
- 项目摘要: awesome-llm-apps 是经过分类的开源 AI 应用案例库，包含基础 Agent、团队协作、RAG、语音、记忆、MCP 和垂直场景。每个子项目通常独立安装和运行，便于学习、改造或作为原型起点。
- 核心特性:
  1. 覆盖主流闭源和开放模型，不把示例绑定在一家供应商上。
  2. 案例按能力和业务场景组织，包含从最小链路到复杂多 Agent 系统。
  3. Apache-2.0 便于复制与二次开发，但各子项目依赖和外部服务成本不同。
- 适用场景: AI 应用入门、内部 PoC、技术选型对比、RAG/Agent 教学和垂直场景原型。
- 一句话推荐: 不知道第一锅怎么炒，先照菜谱做；但上馆子营业前，还得自己把厨房重新收拾一遍。
- Evidence Notes: README 声明 100+ 手工构建并端到端测试的案例，目录按 agents、rag_tutorials、voice_ai_agents 等分类。
- Honest Caveat: 它是应用合集而非统一框架；“能运行”不代表已处理生产安全、成本、并发、评测与数据治理。

### Rank 09 - lobehub/lobehub
- Repo URL: https://github.com/lobehub/lobehub
- Tagline: 把多个 Agent 组织成可招聘、排班、持续运行和汇报的 AI 团队操作平台。
- Stars: 80,334
- Stars Today: 71
- Forks: 15,621
- Language: TypeScript
- License: LobeHub Community License
- Homepage: https://lobehub.com
- Topics: agent, ai, skills, mcp, agent-collaboration, agent-harness, chief-agent-operator
- 技术栈: TypeScript, React/Next.js, Node.js, database adapters, multi-provider LLM, MCP, Docker/Vercel
- Why It Matters Today: Agent 数量一多，聊天窗口就不够用了。LobeHub 把关注点转向角色、排班、协作、知识和报告，试图解决 AI 团队运营问题。
- 项目摘要: LobeHub 从多模型聊天产品演进为 Chief Agent Operator，强调创建和组织 Agent、安排持续任务、接入知识与工具并汇报执行结果。项目支持多模型、多种部署方式与自托管。
- 核心特性:
  1. 通过角色、技能、知识库与工具配置 Agent，并组织协作。
  2. 支持多家模型与 MCP 扩展，减少对单一供应商的绑定。
  3. 提供 Web、自托管和云端使用路径，覆盖个人到团队场景。
- 适用场景: 多 Agent 工作台、知识助手、持续研究与运营任务、团队私有化 AI 门户。
- 一句话推荐: 一个 Agent 是员工，十个 Agent 就得有人排班、发工单、收周报；它瞄准的就是这个办公室。
- Evidence Notes: README、About、topics 和自托管章节支持定位；仓库为大型 TypeScript monorepo。
- Honest Caveat: 使用的是 Community License，不应按标准宽松开源许可证理解；长期自治任务的可靠性、成本和权限仍需实测。

### Rank 10 - YimMenu/YimMenuV2
- Repo URL: https://github.com/YimMenu/YimMenuV2
- Tagline: 面向 GTA 5 Enhanced 的实验性 C++ 菜单与修改框架。
- Stars: 1,532
- Stars Today: 128
- Forks: 363
- Language: C++
- License: GPL-2.0
- Homepage: https://github.com/YimMenu/YimMenuV2
- Topics: gta5, mod-menu, cplusplus
- 技术栈: C++23, CMake, DLL injection, game hooks, ImGui-style UI
- Why It Matters Today: GTA 5 Enhanced 的兼容性变化让旧工具失效，实验性重构项目因此集中获得关注。
- 项目摘要: YimMenuV2 是 GTA 5 Enhanced 的实验性菜单项目，以 C++ 和 CMake 构建，需要 DLL 注入并关闭 BattlEye 才能运行。仓库明确记录了公共会话掉线、FSL 本地存档和启动问题。
- 核心特性:
  1. 针对 Enhanced 版本重建菜单功能和底层钩子。
  2. 提供 CMake 工程、文档、Nightly Release 与常见问题说明。
  3. FSL 可把账户存档重定向到本地，但会改变进度可见性和运行方式。
- 适用场景: 仅限了解游戏 Mod 工程、私有测试环境和 C++ hook 技术研究。
- 一句话推荐: 技术上是拆发动机，使用上是踩红线；别把“能编译”自动翻译成“该上线”。
- Evidence Notes: README 明确要求注入器、关闭 BattlEye，并描述公共会话与存档问题；仓库许可证为 GPL-2.0。
- Honest Caveat: 可能违反游戏服务条款并触发封禁或安全风险；本报告只描述公开仓库，不推荐绕过反作弊或在线滥用。

### Rank 11 - HKUDS/DeepTutor
- Repo URL: https://github.com/HKUDS/DeepTutor
- Tagline: 集知识库、Agent loop、长期记忆、学习路径和多渠道伙伴于一体的个性化 AI 学习平台。
- Stars: 27,083
- Stars Today: 656
- Forks: 3,629
- Language: Python
- License: Apache-2.0
- Homepage: https://deeptutor.info
- Topics: interactive-learning, multi-agent-systems, ai-agents, rag, ai-tutor, deepresearch
- 技术栈: Python 3.11+, FastAPI, Next.js 16, LlamaIndex, FAISS, SQLite/PocketBase, WebSocket/SSE, multi-provider LLM
- Why It Matters Today: AI 教育项目容易停在“聊天回答题”，DeepTutor 把知识库、学习路径、测验、记忆、研究和多个沟通渠道放进一套持续演进系统。
- 项目摘要: DeepTutor 是 Agent-native 学习伴侣，提供 Chat、Deep Research、Deep Solve、Guided Learning、知识库、三层记忆、问题本与可扩展 Partner/Skills。后端 Python，Web 前端为 Next.js，并提供 CLI、容器和多渠道集成。
- 核心特性:
  1. 单一 Agent loop 统一聊天能力，支持工具调用、知识库检索、流式输出和中断恢复。
  2. LlamaIndex/FAISS 等可替换 RAG 后端，支持多类文档解析与版本化索引。
  3. 三层记忆、学习路径、问题库和 Partner 私有知识让系统可持续个性化。
- 适用场景: 自建课程助教、个人知识学习、研究资料问答、企业培训与多渠道教育伙伴。
- 一句话推荐: 普通 AI 家教只会答题，它想把课本、错题本、学习计划和班主任办公室一块儿搬进来。
- Evidence Notes: pyproject、agent_loop、turn_runtime、knowledge、web、CLI、Docker 与发布记录相互支持。
- Honest Caveat: 系统面广且依赖多，部署和模型配置不轻；教育正确性、隐私、成本与长期学习效果需要独立评估。

### Rank 12 - mattpocock/skills
- Repo URL: https://github.com/mattpocock/skills
- Tagline: 把需求澄清、TDD、调试、架构改进和代码审查做成可组合的 Agent Skills。
- Stars: 174,845
- Stars Today: 2,060
- Forks: 14,991
- Language: Shell
- License: MIT
- Homepage: https://www.aihero.dev
- Topics: agent-skills, engineering, tdd, code-review, claude-code
- 技术栈: Agent Skills, Markdown, Shell, Claude Code plugin, skills.sh
- Why It Matters Today: 开发 Agent 写代码越来越快，需求错位、反馈环断裂和架构腐化也能更快。这个仓库把传统工程纪律包装成 Agent 能反复执行的流程。
- 项目摘要: mattpocock/skills 是一组小型、可组合、模型无关的工程 Skills，覆盖需求追问、领域语言、规格、TDD、诊断、代码审查、合并冲突、研究与交接。可复制进项目自行修改，也可作为 Claude Code 插件订阅更新。
- 核心特性:
  1. 区分用户触发的编排 Skill 与模型自动调用的纪律 Skill，避免工作流互相套娃。
  2. 强调需求对齐、共享领域语言和短反馈循环，而不是让 Agent 全权接管流程。
  3. 提供 skills.sh 与 Claude Code plugin 两种安装哲学：可修改副本或只读更新包。
- 适用场景: AI 编程团队规范、需求澄清、TDD、疑难 Bug 诊断、架构治理和代码评审。
- 一句话推荐: 让 Agent 写快不难，让它别把坑也挖快了才难；这套技能就是给刹车、方向盘和后视镜配齐。
- Evidence Notes: README 解释 Skills 的设计动机、调用边界、安装方式与工程清单；最新 Release 为 v1.1.0。
- Honest Caveat: 仓库本身主要是方法与指令资产，不是独立运行系统；效果取决于 Agent 对 Skill 协议的支持和团队执行纪律。

## Language Distribution

- Python:
  - Count: 4
  - Percent: 33.3%
  - Color Hint: #3572A5
- TypeScript:
  - Count: 2
  - Percent: 16.7%
  - Color Hint: #3178C6
- Shell:
  - Count: 2
  - Percent: 16.7%
  - Color Hint: #89E051
- CSS:
  - Count: 1
  - Percent: 8.3%
  - Color Hint: #563D7C
- Rust:
  - Count: 1
  - Percent: 8.3%
  - Color Hint: #DEA584
- HTML:
  - Count: 1
  - Percent: 8.3%
  - Color Hint: #E34C26
- C++:
  - Count: 1
  - Percent: 8.3%
  - Color Hint: #F34B7D

## Explore Highlights

### Explore 1
- Title: Rubber Duck Thursdays
- URL: https://www.youtube.com/@GitHub
- Kind: GitHub Event / Live Coding
- Meta: GitHub Explore 官方活动推荐
- Short Reason: 轻松形式的开源协作与现场编程，适合观察真实维护流程。

### Explore 2
- Title: React
- URL: https://github.com/topics/react
- Kind: Popular Topic
- Meta: GitHub 今日热门话题
- Short Reason: 前端 UI 基础生态继续保持高关注度。

### Explore 3
- Title: Game Engines
- URL: https://github.com/collections/game-engines
- Kind: GitHub Collection
- Meta: 64 个跨平台游戏引擎与框架
- Short Reason: 从成熟引擎到实验框架的一站式选型入口。

### Explore 4
- Title: Repography
- URL: https://repography.com
- Kind: GitHub Staff Recommendation
- Meta: README 数据仪表板与项目可视化海报
- Short Reason: 把仓库贡献与演进数据变成可嵌入的可视化材料。

### Explore 5
- Title: GitHub Checkout — Copilot cloud agent
- URL: https://youtu.be/
- Kind: GitHub Video
- Meta: 合并冲突与 Pull Request 工作流
- Short Reason: 展示云端编码 Agent 如何参与冲突处理和 PR 推进。

### Explore 6
- Title: github/copilot-sdk
- URL: https://github.com/github/copilot-sdk
- Kind: Repository
- Meta: Copilot Agent SDK
- Short Reason: 适合关注如何把 Copilot 能力嵌入自己的应用与工作流。

### Explore 7
- Title: Graphify-Labs/graphify
- URL: https://github.com/Graphify-Labs/graphify
- Kind: Repository
- Meta: 代码与知识图谱方向项目
- Short Reason: 延续近期用图结构增强代码理解和检索的趋势。

### Explore 8
- Title: Deploybot-app
- URL: https://github.com/Deploybot-app
- Kind: Repository / Tool
- Meta: GitHub Explore 补充推荐
- Short Reason: 作为 Trending 之外的部署自动化工具线索，供进一步筛选。

## Rendering Notes

- Hero 主标题建议：GitHub Trending 日报
- Hero 副标题建议：今天最热的不只是 AI，还有让 AI 真正干活的工程底盘
- Top 3 高亮原因：保持 GitHub 官方原始排名 01–03，不按累计 Stars 二次排序。
- 需要在 HTML 中诚实提示的降级点：OpenCut 主仓库处于重写阶段；Bonsai 性能来自项目方与社区基准；YimMenu 存在服务条款和安全风险；Explore 中视频/活动链接信息按抓取页面呈现。
- 不允许省略的区块：Header / Hero、4 张 Stats Cards、今日洞察、今日热门 Top 12、编程语言分布、GitHub Explore 精选、Footer。
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

## Markdown 验收

- [x] Top 12 保留 GitHub Trending 原始排名。
- [x] 累计 Stars 与 Stars Today 分开记录。
- [x] 12 个项目字段、摘要、特性、技术栈、场景、推荐语、证据和 Caveat 完整。
- [x] 4 张统计卡数据已计算。
- [x] 语言分布合计 12 个项目。
- [x] Explore 与 Trending 分区呈现。
- [x] 风险、许可证和成熟度未被热度数字掩盖。
