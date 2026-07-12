# GitHub Trending 日报 · 2026-05-20

## Meta
- **日期**：2026-05-20
- **数据来源**：GitHub Trending（全语言）+ Python Trending
- **今日 Top 12**：12 个项目 | 累计 Stars：~924k | 编程语言：4 | 今日新上榜：8 | 持续上榜 Day 2：4

---

## 今日洞察

### 🌌 "Skills 宇宙"爆炸日——Top 4 全部是 Skills/Agent Methodology 仓库，合计 577k Stars，创本系列日报单日 Skills 记录

今日最令人震撼的 Trending 格局：前四名全部是关于如何让 AI coding agent 更好工作的"Skills / Methodology"仓库，合计 577k Stars：obra/superpowers（198.7k）+ multica-ai/andrej-karpathy-skills（138.7k）+ anthropics/skills（137.7k）+ msitarzewski/agency-agents（101.9k）。这是本系列日报（05-06 至今）中从未出现过的"Skills 四强同框"格局。背后的逻辑：随着 Claude Code / Codex / Cursor 等 AI coding agent 的日活用户在过去两周快速增长（本系列日报持续追踪其 Skills 生态），今日"如何让你的 agent 更聪明更专业"成了整个开发者社区的最大公约数话题——Skills 仓库不再是小众工具，而是每个 AI 开发者的必备基础设施。

### 👑 obra/superpowers（198,743 ⭐）——本系列日报 Stars 新高，Agent Skills 领域"方法论级"作品今日登顶

obra/superpowers 今日以 198,743 Stars 登顶，超越本系列日报迄今最高记录（05-12 SD-webui 162.9k），是本日报系列追踪以来首次突破 198k 的项目。其定位极具野心："Superpowers is a complete software development methodology for your coding agents, built on top of a set of composable skills."——这不是又一个 Skills 集合，而是一套"完整的软件开发方法论"，通过可组合 Skills + 初始指令的方式告诉 agent 如何使用它们。支持 Claude Code / Codex CLI / Codex App / Factory Droid / Gemini CLI / OpenCode / Cursor / GitHub Copilot CLI 8 大 agent 平台。作者 obra（Jesse Vincent）是知名开源贡献者，这个仓库将 Skills 从"工具"升维到了"方法论"层次。

### ⚡ rtk-ai/rtk（51.1k，Rust）——"Claude Code 运行一次 token 消耗降低 60-90%"，今日最务实的 Agent 基础设施

今日第七位 rtk-ai/rtk（51,127 ⭐，3,116 forks）是今日唯一 Rust 语言项目，也是技术最务实的一个："CLI proxy that reduces LLM token consumption by 60-90% on common dev commands. Single Rust binary, zero dependencies."——代理拦截 git/find/grep 等常用 CLI 命令的输出，通过四大策略（Smart Filtering / Grouping / Truncation / Deduplication）将 git status 的 token 消耗从 ~2,000 降至 ~200（减少 90%）。169 次发布，极其活跃。在 AI coding agent 使用成本快速攀升的今天（Claude API 按 token 计费），"不改代码，每次 LLM 调用省 60-90% token"是高度务实的工程需求，直接命中痛点。

### 🔄 四项目持续两日（05-18→05-20）——microsoft/ai-agents-for-beginners、HKUDS/CLI-Anything、ZhuLinsen、K-Dense-AI/scientific-agent-skills 今日全部 Day 2

今日 4 个项目连续两日上榜（05-18 起 Day 2）：microsoft/ai-agents-for-beginners（63,072→64,546，+1,474），HKUDS/CLI-Anything（36,258→37,889，+1,631），ZhuLinsen/daily_stock_analysis（36,748→37,897，+1,149），K-Dense-AI/scientific-agent-skills（24,130→24,818，+688）。其中 HKUDS/CLI-Anything 日增 +1,631 Stars 是今日持续项目中增速最快的，说明"让所有软件 Agent-Native"的产品方向得到持续认可；ZhuLinsen 两日合计 +1,149 Stars 且今日 Fork/Star = 36,606/37,897 = 0.966 依然异常高位（"必须 fork 才能用"的自部署工具特征持续）。

---

## 今日热门 Top 12（按总 Stars 排序）

### #01 obra/superpowers ⭐ 198,743 [新上榜]
- **仓库**：https://github.com/obra/superpowers
- **语言**：Markdown | **License**：MIT | **Forks**：17,731
- **描述**：An agentic skills framework & software development methodology that works. 198,743 ⭐ + 17,731 forks，今日 Top 1，本系列日报 Stars 新高（超越 05-12 SD-webui 162.9k），作者 Jesse Vincent（obra）。
- **核心特性**：
  - "Complete software development methodology for your coding agents"——不只是 Skills 集合，是完整的开发方法论
  - 可组合 Skills（Composable Skills）+ 初始指令体系
  - 支持 8 大 agent 平台：Claude Code / Codex CLI / Codex App / Factory Droid / Gemini CLI / OpenCode / Cursor / GitHub Copilot CLI
  - 5 次发布，Jesse Vincent（知名开源贡献者）出品
  - 关注"让 agent 真正知道如何使用 Skills"而不只是堆砌 Skills 列表
- **技术栈**：Markdown / SKILL.md / Agent Methodology
- **推荐语**："198.7k Stars，本系列日报最高 Stars 新高！obra/superpowers 的价值在于'方法论'层次的提升——它不是教你用哪些 Skills，而是提供一套完整的'如何让 agent 有效使用 Skills 的思维框架'。今日以 198.7k 领衔，加上其他三个 Skills 仓库同框，说明 2026 年 Agent Skills 已从'早期尝鲜者的实验'变成'每个 AI 开发者的标配基础设施'。"

---

### #02 multica-ai/andrej-karpathy-skills ⭐ 138,654 [新上榜]
- **仓库**：https://github.com/multica-ai/andrej-karpathy-skills
- **语言**：Markdown | **License**：MIT | **Forks**：14,221
- **描述**：A single CLAUDE.md file to improve Claude Code behavior, derived from Andrej Karpathy's observations on LLM coding pitfalls. 138,654 ⭐ + 14,221 forks，"一个 CLAUDE.md 文件改变你的 Claude Code 体验"，Karpathy 洞见提炼。
- **核心特性**：
  - 核心形式：单一 CLAUDE.md 文件（极简，无依赖）
  - 内容来源：Andrej Karpathy 对 LLM 编码常见陷阱的系统性观察总结
  - 覆盖：Claude Code 行为优化，避免 LLM 常见编码错误模式
  - 极低安装门槛：拷贝一个文件即可使用
  - 14.2k forks 说明大量开发者直接 fork 并个性化修改
- **技术栈**：Markdown / CLAUDE.md
- **推荐语**："'Karpathy 说过的 LLM 编码坑，我帮你整合成一个 CLAUDE.md。'这种'名人观察→可操作配置文件'的转化方式极其高效，138.7k Stars 证明了开发者对'一行命令改善 Claude Code 质量'的强烈需求。今日与 obra/superpowers（完整方法论）形成有趣对比：一个是'最小可行 Skills 配置'，一个是'完整 Agent 开发方法论'。"

---

### #03 anthropics/skills ⭐ 137,743 [重返（05-11 后 9 天）]
- **仓库**：https://github.com/anthropics/skills
- **语言**：Python | **License**：MIT | **Forks**：16,247
- **描述**：Public repository for Agent Skills. 137,743 ⭐ + 16,247 forks，Anthropic 官方 Agent Skills 仓库，05-11（131,900）首次上榜，今日重返（+5,843 Stars，9 天 ~649/天持续增长）。
- **今日动态**：9 天后重返 Top 12（05-11: 131,900 → 05-20: 137,743，+5,843 Stars），今日与 obra/superpowers + multica-ai/andrej-karpathy-skills + msitarzewski/agency-agents 共同形成"Skills 四强同框"。Anthropic 官方仓库持续获得社区认可，9 天 ~649/天的增速说明 Anthropic 的 Agent Skills 定义持续影响整个生态的 Skills 格式标准。
- **推荐语**："Anthropic 官方 Skills 仓库今日重返，9 天内持续稳定增长 +5.8k Stars（~649/天）。今日在 Skills 四强中代表'平台规范层'：Anthropic 作为 Claude Code 背后的公司，其 Skills 定义事实上成为行业参考标准。与上周（05-18）huggingface/skills 上榜不同，今日 anthropics/skills 与三个'应用层 Skills'（obra / karpathy / agency-agents）同框，印证了'规范层领跑→应用层跟进'的 Skills 生态发展路径。"

---

### #04 msitarzewski/agency-agents ⭐ 101,886 [新上榜]
- **仓库**：https://github.com/msitarzewski/agency-agents
- **语言**：Markdown | **License**：MIT | **Forks**：16,837
- **描述**：A complete AI agency at your fingertips - From frontend wizards to Reddit community ninjas, from whimsy injectors to reality checkers. Each agent is a specialized expert with personality, processes, and proven deliverables. 101,886 ⭐。
- **核心特性**：
  - 完整 AI 虚拟公司：包含工程 / 设计 / 营销 / 销售 / 产品 / 项目管理 / 测试 / 支持 / 空间计算 / 游戏开发 / 学术 / 金融 等多个部门
  - 每个 Agent 都有专属个性、专业知识和可交付成果（非通用 Prompt 模板）
  - "Born from a Reddit thread and months of iteration"——社区驱动，真实打磨
  - 支持 Claude Code（推荐）/ GitHub Copilot / Antigravity / Gemini CLI / OpenCode / OpenClaw / Cursor / Aider / Windsurf / Kimi Code
  - 交付物明确：Real code, processes, and measurable outcomes
- **技术栈**：Markdown / SKILL.md / Agent Personas
- **推荐语**："Reddit 起源 + 个性化 Agent 角色扮演的组合爆炸了！101.9k Stars，16.8k forks（forks/stars = 0.165，开发者二次创作率高）。agency-agents 的精髓是'你的 AI agent 不只是工具，它应该有专业领域、工作风格和可预期的交付物'——这与 obra/superpowers 的'方法论视角'和 multica-ai 的'最小配置视角'形成了今日 Skills 三种哲学的完整呈现。"

---

### #05 unslothai/unsloth ⭐ 64,749 [新上榜]
- **仓库**：https://github.com/unslothai/unsloth
- **语言**：Python | **License**：Apache-2.0 | **Forks**：5,728
- **描述**：Unsloth Studio is a web UI for training and running open models like Gemma 4, Qwen3.6, DeepSeek, gpt-oss locally. 64,749 ⭐ + 5,728 forks，今日唯一"模型训练/微调"方向项目，AI 基础设施层代表。
- **核心特性**：
  - 本地模型训练 Web UI：Gemma 4 / Qwen3.6 / DeepSeek / gpt-oss 等主流开源模型
  - 无需云端，完全本地运行
  - 极大降低模型微调门槛：Web UI 取代命令行配置
  - 高效显存利用：以更少 GPU 内存实现同等微调效果
- **技术栈**：Python / PyTorch / CUDA / Triton
- **推荐语**："今日唯一'模型训练'方向项目。在前四个 Skills 仓库之后，unsloth 代表了'如果你想训练自己的 Agent 专用模型'的需求层——Skills 让现有模型更聪明，unsloth 让你可以自己训练新模型。两种路径今日并存，完整覆盖 Agent 能力提升的两大方向。"

---

### #06 microsoft/ai-agents-for-beginners ⭐ 64,546 [Day 2]
- **仓库**：https://github.com/microsoft/ai-agents-for-beginners
- **语言**：Jupyter Notebook | **License**：MIT | **Forks**：21,339
- **描述**：12 Lessons to Get Started Building AI Agents. 64,546 ⭐（05-18: 63,072，+1,474），Day 2 持续上榜。微软官方 AI Agent 课程，21k+ forks。
- **今日动态**：05-18（63,072）→ 05-20（64,546），+1,474 Stars（Day 2，~737/天）。今日与 unslothai/unsloth 同框，两者共同构成"学习 AI Agent + 训练本地模型"的完整入门路径：先学会构建 Agent（microsoft），再学会训练专属模型（unsloth）。
- **推荐语**："Day 2 稳步增长，每日 +737 Stars 说明微软官方课程的持续曝光。今日在 Skills 四强主导的格局中，microsoft 代表了'从零开始学习'的那部分开发者群体——Skills 生态的壮大也在同步带动 Agent 学习资源的需求。"

---

### #07 rtk-ai/rtk ⭐ 51,127 [新上榜]
- **仓库**：https://github.com/rtk-ai/rtk
- **语言**：Rust | **License**：MIT | **Forks**：3,116
- **描述**：CLI proxy that reduces LLM token consumption by 60-90% on common dev commands. Single Rust binary, zero dependencies. 51,127 ⭐ + 3,116 forks，169 次发布，今日唯一 Rust 项目。
- **核心特性**：
  - CLI 代理拦截器：在 agent 和 shell 之间插入一个 Rust 代理层
  - 四大降 token 策略：Smart Filtering（去噪）/ Grouping（聚合同类）/ Truncation（保留关键）/ Deduplication（折叠重复）
  - 效果：git status ~2,000 tokens → ~200 tokens（-90%）
  - 支持 Claude Code / Copilot / Gemini CLI / Codex / Cursor / Windsurf / Cline / Kilo Code / Antigravity / Hermes
  - Auto-Rewrite Hook：自动把 `git status` 重写为 `rtk git status`，无需修改代码
  - Single Rust binary，零依赖，169 次发布极其活跃
- **技术栈**：Rust
- **推荐语**："今日最务实、最能直接省钱的工具！在 Claude API 按 token 计费的背景下，'不改代码、每次 LLM 调用省 60-90% token'是极高价值的工程贡献。169 次发布 + 51.1k Stars 说明这不是噱头——Rust 单二进制，开箱即用，是今日 Top 12 中最符合'工程师气质'的项目。今日与 Skills 四强同框，两个方向完美互补：Skills 让 agent 更聪明，rtk 让 agent 更省钱。"

---

### #08 ZhuLinsen/daily_stock_analysis ⭐ 37,897 [Day 2]
- **仓库**：https://github.com/ZhuLinsen/daily_stock_analysis
- **语言**：Python | **License**：MIT | **Forks**：36,606
- **描述**：LLM驱动的 A/H/美股智能分析：多数据源行情 + 实时新闻 + LLM决策仪表盘 + 多渠道推送，零成本定时运行，纯白嫖。37,897 ⭐ + 36,606 forks，Fork/Star = 0.966。
- **今日动态**：05-18（36,748）→ 05-20（37,897），+1,149 Stars（Day 2，~575/天）。Fork/Star = 36,606/37,897 = 0.966，比 05-18（0.981）略有下降，但依然是今日全榜最高 Fork/Star 比率，"自部署 + 必须 fork"的特征持续稳定。
- **推荐语**："连续第 2 天上榜，Fork/Star = 0.966 依然保持今日全榜最高 Fork/Star。金融 AI 自动化的长尾效应持续——每天约 575 新用户 fork 用于自部署，说明'零成本 LLM 金融分析'的需求不是一过性热度，而是刚性需求。"

---

### #09 HKUDS/CLI-Anything ⭐ 37,889 [Day 2]
- **仓库**：https://github.com/HKUDS/CLI-Anything
- **语言**：Python | **License**：Apache-2.0 | **Forks**：3,623
- **描述**："CLI-Anything: Making ALL Software Agent-Native" — 7 阶段 Pipeline 将任意 GUI 软件生成 AI agent 可调用的 CLI 接口。37,889 ⭐（05-18: 36,258，+1,631）。
- **今日动态**：05-18（36,258）→ 05-20（37,889），+1,631 Stars（Day 2，~816/天），是今日持续项目中增速最快的，说明"让所有软件 Agent-Native"的产品方向持续获得认可。今日与 obra/superpowers（Agent 方法论）共同构成 Agent 生态的"方法论层 + 工具接口层"。
- **推荐语**："Day 2 日增 +816 Stars，持续项目中增速最快。HKUDS 的 CLI-Anything 在今日 Skills 四强主导的格局中代表了'让 agent 能调用任何工具'的接口层——Skills 告诉 agent 该做什么，CLI-Anything 告诉 agent 该怎么操作任何软件，两者今日完美互补。"

---

### #10 frappe/erpnext ⭐ 34,354 [新上榜]
- **仓库**：https://github.com/frappe/erpnext
- **语言**：Python | **License**：GPL-3.0 | **Forks**：11,316
- **描述**：Free and Open Source Enterprise Resource Planning (ERP). 34,354 ⭐ + 11,316 forks，今日唯一"传统企业软件"方向项目，也是今日语言技术栈最成熟、架构最完整的项目。
- **核心特性**：
  - 完整开源 ERP 系统：会计 / 人力资源 / 库存 / 制造 / 项目管理 / 销售 / 采购
  - 基于 Frappe Framework（Python + MariaDB）
  - 社区版免费，企业级云服务付费
  - 活跃的全球社区（主要来自印度、东南亚等新兴市场）
  - 11.3k forks，是今日非 Skills 类仓库中 forks 最多的
- **技术栈**：Python / JavaScript / MariaDB / Redis / Frappe
- **推荐语**："今日唯一传统企业软件项目，在 Skills 四强主导的 Trending 中显得格外另类——但恰恰说明了开源 ERP 的持续刚需。frappe/erpnext 的上榜可能与 AI 趋势无直接关系，更可能是被推荐算法或某次大型社区活动带动。34.4k Stars + 11.3k forks 代表了一个真实的、数十万企业用户支撑的稳定开源项目。"

---

### #11 Alishahryar1/free-claude-code ⭐ 26,465 [新上榜]
- **仓库**：https://github.com/Alishahryar1/free-claude-code
- **语言**：Python | **License**：MIT | **Forks**：3,946
- **描述**：Use claude-code for free in the terminal, VSCode extension or discord like OpenClaw (voice supported). 26,465 ⭐ + 3,946 forks，今日"免费用 Claude Code"方向代表。
- **核心特性**：
  - 让用户免费使用 Claude Code（终端 / VSCode 扩展 / Discord）
  - 语音支持（voice supported）
  - 类 OpenClaw 体验
  - Python 实现，跨平台
- **推荐语**："'免费 Claude Code'的强烈刚需——在 Claude Code 订阅费用持续上涨的背景下，这类工具自然获得大量关注。26.5k Stars + 3.9k forks（forks/stars = 0.149），说明大量开发者选择自部署。今日与 rtk-ai/rtk（降低 token 消耗）同框，两者代表了'降低 AI 开发成本'的两种路径：rtk 减少 token 消耗，free-claude-code 直接绕过付费。"

---

### #12 K-Dense-AI/scientific-agent-skills ⭐ 24,818 [Day 2]
- **仓库**：https://github.com/K-Dense-AI/scientific-agent-skills
- **语言**：Python | **License**：MIT | **Forks**：2,606
- **描述**：A set of ready to use Agent Skills for research, science, engineering, analysis, finance and writing. 24,818 ⭐（05-18: 24,130，+688）。135 个科研 Skills，76 次发布。
- **今日动态**：05-18（24,130）→ 05-20（24,818），+688 Stars（Day 2，~344/天）。今日与 Skills 四强同框，是今日"垂直 Skills"的代表（科研/医药领域）VS Skills 四强的"通用方法论 Skills"——两者共同说明 Skills 生态在"深度（科研垂直）"和"广度（通用方法论）"两个维度同步扩张。
- **推荐语**："Day 2 稳步增长。今日在 Skills 四强（obra / multica-ai / anthropics / agency-agents）中，scientific-agent-skills 代表了 Skills 向'专业科研领域'的深度延伸。两种 Skills 扩张方向今日同框：广度（通用方法论型）+ 深度（科研垂直型），Skills 生态正在从'一刀切'向'分层专业化'进化。"

---

## 语言分布

| 语言 | 项目数 | 占比 | 代表项目 |
|---|---|---|---|
| Python | 7 | 58% | anthropics/skills / unsloth / ZhuLinsen / CLI-Anything / erpnext / free-claude-code / K-Dense-AI |
| Markdown | 3 | 25% | obra/superpowers / multica-ai/andrej-karpathy-skills / msitarzewski/agency-agents |
| Jupyter Notebook | 1 | 8% | microsoft/ai-agents-for-beginners |
| Rust | 1 | 8% | rtk-ai/rtk |

---

## GitHub Explore 精选

1. **tinyhumansai/openhuman**（21,852 ⭐）— TypeScript — 今日全语言 Trending，从 05-18（15,400）到今日（21,852），2 天 +6,452 Stars（+42%，约 3,226/天），增速依然惊人！05-12 时仅 1,676 Stars，今日已接近 22k，8 天总增速 +1,203%。上今日全语言 Trending 但因 Stars 总量（21,852）低于 K-Dense-AI/scientific-agent-skills（24,818）落出 Top 12。定位："Your Personal AI super intelligence. Private, Simple and extremely powerful."

2. **anthropics/claude-plugins-official**（20,327 ⭐）— Python — 今日全语言 + Python 双榜，"Official, Anthropic-managed directory of high quality Claude Code Plugins." 2,513 forks。Anthropic 官方插件目录，今日与 anthropics/skills（#03，137.7k）同框，Anthropic 今日以"官方 Skills + 官方 Plugins"双重身份出现在 Trending，标志着 Anthropic 正在从"模型公司"向"AI coding 生态平台"全面转型。

3. **humanlayer/12-factor-agents**（21,265 ⭐）— TypeScript — 今日全语言 Trending，05-18（20,204）→ 05-20（21,265），+1,061 Stars（~530/天）。以 797 Stars 之差刚好落出 Top 12（#12 K-Dense-AI 24,818）。今日在 Skills 四强主导的格局中，12-factor-agents 代表了"Agent 生产化工程原则"的视角——与 obra/superpowers（方法论）互补，两者今日一同出现在 Trending 中，共同构成"Agent 工程化"的完整讨论。

4. **HKUDS/ViMax**（5,575 ⭐）— Python — 今日全语言 + Python 双榜，"ViMax: Agentic Video Generation (Director, Screenwriter, Producer, and Video Generator All-in-One)." 935 forks，HKUDS（AI-Trader / CLI-Anything 同组织，港大）第三个上 Trending 的产品！今日 HKUDS 同时有 CLI-Anything（#09，Day 2）+ ViMax（Explore），揭示港大 HKUDS 实验室完整的多模态 Agent 布局：CLI（代码 Agent 工具接口）+ ViMax（视频生成 Agent）+ AI-Trader（金融 Agent）。

5. **Alishahryar1/free-claude-code** 已在 Top 12 #11 收录——今日 Python Trending 另一精选：**alirezarezvani/claude-skills**（15,555 ⭐），"313+ Claude Code skills & agent skills & plugins for Claude Code, Codex, Gemini CLI, Cursor, and 8 more coding agents." 2,123 forks，今日 Python Trending，这是今日 Trending 中第 5 个 Skills 仓库（除 Top 12 内的 4 个）！今日 Skills 类仓库加 Explore 合计出现 6+ 个不同 Skills 仓库，印证了本报告"Skills 宇宙爆炸日"的主题判断。
