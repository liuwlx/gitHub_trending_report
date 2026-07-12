# GitHub Trending 日报 · 2026-05-27

> 数据来源：GitHub Trending（全语言）+ Python Trending  
> 报告日期：2026-05-27（周二）  
> 上次报告：2026-05-26（间隔 1 天）  
> 输出文件：github_trending_report_2026-05-27.md / .html

---

## 元信息

| 指标 | 数值 |
|---|---|
| Top 12 累计 Stars | ~826k |
| 今日新上榜 | 5（MoneyPrinterTurbo / heretic / twenty / FreeDomain / superpowers）|
| Explore→Top 12 | 1（hardikpandya/stop-slop）|
| 重回 Top 12 | 1（Kronos）|
| 持续上榜 | 5（Understand-Anything / ECC / knowledge-work-plugins / taste-skill / Cybersecurity-Skills）|
| 今日 #1 | harry0703/MoneyPrinterTurbo（60,880，🆕 新入）|
| 今日最大单日增量 | Understand-Anything（+7,236，+22.9%！本系列日报单日增量最高纪录）|
| 本周最大新闻 | andrej-karpathy-skills Day 8 首次退出 Top 12（Day 7 创本系列持续最长纪录）|
| Python Trending 重磅 | anthropics/skills（141,766 ⭐，Anthropic 官方 Agent Skills 公共仓库！）|

---

## 今日 Top 12 一览

| 排名 | 仓库 | Stars | 语言 | 状态 |
|---|---|---|---|---|
| #01 | harry0703/MoneyPrinterTurbo | 60,880 | Python | 今日新上榜 |
| #02 | Lum1104/Understand-Anything | 38,811 | Python | Day 4！**+7,236（+22.9%，本系列单日增量最高纪录）** |
| #03 | hardikpandya/stop-slop | 5,448 | Markdown | Explore→Top 12 首入！+990（+22%）|
| #04 | affaan-m/ECC | 195,636 | Markdown | Day 2（+3,109）|
| #05 | anthropics/knowledge-work-plugins | 17,061 | Markdown | Day 3（+1,468）|
| #06 | Leonxlnx/taste-skill | 23,588 | Markdown | Day 2（**+3,746，+18.9%！**）|
| #07 | p-e-w/heretic | 21,876 | Python | 今日新上榜，"自动消除 LLM 内容限制" |
| #08 | shiyu-coder/Kronos | 26,751 | Python | 重回 Top 12 |
| #09 | mukul975/Anthropic-Cybersecurity-Skills | 10,682 | Markdown | Top 12 Day 2（+1,360，+14.6%）|
| #10 | twentyhq/twenty | 47,153 | TypeScript | 今日新上榜，"Open alternative to Salesforce" |
| #11 | DigitalPlatDev/FreeDomain | 168,578 | JavaScript | 今日新上榜，"Free Domain For Everyone" |
| #12 | obra/superpowers | 209,112 | Markdown | 今日新上榜，**今日 Stars 最高新入，"agentic skills framework"** |

---

## 今日洞察

### 1. ⚡ Understand-Anything Day 4 #2，+7,236（+22.9%！）——本系列日报单日增量最高纪录，4天累计 +16,828（+76.5%！）

增长轨迹：05-24（21,983，#12 末位入榜）→ 05-25（27,153，#1，+5,170）→ 05-26（31,575，#1，+4,422）→ 05-27（38,811，#2，+7,236！）。

今日单日 +7,236 打破本系列日报迄今为止单日增量的最高纪录（上记录是 05-25 的 +5,170）。今日降至 #2（被 MoneyPrinterTurbo #1 超越），但增速反而更快。4天累计 +16,828，涨幅 +76.5%，是本系列追踪史上累计涨幅最快的项目。

今日继续与 Kronos（#8，金融 K 线基础模型）保持"金融×技术 Python 双入"，且再次与代码知识图谱赛道（codegraph 未进 Top 12）形成单点主导态势。

---

### 2. 🏆 obra/superpowers（#12，209,112 ⭐，18,629 forks）——今日 Stars 最高新入，"An agentic skills framework & software development methodology that works"

"A complete software development methodology for your coding agents, built on top of a set of composable skills and some initial instructions."

**7步基本工作流**（mandatory workflows, not suggestions）：
1. **brainstorming** — 激活于写代码之前，通过提问精炼 rough idea，保存设计文档
2. **using-git-worktrees** — 设计批准后，创建隔离工作区 + 干净测试基线
3. **writing-plans** — 拆解为 2-5 分钟的 bite-sized 任务，每个任务有精确文件路径、完整代码、验证步骤
4. **subagent-driven-development / executing-plans** — 每任务派遣独立 subagent + 两阶段审查（spec 合规 → 代码质量）
5. **test-driven-development** — 强制 RED-GREEN-REFACTOR 循环
6. **requesting-code-review** — 按严重性汇报问题，Critical issues 阻断进度
7. **finishing-a-development-branch** — 验证测试 → 选项（merge/PR/keep/discard）→ 清理 worktree

跨 8 平台：Claude Code / Codex CLI / Codex App / Factory Droid / Gemini CLI / OpenCode / Cursor / GitHub Copilot CLI。MIT 开源，5 次发布。

今日与 ECC（#4，196k，技术系统层）和 stop-slop（#3，Explore升，输出质量层）构成"Skills 方法论三角"：superpowers（完整软件开发方法论体系）/ ECC（harness 技术基础设施）/ stop-slop（内容质量控制）。

---

### 3. 🎯 andrej-karpathy-skills Day 8 首次退出 Top 12 + taste-skill Day 2 大涨（+3,746，+18.9%！）——Skills 生态"代际接替"信号

karpathy-skills 以 Day 7 创本系列持续最长纪录后，今日（Day 8）首次退出 Top 12，被 5 个新入项目和多个升入项目替代。

同时，taste-skill Day 2 涨幅 +3,746（+18.9%！），超越 ECC（+3,109）和 Cybersecurity-Skills（+1,360），成为今日涨幅最快的留榜项目。

这两个事件共同指向：Skills 生态的"代际接替"正在发生——
- **karpathy-skills**（行为基础层，单文件 CLAUDE.md）开始被更专业化的 Skills 项目接替
- **taste-skill**（UI/设计品味 Skills）和 **stop-slop**（散文品质 Skills）的快速崛起说明 Skills 细分化正在加速
- **superpowers**（完整方法论 Skills）和 **ECC**（技术系统 Skills）的入榜说明 Skills 生态已从"行为配置"升维到"完整工程体系"

---

### 4. 🔬 anthropics/skills（Python Trending，141,766 ⭐，16,747 forks）——Anthropic 官方 Agent Skills 公共仓库，本周"Skills 浪潮"底层验证

"Skills are folders of instructions, scripts, and resources that Claude loads dynamically to improve performance on specialized tasks."

内容覆盖：Creative & Design / Development & Technical / Enterprise & Communication / Document Skills。每个 skill 均为独立文件夹 + SKILL.md 文件。包含 ./spec（Agent Skills 规范）、./template（Skill 模板）、以及 Claude 文档能力背后的 docx/pdf/pptx/xlsx 技能源码（source-available）。141,766 Stars，16,747 forks。

这是本周"Skills 浪潮"最重要的底层验证：当 karpathy-skills / ECC / gstack / superpowers / taste-skill / stop-slop 在 Trending 轮番上榜时，anthropics/skills（141,766 Stars）告诉我们这不是偶然趋势——Anthropic 官方已将 Skills 架构标准化，建立了 spec + template + 示例的完整生态基础设施。**这是 SKILL.md 格式的"官方钦定"**。

---

## Top 12 详情

### #01 · harry0703/MoneyPrinterTurbo

**今日新上榜 · #1 · 利用AI大模型，一键生成高清短视频 · 60,880 ⭐**

- **仓库**：https://github.com/harry0703/MoneyPrinterTurbo
- **Stars**：60,880 | Forks：8,961 | Releases：10
- **语言**：Python
- **描述**：利用AI大模型，一键生成高清短视频 Generate short videos with one click using AI LLM.
- **核心功能**：
  - AI 自动生成文案 / 自定义文案，支持中英文视频文案
  - 多种高清视频尺寸（竖屏 9:16 1080×1920 / 横屏 16:9 1920×1080）
  - 批量视频生成，多种语音合成（实时试听），字幕生成（字体/位置/颜色/大小/描边）
  - 背景音乐（随机/指定文件），高清无版权视频素材（支持本地素材）
  - MVC 架构，支持 API + Web 界面
- **LLM 支持**：OpenAI / Moonshot / Azure / 通义千问 / Google Gemini / Ollama / DeepSeek / MiniMax / 文心一言 / Pollinations / ModelScope 等 10+ 模型接入
- **编辑点评**：今日 #1，60,880 Stars，8,961 forks。本系列日报首次出现 AI 视频生成工具进入 Top 12。推荐中国用户使用 DeepSeek / Moonshot（无需 VPN，注册即送额度），说明是中国开发者社区重要项目。在今日 Skills/配置类项目仍主导的 Top 12 中，MoneyPrinterTurbo 代表了"AI 应用工具层"的突破——不是 agent 配置，而是直接用 AI 做出产品。

---

### #02 · Lum1104/Understand-Anything

**⚡ Day 4！连续 4 天 Top 12 · +7,236（+22.9%！）· 本系列单日增量最高纪录 · 4天累计 +16,828（+76.5%！）**

- **仓库**：https://github.com/Lum1104/Understand-Anything
- **Stars**：38,811（05-24：21,983 → 05-25：27,153 → 05-26：31,575 → 05-27：38,811）| Forks：3,088
- **语言**：Python
- **4天增长轨迹**：+5,170（+23.5%，05-25）→ +4,422（+16.3%，05-26）→ **+7,236（+22.9%，05-27，本系列单日最高）**
- **编辑点评**：今日 #2（昨日 #1，被 MoneyPrinterTurbo 超越），但单日增量 +7,236 反而创本系列日报最高记录！4天累计 +16,828（+76.5%），是本系列追踪史上 4 天内累计涨幅最大的项目。今日与 codegraph（今日未入 Top 12）的"代码知识图谱双入"格局中断，Understand-Anything 暂时成为该方向的单点主导。

---

### #03 · hardikpandya/stop-slop

**🏅 Explore→Top 12 首入 · +990（+22%！）· Anti-Slop 散文技能**

- **仓库**：https://github.com/hardikpandya/stop-slop
- **Stars**：5,448（昨日 Explore 4,458，+990，+22%！）| Forks：423
- **语言**：Markdown
- **描述**：A skill file for removing AI tells from prose
- **编辑点评**：昨日 Explore #2（+990，+22%！），今日首入 Top 12 #3！今日与 taste-skill（#6，+3,746）构成本系列日报首次"Anti-Slop 双入 Top 12"：stop-slop（散文去 AI 味）+ taste-skill（UI 设计品味）。两者共同指向：AI 生成内容的"去 AI 味"与"品质提升"已经成为 2026 开发者社区的独立需求，是 Skills 生态进入"内容质量优化"阶段的信号。

---

### #04 · affaan-m/ECC

**Day 2 · +3,109（+1.6%）· 195,636 ⭐ · Anthropic Hackathon Winner**

- **仓库**：https://github.com/affaan-m/ECC
- **Stars**：195,636（昨日 192,527，+3,109，+1.6%）| Forks：30,095
- **语言**：Markdown
- **编辑点评**：Day 2，+3,109（+1.6%，增速较首日放缓，符合大型成熟项目模式）。今日在"Skills 方法论三角"中占据"harness 技术基础设施层"位置，与 superpowers（#12，完整方法论）互补：superpowers 告诉 agent "如何做软件开发"，ECC 告诉 harness "如何在技术层面优化"。今日持续 #4，说明开发者在新入项目（MoneyPrinterTurbo/heretic）的冲击下仍保持对 ECC 的关注。

---

### #05 · anthropics/knowledge-work-plugins

**Day 3 · +1,468（+9.4%）· 17,061 ⭐ · Anthropic 官方**

- **仓库**：https://github.com/anthropics/knowledge-work-plugins
- **Stars**：17,061（昨日 15,593，+1,468，+9.4%）| Forks：2,004
- **语言**：Markdown
- **编辑点评**：Day 3，+1,468（+9.4%），持续稳健增速。今日是 Anthropic 第 3 天在 Top 12 保持 knowledge-work-plugins，而 Python Trending 还有 anthropics/skills（141,766 Stars）登场——Anthropic 今日正式实现"知识工作者插件（Top 12）+ 官方 Skills 公共仓库（Python Trending）"的双向布局，共同构筑 Skills 生态的官方基础设施层。

---

### #06 · Leonxlnx/taste-skill

**Day 2 · +3,746（+18.9%！）· 23,588 ⭐ · Anti-Slop 前端 Skills**

- **仓库**：https://github.com/Leonxlnx/taste-skill
- **Stars**：23,588（昨日 19,842，+3,746，+18.9%！）| Forks：1,834
- **语言**：Markdown
- **编辑点评**：Day 2，+3,746（+18.9%！），今日留榜项目涨幅第一（超越 ECC 的 +3,109）。昨日 #12（末位新入）→ 今日 #6（大幅提升）。配合 stop-slop（#3，Explore→Top 12）构成"Anti-Slop 双入"，两者方向互补：taste-skill（UI/视觉品味）+ stop-slop（散文/语言品味）。

---

### #07 · p-e-w/heretic

**今日新上榜 · 21,876 ⭐ · 2,337 forks · Fully automatic censorship removal for language models**

- **仓库**：https://github.com/p-e-w/heretic
- **Stars**：21,876 | Forks：2,337 | Releases：4
- **语言**：Python
- **描述**：Fully automatic censorship removal for language models
- **技术原理**：
  - 基于 directional ablation（"abliteration"，Arditi et al. 2024）+ TPE 参数优化器（Optuna）
  - 联合最小化：refusal 数量 + 原始模型的 KL 散度 → 去审查同时最大保留原始模型智能
  - 完全自动化：无需理解 Transformer 内部机制，命令行即用
  - 支持大多数 dense 模型、多模态模型、多种 MoE 架构、混合模型（Qwen3.5）
  - 社区在 HuggingFace 上已创建 3000+ Heretic 模型
  - 核心创新：灵活的 ablation weight kernel 形状 + 可优化参数 + 非整数 direction_index（线性插值）+ 针对 attention/MLP 分别设置 ablation weights
- **编辑点评**：今日最具争议的新入项目。"Censorship removal"（去审查）触及 AI 安全与开放性之间的核心张力。21,876 Stars，2,337 forks，4 次发布，说明这是一个技术上相当成熟的工具。在今日 anthropics/skills（官方 Skills）+ 微软 agent-governance-toolkit（Python Trending，OWASP Agentic Top 10）+ ECC AgentShield（#4）的安全合规背景下，heretic 的 Trending 地位形成了"安全合规 vs. 开放自由"的鲜明对比——这是 AI 生态 2026 年最重要的二元张力之一。

---

### #08 · shiyu-coder/Kronos

**重回 Top 12 · 26,751 ⭐ · AAAI 2026 · 金融 K 线基础模型**

- **仓库**：https://github.com/shiyu-coder/Kronos
- **Stars**：26,751（昨日 26,041，+710，+2.7%）| Forks：4,638
- **语言**：Python
- **描述**：Kronos: A Foundation Model for the Language of Financial Markets
- **编辑点评**：继 05-25（#10）→ 05-26（#14，退出）→ 05-27（#8，重回）的第二次 Top 12 往返。今日 +710（+2.7%），增速平缓但保持活跃。在今日 Python 项目中（MoneyPrinterTurbo/#1 + Understand-Anything/#2 + heretic/#7 + Kronos/#8），Kronos 是唯一金融 AI 方向，说明"量化/金融 AI 基础模型"需求持续稳定。与 Python Trending 的 OpenBB、freqtrade 共同构成金融 AI 三角。

---

### #09 · mukul975/Anthropic-Cybersecurity-Skills

**Top 12 Day 2 · +1,360（+14.6%）· 10,682 ⭐ · 754 cybersecurity skills**

- **仓库**：https://github.com/mukul975/Anthropic-Cybersecurity-Skills
- **Stars**：10,682（昨日 9,322，+1,360，+14.6%！）| Forks：1,237
- **语言**：Markdown
- **编辑点评**：Top 12 Day 2，+1,360（+14.6%！）持续高增速。今日在"Skills 六连"（昨日六连后，今日 Skills 类项目仍有：stop-slop/#3 + ECC/#4 + knowledge-work-plugins/#5 + taste-skill/#6 + Cybersecurity-Skills/#9 + superpowers/#12）= 6 项。Skills 方向今日再次达到 6 项同日上榜，维持历史浓度记录。今日与 heretic（#7，Python Trending）+ microsoft/agent-governance-toolkit（Python Trending）共同构成"agent 安全三角"。

---

### #10 · twentyhq/twenty

**今日新上榜 · 47,153 ⭐ · "The open alternative to Salesforce, designed for AI"**

- **仓库**：https://github.com/twentyhq/twenty
- **Stars**：47,153 | Forks：6,699
- **语言**：TypeScript
- **描述**：The open alternative to Salesforce, designed for AI.
- **编辑点评**：今日新入 #10，47,153 Stars，6,699 forks。"Designed for AI"定位非常精准——在 agent 生态成熟的今天，CRM 系统需要原生 AI 集成（agent 可以操作 CRM 数据、自动化销售流程）。open-source + AI-native CRM 这个定位在 2026 年极具竞争力。今日是本系列第一次出现 CRM/SaaS 替代类项目进入 Top 12。

---

### #11 · DigitalPlatDev/FreeDomain

**今日新上榜 · 168,578 ⭐ · 3,156 forks · "Free Domain For Everyone"**

- **仓库**：https://github.com/DigitalPlatDev/FreeDomain
- **Stars**：168,578 | Forks：3,156
- **描述**：DigitalPlat FreeDomain: Free Domain For Everyone
- **编辑点评**：今日新入 #11，168,578 Stars，3,156 forks——是今日 Top 12 中第二高 Stars 项目（仅次于 superpowers 的 209k）。高 Stars + 低 forks 比（3,156/168,578 ≈ 1.9%）说明这是一个"资源型"项目，用户主要是"用"而非"fork 改"。在 agent 生态中，"免费域名"为 agent 应用部署提供了基础设施支持。今日 Top 12 累计 Stars ~826k 大幅高于昨日 ~597k，主要贡献来自 FreeDomain（169k）+ superpowers（209k）两个高 Stars 历史项目新入。

---

### #12 · obra/superpowers

**今日新上榜 · 209,112 ⭐！今日 Stars 最高新入 · "An agentic skills framework & software development methodology that works"**

- **仓库**：https://github.com/obra/superpowers
- **Stars**：209,112 | Forks：18,629 | Releases：5
- **语言**：Markdown
- **描述**：An agentic skills framework & software development methodology that works.
- **核心理念**："A complete software development methodology for your coding agents, built on top of a set of composable skills." "Mandatory workflows, not suggestions."
- **7步完整工作流**：brainstorming → using-git-worktrees → writing-plans → subagent-driven-development / executing-plans → test-driven-development（RED-GREEN-REFACTOR）→ requesting-code-review → finishing-a-development-branch
- **Skills Library**（部分）：test-driven-development / systematic-debugging / verification-before-completion / brainstorming / writing-plans / executing-plans / dispatching-parallel-agents / requesting-code-review / receiving-code-review / using-git-worktrees / finishing-a-development-branch / subagent-driven-development / writing-skills / using-superpowers
- **跨平台支持**（8个）：Claude Code / Codex CLI / Codex App / Factory Droid / Gemini CLI / OpenCode / Cursor / GitHub Copilot CLI
- **编辑点评**：今日 Stars 最高新入（209,112），是本系列日报迄今为止进入 Top 12 的第三高 Stars 项目（仅次于 ECC 192k 新入时，和 andrej-karpathy-skills 历史峰值 155k）。"Mandatory workflows, not suggestions"——这句话是与 karpathy-skills 等建议式 Skills 的最大差别。superpowers 的哲学是：agent 不应该"可选地"遵循最佳实践，而是必须遵循一套完整的软件开发方法论。在今日"Skills 方法论三角"（superpowers/完整方法论 + ECC/harness 技术系统 + stop-slop/输出质量）中，superpowers 代表了"工程流程"的最高权威。

---

## 语言分布

| 语言 | 项目数 | 占比 | 项目 |
|---|---|---|---|
| Markdown | 6 | 50% | stop-slop / ECC / knowledge-work-plugins / taste-skill / Cybersecurity-Skills / superpowers |
| Python | 4 | 33% | MoneyPrinterTurbo / Understand-Anything / heretic / Kronos |
| TypeScript | 1 | 8% | twentyhq/twenty |
| JavaScript | 1 | 8% | DigitalPlatDev/FreeDomain |

今日 Markdown 达到 50%（连续第 2 天超越 Python，且从昨日 42% 提升至 50%）。6 个 Markdown 项目全部是 Skills/配置/插件/方法论类项目：
- stop-slop（散文品质 Skills）+ ECC（harness 技术系统）+ knowledge-work-plugins（知识工作者插件）+ taste-skill（UI 设计品味 Skills）+ Cybersecurity-Skills（安全专域 Skills）+ superpowers（完整方法论 Skills）

**Markdown-as-infrastructure 趋势今日达到新高：SKILL.md 格式正在成为 agent 行为编程的标准语言。**

---

## GitHub Explore 精选

### Explore #1 · anthropics/skills（Python Trending）

- **Stars**：141,766 | Forks：16,747
- **描述**：Public repository for Agent Skills
- **内容结构**：
  - `./skills`：Creative & Design / Development & Technical / Enterprise & Communication / Document Skills
  - `./spec`：Agent Skills 规范文档
  - `./template`：Skill 模板
  - source-available 技能：docx / pdf / pptx / xlsx（Claude 文档能力背后的技能源码）
- **定位**："Skills are folders of instructions, scripts, and resources that Claude loads dynamically to improve performance on specialized tasks. Each skill is self-contained in its own folder with a SKILL.md file."
- **分析**：141,766 Stars，今日 Python Trending 首位。这是本周"Skills 浪潮"最重要的底层验证：Anthropic 官方已将 SKILL.md 格式标准化，建立 spec + template + 示例的完整生态。当本周 karpathy-skills / ECC / gstack / superpowers / taste-skill / stop-slop 在 Trending 轮番上榜，anthropics/skills 是整个现象的"根基"——这些项目都在使用或参考 Anthropic 定义的 SKILL.md 格式。这是"SKILL.md 官方钦定"时刻。

### Explore #2 · unclecode/crawl4ai（Python Trending）

- **Stars**：66,549 | Forks：6,822
- **描述**：🚀🤖 Crawl4AI: Open-source LLM Friendly Web Crawler & Scraper
- **分析**：66,549 Stars，Python Trending 高位。在 AI agent 生态中，crawl4ai 是"信息摄取层"的核心工具——agent 需要从 web 获取数据，crawl4ai 专门针对 LLM 消费场景优化（clean output, markdown format, structured extraction）。在今日 anthropics/skills（官方 Skills）+ 各类 agent 工具的 Trending 背景下，crawl4ai 代表了 agent 生态中"数据层"的成熟。今日与昨日 sansan0/TrendRadar（MCP + AI 聚合监控）共同构成"agent 信息摄取方向"的连续上榜信号。

### Explore #3 · vllm-project/vllm（Python Trending）

- **Stars**：81,157 | Forks：17,306
- **描述**：A high-throughput and memory-efficient inference and serving engine for LLMs
- **分析**：81,157 Stars，17,306 forks（极高 fork 率）。今日 Python Trending，vllm 代表了"本地 LLM 推理基础设施"——在 ECC/superpowers 等工具使 agent 能力极大提升的同时，vllm 是这些 agent 背后的推理引擎层。今日 vllm + anthropics/skills（官方 Skills）+ heretic（#7，去审查工具）共同构成 2026 LLM 部署生态的"基础设施 + 配置 + 自由化"三角。

### Explore #4 · dograh-hq/dograh（Python Trending）

- **Stars**：3,368 | Forks：717
- **描述**：Open source voice AI platform. Self-hosted alternative to Vapi and Retell. On Prem, BYOK across Speech to Speech or LLM/STT/TTS, with a visual workflow builder, MCP native and telephony support.
- **分析**：今日 Python Trending 新入，3,368 Stars。"Open source, self-hosted alternative to Vapi and Retell" + MCP native + BYOK（Bring Your Own Key） + 电话支持——Voice AI agent 的完整基础设施。在 cmux（macOS terminal for AI agents）退出 Top 12 后，dograh 代表了 AI agent 生态的另一个基础设施方向：**语音 AI 层**。MCP native 的定位意味着可以直接集成进 Claude Code 等 agent 工作流。

### Explore #5 · moeru-ai/airi（全语言 Trending #16）

- **Stars**：40,083 | Forks：4,042
- **描述**：💖🧸 Self hosted, you-owned AI companion — realtime voice chat, Minecraft/Factorio playing. Web/macOS/Windows.
- **分析**：今日全语言 Trending #16，昨日 Explore。40,083 Stars，4,042 forks，TypeScript。在 AI coding agent 工具主导的 Trending 中，airi 代表了 AI 技术向 consumer/entertainment 应用的持续拓展。"Neuro-sama's altitude"目标——与 dograh（语音 AI 基础设施）在技术层面互补：dograh 是 B2B 语音 AI 基础设施，airi 是 consumer-facing 语音 AI 应用。

---

## 今日 vs 昨日（05-26）对比

### 留榜项目（1天增量）

| 项目 | 05-26 Stars（排名）| 05-27 Stars（排名）| +1天 |
|---|---|---|---|
| Lum1104/Understand-Anything | 31,575（#1）| 38,811 | **+7,236（+22.9%！最高纪录）** |
| anthropics/knowledge-work-plugins | 15,593（#2）| 17,061 | +1,468（+9.4%）|
| affaan-m/ECC | 192,527（#4）| 195,636 | +3,109（+1.6%）|
| mukul975/Anthropic-Cybersecurity-Skills | 9,322（#5）| 10,682 | +1,360（+14.6%）|
| Leonxlnx/taste-skill | 19,842（#12）| 23,588 | **+3,746（+18.9%！留榜涨幅第一）** |

### Explore→Top 12

| 项目 | 05-26 Explore Stars | 05-27 Top 12 Stars | 升入 |
|---|---|---|---|
| hardikpandya/stop-slop | 4,458（Explore #2）| 5,448（Top 12 #3）| +990（+22%！）|
| shiyu-coder/Kronos | 26,041（#14）| 26,751（Top 12 #8）| +710（+2.7%，重回）|

### 今日退出（05-26 Top 12 → 05-27 未入）

multica-ai/andrej-karpathy-skills（#8，155,178，**Day 8 退出，本系列持续最长 Day 7 纪录终结**）、rohitg00（#3，Python-only）、codegraph（#6）、cmux（#7）、FinceptTerminal（#9）、paperless-ngx（#10）、claude-cookbooks（#11）

---

*报告生成：2026-05-27 · 数据来源：https://github.com/trending + https://github.com/trending/python?since=daily*
