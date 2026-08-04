# GitHub Trending 日报内容底稿

## Meta

- Report Date: 2026-08-04
- Generated At: 2026-08-04 21:05:00 JST
- Output Markdown: `md/github_trending_report_2026-08-04.md`
- Planned HTML: `html/github_trending_report_2026-08-04.html`
- Fixed Base Template: `.codex/skills/skill-github-trending-report/reference/fixedBaseTemplate_2026-03-16.html`
- User Rules: `.codex/skills/skill-github-trending-report/reference/user-rules.md`
- Trending Scope: Repositories / Any language / Today
- Sources:
  - https://github.com/trending?since=daily
  - https://github.com/explore
  - GitHub repository README / About / source / official documentation

## Page Intent

- 今日主线：AI Agent 工程工具继续占据高位，同时 PDF 结构化解析与本地大模型推理这两类“硬工程”项目表现突出。
- 适合谁阅读：AI 应用开发者、终端工具作者、模型推理工程师、数据处理工程师，以及想从热度里筛出真正可研究代码项目的技术负责人。
- 页面重点：严格保留 GitHub Trending 抓取时的原始 Top 12 顺序；累计 Stars、Forks 与 Stars Today 分开呈现。
- 需要诚实降级说明的地方：Stars Today 是 GitHub 动态快照；项目性能、模型质量、安全性与第三方服务可用性均未独立复测。

## Stats

- Trending 项目数：12
- 今日累计新增 Stars：11,353
- 编程语言数：8
- AI 相关项目数：9（编辑分类，不是 GitHub 官方标签）

## Editorial Insights

### Insight 1
- Title: Agent 工具正在从“会聊天”走向“有规矩地干活”
- Body: reverse-skill、Reasonix、Agent-Reach 和 free-claude-code 分别从任务路由、终端编码、外部平台接入和模型访问入口切入。今天的共同主题不是再造一个聊天框，而是把权限、工具、上下文与执行流程真正接起来。

### Insight 2
- Title: PDF 处理先判断“要不要 OCR”，比一股脑全送 OCR 更实用
- Body: pdf-inspector 先分类文本型、扫描型、图片型或混合型 PDF，再对可直接解析的页面提取带位置信息的文本并转成 Markdown。这个思路适合大批量文档管线：贵活留给 OCR，能直接解析的别绕远路。

### Insight 3
- Title: 本地推理开始针对具体模型和硬件做深度特化
- Body: ds4 明确不做通用 GGUF 运行器，而是围绕少数模型、Metal/CUDA/ROCm、KV 状态和 SSD 流式专家加载一起优化。它牺牲通用性换取可控的性能空间，适合研究“专用引擎为什么能快”，不适合拿来当万能模型启动器。

### Insight 4
- Title: 教程与知识库仍有巨大传播力，但不等于可分析的软件系统
- Body: AI-For-Beginners、generative-ai-for-beginners 和 system-design-primer 长期积累的课程与知识结构仍然强势上榜。它们很适合学习和查阅，但本轮架构深挖会把名额留给具有明确运行时、入口和执行链路的项目。

## Top Projects

### Rank 01 - zhaoxuya520/reverse-skill
- Repo URL: https://github.com/zhaoxuya520/reverse-skill
- Tagline: 面向 AI 编码代理的网络安全技能路由包，把 APK、二进制、前端加密、CTF 等任务导向对应方法与工具。
- Stars: 16,700
- Stars Today: 2,446
- Forks: 2,332
- Language: PowerShell
- License: MIT（仓库还包含第三方工具与资料，具体使用时需继续核对各自许可证）
- Homepage: https://github.com/zhaoxuya520/reverse-skill
- Topics: ai-agent, reverse-engineering, cybersecurity, routing, mcp
- 技术栈: PowerShell, Bash, Python, Node.js, Java, Docker, MCP
- Why It Matters Today: 今日增星第一，反映开发者开始把安全研究经验整理成可复用的 Agent 工作流，而不是临场猜命令。
- 项目摘要: 它更像一套“任务分诊台”：先做授权与范围检查，再按任务类型进入对应技能、脚本或 MCP 工具，最后把过程证据和结果沉淀成报告。
- 核心特性:
  1. 通过 `RULES.md`、主路由和场景技能把任务分类、范围确认与执行步骤串起来。
  2. 覆盖 Android、二进制、JS、恶意样本、固件、安全测试等多类场景，并提供工具索引刷新脚本。
  3. 强调时间线、证据链和报告产出，减少 Agent 在高权限任务中“先动手后补手续”。
- 适用场景: 已获得合法授权的逆向工程、漏洞研究、CTF 与安全实验室流程标准化；不适合未经授权的目标操作。
- 一句话推荐: 安全任务工具太多、流程太散时，它能先把路指明白，但方向盘仍得由有授权的人握着。
- Evidence Notes: README 明确给出 `User task → RULES → MASTER-ROUTING → case-init/scope → Scenario skill → tools/MCP/scripts → timeline/report` 路径。
- Honest Caveat: 仓库覆盖面极广，不代表每个外部工具、平台和场景都已在当前环境验证；安全能力必须在明确授权、隔离环境与当地法律允许范围内使用。

### Rank 02 - firecrawl/pdf-inspector
- Repo URL: https://github.com/firecrawl/pdf-inspector
- Tagline: 用 Rust 对 PDF 做类型分类、位置感知文本提取和 Markdown 转换，并给出逐页 OCR 路由建议。
- Stars: 9,005
- Stars Today: 1,699
- Forks: 595
- Language: Rust
- License: MIT
- Homepage: https://github.com/firecrawl/pdf-inspector
- Topics: pdf, rust, text-extraction, markdown, wasm
- 技术栈: Rust, lopdf, PyO3, napi-rs, wasm-bindgen, Rayon
- Why It Matters Today: 文档处理系统常把所有 PDF 都送 OCR；这个项目把快速分类、直接提取和逐页回退组合成更节省成本的前置层。
- 项目摘要: pdf-inspector 读取一次 PDF 文档，在同一份解析结果上完成类型检测、文字与布局提取、表格判断和 Markdown 生成，并标出需要 OCR 的页面及原因。
- 核心特性:
  1. 识别 TextBased、Scanned、ImageBased、Mixed，并返回置信度和需 OCR 页面。
  2. 提取字体、坐标、链接、表单、表格与多栏阅读顺序，输出结构化 Markdown。
  3. 提供 Rust、Python、Node.js 与浏览器 WASM 入口，便于嵌入服务端或本地应用。
- 适用场景: 报告、论文、发票、合同等原生文本 PDF 的本地批处理，以及“先直读、失败再 OCR”的混合文档管线。
- 一句话推荐: 先看看 PDF 里有没有现成文字，再决定要不要请 OCR 上场，省钱也省时间。
- Evidence Notes: `src/lib.rs` 的 `process_pdf_with_options` 只加载一次文档并共享给检测与提取；结果包含 `pages_needing_ocr`、OCR 原因、布局复杂度和编码问题标记。
- Honest Caveat: README 中的速度与质量基准来自项目方公布的特定语料、版本和硬件，本报告未独立复跑；扫描件仍需要外部 OCR。

### Rank 03 - esengine/DeepSeek-Reasonix
- Repo URL: https://github.com/esengine/DeepSeek-Reasonix
- Tagline: 以配置和插件驱动的终端编码 Agent，主打 DeepSeek 前缀缓存与单文件 Go 分发。
- Stars: 30,342
- Stars Today: 883
- Forks: 1,955
- Language: Go
- License: MIT
- Homepage: https://reasonix.io/
- Topics: coding-agent, deepseek, cli, mcp, go
- 技术栈: Go, TOML, Bubble Tea, JSON-RPC, MCP-compatible plugins, OpenAI-compatible providers
- Why It Matters Today: 它把 CLI/TUI、桌面端和编辑器入口收束到同一本地引擎，并显式处理工具权限、会话恢复和长上下文维护。
- 项目摘要: Reasonix 从 `reasonix.toml` 解析模型、工具和插件配置，组装 Agent 控制器，再通过内置工具或 stdio JSON-RPC 插件执行编码任务；同一引擎也服务桌面端和 VS Code 集成。
- 核心特性:
  1. Provider、模型、工具和插件由配置解析，不把某一家模型接口硬编码进业务流程。
  2. 支持一次性 `reasonix run`、交互会话、ACP、MCP、子 Agent 和会话恢复。
  3. 具备权限模式、无头运行防阻塞、事件流、检查点与上下文压缩等工程控制。
- 适用场景: 希望在终端或编辑器内使用可配置编码 Agent，并愿意自行管理模型密钥、工具权限和工作区边界的开发者。
- 一句话推荐: 想要的是能进项目干活的 Agent，而不是只在旁边点评代码，Reasonix 值得顺着运行链路研究。
- Evidence Notes: `cmd/reasonix/main.go` 进入 `internal/cli.Run`；`runAgent` 解析权限、工作区和会话参数，再由 `boot.Build` 组装 Controller，内置 Provider 与工具通过注册表接入。
- Honest Caveat: 项目变化快，模型成本、缓存命中、插件兼容和安全边界取决于具体配置；本报告未连接真实模型端点完成改码任务。

### Rank 04 - TencentCloud/TencentDB-Agent-Memory
- Repo URL: https://github.com/TencentCloud/TencentDB-Agent-Memory
- Tagline: 为个人和团队 Agent 提供聊天记忆、技能、Wiki 与代码图谱的可管理记忆资产平台。
- Stars: 12,565
- Stars Today: 1,090
- Forks: 1,190
- Language: TypeScript
- License: MIT
- Homepage: https://github.com/TencentCloud/TencentDB-Agent-Memory
- Topics: agent-memory, memory-hub, codegraph, wiki, multi-agent
- 技术栈: TypeScript, Node.js, Web UI, Memory Core, Proxy, container deployment
- Why It Matters Today: Agent 记忆正在从“保存聊天记录”升级为带所有权、版本、可见性和装配关系的团队资产。
- 项目摘要: 项目把会话经验提炼成 Chat Memory、Skill、Wiki 和 CodeGraph，并通过 Memory Hub 让人类管理团队、Agent、权限和资产绑定。
- 核心特性:
  1. 将原始会话逐层提炼为可复用记忆，并支持技能版本和资源文件。
  2. 从文档与代码生成 Wiki 和 CodeGraph，帮助 Agent 查阅上下文与影响范围。
  3. 提供 private、team、restricted 等可见性与 ACL，支持团队级资产协作。
- 适用场景: 多 Agent 团队共享项目知识、工作规范和历史决策；需要先完成权限、数据保留和模型服务评估。
- 一句话推荐: Agent 每次上班都像第一天入职时，这套“团队存档”能少交不少重复学费。
- Evidence Notes: README 提供 `memory-core + memory-hub + proxy` 三服务启动方式，并说明 Chat Memory、Skill、Wiki、CodeGraph 与 ACL 资产模型。
- Honest Caveat: 团队记忆涉及代码、文档和会话数据，生产使用前必须评估访问控制、备份、删除、模型供应商数据边界与升级迁移。

### Rank 05 - microsoft/AI-For-Beginners
- Repo URL: https://github.com/microsoft/AI-For-Beginners
- Tagline: 面向初学者的 12 周、24 课人工智能课程，覆盖符号 AI、神经网络、视觉、NLP 与伦理。
- Stars: 61,305
- Stars Today: 1,902
- Forks: 11,910
- Language: Jupyter Notebook
- License: MIT
- Homepage: https://microsoft.github.io/AI-For-Beginners/
- Topics: ai, curriculum, deep-learning, pytorch, tensorflow
- 技术栈: Jupyter Notebook, Python, PyTorch, TensorFlow, OpenCV
- Why It Matters Today: 在工具快速迭代时，成体系的基础课程仍然能吸引大量新学习者，说明“补基本功”没有过时。
- 项目摘要: 一套从人工智能历史、符号推理到神经网络、视觉和 NLP 的入门课程，配有讲义、测验、实验和多语言版本。
- 核心特性:
  1. 课程按周和主题组织，适合自学或课堂教学。
  2. 同时使用 PyTorch 与 TensorFlow 展示核心概念。
  3. 提供可运行 Notebook、实验任务和伦理讨论。
- 适用场景: AI 零基础学习、大学导论课、团队内部基础培训；不适合作为最新模型工程实践的唯一资料。
- 一句话推荐: 想把 AI 基础补成一条线，而不是东看一篇西抄一段，这套课程比较省腿。
- Evidence Notes: README 明确说明 12 周、24 课，以及测验、实验、PyTorch、TensorFlow 和 AI 伦理覆盖。
- Honest Caveat: 课程定位是入门，部分前沿模型与工程框架可能滞后；学习效果取决于是否真正完成 Notebook 与实验。

### Rank 06 - microsoft/generative-ai-for-beginners
- Repo URL: https://github.com/microsoft/generative-ai-for-beginners
- Tagline: 从提示工程、RAG、向量数据库到 Agent 的生成式 AI 入门课程。
- Stars: 115,916
- Stars Today: 775
- Forks: 61,488
- Language: Jupyter Notebook
- License: MIT
- Homepage: https://microsoft.github.io/generative-ai-for-beginners/
- Topics: generative-ai, llm, rag, agents, curriculum
- 技术栈: Python, TypeScript, Jupyter Notebook, Azure/OpenAI-compatible APIs, vector search
- Why It Matters Today: 生成式 AI 学习需求仍然旺盛，尤其是从“会调用模型”过渡到 RAG、工具和 Agent 的完整应用路径。
- 项目摘要: 一套以项目和课程章节组织的生成式 AI 教程，覆盖模型调用、提示、安全、检索增强、函数调用与 Agent 应用。
- 核心特性:
  1. 同时提供概念讲解与代码示例，适合边学边做。
  2. 覆盖从基础提示到检索、向量数据库与 Agent 的渐进路线。
  3. 提供多语言翻译与不同语言实现入口。
- 适用场景: 需要系统学习生成式 AI 应用开发的初学者和培训团队；生产方案仍需结合所选模型、云服务和数据治理单独评估。
- 一句话推荐: 想把“调个接口”升级成能落地的生成式 AI 应用，这套课给了比较完整的台阶。
- Evidence Notes: 仓库公开课程结构和示例覆盖生成式 AI、RAG、向量数据库、函数调用与 Agent。
- Honest Caveat: 示例会依赖外部模型或云服务，费用、限额、版本与地区可用性会变化；课程代码不等同于生产架构。

### Rank 07 - donnemartin/system-design-primer
- Repo URL: https://github.com/donnemartin/system-design-primer
- Tagline: 系统设计面试与分布式系统基础知识库，整理概念、权衡、题目和解题步骤。
- Stars: 360,799
- Stars Today: 237
- Forks: 57,542
- Language: Python
- License: CC BY 4.0
- Homepage: https://github.com/donnemartin/system-design-primer
- Topics: system-design, distributed-systems, interview, scalability
- 技术栈: Markdown, Python examples, diagrams
- Why It Matters Today: 它仍是系统设计学习的高流量入口，说明可检索、可复习的知识地图具有长期价值。
- 项目摘要: 用图示和条目解释缓存、数据库、负载均衡、异步处理、可用性与一致性等概念，并提供常见设计题的分析框架。
- 核心特性:
  1. 把分散的系统设计概念整理为连续学习路径。
  2. 提供典型题目、估算思路和设计权衡。
  3. 适合作为面试复习索引与术语查阅入口。
- 适用场景: 系统设计入门、面试准备和知识查缺补漏；不能替代真实系统的容量规划、故障演练与生产经验。
- 一句话推荐: 它像一张系统设计地图，能告诉你哪儿有山有河，但真修路还得去工地。
- Evidence Notes: 仓库内容以课程式文档、图示和示例为主，不是一个可部署的软件系统。
- Honest Caveat: 许多内容是通用原则，具体技术选型必须结合业务规模、团队能力和故障模型；部分链接与实践可能随时间变化。

### Rank 08 - antirez/ds4
- Repo URL: https://github.com/antirez/ds4
- Tagline: 为 DeepSeek V4 Flash、GLM 5.2 等少数模型深度特化的原生本地推理引擎。
- Stars: 20,474
- Stars Today: 384
- Forks: 1,809
- Language: C
- License: MIT（包含或改编自 GGML/llama.cpp 的 MIT 许可代码与知识）
- Homepage: https://github.com/antirez/ds4
- Topics: inference-engine, deepseek, gguf, metal, cuda
- 技术栈: C, Objective-C/Metal, CUDA, ROCm/HIP, GGUF, HTTP APIs
- Why It Matters Today: 它展示了“少模型、少硬件组合、整条链一起优化”的专用推理系统路线。
- 项目摘要: ds4 将模型加载、提示渲染、KV 状态、推理后端、HTTP 服务和编码 Agent 放在同一仓库中，以模型特化换取性能与工程可控性。
- 核心特性:
  1. 支持 Metal、CUDA 和 ROCm，并提供多 GPU、张量并行、流水线并行等路径。
  2. 在内存不足时可把路由专家权重留在 SSD，通过缓存按需加载。
  3. 提供 CLI、服务器、基准、评测与 Agent 二进制，支持工具调用和会话 KV 管理。
- 适用场景: 高内存个人工作站或专用推理服务器上的模型研究、性能实验与局域网服务；不适合任意 GGUF 模型即插即用。
- 一句话推荐: 它不是瑞士军刀，是给几种模型磨得很快的一把专用刀。
- Evidence Notes: README 明确说明其非通用 GGUF runner；Makefile 将 `ds4.c`、后端、SSD、分布式、server、agent 和 KV store 分别构建为多个二进制。
- Honest Caveat: 项目自称 beta 且变化很快；硬件需求高，性能数字由项目方在特定模型与设备上测得，本报告未复测。

### Rank 09 - shiyu-coder/Kronos
- Repo URL: https://github.com/shiyu-coder/Kronos
- Tagline: 面向金融 K 线序列的基础模型与研究代码。
- Stars: 35,917
- Stars Today: 200
- Forks: 5,975
- Language: Python
- License: MIT
- Homepage: https://github.com/shiyu-coder/Kronos
- Topics: finance, time-series, foundation-model, forecasting
- 技术栈: Python, PyTorch, time-series modeling, pretrained weights
- Why It Matters Today: 金融时序基础模型持续吸引关注，但模型预测效果与实际交易价值之间仍隔着数据、成本和风险控制三座山。
- 项目摘要: 项目围绕金融 K 线序列预训练模型，提供模型、推理与研究材料，用于预测或表征金融时间序列。
- 核心特性:
  1. 针对开高低收量等金融序列设计训练与推理流程。
  2. 提供预训练模型与示例，降低研究复现门槛。
  3. 面向多市场和多频率场景探索通用时序表征。
- 适用场景: 学术研究、离线回测和特征实验；不应在未做独立验证、成本建模和风控前直接用于真实资金决策。
- 一句话推荐: 可以拿来研究金融序列表示，别把一张漂亮回测图当提款机说明书。
- Evidence Notes: 仓库公开内容以模型、训练/推理代码和研究资料为主。
- Honest Caveat: 历史表现不能保证未来收益；数据泄漏、交易成本、滑点、市场制度变化与模型漂移都可能显著影响结果。

### Rank 10 - Panniantong/Agent-Reach
- Repo URL: https://github.com/Panniantong/Agent-Reach
- Tagline: 为 AI Agent 安装和诊断网页、视频、社交平台等外部信息访问能力。
- Stars: 66,118
- Stars Today: 1,057
- Forks: 5,481
- Language: Python
- License: MIT
- Homepage: https://github.com/Panniantong/Agent-Reach
- Topics: agent, tools, web, mcp, automation
- 技术栈: Python, CLI, external platform adapters, cookies, MCP/tool integrations
- Why It Matters Today: Agent 的瓶颈常常不是“不会想”，而是拿不到网页、视频或平台内容；Agent-Reach 把安装、检测与备用方案做成工具链。
- 项目摘要: 它通过命令行安装不同平台的访问后端，并用 Doctor 检查依赖、登录态和可用性，让 Agent 能按场景选择抓取或搜索入口。
- 核心特性:
  1. 为多类公开平台提供安装与调用适配。
  2. 通过诊断命令发现缺失依赖、Cookie 或后端故障。
  3. 支持首选后端不可用时切换到备选路径。
- 适用场景: 在遵守网站条款、版权和访问授权的前提下，为研究型 Agent 补充公开信息获取能力。
- 一句话推荐: Agent 想得再明白，门口没钥匙也进不去；它管的是钥匙串和门锁体检。
- Evidence Notes: 仓库 README 与命令说明公开了安装、平台能力和诊断流程；该项目已在 2026-08-03 日报中完成独立架构分析。
- Honest Caveat: 第三方平台接口、Cookie、地区限制与风控经常变化，能安装不代表长期可用；必须遵守目标平台规则。

### Rank 11 - Alishahryar1/free-claude-code
- Repo URL: https://github.com/Alishahryar1/free-claude-code
- Tagline: 把 Claude Code 请求转发到其他 OpenAI-compatible 或免费额度模型端点的代理与配置工具。
- Stars: 44,197
- Stars Today: 278
- Forks: 7,282
- Language: Python
- License: MIT
- Homepage: https://github.com/Alishahryar1/free-claude-code
- Topics: claude-code, proxy, openai-compatible, llm
- 技术栈: Python, HTTP proxy, model-provider adapters, CLI configuration
- Why It Matters Today: 开发者希望复用 Claude Code 工作流，同时降低模型费用或切换供应商，代理层因此受到关注。
- 项目摘要: 项目通过本地代理和配置映射，把 Claude Code 的模型请求导向兼容端点，并处理模型名、认证和请求格式差异。
- 核心特性:
  1. 提供快速安装和 Provider 配置入口。
  2. 兼容多种模型服务或免费额度方案。
  3. 让现有 Claude Code 交互方式尽量保持不变。
- 适用场景: 个人实验、兼容性测试和成本敏感的非关键开发任务；企业代码与敏感数据使用前必须审查代理与供应商边界。
- 一句话推荐: 它能帮 Claude Code 换“油站”，但油品、账单和数据去哪儿了得自己看清楚。
- Evidence Notes: 仓库公开说明其本地代理和多 Provider 适配定位。
- Honest Caveat: 第三方免费额度、接口兼容和服务条款可能随时变化；不得假设替代端点与原服务在隐私、能力和稳定性上等价。

### Rank 12 - iv-org/invidious
- Repo URL: https://github.com/iv-org/invidious
- Tagline: 轻量、注重隐私的 YouTube 替代前端。
- Stars: 22,335
- Stars Today: 402
- Forks: 2,487
- Language: Crystal
- License: AGPL-3.0
- Homepage: https://invidious.io/
- Topics: youtube, privacy, alternative-frontend, crystal
- 技术栈: Crystal, Kemal-style web stack, PostgreSQL, HTML, HTTP upstream integration
- Why It Matters Today: 用户仍然需要更轻量、少追踪、可自托管的内容访问前端。
- 项目摘要: Invidious 接收用户的视频浏览和搜索请求，从 YouTube 上游解析必要数据，再以自有页面和 API 返回，减少官方前端的脚本与追踪依赖。
- 核心特性:
  1. 提供搜索、观看、订阅等替代界面与公开 API。
  2. 支持自托管与多实例部署。
  3. 尽量减少广告、追踪与重量级客户端脚本。
- 适用场景: 希望自托管隐私友好视频前端的个人或社区；运维者需持续跟进上游变化和法律、版权要求。
- 一句话推荐: 想给 YouTube 套一个轻一点、少盯人的壳，它是老牌选择，但上游一改门锁它也得连夜配钥匙。
- Evidence Notes: 仓库提供 Crystal Web 应用、配置、数据库迁移与上游解析代码；该项目已在 2026-08-02 日报中完成独立架构分析。
- Honest Caveat: 高度依赖 YouTube 未承诺稳定的上游行为，实例可用性与合规风险因地区、配置和流量而异。

## Language Distribution

- Python:
  - Count: 5
  - Percent: 41.7%
  - Color Hint: `#3572A5`
- Jupyter Notebook:
  - Count: 2
  - Percent: 16.7%
  - Color Hint: `#DA5B0B`
- PowerShell:
  - Count: 1
  - Percent: 8.3%
  - Color Hint: `#012456`
- Rust:
  - Count: 1
  - Percent: 8.3%
  - Color Hint: `#DEA584`
- Go:
  - Count: 1
  - Percent: 8.3%
  - Color Hint: `#00ADD8`
- TypeScript:
  - Count: 1
  - Percent: 8.3%
  - Color Hint: `#3178C6`
- C:
  - Count: 1
  - Percent: 8.3%
  - Color Hint: `#555555`
- Crystal:
  - Count: 1
  - Percent: 8.3%
  - Color Hint: `#000100`

## Explore Highlights

GitHub Explore 获取成功，但“Popular repositories today”与 Trending 高度重合。以下作为补充入口，不参与 Trending 排名或 Stars Today 统计。

### Explore 1
- Title: lyogavin/airllm
- URL: https://github.com/lyogavin/airllm
- Kind: Popular repository
- Meta: Python · 大模型低显存推理
- Short Reason: 通过分层加载等方式降低本地运行大模型的显存门槛。

### Explore 2
- Title: livekit/agents
- URL: https://github.com/livekit/agents
- Kind: Popular repository
- Meta: Python · 实时语音/视频 Agent
- Short Reason: 将实时媒体管线与 Agent 工作流结合，适合关注低延迟多模态交互的开发者。

### Explore 3
- Title: usekaneo/kaneo
- URL: https://github.com/usekaneo/kaneo
- Kind: Popular repository
- Meta: TypeScript · 开源项目管理
- Short Reason: 自托管任务与项目协作工具，适合寻找轻量 Jira/Linear 替代方案的团队。

### Explore 4
- Title: jamiepine/voicebox
- URL: https://github.com/jamiepine/voicebox
- Kind: Popular repository
- Meta: TypeScript · 本地语音工具
- Short Reason: 关注本地语音生成和桌面工作流，属于今日榜单外的工程补充。

### Explore 5
- Title: zhaoxuya520/reverse-skill
- URL: https://github.com/zhaoxuya520/reverse-skill
- Kind: Popular repository
- Meta: PowerShell · Agent 安全技能路由
- Short Reason: 同时出现在 Trending 与 Explore，说明其任务路由主题获得集中关注。

### Explore 6
- Title: firecrawl/pdf-inspector
- URL: https://github.com/firecrawl/pdf-inspector
- Kind: Popular repository
- Meta: Rust · PDF 分类与结构化提取
- Short Reason: 同时出现在两处入口，且代码系统完整，入选本日源码深挖。

## Rendering Notes

- Hero 主标题建议：GitHub Trending 日报 · 2026-08-04
- Hero 副标题建议：Agent 工具继续升温，PDF 解析与专用本地推理冒出硬核新项目
- Top 3 高亮原因：严格对应 GitHub Trending 原始排名前三，不按累计 Stars 或编辑偏好重排。
- 需要在 HTML 中诚实提示的降级点：Stars Today 为动态快照；Explore 与 Trending 高度重合；所有性能与模型效果均未独立复测。
- 不允许省略的区块：Header / Hero、4 张 Stats Cards、今日洞察、原始 Top 12、语言分布、Explore、Footer。
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

## Markdown Gate 验收

- [x] 报告日期为 2026-08-04（Asia/Tokyo）。
- [x] GitHub Trending 原始 Top 12 数量完整、顺序未改。
- [x] 累计 Stars、Forks、Stars Today 分开记录。
- [x] 12 个项目均包含固定字段、Evidence Notes 与 Honest Caveat。
- [x] 语言分布合计 12 个项目。
- [x] Explore 获取成功并明确作为补充，不参与排名统计。
- [x] Rendering Notes 与固定模板映射要求完整。
- [x] 未把项目方性能、模型效果或服务稳定性宣传当成独立验证结论。
