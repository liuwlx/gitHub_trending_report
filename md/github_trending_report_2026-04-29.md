# GitHub Trending 日报 · 2026-04-29

> 数据来源：GitHub Trending + GitHub Explore  
> 生成时间：2026-04-29  
> Top 12 按总 Stars 数量排序

---

## 📊 概览统计

| 指标 | 数值 |
|------|------|
| Trending 项目 | 12 |
| 累计 Stars（12 项）| ~1.34M |
| 涉及编程语言 | 5 种 |
| AI 相关项目 | 6 |

---

## 🔍 今日洞察

### 1. 微软 VibeVoice 开源前沿语音 AI 全家桶
microsoft/VibeVoice 是微软开源的语音 AI 研究框架，包含三个模型：VibeVoice-ASR（60分钟长音频单次识别，含说话人分离/时间戳）、VibeVoice-TTS（90分钟多说话人合成，已在 ICLR 2026 入选 Oral）、VibeVoice-Streaming（0.5B实时TTS，300ms首包延迟）。三模型均已开源到 Hugging Face，支持 50+ 语言，覆盖从转录到合成的完整语音 AI 链条。

### 2. Claude Code 生态工具链持续爆发
今日 Trending 中三个项目直接服务于 Claude Code 生态：davila7/claude-code-templates（100+ 组件配置模板 + 监控面板）、mattpocock/skills（真实工程师日常技能合集）、Alishahryar1/free-claude-code（零成本代理方案）。Claude Code 的"第三方配件市场"正在形成，工具链生态快速标准化。

### 3. 资源型仓库三巨头同日上榜
free-programming-books（386k）、public-apis（428k）、system-design-primer（346k）三大经典资源库同日出现在 Trending，累计已超过 115 万 Stars。这类"永恒价值"仓库每隔一段时间就会被新一批开发者发现，在 GitHub 生态中具有持久的传播生命力。

### 4. Quarkdown：Markdown 进化为可编程文档语言
iamgio/quarkdown 把 Markdown 扩展成一种带有函数调用、变量、条件渲染的文档编程语言，一套源文件可导出为：论文 PDF（via paged.js）、交互式幻灯片（via reveal.js）、静态网站（like Notion/Obsidian）、Wiki 文档库。对比 LaTeX 的复杂语法，quarkdown 保持了 Markdown 的可读性，同时具备了 LaTeX 的文档表达能力。

---

## 🔥 今日热门 Top 12（按总 Stars 排序）

---

### #1 public-apis / public-apis
- **链接**: https://github.com/public-apis/public-apis
- **描述**: A collective list of free APIs.
- **Stars**: 427,792 | **Forks**: 46,732
- **语言**: Python / Markdown
- **Topics**: api, list, free-api, public-api

#### 📖 项目摘要
public-apis 是目前 GitHub Stars 最多的 API 资源合集之一，收录了数百个免费可用的公开 API，按类别分组（动物、天气、地图、金融、游戏、新闻、科学等 40+ 类别），每个 API 均标注了是否需要认证、HTTPS 支持、CORS 支持等信息。

#### ✨ 核心特性
- 40+ 分类，数百个免费 API 完整收录
- 每条目标注 Auth / HTTPS / CORS 三项属性，快速筛选
- 社区维护，持续更新最新可用 API
- 提供配套 Python 验证脚本，确保链接有效性
- 覆盖原型开发、学习测试、黑客马拉松等全场景

#### 🔧 技术栈
Markdown 文档列表、Python（验证脚本）

#### 🎯 适用场景
想快速找到免费 API 做原型验证的开发者；黑客马拉松参赛者；学生练习 API 调用；寻找数据源的研究人员。

#### 💬 一句话推荐
"免费 API 的黄页——收藏了就等于收藏了一个做不完的 side project 仓库。"

---

### #2 EbookFoundation / free-programming-books
- **链接**: https://github.com/EbookFoundation/free-programming-books
- **描述**: 📚 Freely available programming books.
- **Stars**: 386,479 | **Forks**: 66,153
- **语言**: Markdown
- **Topics**: books, programming, education, free, ebook

#### 📖 项目摘要
free-programming-books 是 GitHub 最大的开源编程书籍资源合集，收录了全球数千本免费编程书籍、课程、视频、播客和互动教程，涵盖 100+ 编程语言和技术栈，并提供 30+ 语言版本的翻译目录，为开发者提供零成本自学路径。

#### ✨ 核心特性
- 数千本免费编程书籍，涵盖 100+ 编程语言
- 多媒体形式：书籍 + 在线课程 + 视频教程 + 播客 + 互动编程
- 30+ 语言版本，国际化覆盖广
- 社区持续贡献，每周都有新增
- 适合各个技术层级，从入门到进阶

#### 🔧 技术栈
Markdown 纯文档资源库

#### 🎯 适用场景
自学编程的学生；寻找特定技术深度资料的工程师；教育机构整理参考资料；任何不想花钱买书的开发者。

#### 💬 一句话推荐
"66k Forks 说明了一切——全球开发者人手一份的免费编程书单。"

---

### #3 donnemartin / system-design-primer
- **链接**: https://github.com/donnemartin/system-design-primer
- **描述**: Learn how to design large-scale systems. Prep for the system design interview. Includes Anki flashcards.
- **Stars**: 345,655 | **Forks**: 55,816
- **语言**: Python / Markdown
- **Topics**: system-design, interview, scalability, distributed-systems, architecture

#### 📖 项目摘要
system-design-primer 是最权威的系统设计学习资源之一，涵盖从 DNS/CDN 到 数据库分片、消息队列、缓存、负载均衡、微服务的完整知识体系，并提供配套的 Anki 记忆卡片用于备考。是 FAANG 等大厂系统设计面试的必备参考。

#### ✨ 核心特性
- 完整系统设计知识图谱：可扩展性、高可用、数据库选型、缓存策略等全覆盖
- 真实案例：Twitter/Facebook/Amazon 等真实系统设计拆解
- 配套 Anki 记忆卡片，结构化备考
- 中文等多语言翻译版本
- Python 代码示例辅助理解数据结构和算法

#### 🔧 技术栈
Markdown + Python（代码示例）、Anki（记忆卡）

#### 🎯 适用场景
准备大厂系统设计面试的工程师；希望提升系统架构思维的后端开发者；技术团队内部架构培训。

#### 💬 一句话推荐
"系统设计面试的圣经——没刷完这个就去面 FAANG 的，都是在裸考。"

---

### #4 microsoft / VibeVoice
- **链接**: https://github.com/microsoft/VibeVoice
- **描述**: Open-Source Frontier Voice AI. 微软开源的前沿语音 AI 全栈框架，含 ASR/TTS/实时流式三大模型。
- **Stars**: 44,254 | **Forks**: 4,947
- **语言**: Python
- **Topics**: speech-recognition, text-to-speech, voice-ai, asr, tts, microsoft, open-source

#### 📖 项目摘要
VibeVoice 是微软开源的前沿语音 AI 研究框架，包含三大组件：① VibeVoice-ASR：统一语音识别模型，单次处理 60 分钟连续音频，输出结构化转录（谁说/何时/说什么）；② VibeVoice-TTS：长篇多说话人语音合成，支持 90 分钟 4 人对话合成（ICLR 2026 Oral）；③ VibeVoice-Streaming：0.5B 轻量实时TTS，约 300ms 首包延迟，支持流式文本输入。

#### ✨ 核心特性
- VibeVoice-ASR：60分钟单次处理、说话人分离 + 时间戳、自定义热词、50+ 语言、已入 HuggingFace Transformers
- VibeVoice-TTS：90分钟长篇生成、4 说话人同场对话、富表现力语音、中英文多语言
- VibeVoice-Streaming：0.5B 小模型、300ms 首包、流式文本输入、约 10 分钟长音频生成
- 全部模型均已上线 Hugging Face，支持 vLLM 高速推理
- 开放 Fine-tuning 代码，支持垂直领域定制

#### 🔧 技术栈
Python、PyTorch、HuggingFace Transformers、vLLM（推理加速）、Colab Demo

#### 🎯 适用场景
会议录音自动转录与说话人分离；播客/有声书多人对话语音合成；实时语音助手；垂直领域语音数据标注与合成。

#### 💬 一句话推荐
"微软一次性开源了 ASR + TTS + 实时流式的完整语音 AI 链条，而且都支持 60/90 分钟长音频——语音 AI 领域的基础设施级开源。"

---

### #5 mattpocock / skills
- **链接**: https://github.com/mattpocock/skills
- **描述**: Skills for Real Engineers. Straight from my .claude directory.
- **Stars**: 35,599 | **Forks**: 2,793
- **语言**: Markdown / TypeScript
- **Topics**: claude-code, agent-skills, ai-engineering, cursor, codex

#### 📖 项目摘要
mattpocock/skills 是 TypeScript 专家 Matt Pocock（Total TypeScript 创始人）从自己真实 .claude 目录中提炼的 Agent Skills 合集，代表真实工程工作流。包含规划设计、代码开发、工具配置、写作知识四大类。每个技能可通过 `npx skills@latest add` 一键安装，兼容 Claude Code / Cursor / Codex。

#### ✨ 核心特性
- 规划设计：to-prd、to-issues、grill-me、design-an-interface（并行子代理多方案）
- 开发类：tdd（红绿重构）、triage-issue、improve-codebase-architecture（DDD 语言）
- 工具类：setup-pre-commit（Husky + lint-staged）、git-guardrails-claude-code
- 写作类：write-a-skill、edit-article、ubiquitous-language、obsidian-vault

#### 🔧 技术栈
Markdown + YAML frontmatter、TypeScript、Claude Code / Cursor / Codex 兼容

#### 🎯 适用场景
Claude Code / Cursor 重度用户；想把优秀工程师 AI 工作流拿来就用的开发者；团队标准化 AI 编程实践。

#### 💬 一句话推荐
"Matt Pocock 把他每天真正用的 AI 编程技能全开源了——这不是教程，是直接可用的工作流。"

---

### #6 abhigyanpatwari / GitNexus
- **链接**: https://github.com/abhigyanpatwari/GitNexus
- **描述**: GitNexus: The Zero-Server Code Intelligence Engine — 浏览器端代码知识图谱 + Graph RAG Agent。
- **Stars**: 32,437 | **Forks**: 3,681
- **语言**: TypeScript
- **Topics**: knowledge-graph, code-intelligence, graph-rag, browser-based, zero-server, mcp

#### 📖 项目摘要
GitNexus 是完全在浏览器端运行的代码知识图谱引擎，无需后端服务器。拖入 GitHub 仓库地址或 ZIP 文件，自动解析代码结构，生成交互式依赖知识图谱，内置 Graph RAG Agent 供自然语言提问。核心解决 Cursor / Claude Code 等不真正理解代码依赖关系、频繁引发级联破坏的问题。

#### ✨ 核心特性
- 零服务器：完全客户端，数据不离开浏览器
- 知识图谱：函数/类/模块依赖可视化，360° 符号视图
- Graph RAG Agent：自然语言查询，影响分析、变更检测、批量重命名
- MCP 集成：可作为 Claude Code / Cursor 代码理解增强层
- 支持 10+ 编程语言（Python / TypeScript / Java / Go / Rust 等）

#### 🔧 技术栈
TypeScript、浏览器端静态分析、Graph RAG、Cypher 查询、MCP 协议

#### 🎯 适用场景
想让 AI 编码助手真正理解代码结构的开发者；大型代码库依赖梳理；架构重构前的影响面分析。

#### 💬 一句话推荐
"把整个代码库变成可问答的知识图谱，让 AI 改代码之前先搞清楚'改这里会牵连哪里'。"

---

### #7 davila7 / claude-code-templates
- **链接**: https://github.com/davila7/claude-code-templates
- **描述**: CLI tool for configuring and monitoring Claude Code. 100+ Claude Code 组件模板 + 实时分析监控。
- **Stars**: 26,041 | **Forks**: 2,608
- **语言**: TypeScript / Shell
- **Topics**: claude-code, templates, cli, agents, mcp, hooks, monitoring

#### 📖 项目摘要
claude-code-templates 是一个 npx CLI 工具，提供 100+ Claude Code 配置组件（Agent、Command、Setting、Hook、MCP），可通过交互式菜单或命令行参数一键安装到当前项目。配套的 aitmpl.com 网站提供可视化浏览界面。额外附带四个开发工具：实时分析面板、对话监控（支持 Cloudflare Tunnel 远程访问）、健康检查诊断、插件管理面板。

#### ✨ 核心特性
- 100+ 组件：Agent（代码审查/前端开发等）、Command（测试生成/Bundle 优化/安全检查等）
- Hook 支持：git pre-commit 校验等
- MCP 集成：数据库/GitHub/开发工具等
- 四大监控工具：Analytics / Chats Monitor / Health Check / Plugin Dashboard
- npx 零安装，`--yes` 参数支持脚本化批量配置

#### 🔧 技术栈
TypeScript / Node.js（CLI）、Shell、Cloudflare Tunnel（远程访问）

#### 🎯 适用场景
Claude Code 项目初始化快速配置；团队统一 Claude Code 工作环境；监控和分析 Claude Code 使用情况；开发中快速插入最佳实践钩子。

#### 💬 一句话推荐
"Claude Code 的 App Store + 仪表盘——一条命令把 100+ 最佳实践配置全装好。"

---

### #8 Alishahryar1 / free-claude-code
- **链接**: https://github.com/Alishahryar1/free-claude-code
- **描述**: Use claude-code for free in the terminal, VSCode extension or via discord.
- **Stars**: 17,161 | **Forks**: 2,412
- **语言**: Python
- **Topics**: claude-code, free, proxy, nvidia-nim, openrouter, local-llm, ollama

#### 📖 项目摘要
free-claude-code 是轻量级 Python 代理服务（监听 :8082），将 Claude Code CLI 或 VSCode 插件发出的 Anthropic API 请求透明转发给免费/低价提供商：NVIDIA NIM（40 req/min 免费）、OpenRouter（含免费模型）、DeepSeek（Anthropic 格式兼容）、LM Studio、llama.cpp、Ollama（完全本地）。无需 Anthropic API Key。

#### ✨ 核心特性
- 零 API Key：接入 NVIDIA NIM 或 OpenRouter 免费模型即可跑 Claude Code
- 6 类后端：NVIDIA NIM / OpenRouter / DeepSeek / LM Studio / llama.cpp / Ollama
- 本地化优化：5 类轻量请求本地响应，不消耗 API 配额
- Thinking Tokens：`<think>` 标签 → Claude 原生 thinking blocks 转换
- Discord Bot + Telegram 支持

#### 🔧 技术栈
Python、FastAPI/aiohttp、Anthropic Messages API、SSE 流式输出

#### 🎯 适用场景
希望零成本使用 Claude Code 的开发者；需要接入本地 LLM 的离线/隐私场景；OpenRouter 用户直连 Claude Code 工具链。

#### 💬 一句话推荐
"拦截 Claude Code 的 API 请求，转发给免费的 NVIDIA NIM 或本地 Ollama——不花一分钱也能跑 Claude Code。"

---

### #9 iamgio / quarkdown
- **链接**: https://github.com/iamgio/quarkdown
- **描述**: 🪐 Markdown with superpowers: from ideas to papers, presentations, websites, books, and knowledge bases.
- **Stars**: 11,665 | **Forks**: 305
- **语言**: Kotlin
- **Topics**: markdown, document, presentation, latex-alternative, programmable, kotlin

#### 📖 项目摘要
Quarkdown 将 Markdown 扩展为一种可编程的文档语言：在保留 Markdown 可读性的同时，引入函数调用、变量、条件渲染、自定义函数等编程语言特性。一套 `.qd` 源文件可输出为多种目标格式：连续流网站（类 Notion/Obsidian）、分页 PDF 论文（via paged.js）、交互式幻灯片（via reveal.js）、Wiki 文档库（via 内置文档引擎）。

#### ✨ 核心特性
- 可编程 Markdown：函数调用（.function_name）、变量、条件、循环
- 多目标输出：.doctype {plain/paged/slides/docs} 一行切换
- HTML + PDF 双导出，全文档类型支持
- LaTeX 对比：更短语法达到同等文档表达力
- 跨平台安装：脚本安装 / Homebrew / Scoop / GitHub Actions

#### 🔧 技术栈
Kotlin（核心实现）、paged.js（PDF 排版）、reveal.js（幻灯片）、HTML/CSS（渲染层）

#### 🎯 适用场景
写学术论文但不想学 LaTeX 的研究人员；做技术演讲同时产出文档的工程师；用 Markdown 管理知识库但需要动态内容的团队。

#### 💬 一句话推荐
"Markdown 遇见 LaTeX 的表达力——一份源文件，变成论文、幻灯片、网站或 Wiki，选你所需。"

---

### #10 HunxByts / GhostTrack
- **链接**: https://github.com/HunxByts/GhostTrack
- **描述**: Useful tool to track location or mobile number.
- **Stars**: 10,309 | **Forks**: 1,460
- **语言**: Python
- **Topics**: osint, geolocation, tracking, phone-tracking, python

#### 📖 项目摘要
GhostTrack 是一个基于 Python 的 OSINT 地理位置追踪工具，支持通过手机号码进行号码信息查询和地理位置大致定位，以及通过发送追踪链接来获取目标设备的实时 GPS 位置。主要面向安全研究学习和授权渗透测试场景。

#### ✨ 核心特性
- 手机号码信息查询（运营商、国家、时区等）
- 追踪链接生成与位置捕获
- 简单 Python 环境，依赖少
- Kali Linux / Termux 兼容

#### 🔧 技术栈
Python、Phonenumbers 库、Ngrok/类似隧道工具

#### 🎯 适用场景
OSINT 安全研究学习；渗透测试工程师学习地理位置信息收集技术。（仅限合法授权场景）

#### 💬 一句话推荐
"OSINT 工具箱的位置追踪模块——学习信息安全的好材料，使用时请遵守法律。"

---

### #11 ComposioHQ / awesome-codex-skills
- **链接**: https://github.com/ComposioHQ/awesome-codex-skills
- **描述**: A curated list of practical Codex skills for automating workflows across the Codex CLI and API.
- **Stars**: 3,667 | **Forks**: 242
- **语言**: Markdown
- **Topics**: codex, openai, agent-skills, automation, workflow

#### 📖 项目摘要
awesome-codex-skills 是 Composio 精选的实用 Codex 技能合集，覆盖开发工具、生产力、通讯写作、数据分析、元工具五大类。每个技能为一个 SKILL.md 文件，包含说明和分步骤指导，支持接入 Composio 后可对接 1000+ 应用执行自动化动作（发邮件、建 Issue、发 Slack 等）。

#### ✨ 核心特性
- 五大类技能：开发工具 / 生产力 / 通讯写作 / 数据分析 / 元工具
- 标准 SKILL.md 格式，即插即用
- Composio 接入后可触发 1000+ 应用真实动作
- 活跃贡献社区，持续扩展

#### 🔧 技术栈
Markdown（SKILL.md 定义）、Composio（动作执行层）、OpenAI Codex API

#### 🎯 适用场景
想为 Codex 添加真实动作能力的开发者；希望 Codex 不只生成文本、还能发邮件/建 Issue 的团队。

#### 💬 一句话推荐
"让 Codex 从'生成文本'进化到'执行任务'——发邮件、建 Issue、发 Slack，1000+ 应用任你选。"

---

### #12 CJackHwang / ds2api
- **链接**: https://github.com/CJackHwang/ds2api
- **描述**: Deepseek to API: A lightweight, high-performance full-stack middleware converting client protocols to universal APIs.
- **Stars**: 2,209 | **Forks**: 633
- **语言**: Go / TypeScript
- **Topics**: deepseek, api, middleware, proxy, openai, claude, google, vercel

#### 📖 项目摘要
ds2api 是一个轻量高性能的全栈中间件，将 DeepSeek 客户端协议转换为通用 API 格式，同时兼容 OpenAI、Claude、Google API 格式。支持多账号轮换（负载均衡）、编译后的单二进制部署、Vercel Serverless 部署、Docker 容器化，专为解决 DeepSeek 客户端协议与标准 API 格式之间的转换问题而设计。

#### ✨ 核心特性
- 多协议兼容：同时兼容 OpenAI / Claude / Google API 格式
- 多账号轮换：内置负载均衡，防单账号限速
- 多部署方式：编译二进制 / Vercel Serverless / Docker
- 高性能：Go 核心，低延迟高并发
- 轻量级：无外部依赖，单文件部署

#### 🔧 技术栈
Go（后端核心）、TypeScript（前端/配置界面）、Docker、Vercel Serverless

#### 🎯 适用场景
需要将 DeepSeek 接入现有 OpenAI SDK 的开发者；多账号 DeepSeek API 负载均衡；个人/小团队的 API 网关自建。

#### 💬 一句话推荐
"把 DeepSeek 换上 OpenAI/Claude 的马甲——现有 SDK 一行不改，直接对接。"

---

## 📊 编程语言分布

| 语言 | 项目数 | 占比 | 代表项目 |
|------|--------|------|---------|
| Python | 5 | 42% | public-apis, system-design-primer, VibeVoice, free-claude-code, GhostTrack |
| Markdown | 3 | 25% | free-programming-books, mattpocock/skills, awesome-codex-skills |
| TypeScript | 2 | 17% | GitNexus, claude-code-templates |
| Kotlin | 1 | 8% | quarkdown |
| Go | 1 | 8% | ds2api |

---

## 🌐 GitHub Explore 精选

### 1. fspecii / ace-step-ui
- **链接**: https://github.com/fspecii/ace-step-ui
- **Stars**: 1,488 | **Forks**: 244
- **简介**: 🎵 The Ultimate Open Source Suno Alternative — Professional UI for ACE-Step 1.5 AI Music Generation. Free, local, unlimited. 本地化运行 ACE-Step 1.5 AI 音乐生成模型的开源 Web UI，Suno 的免费平替，无次数限制。

### 2. GitHub Explore：Voice & Speech
- **简介**: 与今日 microsoft/VibeVoice 登榜呼应，GitHub Explore 语音 AI 相关项目持续受关注，开源语音基础设施迎来新一波建设潮。

### 3. GitHub Trending 特别观察：资源型三巨头同日上榜
- **简介**: public-apis（427k）、free-programming-books（386k）、system-design-primer（346k）同日出现在 Trending 榜，累计 Stars 超 115 万，反映每季度的"新人涌入周期"——新加入 GitHub 的开发者集中发现了这批永恒价值仓库。

---

*报告生成：2026-04-29 | skill-github-trending-report v0.8.0*
