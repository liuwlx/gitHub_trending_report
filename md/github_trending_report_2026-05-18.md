# GitHub Trending 日报 · 2026-05-18

## Meta
- **日期**：2026-05-18
- **数据来源**：GitHub Trending（全语言）+ Python Trending
- **今日 Top 12**：12 个项目 | 累计 Stars：~517k | 编程语言：5 | 今日新上榜：12 | 持续上榜：0

---

## 今日洞察

### 🏗️ llama.cpp（110.7k）领衔——AI 推理基础层今日再度主导，与 05-12"SD-webui 日"共同构成 5 月"基础工具层双峰"

今日由 ggml-org/llama.cpp（110,736 ⭐）领衔，这是 05-12 AUTOMATIC1111/stable-diffusion-webui（162.9k）领衔以来第二次"AI 基础工具层主导日"。两次分别对应 AI 生态的两大基础层：图像生成推理层（SD-webui，05-12）与 LLM 文本推理层（llama.cpp，05-18）。llama.cpp 是事实上最重要的本地 LLM 推理库——Ollama / LM Studio / Jan.ai 等几乎所有本地 LLM 工具都以它为底层引擎。今日登顶意味着本周开发者注意力从"AI Agent 应用层"（上周 Skills 生态密集爆发）再次回归"基础推理基础设施"方向。

### 📡 ruvnet/RuView（59.5k）——"WiFi 透视"惊艳登场，AI 应用边界从代码空间延伸至物理空间

今日第三位 ruvnet/RuView（59,505 ⭐，7,763 forks）是本周最具技术惊艳感的项目："Turn ordinary WiFi into a spatial intelligence / sensing system. Detect people, measure breathing and heart rate, track movement, and monitor rooms — through walls, in the dark, with no cameras or wearables. Just physics."——用普通 WiFi 信号穿墙探测人体位置、测量呼吸心率、跟踪运动轨迹，无需摄像头和穿戴设备，纯物理原理。7,763 forks 是今日全榜最高 fork 数，内置 Claude Code & Codex Plugin，是今日唯一将 AI agent 能力引入"物理世界感知"的项目。

### 🔬 K-Dense-AI/scientific-agent-skills（24.1k）+ Imbad0202/academic-research-skills（10.2k）——"研究级 Skills"今日双双出现，Skills 生态向科研纵深拓展

今日 Trending 同时出现两个科研学术方向的 Skills 仓库：K-Dense-AI/scientific-agent-skills（24,130 ⭐，"135 scientific and research skills"，覆盖 100+ 科学数据库 + 70+ Python 科研包 + 药物发现/基因组学/临床研究，76 次发布）与 Imbad0202/academic-research-skills（10,224 ⭐，"Academic Research Skills for Claude Code: research → write → review → revise → finalize"，1,100 forks）。前者是"科学计算深度 Skills"（连接 PubChem / NCBI / UniProt 等真实数据库），后者是"学术写作完整流程 Skills"。两者同框标志着 Skills 生态已从"通用编程辅助"延伸到"专业科研自动化"。

### 🦀 HKUDS/CLI-Anything（36.3k）——港大 HKUDS 继 AI-Trader 后推出通用"Agent-Native 基础设施"

今日第五位 HKUDS/CLI-Anything（36,258 ⭐）来自与 AI-Trader 同一组织（港大 HKUDS）。CLI-Anything 的定位：通过自动化 7 阶段 Pipeline 将任意 GUI 软件生成对应 CLI 接口，使其可被 Claude Code / Codex / Cursor / OpenClaw 等 AI agent 直接调用。CLI-Hub（clianything.cc）提供中心化 CLI 注册表，pip 一行安装。AI-Trader 是面向金融的 Agent-Native 应用，CLI-Anything 是通用 Agent-Native 基础设施——HKUDS 今日完整呈现其"将任意软件 Agent-Native 化"的战略布局。

---

## 今日热门 Top 12（按总 Stars 排序）

### #01 ggml-org/llama.cpp ⭐ 110,736 [新上榜]
- **仓库**：https://github.com/ggml-org/llama.cpp
- **语言**：C++ | **License**：MIT | **Forks**：18,339
- **描述**：LLM inference in C/C++. 110,736 ⭐ + 18,339 forks，几乎所有本地 LLM 工具（Ollama / LM Studio / Jan.ai）的底层推理引擎，今日领衔 Top 12。
- **核心特性**：
  - 纯 C/C++ 实现，无依赖，跨平台（macOS / Linux / Windows）
  - 支持 GGUF 格式：Llama / Mistral / Phi / Gemma / Qwen 等几乎所有主流模型
  - 多后端加速：Apple Metal / CUDA / Vulkan / OpenCL / BLAS
  - 量化支持：2-8 bit 量化，大幅降低内存需求
  - llama-server：内置 HTTP server（OpenAI 兼容 API）
  - Speculative decoding / LoRA 推理 / Function calling
- **技术栈**：C / C++ / GGML / Metal / CUDA
- **推荐语**："今日 Top 1，本地 AI 生态的'底座'。今日登顶意味着本周开发者关注从 Agent Skills 工具层回归到最底层推理基础设施——通常预示着新模型发布或量化支持更新即将带动新工具链迭代。"

---

### #02 microsoft/ai-agents-for-beginners ⭐ 63,072 [新上榜]
- **仓库**：https://github.com/microsoft/ai-agents-for-beginners
- **语言**：Jupyter Notebook | **License**：MIT | **Forks**：21,124
- **描述**：12 Lessons to Get Started Building AI Agents. 63,072 ⭐ + 21,124 forks，微软官方 AI Agent 入门课程，12 课完整覆盖从 AI Agent 基础到实战构建。
- **核心特性**：
  - 12 课完整课程：AI Agent 基础概念到实际构建全覆盖
  - 覆盖 Autogen / Semantic Kernel / OpenAI API 等主流框架
  - Python + TypeScript 双语言示例
  - Jupyter Notebook 格式，配套视频和资源
  - 21k+ forks，企业和高校广泛使用
- **技术栈**：Python / Jupyter / TypeScript / OpenAI API / Azure AI
- **推荐语**："21k forks，fork/star = 0.334 说明大量开发者 fork 用于自定义学习。微软官方背书 + 12 课结构化内容是今日'Agent 学习资源'代表，与 scientific-agent-skills（应用层）形成学习→工具的完整衔接。"

---

### #03 ruvnet/RuView ⭐ 59,505 [新上榜]
- **仓库**：https://github.com/ruvnet/RuView
- **语言**：Python | **License**：MIT | **Forks**：7,763
- **描述**：π RuView turns commodity WiFi signals into real-time spatial intelligence, vital sign monitoring, and presence detection. 59,505 ⭐ + 7,763 forks，今日最具技术惊艳感项目，无摄像头无穿戴，纯 WiFi 信号穿墙感知。
- **核心特性**：
  - WiFi CSI 信号分析：利用信道状态信息分析室内空间
  - 人体存在检测：穿墙探测位置和运动轨迹
  - 生命体征监测：呼吸频率 + 心率实时测量
  - 无侵入式：仅需普通 WiFi 路由器，无额外硬件
  - Claude Code & Codex Plugin：AI agent 可直接调用感知能力
  - 边缘端优化，27 次发布持续更新
- **技术栈**：Python / WiFi CSI / NumPy / SciPy / 信号处理
- **推荐语**："7,763 forks 今日全榜最高！无摄像头穿墙探测人体的 WiFi 感知平台，内置 Claude Code Plugin——今日唯一将 AI agent 能力延伸到物理世界感知的项目。居家安全 / 老人监护 / 空间智能等场景，代表 AI 应用前沿从代码空间向物理空间的突破。"

---

### #04 ZhuLinsen/daily_stock_analysis ⭐ 36,748 [新上榜（重返）]
- **仓库**：https://github.com/ZhuLinsen/daily_stock_analysis
- **语言**：Python | **License**：MIT | **Forks**：36,063
- **描述**：LLM驱动的 A/H/美股智能分析：多数据源行情 + 实时新闻 + LLM决策仪表盘 + 多渠道推送，零成本定时运行，纯白嫖。36,748 ⭐ + 36,063 forks，Fork/Star 比率 0.981，本系列日报最极端的"自部署工具型"项目特征。
- **今日亮点**：重返 Top 12（曾于 05-11 上榜 at 35,102 ⭐），今日 36,748，比 05-11 增加 +1,646 Stars（~235/天的稳定增长）。Fork/Star = 36,063/36,748 = **0.981** 极端异常值——用户必须 fork + 配置自己的 API keys + GitHub Actions 才能使用，天然推高 Fork 率。
- **推荐语**："Fork/Star = 0.981，今日全榜最极端数据。自部署工具型项目的完美案例：零成本白嫖 = 必须 fork。今日重返说明金融 AI 自动化的持续热度——距 05-11 已过去 7 天仍保持 230+/天增速。"

---

### #05 HKUDS/CLI-Anything ⭐ 36,258 [新上榜]
- **仓库**：https://github.com/HKUDS/CLI-Anything
- **语言**：Python | **License**：Apache-2.0 | **Forks**：3,522
- **描述**："CLI-Anything: Making ALL Software Agent-Native" — 港大 HKUDS 出品（与 AI-Trader 同组织），通过 7 阶段自动化 Pipeline 将任意 GUI 软件转化为 AI agent 可调用的 CLI 接口。
- **核心特性**：
  - 7 阶段全自动 Pipeline：任意软件→生成 CLI wrapper
  - SKILL.md 自动生成（Phase 6.5）：每个生成的 CLI 自动附带 AI 可发现的 Skill 定义
  - CLI-Hub（clianything.cc）：中心化 CLI 注册表，pip install 一行安装
  - 支持 Claude Code / Codex / Cursor / OpenClaw / Antigravity
  - 真实演示：FreeCAD（好奇号探测器）/ Blender（无人机轨迹）/ Slay the Spire II（游戏自动化）
  - HARNESS.md 标准规范，社区贡献友好
- **技术栈**：Python / HARNESS.md / SKILL.md / CLI
- **推荐语**："HKUDS 继 AI-Trader（金融 Agent 应用）后推出 CLI-Anything（通用 Agent 基础设施）——完整呈现其'Agent-Native 生态'战略：先做垂直应用，再做通用基础设施。CLI-Anything 的意义在于：任何 GUI 软件都能被 AI agent 调用，这是未来'一切皆 Agent-Native'愿景的工具层实现。"

---

### #06 plausible/analytics ⭐ 25,702 [新上榜]
- **仓库**：https://github.com/plausible/analytics
- **语言**：Elixir | **License**：AGPL-3.0 | **Forks**：1,479
- **描述**：Open source, privacy-first web analytics. Lightweight, cookie-free Google Analytics alternative. Self-hosted or cloud. 25,702 ⭐ + 1,479 forks，今日唯一非 AI 直接相关项目，也是今日唯一 Elixir 语言项目。
- **核心特性**：
  - 隐私优先：无 Cookie，不收集个人数据，GDPR 合规
  - 轻量级：单行脚本，页面加载速度无影响（< 1KB）
  - Google Analytics 替代方案：页面浏览 / 跳出率 / 留存 / 来源分析
  - 自托管或 Cloud：完整自托管方案，数据主权掌握在自己手中
  - 实时仪表盘，自定义事件追踪
- **技术栈**：Elixir / Phoenix / PostgreSQL / ClickHouse
- **推荐语**："今日唯一非 AI 系项目，也是今日语言多样性的代表（Elixir）。在 AI 工具密集爆发的 Trending 中，plausible/analytics 的出现说明开发者对'隐私优先基础设施'的持续关注不会因 AI 热潮而减退——构建 AI 应用同样需要监控自己的用户行为，而 GDPR 合规的分析工具是刚需。"

---

### #07 K-Dense-AI/scientific-agent-skills ⭐ 24,130 [新上榜]
- **仓库**：https://github.com/K-Dense-AI/scientific-agent-skills
- **语言**：Python | **License**：MIT | **Forks**：2,556
- **描述**：A set of ready to use Agent Skills for research, science, engineering, analysis, finance and writing. 24,130 ⭐ + 2,556 forks，76 次发布，135 个科学研究 Skills，今日最专业的垂直 Skills 集合。
- **核心特性**：
  - 135 个科研 Skills，分 5 大类
  - 100+ 科学数据库访问：PubChem / ChEMBL / UniProt / NCBI / ClinicalTrials.gov / FRED / USPTO 等 78 个数据库
  - 70+ Python 科研包 Skills：RDKit / Scanpy / BioPython / PyTorch Lightning / scikit-learn / PennyLane / Qiskit 等
  - 9 科研集成 Skills：Benchling / DNAnexus / LatchBio / Protocols.io 等
  - 30+ 分析与传播工具：文献综述 / 科学写作 / 同行评审 / PPT / 海报 / Mermaid 图等
  - 领域：药物发现 / 基因组学 / 临床研究 / 多组学 / 量子计算
- **技术栈**：Python / SKILL.md / Markdown
- **推荐语**："135 个科研 Skills，覆盖从基因组测序到量子化学的完整科研领域。76 次发布说明这是一个持续维护的专业工程，而非简单的 AI 炒作。今日与 academic-research-skills 同框，两者共同构成了'科研 Skills 双层'：scientific-agent-skills（科学计算工具层）+ academic-research-skills（论文写作流程层）。"

---

### #08 humanlayer/12-factor-agents ⭐ 20,204 [新上榜]
- **仓库**：https://github.com/humanlayer/12-factor-agents
- **语言**：TypeScript | **License**：MIT | **Forks**：1,530
- **描述**：What are the principles we can use to build LLM-powered software that is actually good enough to put in the hands of production customers? 20,204 ⭐ + 1,530 forks，"AI Agent 的十二要素"——类比经典"12-Factor App"方法论，为生产级 LLM Agent 提供设计原则。
- **核心特性**：
  - 12 条 Agent 设计原则：类比 Heroku 的"12-Factor App"
  - 聚焦生产可用性：专门针对"真正能交付给生产用户"的 LLM 软件
  - HumanLayer 出品：人机协作 AI 平台背后的理论沉淀
  - 既有原则说明，也有代码示例
  - 面向工程师：不是学术论文，是实战经验总结
- **技术栈**：TypeScript / Python / Markdown
- **推荐语**："'12-Factor App'是 Web 应用工程化的里程碑方法论。12-factor-agents 试图为 AI Agent 做同样的事：从混乱的 LLM 应用开发实践中提炼出可复用的工程原则。今日 20k Stars 说明社区对'如何真正把 AI Agent 用于生产'的需求远超'如何构建 AI Agent Demo'。"

---

### #09 topoteretes/cognee ⭐ 17,310 [新上榜]
- **仓库**：https://github.com/topoteretes/cognee
- **语言**：Python | **License**：Apache-2.0 | **Forks**：1,813
- **描述**：Memory control plane for AI Agents in 6 lines of code. 17,310 ⭐ + 1,813 forks，"6 行代码为 AI Agent 提供记忆控制面"，比 MemoriLabs/Memori（05-11）更轻量的 Agent 记忆基础设施。
- **核心特性**：
  - 6 行代码集成：极简 API，快速为 Agent 添加记忆能力
  - Memory control plane：统一管理 Agent 的短期/长期记忆
  - 知识图谱 + 向量存储双引擎
  - 支持多种 LLM：OpenAI / Anthropic / Cohere 等
  - 与主流 Agent 框架集成：LangChain / LlamaIndex / AutoGen
- **技术栈**：Python / 知识图谱 / 向量数据库 / LLM
- **推荐语**："今日与 CLI-Anything（工具调用层）+ scientific-agent-skills（专业技能层）同框，三者共同构成 Agent 生态的不同层次：工具接口（CLI-Anything）+ 专业技能（scientific-agent-skills）+ 记忆持久化（cognee）。'6 行代码'的极简集成是今日最实用的 Agent 基础设施更新。"

---

### #10 tinyhumansai/openhuman ⭐ 15,400 [新上榜]
- **仓库**：https://github.com/tinyhumansai/openhuman
- **语言**：TypeScript | **License**：MIT | **Forks**：1,323
- **描述**：Your Personal AI super intelligence. Private, Simple and extremely powerful. 15,400 ⭐ + 1,323 forks，从 05-12（1,676 ⭐）到今日 05-18（15,400 ⭐）6 天内 Stars 暴增 +13,724（+818%）！
- **今日亮点**：6 天 +13,724 Stars（05-12: 1,676 → 05-18: 15,400），平均 +2,287/天，是今日全榜增速最快项目。上次（05-12）以 1,676 Stars 出现在全语言 Trending，当时还是"长尾新项目"，今日已 15.4k Stars，说明在过去 6 天内经历了一次社区传播爆发。
- **推荐语**："今日最惊人的增速——6 天 +818% Stars 增长！从 05-12 的 1,676 到今日 15,400，是本系列日报中见过的最快速度之一。'Private, Simple and extremely powerful' 的定位 + TypeScript 技术栈，显然在隐私 AI 领域触动了社区神经。"

---

### #11 CloakHQ/CloakBrowser ⭐ 14,484 [新上榜]
- **仓库**：https://github.com/CloakHQ/CloakBrowser
- **语言**：Python | **License**：MIT | **Forks**：1,130
- **描述**：Stealth Chromium that passes every bot detection test. Drop-in Playwright replacement with source-level fingerprint patches. 30/30 tests passed. 14,484 ⭐ + 1,130 forks，从 05-10（5,207）→ 05-12（6,529）→ 05-18（14,484），6 天 +7,955 Stars（+122%）。
- **今日亮点**：本系列日报长期持续增长项目——从 05-10 的 5,207 到今日的 14,484，8 天内 +9,277 Stars（+178%）。"30/30 bot detection tests passed" 是核心卖点，Drop-in Playwright 替代方案，source-level fingerprint patches。
- **推荐语**："连续 8 天持续增长（05-10 → 05-18：5.2k → 14.5k），是本系列日报追踪周期内持续增长最稳定的项目之一。Stealth 浏览器自动化赛道需求旺盛的背后：AI Agent 浏览器控制场景的普及让反爬虫检测绕过成为刚需。"

---

### #12 GreyDGL/PentestGPT ⭐ 13,153 [新上榜]
- **仓库**：https://github.com/GreyDGL/PentestGPT
- **语言**：Python | **License**：MIT | **Forks**：2,257
- **描述**：Automated Penetration Testing Agentic Framework Powered by Large Language Models. 13,153 ⭐ + 2,257 forks，LLM 驱动的自动化渗透测试 Agent 框架，今日安全 AI 方向唯一代表。
- **核心特性**：
  - 全自动渗透测试：规划 + 执行 + 报告生成全流程
  - LLM 驱动推理：GPT-4 / Claude 等 LLM 作为决策核心
  - 工具集成：Nmap / SQLMap / Metasploit 等安全工具调用
  - ReAct + Tree-of-Thought 推理框架
  - CTF 竞赛支持：自动化解题
- **技术栈**：Python / LangChain / OpenAI API / 安全工具集
- **推荐语**："今日唯一安全 AI 方向项目，与 RuView（物理空间感知）同框，两者代表了 AI 在传统安全领域的两个不同维度：主动渗透测试自动化（PentestGPT）vs 被动物理空间感知（RuView）。安全 AI 赛道在今日'技术基础设施'主题的 Trending 中自然浮现。"

---

## 语言分布

| 语言 | 项目数 | 占比 | 代表项目 |
|---|---|---|---|
| Python | 7 | 58% | llama.cpp/CLI-Anything/scientific-agent-skills/ZhuLinsen/cognee/CloakBrowser/PentestGPT/RuView |
| C++ | 1 | 8% | ggml-org/llama.cpp |
| TypeScript | 2 | 17% | tinyhumansai/openhuman / humanlayer/12-factor-agents |
| Elixir | 1 | 8% | plausible/analytics |
| Jupyter Notebook | 1 | 8% | microsoft/ai-agents-for-beginners |

---

## GitHub Explore 精选

1. **Imbad0202/academic-research-skills**（10,224 ⭐）— Python — 今日全语言 + Python 双榜，"Academic Research Skills for Claude Code: research → write → review → revise → finalize." 1,100 forks，学术写作完整流程 Skills，与 scientific-agent-skills 构成"科研 Skills 双层"。以 126 Stars 之差刚好落出 Top 12（#12 GreyDGL/PentestGPT 13,153 Stars）——今日 Top 13 就是 academic-research-skills。

2. **yichuan-w/LEANN**（11,423 ⭐）— Python — 今日 Python Trending，"[MLsys2026]: RAG on Everything with LEANN. Enjoy 97% storage savings while running a fast, accurate, and 100% private RAG application on your personal device." 1,020 forks，97% 存储节省的私有化 RAG，入选 MLsys2026 会议。今日 Top 14，与 cognee（#9，记忆控制面）同框，两者代表 Agent 记忆/知识管理的两个方向：长期记忆（cognee）vs 高效本地 RAG（LEANN）。

3. **wanshuiyin/Auto-claude-code-research-in-sleep**（9,817 ⭐）— Python — 今日 Python Trending，ARIS（Auto-Research-In-Sleep），从 05-12 的 8,898 增至今日 9,817（+919，持续稳定增长）。Markdown-only Skills，无框架无锁定，睡觉时自主完成 ML 研究。今日与 scientific-agent-skills + academic-research-skills 共同构成"研究自动化三层"：ARIS（睡眠中自动研究）+ academic（论文写作流程）+ scientific（科学计算技能）。

4. **tech-leads-club/agent-skills**（3,794 ⭐）— Markdown — 今日全语言 Trending，"The secure, validated skill registry for professional AI coding agents. Extend Antigravity, Claude Code, Cursor, Copilot and more with absolute confidence." 334 forks，面向专业团队的 Skills 安全验证注册表，强调安全性与可信度，是今日多个 Skills 仓库中定位最"企业级"的一个。

5. **topoteretes/cognee**（17,310 ⭐，已在 Top 12）— Python — 同时在 Python Trending position 24 出现，与 LEANN（11.4k RAG）今日同框，共同构成 Agent 记忆/知识管理双视角：cognee（记忆控制面，6 行代码集成）vs LEANN（高效私有 RAG，97% 存储节省）。
