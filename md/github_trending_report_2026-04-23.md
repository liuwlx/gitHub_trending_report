# GitHub Trending 日报

## Meta
- 日期：2026-04-23
- 文件名：github_trending_report_2026-04-23.md
- 数据来源：GitHub Trending（全语言 + Python）、GitHub Explore
- 编码：UTF-8
- 语言：简体中文

---

## 页面意图

> 帮助技术人快速判断"今天 GitHub 上什么值得关注、为什么值得关注、对我有没有用"，而不是简单列名字和 star 数。

---

## 今日概况

| 指标 | 数值 |
|---|---|
| 收录项目总数 | 12 |
| 今日新上榜项目 | 7（Shannon、WorldMonitor、Open WebUI、Langfuse、vercel-labs/skills、Pixelle-Video、free-claude-code） |
| 昨日持续在榜 | 5 |
| AI 相关项目 | 11 |
| 编程语言分布 | Python 5、TypeScript 3、JavaScript 2、C++ /Python 1、Jupyter NB 1 |
| 今日最高 Star 项目 | open-webui/open-webui（134k） |

---

## 今日洞察

### 洞察一：AI 渗透测试自动化元年正式开启——Shannon 以 39.9k stars 冲上 Trending
`KeygraphHQ/shannon` 今日进入全语言 Trending，这是一个白盒 AI 自动渗透测试工具，分析源码识别攻击向量、启动真实漏洞利用（注入/XSS/SSRF/越权），只有带可复现 PoC 的漏洞才进入报告。核心价值主张：Claude Code/Cursor 让团队持续不间断交付代码，但渗透测试一年才做一次，Shannon 填补这 364 天的安全空白。这是继昨日 PayloadsAllTheThings 进入 Trending 后，连续第二日出现安全工具，AI 驱动的安全测试正在成为主流工程实践。

### 洞察二：LLMOps 补齐生产链路最后一块——Langfuse 进入 Trending
`langfuse/langfuse`（YC W23，25.8k stars）进入全语言 Trending，这是一个开源 LLM 可观测性 + 提示词管理 + 评估平台，提供追踪、评估、数据集管理和 Playground 四大核心能力。它的出现标志着 LLM 应用开发正在从"跑起来就行"进入"需要监控/评估/持续迭代"的生产成熟阶段。OpenTelemetry + LangChain + OpenAI SDK + LiteLLM 全链路集成，自托管 Docker 一键部署。

### 洞察三：Agent Skills 安装基础设施标准化——vercel-labs/skills 补齐"分发层"
昨日 VoltAgent/awesome-agent-skills（内容目录）上 Trending，今日 `vercel-labs/skills`（npx skills CLI，安装工具）上 Trending。两个项目形成"内容 + 分发"双轮：一个告诉你哪些技能值得安装，一个提供一条命令跨工具安装。更震撼的是 vercel-labs/skills 支持的工具数量：Claude Code、Codex、Cursor、Gemini CLI、Windsurf、GitHub Copilot、kimi-cli、OpenCode、Cline 等 **60+ AI 编程工具**，说明 Agent Skills 生态的边界已经扩展到了整个 AI 编程工具市场。

### 洞察四：Open WebUI 134k stars 重回热榜——自托管 LLM 前端需求仍旺盛
`open-webui/open-webui` 以 134k stars（GitHub 历史最高关注度 LLM Web UI 项目之一）重返 Python Trending，通常意味着触发了重大版本更新或功能发布。叠加今日 Langfuse（LLM 可观测性）也进入 Trending，说明"自托管完整 LLM 栈"的需求不仅没有被商业云产品取代，反而随着 AI 应用普及而继续增长。

---

## Top 12 项目详情

### #01 KeygraphHQ / shannon ⭐ 新上榜
**仓库**：https://github.com/KeygraphHQ/shannon
**Stars**：39,900 | **Forks**：4,400 | **语言**：TypeScript | **协议**：AGPL-3.0

**项目摘要**：
Shannon 是 Keygraph 开发的自主白盒 AI 渗透测试工具。它分析 Web 应用源码识别攻击向量，然后通过浏览器自动化和命令行工具对运行中的应用执行真实漏洞利用（注入攻击、认证绕过、SSRF、XSS），只有带可复现 PoC 的漏洞才进入最终报告。核心动机：Claude Code/Cursor 让团队每天持续交付代码，但渗透测试一年才做一次，Shannon 填补这 364 天的安全空白。在 OWASP Juice Shop 测试中识别出 20+ 个漏洞，包括认证绕过和数据库泄露。

**核心特性**：
- 全自主运营：一条命令启动完整渗透测试，Shannon 自动处理 2FA/TOTP 登录（包括 SSO）、浏览器导航、漏洞利用和报告生成
- 仅报告可复现 PoC：只有能被实际利用的漏洞才进入报告，不产生误报噪音
- 代码感知动态测试：分析源码指导攻击策略，再用实时浏览器/CLI 工具验证发现
- OWASP 漏洞覆盖：注入/XSS/SSRF/认证授权缺陷，更多类别开发中
- 并行处理：漏洞分析和利用阶段跨所有攻击类别并发运行

**技术栈**：TypeScript / 浏览器自动化 / Nmap / Subfinder / WhatWeb / Schemathesis / AGPL-3.0

**适用场景**：
- DevSecOps 团队在每次 Build 或发布时做自动化安全回归测试；
- 没有专职安全团队的中小型企业需要持续安全保障；
- 安全工程师想快速评估应用安全态势。

**一句话推荐**：
> "AI 编程时代的持续渗透测试工具，Claude Code 让你每天交付代码，Shannon 帮你每天做安全验证。"

---

### #02 koala73 / worldmonitor ⭐ 新上榜
**仓库**：https://github.com/koala73/worldmonitor
**Stars**：52,000 | **Forks**：8,300 | **语言**：TypeScript / JavaScript | **协议**：AGPL-3.0

**项目摘要**：
World Monitor 是一个实时全球情报仪表盘，把地缘政治监控、AI 新闻聚合和基础设施追踪整合在统一的态势感知界面里。核心能力：500+ 精选新闻源跨 15 个类别 AI 合成简报；双引擎地图（globe.gl 3D 地球仪 + deck.gl WebGL 平面地图）45 个数据层；覆盖 92 个股票交易所的金融雷达；跨军事/经济/灾难/升级信号的跨流关联分析。支持本地 AI（Ollama，无需 API 密钥），21 种语言含原生语言信息流，一个代码库派生 5 个站点变体（世界/科技/金融/大宗商品/积极信息）。

**核心特性**：
- 500+ 新闻源 × 15 类别：AI 合成情报简报，覆盖地缘政治/军事/经济/灾难/网络安全
- 45 数据层双引擎地图：3D 地球仪和 WebGL 平面地图，可视化全球实时事件分布
- 本地 AI 运行：支持 Ollama，全功能离线运行，不依赖任何 API 密钥
- 国家情报指数：基于 12 个信号类别的综合风险评分，覆盖 92 个股票交易所金融数据

**技术栈**：TypeScript / JavaScript / globe.gl / deck.gl / Ollama / Tauri 2 / AGPL-3.0

**适用场景**：
- 研究人员/记者追踪地缘政治事件和全球风险；
- 金融分析师监控多市场联动信号；
- 需要构建 AI 驱动情报仪表盘的企业用户。

**一句话推荐**：
> "开源版 Palantir，地缘政治 + 金融 + 灾害全覆盖，本地 AI 运行不需要 API 密钥，是目前最完整的开源全球情报仪表盘。"

---

### #03 open-webui / open-webui ⭐ 新上榜
**仓库**：https://github.com/open-webui/open-webui
**Stars**：134,000 | **Forks**：18,900 | **语言**：Python / JavaScript | **协议**：见仓库

**项目摘要**：
Open WebUI 是最流行的开源 LLM Web 交互界面，支持 Ollama 本地模型、OpenAI API 及任意 OpenAI 兼容接口。134k stars 是 GitHub 上 LLM 工具类项目中最高关注度之一。功能覆盖对话管理、RAG 知识库、MCP 工具、多模态支持、管道/插件扩展、用户权限管理，Docker 一键部署。今日重回 Python Trending 通常意味着触发了重大版本发布或功能更新。

**核心特性**：
- Ollama + OpenAI 双模式：一套界面同时管理本地 Ollama 模型和 OpenAI 兼容 API，无缝切换
- RAG 内置：本地知识库检索增强，上传文档直接进入对话上下文
- MCP 工具支持：集成 MCP 协议扩展 AI 能力边界
- 完整权限管理：多用户/多角色/多模型隔离，适合企业内部部署

**技术栈**：Python / JavaScript / Ollama / MCP / Docker / RAG

**适用场景**：
- 企业需要自托管 LLM 对话界面避免数据外泄；
- 开发者想统一管理多个本地/云端模型；
- 团队需要内置 RAG 知识库的 AI 工具。

**一句话推荐**：
> "134k stars 的开源 LLM 前端神器，自托管完整 AI 栈的首选，今日重回热榜通常代表有重大版本更新。"

---

### #04 langfuse / langfuse ⭐ 新上榜
**仓库**：https://github.com/langfuse/langfuse
**Stars**：25,800 | **Forks**：2,600 | **语言**：TypeScript | **协议**：见仓库（部分开源）

**项目摘要**：
Langfuse 是 YC W23 孵化的开源 LLM 工程平台，核心提供：LLM 应用可观测性（追踪 LLM 调用、检索、Agent 行动）、提示词版本管理、评估（LLM-as-a-judge/用户反馈/手动标注）、数据集管理和 LLM Playground。自托管 Docker 部署，全面集成 OpenTelemetry、LangChain、OpenAI SDK、LiteLLM 等生态，提供 Python/JS/TS 类型 SDK。555 次发布，迭代速度极快。

**核心特性**：
- LLM 可观测性：追踪 LLM 调用链路、embedding 和 Agent 行动，支持复杂日志和用户会话检查
- 提示词版本管理：集中管理和版本控制提示词，服务端/客户端双重缓存避免延迟
- 多维评估：LLM 评判/用户反馈/手动标注/自定义评估 Pipeline 四种模式可选
- Playground：直接从追踪中跳入 Playground 迭代有问题的提示词，缩短反馈循环

**技术栈**：TypeScript / OpenTelemetry / LangChain / OpenAI SDK / LiteLLM / Docker

**适用场景**：
- 团队的 LLM 应用上线后需要监控质量和性能；
- 提示词工程师需要版本管理和 A/B 测试；
- 需要建立 LLM 应用评估体系的工程团队。

**一句话推荐**：
> "YC W23 出品的 LLM 可观测性平台，从追踪到评估到提示词管理一体化，LLMOps 工具链的关键缺口正在被它填上。"

---

### #05 vercel-labs / skills ⭐ 新上榜
**仓库**：https://github.com/vercel-labs/skills
**Stars**：15,700 | **Forks**：1,300 | **语言**：TypeScript | **协议**：见仓库

**项目摘要**：
vercel-labs/skills 是 Vercel 官方发布的开放 Agent Skills 安装 CLI 工具（`npx skills`），提供统一命令在 60+ AI 编程工具上安装 Agent Skills。支持工具清单堪称史上最全：Claude Code、Codex、Cursor、Gemini CLI、Windsurf、GitHub Copilot、kimi-cli、OpenCode、Cline、Roo、Goose、Trae、Warp 等 60+ 工具。与 VoltAgent/awesome-agent-skills（内容目录）构成"内容 + 分发"双轮，Agent Skills 生态的最后一块基础设施拼图已经到位。

**核心特性**：
- 60+ AI 工具统一安装：一条 npx skills install 命令，自动检测当前已安装的 AI 工具并正确安装
- 完整 CLI 工具链：skills install / list / find / update / init / remove 全生命周期管理
- SKILL.md 标准格式：YAML frontmatter + Markdown，任何人都可以创建符合规范的技能
- skills.sh 发现平台：官方技能目录网站，可浏览和搜索公开技能

**技术栈**：TypeScript / npx / Node.js / SKILL.md 规范

**适用场景**：
- 所有 AI 编程工具用户，统一跨工具链安装和管理 Agent Skills；
- 开发者创建并发布自己的 Agent Skills 到社区；
- 企业统一管理内部 AI 开发规范技能。

**一句话推荐**：
> "Vercel 官方出品的 Agent Skills 安装 CLI，60+ AI 工具统一支持，一条 npx 命令搞定技能安装，Agent 生态分发层的最终答案。"

---

### #06 AIDC-AI / Pixelle-Video ⭐ 新上榜
**仓库**：https://github.com/AIDC-AI/Pixelle-Video
**Stars**：6,100 | **Forks**：952 | **语言**：Python | **协议**：Apache-2.0

**项目摘要**：
Pixelle-Video 是 AI 全自动短视频生成引擎，输入主题即可全自动生成完整视频：AI 智能创作解说词 → AI 生成配图（支持 FLUX/WAN 2.1 等生成模型）→ AI 合成语音（Edge-TTS/Index-TTS/ChatTTS）→ 添加 BGM → 输出视频。基于 ComfyUI 架构，原子能力灵活组合，支持数字人口播、图生视频、动作迁移等高级功能。Windows 一键整合包，支持 GPT/通义千问/DeepSeek/Ollama 等多种 LLM。

**核心特性**：
- 全自动视频生成：输入主题全自动完成文案→配图→语音→视频合成全流程
- 多种生产模式：数字人口播/图生视频/动作迁移/固定画面/自创脚本等 10+ 场景模板
- 灵活 AI 模型组合：GPT/通义/DeepSeek/Ollama 多 LLM + FLUX/WAN 生图 + 多 TTS 方案自由搭配
- ComfyUI 架构：原子能力可任意组合，可自定义工作流替换任意模型组件

**技术栈**：Python / ComfyUI / Edge-TTS / FLUX / WAN 2.1 / Apache-2.0

**适用场景**：
- 内容创作者想自动化生产短视频；
- 企业需要大批量生成产品介绍/知识科普类视频；
- 开发者想基于 ComfyUI 搭建自定义视频生产流水线。

**一句话推荐**：
> "输入主题全自动出短视频，ComfyUI 架构组件可替换，国产团队出品，短视频创作者的生产力工具。"

---

### #07 Alishahryar1 / free-claude-code ⭐ 新上榜
**仓库**：https://github.com/Alishahryar1/free-claude-code
**Stars**：3,700 | **Forks**：696 | **语言**：Python | **协议**：MIT

**项目摘要**：
free-claude-code 是一个让用户免费使用 Claude Code CLI 和 VS Code 扩展的代理层，不需要 Anthropic API 密钥。它通过接入多个免费/低成本 LLM 提供商（如 Ollama 本地模型、HuggingFace 等），把请求路由到 Claude Code 兼容接口，让用户体验 Claude Code 工作流而无需 API 费用。同时支持 Discord Bot 和 Telegram Bot 模式。作为社区对"高 API 成本"问题的直接响应，3.7k stars 体现了大量对成本敏感用户的需求。

**核心特性**：
- 零 API 费用使用 Claude Code：通过代理接入免费 LLM 提供商，绕过 Anthropic API 订阅
- 多平台支持：终端 CLI、VS Code 扩展、Discord Bot、Telegram Bot 四种使用方式
- 多提供商路由：可配置 Ollama 本地模型、HuggingFace 等多种后端
- npx 一键安装：无需 clone 仓库，直接 npx 全局安装使用

**技术栈**：Python / Ollama / Discord.py / Telegram / MIT

**适用场景**：
- API 成本敏感用户想体验 Claude Code 工作流；
- 开发者学习 AI 编程 Agent 工作模式而无需付费；
- 团队想在低成本环境下评估 Claude Code 适配性。

**一句话推荐**：
> "社区对 API 高成本的直接回应，免费使用 Claude Code CLI，3.7k stars 说明市场需求真实存在，但需注意模型能力会低于官方版本。"

---

### #08 Fincept-Corporation / FinceptTerminal（持续 Trending 第三日）
**仓库**：https://github.com/Fincept-Corporation/FinceptTerminal
**Stars**：10,735 | **Forks**：1,430 | **语言**：C++ / Python | **协议**：AGPL-3.0 / 商业双授权

**项目摘要**：
连续三日位居全语言 Trending 前列的开源 Bloomberg Terminal 替代品。C++20 原生 + Qt6 UI + 嵌入 Python 分析引擎，CFA 级量化分析 + AI 投资研究助手，个人/教育 AGPL-3.0 免费，企业购买商业授权。持续三日 Trending 说明金融分析领域存在对高质量开源工具的持续强烈需求。

**核心特性**：
- CFA 级量化分析：股票/债券/衍生品/宏观经济全覆盖
- AI 投资研究助手：集成 AI 辅助分析，支持自定义数据源
- 双授权模式：个人免费，企业商业授权

**技术栈**：C++20 / Qt6 / Python（嵌入）/ Docker

**一句话推荐**：
> "连续三日 Trending 的开源 Bloomberg 替代，说明金融分析工具的开源需求确实是持续性刚需。"

---

### #09 HKUDS / RAG-Anything（持续）
**仓库**：https://github.com/HKUDS/RAG-Anything
**Stars**：16,474 | **Forks**：1,976 | **语言**：Python | **协议**：MIT

**项目摘要**：
香港大学出品的多模态 RAG 框架，支持 PDF/Office/图片等全格式文档，专门为图表、表格、数学公式设计独立处理器，自动构建多模态知识图谱，完整 Pipeline 从文档解析到问答全覆盖。

**核心特性**：
- 全格式支持：PDF/Word/Excel/PPT/图片直接输入
- 多模态专项处理：图表/表格/公式各有专用分析器
- 多模态知识图谱：跨模态实体关系自动抽取

**技术栈**：Python / MinerU / 知识图谱 / 多模态检索 / MIT

**一句话推荐**：
> "处理含图表公式的复杂文档 RAG 首选，香港大学出品，学术严谨 + 工程完整。"

---

### #10 sansan0 / TrendRadar（持续）
**仓库**：https://github.com/sansan0/TrendRadar
**Stars**：53,200 | **Forks**：23,491 | **语言**：Python | **协议**：GPL-3.0

**项目摘要**：
多平台热点聚合（微博/抖音/知乎/B 站/GitHub 等）+ AI 过滤翻译分析 + 手机直推一体化方案，Docker 部署，微信/飞书/钉钉/Telegram/Slack/邮件多渠道推送。

**核心特性**：
- 多平台聚合 + AI 三级处理：过滤→翻译→分析简报流水线
- MCP 架构：可接入 AI 对话系统做情感分析
- Docker 一键部署 + 多渠道推送

**技术栈**：Python / Docker / MCP / LLM / RSS

**一句话推荐**：
> "多平台 AI 热点过滤器，部署一次告别碎片化刷热点。"

---

### #11 zilliztech / claude-context（持续）
**仓库**：https://github.com/zilliztech/claude-context
**Stars**：6,141 | **Forks**：539 | **语言**：TypeScript | **协议**：MIT

**项目摘要**：
MCP 插件，把代码库索引到 Milvus 向量数据库，让 Claude Code 等 AI Agent 通过自然语言语义搜索整个代码库，降低 Token 成本。混合 BM25 + Dense Vector，AST 分块，增量 Merkle Tree 索引。

**一句话推荐**：
> "Claude Code 大型代码库必装 MCP 插件，百万行代码库也能让 AI 真正看懂。"

---

### #12 ruvnet / RuView（持续）
**仓库**：https://github.com/ruvnet/RuView
**Stars**：48,607 | **Forks**：6,487 | **语言**：Python | **协议**：MIT ⚠️ Beta

**项目摘要**：
用 ESP32 WiFi 设备的 CSI 信号做无摄像头人体姿态估计、生命体征监测和存在感知，17 种感知应用场景，Beta 版本，精度依赖多节点部署。

**一句话推荐**：
> "WiFi 信号替代摄像头做室内感知，老年护理/隐私场所强需求，Beta 阶段生产前请充分测试。"

---

## 编程语言分布

| 语言 | 项目数 | 占比 | 代表项目 |
|---|---|---|---|
| Python | 5 | 41.7% | open-webui / RAG-Anything / TrendRadar / Pixelle-Video / RuView |
| TypeScript | 3 | 25.0% | shannon / langfuse / vercel-labs/skills |
| JavaScript / TS | 1 | 8.3% | worldmonitor |
| C++ / Python | 1 | 8.3% | FinceptTerminal |
| Jupyter Notebook | 1 | 8.3% | ai-agents-for-beginners（今日替换出） |
| Python（代理） | 1 | 8.3% | free-claude-code |

---

## GitHub Explore 精选

今日 Explore 新项目多，以下为值得额外关注的亮点：

1. **KeygraphHQ/shannon** — 今日全语言 Trending 新晋，AI 自主渗透测试，白盒安全测试新范式 · ⭐39.9k
2. **koala73/worldmonitor** — 52k stars 开源全球情报仪表盘，Palantir 开源替代 · 本地 AI 运行
3. **open-webui/open-webui** — 134k stars LLM Web UI 重回热榜，可能触发重大版本更新 · Ollama/MCP 全支持
4. **langfuse/langfuse** — YC W23 LLM 可观测性平台，LLMOps 必备 · 自托管 Docker 一键部署 · ⭐25.8k
5. **vercel-labs/skills** — Vercel 官方 Agent Skills CLI，60+ AI 工具统一安装 · ⭐15.7k
6. **Z4nzu/hackingtool** — 黑客工具集合，安全工具再次进入 Trending，AI 安全浪潮延续 · Python
7. **kyegomez/swarms** — 企业级多 Agent 编排框架 · 6.5k stars · 20+ Multi-Agent 架构可选
8. **davila7/claude-code-templates** — Claude Code 提示词模板合集，今日进入 Python Trending

---

## 渲染备注

- 本文为 HTML 日报生成的内容底稿
- Stars 数据为抓取时近似值
- 含 ⚠️ Beta 标注的项目（RuView）请在生产环境谨慎评估
- Shannon 为 AGPL-3.0 协议，商业用途需谨慎评估许可证条款
