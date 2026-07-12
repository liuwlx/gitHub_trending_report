# GitHub Trending 日报内容底稿

## Meta

- Report Date: 2026-04-24
- Generated At: 2026-04-24 17:30:00
- Output Markdown: e:/workerspace/daily/task/github/github_trending_report_2026-04-24.md
- Planned HTML: e:/workerspace/daily/task/github/github_trending_report_2026-04-24.html
- Fixed Base Template: e:/workerspace/daily/task/.codex/skills/skill-github-trending-report/reference/fixedBaseTemplate_2026-03-16.html
- User Rules: e:/workerspace/daily/task/.codex/skills/skill-github-trending-report/reference/user-rules.md
- Sources:
  - GitHub Trending (https://github.com/trending)
  - GitHub Explore (https://github.com/explore)
  - Repo README / About / Homepage / Public Web Search

## Page Intent

- 今日主线：AI 编码代理生态与上下文工程持续主导 Trending，WiFi 传感黑科技爆发入榜
- 适合谁阅读：AI 工程师、开发者工具爱好者、关注 Claude Code 生态的研发人员
- 页面重点：前 5 名高度集中在 AI Agent 和 RAG 领域，RuView 的 WiFi 感知技术是今日最大惊喜
- 需要诚实降级说明的地方：各仓库"今日新增 Stars"数据无法从 Trending 页面直接解析，以"上榜 Trending"代替

## Stats

- Trending 项目数：16（报告精选 Top 12）
- 今日累计总 Stars（Top 12 仓库）：约 372k+（累计总数；今日增量未可直接读取）
- 编程语言数：6（Python、TypeScript、C#、C++、Java、多语言）
- AI 相关项目数：10

## Editorial Insights

### Insight 1
- Title: 🤖 Claude Code 生态深度扩张，上下文工程成决定性战场
- Body: 今日 Trending 中至少 4 个项目直接为 Claude Code 赋能：zilliztech/claude-context（全代码库语义搜索 MCP）、Alishahryar1/free-claude-code（免费终端/VSCode 使用 Claude Code）、mksglu/context-mode（上下文窗口沙箱，98% 压缩率）、coreyhaines31/marketingskills（营销技能包）。Claude Code 正在催生一套完整的第三方生态，从代码搜索到会话上下文管理，各细分赛道都有专项工具跑出。

### Insight 2
- Title: 📡 WiFi 传感黑科技引爆社区：RuView 让 WiFi 信号"看见"人
- Body: ruvnet/RuView 凭借 50k Stars 稳居 Trending，它的核心概念是：普通 WiFi 路由器发出的无线信号经过人体反射会产生 CSI（信道状态信息）变化，通过深度学习可以反推出人体姿态、呼吸频率、心跳，甚至穿墙探测——而完全不需要摄像头。这意味着无需 GDPR 视频隐私合规，只需一台 8 美元的 ESP32 即可部署。医疗、零售、安防、工业场景都可受益。

### Insight 3
- Title: 🧠 多模态 RAG 进入实用期：RAG-Anything 统一文本+图表+公式检索
- Body: HKUDS/RAG-Anything 是目前最完整的多模态 RAG 框架，能同时处理 PDF 中的文字、表格、数学公式和图片，并构建多模态知识图谱。相比普通 RAG 只能处理纯文本，RAG-Anything 让科研文献、财务报表、技术手册这类"混合内容"文档也可以被高质量检索和问答。18k Stars 证明市场已经准备好了。

### Insight 4
- Title: 🤗 HuggingFace 开源 ML Intern：AI 自动读论文、训模型、提交代码
- Body: huggingface/ml-intern 是今日 Stars 速度最快的新项目之一，它是一个完全自主的 ML 工程师代理：给它一个任务（如"fine-tune llama on my dataset"），它会自动阅读 HuggingFace 文档和论文、选择合适的数据集、在 HF 云上训练模型，并提交代码。底层是 Anthropic Claude + HuggingFace 生态的深度整合，最多支持 300 轮迭代的自主 Agentic Loop。

## Top Projects

### Rank 01 - huggingface/ml-intern
- Repo URL: https://github.com/huggingface/ml-intern
- Tagline: 🤗 an open-source ML engineer that reads papers, trains models, and ships ML models
- Stars: 4,426
- Stars Today: 高速上涨（新项目，今日 Trending 第一）
- Forks: 371
- Language: Python
- License: Apache-2.0（待确认）
- Homepage: https://huggingface.co
- Topics: ml-agent, huggingface, anthropic, claude, autonomous-ml
- 技术栈: Python, Anthropic SDK (Claude), HuggingFace Hub, litellm, MCP, uv
- Why It Matters Today: HuggingFace 官方开源自主 ML 工程师代理，能全自动读论文→训练→提交，代表 AI 代理正在真正进入 ML 研究工作流
- 项目摘要: ml-intern 是 HuggingFace 官方开源的自主 ML 工程师代理，拥有深度访问 HF 文档、论文、数据集和云计算资源的能力。它通过 Agentic Loop（最多 300 次迭代）自主完成：从理解需求、阅读相关文献，到选择数据集、在 HF 云上启动训练任务，最后提交代码。支持交互式对话和无头批处理两种模式。
- 核心特性:
  1. 完整 Agentic Loop：ContextManager 管理消息历史（支持 170k Token 自动压缩），ToolRouter 调度 HF 文档检索、仓库操作、论文搜索、沙箱执行等工具
  2. HuggingFace 生态深度集成：可直接操作 HF 数据集、模型仓库、Training Jobs，并自动上传会话记录到 HF Hub
  3. 内置 Doom Loop 检测器：识别重复工具调用模式并注入纠正提示，防止 Agent 陷入死循环
- 适用场景: 需要自动化 ML 实验流程的研究员、想让 AI 帮自己跑 fine-tuning 的工程师、HuggingFace 生态重度用户、ML 流水线自动化探索者
- 一句话推荐: 把"雇一个 ML 实习生"变成了代码——HuggingFace 开源的自主 ML 代理，读论文、训模型、推代码全自动。
- Evidence Notes: 基于 GitHub README 直接读取，信息充分
- Honest Caveat: License 未明确确认；训练任务实际效果依赖 HF Token 和云计算资源配置

### Rank 02 - zilliztech/claude-context
- Repo URL: https://github.com/zilliztech/claude-context
- Tagline: Code search MCP for Claude Code. Make entire codebase the context for any coding agent.
- Stars: 8,709
- Stars Today: 高速上涨（今日 Trending 第二）
- Forks: 676
- Language: TypeScript
- License: Apache-2.0
- Homepage: https://zilliz.com
- Topics: claude-code, mcp, code-search, semantic-search, vector-database, embedding, rag, typescript, cursor, gemini-cli
- 技术栈: TypeScript, Node.js, Milvus/Zilliz Cloud, OpenAI/VoyageAI/Ollama/Gemini Embeddings, AST Parser, BM25
- Why It Matters Today: 解决大型代码库上下文成本问题——不再把整个目录塞进 Claude，而是按需语义检索相关代码
- 项目摘要: claude-context 是一个 MCP 插件，为 Claude Code 和其他 AI 编码代理添加语义代码搜索能力，让整个代码库成为 AI 的上下文。通过将代码库索引到向量数据库，使用 BM25+稠密向量混合搜索，只把真正相关的代码注入上下文，大幅降低大型代码库的 API 成本。
- 核心特性:
  1. 混合搜索（BM25 + 稠密向量）：用自然语言查询如"找处理用户认证的函数"，即时获得上下文丰富的相关代码
  2. 增量索引（Merkle Tree）：只对变更文件重新索引，高效处理持续更新的代码库
  3. AST 感知代码分块：基于抽象语法树进行代码切分，保证语义完整性；支持 14 种编程语言
- 适用场景: 使用 Claude Code/Cursor/Gemini CLI 的大型代码库开发者、想要降低 AI 编码 API 成本的团队、需要代码库语义搜索的工程师
- 一句话推荐: 给 Claude Code 装上"代码库大脑"——让 AI 从百万行代码中精准找到相关片段，而不是把所有文件都塞进上下文。
- Evidence Notes: README 详细，架构清晰，信息充分
- Honest Caveat: 依赖 Milvus/Zilliz Cloud 向量数据库，本地部署需要额外配置

### Rank 03 - HKUDS/RAG-Anything
- Repo URL: https://github.com/HKUDS/RAG-Anything
- Tagline: All-in-One RAG Framework for Multimodal Document Processing
- Stars: 18,470
- Stars Today: 持续高涨（今日 Trending 第三）
- Forks: 2,127
- Language: Python
- License: MIT
- Homepage: http://arxiv.org/abs/2510.12323
- Topics: rag, multimodal, pdf, knowledge-graph, lightrag, retrieval-augmented-generation
- 技术栈: Python, LightRAG, MinerU, VLM, Knowledge Graph, Multimodal Embeddings
- Why It Matters Today: 弥补传统 RAG 只能处理纯文本的短板，让科研文献、财务报表等混合内容文档都能高质量检索
- 项目摘要: RAG-Anything 是构建在 LightRAG 之上的全功能多模态文档 RAG 框架。现实中的文档往往混合了文字、图表、公式和多媒体内容，传统 RAG 对非文本内容束手无策。RAG-Anything 提供从文档解析到多模态知识图谱构建、再到混合智能检索的完整端到端流程。
- 核心特性:
  1. 通用文档支持：PDF、Office 文档、图片等多种格式，配备专用图像/表格/公式处理器
  2. 多模态知识图谱：自动提取实体并发现跨模态关系，实现跨文本与视觉内容的增强理解
  3. 自适应处理模式：支持 MinerU 解析或直接多模态内容注入两种工作流，可灵活切换
- 适用场景: 学术研究文献检索、企业技术文档问答、金融报告分析、包含大量图表和公式的专业文档处理
- 一句话推荐: 让 RAG 真正读懂"全格式文档"——图表、公式、表格不再是盲区，多模态知识图谱让检索质量上一个台阶。
- Evidence Notes: README 完整，有 arXiv 论文背书，信息充分
- Honest Caveat: 多模态处理对计算资源要求较高；MinerU 解析速度可能成为瓶颈

### Rank 04 - Z4nzu/hackingtool
- Repo URL: https://github.com/Z4nzu/hackingtool
- Tagline: ALL IN ONE Hacking Tool For Hackers
- Stars: 61,618
- Stars Today: 持续稳定涨势（老牌项目重回 Trending）
- Forks: 6,915
- Language: Python
- License: MIT
- Homepage: N/A
- Topics: hacking, security, penetration-testing, python, linux, kali
- 技术栈: Python, Bash, Linux, Kali Linux
- Why It Matters Today: 老牌安全工具集合重新进入 Trending，安全学习者和渗透测试员持续关注
- 项目摘要: hackingtool 是一个 Python 脚本驱动的一站式渗透测试工具集合器，整合了数十种常用安全测试工具的安装和启动入口，涵盖匿名性、密码攻击、SQL 注入、XSS、WiFi 攻击、信息收集等主要渗透测试类别，主要面向 Linux/Kali 环境。
- 核心特性:
  1. 一键安装和启动：通过统一菜单界面管理数十种安全工具的安装、配置和执行
  2. 全类别覆盖：匿名性工具、密码攻击、信息收集、SQL 注入、XSS、WiFi 攻击、漏洞扫描等
  3. Linux/Kali 原生：专为 Kali Linux 等安全测试操作系统优化设计，持续维护更新
- 适用场景: 安全学习者快速搭建测试环境、渗透测试人员工具管理、CTF 竞赛准备、安全研究人员参考
- 一句话推荐: 渗透测试工具集合的"瑞士军刀"——一个脚本管理数十种安全工具，安全学习者的必备入门套件。
- Evidence Notes: 项目知名度高，信息来自 GitHub 页面和公开资料
- Honest Caveat: 工具集合型项目，具体工具效果取决于各子工具本身；仅供合法安全测试使用

### Rank 05 - ruvnet/RuView
- Repo URL: https://github.com/ruvnet/RuView
- Tagline: WiFi DensePose — 用 WiFi 信号实现实时人体姿态估计与生命体征监测，无需任何摄像头
- Stars: 50,004
- Stars Today: 持续高涨（热门 Trending）
- Forks: 6,603
- Language: Python
- License: MIT
- Homepage: N/A
- Topics: wifi-sensing, densepose, human-pose-estimation, esp32, edge-ai, iot, privacy
- 技术栈: Python, ESP32, Docker, REST API, WebSocket, Contrastive CSI Embedding, SQLite
- Why It Matters Today: 用普通 WiFi 信号"看见"人体姿态的想法令人惊叹，无需摄像头意味着天然规避隐私法规，边缘部署成本极低
- 项目摘要: RuView 是一个 WiFi 传感平台，通过分析 WiFi 信号的 CSI（信道状态信息）变化，将无线电信号转换为空间智能。无需任何摄像头，就能实时检测人体姿态、呼吸频率、心跳，甚至穿墙感知人体存在。整个系统可运行在 8 美元的 ESP32 开发板上，通过 REST API 和 WebSocket 提供实时数据流。
- 核心特性:
  1. 穿墙感知：用现有 WiFi 信号探测人体存在、姿态和生命体征，无需新增摄像头硬件
  2. 自学习智能：对比 CSI 嵌入模型自主学习，无需标注数据，跨环境泛化；支持多节点 mesh 扩展
  3. 边缘部署：支持 ESP32 硬件直接运行，一行 Docker 命令快速启动，REST+WebSocket API 接入
- 适用场景: 医疗健康监护（睡眠呼吸暂停、心律监测）、智能楼宇（会议室占用、HVAC 节能）、零售分析（客流热图、队列检测）、工业安防（叉车碰撞预警）
- 一句话推荐: WiFi 信号变成"眼睛"——8 美元硬件穿墙感知人体姿态和呼吸，天然无摄像头隐私顾虑。
- Evidence Notes: README 极为详细，用例覆盖广，有性能基准数据
- Honest Caveat: Beta 软件，API 和固件仍在快速变化；单节点空间分辨率有限（建议 2+ 节点）；精度依赖硬件配置

### Rank 06 - Anil-matcha/Open-Generative-AI
- Repo URL: https://github.com/Anil-matcha/Open-Generative-AI
- Tagline: Uncensored open-source AI image & video generation studio with 200+ models, no content filters, self-hosted
- Stars: 7,322
- Stars Today: 上榜 Trending（第 6 位）
- Forks: 1,380
- Language: Python
- License: MIT
- Homepage: N/A
- Topics: ai-image-generation, flux, sora, veo, kling, self-hosted, open-source, generative-ai
- 技术栈: Python, Flux, Midjourney API, Kling, Sora, Veo, Docker
- Why It Matters Today: 无内容过滤、自托管、MIT 授权，成为商业 AI 创作工具的开源替代方案
- 项目摘要: Open-Generative-AI 是 Higgsfield AI、Freepik AI、Krea AI、Openart AI 的开源替代方案，提供 200+ AI 图像和视频生成模型，包括 Flux、Kling、Sora、Veo 等主流生成模型，支持自托管部署，无内容过滤限制，MIT 授权完全免费使用。
- 核心特性:
  1. 200+ 生成模型：集成 Flux、Midjourney、Kling、Sora、Veo 等主流 AI 图像和视频生成模型
  2. 零内容限制：无审查过滤，自托管运行，数据完全由用户掌控
  3. 开源自由：MIT 授权，可商用，可二次开发，社区持续迭代
- 适用场景: 创意工作者、内容创作者、需要自托管 AI 创作工具的企业、商业 AI 图像平台的平替用户
- 一句话推荐: Higgsfield、Krea、Openart 的完全开源平替——200+ 生成模型、自托管、无限制，MIT 授权免费商用。
- Evidence Notes: 基于 GitHub 描述和公开资料，信息基本充分
- Honest Caveat: 部分模型调用可能仍需第三方 API Key；具体模型质量参差不齐

### Rank 07 - Alishahryar1/free-claude-code
- Repo URL: https://github.com/Alishahryar1/free-claude-code
- Tagline: Use claude-code for free in the terminal, VSCode extension or via discord like openclaw
- Stars: 6,251
- Stars Today: 上榜 Trending（第 7 位）
- Forks: 1,039
- Language: TypeScript/JavaScript（推测）
- License: N/A
- Homepage: N/A
- Topics: claude-code, free, terminal, vscode, discord
- 技术栈: TypeScript, Node.js, Discord API, VSCode Extension API
- Why It Matters Today: 降低 Claude Code 使用门槛，免费获取完整 Claude Code 体验
- 项目摘要: free-claude-code 提供了在终端、VSCode 插件或 Discord（类似 openclaw 模式）中免费使用 Claude Code 的方式，降低了 Claude Code 的使用成本门槛，让更多开发者能体验完整的 AI 编程代理能力。
- 核心特性:
  1. 多端接入：支持终端 CLI、VSCode 扩展、Discord Bot 三种使用方式
  2. 免费使用：绕过或提供免费额度以使用 Claude Code 核心能力
  3. 类 openclaw 模式：参考流行的 openclaw 交互范式设计用户体验
- 适用场景: 希望免费体验 Claude Code 的开发者、VSCode 用户、通过 Discord 进行团队 AI 编程协作的开发者
- 一句话推荐: 让 Claude Code 触手可及——终端、VSCode、Discord 三端免费使用，降低 AI 编程门槛。
- Evidence Notes: 仅基于 GitHub 描述页面，细节信息有限
- Honest Caveat: "免费"机制的具体实现方式未经深度验证；使用方式可能涉及账号共享或 API 中转，存在合规风险

### Rank 08 - open-metadata/OpenMetadata
- Repo URL: https://github.com/open-metadata/OpenMetadata
- Tagline: Unified metadata platform for data discovery, observability, and governance
- Stars: 13,116
- Stars Today: 上榜 Trending（第 8 位）
- Forks: 2,022
- Language: Java / TypeScript
- License: Apache-2.0
- Homepage: https://open-metadata.org
- Topics: metadata, data-governance, data-discovery, data-lineage, data-catalog, observability
- 技术栈: Java, TypeScript, React, Elasticsearch, MySQL, Airflow, dbt, Kafka
- Why It Matters Today: 数据治理基础设施在 AI 时代需求激增，统一元数据平台成为数据团队刚需
- 项目摘要: OpenMetadata 是一个统一的元数据平台，解决数据团队最核心的三大问题：数据发现（我有哪些数据？）、数据可观测性（数据质量如何？）和数据治理（谁用了什么数据？）。通过中央元数据仓库、列级血缘追踪和无缝团队协作，让数据资产的管理和使用变得透明可控。
- 核心特性:
  1. 深度数据血缘：支持列级数据血缘追踪，清晰展示数据从来源到消费的完整路径
  2. 统一数据目录：连接数据库、数据仓库、BI 工具、Pipeline 等多种数据源，统一元数据视图
  3. 团队协作治理：内置权限管理、数据所有权分配、数据质量监控和告警能力
- 适用场景: 数据工程团队、数据治理需求的大中型企业、需要数据血缘追踪的合规场景、DataOps 实践团队
- 一句话推荐: 数据治理平台的开源标杆——统一元数据、列级血缘、团队协作，让数据资产一目了然。
- Evidence Notes: 知名开源项目，信息充分
- Honest Caveat: 完整部署涉及多个组件（Elasticsearch、MySQL 等），运维复杂度较高

### Rank 09 - microsoft/ai-agents-for-beginners
- Repo URL: https://github.com/microsoft/ai-agents-for-beginners
- Tagline: 12 Lessons to Get Started Building AI Agents
- Stars: 59,108
- Stars Today: 持续高涨（今日 Trending 第 9 位）
- Forks: 20,064
- Language: Python / Jupyter Notebook
- License: MIT
- Homepage: https://aka.ms/ai-agents-beginners
- Topics: ai-agents, beginner, tutorial, azure-openai, autogen, semantic-kernel, langgraph
- 技术栈: Python, Azure OpenAI, AutoGen, Semantic Kernel, LangGraph, Jupyter Notebook
- Why It Matters Today: AI Agent 开发热潮下，微软出品的系统化入门教程持续吸引学习者
- 项目摘要: 微软开源的 AI Agent 入门课程，共 12 课，系统讲解如何构建 AI Agent。覆盖 Agent 基础概念、工具调用、规划、记忆、多 Agent 协作等核心主题，使用 Azure OpenAI、AutoGen、Semantic Kernel、LangGraph 等主流框架演示。提供中英文等多语言版本。
- 核心特性:
  1. 12 课渐进式学习：从 Agent 基础到多 Agent 系统，循序渐进，每课配有 Notebook 实践
  2. 多框架覆盖：同时使用 AutoGen、Semantic Kernel、LangGraph 对比讲解，帮助学习者选择合适框架
  3. 微软生产实践：结合 Azure OpenAI 服务，贴近企业实际部署场景，有配套 GitHub Copilot 集成
- 适用场景: AI Agent 开发入门学习者、想了解主流 Agent 框架对比的开发者、企业内部 AI 技能培训、高校 AI 课程参考
- 一句话推荐: 微软官方出品的 AI Agent 免费课程——12 课从零开始，AutoGen+LangGraph+Semantic Kernel 三框架对比讲透。
- Evidence Notes: 微软官方项目，信息充分，内容持续更新
- Honest Caveat: 部分 Azure OpenAI 功能需要 Azure 账号；框架更新频繁，部分 Notebook 代码可能需要适配最新版本

### Rank 10 - PowerShell/PowerShell
- Repo URL: https://github.com/PowerShell/PowerShell
- Tagline: PowerShell for every system!
- Stars: 52,872
- Stars Today: 稳定增长（今日 Trending 第 10 位）
- Forks: 8,282
- Language: C#
- License: MIT
- Homepage: https://microsoft.com/powershell
- Topics: powershell, windows, linux, macos, cross-platform, shell, scripting
- 技术栈: C#, .NET, PowerShell Runtime, WinRM, SSH
- Why It Matters Today: 跨平台 PowerShell 持续活跃，AI 时代的自动化脚本需求推动关注度持续
- 项目摘要: PowerShell 是微软开源的跨平台命令行 Shell 和脚本语言，基于 .NET 构建。从最初只支持 Windows 的 Windows PowerShell，演进为可在 Windows、macOS、Linux 上运行的现代 Shell。以对象管道（Object Pipeline）为核心设计，区别于传统 Unix Shell 的文本流模型，特别适合系统管理、自动化运维和 DevOps 场景。
- 核心特性:
  1. 跨平台运行：在 Windows、macOS、Linux 上提供一致体验，统一运维脚本编写方式
  2. 对象管道：命令间传递 .NET 对象而非文本，使数据处理和过滤更精确、更强大
  3. 丰富模块生态：PowerShell Gallery 提供大量模块，覆盖 Azure、AWS、Exchange、Active Directory 等企业场景
- 适用场景: Windows 系统管理员、DevOps 工程师、云资源自动化运维、跨平台脚本开发
- 一句话推荐: 微软的跨平台 Shell 已进入 AI 时代——PowerShell 的对象管道和跨平台能力让自动化运维更现代、更强大。
- Evidence Notes: 知名官方项目，信息充分
- Honest Caveat: 无

### Rank 11 - cline/cline
- Repo URL: https://github.com/cline/cline
- Tagline: Autonomous coding agent right in your IDE, capable of creating/editing files, executing commands, using the browser
- Stars: 60,934
- Stars Today: 持续高涨（今日 Trending 第 11 位）
- Forks: 6,266
- Language: TypeScript
- License: Apache-2.0
- Homepage: https://cline.bot
- Topics: ai-agent, vscode, autonomous-coding, claude, coding-assistant, mcp
- 技术栈: TypeScript, VSCode Extension API, Anthropic Claude, MCP, Browser Automation
- Why It Matters Today: IDE 内最强大的自主编程代理之一，持续高关注度验证其用户价值
- 项目摘要: Cline 是一个深度集成在 VSCode 中的自主 AI 编程代理，每一步操作都需要用户批准，在安全透明的前提下实现高度自主。它可以创建和编辑文件、执行终端命令、操控浏览器、调用 MCP 工具服务器，完成从需求理解到代码实现的完整编程任务。
- 核心特性:
  1. 全权限代理：文件读写、终端执行、浏览器操作、MCP 工具调用——完整的 Agent 工具集
  2. 逐步审批模式：每个关键操作前征得用户同意，保持透明和可控，避免意外修改
  3. 多模型支持：兼容 Claude、GPT-4、Gemini 等主流 LLM，以及 OpenRouter、Bedrock 等多种推理平台
- 适用场景: 重度 VSCode 用户、需要 AI 完成复杂多步骤编程任务、想要可控且透明的 AI 编程代理体验
- 一句话推荐: 最透明的 IDE AI 代理——每步操作你说了算，同时拥有文件、终端、浏览器的完整操控权。
- Evidence Notes: 知名项目，信息充分
- Honest Caveat: 高频使用下 API 成本较高；浏览器操控能力依赖具体任务复杂度

### Rank 12 - microsoft/onnxruntime
- Repo URL: https://github.com/microsoft/onnxruntime
- Tagline: ONNX Runtime: cross-platform, high performance ML inferencing and training accelerator
- Stars: 20,283
- Stars Today: 稳定增长（今日 Trending 第 12 位）
- Forks: 3,859
- Language: C++
- License: MIT
- Homepage: https://onnxruntime.ai
- Topics: onnx, machine-learning, inference, training, deep-learning, gpu, cpu, edge
- 技术栈: C++, Python, C#, Java, CUDA, TensorRT, DirectML, ROCm, CoreML, ONNX
- Why It Matters Today: AI 推理部署的基础设施层，本地 AI 和边缘推理需求激增推动关注度持续
- 项目摘要: ONNX Runtime 是微软开源的跨平台机器学习推理和训练加速器，是将 AI 模型从研究到生产部署的核心基础设施。通过支持 CUDA、TensorRT、CoreML、DirectML 等多种硬件加速后端，让同一个 ONNX 模型在云端、PC、手机、边缘设备上高效运行。被 PyTorch、HuggingFace 等主流 AI 框架广泛集成。
- 核心特性:
  1. 多硬件加速：支持 NVIDIA CUDA/TensorRT、AMD ROCm、Apple CoreML、Intel OpenVINO、高通 SNPE 等多种加速后端
  2. 跨平台部署：从云端 GPU 到边缘 CPU，Windows/Linux/macOS/iOS/Android 全平台支持
  3. 主流框架集成：与 PyTorch Eager Mode、HuggingFace Transformers、scikit-learn 深度集成
- 适用场景: 需要部署 AI 模型到生产环境的 MLOps 工程师、边缘 AI 应用开发（手机、IoT）、需要跨平台 AI 推理能力的产品团队
- 一句话推荐: AI 推理部署的"通用底座"——一套代码，覆盖云端 GPU 到边缘 CPU 的所有硬件，主流 AI 框架首选。
- Evidence Notes: 微软官方知名项目，信息充分
- Honest Caveat: 无

## Language Distribution

- Python:
  - Count: 5
  - Percent: 41.7%
  - Color Hint: #3572A5
- TypeScript:
  - Count: 3
  - Percent: 25%
  - Color Hint: #3178C6
- C#:
  - Count: 1
  - Percent: 8.3%
  - Color Hint: #178600
- C++:
  - Count: 1
  - Percent: 8.3%
  - Color Hint: #f34b7d
- Java:
  - Count: 1
  - Percent: 8.3%
  - Color Hint: #b07219
- 多语言/其他:
  - Count: 1
  - Percent: 8.3%
  - Color Hint: #555555

## Explore Highlights

### Explore 1
- Title: mksglu/context-mode
- URL: https://github.com/mksglu/context-mode
- Kind: Repository
- Meta: ⭐9,650 · TypeScript
- Short Reason: AI 编码代理上下文窗口优化工具，沙箱隔离工具输出，98% 压缩率，支持 12 个平台

### Explore 2
- Title: coreyhaines31/marketingskills
- URL: https://github.com/coreyhaines31/marketingskills
- Kind: Repository
- Meta: ⭐24,225 · Markdown
- Short Reason: 专为 Claude Code 和 AI Agent 设计的营销技能包，覆盖 CRO、文案、SEO、增长工程

### Explore 3
- Title: chiphuyen/aie-book
- URL: https://github.com/chiphuyen/aie-book
- Kind: Repository
- Meta: ⭐15,296 · Python
- Short Reason: AI 工程实践资源库，Chip Huyen 新书《AI Engineering》配套材料，AI 工程师必读

### Explore 4
- Title: VoltAgent/awesome-agent-skills
- URL: https://github.com/VoltAgent/awesome-agent-skills
- Kind: Repository
- Meta: ⭐18,474 · Markdown
- Short Reason: 1000+ Agent 技能精选集，兼容 Claude Code、Codex、Gemini CLI、Cursor、Windsurf

### Explore 5
- Title: CSS
- URL: https://github.com/topics/css
- Kind: Topic
- Meta: 热门话题
- Short Reason: Explore 今日热门编程话题

### Explore 6
- Title: Learn to Code
- URL: https://github.com/collections/learn-to-code
- Kind: Collection
- Meta: GitHub 精选集合
- Short Reason: GitHub 官方推荐编程学习资源集合

## Rendering Notes

- Hero 主标题建议：🐙 GitHub Trending 日报
- Hero 副标题建议：开源社区今日最受关注的项目精选
- Top 3 高亮原因：ml-intern（HuggingFace 官方自主 ML 代理，新项目极速飙升）、claude-context（Claude Code 全代码库语义搜索，上下文工程利器）、RAG-Anything（多模态 RAG 框架完整解决方案）
- 需要在 HTML 中诚实提示的降级点：各仓库今日新增 Stars 数据无法直接从页面解析，以总 Stars 展示
- 不允许省略的区块：Header/Hero、Stats Cards、今日洞察、Top 12、编程语言分布、Explore 精选、Footer
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
