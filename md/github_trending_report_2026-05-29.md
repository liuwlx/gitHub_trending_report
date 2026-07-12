# GitHub Trending 日报 · 2026-05-29

> 数据来源：GitHub Trending（全语言）+ Python Trending  
> 报告日期：2026-05-29（周四）  
> 上次报告：2026-05-27（间隔 **2 天**）  
> 输出文件：github_trending_report_2026-05-29.md / .html

---

## 元信息

| 指标 | 数值 |
|---|---|
| Top 12 累计 Stars | ~576k |
| 今日新上榜 | 8（markitdown / compound-engineering-plugin / claude-code / cursor/plugins / liteparse / stable-worldmodel / Biohub-esm / project-nomad）|
| 升入 Top 12 | 1（byoungd/English-level-up-tips，#13→#10）|
| 持续上榜 | 3（MoneyPrinterTurbo Day 3 / taste-skill Day 4 / twenty Day 3）|
| 今日 #1 | harry0703/MoneyPrinterTurbo（68,859，Day 3）|
| 2天最大增量 | MoneyPrinterTurbo（+7,979，+13.1%）|
| 本系列 Trending 最高 Stars | codecrafters-io/build-your-own-x（507,071，#17 在 Top 12 外！）|
| 间隔2天重大退出 | affaan-m/ECC（#4→#14）/ hardikpandya/stop-slop（#3→#15）/ Understand-Anything（完全退出）|
| Python Trending 新亮点 | OpenBMB/VoxCPM（21,885，Tokenizer-Free TTS）/ opendatalab/MinerU（65,591，PDF→Markdown）|

---

## 今日 Top 12 一览

| 排名 | 仓库 | Stars | 语言 | 状态 |
|---|---|---|---|---|
| #01 | harry0703/MoneyPrinterTurbo | 68,859 | Python | Day 3（+7,979/2天，+13.1%）|
| #02 | microsoft/markitdown | 129,015 | Python | 今日新上榜 🆕 |
| #03 | EveryInc/compound-engineering-plugin | 18,002 | Markdown | 今日新上榜 🆕，161 次发布！8平台支持 |
| #04 | twentyhq/twenty | 48,215 | TypeScript | Day 3（#10→#4 升位，+1,062/2天）|
| #05 | anthropics/claude-code | 127,689 | TypeScript | 今日新上榜 🆕，Anthropic 官方 Claude Code CLI |
| #06 | Leonxlnx/taste-skill | 27,669 | Markdown | Day 4（+4,081/2天，+17.3%）|
| #07 | cursor/plugins | 1,199 | TypeScript | 今日新上榜 🆕，Cursor 官方插件，极新！|
| #08 | run-llama/liteparse | 6,879 | Python | 今日新上榜 🆕，LlamaIndex 文档解析 |
| #09 | galilai-group/stable-worldmodel | 1,109 | Python | 今日新上榜 🆕，世界模型研究平台 |
| #10 | byoungd/English-level-up-tips | 49,452 | Markdown | 升入 Top 12（#13→#10）|
| #11 | Biohub/esm | 2,521 | Python | 今日新上榜 🆕，蛋白质语言模型 |
| #12 | Crosstalk-Solutions/project-nomad | 26,759 | Shell | 今日新上榜 🆕，离线生存 AI 计算机 |

---

## 今日洞察

### 1. 🔌 "Plugin 战争" 同日引爆 Top 12：claude-code（#5，127k）+ cursor/plugins（#7，极新）+ compound-engineering-plugin（#3，18k，161次发布）——AI coding IDE 插件生态战争正式打响

今日最重要的结构性事件：AI coding IDE 的 **Plugin 生态战争**在 GitHub Trending 层面正式同日呈现，三个角色各占一席：

- **anthropics/claude-code**（#5，127,689 Stars，20,892 forks）——Anthropic 官方 Claude Code CLI 进入 All-language Trending Top 12。"An agentic coding tool that lives in your terminal, understands your codebase"，是 Anthropic 的 IDE 基础设施。
- **cursor/plugins**（#7，1,199 Stars，极新！）——Cursor 官方插件规范与官方插件仓库，今日才进入 Trending（Stars 极低但足以上榜，说明是非常新的仓库）。结构：marketplace.json + 每个 plugin 含 skills/（SKILL.md）+ rules/（.mdc）+ mcp.json。官方插件：continual-learning / cursor-team-kit / thermos / pr-review-canvas / docs-canvas / orchestrate / pstack 等 11 个。
- **EveryInc/compound-engineering-plugin**（#3，18,002 Stars，161 次发布！）——Every.inc 出品的第三方工程方法论插件，支持 Claude Code/Cursor/Codex/GitHub Copilot/Factory Droid/Qwen Code/OpenCode 等 8 个平台。哲学："Each unit of engineering work should make subsequent units easier -- not harder." 核心循环：/ce-strategy → /ce-ideate → /ce-brainstorm → /ce-plan → /ce-work → /ce-code-review → /ce-compound。161 次发布说明是成熟的生产级项目。

三角关系：大平台官方 CLI（Claude Code）+ IDE 官方插件规范（Cursor）+ 第三方插件内容提供商（Compound Engineering）——正如手机 App Store 生态的三层结构：iOS（Claude Code）+ App Store 规范（cursor/plugins）+ 开发者（compound-engineering-plugin）。

**今日是本系列日报首次出现"多 IDE 平台官方 Plugin 仓库同日入 Top 12"**。

---

### 2. 📄 "文档→Markdown 基础设施" 三角浮现：markitdown（#2，129k）+ liteparse（#8，6.8k）+ MinerU（Python Trending，65k）——SKILL.md 生态的数据摄取层正在成熟

今日有三个"文档解析/转换为 Markdown"方向的项目同时在榜：

- **microsoft/markitdown**（#2，129,015 Stars）——Microsoft 官方出品，"Python tool for converting files and office documents to Markdown"，支持 PDF/Word/Excel/PowerPoint/图片/HTML 等几乎所有常见格式。
- **run-llama/liteparse**（#8，6,879 Stars）——LlamaIndex（run-llama）出品，"A fast, helpful, and open-source document parser"。
- **opendatalab/MinerU**（Python Trending，65,591 Stars）——"Transforms complex documents like PDFs and Office docs into LLM-ready markdown/JSON for your Agentic workflows."

为什么这三个项目今日同时在 Trending？根本原因：**SKILL.md + agent 工作流要求所有输入文档必须先转换为 Markdown**——当 claude-code/cursor/plugins/compound-engineering 等 IDE 插件生态成熟后，"将现有企业文档转为 LLM 可消费格式"成为每个 agent 工作流的第一步。markitdown（微软）+ liteparse（LlamaIndex）+ MinerU（OpenDataLab）代表了这一基础设施赛道的三路竞争。

配合 PaddlePaddle/PaddleOCR（Python Trending，78,944，"Turn any PDF or image document into structured data for your AI"），今日 Python Trending 中"文档基础设施"方向项目有 4 个之多，是本系列日报中该方向最高密度。

---

### 3. 🏆 codecrafters-io/build-your-own-x（#17，**507,071 ⭐！**）——本系列日报迄今 Trending 列表中 Stars 最高项目，刚好在 Top 12 外

"Master programming by recreating your favorite technologies from scratch." 507,071 Stars，48,150 forks。今日 All-language Trending #17——刚好排在 Top 12 外。

507,071 Stars 是本系列日报迄今为止出现在 Trending 页面的所有项目中的 Stars 最高记录（超越昨日 obra/superpowers 的 209k）。这个项目并非今日刚创建——它是 GitHub 历史上最受欢迎的学习类仓库之一，今日出现在 Trending 说明有新的活动推动了曝光度。

在今日 IDE 插件和文档基础设施主导的 Trending 中，build-your-own-x 的出现提醒我们：**"基础编程学习"始终是开发者社区的底层常青需求**，即使 AI coding 工具如此发达，自己动手从零构建技术（编写 HTTP 服务器、数据库、编译器）仍有持久魅力。

---

### 4. 🔄 ECC（#4→#14）+ stop-slop（#3→#15）+ Understand-Anything（完全退出）——2天内 Top 12 换血 8 席次，Skills 浪潮退潮，Plugin 生态接棒

2天内的最大变化：
- **ECC**（affaan-m/ECC）：05-27 #4（195,636）→ 05-29 #14（198,220，+2,584/2天但退出 Top 12）
- **stop-slop**：05-27 #3（5,448）→ 05-29 #15（6,784，+1,336/2天但退出 Top 12）
- **Understand-Anything**：05-27 #2（38,811）→ 05-29 **完全不在 Trending 列表**（Day 4 之后急速降温）
- **anthropics/knowledge-work-plugins / p-e-w/heretic / Cybersecurity-Skills / obra/superpowers**：全部退出

今日新入的 8 个项目全部是 IDE 插件生态（claude-code/cursor/plugins/compound-engineering）+ 文档基础设施（markitdown/liteparse）+ 研究工具（stable-worldmodel/Biohub-esm）+ 离线 AI（project-nomad）方向。

信号：GitHub Trending 生态从"Skills 浪潮"（05-24~05-28，以 SKILL.md 格式的 agent 配置工具为核心）转向"Plugin 生态战争"（05-29 起，以 IDE 官方 Plugin 规范和工具为核心）。Skills 是"如何配置 agent 行为"，Plugins 是"如何在 IDE 层扩展 agent 能力"——是同一技术趋势的下一个演化阶段。

---

## Top 12 详情

### #01 · harry0703/MoneyPrinterTurbo

**Day 3 · #1 守位 · 68,859 ⭐ · 2天增量 +7,979（+13.1%）**

- **仓库**：https://github.com/harry0703/MoneyPrinterTurbo
- **Stars**：68,859（05-27：60,880，+7,979，+13.1%）| Forks：9,936
- **语言**：Python | Releases：10
- **描述**：利用AI大模型，一键生成高清短视频 Generate short videos with one click using AI LLM.
- **在榜历程**：05-27 #1（60,880）→ 05-29 #1（68,859，+7,979/2天）
- **编辑点评**：连续 3 天守 #1。2天 +7,979（+13.1%）说明热度真实、持续，不是一日爆发即消退的模式。今日在 8 个新入项目的冲击下仍守 #1，说明其"中文 AI 视频生成"需求的持续度极高。支持 DeepSeek/Moonshot/Ollama 等，中国开发者社区核心项目。今日与 microsoft/markitdown（#2）+ opendatalab/MinerU（Python Trending）共同出现在 Python Trending，代表了"内容生产工具"方向（视频生成 + 文档转换 + 文档解析）的三路成熟。

---

### #02 · microsoft/markitdown

**今日新上榜 · #2 · 129,015 ⭐ · Python 文件/文档→Markdown 转换工具 · 微软官方**

- **仓库**：https://github.com/microsoft/markitdown
- **Stars**：129,015 | Forks：8,845
- **语言**：Python
- **描述**：Python tool for converting files and office documents to Markdown.
- **编辑点评**：今日新入 #2，129,015 Stars，8,845 forks。微软官方出品。在"文档→Markdown 基础设施"三角（markitdown + liteparse + MinerU）中占据最高 Stars、最广格式支持、最强企业背书的位置。在 cursor/plugins（#7）和 compound-engineering-plugin（#3）等 IDE 插件工具的语境中，markitdown 是"将企业现有文档（PPT/Word/Excel/PDF）转换为 agent 可消费 Markdown"的关键前置工具。SKILL.md + RAG + agent 工作流的数据摄取层基础设施代表之一。

---

### #03 · EveryInc/compound-engineering-plugin

**今日新上榜 · #3 · 18,002 ⭐ · 161 次发布 · "AI skills and agents that make each unit of engineering work easier than the last"**

- **仓库**：https://github.com/EveryInc/compound-engineering-plugin
- **Stars**：18,002 | Forks：1,371 | Releases：**161**！
- **语言**：Markdown（TypeScript）
- **描述**：Official Compound Engineering plugin for Claude Code, Codex, Cursor, and more
- **哲学**："Each unit of engineering work should make subsequent units easier -- not harder." 80% 在 planning 和 review，20% 在 execution。
- **核心 slash commands**：
  - `/ce-strategy` — 捕获产品目标/方法/用户画像/指标，存入 STRATEGY.md
  - `/ce-ideate` — 生成并批评更大的想法，产出排名后的 ideation artifact
  - `/ce-brainstorm` — 需求精炼，plan 前置
  - `/ce-plan` — 详细实现计划
  - `/ce-work` — 执行计划
  - `/ce-debug` — 专注 bug 调查
  - `/ce-code-review` / `/ce-doc-review` — 代码/文档审查
  - `/ce-compound` — 将学习编码为可复用知识（防止下一个 agent 重学同样的课）
  - `/ce-product-pulse` — 时间窗口内的用户体验报告，存入 docs/pulse-reports/
- **支持平台**（8个）：Claude Code / Cursor / Codex / GitHub Copilot / Factory Droid / Qwen Code / OpenCode / Pi + Gemini + Kiro
- **编辑点评**：161 次发布（本系列日报中 releases 数最高的入榜项目！）说明这是一个经过长期迭代、真实生产使用的项目，而非新鲜概念项目。Every.inc 是知名 AI 写作和研究工具公司。"/ce-compound"（将工程学习编码为可复用知识）是与 karpathy-skills/ECC 等项目最大的差异点——它不只是给 agent 配置行为，而是帮助 agent 在每次工作后积累可传承的知识，实现复利效应。

---

### #04 · twentyhq/twenty

**Day 3 · #10→#4 升位 · 48,215 ⭐ · "The open alternative to Salesforce, designed for AI"**

- **仓库**：https://github.com/twentyhq/twenty
- **Stars**：48,215（05-27：47,153，+1,062/2天，+2.3%）| Forks：6,831
- **语言**：TypeScript
- **编辑点评**：Day 3，从 05-27 #10 升至今日 #4，大幅提升 6 位。+1,062/2天（+2.3%）增速稳健。今日 TypeScript 项目（twenty/#4 + claude-code/#5 + cursor/plugins/#7）= 3 项（25%），是本系列日报中 TypeScript 比例首次达到 25%，反映了 IDE 工具生态（TypeScript 主导）今日的强势入榜。"Designed for AI"定位在 AI agent 生态成熟后愈发精准：agent 需要操作 CRM 数据、自动化销售流程，twenty 的 AI-native 设计使其成为 agent 可直接集成的 CRM 平台。

---

### #05 · anthropics/claude-code

**今日新上榜 · #5 · 127,689 ⭐ · Anthropic 官方 Claude Code CLI · "Plugin 战争" IDE 端代表**

- **仓库**：https://github.com/anthropics/claude-code
- **Stars**：127,689 | Forks：20,892
- **语言**：TypeScript
- **描述**："Claude Code is an agentic coding tool that lives in your terminal, understands your codebase, and helps you code faster by executing routine tasks, explaining complex code, and handling git workflows - all through natural language commands."
- **编辑点评**：今日新入 #5，127,689 Stars，20,892 forks（本系列日报 Top 12 历史中 forks 数最高之一）。anthropics/claude-code 是本系列日报首次出现的"AI IDE 官方 CLI 仓库入 All-language Trending"——不是 Skills/Plugins，而是 CLI 工具本身。在"Plugin 战争"语境中，claude-code 是 Anthropic 的 IDE 平台层；cursor/plugins（#7）是 Cursor 的 IDE 平台层。两者同日入 Top 12，是 AI coding IDE 生态战争在 GitHub Trending 层面的直接呈现。20,892 forks 说明开发者在深度参与（fork、贡献、构建扩展）。

---

### #06 · Leonxlnx/taste-skill

**Day 4 · 27,669 ⭐ · +4,081（+17.3%，2天）· Anti-Slop 前端 Skills**

- **仓库**：https://github.com/Leonxlnx/taste-skill
- **Stars**：27,669（05-27：23,588，+4,081/2天，+17.3%！）| Forks：2,051
- **语言**：Markdown
- **编辑点评**：Day 4，2天增量 +4,081（+17.3%），是今日留榜项目增速最高（MoneyPrinterTurbo +7,979 但绝对值高，百分比 +13.1%；taste-skill +17.3% 百分比更高）。今日 Skills 类项目大幅减少（上周 6 项→今日仅 2 项：compound-engineering-plugin + taste-skill），taste-skill 是 Skills 方向的"钉子户"——在 Plugin 生态接棒的过渡期，taste-skill 依然保持高增速，说明"AI 生成 UI 的品质"是一个独立于 IDE 工具平台战争的持续刚需。

---

### #07 · cursor/plugins

**今日新上榜 · #7 · 1,199 ⭐ · Cursor 官方插件规范与官方插件仓库 · 极新！**

- **仓库**：https://github.com/cursor/plugins
- **Stars**：1,199 | Forks：105
- **语言**：TypeScript（含 Markdown/JSON）
- **描述**：Cursor plugin specification and official plugins
- **官方插件列表**（11个）：
  - `continual-learning`（持续学习）
  - `cursor-team-kit`（Cursor 团队协作套件）
  - `thermos`（温度/上下文管理）
  - `create-plugin`（插件创建脚手架）
  - `agent-compatibility`（agent 兼容性）
  - `cli-for-agent`（agent 命令行）
  - `pr-review-canvas`（PR 审查画布）
  - `docs-canvas`（文档画布）
  - `cursor-sdk`（Cursor SDK）
  - `orchestrate`（编排）
  - `pstack`（技术栈配置）
- **仓库结构**：每个 plugin 含 `.cursor-plugin/plugin.json`（manifest）+ `skills/`（SKILL.md）+ `rules/`（.mdc 文件）+ `mcp.json`（MCP 服务定义）
- **编辑点评**：今日 Stars 最低新入（1,199！），但意义最重大：这是 Cursor 官方的 plugin 规范和官方插件仓库，stars 低说明是今日或近日刚刚公开发布的新仓库。仓库结构揭示了 Cursor 的 Plugin 规范：plugin.json 定义元数据，SKILL.md 定义技能，.mdc 定义 rules，mcp.json 定义 MCP 服务——这几乎与 Anthropic 的 Skills 规范完全对齐。**两个最主要的 AI coding IDE（Claude Code 和 Cursor）今日同日入 Top 12，且它们的 Plugin 规范都基于 SKILL.md 格式**——这是 SKILL.md 成为跨 IDE 统一标准的重要确认。

---

### #08 · run-llama/liteparse

**今日新上榜 · #8 · 6,879 ⭐ · LlamaIndex 出品 · "A fast, helpful, and open-source document parser"**

- **仓库**：https://github.com/run-llama/liteparse
- **Stars**：6,879 | Forks：429
- **语言**：Python
- **描述**：A fast, helpful, and open-source document parser
- **编辑点评**：今日新入 #8，6,879 Stars。LlamaIndex（run-llama）出品。在"文档→Markdown 基础设施"三角（markitdown/#2 + liteparse/#8 + MinerU/Python Trending）中，liteparse 是 LlamaIndex 生态的文档解析工具——LlamaIndex 一直是 RAG 和 agent 工作流中的核心框架，liteparse 是其文档摄取层的独立开源工具。今日与 markitdown（Microsoft，文件转换）+ MinerU（OpenDataLab，PDF 提取）共同出现，说明"文档基础设施"赛道已形成成熟的竞争格局。

---

### #09 · galilai-group/stable-worldmodel

**今日新上榜 · #9 · 1,109 ⭐ · "A platform for reproducible world model research and evaluation"**

- **仓库**：https://github.com/galilai-group/stable-worldmodel
- **Stars**：1,109 | Forks：143 | Releases：6
- **语言**：Python
- **描述**：A platform for reproducible world model research and evaluation
- **技术定位**："stable-worldmodel provides a single, unified interface for the three stages of world model research — collecting data, training, and evaluating with model-predictive control — across a large suite of standardized environments."
- **核心能力**：统一接口覆盖数据收集/训练/评估三阶段；DeepMind Control Suite/Gymnasium/Atari（100+）/OGBench/Craftax 等多环境；CEM Solver 用于 model-predictive control；支持 LeRobot 数据集；参考实现 LeWM 和 DINO-WM。
- **编辑点评**：今日最具学术色彩的新入项目（1,109 Stars，6 次发布）。"World Model"是具身 AI（Embodied AI）和强化学习的核心概念——agent 学习世界的内部模型以规划行动。在今日以 IDE 插件为主题的 Trending 中，stable-worldmodel 代表了"AI 基础研究工具"方向，是今日 Trending 中与 agent 编程工具生态最不同的项目类型。Name 明显参考了 stable-baselines3（强化学习基础算法库）的命名惯例。

---

### #10 · byoungd/English-level-up-tips

**升入 Top 12 · 49,452 ⭐ · "An advanced guide to learn English"**

- **仓库**：https://github.com/byoungd/English-level-up-tips
- **Stars**：49,452（05-27：46,022/49,452，+1,430）| Forks：5,183
- **语言**：Markdown
- **描述**：An advanced guide to learn English which might benefit you a lot 🎉 . 离谱的英语学习指南/英语学习教程/英语学习/学英语
- **编辑点评**：从 05-27 #13 升入今日 #10。49,452 Stars，5,183 forks。这是一个纯 Markdown 的英语学习指南——在 AI coding 工具和 agent 生态主导的 Trending 中，一个英语学习项目的出现是有趣的对照：随着中国开发者大量参与 AI 开发工具生态（MoneyPrinterTurbo 是 #1），英语学习需求也在同步上升（更多技术文档是英文的，更多 CLI 工具/SKILL.md/AGENTS.md 是英文写作的）。两者共同反映了中国开发者社区在 AI 时代的技术升级需求。

---

### #11 · Biohub/esm

**今日新上榜 · #11 · 2,521 ⭐ · 蛋白质语言模型（ESM）**

- **仓库**：https://github.com/Biohub/esm
- **Stars**：2,521 | Forks：311
- **语言**：Python
- **描述**：（ESM - Evolutionary Scale Modeling，蛋白质序列语言模型，由 Chan Zuckerberg Biohub 维护）
- **编辑点评**：今日最特殊的新入项目——蛋白质语言模型进入 All-language Trending Top 12！ESM（Evolutionary Scale Modeling）最初由 Meta AI Research 开发，是最重要的蛋白质序列预训练模型之一，Chan Zuckerberg Biohub 是 Mark Zuckerberg 和 Priscilla Chan 联合成立的生物医学研究机构。在 AI coding 工具和 agent 基础设施主导的 Trending 中，Biohub/esm 的出现提醒我们：**LLM 技术正在全面渗透生命科学研究领域**，ESM 等蛋白质序列模型正是 LLM 思想在生物学上的直接应用。这是本系列日报首次出现生命科学 AI 模型入 Top 12。

---

### #12 · Crosstalk-Solutions/project-nomad

**今日新上榜 · #12 · 26,759 ⭐ · Project N.O.M.A.D - Node for Offline Media, Archives, and Data**

- **仓库**：https://github.com/Crosstalk-Solutions/project-nomad
- **Stars**：26,759 | Forks：2,645 | Releases：69
- **语言**：Shell
- **描述**：Project N.O.M.A.D, is a self-contained, offline survival computer packed with critical tools, knowledge, and AI to keep you informed and empowered—anytime, anywhere.
- **全称**：Node for Offline Media, Archives, and Data
- **核心理念**：离线优先（offline-first）的知识和教育服务器，可安装在任何 Debian 系统（推荐 Ubuntu），完全基于 terminal 操作，通过浏览器访问所有工具和资源，无需桌面环境。
- **编辑点评**：今日最具"末日预备"气质的项目。69 次发布说明是长期维护的成熟项目。在 AI 工具全面联网的今天，一个强调"完全离线"+"自包含"+"知识永不下线"的项目出现在 Trending，说明**去中心化/离线 AI 需求**正在上升。与 vllm（本地推理引擎）、heretic（去中心化/去审查）、project-nomad（离线生存）共同构成一个趋势：开发者正在构建不依赖云端/不受中心化控制的 AI 基础设施。

---

## 语言分布

| 语言 | 项目数 | 占比 | 项目 |
|---|---|---|---|
| Python | 5 | 42% | MoneyPrinterTurbo / markitdown / liteparse / stable-worldmodel / Biohub-esm |
| TypeScript | 3 | 25% | twentyhq/twenty / anthropics/claude-code / cursor/plugins |
| Markdown | 3 | 25% | compound-engineering-plugin / taste-skill / English-level-up-tips |
| Shell | 1 | 8% | Crosstalk-Solutions/project-nomad |

**关键变化**：Python 从 05-27 的 33% 回升至今日 42%；Markdown 从 05-27 的 50% 大幅降至 25%（Skills 浪潮退潮）；TypeScript 首次以 25% 并列第二，是 IDE 插件生态（claude-code/cursor/twenty）入榜的体现。

**Markdown 降至 25% 的含义**：Skills 浪潮（Markdown-as-infrastructure，05-24~05-28 高峰）已经退潮，今日进入"Plugin 生态战争"阶段——插件生态需要真实的代码（TypeScript，用于实现 plugin.json/plugin manifest 和工具逻辑），不只是 Markdown 配置文件。

---

## GitHub Explore 精选

### Explore #1 · codecrafters-io/build-your-own-x（全语言 Trending #17）

- **Stars**：507,071！ | Forks：48,150
- **描述**：Master programming by recreating your favorite technologies from scratch.
- **分析**：507,071 Stars——本系列日报迄今为止出现在 Trending 页面的所有项目中 Stars 最高记录（超越昨日 superpowers 的 209k）。#17 刚好在 Top 12 外，但绝对值远超任何 Top 12 项目。这是 GitHub 历史上最受欢迎的编程学习项目之一，内容涵盖从零构建 HTTP 服务器/数据库/编译器/操作系统/Git 等 40+ 技术栈。在 AI coding 工具和 Plugin 生态主导的今天，build-your-own-x 的持续活跃说明：**即使有 Claude Code/Cursor 等 AI 助手，开发者仍渴望理解技术底层原理**——这与 heretic（去黑盒化）/ stable-worldmodel（可复现研究）的精神一脉相承。

### Explore #2 · opendatalab/MinerU（Python Trending）

- **Stars**：65,591 | Forks：5,532
- **描述**：Transforms complex documents like PDFs and Office docs into LLM-ready markdown/JSON for your Agentic workflows.
- **分析**：65,591 Stars，Python Trending。今日"文档→Markdown 基础设施"三角的第三角（markitdown/#2 + liteparse/#8 + MinerU）。"LLM-ready markdown/JSON for your Agentic workflows"定位明确，是 agent 工作流的前置数据处理层。opendatalab（上海 AI Lab 下属）出品，代表了中国 AI 研究机构在 agent 基础设施赛道的成熟贡献。

### Explore #3 · PaddlePaddle/PaddleOCR（Python Trending）

- **Stars**：78,944 | Forks：10,518
- **描述**：Turn any PDF or image document into structured data for your AI. A powerful, lightweight OCR toolkit that bridges the gap between images/PDFs and LLMs. Supports 100+ languages.
- **分析**：78,944 Stars，Python Trending。"bridges the gap between images/PDFs and LLMs"——今日文档基础设施方向第四项。PaddleOCR + markitdown + liteparse + MinerU 四项共同出现，说明"非结构化数据→LLM 可消费格式"已经形成完整的工具生态，是 2026 AI agent 基础设施建设的重要组成部分。

### Explore #4 · OpenBMB/VoxCPM（Python Trending）

- **Stars**：21,885 | Forks：2,587
- **描述**：VoxCPM2: Tokenizer-Free TTS for Multilingual Speech Generation, Creative Voice Design, and True-to-Life Cloning
- **分析**：21,885 Stars，Python Trending。"Tokenizer-Free TTS"——TTS（文字转语音）的新一代架构，不需要分词器即可处理多语言语音生成、创意声音设计、逼真克隆。配合 dograh（昨日 Explore #4，自托管语音 AI 平台）+ airi（AI 伴侣语音），今日与 OpenMOSS/MOSS-TTS（2,458 Stars）同日在 Python Trending，说明"AI 语音生成"赛道正在经历密集的新进展期。

### Explore #5 · fastapi/fastapi（Python Trending）

- **Stars**：98,636 | Forks：9,349
- **描述**：FastAPI framework, high performance, easy to learn, fast to code, ready for production
- **分析**：98,636 Stars，Python Trending 今日重新出现。FastAPI 是 Python 最受欢迎的 Web 框架之一，在 AI agent 生态中有重要地位：MCP 服务器、agent API 端点、工具调用接口等大量使用 FastAPI。今日与 run-llama/liteparse（#8）+ anthropics/claude-code（#5）+ cursor/plugins（#7）共同出现，说明 FastAPI 依然是 agent 基础设施的核心 Web 框架选择。

---

## 今日 vs 05-27 对比

### 留榜项目（2天增量）

| 项目 | 05-27 Stars（排名）| 05-29 Stars（排名）| +2天 |
|---|---|---|---|
| harry0703/MoneyPrinterTurbo | 60,880（#1）| 68,859（#1）| +7,979（+13.1%）|
| Leonxlnx/taste-skill | 23,588（#6）| 27,669（#6）| +4,081（+17.3%！）|
| twentyhq/twenty | 47,153（#10）| 48,215（#4）| +1,062（+2.3%，**#10→#4 升位**！）|

### 升入 Top 12

| 项目 | 05-27 位置 | 05-29 排名 |
|---|---|---|
| byoungd/English-level-up-tips | #13（刚出 Top 12）| #10（升入）|

### 今日退出（05-27 Top 12 → 05-29 完全不在或退出）

- **Lum1104/Understand-Anything**（#2，38,811）→ **完全不见**！Day 4 之后急速降温
- **affaan-m/ECC**（#4，195,636）→ #14（198,220，退 Top 12）
- **hardikpandya/stop-slop**（#3，5,448）→ #15（6,784，退 Top 12）
- anthropics/knowledge-work-plugins（#5）/ p-e-w/heretic（#7）/ Kronos（#8）/ Cybersecurity-Skills（#9）/ FreeDomain（#11）/ superpowers（#12）→ 全部退出

---

*报告生成：2026-05-29 · 数据来源：https://github.com/trending + https://github.com/trending/python?since=daily*
