# GitHub Trending 日报 · 2026-05-21

## Meta
- **日期**：2026-05-21
- **数据来源**：GitHub Trending（全语言）+ Python Trending
- **今日 Top 12**：12 个项目 | 累计 Stars：~927k | 编程语言：4 | 今日新上榜：5 | 持续上榜：7（含 Day 2/3）

---

## 今日洞察

### 🎯 obra/superpowers 突破 200k——本系列日报首个 200k+ 项目，Skills 三强连续 Day 2

obra/superpowers 今日以 200,102 Stars 实现历史性突破：自本系列日报（05-06 至今）追踪以来，首次有项目突破 200k Stars 大关。连续 Day 2（05-20: 198,743 → 05-21: 200,102，+1,359），今日与 multica-ai/andrej-karpathy-skills（140,969，+2,315）和 msitarzewski/agency-agents（102,880，+994）同框，三个 Skills/Methodology 类仓库连续第二天包揽 Top 1/2/5，合计 443k Stars，Agent Skills 方法论生态的持续热度在今日达到新高度。Skills 三强的连续上榜意味着 2026 年"如何让 coding agent 更聪明更专业"已成为整个开发者社区的持续性核心议题，而不只是单日热点。

### 🤖 karpathy/autoresearch（82,344 ⭐）——Andrej Karpathy 新作：AI agent 自主做 LLM 研究，"你睡觉的时候完成 100 次实验"

今日最震撼的新项目：Andrej Karpathy（前 Tesla AI 总监、前 OpenAI 科学家）亲自操刀的 autoresearch——"AI agents running research on single-GPU nanochat training automatically"，82,344 Stars + 11,954 forks。机制极其简洁精妙：AI agent 循环执行 ① 修改 train.py → ② 训练 5 分钟 → ③ 评估 val_bpb（验证集 bits per byte）→ ④ 保留或丢弃 → ⑤ 重复。设计原则：single file to modify（只改 train.py）+ fixed 5-minute time budget（12 实验/小时，约 100 实验/晚）+ self-contained（单 GPU，无分布式）。你不再修改 Python 代码，你修改的是 program.md——"programming the program"。README 开头有一段极具 Karpathy 风格的独白："那个时代（人类主导研究）已经结束了……这个 repo 记录了一切的起点。—@karpathy，2026 年 3 月"。今日还有 multica-ai/andrej-karpathy-skills（Karpathy 观察→CLAUDE.md）Day 2 同框，两者形成"Karpathy 洞见的两种形态：别人整理 vs 本人亲作"的有趣对照。

### 🏛️ volcengine/OpenViking（24,311 ⭐）——字节跳动开源"Agent 上下文数据库"，文件系统范式替代向量 RAG

字节跳动 volcengine 今日新上榜 OpenViking（24,311 ⭐，38 次发布），定位"The Context Database for AI Agents"，正面挑战传统向量 RAG 的上下文管理模式。核心创新：用"文件系统范式"统一管理 Agent 的 memories + resources + skills，而非分散在代码/向量库/配置文件中。五大技术支柱：① 文件系统范式（解决上下文碎片化）→ ② L0/L1/L2 三层按需加载（降低 token 消耗）→ ③ 目录递归检索（比平铺向量 RAG 精准）→ ④ 可视化检索轨迹（上下文可观测，告别 RAG 黑盒）→ ⑤ 自动会话管理（Agent 越用越聪明）。字节跳动通过 volcengine + OpenViking + OpenClaw 的三层布局，构建了独立于 Anthropic/OpenAI 体系的完整 Agent 基础设施栈，今日首次进入本系列日报 Top 12。

### 🔥 HKUDS/CLI-Anything + ZhuLinsen 双双 Day 3，CLI-Anything 今日首次超越 ZhuLinsen

两个中国项目今日均连续第三天上榜——这是本系列日报追踪以来中国项目首次出现"两个项目连续 3 天双上榜"的格局。HKUDS/CLI-Anything（05-18: 36,258 → 05-20: 37,889 → 05-21: 38,563，3天 +2,305），ZhuLinsen/daily_stock_analysis（05-18: 36,748 → 05-20: 37,897 → 05-21: 38,144，3天 +1,396）。关键位次变化：今日 CLI-Anything（38,563）Stars 首次反超 ZhuLinsen（38,144），完成了连续三天你追我赶后的位次交换。两者背后的逻辑截然不同：ZhuLinsen 靠"Fork/Star=36,831/38,144=0.965，零成本自部署金融分析"驱动；CLI-Anything 靠"让所有软件 Agent-Native 的产品愿景 + 持续技术迭代"驱动。

---

## 今日热门 Top 12（按总 Stars 排序）

### #01 obra/superpowers ⭐ 200,102 [Day 2 · 200k 里程碑！]
- **仓库**：https://github.com/obra/superpowers
- **语言**：Markdown | **License**：MIT | **Forks**：17,842
- **描述**：An agentic skills framework & software development methodology that works. 200,102 ⭐（05-20: 198,743，+1,359），今日突破 200k Stars，本系列日报首个 200k+ 项目，连续 Day 2。
- **今日动态**：05-20（198,743）→ 05-21（200,102），+1,359 Stars（~1,359/天），实现历史性 200k 突破。连续 Day 2 且三个 Skills 类仓库同框，方法论层 Agent Skills 持续强劲。
- **推荐语**："200k！历史性里程碑。obra/superpowers 连续第二天领衔，作为本系列日报追踪以来首个突破 200k Stars 的项目，它证明了'完整 Agent 开发方法论'不是单日热点，而是一个持续增长的长期需求。今日与 multica-ai（+2,315）和 agency-agents（+994）合计 443k Stars，Skills 方法论三强的连续同框是本周 Trending 最重要的结构性信号。"

---

### #02 multica-ai/andrej-karpathy-skills ⭐ 140,969 [Day 2]
- **仓库**：https://github.com/multica-ai/andrej-karpathy-skills
- **语言**：Markdown | **License**：MIT | **Forks**：14,470
- **描述**：A single CLAUDE.md file to improve Claude Code behavior, derived from Andrej Karpathy's observations on LLM coding pitfalls. 140,969 ⭐（05-20: 138,654，+2,315），今日 Day 2 增速最快的持续项目。
- **今日动态**：05-20（138,654）→ 05-21（140,969），+2,315 Stars（今日持续项目增速第一）。今日与 karpathy/autoresearch（Karpathy 本人新作）同框：一个是"别人把 Karpathy 洞见整理成 CLAUDE.md"，另一个是"Karpathy 本人直接做 AI agent 研究工具"——两种"Karpathy 影响力的形态"今日首次同框出现。
- **推荐语**："Day 2 今日增速最快（+2,315），说明这个单 CLAUDE.md 文件的价值被越来越多开发者认可。今日与 karpathy/autoresearch 同框的意义远超数字本身：Karpathy 的影响力在今日 Trending 中以'思想间接影响（multica-ai）'和'作品直接贡献（autoresearch）'两种形态同框，是今日最有趣的叙事结构。"

---

### #03 ggml-org/llama.cpp ⭐ 111,864 [重返（05-18 后 3 天）]
- **仓库**：https://github.com/ggml-org/llama.cpp
- **语言**：C++ | **License**：MIT | **Forks**：18,510
- **描述**：LLM inference in C/C++. 111,864 ⭐（05-18: 110,736，+1,128 in 3 days），从 05-18 Top 1 后消失 2 天，今日重返。
- **今日动态**：05-18（110,736，Top 1）→ 不在 05-20 Top 12 → 05-21（111,864，重返 #03）。3 天 +1,128 Stars（~376/天），稳定持续增长。今日重返的时机恰好与 github/spec-kit + karpathy/autoresearch 等 AI 工具类项目同框，共同构成"AI Agent 基础基础设施"的讨论背景。
- **推荐语**："llama.cpp 今日重返，稳稳地站在 C++ 本地 LLM 推理的基本盘上。18.5k forks 是今日全榜最高 forks 数，说明它是整个 AI 基础设施中被'拿来改造'最多的项目。在 Skills 三强方法论主导的格局中，llama.cpp 代表了另一个维度：能力再强的 Skills，最终都需要一个高效的 LLM 推理引擎来支撑。"

---

### #04 github/spec-kit ⭐ 104,125 [新上榜]
- **仓库**：https://github.com/github/spec-kit
- **语言**：TypeScript | **License**：MIT | **Forks**：9,172
- **描述**：Toolkit to help you get started with Spec-Driven Development. 104,125 ⭐ + 9,172 forks，GitHub 官方出品，Spec-Driven Development（规格驱动开发）工具包，支持 30+ AI coding agents。
- **核心特性**：
  - 规格驱动开发（Spec-Driven Development）方法论：先写规格，再让 AI agent 实现
  - specify CLI + AI coding agent slash commands
  - 结构化 6 步工作流，支持 30+ AI coding agents
  - 强调"executable specifications（可执行规格）"优于传统文档
  - GitHub 官方（github/ 组织）出品，权威背书
- **推荐语**："今日新上榜，104.1k Stars，GitHub 官方的 Spec-Driven Development 工具包。今日与 obra/superpowers（Skills 方法论）同框，两者代表了'如何让 AI coding agent 更系统化工作'的两种路径：obra 是'Skills 组合驱动'，spec-kit 是'规格文档驱动'。两者均由有影响力的组织（obra 作者 / GitHub 官方）发布，今日同框揭示了'AI coding agent 方法论'正在从单一路径向多元竞争格局演进。"

---

### #05 msitarzewski/agency-agents ⭐ 102,880 [Day 2]
- **仓库**：https://github.com/msitarzewski/agency-agents
- **语言**：Markdown | **License**：MIT | **Forks**：16,955
- **描述**：A complete AI agency at your fingertips — Each agent is a specialized expert with personality, processes, and proven deliverables. 102,880 ⭐（05-20: 101,886，+994），连续 Day 2。
- **今日动态**：05-20（101,886）→ 05-21（102,880），+994 Stars（Day 2）。今日与 obra/superpowers（方法论层）和 multica-ai（最小配置层）共同构成"Skills 三强"连续 Day 2，agency-agents 在三者中代表"角色人格层"。
- **推荐语**："Day 2 稳步增长，Skills 三强中的'角色人格层'代表。今日与 github/spec-kit 的新上榜共同说明：AI coding agent 的'工作方式'正在成为整个社区持续讨论的核心课题——无论是 Skills（obra）、最小配置（karpathy-skills）、角色人格（agency-agents），还是规格文档（spec-kit），都是这个大课题下的不同答案。"

---

### #06 karpathy/autoresearch ⭐ 82,344 [新上榜]
- **仓库**：https://github.com/karpathy/autoresearch
- **语言**：Python | **License**：MIT | **Forks**：11,954
- **描述**：AI agents running research on single-GPU nanochat training automatically — Andrej Karpathy 新作，AI agent 自主做 LLM 研究，每晚约 100 次自主实验。82,344 ⭐ + 11,954 forks。
- **核心特性**：
  - 核心机制：AI agent 循环（修改 train.py → 训练 5 分钟 → 评估 val_bpb → 保留/丢弃 → 重复）
  - 三个核心文件：prepare.py（固定，数据准备）/ train.py（agent 修改的唯一文件）/ program.md（你设定的"研究组代码"）
  - Fixed 5-minute time budget：12 实验/小时，~100 实验/晚（睡一觉醒来有完整实验日志）
  - "You are programming the program.md"——你不写代码，你写 Agent 的工作方式
  - 训练 nanochat（简化版 GPT），单 GPU H100，评估指标 val_bpb（词汇表无关）
  - Self-contained：无分布式，无复杂配置，PyTorch + uv
- **技术栈**：Python / PyTorch / CUDA / nanochat (GPT-style mini LLM)
- **推荐语**："今日最震撼的项目！Karpathy 的独白是今日报告最值得收藏的段落：'那个时代（人类在 group meeting 中同步的研究范式）已经结束了……这个 repo 记录了一切的起点。'autoresearch 把 AI coding agent 的使用推向了新的边界：不是让 agent 写功能代码，而是让 agent 做机器学习研究。这不是科幻，这是今日就能跑的真实工具——一个 H100，一晚 100 次实验，醒来有更好的模型。"

---

### #07 vllm-project/vllm ⭐ 80,586 [新上榜]
- **仓库**：https://github.com/vllm-project/vllm
- **语言**：Python | **License**：Apache-2.0 | **Forks**：17,023
- **描述**：A high-throughput and memory-efficient inference and serving engine for LLMs. 80,586 ⭐ + 17,023 forks，LLM 推理 serving 框架，高吞吐 + 内存高效。
- **核心特性**：
  - PagedAttention：革命性 KV cache 管理算法，大幅降低显存碎片
  - Continuous Batching：动态批处理，极大提升吞吐量
  - 支持主流模型：Llama / Mistral / Qwen / GPT-NeoX 等
  - 兼容 OpenAI API
  - 17k forks，是今日仅次于 llama.cpp（18.5k）的第二高 forks 项目
- **技术栈**：Python / CUDA / C++ / PagedAttention
- **推荐语**："今日新上榜，80.6k Stars + 17k forks，LLM 推理 serving 的行业标准工具。今日与 llama.cpp（本地单机推理，C++）同框，两者代表了 LLM 推理的两大方向：llama.cpp 是'边缘端/个人电脑'的极致优化，vllm 是'数据中心/API 服务'的高吞吐优化——今日 Trending 同时覆盖这两个方向，说明 AI 基础设施的两端都在同步升温。"

---

### #08 unslothai/unsloth ⭐ 64,855 [Day 2]
- **仓库**：https://github.com/unslothai/unsloth
- **语言**：Python | **License**：Apache-2.0 | **Forks**：5,740
- **描述**：Unsloth Studio is a web UI for training and running open models like Gemma 4, Qwen3.6, DeepSeek, gpt-oss locally. 64,855 ⭐（05-20: 64,749，+106），Day 2。
- **今日动态**：05-20（64,749）→ 05-21（64,855），+106 Stars（Day 2，今日增速较慢）。今日与 karpathy/autoresearch（同为"本地训练"方向）同框，两者覆盖本地 LLM 训练的两种视角：unsloth 是"Web UI 降低门槛"，autoresearch 是"自主 agent 提高效率"。
- **推荐语**："Day 2，增速放缓（+106），但今日与 karpathy/autoresearch 同框颇有意思：unsloth 用 Web UI 让普通开发者可以在本地训练模型，autoresearch 让 AI agent 自主进行 LLM 研究——两者共同定义了'民主化 LLM 训练'的边界正在向何处扩展。"

---

### #09 HKUDS/CLI-Anything ⭐ 38,563 [Day 3]
- **仓库**：https://github.com/HKUDS/CLI-Anything
- **语言**：Python | **License**：Apache-2.0 | **Forks**：3,664
- **描述**："CLI-Anything: Making ALL Software Agent-Native" — 7 阶段 Pipeline，将任意 GUI 软件生成 AI agent 可调用的 CLI 接口。38,563 ⭐（05-20: 37,889，+674），Day 3。
- **今日动态**：05-18（36,258）→ 05-20（37,889）→ 05-21（38,563），3天累计 +2,305 Stars。**今日 38,563 首次超越 ZhuLinsen（38,144），完成连续 3 天你追我赶后的位次交换。** 是本系列日报追踪以来连续上榜天数最多的中国项目之一（并列 ZhuLinsen）。
- **推荐语**："Day 3！今日 38,563 首次反超 ZhuLinsen（38,144），虽然只差 419 Stars，但这是一个象征性节点：'让所有软件 Agent-Native 的产品愿景'以稳定日增速（~674/天）超过了'Fork/Star 异常高的金融工具'。今日与 volcengine/OpenViking（字节的 Agent 上下文数据库）同框，两者共同代表中国 AI 团队在 Agent 基础设施领域的两种布局：工具接口层（CLI-Anything）vs 上下文管理层（OpenViking）。"

---

### #10 ZhuLinsen/daily_stock_analysis ⭐ 38,144 [Day 3]
- **仓库**：https://github.com/ZhuLinsen/daily_stock_analysis
- **语言**：Python | **License**：MIT | **Forks**：36,831
- **描述**：LLM驱动的 A/H/美股智能分析：多数据源行情 + 实时新闻 + LLM决策仪表盘 + 多渠道推送，零成本定时运行。38,144 ⭐（05-20: 37,897，+247）。
- **今日动态**：05-18（36,748）→ 05-20（37,897）→ 05-21（38,144），3天累计 +1,396 Stars。Fork/Star = 36,831/38,144 = 0.965，今日依然是全榜最高 Fork/Star 比率。今日增速放缓（+247，vs 05-20 的 +1,149），但 Fork/Star 依然异常高位。
- **推荐语**："Day 3，增速明显放缓（+247 vs 昨日 +1,149），但 Fork/Star = 0.965 依然是今日全榜最高——说明'必须 fork 才能用'的自部署需求依然持续，只是新用户流入速度放缓。从 3 天数据看 CLI-Anything vs ZhuLinsen：CLI-Anything 增速持续稳定（+674/天），ZhuLinsen 增速逐渐放缓（3天从 1,149/天→247/天），两条曲线的交叉在今日体现为 CLI-Anything 首次超越 ZhuLinsen。"

---

### #11 Alishahryar1/free-claude-code ⭐ 26,970 [Day 2]
- **仓库**：https://github.com/Alishahryar1/free-claude-code
- **语言**：Python | **License**：MIT | **Forks**：4,009
- **描述**：Use claude-code for free in the terminal, VSCode extension or discord like OpenClaw (voice supported). 26,970 ⭐（05-20: 26,465，+505），Day 2。
- **今日动态**：05-20（26,465）→ 05-21（26,970），+505 Stars（Day 2，~505/天），持续稳定增长，说明"免费 Claude Code"的刚需持续旺盛。
- **推荐语**："Day 2，稳定 +505/天。'免费 Claude Code'的刚需是一个持续性话题而非单日热点——尤其是在今日 github/spec-kit（官方 Spec-Driven Development）和 obra/superpowers（付费平台方法论）高调出现的背景下，free-claude-code 代表了一批'想要用 Claude Code 但不愿付费'的开发者群体，这个群体的持续存在和增长本身就是一个重要的市场信号。"

---

### #12 volcengine/OpenViking ⭐ 24,311 [新上榜]
- **仓库**：https://github.com/volcengine/OpenViking
- **语言**：Python | **License**：Apache-2.0 | **Forks**：1,821
- **描述**：OpenViking is an open-source context database designed specifically for AI Agents. Unifies management of context (memory, resources, and skills) through a file system paradigm. 24,311 ⭐，字节跳动 volcengine 出品，38 次发布。
- **核心特性**：
  - 定位：Agent 上下文数据库，替代传统碎片化向量 RAG 方案
  - 五大技术支柱：
    1. 文件系统范式（统一管理 memories + resources + skills，解决碎片化）
    2. L0/L1/L2 三层按需加载（降低 token 消耗）
    3. 目录递归检索（目录定位 + 语义搜索，精准度超平铺向量 RAG）
    4. 可视化检索轨迹（上下文可观测，告别 RAG 黑盒）
    5. 自动会话管理（上下文自迭代，Agent 越用越聪明）
  - 38 次发布，英文/中文/日语三语言文档
  - 与 OpenClaw（volcengine Agent 平台）深度集成
- **技术栈**：Python / File System Paradigm / Context DB
- **推荐语**："字节跳动 volcengine 的 OpenViking 首次进入本系列日报 Top 12。'文件系统范式取代向量数据库'是今日技术上最有原创性的主张：你管理 Agent 记忆/资源/Skills 就像管理本地文件夹一样直观，L0/L1/L2 分层加载按需取用，检索轨迹可视化。这与今日同框的 karpathy/autoresearch（用 program.md 指挥 Agent）一起，共同代表了'让 Agent 的工作方式更可控、更可解释'的设计趋势。"

---

## 语言分布

| 语言 | 项目数 | 占比 | 代表项目 |
|---|---|---|---|
| Python | 7 | 58% | karpathy/autoresearch / vllm / unsloth / CLI-Anything / ZhuLinsen / free-claude-code / OpenViking |
| Markdown | 3 | 25% | obra/superpowers / multica-ai/andrej-karpathy-skills / msitarzewski/agency-agents |
| C++ | 1 | 8% | ggml-org/llama.cpp |
| TypeScript | 1 | 8% | github/spec-kit |

---

## GitHub Explore 精选

1. **tinyhumansai/openhuman**（23,712 ⭐）— TypeScript — 今日以 599 Stars 之差刚好落出 Top 12（#12 OpenViking 24,311）。**连续第三天追踪**：05-18（15,400）→ 05-20（21,852）→ 05-21（23,712），3天 +8,312 Stars（+54%）！从 05-12（1,676）到今日（23,712），9 天总增速 +1,316%。今日全语言 Trending 中。"Your Personal AI super intelligence. Private, Simple and extremely powerful."

2. **anthropics/claude-plugins-official**（20,816 ⭐）— Python — 今日全语言 + Python 双榜 Day 2，05-20 Explore（20,327）→ 05-21（20,816），+489 Stars（~489/天），"Official, Anthropic-managed directory of high quality Claude Code Plugins." 今日与 obra/superpowers（Skills 方法论）同框，Anthropic 继续以"官方 Skills + 官方 Plugins"双轨并行。

3. **hugohe3/ppt-master**（19,026 ⭐）— Python — 今日 Python Trending 新上，"AI generates natively editable PPTX from any document — real PowerPoint shapes with native animations, not images." 1,787 forks，今日唯一 AI 内容生成工具类项目。核心亮点："not images"——生成的是真实的 PowerPoint shapes + 原生动画，可以直接在 PowerPoint 中二次编辑。这是"AI 内容生成"赛道中一个被长期低估的痛点解法。

4. **Imbad0202/academic-research-skills**（16,278 ⭐）— Python — 今日全语言 + Python 双榜，从 05-18（14,409）持续增长到今日（16,278），3 天 +1,869 Stars（~623/天）。"Academic Research Skills for Claude Code: research → write → review → revise → finalize." 今日与 karpathy/autoresearch（自主 LLM 研究）同框，两者共同代表"AI 加速学术研究"的宏观趋势——一个让 Agent 帮你写论文，另一个让 Agent 帮你做机器学习实验。

5. **rohitg00/ai-engineering-from-scratch**（9,624 ⭐）— Python — 今日全语言 + Python 双榜，"Learn it. Build it. Ship it for others." 1,949 forks（forks/stars = 0.202，开发者实践率高）。今日 rohitg00 同时有 ai-engineering-from-scratch（Explore）+ agentmemory（Explore 候选），说明 rohitg00 是今日 Trending 中活跃度最高的个人开发者账号之一。从零开始学习 AI 工程，是今日微软 ai-agents-for-beginners 不在榜后的"入门学习"方向代表。
