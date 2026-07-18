# GitHub Trending 日报内容底稿

## Meta

- Report Date: 2026-07-18
- Generated At: 2026-07-18 21:15 JST
- Output Markdown: `md/github_trending_report_2026-07-18.md`
- Planned HTML: `html/github_trending_report_2026-07-18.html`
- Fixed Base Template: `.codex/skills/skill-github-trending-report/reference/fixedBaseTemplate_2026-03-16.html`
- User Rules: `.codex/skills/skill-github-trending-report/reference/user-rules.md`
- Sources:
  - https://github.com/trending?since=daily
  - https://github.com/explore
  - Top 项目的 GitHub 仓库页、README、依赖清单、官方文档和必要源码

## Page Intent

- 今日主线：开发者一边补基本功，一边把 AI 能力塞进真实工程系统；榜首是教程索引，但真正值得源码深挖的是 Agent SDK、代码关系图和电子签署工作流。
- 适合谁阅读：希望快速判断当天开源热点、找开发工具，或评估项目架构与落地风险的开发者、架构师和技术负责人。
- 页面重点：保留 GitHub 原始 Top 12 顺序，严格区分累计 Stars、Forks 与 Stars Today；资源合集与可运行系统分开看。
- 诚实降级：本报告基于 2026-07-18 GitHub Trending / Explore 页面快照与公开仓库静态证据；性能、召回率、模型质量和生产容量未做独立复测。

## Stats

- Trending 项目数：12
- 今日累计新增 Stars：4,634
- 编程语言数：9
- AI 相关项目数：9

## Editorial Insights

### Insight 1
- Title: 📚 榜首回到“从零造轮子”，一天新增 1,068 Stars
- Body: `build-your-own-x` 不是一个软件产品，而是一张大型学习路线图。它今天排名第一，说明开发者在 AI 工具大行其道时，反而更愿意补数据库、编译器、容器、搜索引擎等底层原理。热度很高，但别拿资源合集去画不存在的系统架构。

### Insight 2
- Title: 🎨 Hallmark 一天新增 1,485 Stars，AI 生成界面开始卷“品控”
- Body: Hallmark 用宏观结构、20 套主题、57 道反套路检查和自我审查来约束编码 Agent。它的意义不在于又多一个模板，而在于把“看起来不像默认 AI 页面”变成可重复执行的质量门禁；不过实际设计质量仍需要人工和项目级评测。

### Insight 3
- Title: 🧠 Agent 工程从聊天框走向 SDK、协议和权限边界
- Body: `github/copilot-sdk`、`openinterpreter` 和 `cwc-workshops` 同时上榜。前两者分别强调 JSON-RPC Agent 运行时、ACP/Codex 协议兼容与权限控制，后者展示多 Agent、记忆和评测工作坊。今天的关键词不是“能聊天”，而是能不能嵌入应用、调用工具、管理状态并在失败时收口。

### Insight 4
- Title: 🗺️ 本地代码图与压缩向量索引都在抢“少读、少存、快查”
- Body: `code-review-graph` 用 Tree-sitter、SQLite 图和增量更新缩小 AI 代码审查上下文；`turbovec` 用 TurboQuant、SIMD 和低比特存储压缩向量索引。两者都瞄准成本和延迟，但仓库自报基准应视为待复验数据，不是盖章认证。

## Top Projects

### Rank 01 - codecrafters-io/build-your-own-x
- Repo URL: https://github.com/codecrafters-io/build-your-own-x
- Tagline: 通过从零重建数据库、容器、编译器等经典技术，学习其内部原理。
- Stars: 527,763
- Stars Today: 1,068
- Forks: 49,941
- Language: Markdown
- License: 未发现明确仓库许可证
- Homepage: https://github.com/codecrafters-io/build-your-own-x
- Topics: programming, tutorials, awesome-list, tutorial-code
- 技术栈: Markdown, 多语言教程索引
- Why It Matters Today: 今日排名第一，新增 1,068 Stars，基础原理型学习资源重新占据注意力中心。
- 项目摘要: 这是按技术类别整理的“自己实现 X”教程集合，覆盖数据库、容器、Git、搜索引擎、神经网络、操作系统等主题。它帮助读者沿着真实系统拆解原理，但本身不是统一运行时或可部署产品。
- 核心特性:
  1. 按技术领域组织大量跨语言教程，便于从具体目标进入学习。
  2. 强调亲手重建，而不是只读概念说明。
  3. 社区长期维护，覆盖面广，适合搭建系统学习路线。
- 适用场景: 自学计算机系统、准备技术面试、寻找教学项目；不适合直接当生产组件或架构框架。
- 一句话推荐: 这是“造轮子说明书大全”，不是把目录一克隆，数据库和浏览器就自己长出来。
- Evidence Notes: GitHub Trending 原始排名、Stars、Forks、Stars Today；GitHub Explore 与仓库 README/目录。
- Honest Caveat: 教程质量、时效和完整度各不相同；仓库未形成统一的软件架构，也未发现明确许可证声明。

### Rank 02 - PostHog/posthog
- Repo URL: https://github.com/PostHog/posthog
- Tagline: 集产品分析、会话回放、功能开关、实验、错误追踪、日志和 AI 可观测性于一体的平台。
- Stars: 36,319
- Stars Today: 438
- Forks: 3,012
- Language: Python
- License: MIT（`ee` 目录另有许可）
- Homepage: https://posthog.com
- Topics: analytics, session-replay, feature-flags, experiments, data-warehouse, ai-observability
- 技术栈: Python, TypeScript/React, 数据摄取与分析管线, SDK, MCP
- Why It Matters Today: 今日新增 438 Stars；产品数据平台正继续向 Agent 主动诊断和自动修复延伸。
- 项目摘要: PostHog 把用户行为事件、回放、错误、日志、特性开关和数据仓库放到同一产品体系，并用 self-driving 模式把异常信号转成研究报告或待审核 PR。官方推荐云服务，开源自托管定位为高级用户的 hobby 部署。
- 核心特性:
  1. 产品分析、Web 分析、会话回放、实验和功能开关共用产品上下文。
  2. SDK、API、Slack、Web、桌面和 MCP 提供多种操作入口。
  3. 自托管脚本可快速启动，但官方明确给出容量和支持边界。
- 适用场景: 产品增长分析、实验平台、错误诊断、LLM 应用追踪；大规模生产自托管需独立容量规划。
- 一句话推荐: 像一间产品数据百货商场，东西齐全；自己开分店之前，先看看仓库、电梯和消防够不够用。
- Evidence Notes: GitHub Trending；官方 README 的产品模块、自托管说明、SDK/MCP 和许可证边界。
- Honest Caveat: README 提到的自托管约 10 万事件/月为官方说明，不是本报告独立压测结果；云版与开源版能力并非完全相同。

### Rank 03 - HenryNdubuaku/maths-cs-ai-compendium
- Repo URL: https://github.com/HenryNdubuaku/maths-cs-ai-compendium
- Tagline: 从数学、计算机系统到现代 AI 推理与 ML 系统设计的开放教材。
- Stars: 6,801
- Stars Today: 200
- Forks: 820
- Language: TypeScript
- License: 未发现明确仓库许可证
- Homepage: https://henryndubuaku.github.io/maths-cs-ai-compendium/
- Topics: mathematics, computer-science, machine-learning, ai, education
- 技术栈: Markdown 教材, TypeScript/MCP Server, GitHub Pages
- Why It Matters Today: 今日新增 200 Stars，长篇、体系化、直觉优先的 AI 工程知识仍然稀缺。
- 项目摘要: 这是覆盖向量、矩阵、概率、机器学习、视觉、语音、GPU、推理和 ML 系统设计的开放教材。仓库带本地 MCP Server，可让 AI 助手检索教材，但主体仍是教育内容而非软件平台。
- 核心特性:
  1. 从基础数学一路延伸到生产软件、GPU 和推理系统。
  2. 强调直觉、真实背景和代码实现，而非只给公式。
  3. 提供 MCP 接入，让本地 AI 助手把教材作为知识库使用。
- 适用场景: AI/ML 系统化学习、补数学与系统基础、面试准备；不适合作为经过同行评审的标准教材替代品。
- 一句话推荐: 内容像一整桌自助餐，吃得下很补；别因为盘子多，就以为每道菜都经过学术期刊盖章。
- Evidence Notes: GitHub Trending；仓库 README 的章节目录、定位、在线阅读与 MCP Server 说明。
- Honest Caveat: 多项教育与个人经历叙述属于作者自述；仓库未发现明确许可证，复用内容前应核实授权。

### Rank 04 - Nutlope/hallmark
- Repo URL: https://github.com/Nutlope/hallmark
- Tagline: 为 Claude Code、Cursor 和 Codex 提供的反“AI 套路页面”设计 Skill。
- Stars: 12,396
- Stars Today: 1,485
- Forks: 618
- Language: CSS
- License: MIT
- Homepage: https://www.usehallmark.com
- Topics: design-skill, claude-code, cursor, codex, web-design
- 技术栈: Agent Skill, Markdown 规则, HTML/CSS, 主题系统, 质量检查门禁
- Why It Matters Today: 今日新增 1,485 Stars，是 Top 12 增速最高项目，说明 AI 前端质量控制成为显性需求。
- 项目摘要: Hallmark 在生成页面前选择宏观结构和主题，在交付前执行 57 项反套路检查与自我审查。它提供 build、audit、redesign、study 四类工作方式，目标是让不同 brief 产出真正不同的页面结构，而不是只换颜色。
- 核心特性:
  1. 20 套主题与 Custom 分支，根据 brief 选择结构与视觉语言。
  2. `audit` 只给问题清单，`redesign` 重建结构，`study` 提取设计 DNA。
  3. 可用 `npx skills add nutlope/hallmark` 安装到兼容编码 Agent。
- 适用场景: AI 辅助落地页、营销页、设计审计与改版探索；关键品牌项目仍需设计师复核。
- 一句话推荐: 它不是给 AI 换件西装，是先检查 AI 有没有又穿着同一件“渐变紫色工服”来上班。
- Evidence Notes: GitHub Trending；README 的四个 verbs、20 themes、57 gates、安装方法与 MIT 许可证。
- Honest Caveat: “不像 AI 生成”是审美目标而非客观标准；示例效果不能替代真实业务、无障碍和转化率验证。

### Rank 05 - github/copilot-sdk
- Repo URL: https://github.com/github/copilot-sdk
- Tagline: 将 GitHub Copilot Agent 工作流嵌入应用和服务的多语言 SDK。
- Stars: 9,844
- Stars Today: 233
- Forks: 1,336
- Language: Java
- License: MIT
- Homepage: https://github.com/github/copilot-sdk
- Topics: copilot, agent-runtime, sdk, json-rpc, tool-calling
- 技术栈: TypeScript, Python, Go, .NET, Java, Rust, Copilot CLI, JSON-RPC
- Why It Matters Today: 今日新增 233 Stars；Agent 能力正在从独立 CLI 变成应用可调用的基础设施。
- 项目摘要: Copilot SDK 封装与 Copilot CLI server mode 的 JSON-RPC 通信，负责启动或连接运行时、创建会话、流式接收事件、处理权限请求和自定义工具。官方同时提供六种语言实现，并支持 GitHub 登录令牌或 BYOK。
- 核心特性:
  1. 应用通过 SDK 创建会话，运行时处理规划、工具调用、文件编辑和事件。
  2. SDK 可自动管理 CLI 子进程，也可连接外部 server mode。
  3. 支持自定义 Agent、Skill、MCP、工具、Hooks 与权限处理器。
- 适用场景: 在桌面应用、后台服务、开发工具中嵌入 Copilot Agent；需评估订阅、认证、权限和运行时隔离。
- 一句话推荐: 以前 Agent 住在终端里，现在 SDK 给它办了“应用内营业执照”，但权限章得你自己盖清楚。
- Evidence Notes: GitHub Trending；官方 README、Getting Started、`nodejs/src/client.ts`、`nodejs/src/session.ts`。
- Honest Caveat: 使用标准 Copilot 路径通常涉及订阅与用量计费；BYOK、模型可用性和工具权限依部署配置而变。

### Rank 06 - anthropics/cwc-workshops
- Repo URL: https://github.com/anthropics/cwc-workshops
- Tagline: Anthropic Code with Claude 活动使用的 Agent、评测、记忆和多 Agent 工作坊材料。
- Stars: 1,664
- Stars Today: 45
- Forks: 491
- Language: TypeScript
- License: Apache-2.0
- Homepage: https://github.com/anthropics/cwc-workshops
- Topics: claude, workshops, managed-agents, mcp, evals
- 技术栈: TypeScript, Python, React/Next.js, Streamlit, MCP, Managed Agents
- Why It Matters Today: 今日增量不高但进入 Top 12，说明开发者希望看到 Agent 从 Demo 走向分解、记忆和评测的完整练习。
- 项目摘要: 仓库汇集 Anthropic 主办工作坊材料，覆盖模型选择、Agent 分解、记忆、评测驱动开发、生产研究台和多 Agent 协作。它明确标注不维护、不接受贡献，定位是教学快照。
- 核心特性:
  1. 每个 workshop 围绕一个可操作的 Agent 工程主题。
  2. 多个案例带评测、工具调用、MCP 和记忆模块。
  3. 可用于复盘官方活动流程和教学设计。
- 适用场景: 团队培训、Agent 课程设计、概念验证；不适合直接依赖为长期维护的生产框架。
- 一句话推荐: 这是培训班留下的全套讲义，不是售后七年的企业中间件。
- Evidence Notes: GitHub Trending；官方 README 的 workshop 清单、维护状态与 Apache-2.0 许可证。
- Honest Caveat: 仓库明确不维护，外部 API 和依赖可能随时间失效，使用时要自行修正。

### Rank 07 - PrismML-Eng/Bonsai-demo
- Repo URL: https://github.com/PrismML-Eng/Bonsai-demo
- Tagline: 在 macOS、Linux、Windows 或 CPU 上运行 1-bit 与 ternary Bonsai 模型的本地演示仓库。
- Stars: 1,768
- Stars Today: 278
- Forks: 170
- Language: Shell
- License: Apache-2.0
- Homepage: https://prismml.com
- Topics: bonsai, mlx, llm, small-models, llamacpp
- 技术栈: Shell/PowerShell, llama.cpp, MLX, GGUF, CUDA/Metal/Vulkan/ROCm
- Why It Matters Today: 今日新增 278 Stars；低比特本地模型、视觉输入和工具调用继续吸引端侧部署关注。
- 项目摘要: 该仓库提供下载、编译和运行脚本，让用户选择 Bonsai 或 Ternary-Bonsai 的 27B、8B、4B、1.7B 模型。27B 路线宣称支持视觉、工具调用、推理预算和长上下文，并通过 llama.cpp/MLX 适配多硬件。
- 核心特性:
  1. `setup.sh` / `setup.ps1` 完成依赖、模型和二进制准备。
  2. 支持模型家族和尺寸切换，多后端本地运行。
  3. README 明确列出上游格式迁移与不同 GGUF 变体兼容状态。
- 适用场景: 本地模型试用、硬件兼容验证、低比特推理研究；生产部署前需复核模型许可、质量和硬件基准。
- 一句话推荐: 它把“下载一堆神秘二进制”整理成了能走的路，但路牌上写的速度，最好自己开一圈再信。
- Evidence Notes: GitHub Trending；README 的 Quick Start、模型矩阵、后端状态、工具调用说明与 Apache-2.0 代码许可证。
- Honest Caveat: 模型文件可能有独立许可和访问条件；性能、长上下文和质量主张未由本报告独立验证。

### Rank 08 - protocolbuffers/protobuf
- Repo URL: https://github.com/protocolbuffers/protobuf
- Tagline: Google 的跨语言结构化数据交换格式、编译器和运行时实现。
- Stars: 71,569
- Stars Today: 11
- Forks: 16,194
- Language: C++
- License: BSD-3-Clause
- Homepage: https://protobuf.dev
- Topics: serialization, protobuf, protoc, rpc, protocol-compiler
- 技术栈: C++, Bazel/CMake, protoc, 多语言运行时
- Why It Matters Today: 今日新增只有 11 Stars，却仍上榜，说明成熟基础设施也会因生态事件或版本活动重新进入视野。
- 项目摘要: Protocol Buffers 通过 `.proto` Schema 定义数据结构，由 `protoc` 生成多语言代码，用紧凑二进制格式在存储和通信场景交换数据。它是成熟基础设施，而非今日新出现的项目。
- 核心特性:
  1. Schema 优先、跨语言代码生成和向后兼容演进机制。
  2. 多语言官方运行时与广泛 RPC/存储生态集成。
  3. 编译器、库、测试与规范长期维护。
- 适用场景: 服务协议、配置和持久化数据结构；不适合需要人类可读文本或完全无 Schema 的快速交换。
- 一句话推荐: 它今天没冲刺，是老将散步也进了前十二——基础设施的江湖地位摆在那儿。
- Evidence Notes: GitHub Trending；官方仓库、protobuf.dev 与 BSD-3-Clause 许可证。
- Honest Caveat: 具体语言版本、Edition 与兼容规则应以对应 Release 和语言文档为准，本报告未展开版本迁移细节。

### Rank 09 - tirth8205/code-review-graph
- Repo URL: https://github.com/tirth8205/code-review-graph
- Tagline: 本地优先的代码知识图，通过 MCP/CLI 为 AI 审查提供最小必要上下文。
- Stars: 19,905
- Stars Today: 74
- Forks: 2,113
- Language: Python
- License: MIT
- Homepage: https://code-review-graph.com
- Topics: tree-sitter, mcp, static-analysis, knowledge-graph, code-review
- 技术栈: Python, Tree-sitter, SQLite/WAL, NetworkX, FastMCP, Watchdog
- Why It Matters Today: 今日新增 74 Stars；大型代码库里“让 Agent 少读无关文件”已经成为独立工程问题。
- 项目摘要: 项目解析仓库 AST，把文件、类、函数、调用、继承和测试关系写入 SQLite 图；文件变化时增量重建，再通过 MCP 暴露影响半径、审查上下文、流程和查询工具。它强调本地运行，不把源码发到外部服务。
- 核心特性:
  1. Tree-sitter 多语言解析，节点与边持久化到 SQLite。
  2. Git diff、文件哈希、Watch 模式和 Hooks 支持增量更新。
  3. MCP 工具返回影响半径、最小上下文、流程与风险信息。
- 适用场景: 大仓库 AI 代码审查、影响分析、Agent 导航和本地 CI；语义完整度需按语言与框架验证。
- 一句话推荐: 它像先给代码库画地图，再让 Agent 出门；比蒙着眼把整个仓库背一遍省事多了。
- Evidence Notes: GitHub Trending；README、`pyproject.toml`、`code_review_graph/main.py`、`graph.py`、`incremental.py`。
- Honest Caveat: 约 82 倍中位数上下文缩减为项目自有评测结果；静态图无法自动理解所有动态调用、反射和运行时配置。

### Rank 10 - docusealco/docuseal
- Repo URL: https://github.com/docusealco/docuseal
- Tagline: 可自托管的开源文档填写和电子签署平台。
- Stars: 17,951
- Stars Today: 91
- Forks: 1,774
- Language: Ruby
- License: AGPLv3 + Section 7(b) Additional Terms
- Homepage: https://www.docuseal.com
- Topics: pdf, e-signature, self-hosted, ruby-on-rails, document-signing
- 技术栈: Ruby on Rails, Hotwire/Turbo, Active Storage, SQLite/PostgreSQL/MySQL, Sidekiq, SMTP
- Why It Matters Today: 今日新增 91 Stars；电子签署的自托管、API 集成和数据控制需求保持稳定。
- 项目摘要: DocuSeal 提供 PDF 表单构建、多签署人、移动端填写、邮件通知、签名验证、API 和 Webhook。默认 Docker 部署使用 SQLite，也支持 PostgreSQL/MySQL；文件可落磁盘或对象存储。
- 核心特性:
  1. WYSIWYG 字段编辑、多签署人顺序与公开签署链接。
  2. 表单值验证、签署完成事件、异步完成任务和搜索重建。
  3. API、Webhook、SMTP 与多种存储后端便于嵌入业务系统。
- 适用场景: 合同、授权书、表单签署和嵌入式签署；强监管场景需独立做身份、审计、地区法律和灾备评估。
- 一句话推荐: 自托管确实能把钥匙拿回自己手里，但合规、备份和送达证明也不会顺便替你下班。
- Evidence Notes: GitHub Trending；README、Gemfile、`config/routes.rb`、`SubmitFormController` 与 `Submitters::SubmitValues`。
- Honest Caveat: 许可证包含额外条款；不同地区电子签名法律效力与高级商业功能需要单独核实。

### Rank 11 - openinterpreter/openinterpreter
- Repo URL: https://github.com/openinterpreter/openinterpreter
- Tagline: 面向 Kimi K3 等开放模型、兼容 ACP 与 Codex 执行协议的 Rust 编码 Agent。
- Stars: 66,551
- Stars Today: 431
- Forks: 5,716
- Language: Rust
- License: Apache-2.0
- Homepage: https://www.openinterpreter.com
- Topics: rust, acp, kimi, qwen, deepseek, coding-agent
- 技术栈: Rust, Codex exec protocol, ACP, MCP, native sandboxing, TUI
- Why It Matters Today: 今日新增 431 Stars；低成本模型要发挥效果，Agent harness 和协议兼容正在变成关键竞争点。
- 项目摘要: 新版 Open Interpreter 基于 Codex 的 Rust 实现，重点是复刻不同模型提供商推荐的 Agent harness。它支持在 TUI 内切换 harness/model，以 ACP 接入编辑器，并与 Codex SDK 保持执行协议兼容。
- 核心特性:
  1. 多种模型 harness 可运行时切换。
  2. ACP、Codex exec、MCP、Skills、Hooks 和权限机制并存。
  3. macOS、Linux、Windows 原生沙箱，配置与会话状态保存在本地。
- 适用场景: 开放模型编码 Agent、编辑器接入、harness 对比和本地自动化；高权限命令执行必须使用审批与沙箱。
- 一句话推荐: 同一位演员换不同导演，效果真可能差一截；不过让它碰终端之前，保安制度先别省。
- Evidence Notes: GitHub Trending；官方 README 的 Rust/Codex 基础、harness、ACP、沙箱和本地状态说明。
- Honest Caveat: “低成本模型最佳表现”与各 harness 效果依模型版本和任务而变；命令执行具有真实系统风险。

### Rank 12 - RyanCodrai/turbovec
- Repo URL: https://github.com/RyanCodrai/turbovec
- Tagline: 基于 TurboQuant 的 Rust 向量索引，提供 Python 绑定、低比特压缩与 SIMD 搜索。
- Stars: 13,420
- Stars Today: 280
- Forks: 1,182
- Language: Python
- License: MIT
- Homepage: https://github.com/RyanCodrai/turbovec
- Topics: rust, python, simd, vector-search, quantization, rag
- 技术栈: Rust, PyO3/Maturin, TurboQuant, NEON, AVX-512/AVX2, 本地文件持久化
- Why It Matters Today: 今日新增 280 Stars；RAG 和检索系统正在持续追求更低内存、更快本地搜索与在线增量写入。
- 项目摘要: turbovec 把向量归一化、随机旋转、低比特标量量化和长度校正结合起来，提供可在线 `add`、过滤搜索、稳定外部 ID 和索引持久化。Rust 内核通过 Python 绑定接入常见 RAG 框架。
- 核心特性:
  1. 2-bit/4-bit 压缩，不需要独立训练阶段。
  2. ARM NEON 与 x86 SIMD 内核，支持 allowlist 在内核内过滤。
  3. Rust/Python API、文件写入加载和多框架适配。
- 适用场景: 本地或内网 RAG、内存敏感向量检索、混合检索重排；替换生产索引前需验证召回、并发和数据恢复。
- 一句话推荐: 它想把向量索引从“大衣柜”压成“登机箱”，但你的数据能不能都装下，还得自己称重。
- Evidence Notes: GitHub Trending；README 的 API、算法、SIMD、基准、持久化说明与 MIT 许可证。
- Honest Caveat: 与 FAISS 的速度和召回对比来自项目自测；硬件、维度、数据分布和参数变化可能显著改变结果。

## Language Distribution

| Language | Count | Share |
|---|---:|---:|
| Python | 3 | 25.0% |
| TypeScript | 2 | 16.7% |
| Markdown | 1 | 8.3% |
| CSS | 1 | 8.3% |
| Java | 1 | 8.3% |
| Shell | 1 | 8.3% |
| C++ | 1 | 8.3% |
| Ruby | 1 | 8.3% |
| Rust | 1 | 8.3% |

## GitHub Explore 补充

> Explore 页面与 Trending 高度重合，以下内容只作为编辑补充，不参与 Top 12 排名、Stars Today 汇总或语言统计。

1. **Rubber Duck Thursdays** — GitHub 推荐的开源直播活动，强调轻量协作与现场编码。
2. **codecrafters-io/build-your-own-x** — Explore 同时推荐该仓库，并标注 programming、tutorials、awesome-list 等主题。
3. **PostHog/posthog** — Explore 强调产品分析、回放、功能开关、数据仓库和 AI 分析主题。
4. **GitHub Checkout：Fixing merge conflicts and PRs with Copilot cloud agent** — 演示云端 Agent 处理冲突与 PR。
5. **Popular topic: Node.js** — Explore 当日推荐的热门技术主题。
6. **Nutlope/hallmark** — 反 AI 套路设计 Skill，与当天最高 Stars Today 增量相呼应。
7. **Learn to Code collection** — GitHub 官方学习编程资源集合。
8. **Mokuren for GitHub** — GitHub staff 推荐的 Issue 侧栏组织工具。

## Architecture Analysis Selection

### Selected

1. `github/copilot-sdk` — 多语言 SDK、JSON-RPC 运行时、会话、权限和工具链路证据完整。
2. `tirth8205/code-review-graph` — Tree-sitter 解析、SQLite 图、增量更新和 MCP 查询形成清晰端到端系统。
3. `docusealco/docuseal` — Rails Web 应用、公开签署入口、事务校验、异步完成任务与存储集成适合业务链路分析。

### Not Selected

- `codecrafters-io/build-your-own-x`：资源索引，不是统一软件系统。
- `PostHog/posthog`：系统非常庞大，本轮时间窗口内无法在不牺牲证据质量的前提下追完整主线。
- `HenryNdubuaku/maths-cs-ai-compendium`：主体是教材，MCP 仅为附属能力。
- `Nutlope/hallmark`：核心是 Skill 与规则资产，运行时主要由宿主 Agent 提供。
- `anthropics/cwc-workshops`：教学材料集合且明确不维护。
- `PrismML-Eng/Bonsai-demo`：以模型下载和演示脚本为主，模型权重与上游运行时占主导。
- `protocolbuffers/protobuf`：成熟且值得研究，但体量跨多语言，今日增量低，优先级让给新兴工具。
- `openinterpreter/openinterpreter`：架构可分析，但与 Copilot SDK 同属 Agent 运行时方向，本轮避免重复。
- `RyanCodrai/turbovec`：算法与内核很有价值，但今日深挖名额优先保证业务系统和工具链多样性。

## Evidence Notes

- GitHub Trending 使用 `Repositories / Any language / Today` 页面，保留页面原始前 12 名；第 13、14 名未纳入。
- Stars 表示累计 Stars；Stars Today 表示当日 Trending 页面显示的新增数；两者未混用。
- GitHub Explore 成功抓取，只作为补充，不进入排名和统计。
- 项目能力优先依据仓库源码、依赖清单和官方 README；性能或效果数字均标注为项目自报。
- 深度分析为静态源码和官方资料研究，不声称已经本地编译、运行或压测。

## Honest Caveat

- Trending 是时点快照，Stars 与页面内容可能在当天继续变化。
- AI 相关项目数是编辑分类：凡核心定位直接涉及 LLM、Agent、AI 教育、代码智能或向量检索的项目计入；它不是 GitHub 官方标签统计。
- 许可证摘要仅用于风险提示，不能替代法律意见；特别是未声明许可、混合许可和附加条款项目。
- `code-review-graph`、`turbovec`、Bonsai 等项目的性能和质量主张未由本报告独立复测。

## Markdown Acceptance Checklist

- [x] 报告日期、来源和输出路径完整。
- [x] Top 12 数量为 12，原始顺序未改变。
- [x] 每个项目包含 Stars、Stars Today、Forks、Language、License、摘要、特性、场景、推荐和限制。
- [x] Stars Today 合计为 4,634。
- [x] 语言分布合计为 12，语言种类为 9。
- [x] Explore 与 Trending 排名统计明确分离。
- [x] 深度分析选择为 3 个真实软件系统。
- [x] 未将 README 宣传语、项目自测或目录名冒充已验证事实。
