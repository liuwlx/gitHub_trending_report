# GitHub Trending 日报 · 2026-05-10

## Meta
- **日期**：2026-05-10
- **数据来源**：GitHub Trending（全语言）+ Python Trending
- **今日 Top 12**：12 个项目 | 累计 Stars：~516k | 编程语言：3 | 今日新上榜：9 | 持续上榜：3

---

## 今日洞察

### 🔧 ChromeDevTools/chrome-devtools-mcp（38.97k）——Chrome 官方 DevTools MCP，AI coding agent 首次获得浏览器原生调试权限

Chrome DevTools 官方团队出品（Google 背书），38,971 ⭐ + 2,465 forks + 47 releases。让 coding agents（Claude Code / Cursor / Copilot / Gemini）通过 MCP 协议直接控制和检查 Chrome 浏览器：获取性能 insights（Puppeteer 驱动 + Chrome DevTools traces 可操作分析）、高级调试（网络请求 / 截图 / 控制台消息 + source-mapped stack traces）、可靠自动化。这是今日技术价值最高的项目：浏览器调试从"人工操作 DevTools"向"AI agent 原生接入"迈出第一步。与 spec-kit（规格驱动）+ agent-skills（行为约束）+ chrome-devtools-mcp（浏览器调试），AI coding 工作流的完整闭环首次成型：AI agent 不仅能写代码，还能直接调试运行中的浏览器。

### 💎 hesreallyhim/awesome-claude-code（43.2k）——Claude Code 生态精华资源库，43k Stars 证明 Claude Code 已自成体系

43,201 ⭐ + 3,671 forks，精选 Claude Code 的 skills / hooks / slash-commands / agent orchestrators / applications / plugins，强调代码质量、安全性、原创性。今日与 agent-skills（Day 4，37,757）同框，两者是 Claude Code 重度用户的必备双组合：agent-skills 是工程 Skill 约束层，awesome-claude-code 是生态资源导航层。本周 Claude Code 生态四大维度完整成型：karpathy-skills（05-06，原则）→ agent-skills（05-07，工程 Skill）→ spec-kit（05-08，规格驱动）→ awesome-claude-code（05-10，生态资源），这是今日在 Trending 日报跨日叙事中最值得记录的里程碑。

### 📚 中文 LLM 学习三部曲：minimind（49.4k）+ hello-agents（45.97k）+ dive-into-llms（36.66k）——教育大周

今日三个大型中文 LLM 学习资源同时上榜：minimind（"2小时从零训练 64M LLM"，做 LLM）+ datawhalechina/hello-agents（《从零开始构建智能体》，用 LLM 做 Agent）+ Lordog/dive-into-llms（《动手学大模型》系列，学 LLM 原理），构成 LLM 学习完整三部曲。三个项目合计超 131k Stars，在 AI 工具爆发的时代，中文社区"动手学"内容的热情不减反增——这说明即使工具越来越易用，开发者对"真正理解底层"的需求依然强劲。

### 🏛️ 今日大换血背后：从"小团队爆款"到"大平台工具"——Trending 信号质量升级

05-08 Top 12 主要是 goose（Block/AAIF）、PageIndex（VectifyAI）等新兴团队项目，今日则是 Chrome DevTools 官方（Google）、PaddleOCR（百度飞桨）、Datawhale（中文 AI 教育最大社区）、ByteDance（UI-TARS）、Anthropic（claude-agent-sdk）、HKUDS（港大）的集中亮相。这种从"创业者/个人"主导到"机构/大厂"主导的 Trending 轮换模式在近 5 日出现了 2 次（05-08、05-10），说明 AI coding 生态的工具层正在进入快速机构化阶段。

---

## 今日热门 Top 12（按总 Stars 排序）

### #01 github/spec-kit ⭐ 94,739 [持续 Day 3]
- **仓库**：https://github.com/github/spec-kit
- **语言**：Python | **License**：MIT | **Forks**：8,236
- **描述**：💫 Toolkit to help you get started with Spec-Driven Development. GitHub 官方出品，Day 3 持续上榜，Stars 从 05-08 的 93,239 增至今日 94,739，日均增 +750，8,236 forks。
- **今日亮点**：今日与 awesome-claude-code（#5）和 chrome-devtools-mcp（#6）同框，spec-kit（规格驱动）+ agent-skills（行为约束）+ chrome-devtools-mcp（浏览器调试）= AI coding 工作流完整闭环，首次在同一天 Trending 出现。
- **推荐语**："持续 Day 3 的 spec-kit 今日意义不同于前两天——今日它不再是独立热点，而是 AI coding 工作流三件套（规格→约束→调试）的'锚点'。这是方法论工具链逐步完善的标志。"

---

### #02 PaddlePaddle/PaddleOCR ⭐ 77,521 [新上榜]
- **仓库**：https://github.com/PaddlePaddle/PaddleOCR
- **语言**：Python | **License**：Apache-2.0 | **Forks**：10,400
- **描述**：Turn any PDF or image document into structured data for your AI. A powerful, lightweight OCR toolkit that bridges the gap between images/PDFs and LLMs. Supports 100+ languages. 百度飞桨官方出品，77,521 ⭐ + 10,400 forks，今日重新焦点化——以"桥接图像/PDF 与 LLM"的 AI 原生新定位重新上 Trending。
- **核心特性**：
  - 100+ 语言 OCR 识别，准确率行业领先
  - PDF 转结构化数据，直接喂给 LLM（新定位：LLM 前置数据处理层）
  - 轻量级，支持 CPU 部署，端到端部署无需专用 GPU
  - 支持 PP-OCR / PP-Structure / PP-ChatOCRv3 三大系列
  - 覆盖：表格 / 公式 / 图表 / 印章 / 手写体
- **技术栈**：Python / PaddlePaddle / ONNX
- **适用场景**：文档理解 RAG 前处理；PDF / 扫描件转结构化数据；多语言文档批量提取。
- **推荐语**："77.5k Stars + 10.4k forks 的 PaddleOCR 今日以'LLM 前置数据处理层'的新定位重上 Trending——结合今日 PageIndex（Explore 候选，vectorless RAG）的逻辑，今日的信号是：文档 → 结构化 → LLM 推理这个管道的每个环节都在工具化。"

---

### #03 jingyaogong/minimind ⭐ 49,407 [新上榜]
- **仓库**：https://github.com/jingyaogong/minimind
- **语言**：Python | **License**：Apache-2.0 | **Forks**：6,276
- **描述**：🧠「大模型」2小时完全从0训练64M的小参数LLM！Train a 64M-parameter LLM from scratch in just 2h! 49,407 ⭐ + 6,276 forks，中文 LLM 教育项目中 Stars 最高，今日"LLM 学习三部曲"第一部。
- **核心特性**：
  - 2 小时从零训练 64M 参数 LLM，极低门槛
  - 完整训练流程：预训练 / SFT / RLHF / LoRA 微调 / DPO 全覆盖
  - 支持 MOE（Mixture of Experts）架构实现
  - 支持 MiniMind-V（多模态视觉语言模型）
  - 中文优先，支持 BPE tokenizer 自定义
  - 完整模型架构注释，极适合学习
- **技术栈**：Python / PyTorch / CUDA
- **适用场景**：LLM 原理学习（从代码层面理解 Transformer）；快速验证训练配方；AI 课程实验用例。
- **推荐语**："49k Stars 的 minimind 今日与 hello-agents（45.9k）和 dive-into-llms（36.7k）同框，三者各有侧重：minimind 是'做 LLM'，hello-agents 是'用 LLM 构建 Agent'，dive-into-llms 是'学 LLM 原理'。今日是中文 AI 教育社区的集体爆发日。"

---

### #04 datawhalechina/hello-agents ⭐ 45,976 [新上榜]
- **仓库**：https://github.com/datawhalechina/hello-agents
- **语言**：Python | **License**：CC-BY-4.0 | **Forks**：5,548
- **描述**：📚《从零开始构建智能体》——从零开始的智能体原理与实践教程。Datawhale（国内最大 AI 教育社区）出品，45,976 ⭐ + 5,548 forks，今日同时出现在全语言和 Python 双榜。
- **核心特性**：
  - 《从零开始构建智能体》完整教程，中文原创
  - 覆盖：Agent 原理 / Function Calling / 工具使用 / 多 Agent 框架
  - Datawhale 社区维护，活跃贡献者众多
  - 配套代码可直接运行的 Jupyter Notebook
  - 支持 LangChain / LangGraph / AutoGen / CrewAI 等主流框架
- **技术栈**：Python / LangChain / LangGraph / Jupyter
- **适用场景**：智能体开发入门学习；从 API 使用到 Agent 架构系统学习；中文 AI 教育课程参考。
- **推荐语**："Datawhale 是国内最有影响力的 AI 教育社区，hello-agents 的 45.9k 说明'从零开始'类教程仍然是最有吸引力的学习范式——今日与 easy-vibe（Explore，8.7k）同框，Datawhale 今日在 Trending 上双项目亮相。"

---

### #05 hesreallyhim/awesome-claude-code ⭐ 43,201 [新上榜]
- **仓库**：https://github.com/hesreallyhim/awesome-claude-code
- **语言**：Markdown | **License**：MIT | **Forks**：3,671
- **描述**：A curated list of awesome skills, hooks, slash-commands, agent orchestrators, applications, and plugins for Claude Code by Anthropic. 43,201 ⭐ + 3,671 forks，Claude Code 生态精华资源库，今日新上榜 Top 12。
- **核心特性**：
  - 精选 Claude Code 的 skills / hooks / slash-commands 全品类
  - 覆盖 agent orchestrators / applications / plugins 完整生态
  - 强调代码质量、安全性、原创性三原则
  - 持续跟进 Claude Code 最新特性（hooks / projects / memory 等）
  - 社区贡献，人工精选，非自动收录
- **技术栈**：Markdown / Claude Code / AGENTS.md
- **适用场景**：Claude Code 用户资源导航；AI agent 工具链建设参考；SKILL.md / hooks 最佳实践学习。
- **推荐语**："本周 Claude Code 生态四大维度完整成型：原则（karpathy-skills，05-06）→ Skill（agent-skills，05-07）→ 规格（spec-kit，05-08）→ 资源（awesome-claude-code，05-10）。这四个项目合并起来是目前最系统的 Claude Code 使用指南。"

---

### #06 ChromeDevTools/chrome-devtools-mcp ⭐ 38,971 [新上榜]
- **仓库**：https://github.com/ChromeDevTools/chrome-devtools-mcp
- **语言**：TypeScript | **License**：Apache-2.0 | **Forks**：2,465
- **描述**：Chrome DevTools for coding agents. Chrome DevTools 官方团队出品（Google），38,971 ⭐ + 2,465 forks + 47 releases，让 AI coding agent 直接通过 MCP 协议接入 Chrome 原生调试能力。
- **核心特性**：
  - 官方 MCP server：Claude Code / Cursor / Copilot / Gemini 一行配置接入
  - 性能分析：记录 Chrome DevTools traces，提取可操作性能 insights，CrUX 真实用户数据
  - 高级调试：网络请求分析 / 截图 / 控制台消息 + source-mapped stack traces
  - 可靠自动化：Puppeteer 驱动 Chrome 操作，自动等待 action 完成
  - CLI 模式：不需要 MCP 也可命令行使用
  - 47 次发布，高迭代节奏
- **技术栈**：TypeScript / Chrome DevTools Protocol / Puppeteer / MCP
- **适用场景**：AI coding agent 调试前端应用；自动化 UI 测试生成；性能回归分析自动化。
- **推荐语**："今日技术价值最高的项目——Chrome 官方 DevTools 团队直接提供 MCP server，是'浏览器调试进入 AI agent 工作流'的里程碑。与 spec-kit + agent-skills 组合，AI coding 的写-规范-调试闭环首次在同一天 Trending 出现。"

---

### #07 addyosmani/agent-skills ⭐ 37,757 [持续 Day 4]
- **仓库**：https://github.com/addyosmani/agent-skills
- **语言**：Markdown | **License**：MIT | **Forks**：4,209
- **描述**：Production-grade engineering skills for AI coding agents. 连续第 4 日上榜，Stars 从 05-08 的 33,578 增至今日 37,757，2 日增 +4,179，4,209 forks（2 日增 +341）。
- **今日亮点**：与 awesome-claude-code（#5）形成今日 Claude Code 生态双雄组合——agent-skills 是行为约束层，awesome-claude-code 是生态资源层，两者完美互补。
- **推荐语**："连续 Day 4，2 日增 4,179——agent-skills 是今日 Top 12 中连续上榜天数最长的项目，说明其价值被持续验证而非一日昙花。今日与 awesome-claude-code 同框更是强化了 Claude Code 生态双轮驱动的信号。"

---

### #08 Lordog/dive-into-llms ⭐ 36,657 [新上榜]
- **仓库**：https://github.com/Lordog/dive-into-llms
- **语言**：Python | **License**：MIT | **Forks**：4,506
- **描述**：《动手学大模型 Dive into LLMs》系列编程实践教程。36,657 ⭐ + 4,506 forks，今日"中文 LLM 学习三部曲"第三部（学 LLM 原理）。
- **核心特性**：
  - 系列编程实践教程，中英双语
  - 覆盖：Transformer 原理 / 预训练 / 微调 / RLHF / Agent / RAG 全栈
  - 每章配套可运行代码，理论 + 实践结合
  - 持续更新，跟进最新 LLM 技术进展
  - 适合有编程基础的 AI 学习者
- **技术栈**：Python / PyTorch / Jupyter / Transformers
- **适用场景**：LLM 系统学习；AI 工程师技能提升；大模型应用开发基础。
- **推荐语**："今日与 minimind（做 LLM）和 hello-agents（用 LLM）构成完整的'LLM 学习三部曲'——dive-into-llms 是'学 LLM 原理'的核心资源，三者合计 131k Stars 说明中文 AI 教育内容在 Trending 上的影响力不亚于任何工具项目。"

---

### #09 bytedance/UI-TARS-desktop ⭐ 31,652 [新上榜]
- **仓库**：https://github.com/bytedance/UI-TARS-desktop
- **语言**：TypeScript | **License**：Apache-2.0 | **Forks**：3,145
- **描述**：The Open-Source Multimodal AI Agent Stack: Connecting Cutting-Edge AI Models and Agent Infra. ByteDance 出品，31,652 ⭐ + 3,145 forks，包含 Agent TARS（通用多模态 Agent CLI + Web UI）和 UI-TARS Desktop（GUI 自动化桌面应用）两大产品。
- **核心特性**：
  - **Agent TARS**：通用多模态 AI Agent，终端 + 浏览器 + 计算机 + 产品全覆盖
  - GUI Agent + Vision：视觉理解驱动的 GUI 自动化
  - 混合浏览器控制：GUI Agent / DOM / 混合策略三选一
  - MCP 内核：基于 MCP 协议，支持挂载任意 MCP Server
  - Event Stream：协议驱动的数据流追踪 + 调试
  - **UI-TARS Desktop**：Remote Computer Operator + Remote Browser Operator，免配置远程控制
  - 支持 Anthropic / VolcEngine doubao 等多个 LLM Provider
- **技术栈**：TypeScript / Electron / MCP / Puppeteer / Node.js
- **适用场景**：复杂多步骤网页自动化；跨平台 GUI 自动化测试；AI 原生产品开发 Agent 基础设施。
- **推荐语**："ByteDance 的 UI-TARS-desktop 今日与 chrome-devtools-mcp（#6）同框——两者都是'AI agent 控制浏览器'的工具，但路径不同：chrome-devtools-mcp 用 DevTools Protocol（调试视角），UI-TARS 用视觉 + DOM（用户视角）。今日 Trending 正在告诉我们：AI agent 操控浏览器将有多种路径共存。"

---

### #10 sgl-project/sglang ⭐ 27,588 [新上榜]
- **仓库**：https://github.com/sgl-project/sglang
- **语言**：Python | **License**：Apache-2.0 | **Forks**：5,808
- **描述**：SGLang is a high-performance serving framework for large language models and multimodal models. 27,588 ⭐ + 5,808 forks，今日出现在 Python Trending，是 LLM 服务框架领域的重要竞争者。
- **核心特性**：
  - 高性能 LLM 推理服务，吞吐量优于 vLLM（在多数场景下）
  - 支持 LLM + VLM（Vision Language Models）双模
  - RadixAttention：共享 KV cache 前缀，降低重复前缀场景延迟
  - SGLang Runtime（SRT）：优化的 Attention / Schedule / Memory Management
  - 支持 Llama / Qwen / DeepSeek / Mistral / Gemma 等主流模型
  - OpenAI API 兼容接口
- **技术栈**：Python / CUDA / Triton / OpenAI-compatible API
- **适用场景**：LLM 推理服务部署；高吞吐量 API server；多模态模型服务。
- **推荐语**："SGLang 今日以 27.6k Stars + 5.8k forks 上 Trending，可能与 DeepSeek 系列模型的最新支持或性能基准更新有关。是 vLLM 之后值得关注的 LLM serving 框架第二选择。"

---

### #11 anthropics/financial-services ⭐ 17,870 [持续 Day 3]
- **仓库**：https://github.com/anthropics/financial-services
- **语言**：Python | **License**：MIT | **Forks**：2,293
- **描述**：Anthropic 官方金融服务示例库。连续第 3 日上榜，Stars 从 05-08 的 12,894 增至今日 17,870，2 日增 +4,976，2,293 forks（显著增长）。
- **今日亮点**：三日累计：05-07 Explore（9.4k）→ 05-08 Top 12（12.9k）→ 05-10 Top 12（17.9k），持续高速增长，说明 Anthropic 金融 API 示例库的需求极为旺盛。
- **推荐语**："连续 Day 3 保持高增速——anthropics/financial-services 和 HKUDS/AI-Trader（#12）今日同框，金融 AI 今日从'教程'（financial-services）到'实战'（AI-Trader）全链路在 Trending 呈现，是金融 AI 赛道最强的联合信号。"

---

### #12 HKUDS/AI-Trader ⭐ 15,127 [新上榜]
- **仓库**：https://github.com/HKUDS/AI-Trader
- **语言**：Python | **License**：MIT | **Forks**：2,490
- **描述**："AI-Trader: 100% Fully-Automated Agent-Native Trading". 港大 HKUDS 数据科学实验室出品，15,127 ⭐ + 2,490 forks，完全自动化的 Agent 原生交易系统。今日 HKUDS 双项目同时上榜（AI-Trader Top 12 + ViMax Explore）。
- **核心特性**：
  - 100% 全自动 Agent 原生交易：从行情 → 分析 → 决策 → 执行全链路
  - Agent-Native 架构：非脚本自动化，而是 Agent 驱动的自主决策
  - 对接主流交易平台 API
  - 支持多种资产类别（股票 / 加密货币 / 期货）
  - HKUDS 学术背景：香港大学数据科学研究室背景
- **技术栈**：Python / LLM API / 交易所 API
- **适用场景**：量化 AI 交易研究；Agent 决策交易策略实验；全自动交易系统原型。
- **推荐语**："今日与 anthropics/financial-services（#11）同框，金融 AI 今日全链路呈现——教程层（financial-services，怎么用 Claude 做金融 AI）+ 实战层（AI-Trader，怎么用 Agent 做全自动交易）。同时 HKUDS 双项目（AI-Trader + ViMax Explore）同日上榜说明该实验室的研究产出爆发力极强。"

---

## 语言分布

| 语言 | 项目数 | 占比 | 代表项目 |
|---|---|---|---|
| Python | 8 | 67% | spec-kit / PaddleOCR / minimind / hello-agents / dive-into-llms / sglang / financial-services / AI-Trader |
| Markdown | 2 | 17% | awesome-claude-code / agent-skills |
| TypeScript | 2 | 17% | chrome-devtools-mcp / UI-TARS-desktop |

---

## GitHub Explore 精选

1. **datawhalechina/easy-vibe**（8,741 ⭐）— Python — 今日全语言 Trending。"💻 vibe coding 2026 | Your first modern programming course for beginners to master step by step." Datawhale 出品，870 forks。与 hello-agents（Top 12 #4）今日同框，Datawhale 今日双项目亮相：hello-agents（高阶，构建智能体）+ easy-vibe（入门，现代编程课），覆盖从编程零基础到 AI Agent 开发的完整学习路径。

2. **rowboatlabs/rowboat**（13,910 ⭐）— TypeScript — 今日全语言 Trending。"Open-source AI coworker, with memory." 1,378 forks，内置持久记忆的开源 AI 协作工作伙伴。今日与 rohitg00/agentmemory（Explore，3,712 ⭐，"Persistent memory for AI coding agents"）同框，agent memory 是今日 Trending 的另一条隐线主题——两个 memory 方向项目同日上全语言 Trending，证明"记忆"是 2026 年 AI agent 赛道的必争基础设施。

3. **lsdefine/GenericAgent**（10,355 ⭐）— Python — 今日 Python Trending。"Self-evolving agent: grows skill tree from 3.3K-line seed, achieving full system control with 6x less token consumption." 1,175 forks，自进化 Agent：从 3.3K 行种子代码生长 skill tree，实现完整系统控制，token 消耗降低 6 倍。今日最具学术研究价值的 Agent 架构项目。

4. **anthropics/claude-agent-sdk-python**（6,775 ⭐）— Python — 今日 Python Trending。Anthropic 官方 Claude Agent SDK Python 版本，972 forks。今日与 financial-services（Top 12 #11）和 awesome-claude-code（Top 12 #5）同框，Anthropic 今日三项目同时在 Trending——financial-services + claude-agent-sdk-python + Explore 中的 ViMax 引用，是 Anthropic 生态今日最密集的一次集体曝光。

5. **HKUDS/ViMax**（3,620 ⭐）— Python — 今日 Python Trending。"ViMax: Agentic Video Generation (Director, Screenwriter, Producer, and Video Generator All-in-One)" 665 forks，一个 AI agent 同时担任导演 + 编剧 + 制片人 + 视频生成器，全流程视频生成。今日与 AI-Trader（Top 12 #12）同属 HKUDS 实验室，HKUDS 今日成为 Trending 上"最多产出"的研究机构：金融交易 Agent + 多角色视频生成 Agent 同日亮相，技术广度极高。
