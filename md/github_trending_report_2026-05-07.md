# GitHub Trending 日报 · 2026-05-07

## Meta
- **日期**：2026-05-07
- **数据来源**：GitHub Trending（全语言） + Python Trending
- **今日 Top 12**：12 个项目 | 累计 Stars：~1.0M | 编程语言：4 | 今日新上榜：8 | 持续上榜：4

---

## 今日洞察

### 🔁 addyosmani/agent-skills（31k）——昨日"4 条原则"，今日"20 个 Skill"：Karpathy 接力赛

昨日 forrestchang/andrej-karpathy-skills（115k）用"4 条哲学原则"引发 Claude Code 用户病毒传播，今日 addyosmani/agent-skills（31k）用"20 个工程生命周期 Skill"接棒——同是 AI 编程行为约束工具，层次截然不同。前者是哲学层面的"怎么想"，后者是工程流程层面的"怎么做"。作者 Addy Osmani 是 Google Chrome 团队 Engineering Manager，20 个 Skill 完整覆盖 Define→Plan→Build→Verify→Review→Ship 六阶段，7 个 slash command 自动激活对应 Skill，兼容 Claude Code / Cursor / Windsurf / Gemini CLI / Copilot / OpenCode / Kiro 全主流 AI IDE。两天内同一赛道从原则到工程的两次爆发，AI coding Skill 生态的系统化演进正在加速。

### 💹 金融 AI 三连今日同框：TradingAgents-CN（25.8k）+ dexter（24.5k）+ Kronos（23.3k）

昨日 TradingAgents（69.8k，多 Agent 决策层）刚从 Top 12 退出，今日金融 AI 以更大规模回归：TradingAgents-CN（中文 A 股增强版）+ virattt/dexter（自主深度金融研究 Agent）+ shiyu-coder/Kronos（AAAI 2026 录用，K 线基础模型）三项同时上榜。这是从昨日的"决策层 Agent"到今日"数据层 + 研究层 + 本地化适配"的演进——金融 AI 的 Trending 叙事正在从"用 LLM 做交易决策"转向"为金融数据建立专属基础模型"。Kronos 是第一个在 45 个全球交易所数据上预训练的开源金融 K 线基础模型，OHLCV 专属 tokenizer + 自回归 Transformer，AAAI 2026 学术背书。

### 📦 Shubhamsaboo/awesome-llm-apps（109k）——"可运行 cookbook" 击败"资源收藏列表"

109,087 ⭐，16,139 forks，Apache-2.0，是今日新上榜中 Stars 最高的项目。与昨日 coding-interview-university 类型（"收藏清单"）不同，awesome-llm-apps 的每个模板都是原创手写 + 端到端测试 + 3 条命令运行，覆盖 Starter AI Agents / Advanced Agents / Multi-agent Teams / Voice AI / MCP Agents / RAG / Agent Skills / Memory / Fine-tuning，Claude / Gemini / GPT / Llama / Qwen / xAI 全 Provider 支持。"可运行 cookbook > 资源收藏列表"是今日社区用 Star 投票的核心判断：开发者要的不是指路牌，是能跑的代码。

### 🌐 LadybirdBrowser/ladybird（63k）——独立浏览器重新登场，"基础设施日"信号

今日 Trending 的一个独特特征是"基础设施类项目集中"：pytorch（99.7k，ML 基础框架）+ LadybirdBrowser（63k，独立浏览器）+ Kronos（金融基础模型）+ onyx（开源 AI 平台）同日出现。ladybird 是唯一不依赖 Chromium / WebKit 的真正独立浏览器，C++ 实现，SerenityOS 作者 Andreas Kling 创立，每次 Trending 登榜通常对应一个重大里程碑（milestone 发布或重大架构进展）。63k Stars + 3k forks，是今日 Trending 中唯一的"基础设施而非 AI 工具"代表，提醒我们：即使在 AI 工具爆发的时代，浏览器引擎这类基础软件依然有强劲社区关注度。

---

## 今日热门 Top 12（按总 Stars 排序）

### #01 public-apis/public-apis ⭐ 432,826 [持续 Day 2]
- **仓库**：https://github.com/public-apis/public-apis
- **语言**：Python | **License**：MIT | **Forks**：47,330
- **描述**：A collective list of free APIs. 连续第 2 日上榜，Stars 从 432,503 增至 432,826，日增 323。
- **推荐语**："连续第 2 日榜首——public-apis 昨日带动的社区分享潮尚未结束，今日 Stars 再增 323，依然是 GitHub 全站前 5。"

---

### #02 Shubhamsaboo/awesome-llm-apps ⭐ 109,087 [新上榜]
- **仓库**：https://github.com/Shubhamsaboo/awesome-llm-apps
- **语言**：Python | **License**：Apache-2.0 | **Forks**：16,139
- **描述**：100+ AI Agent & RAG apps you can actually run — clone, customize, ship. 每个模板原创手写 + 端到端测试 + 3 条命令即可运行，16k forks 是今日新上榜项目最高。
- **核心特性**：
  - 100+ 可运行模板：Starter AI Agents / Advanced Agents / Multi-agent Teams / Voice AI / MCP AI Agents / RAG / Agent Skills / Memory / Fine-tuning
  - 每个模板：原创手写 + 端到端测试前验证 + 3 条命令启动
  - Provider 无关：Claude / Gemini / GPT / Llama / Qwen / xAI 一键切换
  - Featured This Month：Insurance Claim Live Agent Team / Home Renovation Agent / Self-Improving Agent Skills
  - Apache-2.0：fork it, ship it, sell it，无 paywall
- **技术栈**：Python / Streamlit / Claude / OpenAI / LangChain / Phidata / CrewAI
- **适用场景**：AI 项目快速启动参考；LLM App 模板选型；Agent / RAG / Voice 场景学习。
- **推荐语**："109k Stars + 16k forks——'可运行 cookbook' 的王者。与昨日 coding-interview-university（346k，学习路线图）形成鲜明对比：今日社区证明，能直接跑的代码比指路牌更值钱。"

---

### #03 pytorch/pytorch ⭐ 99,711 [新上榜]
- **仓库**：https://github.com/pytorch/pytorch
- **语言**：Python | **License**：BSD-3-Clause | **Forks**：27,695
- **描述**：Tensors and Dynamic neural networks in Python with strong GPU acceleration. ML 领域最重要的基础框架，99.7k Stars + 27.7k forks，今日上 Trending 通常对应重大版本发布或大型 ML 事件。
- **核心特性**：
  - 动态计算图（define-by-run），Python 优先
  - 强大 GPU 加速：CUDA 原生支持 + Apple Silicon MPS
  - torch.compile：基于 TorchInductor 的图编译加速
  - 分布式训练：torch.distributed / FSDP / DDP
  - TorchScript + ONNX：生产部署
  - 活跃生态：transformers / diffusers / torchvision / torchaudio
- **技术栈**：Python / C++ / CUDA / Triton / TorchInductor
- **适用场景**：深度学习模型研究与训练；生产部署 ML pipeline；GPU 加速计算。
- **推荐语**："99.7k Stars 的 ML 基础框架今日登 Trending——pytorch 出现在 Trending 通常是重大发布或技术社区事件的信号，配合今日 Kronos（金融基础模型）同框，ML 基础设施今日存在感极强。"

---

### #04 bytedance/deer-flow ⭐ 65,667 [持续 Day 2]
- **仓库**：https://github.com/bytedance/deer-flow
- **语言**：Python | **License**：MIT | **Forks**：8,681
- **描述**：DeerFlow 2.0 - An open-source long-horizon SuperAgent harness. 连续第 2 日上榜，Stars 从 65,293 增至 65,667，日增 374，8.7k forks。
- **推荐语**："连续第 2 日上榜，日增 374——DeerFlow 2.0 今日与 addyosmani/agent-skills 共同出现，字节跳动 SuperAgent 运行时 + Google Chrome DevRel 工程 Skill 体系，SuperAgent 生态上下游今日同框。"

---

### #05 LadybirdBrowser/ladybird ⭐ 63,044 [新上榜]
- **仓库**：https://github.com/LadybirdBrowser/ladybird
- **语言**：C++ | **License**：BSD-2-Clause | **Forks**：2,999
- **描述**：Truly independent web browser. 唯一不基于 Chromium / WebKit 的真正独立浏览器引擎，C++ 实现，SerenityOS 作者 Andreas Kling 创立，63k Stars + 3k forks，今日登 Trending 通常对应重大里程碑。
- **核心特性**：
  - 完全独立实现：不 fork Chromium / Firefox / WebKit，从零构建
  - 完整 Web 标准支持目标：HTML / CSS / JavaScript / WebAssembly
  - LibWeb：核心布局/渲染引擎；LibJS：JavaScript 引擎
  - 跨平台：macOS / Linux / Windows（实验性）
  - 开发透明：Kling 的 YouTube 系列 "Browser from Scratch" 直播开发过程
- **技术栈**：C++ / Swift（macOS）/ LibWeb / LibJS
- **适用场景**：关注浏览器引擎开发的工程师；Web 标准实现研究；独立浏览器生态支持。
- **推荐语**："今日 Trending 中最独特的项目——在 AI 工具爆发的时代，一个用 C++ 从零构建的独立浏览器登上热榜，说明基础软件基础设施依然有最强劲的社区情感支持。"

---

### #06 D4Vinci/Scrapling ⭐ 46,566 [持续 Day 2]
- **仓库**：https://github.com/D4Vinci/Scrapling
- **语言**：Python | **License**：MIT | **Forks**：4,308
- **描述**：🕷️ 自适应爬虫全栈框架，连续第 2 日上榜，Stars 从 45,604 增至 46,566，日增 962，是今日持续项目中日增最高。
- **推荐语**："连续第 2 日上榜，日增 962——Scrapling 是今日 4 个持续项目中日增 Stars 最高的，MCP Server + 反 bot 全功能爬虫框架的吸引力持续。"

---

### #07 ruvnet/ruflo ⭐ 45,500 [持续 Day 5]
- **仓库**：https://github.com/ruvnet/ruflo
- **语言**：TypeScript | **License**：MIT | **Forks**：5,031
- **描述**：🌊 The leading agent orchestration platform for Claude. 连续第 5 日上榜，Stars 从 44,548 增至 45,500，日增 952，5 日累计增长约 8,210（05-03：37,290）。
- **推荐语**："连续第 5 日上榜，5 日累计增 8.2k——Ruflo 是今日 Trending 中持续天数最长的项目，单日增量始终维持在 900+ 级别，Claude Code 生态 Agent 编排热度不退。"

---

### #08 addyosmani/agent-skills ⭐ 31,246 [新上榜]
- **仓库**：https://github.com/addyosmani/agent-skills
- **语言**：Markdown | **License**：MIT | **Forks**：3,678
- **描述**：Production-grade engineering skills for AI coding agents. Google Chrome 团队 Engineering Manager Addy Osmani 出品，20 个 Skill + 7 个 slash command，完整覆盖工程生命周期。
- **核心特性**：
  - **7 个 slash command**：/spec / /plan / /build / /test / /review / /code-simplify / /ship
  - **20 个 Skill，6 大阶段**：
    - Define：idea-refine / spec-driven-development
    - Plan：planning-and-task-breakdown
    - Build：incremental-implementation / TDD / context-engineering / source-driven-development / frontend-ui-engineering / api-and-interface-design
    - Verify：browser-testing-with-devtools / debugging-and-error-recovery
    - Review：code-review-and-quality / code-simplification / security-and-hardening / performance-optimization
    - Ship：git-workflow-and-versioning / ci-cd-and-automation / deprecation-and-migration / documentation-and-adrs / shipping-and-launch
  - **上下文自动激活**：设计 API 时触发 api-and-interface-design，构建 UI 时触发 frontend-ui-engineering
  - **全 IDE 支持**：Claude Code / Cursor / Windsurf / Gemini CLI / Copilot / OpenCode / Kiro
- **技术栈**：Markdown（SKILL.md）/ 支持 AGENTS.md / .cursor/rules / .github/copilot-instructions.md
- **适用场景**：Claude Code 用户系统性提升工程质量；AI coding agent 全生命周期约束；前端工程师 AI 辅助开发工作流。
- **推荐语**："昨日 karpathy-skills（115k，4 条原则）→ 今日 agent-skills（31k，20 个 Skill）——AI coding Skill 生态从哲学层走向工程流程层，Addy Osmani 的 Google 工程背景为这套体系带来了真实生产级的可信度。"

---

### #09 onyx-dot-app/onyx ⭐ 29,101 [新上榜]
- **仓库**：https://github.com/onyx-dot-app/onyx
- **语言**：Python | **License**：MIT | **Forks**：3,915
- **描述**：Open Source AI Platform - AI Chat with advanced features that works with every LLM. 开源 AI 平台，支持所有主流 LLM，企业级功能（权限管理/连接器/RAG），29k Stars + 3.9k forks。
- **核心特性**：
  - 支持所有主流 LLM：Claude / GPT / Llama / Gemini / 本地模型
  - 企业知识连接器：Slack / GitHub / Confluence / Jira / Google Drive / Salesforce 等 40+ 数据源
  - 权限感知 RAG：按用户权限过滤检索结果
  - 企业级安全：SSO / SAML / 本地部署选项
  - Chat + Search + Agent 三种使用模式
- **技术栈**：Python / FastAPI / PostgreSQL / Redis / Vespa
- **适用场景**：企业内部 AI 知识库搭建；开源版 Notion AI / Glean 替代；多数据源统一 RAG 平台。
- **推荐语**："29k Stars 的企业级开源 AI 平台——onyx 今日与 InsForge（Explore）共同出现，今日 Trending 对'企业 AI 基础设施'（AI 平台 + AI 网关 + AI backend）的关注度显著上升。"

---

### #10 hsliuping/TradingAgents-CN ⭐ 25,810 [新上榜]
- **仓库**：https://github.com/hsliuping/TradingAgents-CN
- **语言**：Python | **License**：MIT | **Forks**：5,442
- **描述**：基于多智能体 LLM 的中文金融交易框架——TradingAgents 中文增强版。针对中国 A 股市场数据和工具进行深度适配，5,442 forks 是今日所有新上榜项目中最高。
- **核心特性**：
  - 基于 TauricResearch/TradingAgents 深度 fork，专为中国 A 股市场适配
  - 中文数据源：东方财富 / 同花顺 / AKShare / Tushare 等 A 股数据接口
  - 中文 LLM 支持：DeepSeek / Qwen / ChatGLM 优先优化
  - 中文分析报告生成：基于 A 股规则的多 Agent 分析辩论
  - Docker 一键部署，中文文档完整
- **技术栈**：Python / LangGraph / LangChain / AKShare / DeepSeek
- **适用场景**：中国 A 股量化研究；中文金融 AI 策略研究；本地化 LLM 金融应用。
- **推荐语**："5,442 forks 今日新上榜项目最高——TradingAgents-CN 是 TauricResearch/TradingAgents（昨日 Day 6）的中文本地化版本，昨日国际版退出 Top 12，今日中文版接棒，中国量化 AI 社区的用脚投票。"

---

### #11 virattt/dexter ⭐ 24,469 [新上榜]
- **仓库**：https://github.com/virattt/dexter
- **语言**：Python | **License**：MIT | **Forks**：2,977
- **描述**：An autonomous agent for deep financial research. 自主深度金融研究 Agent，2,977 forks，今日与 TradingAgents-CN 和 Kronos 形成金融 AI 三连组合。
- **核心特性**：
  - 全自动深度金融研究：从问题到完整研究报告
  - 多数据源：SEC 文件 / 财务报表 / 新闻 / 分析师报告
  - 结构化研究流程：数据收集 → 分析 → 报告生成
  - 支持 Claude 和 GPT 系列模型
- **技术栈**：Python / Claude / LangGraph / SEC API / 财务数据 API
- **适用场景**：自动化股权研究报告生成；投资决策辅助信息收集；SEC 文件分析自动化。
- **推荐语**："dexter 是今日金融 AI 三连中的'研究中间层'——Kronos 负责市场预测（数据层），dexter 负责深度研究（信息层），TradingAgents-CN 负责多 Agent 决策（决策层），今日金融 AI 全栈在 Trending 同时出现。"

---

### #12 shiyu-coder/Kronos ⭐ 23,262 [新上榜]
- **仓库**：https://github.com/shiyu-coder/Kronos
- **语言**：Python | **License**：MIT | **Forks**：4,070
- **描述**：Kronos: A Foundation Model for the Language of Financial Markets. AAAI 2026 录用，第一个在 45 个全球交易所 K 线数据上预训练的开源金融基础模型，4,070 forks。
- **核心特性**：
  - **两阶段框架**：① 专属 Tokenizer：将 OHLCV 连续数据量化为层次化离散 token；② 大型自回归 Transformer：在金融 K 线语言上预训练
  - **训练数据**：45+ 全球交易所，覆盖股票/加密货币/期货
  - **模型家族**：Kronos-mini / Kronos-small / Kronos-base（Hugging Face 开放）
  - **支持任务**：多空预测 / 价格预测 / 趋势识别 / 波动率预测
  - **A 股微调**：内置 A 股微调脚本（Configure → 准备数据集 → 运行微调 → 回测评估）
  - **Live Demo**：BTC/USDT 未来 24 小时预测可视化页面
- **技术栈**：Python / PyTorch / Transformers / HuggingFace Hub / Gradio
- **适用场景**：金融时序预测研究；量化策略基础模型微调；K 线模式识别。
- **推荐语**："AAAI 2026 录用 + 45 个全球交易所数据预训练——Kronos 是今日最具学术深度的项目，4,070 forks 对一个学术 ML 项目而言极为罕见，说明量化社区已大量fork用于实验。"

---

## 语言分布

| 语言 | 项目数 | 占比 | 代表项目 |
|---|---|---|---|
| Python | 9 | 75% | public-apis / awesome-llm-apps / pytorch / deer-flow / Scrapling / onyx / TradingAgents-CN / dexter / Kronos |
| C++ | 1 | 8% | LadybirdBrowser/ladybird |
| TypeScript | 1 | 8% | ruvnet/ruflo |
| Markdown | 1 | 8% | addyosmani/agent-skills |

---

## GitHub Explore 精选

1. **cheahjs/free-llm-api-resources**（20,639 ⭐）— 今日同时出现在全语言 Trending 和 Python Trending 双榜。免费 LLM 推理 API 资源列表，2,098 forks，与 awesome-llm-apps 和 public-apis 同日出现，今日"可用 AI 资源"类项目是第二热门主题。

2. **anthropics/financial-services**（9,421 ⭐）— 今日同时出现在全语言 Trending 和 Python Trending 双榜。Anthropic 官方出品的金融服务示例库，1,274 forks，与今日金融 AI 三连（Kronos + dexter + TradingAgents-CN）共同出现，Anthropic 亲身入场金融 AI 生态。

3. **InsForge/InsForge**（8,566 ⭐）— 今日首次出现在全语言 Trending。"Postgres-based backend with auth, storage, compute, hosting, and AI gateway. Built for coding agents." 708 forks，类 Supabase 的 AI agent 原生后端，与 onyx（AI 平台）今日同框，企业 AI 基础设施赛道今日集中登场。

4. **Hmbown/DeepSeek-TUI**（15,564 ⭐）— 连续第 2 日出现在全语言 Trending（昨日 Explore），1,213 forks，终端 DeepSeek 编程 Agent，今日 Stars 从昨日 10,854 大幅跳升至 15,564，日增约 4,710，是今日所有项目中日增最快的。

5. **AIDC-AI/Pixelle-Video**（12,929 ⭐）— 连续多日出现在 Python Trending，AI 全自动短视频引擎，1,951 forks，持续热度稳定。
