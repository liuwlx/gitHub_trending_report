# GitHub Trending 日报 · 2026-05-11

## Meta
- **日期**：2026-05-11
- **数据来源**：GitHub Trending（全语言）+ Python Trending
- **今日 Top 12**：12 个项目 | 累计 Stars：~846k | 编程语言：3 | 今日新上榜：7 | 持续上榜：5

---

## 今日洞察

### 🏆 史上最强"王者齐聚"日：4 个 100k+ Stars 项目同日 Trending，累计 ~590k Stars 打头阵

今日 Top 12 前 4 名全部突破 100k Stars：everything-claude-code（178.8k）→ hermes-agent（143.3k）→ open-webui（136.5k）→ anthropics/skills（131.9k），是本系列日报记录以来单日出现最多 100k+ 项目的一天（之前最多是 1~2 个）。这 4 个巨头合计 590k Stars，占今日 Top 12 总 Stars 的 ~70%。这种"王者齐聚"格局不代表这 4 个都是今日诞生的爆款，而是说今日 GitHub Trending 算法将这 4 个大体量、高互动的项目同时推向了顶部——背后是今日 Claude Code 生态的集体大爆发触发了社区联动效应。

### 🔗 everything-claude-code（178.8k）+ hermes-agent（143.3k）+ anthropics/skills（131.9k）+ agent-skills（38.9k，Day 5）——Agent Skills 四层生态今日完整呈现

今日出现了史上最完整的"Agent Skills 纵向全景"：
- **anthropics/skills（131.9k）**：Anthropic 官方 Skills 规范仓库，SKILL.md 标准 + document/pdf/pptx/xlsx 生产级 skills，Claude.ai 内部已使用
- **addyosmani/agent-skills（38.9k，Day 5）**：工程层，生产级 AI coding agent Skills，20 个 Skill × 6 阶段
- **affaan-m/everything-claude-code（178.8k）**：综合优化层，Anthropic Hackathon Winner，Skills + instincts + memory + security，跨 Claude Code / Codex / Cursor / OpenCode / Gemini，ECC v2.0 集成 hermes-agent 作为 operator 层
- **NousResearch/hermes-agent（143.3k）**：ECC v2.0 的 operator 层，自我进化 Agent，内置学习循环，从经验中创建并改进 Skills

四层：官方规范（anthropics/skills）→ 工程 Skill（agent-skills）→ 综合优化系统（ECC）→ 自进化 operator（hermes-agent）。今日是 Claude Code + Agent Skills 生态历史上最全面的一次同框。

### 🤖 NousResearch/hermes-agent（143.3k）——"唯一内置学习循环的 Agent"，自我进化 + $5 VPS 低成本运行

Nous Research 出品，"The self-improving AI agent built by Nous Research. It's the only agent with a built-in learning loop — it creates skills from experience, improves them during use, nudges itself to persist knowledge, searches its own past conversations, and builds a deepening model of who you are across sessions." $5 VPS 或 serverless 低成本运行，不绑定本地机器，支持 Telegram 交互，支持 200+ 模型（OpenRouter / NVIDIA NIM / Nous Portal / OpenAI / Hugging Face 等），一行命令 `hermes model` 切换模型无需改代码。ECC v2.0 将其集成为 operator 层——两个项目今日同时上 Trending 并非巧合，而是同一生态的双向引流。

### 📊 ZhuLinsen/daily_stock_analysis（35.1k Stars，34.7k Forks）——Fork/Star 比率 0.989，今日最罕见的数据异常

35,102 Stars vs 34,716 Forks，Fork/Star 比率接近 1（正常项目约 0.2~0.3）。"LLM驱动的 A/H/美股智能分析：多数据源行情 + 实时新闻 + LLM决策仪表盘 + 多渠道推送，零成本定时运行，纯白嫖"——"零成本"+"纯白嫖"是高 Fork 率的直接原因：用户必须 fork 后配置自己的 API keys 并部署自己的实例，而非只是"看看"。这种"实用工具性 > 阅读性"的项目天然会产生高 Fork 率。今日它以 35.1k Stars + 34.7k Forks 上 Python Trending，是近期日报中最极端的 Fork/Star 比率案例，也反映了国内开发者对"AI 股票分析"赛道的强烈需求。

---

## 今日热门 Top 12（按总 Stars 排序）

### #01 affaan-m/everything-claude-code ⭐ 178,782 [新上榜]
- **仓库**：https://github.com/affaan-m/everything-claude-code
- **语言**：Markdown | **License**：MIT | **Forks**：27,572
- **描述**：The agent harness performance optimization system. Skills, instincts, memory, security, and research-first development for Claude Code, Codex, Opencode, Cursor and beyond. 178,782 ⭐ + 27,572 forks，Anthropic Hackathon Winner，170+ 贡献者，12+ 语言生态，今日 Top 12 Stars 最高。
- **核心特性**：
  - Skills + instincts + memory optimization + continuous learning + security scanning + research-first development 全栈
  - 跨平台：Claude Code / Codex / Cursor / OpenCode / Gemini 等 AI agent harness 全覆盖
  - ECC v2.0-rc.1：新增 public Hermes operator story（与今日 #2 hermes-agent 深度集成）
  - cross-harness architecture：跨平台统一架构，DRY Adapter Pattern
  - 12+ 语言生态：English / 中文 / 日本語 / 한국어 / Türkçe / Português 等
  - 10+ 个月密集日常使用 + 真实产品构建积累的生产级 configs
  - Anthropic Hackathon Winner 背书
- **技术栈**：Markdown / Shell / Claude Code hooks / AGENTS.md / SKILL.md
- **适用场景**：Claude Code 深度用户的完整 harness 优化；跨工具 AI coding agent 统一配置；production-ready Skills + hooks + rules + MCP configs 开箱即用。
- **推荐语**："178.8k 今日 Trending 第一，不只是最高 Stars，而是最重要的信号——ECC + hermes-agent + anthropics/skills + agent-skills 今日四层同框，Claude Code 生态的 Skills 体系在今日已形成完整工业级闭环。"

---

### #02 NousResearch/hermes-agent ⭐ 143,269 [新上榜]
- **仓库**：https://github.com/NousResearch/hermes-agent
- **语言**：Python | **License**：Apache-2.0 | **Forks**：22,353
- **描述**：The agent that grows with you. Nous Research 出品，143,269 ⭐ + 22,353 forks，唯一内置学习循环的自我进化 AI Agent，与 everything-claude-code ECC v2.0 深度集成，今日 Agent Skills 四层生态的 operator 层。
- **核心特性**：
  - 内置学习循环：从经验创建 Skills，使用中改进，主动持久化知识，跨 session 建立用户模型
  - 低成本运行：$5 VPS 或 serverless（空闲时近零成本），不绑定本地笔记本
  - Telegram 交互：云端运行时通过 Telegram 对话
  - 200+ 模型支持：OpenRouter / NVIDIA NIM / Nous Portal / OpenAI / Hugging Face / Kimi / MiniMax / z.ai 等
  - `hermes model` 一键切换模型，无需改代码，无 vendor lock-in
  - ECC v2.0 operator：everything-claude-code v2.0 的 Hermes operator story 基于此
  - 12 次发布，迭代持续
- **技术栈**：Python / OpenRouter / Telegram API / MCP
- **适用场景**：需要持久记忆 + 自我进化的个人 AI agent；多模型切换无锁定的 agent 开发；低成本云端 AI agent 部署。
- **推荐语**："今日与 everything-claude-code 同框并非偶然——ECC v2.0 专门集成了 hermes-agent 的 Hermes operator story。两个项目之间的引流是今日 143k 和 178k 同时出现在 Trending 的核心原因。"

---

### #03 open-webui/open-webui ⭐ 136,548 [新上榜]
- **仓库**：https://github.com/open-webui/open-webui
- **语言**：Python | **License**：MIT | **Forks**：19,444
- **描述**：User-friendly AI Interface (Supports Ollama, OpenAI API, ...). 136,548 ⭐ + 19,444 forks，LLM 本地化部署 UI 领域的龙头项目，今日重回 Trending Top 12。
- **核心特性**：
  - 支持 Ollama（本地 LLM）+ OpenAI API + 任意 OpenAI 兼容 endpoint
  - 完整对话 UI：历史记录 / 文件上传 / 语音输入 / 图像理解
  - Pipelines（插件系统）：自定义工作流 + RAG + 工具调用
  - 用户管理：多用户权限 + API key 管理
  - Docker 一键部署
  - 模型管理：从 Ollama 直接拉取、管理模型
- **技术栈**：Python / Svelte / Docker / Ollama API / OpenAI API
- **适用场景**：本地 LLM Web UI；企业内网 AI 对话平台；Ollama 图形化管理界面。
- **推荐语**："open-webui 今日以 136.5k Stars 重回 Top 12，可能是受到今日 Claude Code 生态集体爆发的带动——大量新用户进入 AI 生态圈后，开始寻找本地化部署解决方案。LLM UI 基础设施今日与 Agent Skills 层同步升温。"

---

### #04 anthropics/skills ⭐ 131,906 [新上榜]
- **仓库**：https://github.com/anthropics/skills
- **语言**：Python | **License**：Apache-2.0（部分 source-available） | **Forks**：15,531
- **描述**：Public repository for Agent Skills. Anthropic 官方 Agent Skills 规范仓库，131,906 ⭐ + 15,531 forks，今日 Agent Skills 四层生态的官方规范层，Claude.ai 内部已使用的生产级 skills 均开源于此。
- **核心特性**：
  - 官方 Skills 规范：SKILL.md 标准定义，Claude 动态加载 Skills 的机制文档
  - 生产级 Skills 开源：文档创建（skills/docx）/ PDF / PowerPoint（skills/pptx）/ Excel（skills/xlsx）均为 source-available
  - 多场景 Skills：创意应用（艺术/音乐/设计）/ 技术任务（Web 测试 / MCP server 生成）/ 企业工作流（沟通 / 品牌）
  - 可在 Claude Code / Claude.ai / Claude API 三端试用
  - Partner Skills 生态：合作伙伴贡献的 Skills
  - 完整 Skills 创建教程：[How to create custom skills](https://support.claude.com/en/articles/12512198-creating-custom-skills)
- **技术栈**：Markdown / Python / SKILL.md
- **适用场景**：学习 Anthropic 官方 Skills 最佳实践；参考生产级 Skills 实现；理解 Claude.ai 内部文档处理 Skills 的实现机制。
- **推荐语**："anthropics/skills 是今日四层 Skills 生态中最重要的'规范层'——Anthropic 官方定义了什么是 SKILL.md，什么是 Skills 的正确实现。如果你在用 agent-skills 或 everything-claude-code，今日应该同时查阅这个官方规范仓库。"

---

### #05 ultralytics/ultralytics ⭐ 56,990 [新上榜]
- **仓库**：https://github.com/ultralytics/ultralytics
- **语言**：Python | **License**：AGPL-3.0 | **Forks**：10,945
- **描述**：Ultralytics YOLO 🚀. 56,990 ⭐ + 10,945 forks，YOLO 系列目标检测框架的官方维护仓库，今日重回 Python Trending。
- **核心特性**：
  - YOLO11 / YOLOv8 系列最新模型：检测 / 分割 / 分类 / 姿态估计 / OBB
  - 多框架导出：ONNX / CoreML / TensorRT / TFLite / OpenVINO 等 20+ 格式
  - 极简 API：3 行代码实现推理或训练
  - 内置数据集管理 + 训练可视化（Weights & Biases / MLflow）
  - 支持分布式训练、多 GPU
  - HUB：无代码训练和部署平台
- **技术栈**：Python / PyTorch / ONNX / TensorRT
- **适用场景**：目标检测工程化部署；视觉模型快速原型；边缘设备 AI 视觉推理。
- **推荐语**："ultralytics 今日以 57k Stars 重回 Python Trending——在 AI coding 工具爆发的同一天，Computer Vision 基础工具也在同步升温，说明今日 Trending 不是单赛道的上涨，而是 AI 生态多维度的全面活跃。"

---

### #06 datawhalechina/hello-agents ⭐ 47,098 [持续 Day 2]
- **仓库**：https://github.com/datawhalechina/hello-agents
- **语言**：Python | **License**：CC-BY-4.0 | **Forks**：5,667
- **描述**：📚《从零开始构建智能体》——从零开始的智能体原理与实践教程。连续第 2 日上榜，Stars 从 05-10 的 45,976 增至今日 47,098（+1,122），5,667 forks。
- **今日亮点**：今日与 anthropics/skills（官方 Skills 教程）+ hermes-agent（自进化 Agent）同框，hello-agents 的"从零开始构建智能体"教程在今日 Agent 爆发日具有最直接的入门价值——想理解今日 Trending 各项目原理，从 hello-agents 开始是最佳路径。
- **推荐语**："连续 Day 2，在今日 Agent 技术集体爆发的背景下，hello-agents 是'明白人看懂今日 Trending'的最佳入口——从零理解 Agent 原理，再看 ECC/hermes-agent 会更清晰。"

---

### #07 addyosmani/agent-skills ⭐ 38,956 [持续 Day 5]
- **仓库**：https://github.com/addyosmani/agent-skills
- **语言**：Markdown | **License**：MIT | **Forks**：4,307
- **描述**：Production-grade engineering skills for AI coding agents. 连续第 5 日上榜！Stars 从 05-10 的 37,757 增至今日 38,956（+1,199），4,307 forks。
- **今日亮点**：今日 Day 5，与 anthropics/skills（官方层）+ everything-claude-code（综合优化层）+ hermes-agent（operator 层）同框，是今日"Agent Skills 四层生态"中的工程实践层，四层在同一天完整出现。
- **推荐语**："连续 Day 5——5 日连续上榜在本周日报记录中是空前的。今日四层 Skills 生态同框，agent-skills 作为工程实践层的地位被再次确认。"

---

### #08 ZhuLinsen/daily_stock_analysis ⭐ 35,102 [新上榜]
- **仓库**：https://github.com/ZhuLinsen/daily_stock_analysis
- **语言**：Python | **License**：MIT | **Forks**：34,716
- **描述**：LLM驱动的 A/H/美股智能分析：多数据源行情 + 实时新闻 + LLM决策仪表盘 + 多渠道推送，零成本定时运行，纯白嫖. LLM-powered stock analysis system for A/H/US markets. 35,102 ⭐ + 34,716 forks，Fork/Star 比率接近 1（今日最异常）。
- **核心特性**：
  - A/H/美股 三市场全覆盖智能分析
  - 多数据源行情：akshare / tushare / yfinance 聚合
  - LLM 决策仪表盘：GPT / Claude / DeepSeek 驱动的分析报告
  - 实时新闻 + 情感分析
  - 多渠道推送：微信 / 邮件 / Telegram / 钉钉
  - 零成本定时运行：GitHub Actions 自动执行
  - "纯白嫖"：利用免费 API 额度和 GitHub Actions CI
- **技术栈**：Python / akshare / tushare / LLM API / GitHub Actions
- **适用场景**：个人 A/H 股 + 美股自动化分析推送；量化研究辅助工具；LLM 金融分析原型。
- **推荐语**："34,716 Forks vs 35,102 Stars——Fork/Star 比率 0.989，近期日报中最极端的异常值。'零成本定时运行 + 纯白嫖'是直接原因：用户必须 fork 才能配置自己的 API keys 并部署。这是一个'自部署工具'而非'看看即可'的项目，今日与 HKUDS/AI-Trader（#11）同框，金融 AI 赛道在 Trending 连续多日活跃。"

---

### #09 bytedance/UI-TARS-desktop ⭐ 32,529 [持续 Day 2]
- **仓库**：https://github.com/bytedance/UI-TARS-desktop
- **语言**：TypeScript | **License**：Apache-2.0 | **Forks**：3,218
- **描述**：The Open-Source Multimodal AI Agent Stack: Connecting Cutting-Edge AI Models and Agent Infra. 连续第 2 日上榜，Stars 从 05-10 的 31,652 增至今日 32,529（+877），3,218 forks。Agent TARS + UI-TARS Desktop 双产品栈，ByteDance 出品。
- **今日亮点**：在今日 Agent 生态大爆发的背景下，UI-TARS-desktop 持续 Day 2 说明"多模态 Agent + GUI 自动化"赛道的持续热度。今日与 hermes-agent（学习循环 Agent）+ MemoriLabs/Memori（Agent 记忆）同框，Agent 基础设施三个维度（GUI 操控 + 持续学习 + 结构化记忆）今日齐聚。
- **推荐语**："Day 2 持续，今日与 hermes-agent + Memori 同框——GUI 操控 + 自我进化 + 结构化记忆三维度同日升温，2026 年 AI agent 基础设施的三个核心能力今日完整呈现。"

---

### #10 anthropics/financial-services ⭐ 19,502 [持续 Day 4]
- **仓库**：https://github.com/anthropics/financial-services
- **语言**：Python | **License**：MIT | **Forks**：2,529
- **描述**：Anthropic 官方金融服务示例库。连续第 4 日上榜！Stars 从 05-10 的 17,870 增至今日 19,502（+1,632），2,529 forks。4 日轨迹：05-07 Explore（9.4k）→ 05-08 Top 12（12.9k）→ 05-10 Top 12（17.9k）→ 05-11 Top 12（19.5k），累计增长 +10.1k。
- **今日亮点**：连续 Day 4，今日又与 ZhuLinsen/daily_stock_analysis（#8）和 HKUDS/AI-Trader（#11）同框——金融 AI 今日三项目同在 Top 12，是近 5 日最密集的一次金融 AI 集中出现：Anthropic 官方教程（how to）+ 港大全自动 Agent 交易（实战系统）+ 国内 LLM 分析工具（零成本自部署）。
- **推荐语**："4 日连续上榜，今日与 AI-Trader + daily_stock_analysis 金融 AI 三项目同框——三层金融 AI：Anthropic 官方 API 教程（如何用 Claude 做金融 AI）+ HKUDS Agent 原生交易系统 + 国内 LLM 分析工具。金融 AI 赛道本周是 Trending 最活跃的应用赛道。"

---

### #11 HKUDS/AI-Trader ⭐ 15,887 [持续 Day 2]
- **仓库**：https://github.com/HKUDS/AI-Trader
- **语言**：Python | **License**：MIT | **Forks**：2,552
- **描述**："AI-Trader: 100% Fully-Automated Agent-Native Trading". 连续第 2 日上榜，Stars 从 05-10 的 15,127 增至今日 15,887（+760），2,552 forks。港大 HKUDS 数据科学实验室出品。
- **今日亮点**：今日与 daily_stock_analysis（#8）+ financial-services（#10）构成金融 AI 三项目同框，HKUDS 今日也是连续第 2 日出现在 Top 12（昨日还有 ViMax 在 Explore）。
- **推荐语**："金融 AI 三件套今日再次同框：Anthropic 金融教程（#10）+ 国内 LLM 分析工具（#8）+ 港大 Agent 交易（#11）——这 3 个项目从'如何做'到'工具层'到'系统层'的三层覆盖，是金融 AI 赛道本周持续升温的最强信号。"

---

### #12 MemoriLabs/Memori ⭐ 14,278 [新上榜]
- **仓库**：https://github.com/MemoriLabs/Memori
- **语言**：Python | **License**：MIT | **Forks**：1,974
- **描述**：Memori is agent-native memory infrastructure. A LLM-agnostic layer that turns agent execution and conversation into structured, persistent state for production systems. 14,278 ⭐ + 1,974 forks，agent-native 结构化持久记忆基础设施。
- **核心特性**：
  - agent-native 记忆层：Agent 执行和对话转化为结构化持久状态
  - LLM-agnostic：不绑定任何特定 LLM，兼容所有主流 LLM API
  - 生产系统级：设计为 production system 的 memory layer，非 toy 项目
  - 结构化存储：非向量数据库，而是结构化状态持久化
  - 跨 session 持久记忆：Agent 可跨对话、跨任务访问历史状态
- **技术栈**：Python / LLM API / 结构化存储
- **适用场景**：生产 Agent 系统的记忆层；多轮对话持久化；Agent 执行历史结构化存储。
- **推荐语**："今日与 hermes-agent（自进化 Agent，内置学习循环）和 UI-TARS-desktop（GUI Agent）同框——三者今日构成 Agent 基础设施三件套：GUI 操控（UI-TARS）+ 持续学习（hermes-agent）+ 结构化记忆（Memori）。2026 年 AI agent 的三个核心基础设施今日同时在 Trending 出现。"

---

## 语言分布

| 语言 | 项目数 | 占比 | 代表项目 |
|---|---|---|---|
| Python | 9 | 75% | hermes-agent / open-webui / anthropics-skills / ultralytics / hello-agents / daily_stock_analysis / financial-services / AI-Trader / Memori |
| Markdown | 2 | 17% | everything-claude-code / agent-skills |
| TypeScript | 1 | 8% | UI-TARS-desktop |

---

## GitHub Explore 精选

1. **jundot/omlx**（13,466 ⭐）— TypeScript/Swift — 今日全语言 Trending。"LLM inference server with continuous batching & SSD caching for Apple Silicon — managed from the macOS menu bar." 1,144 forks，为 Apple Silicon 专属优化的 LLM 推理服务器，macOS 菜单栏管理，持续批处理 + SSD 缓存。在今日大量云端 Agent 工具集中的背景下，omlx 代表了另一个方向：Mac 本地 LLM 推理的极致优化，是对"不想依赖云 API"用户的最佳选择。

2. **lsdefine/GenericAgent**（10,710 ⭐）— Python — 今日全语言 + Python 双榜，Day 2（昨日 10,355）。"Self-evolving agent: grows skill tree from 3.3K-line seed, achieving full system control with 6x less token consumption." 1,205 forks，自进化 Agent 第二日。今日与 hermes-agent（自进化，学习循环）同框，两者是"自进化 Agent"赛道今日的双代表——hermes-agent 走"自然语言+多模型"路线，GenericAgent 走"代码进化+token 效率"路线，路径不同但方向一致。

3. **CloakHQ/CloakBrowser**（5,207 ⭐）— Python — 今日全语言 + Python 双榜。"Stealth Chromium that passes every bot detection test. Drop-in Playwright replacement with source-level fingerprint patches. 30/30 tests passed." 393 forks，通过所有反爬虫检测的 Stealth Chromium，Playwright 直接替代品，源码级指纹补丁。今日与 UI-TARS-desktop（GUI Agent 浏览器控制）和 chrome-devtools-mcp（昨日 #6，DevTools MCP）的连续叙事中，CloakBrowser 代表了"AI agent 浏览器控制"的第三条路线：反检测隐身路线。

4. **OpenTalker/SadTalker**（13,797 ⭐）— Python — 今日 Python Trending。"[CVPR 2023] SadTalker: Learning Realistic 3D Motion Coefficients for Stylized Audio-Driven Single Image Talking Face Animation." 2,627 forks，CVPR 2023 音频驱动的单图说话人脸动画生成。今日与 ultralytics（YOLO，#5）同框，Computer Vision 经典项目今日双上 Trending，说明 CV 领域在 LLM/Agent 大潮下依然保持强劲社区活力。

5. **MemoriLabs/Memori** → 已进入 Top 12 #12，不重复列出。替补：**decolua/9router**（7,634 ⭐）— TypeScript — 今日全语言 Trending。"Unlimited FREE AI coding. Connect Claude Code, Codex, Cursor, Cline, Copilot, Antigravity to FREE Claude/GPT/Gemini via 40+ providers. Auto-fallback, RTK -40% tokens, never hit limits." 1,261 forks。今日与 everything-claude-code（#1，178.8k）同框，9router 是"降低 AI coding 成本"的最直接工具——ECC 解决"如何更好地用 AI coding agent"，9router 解决"如何免费无限用 AI coding agent"，两者今日同时上榜是开发者社区对"AI coding 成本优化"需求的双重验证。
