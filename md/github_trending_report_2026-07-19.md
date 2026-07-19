# GitHub Trending 日报内容底稿

## Meta

- Report Date: 2026-07-19
- Generated At: 2026-07-19 21:16 JST
- Output Markdown: `md/github_trending_report_2026-07-19.md`
- Planned HTML: `html/github_trending_report_2026-07-19.html`
- Fixed Base Template: `.codex/skills/skill-github-trending-report/reference/fixedBaseTemplate_2026-03-16.html`
- User Rules: `.codex/skills/skill-github-trending-report/reference/user-rules.md`
- Sources:
  - https://github.com/trending?since=daily
  - https://github.com/explore
  - Top 项目的 GitHub 仓库页、README、依赖清单、官方文档和必要源码

## Page Intent

- 今日主线：今天榜单一头连着“从零学习”，一头连着“让 Agent 真干活”。榜首是流式三维重建模型，增星冠军却是老牌学习索引；中段则集中出现语义标准、代码图、网页研究 MCP、低显存推理和终端 Agent。
- 适合谁阅读：希望快速判断当天开源热点、寻找 AI 工程工具、评估项目成熟度和源码研究价值的开发者、架构师与技术负责人。
- 页面重点：严格保留 GitHub 官方返回的 11 个仓库顺序，累计 Stars 与 Stars Today 分开呈现；固定模板需要 12 个展开位，因此额外放入一个明确标为 `E1` 的 Explore 补充项，它不参与排名和统计。
- 需要诚实降级说明的地方：GitHub Trending 本次只返回 11 个仓库；模型速度、低显存能力、Token 节省、搜索质量和课程规模均以项目方公开资料为证据，没有在本报告中独立复测。

## Stats

- Trending 项目数：11
- 今日累计新增 Stars：3,509
- 编程语言数：4
- AI 相关项目数：9

## Editorial Insights

### Insight 1
- Title: 🗺️ 流式三维重建登顶，重点从“拍完再算”转向“边走边建图”
- Body: `Robbyant/lingbot-map` 以 831 Stars Today 排名第一。它不是把所有帧攒齐后再做全局优化，而是用流式 Transformer、关键帧和 KV Cache 持续更新场景表示。对机器人、长视频和大尺度空间建模很有吸引力，不过约 20 FPS 与 SOTA 都是官方结果，先别拿宣传海报当显卡验收单。

### Insight 2
- Title: 📚 今日增星冠军还是“自己造一个 X”，基础功又回来抢镜
- Body: `build-your-own-x` 一天新增 1,126 Stars，是榜单增速最高项目。它说明大家一边用 Agent 写代码，一边又开始补数据库、编译器、容器、浏览器这些底层原理。好处是学习路径丰富；边界也很清楚：它是教程索引，不是一个可部署的软件系统，不能给目录画微服务图。

### Insight 3
- Title: 🔌 Agent 工具开始围着协议、上下文和本地数据打磨
- Body: `code-review-graph` 用结构图减少代码审查时的无效上下文，`wigolo` 把搜索、抓取、爬取和研究封装成 MCP，`kimi-cli` 则把工具调用、终端操作和 ACP/MCP 接入放进一个 CLI Agent。今天真正值得看的不是“又一个聊天框”，而是入口、权限、缓存、失败降级和结果回传有没有说清楚。

### Insight 4
- Title: 🧱 标准化与低显存推理同时升温，工程界在补两种地基
- Body: `apache/ossie` 试图统一 AI、BI 与分析工具之间的语义模型，解决同一个指标在不同系统里各说各话；`airllm` 则继续强调分层加载，让超大模型在小显存设备上运行。一个治理“数据含义”，一个治理“显存账本”，都很实用，也都需要在真实环境里验证兼容性和性能代价。

## Top Projects

### Rank 01 - Robbyant/lingbot-map
- Repo URL: https://github.com/Robbyant/lingbot-map
- Tagline: 面向流式图像或视频的前馈式三维场景重建基础模型。
- Stars: 13,249
- Stars Today: 831
- Forks: 1,372
- Language: Python
- License: Apache-2.0
- Homepage: https://technology.robbyant.com/lingbot-map
- Topics: 3d-reconstruction, computer-vision, transformer, streaming-inference, robotics
- 技术栈: Python, PyTorch, Geometric Context Transformer, FlashInfer/SDPA, OpenCV, Viser, ONNX Runtime
- Why It Matters Today: 排名第一且新增 831 Stars，把长序列三维重建的实时性、缓存策略和大场景漂移问题推到当天技术焦点。
- 项目摘要: LingBot-Map 从图片文件夹或视频帧持续预测相机位姿、深度和世界点云。核心 Geometric Context Transformer 把锚点上下文、位姿参考窗口和轨迹记忆放进同一条流式链路，并通过关键帧与分页 KV Cache 控制长序列成本。
- 核心特性:
  1. 支持逐帧 streaming 与重叠窗口 windowed 两种推理模式，面向短序列和超长序列分别处理。
  2. 可自动选择关键帧间隔，并支持 CPU offload、FlashInfer 或 PyTorch SDPA 后端。
  3. 提供浏览器三维查看器、天空分割遮罩和离线批量渲染管线。
- 适用场景: 机器人或移动设备采集后的三维建图研究、长视频空间重建、算法评测与可视化；没有 CUDA 环境、需要轻量移动端部署或要求商业生产 SLA 的团队应先做硬件和许可证评估。
- 一句话推荐: 它像一边走路一边搭地图，不必等整趟旅程结束再开工；但路况好不好，还得拿你的相机和显卡亲自跑一圈。
- Evidence Notes: GitHub Trending 原始排名与增星；README 的 GCT、KV Cache、安装、Quick Start、长序列模式；`demo.py` 的输入、模型加载、推理、后处理和 Viser 链路；`pyproject.toml` 依赖。
- Honest Caveat: 约 20 FPS、超过 10,000 帧和基准领先均为维护者披露，未独立复测；模型权重、CUDA、显存和输入域差异会显著影响结果。

### Rank 02 - apache/ossie
- Repo URL: https://github.com/apache/ossie
- Tagline: 在数据分析、AI 与 BI 工具之间交换统一语义模型的开放规范。
- Stars: 1,342
- Stars Today: 47
- Forks: 157
- Language: Python
- License: Apache-2.0
- Homepage: https://ossie.apache.org/
- Topics: metadata, semantic, semantic-layer, analytics, business-intelligence
- 技术栈: JSON/YAML, JSON Schema, Python, Java, converters, validation tooling
- Why It Matters Today: 数据工具越多，指标口径越容易“一个部门一套算法”；Ossie 上榜说明语义互操作正从厂商功能变成行业级基础问题。
- 项目摘要: Apache Ossie 是孵化中的开放规范，目标是让 AI Agent、BI 平台和分析系统读写同一套业务指标、维度、关系与语义定义。仓库不只放规范文档，还包含机器可读 Schema、转换器、验证工具和示例模型。
- 核心特性:
  1. 用 JSON/YAML 规范和 Schema 表达可跨工具交换的语义模型。
  2. 提供面向 dbt、GoodData、Polaris、Salesforce 等格式的参考转换器。
  3. 提供验证工具与 TPC-DS 示例，便于实现方测试兼容性。
- 适用场景: 数据平台厂商、BI 工具、语义层产品和需要让 Agent 理解统一业务口径的企业；短期只用单一 BI 工具且没有跨系统治理需求的团队，收益可能有限。
- 一句话推荐: 它想给“营收到底怎么算”办一张通用身份证，省得每个系统见面先对半天暗号。
- Evidence Notes: GitHub Trending；Apache 仓库 README 的规范定位、core-spec、converters、examples、validation 与 Apache-2.0 许可。
- Honest Caveat: 项目仍处 Apache 孵化和规范演进阶段；跨厂商采用度、版本兼容和治理流程尚需结合实际生态验证。

### Rank 03 - PostHog/posthog
- Repo URL: https://github.com/PostHog/posthog
- Tagline: 把产品分析、回放、实验、特性开关、错误、日志和 AI 可观测性放进同一平台。
- Stars: 36,731
- Stars Today: 338
- Forks: 3,037
- Language: Python
- License: MIT（`ee` 目录另有许可）
- Homepage: https://posthog.com
- Topics: analytics, session-replay, feature-flags, experiments, error-tracking, ai-observability
- 技术栈: Python, TypeScript/React, event ingestion, analytics pipelines, SDK, API, MCP
- Why It Matters Today: 新增 338 Stars，说明产品数据平台正在从“给人看报表”扩展到“给 Agent 足够上下文去诊断和修复”。
- 项目摘要: PostHog 将用户行为事件、会话回放、实验、功能开关、错误和日志统一到产品上下文中，并通过 Web、Slack、桌面端和 MCP 等入口供人或 Agent 操作。它既有开源自托管代码，也有云服务与企业能力。
- 核心特性:
  1. 产品分析、回放、实验、开关、错误和日志共享同一用户与事件上下文。
  2. 多语言 SDK、API 和 MCP 便于把采集、查询和自动化接入现有应用。
  3. 支持自托管，但官方对规模、运维和不同版本能力给出了明确边界。
- 适用场景: 产品增长分析、实验平台、线上问题复盘、LLM/Agent 观测；大规模生产自托管需要专门的数据管线、容量和运维评估。
- 一句话推荐: 像把产品数据、录像和故障单搬进同一间值班室，Agent 想查案不用再挨个楼层找档案。
- Evidence Notes: GitHub Trending；官方 README、产品模块、自托管与许可证说明；仓库多产品目录和公开文档。
- Honest Caveat: 云版、开源版和企业目录能力不完全相同；官方容量与自动修复效果不是本报告独立压测或安全审计结论。

### Rank 04 - ibelick/ui-skills
- Repo URL: https://github.com/ibelick/ui-skills
- Tagline: 为设计工程师和编码 Agent 提供可按任务路由的 UI 技能集合。
- Stars: 5,239
- Stars Today: 123
- Forks: 224
- Language: TypeScript
- License: MIT
- Homepage: https://www.ui-skills.com/
- Topics: skills, ui-skills, design-engineering, agent-skills
- 技术栈: TypeScript, Node.js CLI, Astro, Markdown skills, web catalog
- Why It Matters Today: 新增 123 Stars，反映团队开始把 UI 质量要求从一句 Prompt 拆成可检索、可组合、可执行的技能模块。
- 项目摘要: UI Skills 提供一套面向设计工程任务的技能库和 CLI。`npx ui-skills start` 会根据当前任务把 Agent 路由到合适的技能集合，也可按分类列出或获取具体技能。
- 核心特性:
  1. 用 CLI 浏览、筛选和加载 UI 技能，减少每次手工拼 Prompt。
  2. 技能按 motion、baseline UI 等任务维度组织，适合渐进式采用。
  3. 提供网站目录与版本发布，便于查阅和更新。
- 适用场景: 使用 Claude Code、Codex、Cursor 等工具做界面设计和前端实现的团队；品牌级设计、无障碍验收和真实用户研究仍需专业人员负责。
- 一句话推荐: 它给 Agent 发的是“设计工种说明书”，不是一张万能审美证；规矩能少走弯路，品味还得有人把关。
- Evidence Notes: GitHub Trending；仓库 README 的 CLI 命令、技能定位、网站和 MIT 许可证。
- Honest Caveat: 技能规则能改善流程一致性，但不能保证生成页面的审美、可用性或业务转化效果。

### Rank 05 - rohitg00/ai-engineering-from-scratch
- Repo URL: https://github.com/rohitg00/ai-engineering-from-scratch
- Tagline: 从数学、模型到 Agent、MCP 和生产工程的开放式 AI 课程与练习体系。
- Stars: 39,282
- Stars Today: 191
- Forks: 6,570
- Language: Python
- License: MIT
- Homepage: https://aiengineeringfromscratch.com
- Topics: ai-engineering, llm, agents, mcp, machine-learning, education
- 技术栈: Markdown, Python, TypeScript, Rust, Julia, static site, reusable prompts/skills/agents
- Why It Matters Today: 新增 191 Stars，说明“会调 API”已经不够，开发者希望从注意力机制一路补到 Agent 与生产系统。
- 项目摘要: 这是一个按 20 个阶段组织的 AI 工程课程仓库，维护者称包含 503 节内容，覆盖数学、训练、推理、RAG、Agent、MCP 和多语言工程。每节强调产出可复用的代码、Prompt、Skill 或服务。
- 核心特性:
  1. 从基础数学和模型原理逐步推进到生产 Agent 与系统设计。
  2. 同时使用 Python、TypeScript、Rust 和 Julia，展示不同工程取舍。
  3. 仓库包含课程、项目、站点和输出物，适合边学边做。
- 适用场景: 系统补齐 AI 工程知识、带教、内部训练营和自学路线规划；不适合作为经过同行评审的标准教材或生产组件直接引入。
- 一句话推荐: 这是一条很长的 AI 健身计划，器械挺全；别收藏完就当练过，肌肉不会靠 Star 自动长出来。
- Evidence Notes: GitHub Trending；README 的 503 lessons、20 phases、四种语言、课程结构和 MIT 许可。
- Honest Caveat: 课程规模、阅读量和学习收益为维护者自述；不同章节深度与时效需要读者逐项判断。

### Rank 06 - tirth8205/code-review-graph
- Repo URL: https://github.com/tirth8205/code-review-graph
- Tagline: 为 MCP 与 CLI 构建本地持久化代码关系图，缩小 AI 审查所需上下文。
- Stars: 20,373
- Stars Today: 355
- Forks: 2,135
- Language: Python
- License: MIT
- Homepage: https://github.com/tirth8205/code-review-graph
- Topics: tree-sitter, mcp, static-analysis, knowledge-graph, code-review, local-first
- 技术栈: Python, Tree-sitter, SQLite, graph traversal, MCP, CLI, Git hooks
- Why It Matters Today: 新增 355 Stars，继续证明“让模型少读无关代码”是 Agent 工程里比单纯加长上下文更现实的降本方向。
- 项目摘要: code-review-graph 用 Tree-sitter 解析代码结构，将定义、调用和依赖关系写入本地持久化图，并通过 CLI/MCP 回答影响半径、调用链和改动相关上下文。增量更新避免每次从头扫描整个仓库。
- 核心特性:
  1. 为多语言仓库构建可持续更新的结构关系图。
  2. 提供影响分析、调用路径和相关测试等面向审查的查询。
  3. 可自动安装到多种 AI 编码工具，并注入 MCP 配置与规则。
- 适用场景: 大型代码库审查、重构影响分析、为 Agent 提供精准上下文；动态调用、反射或未支持语言仍需人工补证。
- 一句话推荐: 它先给代码库画张地铁图，再让 Agent 查路线，免得每次出门都把整座城翻一遍。
- Evidence Notes: GitHub Trending；README 的 Tree-sitter、增量图、MCP、安装与基准复现说明；前一日已完成独立架构分析。
- Honest Caveat: Token 缩减和基准数据为项目方测试结果；静态图不能完整覆盖所有运行时行为。

### Rank 07 - elder-plinius/G0DM0D3
- Repo URL: https://github.com/elder-plinius/G0DM0D3
- Tagline: 面向红队、认知研究和多模型比较的开源聊天界面。
- Stars: 9,604
- Stars Today: 69
- Forks: 2,263
- Language: TypeScript
- License: AGPL-3.0
- Homepage: https://godmod3.ai
- Topics: multi-model-chat, red-teaming, local-models, openrouter, ollama
- 技术栈: TypeScript, React/Next.js, Tailwind CSS, provider APIs, local model runtimes, Docker
- Why It Matters Today: 它把多模型并行、评分和本地模型接入放到同一聊天产品里，适合观察模型差异，也把安全与合规边界摆到了台面上。
- 项目摘要: G0DM0D3 是多模型聊天与实验界面，可连接 OpenRouter、Venice 或 Ollama、LM Studio、llama.cpp、vLLM 等本地运行时。项目强调红队、认知研究和“弱约束”交互，并提供多模型并行与分层评估模式。
- 核心特性:
  1. 同时接入云端和本地模型，支持多模型并行回答与比较。
  2. 提供 GODMODE CLASSIC、ULTRAPLINIAN 等组合和评分流程。
  3. 支持 Docker 与本地模型部署，并公开隐私、安全和服务条款文档。
- 适用场景: 模型红队、提示词研究、输出差异比较和本地模型实验；企业生产、未成年人场景或强合规业务不应未经治理直接使用。
- 一句话推荐: 它像把一群性格各异的模型请进同一间辩论室；热闹是真热闹，门口的安全员也不能请假。
- Evidence Notes: GitHub Trending；README 的多供应商、本地模型、多模型评估、Docker、AGPL 和项目定位。
- Honest Caveat: “liberated”定位伴随明显内容安全、供应商条款和数据隐私风险；项目功能描述不等于适合所有组织使用。

### Rank 08 - lyogavin/airllm
- Repo URL: https://github.com/lyogavin/airllm
- Tagline: 通过分层加载与卸载，让超大语言模型在小显存 GPU 上执行推理。
- Stars: 23,462
- Stars Today: 161
- Forks: 2,664
- Language: Jupyter Notebook
- License: Apache-2.0
- Homepage: https://github.com/lyogavin/airllm
- Topics: llm, low-memory-inference, transformers, llama, deepseek, qwen
- 技术栈: Python, PyTorch, Hugging Face Transformers, layer-wise loading, CPU/GPU offload, prefetching
- Why It Matters Today: 新增 161 Stars；随着模型体量继续增长，“能不能在手头设备上跑起来”仍是开发者最直接的成本问题。
- 项目摘要: AirLLM 通过按层加载模型权重、计算后释放并预取后续层，把显存占用压到远低于完整模型权重大小。官方宣称可在 4GB GPU 上运行 70B 模型，并在新版本支持 FP8 与更大模型。
- 核心特性:
  1. 不必把整套模型权重同时放进显存，降低峰值 GPU 内存需求。
  2. 支持多类 Hugging Face 模型、CPU 推理、MacOS 和量化配置。
  3. 通过预取与统一 AutoModel 接口简化不同模型的加载方式。
- 适用场景: 低成本模型可行性验证、离线实验和显存受限设备；需要高吞吐、低延迟服务时，应评估磁盘、内存和层间传输开销。
- 一句话推荐: 它不是把大象变小，而是让大象分批进电梯；能上楼，速度和电梯磨损还得另算。
- Evidence Notes: GitHub Trending；README 的分层低显存思路、v3.0 支持、Quick Start 与 Apache-2.0 许可。
- Honest Caveat: 70B/4GB、405B/8GB、671B/12GB 等为项目方声明；实际速度、内存、磁盘和模型兼容性高度依赖环境。

### Rank 09 - KnockOutEZ/wigolo
- Repo URL: https://github.com/KnockOutEZ/wigolo
- Tagline: 给 AI 编码 Agent 使用的本地优先网页搜索、抓取、爬取和研究 MCP 服务。
- Stars: 1,438
- Stars Today: 203
- Forks: 93
- Language: TypeScript
- License: AGPL-3.0-only
- Homepage: https://github.com/KnockOutEZ/wigolo
- Topics: mcp, web-search, web-scraping, local-first, ai-agent, research
- 技术栈: TypeScript, Node.js 20+, MCP SDK, SQLite/sqlite-vec, Playwright, Readability/Defuddle, local embeddings, REST
- Why It Matters Today: 新增 203 Stars且处于公开测试阶段，显示开发者希望把 Agent 的网页研究能力掌握在本机，而不是每次查询都交给计费 API。
- 项目摘要: wigolo 以单个 Node 进程提供 MCP stdio 服务，并可启用 REST。它将搜索引擎聚合、HTTP/浏览器抓取、正文提取、本地缓存、向量相似检索、研究和 Agent 工具封装在一起，核心路径无需 API Key。
- 核心特性:
  1. 提供 search、fetch、crawl、extract、cache、find_similar、research、agent 等工具。
  2. 使用多搜索后端、路由降级、浏览器池和本地缓存应对公开网页的不稳定性。
  3. 数据保存在 `~/.wigolo`，支持 MCP、REST、Docker 与 TypeScript/Python SDK。
- 适用场景: 本地编码 Agent 查文档、抓网页、做轻量研究或构建私有搜索缓存；高并发爬取、严格法律审查和企业级 SLA 仍需额外治理。
- 一句话推荐: 它给 Agent 配了一间本地资料室，查书不用次次刷卡；不过公共搜索引擎偶尔关门，这位图书管理员也得学会绕路。
- Evidence Notes: GitHub Trending；README 的工具、安装、架构和公开测试说明；`package.json` 的依赖、MCP 元数据和 AGPL；`src/server.ts` 的子系统、工具分发与降级处理。
- Honest Caveat: 搜索质量、成本对比和性能基准为维护者披露；公共搜索引擎规则、网页结构和 robots.txt 会持续变化。

### Rank 10 - codecrafters-io/build-your-own-x
- Repo URL: https://github.com/codecrafters-io/build-your-own-x
- Tagline: 按技术领域整理“从零实现一个 X”的教程索引。
- Stars: 528,522
- Stars Today: 1,126
- Forks: 50,012
- Language: Markdown
- License: CC0
- Homepage: https://codecrafters.io
- Topics: programming, tutorials, free, awesome-list, tutorial-code
- 技术栈: Markdown, 多语言教程链接, 社区维护索引
- Why It Matters Today: 一天新增 1,126 Stars，为今日增星最高项目；在 AI 自动生成代码的背景下，理解底层系统的需求反而更强。
- 项目摘要: 这是一个按数据库、容器、编译器、操作系统、浏览器、搜索引擎等类别整理的教程清单。它帮助读者通过亲手重建经典系统理解内部原理，本身不包含统一运行时或可部署平台。
- 核心特性:
  1. 覆盖大量技术类别和多种编程语言，入口清晰。
  2. 强调从零实现，适合作为项目式学习路线。
  3. 社区持续提交和审查外部教程链接。
- 适用场景: 系统基础学习、面试准备、课程设计和寻找练手项目；不适合作为生产依赖或完整架构方案。
- 一句话推荐: 这是一座“造轮子图书馆”，目录很厚；借完书还得自己拧螺丝，Star 不负责代工。
- Evidence Notes: GitHub Trending；README 的教程分类、贡献方式、CC0 与项目来源。
- Honest Caveat: 外链教程的质量、可访问性和技术时效不一致；仓库本身不是可分析的软件系统，因此不进入今日架构深挖。

### Rank 11 - MoonshotAI/kimi-cli
- Repo URL: https://github.com/MoonshotAI/kimi-cli
- Tagline: 支持代码编辑、Shell、Web、MCP 与 ACP 的终端 AI Agent。
- Stars: 9,628
- Stars Today: 65
- Forks: 1,167
- Language: Python
- License: Apache-2.0
- Homepage: https://moonshotai.github.io/kimi-cli/en/
- Topics: cli-agent, coding-agent, mcp, acp, terminal, python
- 技术栈: Python 3.12+, Typer, prompt-toolkit, kosong, FastMCP, ACP, FastAPI/WebSocket, Pydantic
- Why It Matters Today: 虽然项目正在迁移到下一代 Kimi Code CLI，它仍以 65 Stars Today 上榜，是观察终端 Agent 工具编排和迁移策略的完整样本。
- 项目摘要: Kimi CLI 在终端中读取和修改代码、执行 Shell、搜索网页，并按模型决策循环调用工具。它支持交互式终端、Shell 模式、VS Code、ACP 编辑器接入和 MCP 服务器管理。
- 核心特性:
  1. 在同一交互中切换 Agent 模式与直接 Shell 命令模式。
  2. 通过 ACP 作为 IDE Agent Server，也可连接 stdio、HTTP 和 OAuth MCP 服务。
  3. 保存配置与会话，并为迁移到 Kimi Code CLI 提供自动迁移路径。
- 适用场景: 终端编程辅助、自动化小任务、研究 ACP/MCP Agent 集成；新部署应优先评估继任项目 Kimi Code CLI，而非把正在收尾的旧仓库作为长期基座。
- 一句话推荐: 这辆终端 Agent 老车配置挺全，但站牌已经写着“下一站换乘”；研究发动机可以，新项目别假装没看见通知。
- Evidence Notes: GitHub Trending；README 的终端能力、Shell、ACP、MCP 与迁移公告；`pyproject.toml` 的入口和依赖；源码入口 `src/kimi_cli/__main__.py`。
- Honest Caveat: 官方明确说明项目将逐步收尾并迁移到 Kimi Code CLI；长期维护、兼容性和新功能应以继任仓库为准。

### Explore Supplement E1 - CodeFactor（非 Trending 排名）
- Repo URL: https://github.com/marketplace/codefactor
- Tagline: GitHub 官方 Explore 推荐的自动代码质量检查服务。
- Stars: N/A
- Stars Today: N/A
- Forks: N/A
- Language: N/A
- License: 服务条款适用
- Homepage: https://www.codefactor.io/
- Topics: code-quality, pull-request, static-analysis, autofix, github-app
- 技术栈: GitHub App, commit/PR checks, static analysis, autofix, Slack/MS Teams integration
- Why It Matters Today: GitHub Explore 以员工推荐形式展示 CodeFactor，补充了今日代码审查与自动质量门禁的主题。
- 项目摘要: CodeFactor 在 Commit 或 Pull Request 上运行代码质量检查，向开发者返回问题、重构建议和可配置规则，并可对部分问题执行 Autofix。
- 核心特性:
  1. 在 GitHub PR 页面展示检查状态和代码建议。
  2. 支持规则定制、忽略无关问题和部分自动修复。
  3. 可通过 Slack 或 Microsoft Teams 同步团队状态。
- 适用场景: 希望快速增加基础静态检查和 PR 反馈的团队；它不是今日 Trending 仓库，也不应被计入开源项目排名、Stars Today 或语言统计。
- 一句话推荐: 这是 Explore 临时请来的质检员，不是硬塞进榜单的第十二名；工牌颜色都给它换成 E1 了。
- Evidence Notes: GitHub Explore 的 “This recommendation was created by GitHub staff” 与 CodeFactor 功能说明。
- Honest Caveat: 该项是商业服务推荐而非 Trending 开源仓库；具体语言覆盖、计费、数据处理和 Autofix 风险应查看当前服务条款。

## Language Distribution

- Python:
  - Count: 6
  - Percent: 54.5%
  - Color Hint: #3572A5
- TypeScript:
  - Count: 3
  - Percent: 27.3%
  - Color Hint: #3178C6
- Jupyter Notebook:
  - Count: 1
  - Percent: 9.1%
  - Color Hint: #DA5B0B
- Markdown:
  - Count: 1
  - Percent: 9.1%
  - Color Hint: #083FA1
- Other:
  - Count: 0
  - Percent: 0%
  - Color Hint: #555

## Explore Highlights

### Explore 1
- Title: Robbyant/lingbot-map
- URL: https://github.com/Robbyant/lingbot-map
- Kind: Trending repository
- Meta: 13.2k Stars · Python · Updated 2026-07-12
- Short Reason: 流式三维重建模型，同时位列今日 Trending 第一。

### Explore 2
- Title: apache/ossie
- URL: https://github.com/apache/ossie
- Kind: Trending repository
- Meta: 1.3k Stars · Python · Updated 2026-07-17
- Short Reason: 用开放规范统一 AI、BI 与分析工具的语义模型。

### Explore 3
- Title: Copilot CLI update: chronicle, plugins, and fleet mode
- URL: https://www.youtube.com/
- Kind: GitHub Checkout
- Meta: plugin marketplace · /chronicle · fleet mode · autopilot
- Short Reason: GitHub 官方视频介绍 Copilot CLI 的插件、自愈提示和并行模型实验能力。

### Explore 4
- Title: React
- URL: https://github.com/topics/react
- Kind: Popular topic
- Meta: GitHub 今日热门话题
- Short Reason: 前端组件生态继续保持高关注度。

### Explore 5
- Title: PostHog/posthog
- URL: https://github.com/PostHog/posthog
- Kind: Trending repository
- Meta: 36.7k Stars · Python · Updated 2026-07-19
- Short Reason: 产品数据平台继续向 Agent 诊断与自动化延伸。

### Explore 6
- Title: tirth8205/code-review-graph
- URL: https://github.com/tirth8205/code-review-graph
- Kind: Trending repository
- Meta: 20.3k Stars · Python · Updated 2026-07-18
- Short Reason: 本地代码关系图与 MCP 继续吸引 AI 编码工具用户。

### Explore 7
- Title: KnockOutEZ/wigolo
- URL: https://github.com/KnockOutEZ/wigolo
- Kind: Trending repository
- Meta: 1.4k Stars · TypeScript · Updated 2026-07-19
- Short Reason: 把网页搜索、抓取和研究能力交给本地 Agent。

### Explore 8
- Title: CodeFactor
- URL: https://github.com/marketplace/codefactor
- Kind: GitHub staff recommendation
- Meta: PR review · code quality · Autofix
- Short Reason: GitHub 官方推荐的自动代码质量与 PR 检查服务，作为 E1 补充项展示。

## Rendering Notes

- Hero 主标题建议：GitHub 开源趋势日报 · 2026-07-19
- Hero 副标题建议：11 个官方 Trending 项目，外加 1 个明确标注的 Explore 补位；今天从流式三维建图一路看到本地 Agent 网页研究。
- Top 3 高亮原因：LingBot-Map 代表流式三维基础模型；Ossie 代表语义互操作标准；PostHog 代表产品数据与 Agent 上下文融合。
- 需要在 HTML 中诚实提示的降级点：官方 Trending 页面仅返回 11 项；E1 CodeFactor 不是仓库排名，不计入项目数、增星、语言或 AI 统计。
- 不允许省略的区块：Header / Hero、4 张 Stats Cards、今日洞察、11 个 Trending 项目与 E1 补位、编程语言分布、GitHub Explore 精选、Footer。
- 必须保留的固定模板结构：
  - Header / Hero
  - 4 张 Stats Cards
  - 今日洞察
  - 今日热门榜单
  - 编程语言分布
  - GitHub Explore 精选
  - Footer
- Top 详情固定顺序：
  1. 项目摘要
  2. 核心特性
  3. 技术栈
  4. 适用场景
  5. 一句话推荐

## Markdown Acceptance

- [x] 报告日期使用 Asia/Tokyo 的 2026-07-19。
- [x] GitHub Trending Repositories / Any language / Today 抓取成功。
- [x] 保留官方返回的 11 个项目原始顺序。
- [x] 累计 Stars、Forks 与 Stars Today 分开记录。
- [x] 11 个 Trending 项目字段完整，E1 补位明确排除在排名和统计之外。
- [x] 4 个 Stats、4 条洞察、语言分布、Explore 与渲染说明完整。
- [x] 每项均包含 Evidence Notes 与 Honest Caveat。
- [x] Markdown 通过内容验收，可以进入架构分析阶段。
