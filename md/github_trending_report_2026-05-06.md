# GitHub Trending 日报 · 2026-05-06

## Meta
- **日期**：2026-05-06
- **数据来源**：GitHub Trending（全语言） + Python Trending
- **今日 Top 12**：12 个项目 | 累计 Stars：1.46M+ | 编程语言：4 | 今日新上榜：7 | 持续上榜：5

---

## 今日洞察

### 🏆 "超级资源三件套"同日登场——432k + 346k + 121k，知识资源共振现象

public-apis/public-apis（432,503 ⭐）、jwasham/coding-interview-university（346,120 ⭐）、microsoft/markitdown（120,948 ⭐）三大知识资源类项目同日出现在 Trending，合计星数超过 90 万。这三个项目共同特征是"无业务逻辑、纯粹输出价值"：public-apis 是 500+ 免费 API 集合、coding-interview-university 是 CS 系统学习路线图、markitdown 是微软的文档格式转 Markdown 工具。三者在同一天集体登榜，是社区学习与技术分享热潮的最强信号：当大量开发者同时分享"让你变强"的资源时，Trending 就会出现这种集体共振。

### 🤖 forrestchang/andrej-karpathy-skills（115k）——"一个 CLAUDE.md 文件"引发的 GitHub 现象级事件

115,419 ⭐、11,544 forks，仓库核心内容是一个 CLAUDE.md 文件。作者将 Andrej Karpathy 在社交媒体上批评 LLM 编程缺陷的帖子（"LLM 不管理自己的困惑 / 不推回 / 偏爱过度复杂的代码"）提炼为 4 条原则：① Think Before Coding（主动问清需求，不默默做假设）② Simplicity First（最少代码解决问题，拒绝过度设计）③ Surgical Changes（只改动必须改动的，不"顺手优化"）④ Goal-Driven Execution（每步定义成功标准，自我验证循环）。它不是工具，不是框架，是一个行为约束文件——却在 Claude Code 用户社区中病毒传播，到 115k Stars。这是"Karpathy 品牌 × AI 编程工具爆发"最具代表性的交叉现象。

### 🦌 bytedance/deer-flow 2.0（65k）——字节跳动 SuperAgent Harness 重磅开源

从 Deep Research 框架重构为 SuperAgent Harness，是今日最重要的企业开源事件。DeerFlow 2.0 不再是"框架"而是一个"运行时"：内置文件系统 / 长期记忆 / 技能架构（.skill archive）/ 沙箱隔离执行 / 动态子 Agent 孵化（并行探索，汇报结构化结果）。技能系统按需加载（避免 context 膨胀），支持 MCP 自定义工具，并已内置 claude-to-deerflow 技能，让 Claude Code 用户一条命令接入本地 DeerFlow 实例。65k Stars + 8.6k forks，是今日除 agency-agents 外最受关注的 AI 工程项目。

### 🕷️ D4Vinci/Scrapling（45.6k）——Python 自适应爬虫框架，"反检测 + MCP + Scrapy API"三合一

45,604 ⭐，45 次发布，92% 测试覆盖率。Scrapling 不是普通爬虫库，而是一个全栈爬虫框架：StealthyFetcher（内置反 bot 检测 + TLS 指纹伪装）+ DynamicFetcher（Playwright 浏览器自动化）+ Scrapy 风格 Spider API（并发/断点续传/Streaming）+ MCP Server（AI 辅助数据提取，与 Claude/Cursor 集成），全异步支持，比主流 Python 爬虫库快 10x JSON 序列化。45k Stars 对于一个专用工程工具来说极为罕见，说明其已形成真实用户群体。

---

## 今日热门 Top 12（按总 Stars 排序）

### #01 public-apis/public-apis ⭐ 432,503 [新上榜]
- **仓库**：https://github.com/public-apis/public-apis
- **语言**：Python | **License**：MIT | **Forks**：47,283
- **描述**：A collective list of free APIs. 全球最大免费 API 资源列表，分类收录 500+ 开放 API（天气/金融/机器学习/游戏/地图/安全等），是每个 Web 开发者书签中的必备资源。
- **核心特性**：
  - 分类收录 500+ 免费公开 API，持续更新
  - HTTPS / Auth / CORS 属性标注，一眼可判断可用性
  - 社区维护 + 自动化校验，质量有保障
  - 支持按类别筛选（Animals / Business / Finance / Science / Weather 等）
- **技术栈**：Python（校验脚本）/ Markdown（主体内容）
- **适用场景**：Web 开发项目快速找 API；学习 REST API；构建 Demo 或 Hackathon 项目。
- **推荐语**：432k Stars 是 GitHub 全站前 5——今日登榜只说明一件事：又一波"新人开发者"发现了这个列表，并且每次发现都是爆炸式传播。

---

### #02 jwasham/coding-interview-university ⭐ 346,120 [新上榜]
- **仓库**：https://github.com/jwasham/coding-interview-university
- **语言**：Markdown | **License**：CC-BY-SA-4.0 | **Forks**：82,774
- **描述**：A complete computer science study plan to become a software engineer. John Washam（前亚马逊工程师）2016 年创建的 CS 系统学习路线图，82k forks 是今日所有项目中第一。
- **核心特性**：
  - 覆盖算法/数据结构/操作系统/网络/分布式系统/系统设计/数学基础全领域
  - 每个知识点附带推荐学习资源（书籍/视频/实现代码）
  - 内置学习打卡机制：checkbox 自我追踪
  - 多语言翻译版本（中文/日文/韩文/葡萄牙文等）
- **技术栈**：Markdown + 社区维护
- **适用场景**：自学 CS 准备软件工程岗位；系统性补全 CS 基础；刷题前的知识储备阶段。
- **推荐语**：82k forks 是今日最高——2016 年起持续被分享，10 年不衰。每当技术招聘季到来，coding-interview-university 就会重新进入热榜。

---

### #03 microsoft/markitdown ⭐ 120,948 [新上榜]
- **仓库**：https://github.com/microsoft/markitdown
- **语言**：Python | **License**：MIT | **Forks**：8,096
- **描述**：Python tool for converting files and office documents to Markdown. 微软出品，支持 PDF / Word / Excel / PowerPoint / 图片 / HTML / 音频等多种格式转 Markdown，LLM 文档预处理管道的标配工具。
- **核心特性**：
  - 支持格式：PDF / Word（.docx）/ PowerPoint（.pptx）/ Excel（.xlsx）/ 图片（EXIF + OCR）/ 音频（转录）/ HTML / ZIP
  - 一行命令或 Python API 调用
  - 插件系统：自定义转换器
  - LLM 集成友好：统一 Markdown 输出 + token 友好格式
- **技术栈**：Python / pdfminer / python-pptx / openpyxl / Pillow / OpenAI Whisper（音频）
- **适用场景**：LLM 文档 RAG 预处理；文件格式统一转换；PDF/Office 内容提取自动化。
- **推荐语**："微软版 pandoc，专为 LLM 优化"——markitdown 在 RAG 工程师圈已成事实标准，121k Stars 证明这个痛点有多普遍。

---

### #04 forrestchang/andrej-karpathy-skills ⭐ 115,419 [新上榜]
- **仓库**：https://github.com/forrestchang/andrej-karpathy-skills
- **语言**：Markdown | **License**：MIT | **Forks**：11,544
- **描述**：A single CLAUDE.md file to improve Claude Code behavior, derived from Andrej Karpathy's observations on LLM coding pitfalls. 一个文件，4 条原则，115k Stars。
- **核心特性**：
  - **Think Before Coding**：明确说出假设，有歧义时询问而非猜测，可以推回不合理需求
  - **Simplicity First**：最小代码解决问题，拒绝没被要求的抽象/配置/灵活性/错误处理
  - **Surgical Changes**：只改必须改的，不"顺手优化"相邻代码，自己制造的孤儿代码才清理
  - **Goal-Driven Execution**：每步定义可验证的成功标准，强标准 = AI 可独立循环完成
- **技术栈**：Markdown（CLAUDE.md / .cursorrules）
- **适用场景**：Claude Code / Cursor 用户直接放入项目根目录；AI 编程行为约束基础配置；Claude Code 新手入门最佳第一个 CLAUDE.md。
- **推荐语**："Karpathy 品牌 × AI 编程工具爆发的交叉点"——一个 CLAUDE.md 文件涨了 115k Stars，说明开发者对 LLM Coding 的行为约束有多迫切。

---

### #05 msitarzewski/agency-agents ⭐ 94,100 [持续 Day 2]
- **仓库**：https://github.com/msitarzewski/agency-agents
- **语言**：Markdown | **License**：MIT | **Forks**：15,475
- **描述**：A complete AI agency at your fingertips. 连续第 2 日上榜，Stars 从 93,034 增至 94,100，日增约 1,066，依然是近期 Trending 单日新上榜项目的 Stars 冠军。
- **核心特性**（同昨日）：13 部门 100+ 专业 Agent，全主流 AI IDE 支持
- **推荐语**："连续第 2 日上榜，依然是今日 Stars 第 5——The Agency 的病毒传播势头尚未减退。"

---

### #06 TauricResearch/TradingAgents ⭐ 69,837 [持续 Day 6]
- **仓库**：https://github.com/TauricResearch/TradingAgents
- **语言**：Python | **License**：Apache-2.0 | **Forks**：13,479
- **描述**：TradingAgents: Multi-Agents LLM Financial Trading Framework. 连续第 6 日上榜，Stars 从 68,346 增至 69,837，6 日累计增长约 4,364（05-01：65,473）。
- **推荐语**："连续第 6 日上榜——TradingAgents 是今日 Trending 持续热度最长的项目，6 日日均增约 727 Stars。"

---

### #07 bytedance/deer-flow ⭐ 65,293 [新上榜]
- **仓库**：https://github.com/bytedance/deer-flow
- **语言**：Python | **License**：MIT | **Forks**：8,636
- **描述**：DeerFlow 2.0 - An open-source long-horizon SuperAgent harness. 字节跳动开源，从 Deep Research 框架重构为带文件系统/记忆/技能/沙箱/子 Agent 的 SuperAgent 运行时，内置 Claude Code 接入技能。
- **核心特性**：
  - **SuperAgent 运行时**：内置文件系统 / 长期记忆 / .skill 技能架构 / 沙箱隔离执行
  - **动态子 Agent**：Lead Agent 按需孵化并行子 Agent，结构化汇报并合成
  - **技能系统**：按需加载（防 context 膨胀），内置研究/报告/PPT/图片生成等 Skill
  - **Claude Code 集成**：`claude-to-deerflow` 技能，一条命令接入本地 DeerFlow 实例
  - **4 种执行模式**：flash（快）/ standard / pro（规划）/ ultra（子 Agent）
  - **MCP 自定义工具**：支持 MCP Server + Python 函数 swap 任何工具
- **技术栈**：Python / LangGraph / LangChain / Docker / FastAPI
- **适用场景**：长时任务（分钟级到小时级）Agent 编排；研究报告/PPT/网页全自动生成；Claude Code 接入本地 SuperAgent。
- **推荐语**："字节跳动的 SuperAgent 答案——DeerFlow 2.0 不是框架而是运行时，内置 claude-to-deerflow 技能，是今日最值得 Claude Code 用户关注的新项目。"

---

### #08 sansan0/TrendRadar ⭐ 56,764 [持续 Day 2]
- **仓库**：https://github.com/sansan0/TrendRadar
- **语言**：Python | **License**：MIT | **Forks**：24,110
- **描述**：AI 驱动全网热点聚合 + 舆情监控，连续第 2 日上榜，Stars 从 56,599 增至 56,764，日增 165。
- **推荐语**："连续第 2 日上榜，24k forks 依然是今日最高，TrendRadar 是中文开源信息自动化工具的持续热门。"

---

### #09 D4Vinci/Scrapling ⭐ 45,604 [新上榜]
- **仓库**：https://github.com/D4Vinci/Scrapling
- **语言**：Python | **License**：MIT | **Forks**：4,219
- **描述**：🕷️ An adaptive Web Scraping framework that handles everything from a single request to a full-scale crawl! 45 次发布，92% 测试覆盖率，内置反 bot 检测 + MCP Server + Scrapy 风格 Spider API。
- **核心特性**：
  - **Scrapy 风格 Spider**：start_urls / async parse callbacks / 并发限速 / 断点续传 / Streaming 模式
  - **多种 Fetcher**：HTTP（TLS 指纹伪装）/ StealthyFetcher（全反 bot）/ DynamicFetcher（Playwright）
  - **反 bot bypass**：自动绕过 Cloudflare Turnstile/Interstitial，内置代理轮换
  - **AI 集成 MCP Server**：内置 MCP 服务，Claude/Cursor 直接调用，减少 token 消耗
  - **自适应元素追踪**：网站结构变化后智能重定位元素
  - **高性能**：JSON 序列化 10x 快于标准库，内存优化，完整 async 支持
- **技术栈**：Python / Playwright / asyncio / aiohttp / MCP
- **适用场景**：绕过反爬检测的数据采集；大规模并发爬虫；AI 辅助数据提取（+ Claude）。
- **推荐语**："45k Stars + 45 次发布的 Python 全栈爬虫框架——反 bot + MCP + Scrapy API 三合一，比市面上大多数爬虫库功能完整得多。"

---

### #10 ruvnet/ruflo ⭐ 44,548 [持续 Day 4]
- **仓库**：https://github.com/ruvnet/ruflo
- **语言**：TypeScript | **License**：MIT | **Forks**：4,935
- **描述**：🌊 The leading agent orchestration platform for Claude. 连续第 4 日上榜，Stars 从 42,206 增至 44,548，日增约 2,342，4 日累计增约 7.5k（05-03：37,290）。
- **推荐语**："连续第 4 日上榜，日增 2.3k——Ruflo 是今日 Claude Code 生态 Agent 编排的持续热度担当，4 天累计增 7.5k Stars。"

---

### #11 ccxt/ccxt ⭐ 42,289 [新上榜]
- **仓库**：https://github.com/ccxt/ccxt
- **语言**：JavaScript/Python | **License**：MIT | **Forks**：8,645
- **描述**：A cryptocurrency trading API with more than 100 exchanges in JavaScript / TypeScript / Python / C# / PHP / Go. 跨语言加密货币交易 API 库，100+ 交易所统一接口，42k Stars + 8.6k forks。
- **核心特性**：
  - 100+ 交易所统一 API（币安/OKX/Bybit/Coinbase/Kraken/HTX 等）
  - 6 种语言：JavaScript / TypeScript / Python / C# / PHP / Go
  - 统一接口：相同代码在不同交易所间切换
  - 支持 REST + WebSocket，支持现货/合约/期权/保证金
- **技术栈**：JavaScript / TypeScript / Python / C# / PHP / Go
- **适用场景**：加密货币量化交易程序开发；多交易所套利策略；加密货币数据采集。
- **推荐语**："42k Stars 的多语言加密货币交易 API 标准库——100+ 交易所统一接口，在 TradingAgents 连续 6 日上榜的背景下，ccxt 今日登场更像是金融 AI 生态的底层管道来集合。"

---

### #12 soxoj/maigret ⭐ 25,771 [持续 Day 6]
- **仓库**：https://github.com/soxoj/maigret
- **语言**：Python | **License**：MIT | **Forks**：1,788
- **描述**：🕵️ Collect a dossier on a person by username from 3000+ sites. 连续第 6 日上榜，Stars 从 25,216 增至 25,771，6 日累计增长 2,658（05-01：23,113）。
- **推荐语**："连续第 6 日上榜——maigret 是今日 Trending 连续上榜天数并列最长的项目（与 TradingAgents 均为 6 日），OSINT 赛道极为稳定。"

---

## 语言分布

| 语言 | 项目数 | 占比 | 代表项目 |
|---|---|---|---|
| Python | 7 | 58% | public-apis / markitdown / TradingAgents / deer-flow / TrendRadar / Scrapling / maigret |
| Markdown | 3 | 25% | coding-interview-university / andrej-karpathy-skills / agency-agents |
| TypeScript | 1 | 8% | ruvnet/ruflo |
| JavaScript | 1 | 8% | ccxt/ccxt |

---

## GitHub Explore 精选

1. **mksglu/context-mode**（13,416 ⭐）— 今日全语言 Trending 中最值得关注的工程工具。Context window 优化工具，对 AI coding agent 的工具输出进行沙箱化，减少 98% context 占用，支持 14 个平台（Claude Code / Cursor / Windsurf / Copilot 等），916 forks。

2. **AIDC-AI/Pixelle-Video**（12,465 ⭐）— 连续多日同时出现在全语言和 Python Trending。AI 全自动短视频引擎，今日继续热。

3. **Arindam200/awesome-ai-apps**（11,726 ⭐）— RAG / Agent / Workflow AI 应用合集，同时出现在全语言和 Python Trending，11.7k Stars + 1.5k forks，是今日 AI 应用资源类项目的代表。

4. **Hmbown/DeepSeek-TUI**（10,854 ⭐）— 在终端中运行的 DeepSeek 编程 Agent，825 forks，今日首次登 Trending。

5. **cocoindex-io/cocoindex**（8,561 ⭐）— 长期 Agent 增量处理引擎，同时出现在全语言 Trending 和 Python Trending 两张榜单，RAG/知识库/Agent 记忆层增量更新的核心基础设施。
