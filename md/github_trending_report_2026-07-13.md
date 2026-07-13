# GitHub Trending 日报内容底稿

## Meta

- Report Date: 2026-07-13
- Generated At: 2026-07-13 09:04:33 JST
- Output Markdown: md/github_trending_report_2026-07-13.md
- Planned HTML: html/github_trending_report_2026-07-13.html
- Fixed Base Template: .codex/skills/skill-github-trending-report/reference/fixedBaseTemplate_2026-03-16.html
- User Rules: .codex/skills/skill-github-trending-report/reference/user-rules.md
- Data Scope: GitHub Trending · Repositories · Any language · Today
- Sources:
  - https://github.com/trending
  - https://github.com/explore
  - Repo README / About / Homepage / License pages
  - GitHub 公开仓库资料与项目官方文档

## Page Intent

- 今日主线：AI Agent 正在从“会写代码”继续向“能安全执行命令、操作本地环境、长期后台工作和进入垂直业务”扩展；与此同时，工作流编排、家庭自动化和离线知识系统等成熟工程项目保持强势。
- 适合谁阅读：使用 AI 编程工具的开发者、数据与自动化工程师、关注 Agent 安全与落地边界的技术负责人，以及寻找可运行开源样例的学习者。
- 页面重点：严格保留 GitHub Trending 原始 Top 12 顺序，同时独立展示 Stars Today；原始排名是平台综合排序，不等于当天增星速度排名。
- 需要诚实降级说明的地方：GitHub 未公开 Trending 完整算法；多个项目涉及高权限终端、金融研究或第三方客户端修改，必须单独评估安全、合规和生产适用性；Wand-Enhancer 的 Trending 快照显示 Forks 高于 Stars，虽与仓库页一致，仍属于异常分布，报告只忠实记录而不作推断。

## Stats

- Trending 项目数：12
- 今日累计新增 Stars：3,722
- 编程语言数：5
- AI 相关项目数：9

## Editorial Insights

### Insight 1
- Title: AI Agent 的新战场，是“动手之前先别闯祸”
- Body: 榜首 `destructive_command_guard` 不负责让 Agent 更聪明，而是把危险命令挡在执行前；`DesktopCommanderMCP` 和 `background-agents` 则把终端、文件系统与后台开发环境交给模型。能力越接近真实机器，权限边界越不能靠一句“请谨慎”维持。今天的信号很明确：Agent 工程正在从功能竞赛进入执行安全与治理阶段。

### Insight 2
- Title: AI 正从通用助手下沉到交易、知识库与家庭场景
- Body: `Vibe-Trading`、`ai-hedge-fund` 把多 Agent 带进量化研究与投资实验，`project-nomad` 把本地模型和离线知识库装进自托管设备，Home Assistant 继续守住本地优先的家庭自动化。大家不再只问“模型会不会回答”，而是开始问“它能否在一个具体系统里持续工作”。

### Insight 3
- Title: 可运行样例仍然是 AI 开发最硬的学习资料
- Body: `awesome-llm-apps` 和 Anthropic 官方 `claude-cookbooks` 同时上榜，一个提供大量可克隆应用，一个提供 API 使用配方。文档讲概念，样例替你踩第一遍坑；不过样例能跑不等于可直接上线，密钥、成本、依赖版本和数据安全仍要自己收拾。

### Insight 4
- Title: 原始排名与今日增星速度，还是两本账
- Body: 第 3 名 `Vibe-Trading` 今日新增 776 Stars，第 10 名 `Wand-Enhancer` 新增 603，而第 4 名 Prefect 只有 55。GitHub 的榜单顺序不是简单按 Stars Today 排列；阅读时应把“平台排名”与“当日加速”分开，前者看综合趋势，后者看突然升温。

## Top Projects

### Rank 01 - Dicklesworthstone/destructive_command_guard
- Repo URL: https://github.com/Dicklesworthstone/destructive_command_guard
- Tagline: 给 AI 编程代理加一道命令执行闸门，在危险 Git、文件系统、云平台或数据库操作真正落地前进行拦截。
- Stars: 2,721
- Stars Today: 444
- Forks: 102
- Language: Rust
- License: MIT
- Homepage: https://github.com/Dicklesworthstone/destructive_command_guard
- Topics: git, rust, cli, developer-tools, safety, ai-agents
- 技术栈: Rust, CLI hooks, command parsing, regex/SIMD matching, TOML configuration
- Why It Matters Today: AI Agent 获得终端权限后，最现实的风险往往不是模型答错，而是模型把错误命令真的执行了。这个项目直接补上执行前防线，因此冲到原始榜首很有代表性。
- 项目摘要: Destructive Command Guard（dcg）是安装在 AI 编程工具与 Shell 执行之间的安全钩子。它检查 Agent 准备运行的命令，识别破坏性 Git 操作、递归删除、云资源销毁和数据库高风险操作，并在拦截时给出原因或更安全的替代建议。
- 核心特性:
  1. 支持 Claude Code、Codex CLI、Gemini CLI、Copilot CLI、Cursor 等多种 Agent 工具的命令钩子。
  2. 通过模块化安全规则包覆盖 Git、文件系统、云平台、容器和数据库命令，并能扫描内联脚本与组合命令。
  3. 提供 explain、allowlist、scan 与 CI 使用方式，方便团队解释规则、处理例外并在流水线中检查风险。
- 适用场景: 给具备 Shell 权限的编码 Agent 增加最后一道防误操作保护；希望统一团队危险命令策略的开发环境；在 CI 中提前发现脚本中的高风险操作。
- 一句话推荐: Agent 能帮你敲命令，也可能帮你把盘掀了；dcg 就是上菜前先看一眼托盘稳不稳。
- Evidence Notes: GitHub Trending 明确将其列为原始第 1 名并显示 444 Stars Today；项目 README 将其定义为执行前命令安全钩子，列出多 Agent 支持、模块化规则包、解释与扫描能力；仓库显示 MIT License。
- Honest Caveat: 它不是完整沙盒或权限隔离系统，项目也提供绕过与 fail-open 机制；默认启用的规则包并非覆盖所有云与数据库风险。README 中的亚毫秒性能为维护者自测口径，未经独立验证。

### Rank 02 - wonderwhy-er/DesktopCommanderMCP
- Repo URL: https://github.com/wonderwhy-er/DesktopCommanderMCP
- Tagline: 通过 MCP 把终端、文件搜索、进程管理和差异化文件编辑能力交给 Claude 等 AI 客户端。
- Stars: 7,950
- Stars Today: 207
- Forks: 984
- Language: TypeScript
- License: MIT
- Homepage: https://github.com/wonderwhy-er/DesktopCommanderMCP
- Topics: agent, ai, mcp, code-analysis, code-generation, terminal-automation, vibe-coding
- 技术栈: TypeScript, Node.js, Model Context Protocol, terminal processes, filesystem APIs, diff editing
- Why It Matters Today: 它代表 Agent 从“建议你怎么做”迈向“直接在你的电脑上做”。这种能力很实用，也意味着权限、目录和命令边界必须同时进入设计范围。
- 项目摘要: Desktop Commander MCP 是一个本地 MCP Server，让支持 MCP 的 AI 客户端能够搜索和编辑文件、执行终端命令、管理长时间运行进程，并通过差异化编辑减少整文件重写。它适合把桌面开发任务交给 Agent 连续完成。
- 核心特性:
  1. 提供终端执行、进程管理、文件搜索、读取和差异编辑等一组本地工具。
  2. 支持长任务会话、输出流与进程交互，让 Agent 不只会跑一次性命令。
  3. 提供配置、日志和目录或命令限制选项，并能与多个 MCP 客户端连接。
- 适用场景: 让 Claude Desktop 等客户端直接处理本地代码库；执行批量文件修改与搜索；在对话中管理构建、测试或数据处理进程。
- 一句话推荐: 想让 AI 真正在桌面上干活，它很能干；也正因为太能干，门钥匙别随手扔给它。
- Evidence Notes: GitHub Trending 显示原始第 2 名和 207 Stars Today；README 明确列出终端控制、文件搜索、差异编辑、长进程管理和配置日志能力；仓库显示 MIT License。
- Honest Caveat: 项目文档明确提醒目录和命令限制可以被终端路径绕过，`allowedDirectories` 只约束文件工具，不约束终端命令；生产或不可信任务应使用容器、最小权限目录与额外隔离。

### Rank 03 - HKUDS/Vibe-Trading
- Repo URL: https://github.com/HKUDS/Vibe-Trading
- Tagline: 用自然语言启动研究、回测和多 Agent 讨论的个人交易研究工具箱。
- Stars: 20,420
- Stars Today: 776
- Forks: 3,582
- Language: Python
- License: MIT
- Homepage: https://vibetrading.wiki/
- Topics: python, trading, mcp, multi-agent, quantitative-finance, backtesting, ai-agent, llm
- 技术栈: Python, FastAPI, React, quantitative backtesting, multi-agent swarms, MCP/API
- Why It Matters Today: 它是 Top 12 中 Stars Today 最高的项目，说明“把 Agent 接进量化研究流程”正在快速吸引开发者；但金融场景也最容易把演示效果误读成真实收益。
- 项目摘要: Vibe-Trading 把行情研究、策略回测、量化因子和多 Agent 讨论组合成一个可通过命令行、Web 或 MCP 调用的个人交易研究环境。用户可以用自然语言描述资产、时间区间和研究目标，再让系统组织数据与分析流程。
- 核心特性:
  1. 支持自然语言触发回测、市场分析和策略研究，并提供 CLI、Web 界面与 API/MCP 入口。
  2. 内置多种专家与委员会式 Agent 预设，可围绕技术分析、风险和跨市场配置进行讨论。
  3. 提供量化 Alpha 库、回测约束和防止前视偏差的检查机制，便于做可重复研究。
- 适用场景: 学习量化研究工作流；快速搭建个人策略实验室；为 Agent 接入市场数据、回测和风险讨论能力。
- 一句话推荐: 它适合拿来做研究搭子，不适合拿来当财神爷——回测曲线再漂亮，也不会替你承担亏损。
- Evidence Notes: GitHub Trending 显示原始第 3 名和 776 Stars Today；README 将其定位为 Personal Trading Agent，展示 Python/FastAPI/React、自然语言回测、多 Agent 预设、Alpha Zoo 与 API/MCP；仓库显示 MIT License。
- Honest Caveat: 金融结果依赖数据质量、费用假设、滑点与回测设计，历史表现不保证未来收益；本报告不验证项目策略收益，也不构成投资建议。

### Rank 04 - PrefectHQ/prefect
- Repo URL: https://github.com/PrefectHQ/prefect
- Tagline: 把普通 Python 函数升级为可调度、可重试、可观察的数据与自动化工作流。
- Stars: 23,101
- Stars Today: 55
- Forks: 2,386
- Language: Python
- License: Apache-2.0
- Homepage: https://www.prefect.io/
- Topics: python, workflow, data-engineering, orchestration, observability, mlops, automation
- 技术栈: Python, workflow orchestration, scheduling, retries, caching, event automation, workers
- Why It Matters Today: 在一片 Agent 项目里，成熟工作流编排框架仍排到第 4，提醒大家生产系统最后还得靠调度、重试、状态和可观察性把活干稳。
- 项目摘要: Prefect 是 Python 工作流编排框架，可以在尽量保留普通 Python 编程体验的同时，为任务增加调度、重试、缓存、状态跟踪和事件触发。它常用于数据管道、机器学习任务和跨系统自动化。
- 核心特性:
  1. 用 Python 装饰器把函数组织成 Flow 与 Task，并保留本地开发和调试体验。
  2. 提供计划调度、失败重试、缓存、并发与状态管理，增强长流程韧性。
  3. 支持事件自动化、Worker 执行和可观察界面，便于管理分布式任务。
- 适用场景: 数据清洗和 ETL；机器学习训练或批处理；需要可靠重试、定时执行和运行状态追踪的 Python 自动化。
- 一句话推荐: 脚本偶尔跑一次叫工具，天天准时跑、失败会重来、出了事能查，才叫系统；Prefect 管的就是这一步。
- Evidence Notes: GitHub Trending 显示原始第 4 名和 55 Stars Today；官方 README 将 Prefect 定义为 Python workflow orchestration，并列出 scheduling、caching、retries 与 event-based automations；仓库使用 Apache-2.0。
- Honest Caveat: 引入编排平台也会增加部署、Worker、状态存储和运维复杂度；开源自托管与 Prefect Cloud 的能力和成本需要按团队需求分别评估。

### Rank 05 - Shubhamsaboo/awesome-llm-apps
- Repo URL: https://github.com/Shubhamsaboo/awesome-llm-apps
- Tagline: 汇集 100 多个能实际运行的 AI Agent、RAG 和多模型应用，适合克隆后拆解或改造。
- Stars: 118,429
- Stars Today: 450
- Forks: 17,616
- Language: Python
- License: Apache-2.0
- Homepage: https://www.theunwindai.com/
- Topics: python, agents, rag, llms, generative-ai, examples
- 技术栈: Python, LLM APIs, RAG, vector databases, agent frameworks, multimodal models
- Why It Matters Today: 它是榜单总 Stars 最高的仓库，说明开发者仍强烈需要“能跑起来的完整样例”，而不是又一篇只画架构图的概念文章。
- 项目摘要: awesome-llm-apps 是一组按应用场景整理的可运行 AI 项目，覆盖 Agent、RAG、语音、视觉、记忆、多 Agent 和不同模型服务商。它更像一个大型实验货架，适合快速找到起点并研究项目结构。
- 核心特性:
  1. 提供大量独立应用目录，可直接查看依赖、配置和运行入口。
  2. 覆盖 OpenAI、Anthropic、Google、开源模型及多种向量数据库和 Agent 框架。
  3. 场景从基础聊天、文档问答延伸到多 Agent、研究助手和垂直行业应用。
- 适用场景: AI 应用入门；寻找 PoC 或黑客松起点；比较不同 RAG、模型和 Agent 框架的实现方式。
- 一句话推荐: 想学 AI 应用，别只在岸上背泳姿；这里有一百多个泳池，不过下水前记得先看水深。
- Evidence Notes: GitHub Trending 显示原始第 5 名和 450 Stars Today；README 明确称其收录 100+ 可运行 AI Agent 与 RAG 应用，并展示多个模型服务和项目类别；仓库使用 Apache-2.0。
- Honest Caveat: 这些项目主要是示例和学习材料，各目录的维护状态、依赖版本、安全措施和生产成熟度并不一致；使用前需逐个审查密钥管理、数据隐私与运行成本。

### Rank 06 - anthropics/claude-cookbooks
- Repo URL: https://github.com/anthropics/claude-cookbooks
- Tagline: Anthropic 官方提供的 Claude API Notebook 与配方集，用可复制代码演示常见能力和组合方式。
- Stars: 48,304
- Stars Today: 464
- Forks: 5,718
- Language: Jupyter Notebook
- License: MIT
- Homepage: https://docs.claude.com/
- Topics: claude, anthropic, notebooks, api-examples, prompt-engineering, multimodal
- 技术栈: Jupyter Notebook, Python, Anthropic API, tool use, multimodal prompting, retrieval
- Why It Matters Today: 官方 Cookbook 与社区大型样例库同时上榜，说明开发者既需要广度，也需要一份接近官方最佳实践的参考实现。
- 项目摘要: claude-cookbooks 是 Anthropic 官方维护的 Notebook 和代码配方集合，围绕 Claude API 展示提示设计、工具调用、视觉理解、检索和不同平台集成。内容适合复制到自己的实验环境后逐段修改。
- 核心特性:
  1. 以 Notebook 和可运行代码呈现 Claude 的常见 API 模式，降低第一次接入成本。
  2. 覆盖工具使用、视觉、多轮工作流、检索与第三方平台等主题。
  3. 示例通常配有解释和输入输出，便于定位请求结构与模型行为。
- 适用场景: Claude API 入门；验证某项能力是否适合自己的产品；为团队建立内部示例和实验基线。
- 一句话推荐: 官方菜谱的好处不是保证你一夜成大厨，而是至少先告诉你锅该放哪儿。
- Evidence Notes: GitHub Trending 显示原始第 6 名和 464 Stars Today；README 将其定义为可复制的 Claude 使用代码与指南，说明主要使用 Python 并要求 Claude API Key；仓库使用 MIT License。
- Honest Caveat: 示例会随 API 和模型版本演进，部分云平台样例需要额外修改；运行会产生 API 成本，且 Cookbook 并不替代生产级错误处理、限流、审计和隐私设计。

### Rank 07 - home-assistant/core
- Repo URL: https://github.com/home-assistant/core
- Tagline: 本地优先、重视隐私的开源家庭自动化核心，统一连接设备、传感器和自动化规则。
- Stars: 88,985
- Stars Today: 404
- Forks: 38,076
- Language: Python
- License: Apache-2.0
- Homepage: https://www.home-assistant.io/
- Topics: home-automation, mqtt, raspberry-pi, iot, internet-of-things, asyncio
- 技术栈: Python, asyncio, IoT integrations, MQTT, event-driven automation, local deployment
- Why It Matters Today: Home Assistant 不是新鲜概念，却仍以 404 Stars Today 排在第 7。它说明本地控制、数据自主和庞大设备兼容性仍是智能家居的核心价值。
- 项目摘要: Home Assistant Core 是 Home Assistant 的 Python 自动化引擎，负责接入设备和服务、维护实体状态并执行自动化。它强调在本地服务器或树莓派上运行，让家庭数据和控制尽量留在用户自己的网络中。
- 核心特性:
  1. 通过大量集成连接灯具、传感器、能源设备、媒体和云服务。
  2. 使用事件和状态驱动自动化，可根据时间、设备变化或复杂条件触发动作。
  3. 支持本地部署与多种安装方式，并提供仪表盘、移动端和语音生态配套。
- 适用场景: 自建智能家居中枢；将不同品牌设备统一到一套自动化规则中；重视本地控制与隐私的家庭和实验室。
- 一句话推荐: 智能家居最怕每个插座都有自己的脾气，Home Assistant 干的就是把这一屋子“亲戚”拉进同一个群聊。
- Evidence Notes: GitHub Trending 显示原始第 7 名和 404 Stars Today；官方 README 强调 local control and privacy first，并提供安装、演示、文档及模块化集成说明；仓库使用 Apache-2.0。
- Honest Caveat: 设备兼容、网络隔离、远程访问和升级维护仍可能复杂；接入家庭关键设备前应规划备份、安全更新和故障时的手动控制方案。

### Rank 08 - Crosstalk-Solutions/project-nomad
- Repo URL: https://github.com/Crosstalk-Solutions/project-nomad
- Tagline: 把离线百科、教育资源、地图、工具和本地 AI 打包成自托管知识服务器。
- Stars: 33,733
- Stars Today: 122
- Forks: 3,384
- Language: TypeScript
- License: Apache-2.0
- Homepage: https://github.com/Crosstalk-Solutions/project-nomad
- Topics: offline, survival, knowledge-base, ollama, qdrant, self-hosted, education
- 技术栈: TypeScript, Debian/Linux, Docker services, Kiwix, Ollama, Qdrant, Kolibri, ProtoMaps
- Why It Matters Today: 它把“本地 AI”放进更具体的离线知识场景：断网时仍能查资料、地图、课程和文档。相比单纯跑一个模型，它更接近完整离线信息系统。
- 项目摘要: Project N.O.M.A.D 是面向 Debian 系统的一套离线知识与教育服务器安装方案。它组合 Kiwix、离线百科与医疗资料、Kolibri 课程、离线地图、CyberChef，以及由 Ollama 和 Qdrant 支撑的本地问答与文档检索。
- 核心特性:
  1. 在局域网浏览器中提供统一入口，无需持续互联网连接即可访问知识和工具。
  2. 集成离线百科、教育内容、电子书、地图和应急资料等多类内容源。
  3. 通过本地模型与向量检索支持离线聊天和文档语义搜索。
- 适用场景: 网络不稳定地区的教育与资料站；应急准备；房车、船只、社区中心或家庭实验室的离线知识服务。
- 一句话推荐: 这不是“断网后还能聊两句”的小玩具，而是一整座离线资料室；问题是，资料室也得有人定期换新书。
- Evidence Notes: GitHub Trending 显示原始第 8 名和 122 Stars Today；README 将 N.O.M.A.D 解释为 Node for Offline Media Archives Data，并列出 Kiwix、Ollama、Qdrant、Kolibri、ProtoMaps 和 CyberChef；仓库使用 Apache-2.0。
- Honest Caveat: 安装脚本需要较高系统权限并部署多个服务，对存储、内存和运维有要求；离线内容的准确性与时效取决于用户主动更新，不能把“离线可用”理解为“永远最新”。

### Rank 09 - ColeMurray/background-agents
- Repo URL: https://github.com/ColeMurray/background-agents
- Tagline: 开源的后台编码 Agent 系统，让开发任务在独立环境中持续执行并通过 GitHub、Slack 或 Web 管理。
- Stars: 2,223
- Stars Today: 9
- Forks: 341
- Language: TypeScript
- License: MIT
- Homepage: https://backgroundagents.dev/
- Topics: coding-agents, background-jobs, github, slack, linear, webhooks, open-source
- 技术栈: TypeScript, isolated dev environments, GitHub App, Slack/Linear integrations, browser automation, webhooks
- Why It Matters Today: 它当日增星不高却仍排第 9，说明 GitHub 排名并非只看即时增速；更重要的是，编码 Agent 正从前台对话转为可以独立跑几小时的后台工作单元。
- 项目摘要: background-agents（Open Inspect）让用户把编码任务交给独立开发环境中的 Agent 后继续做别的事情。Agent 可以安装依赖、运行代码和浏览器、修改仓库并提交结果，用户可从 Web、Slack、GitHub PR、Linear 或 Webhook 发起和跟踪任务。
- 核心特性:
  1. 为任务提供包含 Node、Python、Git、浏览器自动化和 VS Code 的完整开发环境。
  2. 支持从 Web、Slack、GitHub、Linear、定时任务与 Webhook 触发后台工作。
  3. 提供多人协作、提交归属和任务结果回传，便于团队查看 Agent 做了什么。
- 适用场景: 把耗时的代码改造、测试或调查放到后台；为团队构建自托管编码 Agent 平台；将错误监控或工单自动转为开发任务。
- 一句话推荐: 它像给编码 Agent 安排了夜班，但夜班员工拿着仓库钥匙——门禁和摄像头一个都不能少。
- Evidence Notes: GitHub Trending 显示原始第 9 名和 9 Stars Today；README 列出完整开发环境、Web/Slack/GitHub/Linear/Webhook 入口及多人协作能力；仓库使用 MIT License。
- Honest Caveat: 项目安全说明明确面向单租户和可信组织用户，不适合直接作为开放多租户服务；部署时应放在 SSO/VPN 后，并严格限制 GitHub App 可访问的仓库与用户。

### Rank 10 - k1tbyte/Wand-Enhancer
- Repo URL: https://github.com/k1tbyte/Wand-Enhancer
- Tagline: 面向 Wand（WeMod）桌面客户端的开源本地增强工具，改善界面、兼容性和设备互操作体验。
- Stars: 6,846
- Stars Today: 603
- Forks: 19,248
- Language: C#
- License: Apache-2.0
- Homepage: https://gitlab.com/kitbyte/wand-enhancer
- Topics: csharp, wpf, wand, wemod, local-client, ux
- 技术栈: C#, WPF, local client configuration, web panel, desktop interoperability
- Why It Matters Today: 它以 603 Stars Today 成为当日增速第二高项目，但用途不是主流开发框架，而是第三方桌面客户端增强，显示榜单热度也会被特定用户社区快速推动。
- 项目摘要: Wand-Enhancer 是一个本地运行的 Wand（WeMod）客户端互操作与 UX 增强项目。它调整本地配置、处理版本兼容、提供界面和主题改进，并可通过同一局域网中的移动 Web 面板进行部分控制。
- 核心特性:
  1. 扩展本地客户端配置并进行自动兼容性调整，减少版本变化带来的手动处理。
  2. 提供界面、主题和交互体验增强，以及项目所称的 AI 相关功能。
  3. 可启动移动端远程 Web 面板，在同一 Wi-Fi 网络中访问本机服务。
- 适用场景: 已使用 Wand/WeMod 且希望改善桌面操作体验的用户；研究 C# 桌面客户端扩展与本地配置互操作的开发者。
- 一句话推荐: 这是给特定客户端“精装修”的工具，不是万能扳手；先认准官方仓库，别从野生视频评论区捡安装包。
- Evidence Notes: GitHub Trending 显示原始第 10 名、603 Stars Today、6,846 Stars 与 19,248 Forks；仓库页同样显示约 6.9k Stars 和 19.3k Forks，README 明确警告不存在官方 YouTube 教程或预编译 EXE，并说明本地运行、配置增强和 Web 面板；仓库使用 Apache-2.0。
- Honest Caveat: 项目依赖第三方专有客户端，兼容性可能随上游更新变化；移动面板会开放本地端口，应仅在可信网络使用。Forks 显著高于 Stars 的异常分布已由页面交叉确认，但其原因无法从公开证据确定。

### Rank 11 - pingdotgg/t3code
- Repo URL: https://github.com/pingdotgg/t3code
- Tagline: 用一个简洁 Web/桌面界面统一启动和操作 Codex、Claude、Cursor 与 OpenCode 编码代理。
- Stars: 13,712
- Stars Today: 79
- Forks: 2,879
- Language: TypeScript
- License: MIT
- Homepage: https://t3.codes/
- Topics: coding-agents, codex, claude, cursor, opencode, web-gui
- 技术栈: TypeScript, Vite+, web UI, desktop packaging, provider CLI integrations
- Why It Matters Today: 编码 Agent 越来越多，新的痛点开始变成“我不想为每家工具维护一套入口”。T3 Code 的价值在于统一界面，而不是再造一个模型。
- 项目摘要: T3 Code 是一个面向编码 Agent 的轻量 Web GUI，目前支持 Codex、Claude、Cursor 和 OpenCode。它复用用户已经安装并登录的各家 CLI，也提供桌面安装包，让用户在统一界面中选择不同提供方处理代码任务。
- 核心特性:
  1. 在同一界面中接入多种主流编码 Agent，减少工具切换成本。
  2. 支持通过 `npx t3@latest` 快速运行，也提供 Windows、macOS 与 Arch Linux 桌面安装方式。
  3. 保留各提供方原有认证方式，不要求把所有凭据重新交给一套自建模型服务。
- 适用场景: 同时使用多个编码 Agent 的开发者；希望给团队提供更统一操作入口；比较不同 Agent 在同一任务上的表现。
- 一句话推荐: 当 AI 编程工具多到像电视遥控器，T3 Code 想做的就是那只“万能遥控器”——目前还属于早期工程样机。
- Evidence Notes: GitHub Trending 显示原始第 11 名和 79 Stars Today；README 将其定义为 Codex、Claude、Cursor、OpenCode 的 minimal web GUI，列出各提供方认证与多平台安装方式；仓库使用 MIT License。
- Honest Caveat: README 明确称项目仍“very very early”并提示可能有 Bug，公共文档也仍在完善；它依赖用户自行安装、认证和维护各家 Provider CLI。

### Rank 12 - virattt/ai-hedge-fund
- Repo URL: https://github.com/virattt/ai-hedge-fund
- Tagline: 用多个投资风格 Agent、风险与组合管理角色模拟 AI 投资研究团队的教育型项目。
- Stars: 61,352
- Stars Today: 109
- Forks: 10,851
- Language: Python
- License: MIT
- Homepage: https://github.com/virattt/ai-hedge-fund
- Topics: ai, finance, trading, multi-agent, llm, backtesting, education
- 技术栈: Python, multi-agent orchestration, financial data APIs, LLM providers, backtesting, portfolio analysis
- Why It Matters Today: 它与 Vibe-Trading 同日上榜，进一步说明金融 Agent 仍是最吸睛的垂直方向之一；但项目自己的第一句话就是“概念验证与教育用途”，这条边界比任何收益截图都重要。
- 项目摘要: ai-hedge-fund 用多个模拟知名投资方法的 Agent 分析公司、估值、基本面和市场信号，再由风险管理与组合角色汇总意见。项目正在向可持续回测、模拟交易和可选实时运行演进，但当前定位仍是探索 AI 投资决策的概念验证。
- 核心特性:
  1. 组织多个投资风格 Agent 并行给出观点，再由风险与组合管理角色进行汇总。
  2. 支持接入金融数据与不同 LLM Provider，方便比较分析流程和模型输出。
  3. 提供回测、命令行和可视化应用相关代码，并公开后续持久化基金与纸面交易路线图。
- 适用场景: 学习多 Agent 协作与金融分析流程；研究提示、数据和角色分工如何影响结果；搭建教育型回测实验。
- 一句话推荐: 把它当金融 Agent 实验室很有意思，把它当持牌基金经理就有点拿相声票进证券交易所了。
- Evidence Notes: GitHub Trending 显示原始第 12 名和 109 Stars Today；README 明确称其为 AI-powered hedge fund proof of concept，列出多位投资风格 Agent，并说明正在向回测、纸面交易和可选实时模式演进；仓库使用 MIT License。
- Honest Caveat: 项目明确声明仅供教育，不用于真实交易或投资；Agent 输出可能包含事实错误、数据延迟与模型偏见，本报告不验证策略收益，也不构成金融建议。

## Language Distribution

- Python:
  - Count: 5
  - Percent: 41.7%
  - Color Hint: #3572A5
- TypeScript:
  - Count: 4
  - Percent: 33.3%
  - Color Hint: #3178C6
- Rust:
  - Count: 1
  - Percent: 8.3%
  - Color Hint: #DEA584
- C#:
  - Count: 1
  - Percent: 8.3%
  - Color Hint: #178600
- Jupyter Notebook:
  - Count: 1
  - Percent: 8.3%
  - Color Hint: #DA5B0B

## Explore Highlights

Explore 页面抓取成功，但当天推荐与 Trending Top 12 高度重合。以下保持为补充列表，不另造第二份排行榜。

### Explore 1
- Title: Dicklesworthstone/destructive_command_guard
- URL: https://github.com/Dicklesworthstone/destructive_command_guard
- Kind: Trending repository
- Meta: Rust · 约 2.8k Stars · Updated Jul 11, 2026
- Short Reason: Agent 命令执行安全成为今日最鲜明的新信号。

### Explore 2
- Title: wonderwhy-er/DesktopCommanderMCP
- URL: https://github.com/wonderwhy-er/DesktopCommanderMCP
- Kind: Trending repository
- Meta: TypeScript · 约 8k Stars · Updated Jul 12, 2026
- Short Reason: 把终端和文件系统交给 MCP，能力与风险都值得关注。

### Explore 3
- Title: HKUDS/Vibe-Trading
- URL: https://github.com/HKUDS/Vibe-Trading
- Kind: Trending repository
- Meta: Python · 约 20.5k Stars · Updated Jul 12, 2026
- Short Reason: 今日 Stars Today 最高，代表金融 Agent 研究工具快速升温。

### Explore 4
- Title: PrefectHQ/prefect
- URL: https://github.com/PrefectHQ/prefect
- Kind: Trending repository
- Meta: Python · 约 23.1k Stars · Updated Jul 12, 2026
- Short Reason: 在 Agent 热潮中，可靠工作流编排仍是生产系统底座。

### Explore 5
- Title: anthropics/claude-cookbooks
- URL: https://github.com/anthropics/claude-cookbooks
- Kind: Trending repository
- Meta: Jupyter Notebook · 约 48.4k Stars · Updated Jul 10, 2026
- Short Reason: 官方可运行配方适合核对 Claude API 的标准使用方式。

### Explore 6
- Title: home-assistant/core
- URL: https://github.com/home-assistant/core
- Kind: Trending repository
- Meta: Python · 约 89k Stars · Updated Jul 12, 2026
- Short Reason: 本地控制和隐私优先的成熟开源项目继续保持热度。

### Explore 7
- Title: GitHub Copilot SDK Reddit Contest Winners
- URL: https://github.com/collections/github-copilot-sdk-reddit-contest-winners
- Kind: GitHub Collection
- Meta: 11 个周末竞赛获奖项目
- Short Reason: 可用来观察开发者如何把 Copilot SDK 组合成具体产品原型。

### Explore 8
- Title: CSS
- URL: https://github.com/topics/css
- Kind: Popular topic
- Meta: GitHub 今日推荐话题
- Short Reason: Explore 不只有仓库榜单，也保留了面向前端生态的主题入口。

## Rendering Notes

- Hero 主标题建议：GitHub Trending 日报
- Hero 副标题建议：AI Agent 开始补上安全闸门，并继续进入交易、后台开发与离线知识系统
- Top 3 高亮原因：严格按 GitHub Trending 原始排名高亮 Rank 01-03，不按总 Stars 或 Stars Today 重排。
- 需要在 HTML 中诚实提示的降级点：GitHub 排名算法不公开；高权限 Agent 不是沙盒；金融项目仅作研究与教育；Wand-Enhancer Forks 异常但已由 Trending 与仓库页交叉确认；Explore 与 Trending 高度重合但抓取成功。
- UI/UX 守门意见：主叙事清晰，Hero 可在首屏说明“安全治理 + 垂直落地”；项目封面仅保留定位与关键 Meta，完整 Caveat 留在展开区；Top 3 延续原模板克制高亮；Explore 保持 8 条紧凑编号列表。
- 不允许省略的区块：主题切换、Header / Hero、4 张 Stats Cards、今日洞察、今日热门 Top 12、编程语言分布、GitHub Explore 精选、Footer。
- 必须保留的固定模板结构：`.theme-toggle`、`.container`、`.header`、`.stats-grid`、`.project-card`、`.project-details`、`.trending-list`、`.footer`，以及 `toggleDetail(btn)`、`toggleTheme()`。
- Top 详情固定顺序：
  1. 项目摘要
  2. 核心特性
  3. 技术栈
  4. 适用场景
  5. 一句话推荐
