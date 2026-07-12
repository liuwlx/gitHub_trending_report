# GitHub Trending 日报内容底稿

## Meta

- Report Date: 2026-04-18
- Generated At: 2026-04-18 13:20:44
- Output Markdown: E:\workerspace\daily\task\github\github_trending_report_2026-04-18.md
- Planned HTML: E:\workerspace\daily\task\github\github_trending_report_2026-04-18.html
- Fixed Base Template: E:\workerspace\daily\task\.codex\skills\skill-github-trending-report\reference\fixedBaseTemplate_2026-03-16.html
- User Rules: E:\workerspace\daily\task\.codex\skills\skill-github-trending-report\reference\user-rules.md
- Sources:
  - GitHub Trending
  - GitHub Explore
  - Repo README / About / Homepage
  - GitHub REST API repo metadata
  - Public web pages when repo self-description was insufficient

## Page Intent

- 今日主线：今天最值得看的，不是某个单一模型，而是一批正在把 AI 从“聊天助手”推进成“可执行工作台”的项目。
- 适合谁阅读：正在使用 AI 编码、Agent 工作流、浏览器自动化、多模态生产工具的开发者、技术负责人和产品平台团队。
- 页面重点：先帮读者 30 秒内看懂今天的主线，再用 Top 12 告诉你哪些项目值得点开、为什么值得点开、第一眼该看哪里。
- 需要诚实降级说明的地方：GitHub Explore 与今日 Trending 重合度很高，更适合做延伸阅读清单，而不是另一套完全不同的发现列表。

## Stats

- Trending 项目数：15
- 今日累计新增 Stars：9294
- 编程语言数：6
- AI 相关项目数：15

## Editorial Insights

### Insight 1
- Title: 今天最热的不是某个模型，而是 Agent 的工作流基础设施
- Body: `superpowers`、`openai-agents-python`、`chrome-devtools-mcp`、`craft-agents-oss`、`GenericAgent` 这一批项目指向的是同一个问题：团队已经不满足于“AI 会写几段代码”，而是开始要它能拆任务、接工具、看运行结果、长期记住上下文、稳定把活干完。

### Insight 2
- Title: “能操作环境”正在取代“能回答问题”成为新的竞争点
- Body: `chrome-devtools-mcp` 把浏览器调试和性能分析接给 Agent，`GenericAgent` 直接把本地电脑、浏览器、ADB 设备纳进控制面，`omi` 则把屏幕和语音流并入上下文。今天的热点不是多会说，而是谁真正碰得到真实环境。

### Insight 3
- Title: 本地可用、立即上手的多模态工具开始抢走注意力
- Body: `voicebox` 和 `omi` 代表的是另一条很现实的路线：不先讲宏大愿景，先把声音、会议、屏幕、摘要这些每天都能用到的能力做成产品。它们热起来，说明大家对“能今天装上就开始用”的 AI 工具越来越买账。

### Insight 4
- Title: Explore 今天更像“同步推荐”，不是另一张完全不同的榜
- Body: 今天 Explore 上能看到的大部分重点仓库，和 Trending 主榜高度重合。它的价值更像是帮你做二次筛选和延伸点击，而不是提供另一条截然不同的开源发现路径。

## Top Projects

### Rank 01 - obra/superpowers
- Repo URL: https://github.com/obra/superpowers
- Tagline: 把 AI 编码经验沉淀成可复用技能和开发方法论
- Stars: 157990
- Stars Today: 1713
- Forks: 13747
- Language: Shell
- License: MIT
- Homepage:
- Topics: agent-workflow, spec-first, tdd, multi-agent, developer-productivity
- 技术栈: Shell, Markdown, Claude Code, Cursor, Codex, Gemini CLI, TDD
- Why It Matters Today: 它不是单个插件或命令，而是一整套“让编码 Agent 少走弯路”的工作方式；今天 Agent 工作流类项目爆发时，它是最成熟也最具代表性的样本。
- 项目摘要: `superpowers` 本质上是一套给编码 Agent 用的软件开发方法论和技能库，不只是“帮你多写点 prompt”。它最想解决的是：团队明明已经在用 Claude Code、Codex、Cursor，但输出依然不稳定、流程不可复用、复杂任务一容易就跑偏。README 给出的路径很清楚：先把需求聊清楚，再产出可读的 spec，再拆计划、做 TDD、派子代理执行、最后审查结果。对想把 AI 编码从“偶尔试试”变成“团队可复用能力”的人，这个项目很值得细看。
- 核心特性:
  1. 它把 spec-first、TDD、系统化调试、子代理分工这些经验做成可组合技能，不用每次从头教 Agent。
  2. 适配 Claude Code、Cursor、Codex、Gemini CLI 等多种编码 Agent，迁移时不需要整套方法全部重来。
  3. 强调“先想清楚再动手”，能明显降低 AI 在长任务里越写越偏、越改越乱的概率。
- 适用场景: 适合已经开始重度使用 AI 编码、想把个人经验升级成团队工作流的开发者和技术负责人。第一次试用时，最值得先看的不是全部技能，而是 `How it works`、TDD 和调试相关技能，看它能不能解决你当前最痛的流程问题。如果你只是想找一个开箱即用的成品应用，而不是建立自己的 AI 开发方法，它会显得偏重。
- 一句话推荐: 今天最值得点开它的原因，是它能帮你判断“AI 编码到底该怎么管起来才不失控”；第一次打开先看工作流主线和最常用的 2 到 3 个技能，5 分钟内就能看出它是不是你团队缺的那块方法论。
- Evidence Notes: README 明确写到它会先澄清需求、生成 spec、给出实现计划、强调红绿重构 TDD，并通过 subagent-driven-development 推进执行。
- Honest Caveat: 它更像方法论和技能体系，不是“一键安装就马上更强”的产品；要吃到红利，团队得愿意接受流程约束。

### Rank 02 - ChromeDevTools/chrome-devtools-mcp
- Repo URL: https://github.com/ChromeDevTools/chrome-devtools-mcp
- Tagline: 把真实 Chrome 浏览器接入编码 Agent 的调试和自动化能力
- Stars: 35931
- Stars Today: 196
- Forks: 2195
- Language: TypeScript
- License: Apache-2.0
- Homepage: https://npmjs.org/package/chrome-devtools-mcp
- Topics: browser, chrome, chrome-devtools, debugging, devtools, mcp, mcp-server, puppeteer
- 技术栈: TypeScript, MCP, Puppeteer, Chrome DevTools, Network Analysis, Performance Tracing
- Why It Matters Today: 今年很多 Agent 都会“写前端代码”，但真正难的是看运行结果、查网络请求、抓性能瓶颈；这个项目恰好补上了这块执行环境能力。
- 项目摘要: `chrome-devtools-mcp` 是一个 MCP server，让 Claude、Gemini、Cursor、Copilot 这类编码 Agent 直接控制并检查一个真实运行中的 Chrome 浏览器。它解决的问题很实际：AI 会改代码，不代表它真的知道页面为什么白屏、接口为什么报错、性能为什么抖动。有了这个桥，Agent 不只是“想象浏览器”，而是能读控制台、看网络、抓 trace、做可靠自动化。对前端开发、端到端验证、页面性能排查来说，它的价值非常直接。
- 核心特性:
  1. 能把性能 trace、网络请求、控制台错误、截图这类原本需要手动打开 DevTools 的工作直接交给 Agent。
  2. 不是只做脚本自动化，还能给出调试和性能分析层面的可执行信息，更适合实际开发流程。
  3. 基于 MCP 和 Puppeteer，接入思路清晰，适合并入现有 Agent 工具链。
- 适用场景: 适合前端工程师、测试工程师、做网页自动化和浏览器调试的 Agent 工作流团队。第一次试用，先看 tool reference 和 troubleshooting，确认它能否覆盖你最常见的调试动作。如果你做的是纯后端任务、CLI 工程或完全不碰浏览器的系统，这个项目的收益会明显下降。
- 一句话推荐: 今天值得看它，因为它回答了“Agent 到底能不能真的看懂浏览器”这个关键问题；第一次打开先看支持哪些调试动作，再看性能和网络能力，立刻就能判断它是不是你工作流缺的那根线。
- Evidence Notes: README 明确写到它支持 live Chrome 控制、performance insights、network analysis、screenshots、console messages 和 reliable automation。
- Honest Caveat: 它解决的是浏览器观察与控制，不会替你自动修好所有前端问题；要稳定用起来，还需要你自己的调试流程配合。

### Rank 03 - Lordog/dive-into-llms
- Repo URL: https://github.com/Lordog/dive-into-llms
- Tagline: 面向中文读者的“动手学大模型”编程实践教程
- Stars: 31648
- Stars Today: 944
- Forks: 3860
- Language: Jupyter Notebook
- License:
- Homepage:
- Topics: llm-tutorial, chinese-learning, notebooks, hands-on-practice
- 技术栈: Jupyter Notebook, Python, LLM Fundamentals, Training, Inference, Tutorials
- Why It Matters Today: 在一堆“直接上 Agent”的项目中，它代表另一种真实需求: 团队仍然需要能真正把人带进门的高质量中文学习路径。
- 项目摘要: `dive-into-llms` 本质上是一套代码驱动的大模型实践教程，目标不是科普热词，而是带着你真正动手做。它想解决的是很多中文开发者都遇到的问题：知道大模型很重要，也看过很多概念文章，但一到实现、训练、推理或应用层改造就容易断档。这个仓库把学习路径拆成可跟着敲的教程，对学生、自学者、转型做 LLM 的工程师都很友好。它不替你做产品决策，但很适合用来补齐“我到底懂没懂”的那段学习缺口。
- 核心特性:
  1. 中文语境下可直接上手的代码实践，对很多第一次系统学 LLM 的人很友好。
  2. 不是只讲概念，而是用 Notebook 和编程练习把抽象知识压成可执行路径。
  3. 适合拿来做自学路线，也适合团队内部给新同学做统一入门材料。
- 适用场景: 适合想系统补 LLM 基础和实践能力的学生、工程师、科研转工程人群。第一次阅读，不必试图“一天看完整套”，更建议先挑自己最近最缺的一块，比如 tokenizer、训练流程、推理实战或应用案例。如果你现在想找的是一个能直接商用部署的 Agent 框架，它不是那种工具型项目。
- 一句话推荐: 今天值得点开它，因为再热的 Agent 最终也绕不过对基础能力的理解；第一次打开先看教程目录和更新说明，挑一个最贴近你当前工作的章节开始最划算。
- Evidence Notes: README 顶部明确定位为《动手学大模型》系列编程实践教程，并持续根据社区反馈更新内容。
- Honest Caveat: 它更像持续建设中的教学项目，不是已经完全封版的标准教材；不同章节成熟度可能不完全一致。

### Rank 04 - openai/openai-agents-python
- Repo URL: https://github.com/openai/openai-agents-python
- Tagline: 用 Python 搭多 Agent 工作流的轻量级工程框架
- Stars: 21904
- Stars Today: 625
- Forks: 3502
- Language: Python
- License: MIT
- Homepage: https://openai.github.io/openai-agents-python/
- Topics: agents, ai, framework, llm, openai, python
- 技术栈: Python, Agents SDK, Tools, Handoffs, Guardrails, Tracing
- Why It Matters Today: 当团队从“玩 Agent demo”走到“要做成产品功能”时，最缺的往往不是模型，而是一个能组织 handoff、tools、guardrails、sessions 的工程底座。
- 项目摘要: `openai-agents-python` 是一个面向多 Agent 工作流的 Python SDK，重点不是堆功能名词，而是把 Agent 在工程里真正常见的几件事做顺: agent 定义、工具接入、handoff、guardrails、session、tracing。它要解决的是很多 Agent 项目都会遇到的尴尬：demo 很炫，但一进真实业务就开始上下文混乱、可观测性差、职责边界不清。这个 SDK 更像是一个能支撑你往产品和服务里落的底层框架。对 Python 团队来说，它值得关注的不是“会不会多 Agent”，而是“能不能更稳地多 Agent”。
- 核心特性:
  1. 把 Agents、Tools、Handoffs、Guardrails、Sessions、Tracing 这些关键能力统一在一套开发语义里。
  2. 支持把 Agent 当工具调用，也支持在更长时间跨度里用 sandbox agents 执行工作。
  3. 文档和概念边界清楚，适合从实验原型逐步走向更稳的工程实现。
- 适用场景: 适合用 Python 做客服、研究助手、自动化流程、内部 Copilot 的团队。第一次看时，最值得优先打开的是 Core Concepts 和 Tracing，看它是不是你想要的工程抽象层。如果你只是需要一个单轮 prompt 封装，或者团队主栈是 JS/TS，这个版本未必是最顺手的入口。
- 一句话推荐: 今天值得看它，因为它能帮你判断“我的 Agent 项目该不该开始进入工程化阶段”；第一次打开先看概念和 tracing，再决定要不要把现有 demo 迁进去。
- Evidence Notes: README 明确列出 Agents、Sandbox Agents、Agents as tools、Handoffs、Tools、Guardrails、Sessions 和 Tracing 等核心概念。
- Honest Caveat: 它是框架，不是“替你把业务流程已经设计好”的成品；真正落地仍然要你自己做任务建模和系统边界设计。

### Rank 05 - jamiepine/voicebox
- Repo URL: https://github.com/jamiepine/voicebox
- Tagline: 本地运行的开源语音合成与声音工作室
- Stars: 19979
- Stars Today: 797
- Forks: 2288
- Language: TypeScript
- License: MIT
- Homepage: https://voicebox.sh
- Topics: ai, cuda, mlx, qwen3-tts, qwen3-tts-ui, voice-ai, voice-clone, whisper
- 技术栈: TypeScript, Qwen3-TTS, Voice Cloning, Whisper, CUDA, MLX
- Why It Matters Today: 它不是论文式“多模态想象”，而是可以直接拿来做配音、声音克隆和语音产品原型的本地工具，这类“今天就能用”的项目正在明显吸走注意力。
- 项目摘要: `voicebox` 是一个开源语音合成工作室，聚焦的是你真的会打开来用的几件事：克隆声音、生成语音、做声音效果、搭建语音驱动应用，而且强调这些能力可以在本地机器上运行。它解决的是很多语音项目都很烦的一点：模型有了，但流程分散，创作和调试成本高，真正做成可用工具链很麻烦。对内容创作者、独立开发者、做 AI 语音体验的产品团队来说，它是那种一看就知道能不能派上用场的项目。
- 核心特性:
  1. 把声音克隆、语音生成、效果处理和应用构建放在同一个工作流里，少折腾一堆分散脚本。
  2. 强调本地运行，适合在性能、隐私和延迟上做更可控的尝试。
  3. 有站点和文档入口，比较像能直接落进真实使用场景的产品型开源项目。
- 适用场景: 适合做播客、短视频、配音、AI 助手语音能力、语音原型验证的开发者和创作者。第一次试用，先看支持的模型、硬件要求和本地性能，再看克隆效果是否真的满足你的标准。如果你要的是企业级托管语音服务、严格合规链路或大规模分发，这个项目更像原型和生产前工具，而不是整套云服务。
- 一句话推荐: 今天值得看它，因为它不是在讲“语音 AI 将来能做什么”，而是在告诉你“今天就能做什么”；第一次打开先看 demo 和硬件要求，很快就能判断值不值得装。
- Evidence Notes: README 顶部直接写明 Clone voices、Generate speech、Apply effects、Build voice-powered apps，并强调 all running locally on your machine。
- Honest Caveat: 本地运行带来可控性，也意味着你要自己承担设备性能、模型效果和部署体验差异。

### Rank 06 - google/magika
- Repo URL: https://github.com/google/magika
- Tagline: 用文件内容而不是后缀名来判断文件类型的 AI 检测器
- Stars: 15576
- Stars Today: 956
- Forks: 863
- Language: Python
- License: Apache-2.0
- Homepage: https://securityresearch.google/magika/
- Topics: ai, deep-learning, filetype, keras-classification-models, keras-models, mime-types, onnx
- 技术栈: Python, ONNX, Deep Learning, File Classification, MIME Detection, Security Pipelines
- Why It Matters Today: 这类项目证明 AI 的价值不只在聊天和创作，很多底层基础设施问题也开始被更聪明、更实用的模型方法接管。
- 项目摘要: `magika` 是 Google 开源的文件类型识别工具，但它和传统“看后缀名、看 MIME”那套不一样，重点是根据文件内容判断它到底是什么。它想解决的是上传、扫描、归档、风控、数据管道里一个很常见但又经常被低估的问题：文件名可以骗人、扩展名可能缺失、MIME 也不总靠谱。`magika` 的价值在于让这类判断更快、更准，而且能直接嵌进安全和数据流程。对做内容安全、文件处理、企业上传链路、自动化扫描的人来说，它非常实用。
- 核心特性:
  1. 用内容识别文件类型，比只看扩展名更可靠，尤其适合不可信文件来源。
  2. 主打快和准，适合接在高频文件处理链路里，而不是只能做离线实验。
  3. 不局限于单一语言生态，Python、npm、Go 等入口让它更容易被工程系统吸收。
- 适用场景: 适合做安全扫描、文件上传校验、数据治理、文档处理和自动化内容管道的团队。第一次看它，先看 benchmark 和支持的接入方式，再判断能不能替换你现在那套脆弱的文件类型判断逻辑。如果你需要的是恶意样本深度分析、内容审计或复杂语义理解，它不是用来解决那个层级问题的。
- 一句话推荐: 今天值得看它，因为它解决的是每个文件系统、上传系统和安全系统都会踩到的低层问题；第一次打开先看支持场景和接入方式，很快就能判断它是不是你链路里那块“该升级但一直没升”的基础设施。
- Evidence Notes: README 与仓库描述都明确强调 fast and accurate AI powered file content types detection，并提供 Python、npm 和 Go 入口。
- Honest Caveat: 它是文件类型识别器，不是万能内容理解器；遇到极少见格式或高度异常文件时，仍然需要回退策略。

### Rank 07 - Donchitos/Claude-Code-Game-Studios
- Repo URL: https://github.com/Donchitos/Claude-Code-Game-Studios
- Tagline: 把单个 Claude Code 会话扩成一整个 AI 游戏开发工作室
- Stars: 11889
- Stars Today: 311
- Forks: 1729
- Language: Shell
- License: MIT
- Homepage:
- Topics: ai-agents, ai-assisted-development, anthropic, claude, claude-code, game-design, game-development, gamedev, godot, indie-game-dev, unity, unreal-engine
- 技术栈: Shell, Claude Code, Multi-Agent, Godot, Unity, Unreal Engine
- Why It Matters Today: 它很夸张，也很能说明问题：大家已经不满足于让 AI 写一个函数，而是开始尝试让 AI 扮演一个真实团队里的多个岗位。
- 项目摘要: `Claude-Code-Game-Studios` 本质上是一个把 Claude Code 组织成“游戏工作室”的多角色协作系统。它不是简单地多放几个 prompt，而是把策划、程序、美术、测试、制作等工作想象成一个有层级和工作流的 AI 团队，配上 49 个 agents、72 个 skills、12 个 hooks 和一套协调机制。它要解决的是独立游戏和小团队常见的资源矛盾：事情很多、岗位很多，但人手和预算不够。即便你不做游戏，它也很值得当成“多角色 Agent 编排”案例来研究。
- 核心特性:
  1. 用“工作室组织结构”来包装多 Agent 协作，比抽象讲 orchestration 更容易落到具体任务上。
  2. 明确针对 Godot、Unity、Unreal 这些游戏引擎语境设计，场景聚焦度很高。
  3. 对独立开发者来说，它最大的价值是把分工想法和流程框架先搭出来，而不是所有事都从零摸索。
- 适用场景: 适合独立游戏开发者、小型游戏团队，以及想研究多 Agent 分工设计的人。第一次看它，先看 agents、skills 和 studio hierarchy 的组织方式，再决定是否适合照搬到自己项目里。如果你需要的是成熟稳定的生产流水线，而不是实验性很强的 AI 工作室设定，它会显得过于激进。
- 一句话推荐: 今天值得看它，因为它把“多 Agent 协作”做成了一个非常具体、非常好想象的案例；第一次打开先看角色分工和工作流层级，马上就能判断它是噱头还是灵感来源。
- Evidence Notes: README 顶部直接写明 49 agents、72 skills、12 hooks，并强调 Turn a single Claude Code session into a full game development studio。
- Honest Caveat: 它更像一套高概念协作蓝图，不代表所有环节都已经达到生产级稳定性；真正输出仍然要靠人审和迭代。

### Rank 08 - BasedHardware/omi
- Repo URL: https://github.com/BasedHardware/omi
- Tagline: 把屏幕、对话、摘要和行动建议接进同一个“第二大脑”
- Stars: 9936
- Stars Today: 824
- Forks: 1676
- Language: Dart
- License: MIT
- Homepage: https://omi.me
- Topics: ai, app, bci, c, flutter, friend, mobile, necklace, nextjs, omi, personas, python, smartglasses, summary, transcription, wearable
- 技术栈: Dart, Flutter, Real-time Transcription, Summaries, Wearables, Context Memory
- Why It Matters Today: 它代表的是另一条快速升温的路线: AI 不只是帮你生成内容，而是持续捕获工作和生活上下文，变成跨设备的行动助手。
- 项目摘要: `omi` 想做的是一个你真的会“带着走”的第二大脑。它会捕获你的屏幕和对话，实时转写、生成摘要和行动项，并把这些上下文变成一个可以继续聊天和追问的长期记忆层。这个项目解决的是很多知识工作者每天都在承受的碎片化问题：会议记不全、任务丢在不同设备里、重要信息转眼就没了。对忙碌的专业人士、创业者、运营和高频会议人群来说，它的吸引力非常直接。
- 核心特性:
  1. 不只做转写，而是把屏幕、语音、摘要、后续问答串成一个完整上下文链。
  2. 覆盖桌面、手机和可穿戴设备，比单一会议纪要工具更像持续陪跑式助手。
  3. 适合那些信息输入密度很高、一天里频繁切上下文的人群。
- 适用场景: 适合会议很多、任务切换频繁、希望减少漏记和回溯成本的知识工作者。第一次看它时，最应该优先检查的是设备支持、数据流向和隐私边界，而不是只盯着功能数量。如果你所在组织对录音、屏幕采集或持续监听有很严格的合规要求，需要先把这关过了再谈落地。
- 一句话推荐: 今天值得看它，因为它展示了“上下文捕获型 AI 产品”最直白的一种形态；第一次打开先看隐私模型和支持设备，再判断它是效率神器还是隐私负担。
- Evidence Notes: README 直接描述了 captures your screen and conversations、real-time transcription、summaries and action items、works on desktop, phone and wearables。
- Honest Caveat: 这类产品天然伴随强隐私和接受度问题，是否能长期使用，很大程度取决于数据处理方式和组织文化。

### Rank 09 - pingdotgg/t3code
- Repo URL: https://github.com/pingdotgg/t3code
- Tagline: 给 Codex 和 Claude 这类编码 Agent 做的极简 GUI
- Stars: 9500
- Stars Today: 227
- Forks: 1783
- Language: TypeScript
- License: MIT
- Homepage: https://t3.codes
- Topics: agent-gui, codex, claude, desktop-app, web-ui
- 技术栈: TypeScript, Web GUI, Desktop App, Codex, Claude, Provider Switching
- Why It Matters Today: 不是所有人都愿意先跨过终端门槛再用 Agent；这个项目很直接地抓住了“Agent 也需要更友好的操作界面”这件事。
- 项目摘要: `t3code` 是一个给编码 Agent 做的最小化图形界面，当前重点支持 Codex 和 Claude。它解决的是一个经常被忽略的问题：很多团队并不是不会用 AI，而是 CLI 工具链太容易把普通开发者和跨职能成员挡在门外。这个项目的价值不在于发明新的 Agent 能力，而是让你更轻松地启动、切换、观察和演示现有 Agent。对想降低采用门槛、做内部试点和可视化演示的团队来说，它很有现实意义。
- 核心特性:
  1. 支持网页或桌面形式使用编码 Agent，减少“必须会命令行”这道门槛。
  2. 当前就支持 Codex 和 Claude，适合拿来做双栈对比或团队内演示。
  3. 安装路径简单，`npx`、桌面包管理器都能上手，试用成本低。
- 适用场景: 适合想给团队做 Agent 入门、想在 GUI 里观察和演示编码助手、或者个人不喜欢一直待在终端里的用户。第一次看它，先连通一个 provider，然后判断 GUI 到底是在帮你降门槛，还是只是给 CLI 套了层壳。如果你需要的是深度自动化、流水线式终端控制或非常成熟稳定的生产工具，它当前还偏早期。
- 一句话推荐: 今天值得看它，因为它回答了“编码 Agent 能不能更像普通人愿意打开的软件”；第一次打开先跑通一个 provider，再看这层界面对你是增益还是噪音。
- Evidence Notes: README 开头直接写明 T3 Code is a minimal web GUI for coding agents，当前支持 Codex 和 Claude，并提供桌面安装方式。
- Honest Caveat: README 也明确提醒项目 very very early，预期会有 bug；它更适合探索和试用，不适合一开始就押重生产。

### Rank 10 - EvoMap/evolver
- Repo URL: https://github.com/EvoMap/evolver
- Tagline: 用“自我进化”而不是预装技能来驱动 Agent 长期成长
- Stars: 4457
- Stars Today: 737
- Forks: 432
- Language: JavaScript
- License: GPL-3.0
- Homepage: https://evomap.ai
- Topics:
- 技术栈: JavaScript, Genome Evolution Protocol, Memory, Skill Tree, Evolution Assets, Agent Research
- Why It Matters Today: “Self-evolving agent” 正在成为热门话题，这个项目几乎就是把这个方向直接写进了产品定位里。
- 项目摘要: `evolver` 是一个面向 AI Agent 的自我进化引擎，核心主张非常鲜明：不要预装一堆静态技能，而是让 Agent 在解决任务过程中逐步长出自己的 memory、skills 和 evolution assets。它要解决的问题是很多 Agent 系统都会撞到的天花板：刚开始看起来很聪明，但换场景、拉长时间、任务复杂一点，就会暴露出静态 prompt 和静态工具组合的局限。这个项目非常适合想研究长期改进、技能积累、Agent 可持续成长机制的人。
- 核心特性:
  1. 不把技能体系视为一次性配置，而是强调用任务结果驱动技能演化。
  2. 公开把 memory、skill、evolution asset 这几层结构摆到台面上，便于理解它的系统想法。
  3. 有网站、Wiki 和中文文档入口，便于非核心开发者快速把理念看明白。
- 适用场景: 适合做 Agent 研究、长期自治系统、实验型工作流平台的开发者和团队。第一次看它，最该先判断的不是 demo 炫不炫，而是你是否认同“让 Agent 自己长能力”这套系统哲学。如果你现在更需要的是流程可预测、行为可控、马上能进生产的框架，它未必是最稳的一条路。
- 一句话推荐: 今天值得看它，因为它把最热门的“Agent 会不会长期进化”问题，做成了一个可以具体讨论的系统原型；第一次打开先看设计哲学和资产结构，再判断你要不要沿这条路继续深挖。
- Evidence Notes: README 直接写出 self-evolution engine、Genome Evolution Protocol，并明确提出 don't preload skills — evolve them。
- Honest Caveat: “自我进化”很吸引人，但要证明长期稳定收益比做出一两个精彩 demo 难得多；另外 GPL-3.0 许可也会影响一部分团队的采用决策。

### Rank 11 - lukilabs/craft-agents-oss
- Repo URL: https://github.com/lukilabs/craft-agents-oss
- Tagline: 面向真实协作场景的文档中心型 Agent 工作台
- Stars: 4323
- Stars Today: 110
- Forks: 637
- Language: TypeScript
- License: Apache-2.0
- Homepage:
- Topics:
- 技术栈: TypeScript, Agent Workspace, Session Sharing, API Integration, Document Workflow, Multitasking
- Why It Matters Today: 大量 Agent 项目还停留在终端和 demo 阶段时，它关注的是“团队怎么真的和 Agent 一起工作”这个更靠近日常使用的问题。
- 项目摘要: `craft-agents-oss` 是一个更偏产品工作台形态的 Agent 工具，强调直观的多任务处理、轻量连接任意 API / Service、共享会话，以及“以文档而不是代码视图为中心”的协作方式。它解决的是这样一种断层：SDK 很强、Agent 很能跑，但普通团队成员很难在一个漂亮、低摩擦、支持多人协作的界面里把这些能力真正用起来。这个方向对于产品、运营、研究、跨职能协作场景尤其重要。
- 核心特性:
  1. 把 multitasking、session sharing、文档中心工作流放在核心位置，而不是默认每个人都用终端。
  2. 强调和 API、服务快速连接，适合做“把 Agent 放进真实工作流”的工具层。
  3. 用 Agent Native 原则去组织界面和交互，明显不是只给 SDK 套一个普通后台壳。
- 适用场景: 适合想在团队内部搭建 Agent 工作台、让非 CLI 用户也能参与 Agent 协作的组织。第一次看它，建议先看 demo 视频，再看为什么要做成 document-centric workflow，因为这正是它和大多数终端式 Agent 工具拉开距离的地方。如果你只是想找一个脚本级多 Agent 框架，它的价值点不在那儿。
- 一句话推荐: 今天值得看它，因为它在回答“Agent 该怎么变成团队能一起用的软件，而不是少数人会玩的工具”；第一次打开先看视频和协作方式，最容易判断它有没有真正解决你的采用问题。
- Evidence Notes: README 明确写到 intuitive multitasking、connection to any API or Service、sharing sessions、document-centric workflow，并强调 built with Agent Native software principles。
- Honest Caveat: 相比一些更成熟的框架型项目，它更依赖你通过演示和产品体验去理解价值；公开文字材料目前没有把每个能力边界都讲得特别细。

### Rank 12 - lsdefine/GenericAgent
- Repo URL: https://github.com/lsdefine/GenericAgent
- Tagline: 从约 3K 行种子代码长出技能树的自进化 Agent，主打系统级控制与高性价比推理
- Stars: 3815
- Stars Today: 845
- Forks: 406
- Language: Python
- License: MIT
- Homepage: https://github.com/lsdefine/GenericAgent
- Topics: ai-agent, automation, autonomous-agent, browser-automation, claude, computer-control, desktop-automation, gemini, lightweight, llm-agent, memory-system, python, self-evolving, skill-tree, task-automation
- 技术栈: Python, Skill Tree, Browser Automation, Computer Control, ADB, Memory System
- Why It Matters Today: 它同时踩中了两个当下最热的关键词: computer control 和 self-evolving；更关键的是它把“少量核心代码 + 持续学会新技能”的路线做成了可阅读、可验证的实现样本。
- 项目摘要: `GenericAgent` 是一个极简、自进化的自治 Agent 框架。它最有辨识度的地方在于：核心代码只有大约 3K 行，却通过 9 个原子工具和一个很短的 agent loop，拿到了浏览器、终端、文件系统、键鼠、屏幕视觉、ADB 这些系统级控制能力。它想解决的是很多 Agent 框架越来越重、越来越黑盒的问题: 你能用，但不一定知道它为什么这样做，也很难把自己的能力积累沉淀下来。对想做本地自治、电脑控制、Agent 演化实验的人来说，它非常值得细读。
- 核心特性:
  1. 核心很小、透明度高，适合真正想改、想学、想验证 Agent 循环的人。
  2. 解决新任务后会把执行路径沉淀成可复用 skill，长期使用会长出属于自己的技能树。
  3. 工具覆盖面很广，从浏览器到本地电脑再到移动设备，是真正接触执行环境的 Agent。
- 适用场景: 适合研究自进化 Agent、探索电脑控制自动化、希望自己掌控框架内核的高级开发者。第一次看它，最该先读的是 Overview 和工具边界，看这套“小核心、后天长技能”的哲学是否符合你的预期。如果你所在环境对安全、权限、合规、稳定性要求非常高，直接把它用于敏感流程会有明显风险。
- 一句话推荐: 今天值得看它，因为它让“Agent 长期学会新能力”这件事从抽象口号变成了可以读代码、看机制的系统设计；第一次打开先看核心 loop 和 skill tree 逻辑，最容易判断它是研究样本还是你真想改造的底座。
- Evidence Notes: README 明确写出 ~3K lines of code、9 atomic tools、~100-line Agent Loop、system-level control，以及 don't preload skills — evolve them；Trending 描述还强调了 6x less token consumption 的效率主张。
- Honest Caveat: 能力越强，安全和约束问题越重；真正用于本地系统控制前，需要你自己做足权限边界和失败回滚设计。

## Language Distribution

- Language 1:
  - Count: Python 5
  - Percent: 33.3%
  - Color Hint: #3572A5
- Language 2:
  - Count: TypeScript 4
  - Percent: 26.7%
  - Color Hint: #3178C6
- Language 3:
  - Count: Shell 3
  - Percent: 20.0%
  - Color Hint: #89E051
- Language 4:
  - Count: JavaScript 1
  - Percent: 6.7%
  - Color Hint: #F1E05A
- Language 5:
  - Count: Dart 1
  - Percent: 6.7%
  - Color Hint: #00B4AB
- Language 6:
  - Count: Jupyter Notebook 1
  - Percent: 6.7%
  - Color Hint: #DA5B0B

## Explore Highlights

### Explore 1
- Title: obra/superpowers
- URL: https://github.com/obra/superpowers
- Kind: Explore 同步推荐仓库
- Meta: Trending / Explore 双重出现
- Short Reason: 如果你今天只看一个 Agent 方法论项目，它仍然是最有代表性的入口。

### Explore 2
- Title: ChromeDevTools/chrome-devtools-mcp
- URL: https://github.com/ChromeDevTools/chrome-devtools-mcp
- Kind: Explore 同步推荐仓库
- Meta: 浏览器控制与调试能力
- Short Reason: 它是“Agent 能不能真正接浏览器”的高价值样本，适合顺手延伸点开。

### Explore 3
- Title: lsdefine/GenericAgent
- URL: https://github.com/lsdefine/GenericAgent
- Kind: Explore 同步推荐仓库
- Meta: 自进化 + computer control
- Short Reason: 如果你对“技能树会自己长”这套设定感兴趣，这个项目非常值得继续挖。

### Explore 4
- Title: Lordog/dive-into-llms
- URL: https://github.com/Lordog/dive-into-llms
- Kind: Explore 同步推荐仓库
- Meta: 中文 LLM 学习路径
- Short Reason: 它不是工具，却是今天榜单里最适合拿来系统补课的一项。

### Explore 5
- Title: BasedHardware/omi
- URL: https://github.com/BasedHardware/omi
- Kind: Explore 同步推荐仓库
- Meta: 上下文捕获型多模态产品
- Short Reason: 如果你关心 AI 如何进入真实工作日常，这个方向很值得看。

### Explore 6
- Title: jamiepine/voicebox
- URL: https://github.com/jamiepine/voicebox
- Kind: Explore 同步推荐仓库
- Meta: 本地语音合成工作室
- Short Reason: 它是今天最“能立即装起来玩”的多模态项目之一。

### Explore 7
- Title: pingdotgg/t3code
- URL: https://github.com/pingdotgg/t3code
- Kind: Explore 同步推荐仓库
- Meta: 编码 Agent GUI
- Short Reason: 如果你想降低团队使用 Agent 的门槛，这一类 GUI 项目值得持续跟。

### Explore 8
- Title: lukilabs/craft-agents-oss
- URL: https://github.com/lukilabs/craft-agents-oss
- Kind: Explore 同步推荐仓库
- Meta: 文档中心型 Agent 工作台
- Short Reason: 它更像“团队怎么一起用 Agent”的产品思路补充，而不是又一个命令行框架。

## Rendering Notes

- Hero 主标题建议：GitHub Trending 日报
- Hero 副标题建议：今天值得点开的，不只是热门仓库，而是一批正在把 AI 变成真实工作流的项目
- 页面主叙事：首屏先回答“今天看什么”，然后用 4 张统计卡建立盘面感，再用 4 条洞察解释为什么值得看，最后把 Top 12 做成可按需深入的主榜单。
- 首屏层级建议：Hero 只放标题、副标题、日期和来源，不提前塞长段文字；首屏要让用户立刻知道今天的主线是“Agent 工作流基础设施 + 可操作环境 + 多模态实用工具”。
- Top 3 高亮原因：`superpowers` 代表工作流方法论、`chrome-devtools-mcp` 代表真实环境接入、`dive-into-llms` 代表学习路径补位，这三者覆盖“怎么做、怎么连环境、怎么补基础”三个不同入口。
- 卡片密度控制建议：封面态只保留 repo 名、tagline、核心 meta、少量 badge；项目摘要、核心特性、适用场景、一句话推荐放进展开层，避免首屏挤爆。
- Explore 列表样式建议：保持紧凑编号列表，不做卡片墙；明确告诉用户它和 Trending 高度重合，更适合作为顺手点开的延伸清单。
- 语言分布呈现建议：使用横向进度条，显示语言名、占比、项目数即可，不要再叠加额外图表噪音。
- 移动端收敛建议：所有主内容单列，Top 12 的封面态 meta 自动换行，展开区内部卡片纵向排列，保证手机上也能顺着读。
- 需要在 HTML 中诚实提示的降级点：Explore 今天与 Trending 重合度很高；部分项目没有完整 GitHub topics 或 homepage；总 Stars 取自仓库公开元数据，今日新增取自 Trending 页面。
- 不允许省略的区块：主题切换、Hero、4 张统计卡、4 条洞察、Top 12 折叠榜、语言分布、Explore 紧凑列表、页脚来源说明。
- 必须保留的固定模板结构：
  - Header / Hero
  - 4 张 Stats Cards
  - 今日洞察
  - 今日热门 Top 12
  - 编程语言分布
  - GitHub Explore 精选
  - Footer
- Top 详情固定顺序：
  1. 项目摘要
  2. 核心特性
  3. 技术栈
  4. 适用场景
  5. 一句话推荐
