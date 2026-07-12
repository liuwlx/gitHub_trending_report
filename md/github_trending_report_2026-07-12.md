# GitHub Trending 日报内容底稿

## Meta

- Report Date: 2026-07-12
- Generated At: 2026-07-12 14:25:58 JST
- Output Markdown: md/github_trending_report_2026-07-12.md
- Planned HTML: html/github_trending_report_2026-07-12.html
- Fixed Base Template: .codex/skills/skill-github-trending-report/reference/fixedBaseTemplate_2026-03-16.html
- User Rules: .codex/skills/skill-github-trending-report/reference/user-rules.md
- Data Scope: GitHub Trending · Repositories · Any language · Today
- Sources:
  - https://github.com/trending
  - https://github.com/explore
  - Repo README / About / Homepage / Release pages
  - GitHub 公开仓库元数据与本次会话的公开网页抓取结果

## Page Intent

- 今日主线：AI 编程工具正在从“聊天辅助”走向可安装的插件、Skills 与本地执行能力；与此同时，C++、基础设施、CI 和家庭自动化等成熟底座项目集体回榜。
- 适合谁阅读：希望快速发现开发工具、AI 工程、基础设施与底层库变化的软件工程师、技术负责人和开源观察者。
- 页面重点：保留 GitHub Trending 原始 Top 12 顺序，同时单独提醒“原始排名不等于当日增星速度”。
- 需要诚实降级说明的地方：GitHub Trending 排名算法不公开；Explore 当前与 Trending 高度重合；部分仓库的许可证或性能表述需要读者进一步核验。

## Stats

- Trending 项目数：12
- 今日累计新增 Stars：2,902
- 编程语言数：6
- AI 相关项目数：4

## Editorial Insights

### Insight 1
- Title: AI 编程开始“装插件、装技能、接本地工具”
- Body: `claude-code-templates`、`stitch-skills`、`openai/plugins` 与 `DesktopCommanderMCP` 分别覆盖配置目录、可复用 Skills、插件示例和本地终端/文件操作。今天的共同信号不是“又多了几个 Prompt”，而是 AI 编程能力正在变成可安装、可组合、可治理的工程资产。

### Insight 2
- Title: 老牌底层项目集体回榜，说明工程基本功仍然吃香
- Body: Catch2、Abseil、Terraform、meshoptimizer、Asio 与 actions/checkout 横跨测试、通用库、基础设施、图形优化、异步 I/O 和 CI。AI 再热，生产系统最后仍要落到可测试、可部署、可维护的底座上；今天这张榜单像一桌酒席，AI 坐主桌，基础设施掌勺。

### Insight 3
- Title: GitHub 原始排名与今日增星速度不是一回事
- Body: 榜首 Catch2 今日新增 113 Stars，而第 8 名 DesktopCommanderMCP 新增 909，第 10 名 Bun 新增 658。看榜时应同时看“平台排序”和“当日增量”：前者反映综合趋势，后者更容易发现突然加速的项目。

### Insight 4
- Title: 热度之外，权限与许可证值得单独看一眼
- Body: Terraform 当前采用 Business Source License 1.1；DesktopCommanderMCP 能操作终端和文件系统；actions/checkout v7 又在强化高风险触发场景的默认保护；`openai/plugins` 仓库概览没有清晰显示统一许可证。星标负责招手，边界负责不让你踩坑。

## Top Projects

### Rank 01 - catchorg/Catch2
- Repo URL: https://github.com/catchorg/Catch2
- Tagline: 现代 C++ 测试框架，用接近自然语言的断言和 Section 组织测试，也提供基础微基准能力。
- Stars: 21,102
- Stars Today: 113
- Forks: 3,428
- Language: C++
- License: BSL-1.0
- Homepage: https://github.com/catchorg/Catch2
- Topics: testing, framework, tdd, cpp, bdd, cpp14, test-framework, no-dependencies
- 技术栈: C++14+, CMake, unit testing, BDD macros, micro-benchmarking
- Why It Matters Today: 一个成熟测试框架重新登顶，说明开发者仍在集中关注“让 C++ 代码更容易验证”这件基础而高频的事。
- 项目摘要: Catch2 是面向现代 C++ 的单元测试框架。它把断言、测试分段、BDD 风格描述和基础基准测试放在一套轻量接口里，适合希望降低测试样板代码、又不想引入庞大测试基础设施的 C++ 团队。
- 核心特性:
  1. 断言表达式直接、可读，失败时能给出较清楚的表达式展开与上下文。
  2. 通过 `SECTION` 复用测试准备逻辑，减少同类测试重复搭脚手架。
  3. 同时提供 BDD 宏与基础微基准，能覆盖行为描述和小范围性能回归检查。
- 适用场景: C++ 库、桌面程序、游戏或系统组件的单元测试；需要从零建立测试体系的中小项目；希望用较低接入成本补齐回归测试的团队。
- 一句话推荐: 想让 C++ 测试少写架子、多写判断，Catch2 是今天最该先点开的成熟选项。
- Evidence Notes: README 明确将其定义为 C++ 单元测试框架，支持基础 micro-benchmarking 与 BDD macros；GitHub About 显示 BSL-1.0 和测试相关 Topics；页面显示 2026-07-07 发布 v3.15.2。
- Honest Caveat: “轻量”不等于所有项目都零迁移成本；大型代码库仍需评估测试发现、编译时间和现有框架兼容性。

### Rank 02 - abseil/abseil-cpp
- Repo URL: https://github.com/abseil/abseil-cpp
- Tagline: Google 开源的 C++17 通用基础库，为标准库补充字符串、容器、时间、同步等常用能力。
- Stars: 17,831
- Stars Today: 118
- Forks: 3,209
- Language: C++
- License: Apache-2.0
- Homepage: https://abseil.io/
- Topics: c-plus-plus, cpp17, library, google, utilities
- 技术栈: C++17, CMake, Bazel, containers, strings, synchronization, time
- Why It Matters Today: Abseil 的价值不在“新奇”，而在大量生产环境验证过的基础能力重新获得关注，适合观察 C++ 工程实践的共同底座。
- 项目摘要: Abseil 是一组从 Google 大型 C++ 代码库中沉淀出的通用组件，目标是补充而不是取代 C++ 标准库。它适合需要稳定的字符串处理、哈希容器、时间、状态值和并发原语，又希望保持一致工程风格的团队。
- 核心特性:
  1. 提供大量标准库尚未覆盖或使用体验不够统一的常用组件。
  2. 组件长期在大规模生产代码中使用和测试，强调兼容性与工程可靠性。
  3. 支持 CMake 与 Bazel 等主流构建方式，便于接入既有 C++ 工程。
- 适用场景: 大型 C++ 服务、基础库、跨平台客户端和需要统一基础组件规范的团队；尤其适合已经在使用 Google 风格 C++ 工程体系的项目。
- 一句话推荐: 它不是闪亮的新玩具，而是能少造一批轮子的 C++ 工具箱。
- Evidence Notes: 官方 README 将其定义为 C++17 库集合，用于增强标准库，并说明代码来源于 Google 内部代码库且在生产环境广泛测试；许可证为 Apache-2.0。
- Honest Caveat: 引入 Abseil 会带来一套较大的基础依赖；小型项目应先确认真正需要哪些组件，避免为了一个工具函数搬来整间仓库。

### Rank 03 - davila7/claude-code-templates
- Repo URL: https://github.com/davila7/claude-code-templates
- Tagline: 面向 Claude Code 的配置、Agent、Command、Skill、Hook 与 MCP 管理工具和模板目录。
- Stars: 29,056
- Stars Today: 232
- Forks: 3,187
- Language: Python
- License: MIT
- Homepage: https://aitmpl.com/
- Topics: claude, anthropic, anthropic-claude, claude-code
- 技术栈: Python, CLI, Claude Code, MCP, Agents, Skills, Hooks
- Why It Matters Today: Claude Code 周边正在从“个人配置文件”成长为可以搜索、安装、监控和复用的生态目录，这个项目正好站在入口位置。
- 项目摘要: `claude-code-templates` 是一个面向 Claude Code 的配置与资源管理工具。它把社区 Agent、Commands、Skills、Hooks、MCP 配置和项目设置集中起来，帮助开发者少翻帖子、少手工复制文件，更快搭出符合自己工作流的 Claude Code 环境。
- 核心特性:
  1. 通过 CLI 搜索和安装 Claude Code 相关模板与扩展资源。
  2. 覆盖 Agent、Command、Skill、Hook、MCP 和 Settings 等多个配置层。
  3. 提供监控与目录化浏览入口，便于比较社区方案而不是逐个仓库摸索。
- 适用场景: Claude Code 重度用户；需要为团队统一配置、命令与 Agent 角色的技术负责人；希望快速试用 MCP 或 Skills 的开发者。
- 一句话推荐: Claude Code 配置越堆越多时，它像一个工具柜；比把螺丝刀都扔桌上强多了。
- Evidence Notes: GitHub About 明确写明是“CLI tool for configuring and monitoring Claude Code”；主页为 aitmpl.com；Topics 聚焦 Claude/Anthropic；仓库内容展示 Skills、Agents、Commands & Tools 等分类。
- Honest Caveat: 目录里的模板质量和安全边界不一定一致，安装前仍应查看来源、脚本内容、权限和维护状态。

### Rank 04 - google-labs-code/stitch-skills
- Repo URL: https://github.com/google-labs-code/stitch-skills
- Tagline: 围绕 Google Stitch 的 Agent Skills 与插件，让多种编码 Agent 具备设计生成、设计系统和代码组件工作流。
- Stars: 7,113
- Stars Today: 340
- Forks: 947
- Language: TypeScript
- License: Apache-2.0
- Homepage: https://github.com/google-labs-code/stitch-skills
- Topics: agent-skills, stitch, design-to-code, mcp, claude-code, codex, gemini-cli
- 技术栈: TypeScript, Agent Skills, MCP, Stitch, React, design-to-code
- Why It Matters Today: Skills 正在成为跨 Agent 复用能力的包装方式；这个仓库同时覆盖 Codex、Gemini CLI、Claude Code、Cursor 等环境，代表“能力包跨工具迁移”的方向。
- 项目摘要: `stitch-skills` 为 Google Stitch 相关工作流提供可安装的 Agent Skills 和插件。它不是单纯放几段 Prompt，而是把设计生成、从代码同步设计、提取 HTML、生成组件和维护设计系统等任务包装成 Agent 可以调用的流程。
- 核心特性:
  1. 提供 `stitch-design`、`stitch-build`、`stitch-utilities` 等分组插件。
  2. 支持从代码到设计、设计到组件、设计系统生成与页面提取等工作流。
  3. 按开放的 Agent Skills 形式组织，可在多种主流编码 Agent 中使用。
- 适用场景: 设计与前端协作团队；正在尝试 Stitch MCP 的开发者；希望把设计生成和组件生产流程交给 Agent 执行的产品工程团队。
- 一句话推荐: 这是“Agent 会用设计工具”迈向“Agent 按流程做设计工程”的一块拼图。
- Evidence Notes: README 明确说明 Skills 面向 Stitch MCP，并列出 Codex、Antigravity、Gemini CLI、Claude Code、Cursor 等兼容环境；仓库为 Apache-2.0。
- Honest Caveat: 仓库明确注明并非 Google 官方支持产品；能力效果还依赖 Stitch 服务、模型和具体 Agent 环境。

### Rank 05 - hashicorp/terraform
- Repo URL: https://github.com/hashicorp/terraform
- Tagline: 用声明式配置描述、计划并变更云和本地基础设施的 Infrastructure as Code 工具。
- Stars: 49,388
- Stars Today: 229
- Forks: 10,682
- Language: Go
- License: Business Source License 1.1
- Homepage: https://developer.hashicorp.com/terraform
- Topics: cloud, graph, terraform, cloud-management, infrastructure-as-code
- 技术栈: Go, HCL, provider plugins, dependency graph, infrastructure as code
- Why It Matters Today: IaC 仍是云工程的核心基础设施；Terraform 回榜说明多云资源管理、计划审阅和可重复交付依然是团队的刚需。
- 项目摘要: Terraform 允许团队用配置文件声明基础设施，再通过执行计划预览变化，并按依赖图创建、更新或销毁资源。它把手工点控制台变成可以审查、版本化和重复执行的工程流程。
- 核心特性:
  1. 执行计划在变更前展示将新增、修改或删除的资源。
  2. 通过资源依赖图并行处理无依赖操作，并按正确顺序执行关联变更。
  3. Provider 插件连接不同云厂商、SaaS 和本地平台，保持统一工作流。
- 适用场景: 多云或混合云基础设施；需要代码审查和审计的运维团队；希望把环境创建、灾备恢复和变更流程标准化的组织。
- 一句话推荐: 当基础设施不能再靠“谁记得上次点了什么”，Terraform 就该上场了。
- Evidence Notes: 官方 README 说明 Terraform 通过配置、执行计划、资源图和变更自动化管理基础设施；GitHub 显示 BSL-1.1；官方文档站为 developer.hashicorp.com/terraform。
- Honest Caveat: BSL-1.1 属于 source-available，并非传统 OSI 开源许可证；商业托管、竞争性服务和再分发场景必须先核对许可条款。

### Rank 06 - zeux/meshoptimizer
- Repo URL: https://github.com/zeux/meshoptimizer
- Tagline: 优化、简化和压缩三角网格，减少 GPU 顶点处理、存储和传输成本。
- Stars: 8,151
- Stars Today: 110
- Forks: 786
- Language: C++
- License: MIT
- Homepage: https://meshoptimizer.org/
- Topics: compression, gpu, optimization, simplification, gltf, mesh-processing
- 技术栈: C++, WebAssembly/JavaScript bindings, Rust crate, glTF, GPU mesh pipeline
- Why It Matters Today: 实时 3D、游戏和 Web 图形对资产体积与渲染效率越来越敏感；该库提供的是能直接嵌入资产管线的底层算法，而不是只给一篇论文。
- 项目摘要: `meshoptimizer` 是一套面向三角网格的优化库，覆盖顶点缓存、过度绘制、顶点获取、简化与压缩。它帮助 3D 资产在视觉质量尽量不变的前提下，更快加载、更少占内存，并降低 GPU 处理成本。
- 核心特性:
  1. 对索引和顶点数据重新排序，改善 GPU 顶点缓存和内存访问效率。
  2. 支持网格简化、LOD 与压缩，适合大型场景和网络传输。
  3. 除 C/C++ 接口外，还提供 JavaScript、Rust 等生态入口，并配套 `gltfpack` 工具。
- 适用场景: 游戏引擎、数字孪生、WebGL/WebGPU、AR/VR 和 glTF 资产生产管线；需要批量压缩与优化模型的内容平台。
- 一句话推荐: 3D 模型太胖、GPU 跑得喘，它就是给网格做体检和减脂的。
- Evidence Notes: README 明确列出顶点/索引管线优化、简化、压缩与多语言接口；GitHub About 说明目标是减少 GPU 处理时间与存储成本；许可证 MIT。
- Honest Caveat: 优化参数会影响精度和外观，必须在目标设备和真实资产上做视觉回归与性能基准，不能只看示例数字。

### Rank 07 - openai/plugins
- Repo URL: https://github.com/openai/plugins
- Tagline: OpenAI 提供的 Codex 插件示例集合，展示 manifest、Skills、App、MCP、Agents、Commands 与 Hooks 的组织方式。
- Stars: 4,442
- Stars Today: 29
- Forks: 659
- Language: JavaScript
- License: 仓库概览未明确显示统一许可证
- Homepage: https://github.com/openai/plugins
- Topics: codex, plugins, skills, mcp, agents, developer-tools
- 技术栈: JavaScript, TypeScript, Codex plugins, MCP, Skills, Agents, Hooks
- Why It Matters Today: 插件示例把“如何扩展 Codex”从口头概念变成可照着拆解的目录结构，适合开发者理解插件能力边界和打包方式。
- 项目摘要: `openai/plugins` 是一组 Codex 插件范例。每个插件可以包含 manifest、Skills、应用代码、MCP 服务、Agents、Commands、Hooks 和资源文件，开发者可以从 Figma、Notion、iOS、Web、Expo、Remotion 等例子中理解如何把特定领域工作流接入 Codex。
- 核心特性:
  1. 用真实插件目录展示 manifest 与可选能力模块如何组合。
  2. 覆盖设计、文档、移动端、Web、视频和部署等多类开发场景。
  3. 适合作为插件工程结构、命名和集成方式的参考样板。
- 适用场景: 正在开发 Codex 插件的工程师；需要把内部工具或专业流程接入 Agent 的平台团队；想了解 Skills、MCP 与 Agent 配置关系的开发者。
- 一句话推荐: 想做 Codex 插件，先看官方例子怎么搭骨架，比对着空气拧螺丝靠谱。
- Evidence Notes: 仓库 README 将其描述为 curated collection of Codex plugin examples，并说明每个插件可包含 manifest、skills、app、MCP、agents、commands、hooks、assets；列出 Figma、Notion、iOS、Web 等示例。
- Honest Caveat: 仓库概览没有显示统一 License；采用、复制或分发具体插件前，应逐个检查目录和依赖的许可与凭证要求。

### Rank 08 - wonderwhy-er/DesktopCommanderMCP
- Repo URL: https://github.com/wonderwhy-er/DesktopCommanderMCP
- Tagline: 让 Claude 等 MCP 客户端能够执行终端命令、搜索和编辑本地文件，并处理常见数据与文档。
- Stars: 7,803
- Stars Today: 909
- Forks: 972
- Language: TypeScript
- License: MIT
- Homepage: https://desktopcommander.app/
- Topics: agent, ai, mcp, code-analysis, code-generation, terminal-ai, terminal-automation, vibe-coding
- 技术栈: TypeScript, MCP, terminal process control, filesystem APIs, diff editing, document/data tooling
- Why It Matters Today: 它是 Top 12 中今日增星最快的项目，代表 Agent 正从“给建议”走向“直接操作本地终端与文件”的高权限阶段。
- 项目摘要: Desktop Commander 是一个 MCP 服务器，为兼容客户端提供终端进程控制、文件搜索、差异化编辑和数据/文档处理能力。它可以让 Agent 在本地项目中执行命令、读写文件、分析 CSV/JSON/Excel，并处理 PDF、DOCX 等内容。
- 核心特性:
  1. 管理终端进程和命令执行，支持持续运行任务与输出交互。
  2. 提供文件搜索、读取和 diff 编辑，适合在真实代码库中完成多步修改。
  3. 集成表格、文档与常见数据格式处理，减少在多个工具之间搬运内容。
- 适用场景: 本地 AI 编程、批量文件处理、数据分析辅助、需要 Agent 直接操作项目环境的个人开发者和小团队。
- 一句话推荐: 它把 Agent 的手伸进了终端和文件夹——效率很高，门锁也得跟着升级。
- Evidence Notes: GitHub About 与 README 明确列出 terminal control、filesystem search、diff editing、process control、CSV/JSON/Excel、PDF/DOCX 等能力；MIT；主页 desktopcommander.app。
- Honest Caveat: 这是高权限本地工具。启用前应限制可访问目录、审查命令确认机制、避免暴露密钥，并在可回滚环境中运行。

### Rank 09 - chriskohlhoff/asio
- Repo URL: https://github.com/chriskohlhoff/asio
- Tagline: 跨平台 C++ 网络与低层 I/O 库，提供同步、异步套接字、定时器和执行模型。
- Stars: 6,144
- Stars Today: 76
- Forks: 1,507
- Language: C++
- License: BSL-1.0（仓库页面同时显示混合/未知提示，采用前请核对 COPYING）
- Homepage: https://think-async.com/Asio/
- Topics: c-plus-plus, networking, asynchronous-io, sockets, timers, cross-platform
- 技术栈: C++, asynchronous I/O, networking, executors, sockets, timers
- Why It Matters Today: 高并发网络服务仍需要稳定的异步 I/O 抽象；Asio 回榜说明 C++ 网络底座在现代服务、设备和客户端中仍有长期需求。
- 项目摘要: Asio 是跨平台 C++ 网络与低层 I/O 库。它用统一的同步和异步接口封装套接字、定时器及执行上下文，帮助开发者构建网络服务器、客户端和事件驱动程序，而不必为每个平台分别维护一套 I/O 代码。
- 核心特性:
  1. 支持 TCP、UDP、定时器等常见 I/O 对象的同步与异步操作。
  2. 通过事件循环和执行器组织回调、协程及并发任务。
  3. 可作为独立 Asio 使用，也与 Boost.Asio 生态长期保持紧密关系。
- 适用场景: 高并发网络服务、游戏网络层、IoT 网关、跨平台客户端、需要精细控制 I/O 生命周期的 C++ 系统。
- 一句话推荐: 要写 C++ 网络程序又不想和各平台 API 轮流吵架，Asio 是成熟的和事佬。
- Evidence Notes: 官方仓库和项目站将其定义为 C++ Library；页面显示 2026-05-14 发布 Asio 1.38.1；许可证区域包含 BSL-1.0 信息。
- Honest Caveat: 独立 Asio 与 Boost.Asio 的版本、命名空间和集成方式不同；团队应先统一依赖路线，并确认编译器与协程支持。

### Rank 10 - oven-sh/bun
- Repo URL: https://github.com/oven-sh/bun
- Tagline: 把 JavaScript/TypeScript Runtime、包管理器、测试、脚本运行与构建工具放进一个高性能可执行文件。
- Stars: 94,581
- Stars Today: 658
- Forks: 4,955
- Language: Rust
- License: 复合许可（详见仓库 License 页面及所含第三方组件）
- Homepage: https://bun.com/
- Topics: react, nodejs, javascript, rust, npm, bundler, typescript, jsx, transpiler, javascriptcore
- 技术栈: Rust, Zig/C++, JavaScriptCore, JavaScript, TypeScript, package manager, test runner
- Why It Matters Today: Bun 已是高星成熟项目，今天仍新增 658 Stars，显示开发者对更快、更统一的 JavaScript 工具链兴趣仍在上升。
- 项目摘要: Bun 是一套一体化 JavaScript/TypeScript 工具链。它试图用一个可执行文件覆盖 Node.js 兼容运行时、依赖安装、脚本运行、测试和打包等常见任务，减少工具拼装和启动等待。
- 核心特性:
  1. 以 Node.js 兼容为目标的 JavaScript Runtime，并使用 JavaScriptCore 引擎。
  2. 内置高性能包管理器、测试运行器和脚本执行能力。
  3. 支持 Linux、macOS 与 Windows，方便在团队和 CI 中统一工具入口。
- 适用场景: JavaScript/TypeScript 全栈项目、希望缩短安装与测试时间的团队、愿意验证 Node 兼容性的工具链实验和新项目。
- 一句话推荐: 想把 npm、测试器、脚本工具和 Runtime 少开几桌，Bun 就是“一锅端”的那口锅。
- Evidence Notes: 官方 README 将 Bun 定义为 all-in-one toolkit，包含 Node.js drop-in runtime、test runner、script runner、package manager；主页 bun.com；Topics 覆盖 Node.js、Rust、npm、bundler、TypeScript。
- Honest Caveat: 与 Node.js 的兼容性仍应按项目依赖逐项验证；许可证涉及 Bun 本体与所含引擎/第三方组件，商用分发前应查看完整 License 说明。

### Rank 11 - actions/checkout
- Repo URL: https://github.com/actions/checkout
- Tagline: GitHub Actions 工作流中最常用的仓库检出 Action，支持浅克隆、稀疏检出、多仓库和认证配置。
- Stars: 8,473
- Stars Today: 8
- Forks: 2,713
- Language: TypeScript
- License: MIT
- Homepage: https://github.com/features/actions
- Topics: github-actions, checkout, git, ci-cd, automation
- 技术栈: TypeScript, Node.js, Git, GitHub Actions
- Why It Matters Today: 它不是热闹型项目，却是大量 CI 工作流的入口。v7 对 `pull_request_target` 和 `workflow_run` 等高风险场景加强默认保护，体现供应链安全正在进入基础 Action 的默认行为。
- 项目摘要: `actions/checkout` 在 GitHub Actions Runner 上把仓库代码检出到工作区，是绝大多数构建、测试和发布流水线的第一步。它支持控制历史深度、分支、子模块、稀疏检出和多仓库认证。
- 核心特性:
  1. 默认浅克隆并允许通过 `fetch-depth` 控制完整历史或特定提交。
  2. 支持 sparse checkout、多仓库检出、子模块与私有仓库 PAT。
  3. v7 对高风险触发上下文采用更安全的默认拒绝策略，并要求显式选择。
- 适用场景: 几乎所有基于 GitHub Actions 的构建、测试、发布和代码分析流水线；尤其适合需要最小权限与受控检出范围的安全敏感仓库。
- 一句话推荐: CI 里最不起眼的一步，往往也是供应链大门；这把门锁值得跟着升级。
- Evidence Notes: README 标题为 Checkout v7，列出 sparse checkout、fetch depth、多仓库和 PAT 示例，并建议 `contents: read` 最小权限；仓库 MIT。
- Honest Caveat: 大版本升级可能涉及 Runner 与 Node 运行时要求；升级前应在分支流水线验证第三方 Action、子模块和私有仓库认证。

### Rank 12 - home-assistant/core
- Repo URL: https://github.com/home-assistant/core
- Tagline: Home Assistant 的 Python 核心后端，以本地控制和隐私优先连接家庭设备、自动化与集成。
- Stars: 88,736
- Stars Today: 80
- Forks: 38,051
- Language: Python
- License: Apache-2.0
- Homepage: https://www.home-assistant.io/
- Topics: python, home-automation, mqtt, raspberry-pi, iot, internet-of-things, asyncio, hacktoberfest
- 技术栈: Python, asyncio, MQTT, IoT integrations, local automation
- Why It Matters Today: 本地优先、隐私优先的智能家居路线继续受到关注；Core 回榜也说明社区对可自行托管、跨品牌自动化平台的需求稳定。
- 项目摘要: `home-assistant/core` 是 Home Assistant 的核心后端，负责设备集成、状态管理、事件和自动化逻辑。它强调本地运行与隐私，让用户在 Raspberry Pi、家庭服务器或受支持的系统上统一控制不同品牌设备。
- 核心特性:
  1. 大量设备和服务集成，将不同品牌的状态与控制统一到一个事件模型。
  2. 以本地控制为优先，减少对厂商云的依赖并提升隐私和响应速度。
  3. 基于 Python/asyncio 的模块化架构，社区可以持续扩展集成和自动化能力。
- 适用场景: 希望统一智能家居设备、重视本地控制和隐私的家庭用户；开发设备集成或复杂自动化的工程爱好者。
- 一句话推荐: 不想让每个灯泡都单独开一场发布会，Home Assistant 负责把它们请到同一个群里。
- Evidence Notes: GitHub About 明确写明“Open source home automation that puts local control and privacy first”；主页 home-assistant.io；Apache-2.0；页面显示 2026.7.2 于 2026-07-10 发布。
- Honest Caveat: `core` 是后端源码仓库，不是普通用户最省事的安装入口；家庭使用通常应优先选择官方支持的 Home Assistant OS/Container 等部署方式。

## Language Distribution

- C++:
  - Count: 4
  - Percent: 33.3%
  - Color Hint: #F34B7D
- TypeScript:
  - Count: 3
  - Percent: 25.0%
  - Color Hint: #3178C6
- Python:
  - Count: 2
  - Percent: 16.7%
  - Color Hint: #3572A5
- Go:
  - Count: 1
  - Percent: 8.3%
  - Color Hint: #00ADD8
- JavaScript:
  - Count: 1
  - Percent: 8.3%
  - Color Hint: #F1E05A
- Rust:
  - Count: 1
  - Percent: 8.3%
  - Color Hint: #DEA584

## Explore Highlights

### Explore 1
- Title: catchorg/Catch2
- URL: https://github.com/catchorg/Catch2
- Kind: Trending repository
- Meta: C++ 测试框架 · 今日 +113
- Short Reason: 成熟测试工具登顶，适合关注 C++ 工程质量与测试体验。

### Explore 2
- Title: wonderwhy-er/DesktopCommanderMCP
- URL: https://github.com/wonderwhy-er/DesktopCommanderMCP
- Kind: Trending repository
- Meta: MCP 本地执行工具 · 今日 +909
- Short Reason: 今日增星速度最高，代表 Agent 本地操作能力升温。

### Explore 3
- Title: oven-sh/bun
- URL: https://github.com/oven-sh/bun
- Kind: Trending repository
- Meta: JavaScript 一体化工具链 · 今日 +658
- Short Reason: 高星成熟项目仍快速增长，工具链整合趋势明显。

### Explore 4
- Title: malisper/pgrust
- URL: https://github.com/malisper/pgrust
- Kind: Trending repository
- Meta: Rust 重写 PostgreSQL 的实验项目 · 今日 +774
- Short Reason: 增速突出，但性能数据主要来自维护者自述，适合持续观察而非立刻选型。

### Explore 5
- Title: obra/superpowers
- URL: https://github.com/obra/superpowers
- Kind: Trending repository
- Meta: Agent Skills 与开发方法论 · 今日 +740
- Short Reason: 把 TDD、调试、评审和并行 Agent 组织成可复用技能。

### Explore 6
- Title: anthropics/claude-cookbooks
- URL: https://github.com/anthropics/claude-cookbooks
- Kind: Trending repository
- Meta: Claude 应用示例与实践
- Short Reason: 适合从可运行案例理解 Claude API、工具调用和应用模式。

### Explore 7
- Title: prisma/prisma
- URL: https://github.com/prisma/prisma
- Kind: Trending repository
- Meta: TypeScript ORM 与数据库工具链
- Short Reason: 成熟数据访问工具回榜，可观察 TypeScript 后端工程需求。

### Explore 8
- Title: dotnet/aspnetcore
- URL: https://github.com/dotnet/aspnetcore
- Kind: Trending repository
- Meta: .NET Web 框架与运行时组件
- Short Reason: 大型成熟框架进入 Explore，说明今日并非只有 AI 项目唱独角戏。

## Rendering Notes

- Hero 主标题建议：🐙 GitHub Trending 日报
- Hero 副标题建议：今天值得点开的 12 个开源项目：AI 插件化升温，工程底座集体回榜
- Top 3 高亮原因：严格沿用 GitHub Trending 原始页面前 3 名，不按总 Stars 或今日新增重新排序。
- 需要在 HTML 中诚实提示的降级点：
  - Trending 为动态榜单，数字在报告生成后仍可能变化。
  - Trending 排名算法未公开，不能理解为简单的今日 Stars 排序。
  - Explore 当前与 Trending 高度重合，精选区用于补充观察而非独立榜单。
  - Terraform、openai/plugins、DesktopCommanderMCP、Bun、Asio 等项目需保留许可、权限或兼容性边界。
- 不允许省略的区块：
  - Header / Hero
  - 4 张 Stats Cards
  - 今日洞察
  - 今日热门 Top 12
  - 编程语言分布
  - GitHub Explore 精选
  - Footer
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
