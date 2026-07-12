# GitHub Trending 日报

## Meta

- 日期：2026-05-03
- 数据来源：https://github.com/trending + https://github.com/trending/python?since=daily
- 文件名：github_trending_report_2026-05-03.md
- 编码：UTF-8
- 语言：中文简体

---

## Page Intent

本报告记录 2026-05-03 GitHub Trending 全语言与 Python 频道的热门项目。与上期（2026-05-02）对比，今日共 **8 个新上榜项目**，4 个持续上榜项目。今日最大亮点：jwasham/coding-interview-university（345k）+ TheAlgorithms/Python（221k）两大 CS 经典巨头同日登榜；ruvnet/ruflo（37k，1,471 次发布）以"Claude Code 神经系统"身份强势入场；金融 AI 在今日榜单中最为密集——TradingAgents + qlib + AI-Trader 三路并进；tirth8205/code-review-graph 是本周最有工程深度的 Claude Code 优化工具，Tree-sitter 知识图谱让 token 消耗减少 6.8-49 倍。

---

## Stats

- 今日关注项目总数：12
- 今日新上榜：8
- 今日持续上榜：4
- 本期最高 Stars：jwasham/coding-interview-university（344,750 ⭐）
- 语言分布：Python 8 / TypeScript 1 / C# 1 / Batchfile 1 / Markdown 1

---

## Editorial Insights

### 洞察一：CS 经典双巨头同日登榜，合计 565k Stars

jwasham/coding-interview-university（345k）是 GitHub 史上最受欢迎的 CS 自学路径，一份帮你"从不会到通过 FAANG 技术面试"的完整月度计划，覆盖数据结构、算法、操作系统、网络、数据库全部核心领域。TheAlgorithms/Python（221k）是全球最全的算法 Python 实现开源库，50k+ forks、全社区驱动。两大"教育类经典"同日登上 Trending，反映 AI 编程工具（Claude Code / Copilot）对经典仓库的二次引流效应——用户把这些经典仓库纳入 AI 辅助学习与工作流，带动了今日热度。

### 洞察二：Ruflo 以 1,471 次发布登榜，Agent 编排平台加速分化

ruvnet/ruflo（37k）前身为 claude-flow，改名并升级为"Claude Code 的神经系统"。一次 init 给 agents 接入 Router → Swarm → Agents → Memory → LLM 的自学习/自优化架构，Rust WASM 内核驱动策略引擎、嵌入和证明系统，跨机器 federation 让 agents 在多台机器间安全通信。1,471 次发布的节奏创下本周纪录，是今日上榜项目发布次数最高的。加上昨日的 simstudioai/sim（261 次）、github/awesome-copilot，Agent 编排平台赛道正在加速分化为"重编排系统（Ruflo）"和"可视化画布（Sim）"两条路线。

### 洞察三：金融 AI 三路并进，qlib + AI-Trader 新加入 TradingAgents

今日金融 AI 最密集：TradingAgents（64k，持续）+ microsoft/qlib（42k，新上榜）+ HKUDS/AI-Trader（14k，新上榜）三路同日在场。qlib 是研究基础设施层（量化因子建模 + RL + 市场动态 + RD-Agent 自动化 R&D），AI-Trader 是执行层（Agent 一条 SKILL.md 指令接入平台，自动发布信号、跨经纪商同步交易），TradingAgents 是决策层（多路分析师辩论 + 风控审批）。三个层次完整互补，构成今日 GitHub 上最完整的 AI 金融技术栈截面。

### 洞察四：code-review-graph 代表 Claude Code 本地优化生态的新方向

tirth8205/code-review-graph（15k）用 Tree-sitter 构建代码库结构知识图谱，通过 blast-radius 分析只给 Claude Code 传递"受影响文件"上下文，而非整个代码库。评测数据：code review 节省 6.8× tokens，日常编码任务节省 49× tokens，2,900 文件项目增量重索引 < 2 秒，23 种语言支持，通过 MCP 接入 Claude Code。这是目前"减少 AI 编码 token 浪费"方向中验证最充分的开源工具，代表 Claude Code 生态中"本地上下文工程"这一新子赛道的兴起。

---

## Top 12 Projects

### 01 jwasham/coding-interview-university

- 仓库：https://github.com/jwasham/coding-interview-university
- Stars：344,750 | Forks：82,498
- 语言：Markdown
- 许可：未明确（CC BY-SA 4.0 精神）
- 标签：computer-science, interview, study-plan, algorithms, data-structures
- 是否新上榜：**是（今日新上榜）**

**核心摘要**

GitHub 上最受欢迎的 CS 自学学习路径，由前亚马逊工程师 John Washam 创作。这是一份真实的"从不会到通过 FAANG 技术面试"的完整学习计划，覆盖数据结构、算法、操作系统、计算机网络、数据库、分布式系统等所有面试核心领域。作者本人用这份计划从网页开发工程师转型成为亚马逊软件工程师，并持续维护更新至今。

**主要特性**

- 全面覆盖：数据结构（数组/链表/栈/队列/堆/树/图）+ 算法（排序/搜索/DP/BFS/DFS）+ 系统设计
- 月度学习计划：每个知识点给出具体视频/书单，并附带学习时间估算
- 多语言翻译：已有中文、日语、韩语、葡萄牙语等多语言版本
- 82k+ forks：全球最多 fork 数的学习资源仓库之一
- 持续更新：作者持续增补新内容，保持与现代面试的同步

**技术栈**

Markdown / YouTube 视频资源 / 多语言翻译

**适用场景**

准备技术面试（FAANG / 大厂）；系统补齐 CS 基础知识；自学计算机科学的结构化路线图。

**推荐语**

> "GitHub 上 345k Stars 不是营销数字，是无数自学工程师用它通过了面试的真实证明——John Washam 亲历者写给你的 CS 自学路线图。"

---

### 02 TheAlgorithms/Python

- 仓库：https://github.com/TheAlgorithms/Python
- Stars：220,647 | Forks：50,513
- 语言：Python
- 许可：MIT
- 标签：algorithms, data-structures, python, education, open-source
- 是否新上榜：**是（今日新上榜）**

**核心摘要**

全球最全的算法 Python 实现开源库，由全球社区共同维护。覆盖排序、搜索、图论、机器学习、密码学、字符串处理、数学等数百个算法的 Python 实现，每个实现都附带单元测试。221k Stars + 50k forks，是 GitHub 上 Python 类仓库中 fork 数最高的项目之一。

**主要特性**

- 数百个算法的标准 Python 实现（排序/搜索/图/树/DP/字符串/数学等）
- 每个算法附带完整单元测试（pytest）
- 机器学习、密码学、区块链等现代算法覆盖
- 全社区维护，PR 贡献友好，是练习开源贡献的理想项目
- 同系列支持 C / Java / C++ / JavaScript / Go / Rust 等语言

**技术栈**

Python / pytest / GitHub Actions CI

**适用场景**

查找标准算法 Python 实现参考；刷题/面试准备时验证算法思路；学习贡献开源项目的入门练习。

**推荐语**

> "221k Stars + 50k forks——TheAlgorithms/Python 是算法学习的'维基百科'，每道题都有测试覆盖的 Python 实现，随查随用。"

---

### 03 TauricResearch/TradingAgents

- 仓库：https://github.com/TauricResearch/TradingAgents
- Stars：63,743 | Forks：12,342
- 语言：Python
- 许可：Apache-2.0
- 标签：llm, multi-agent, trading, finance, langgraph, deepseek
- 是否新上榜：**否（持续上榜）**

**核心摘要**

模拟真实交易公司架构的多 Agent LLM 金融交易框架：四路分析师（基本面/情绪/新闻/技术）+ 多头空头研究员对抗辩论 + 交易 Agent + 风险管理与组合经理。v0.2.4 支持 DeepSeek/Qwen/GLM/Azure，具备 LangGraph checkpoint 断点续跑与持久化决策日志。今日与 qlib + AI-Trader 同日在场，构成 GitHub 史上最完整的单日金融 AI 技术栈截面。

**主要特性**

- Analyst Team：基本面（估值/财务）/ 情绪（社交媒体）/ 新闻（宏观）/ 技术（MACD/RSI）
- Researcher Team：多头/空头结构化辩论
- Trader Agent：综合所有报告决策交易时机和规模
- Risk Management：Portfolio Manager 审批/拒绝交易提案
- 多 LLM Provider：DeepSeek / Qwen / GLM / Azure / GPT / Claude / Gemini

**技术栈**

Python / LangGraph / DeepSeek / Docker / CLI

**适用场景**

LLM 量化研究与策略回测；多 Agent 协作决策研究（非投资建议）。

**推荐语**

> "金融 AI 三路并进之一——TradingAgents 负责'决策层'，今日与 qlib（研究层）、AI-Trader（执行层）同日在场。"

---

### 04 9001/copyparty

- 仓库：https://github.com/9001/copyparty
- Stars：44,648 | Forks：1,819
- 语言：Python
- 许可：MIT
- 标签：file-server, webdav, sftp, ftp, media-server, self-hosted
- 是否新上榜：**是（今日新上榜）**

**核心摘要**

"单文件全协议可移植文件服务器"——整个 copyparty 只是一个 Python 文件（或 .exe），包含 WebDAV / SFTP / FTP / TFTP / SMB 五种文件传输协议、断点续传加速上传、文件去重（内容匹配）、媒体索引、缩略图生成等全部功能。340 次发布，支持 Windows / Linux / macOS / Android / iOS / FreeBSD / arm32 / RISC-V / SGI IRIX。

**主要特性**

- 单文件部署：整个服务器就是一个 Python 文件或 .exe
- 五协议支持：WebDAV / SFTP / FTP / TFTP / SMB
- 无文件大小限制（包括 Cloudflare 中转场景）
- up2k：断点续传 + 多线程加速上传
- 文件去重：内容匹配哈希，自动去重或软链接
- 媒体功能：内置音频/视频/图片播放器、m3u8 播放列表、CBZ 漫画阅读器
- zeroconf/mDNS/SSDP 局域网自动发现

**技术栈**

Python / Pillow / FFmpeg / SQLite / WebDAV / SFTP / SMB

**适用场景**

家庭/团队自托管文件服务器；替代 Samba/NextCloud 的轻量方案；局域网设备间高速文件传输。

**推荐语**

> "340 次发布的单文件服务器——copyparty 把 WebDAV + SFTP + FTP + SMB + 媒体索引全塞进一个 Python 文件，零依赖安装，跑遍所有平台。"

---

### 05 microsoft/qlib

- 仓库：https://github.com/microsoft/qlib
- Stars：41,871 | Forks：6,581
- 语言：Python
- 许可：MIT
- 标签：quant, quantitative-finance, machine-learning, reinforcement-learning, microsoft, rd-agent
- 是否新上榜：**是（今日新上榜）**

**核心摘要**

微软开源的 AI 量化投研平台，面向量化研究从想法探索到生产上线全链路。支持监督学习、市场动态建模、强化学习三种 ML 范式，已与 microsoft/RD-Agent 集成，实现 LLM 自主 Agent 自动完成量化因子研究 R&D 全流程（从假设生成到实验验证）。

**主要特性**

- 三种 ML 范式：监督学习（因子预测）/ 市场动态建模 / RL（订单执行优化）
- Quant Model Zoo：20+ 论文级模型实现（LightGBM / LSTM / Transformer 等）
- 与 RD-Agent 集成：LLM 自主 Agent 自动化量化因子 R&D 全流程
- 在线服务模式：低成本模型在线部署
- 数据层：Yahoo Finance 自动日频数据更新

**技术栈**

Python / LightGBM / PyTorch / pandas / RL / Microsoft RD-Agent

**适用场景**

量化因子研究与策略回测；AI 自动化量化研究（+ RD-Agent）；研究级 RL 订单执行优化。

**推荐语**

> "微软量化研究基础设施开源——qlib 不是单个模型，而是整个量化 R&D 工作台，配合 RD-Agent 还能让 LLM Agent 自主跑实验。"

---

### 06 ruvnet/ruflo

- 仓库：https://github.com/ruvnet/ruflo
- Stars：37,290 | Forks：4,265
- 语言：TypeScript
- 许可：MIT
- 标签：claude-code, agent-orchestration, swarm, federation, mcp, rust-wasm
- 是否新上榜：**是（今日新上榜）**

**核心摘要**

前身为 claude-flow，改名为 Ruflo（"Ru"=rUv，"flo"=flow state）。自称"给 Claude Code 一个神经系统"：一次 init 给 agents 接入 Router → Swarm → Agents → Memory → LLM 的自学习/自优化架构，每次任务后主动学习成功模式并跨 session 记忆。Rust WASM 内核驱动策略引擎、嵌入和证明系统。1,471 次发布，Agent federation 支持多机安全通信。

**主要特性**

- 一次 init：自动路由任务、学习模式、协调 agents，无需手动配置
- 自学习架构：Learning Loop 在每次任务后优化路由和执行策略
- Swarm：agents 自组织为 swarm，协同完成复杂任务
- Federation：跨机器 agent 安全通信（不泄露数据）
- Rust WASM 内核：策略引擎 + 嵌入 + 证明系统
- Claude Code 原生插件：`/plugin install ruflo-core@ruflo` 一键安装
- ruvector：内置向量记忆（npm 包）

**技术栈**

TypeScript / Rust / WASM / MCP / Claude Code Plugin / npm / curl

**适用场景**

把 Claude Code 升级为自学习 Agent 协作系统；多 agent swarm 工作流自动化；跨机器 Agent federation 协同；无需学 314 个 MCP 工具。

**推荐语**

> "1,471 次发布的 Ruflo 是本周更新最激进的 Agent 编排项目——从 claude-flow 到 Ruflo，Rust WASM 内核让它从配置层升级为真正的 Agent 神经系统。"

---

### 07 ShareX/ShareX

- 仓库：https://github.com/ShareX/ShareX
- Stars：36,980 | Forks：3,691
- 语言：C#
- 许可：GPL-3.0
- 标签：screenshot, screen-capture, screen-recorder, file-sharing, windows, productivity
- 是否新上榜：**是（今日新上榜）**

**核心摘要**

Windows 上最强大的免费开源截图与文件共享工具，单键截图、区域选择、滚动截图、屏幕录制、OCR，支持 100+ 上传目标（图床/云存储/FTP 等），内置图片注释编辑器、颜色选取、哈希检测等工具。87 次发布，开源 14 年。

**主要特性**

- 截图模式：全屏/窗口/区域/滚动截图/延时截图
- 屏幕录制：支持 GIF + 视频（MP4/WebM）
- 100+ 上传目标：imgur / Dropbox / Google Drive / OneDrive / FTP / S3 等
- 内置工具：图片注释/模糊/水印 + 颜色选取 + OCR + 哈希校验
- 工作流自动化：截图后自动注释 → 自动上传 → 自动复制链接
- 完全免费，无广告，无会员

**技术栈**

C# / .NET / Windows / FFmpeg（录屏）

**适用场景**

日常 Windows 截图与标注工作流；批量上传图片到多云存储；替代收费截图工具（Snagit 等）。

**推荐语**

> "14 年、87 次发布、GPL-3.0 纯开源——ShareX 是 Windows 上没有'最强'只有'全能'的截图工具，100+ 上传目标让它成为生产力标配。"

---

### 08 Flowseal/zapret-discord-youtube

- 仓库：https://github.com/Flowseal/zapret-discord-youtube
- Stars：27,160 | Forks：2,116
- 语言：Batchfile
- 许可：未明确（个人项目）
- 标签：dpi-bypass, discord, youtube, windows, network-freedom
- 是否新上榜：**否（持续上榜）**

**核心摘要**

俄语 Windows DPI 绕过工具，通过 WinDivert 在 Windows 内核层拦截并修改数据包，解决 Discord / YouTube 在特定地区访问受限问题。39 次发布，42 位贡献者，27k Stars 持续在全语言 Trending。

**主要特性**

- DPI 绕过：WinDivert 内核层数据包修改，绕过 ISP 封锁
- 支持 Discord（语音聊天）/ YouTube 视频访问
- 需配合浏览器 Secure DNS（DoH）使用
- Windows 专用，Batch 脚本一键启动

**技术栈**

Batchfile / WinDivert / Windows 内核驱动

**适用场景**

在互联网访问受限地区恢复 Discord / YouTube 正常使用（仅限合法用途）。

**推荐语**

> "连续上榜，27k Stars 的俄语 Batch 脚本——区域性互联网限制催生的全球热门工具。"

---

### 09 soxoj/maigret

- 仓库：https://github.com/soxoj/maigret
- Stars：23,113 | Forks：1,625
- 语言：Python
- 许可：MIT
- 标签：osint, username, social-media, recon, dossier
- 是否新上榜：**否（持续上榜）**

**核心摘要**

OSINT 用户名情报收集工具，通过用户名在 3000+ 网站上搜集完整数字足迹，生成档案报告。不只找账号是否存在，还提取关联个人信息（邮箱、电话、真实姓名等）并分析标识符关联，生成 HTML / PDF / JSON / CSV 格式报告。

**主要特性**

- 3000+ 网站支持（社交媒体、论坛、专业平台、游戏平台等）
- 提取关联个人信息
- 多格式报告输出
- 标识符关联分析，串联更多账号

**技术栈**

Python / 异步 HTTP / OSINT 数据源

**适用场景**

安全研究与渗透测试；检查个人数字足迹暴露面；OSINT 工具链集成。

**推荐语**

> "连续上榜，3000+ 站点覆盖——maigret 是用户名 OSINT 的最全面开源工具。"

---

### 10 google-research/timesfm

- 仓库：https://github.com/google-research/timesfm
- Stars：19,301 | Forks：1,874
- 语言：Python
- 许可：Apache-2.0
- 标签：time-series, forecasting, foundation-model, google, lora, agent
- 是否新上榜：**否（持续上榜）**

**核心摘要**

Google Research 时序预测基础模型 TimesFM 2.5：200M 参数 + 16k 上下文 + 1k 预测步长，连续分位数预测，XReg 协变量支持，LoRA 微调（HuggingFace PEFT），Agent SKILL.md 接入（2026-03 新增）。连续第二日上榜，说明时序基础模型社区关注度持续高涨。

**主要特性**

- 200M 参数，16k 上下文，1k 预测步长
- 连续分位数预测（可选 30M 分位数头）
- LoRA 微调支持
- Agent SKILL.md 接入
- 双框架：PyTorch + Flax

**技术栈**

Python / PyTorch / Flax / HuggingFace PEFT / XReg

**适用场景**

工业时序预测（能源/金融/零售）；zero-shot 时序预测；LoRA 垂直领域微调定制。

**推荐语**

> "连续第二日上榜，TimesFM 2.5 的 LoRA + SKILL.md 组合让时序预测基础模型进入了 Agent 可直接接入的时代。"

---

### 11 tirth8205/code-review-graph

- 仓库：https://github.com/tirth8205/code-review-graph
- Stars：14,935 | Forks：1,644
- 语言：Python
- 许可：MIT
- 标签：claude-code, mcp, code-review, knowledge-graph, tree-sitter, token-optimization
- 是否新上榜：**是（今日新上榜）**

**核心摘要**

Claude Code 专属本地知识图谱工具，用 Tree-sitter 构建代码库结构图，通过 blast-radius 分析只给 Claude Code 传递"受影响文件"上下文，而非整个代码库。经 6 个真实开源项目基准测试：code review 节省 6.8× tokens，日常编码任务节省 49× tokens，2,900 文件项目增量重索引 < 2 秒，23 种语言支持，通过 MCP 接入。

**主要特性**

- blast-radius 分析：只传递变更影响文件（perfect recall，零漏报）
- 增量更新：git commit 或文件保存时触发，< 2 秒完成 2,900 文件重索引
- 23 种语言 + Jupyter notebooks（.ipynb + 多语言 cell 支持）
- monorepo 支持：27,700+ 文件排除，只读 ~15 文件的精准上下文
- MCP 接入：Claude Code 原生集成
- 已验证基准：6 个真实开源项目，13 次 commits 测试

**技术栈**

Python / Tree-sitter / MCP / Git hooks / SQLite / SHA-256 增量校验

**适用场景**

Claude Code 日常编码 token 节省（大项目效果尤为显著）；大型 monorepo code review 精准上下文；减少 AI 编码工具无效上下文的根本性解法。

**推荐语**

> "code-review-graph 是今日榜单中工程深度最扎实的工具——49× token 节省不是营销数字，是 6 个真实项目基准测试的实测结果。"

---

### 12 HKUDS/AI-Trader

- 仓库：https://github.com/HKUDS/AI-Trader
- Stars：13,903 | Forks：2,366
- 语言：Python
- 许可：未明确（商业平台）
- 标签：trading, agent-native, llm, automated-trading, multi-agent, cross-broker
- 是否新上榜：**是（今日新上榜）**

**核心摘要**

100% 全自动 Agent 原生交易平台，来自香港大学数据科学院（HKUDS）。AI agent 通过一条指令接入平台（读取 ai4trade.ai/skill/ai4trade 自动注册），即可发布交易信号、参与 collective intelligence 辩论、一键 copy trade 跟随顶级交易者、跨多经纪商同步信号。支持股票/加密货币/外汇/期权/期货全市场。

**主要特性**

- Agent 一指令接入：发送一条消息 + agent 自动注册平台
- Collective Intelligence Trading：agents 协作辩论推选最优交易想法
- 跨经纪商信号同步：自有经纪商 + 同步到其他平台
- 一键 Copy Trade：实时跟随顶级交易者
- 全市场：股票/加密/外汇/期权/期货
- 2026-04-10 生产稳定性更新：FastAPI 独立进程 + 后台 worker 分离

**技术栈**

Python / FastAPI / Agent SKILL.md 接入协议 / 多经纪商 API / WebSocket

**适用场景**

AI Agent 自主交易信号发布与跟单；多 agent 协作金融决策研究；全自动量化策略执行（非个人投资建议）。

**推荐语**

> "金融 AI 三路并进之三——AI-Trader 是'执行层'，SKILL.md 一条指令让任意 AI agent 加入全自动交易平台，Copy Trade 实时跟单。"

---

## Language Distribution

| 语言 | 项目数 | 代表项目 |
|---|---|---|
| Python | 8 | TheAlgorithms, TradingAgents, copyparty, qlib, maigret, timesfm, code-review-graph, AI-Trader |
| TypeScript | 1 | ruvnet/ruflo |
| C# | 1 | ShareX/ShareX |
| Batchfile | 1 | Flowseal/zapret |
| Markdown | 1 | jwasham/coding-interview-university |

---

## GitHub Explore Highlights

以下项目出现在 Trending 但未进入 Top 12，或今日关注度值得标注：

1. **Q00/ouroboros**（3,128 ⭐）- Agent OS：规格优先工作流运行时，把"临时 prompting"替换为"面谈 → 结晶 → 执行 → 评估 → 演化"的完整循环，支持 Claude Code / Codex CLI / OpenCode / Hermes，76 次发布

2. **browserbase/skills**（1,612 ⭐）- 从昨日 Explore 升入今日通用 Trending，为 Claude Code 提供完整浏览器自动化能力（browser / fetch / search / ui-test / cookie-sync），标志浏览器控制工具进入 Agent Skills 标准配置

3. **1jehuang/jcode**（3,058 ⭐）- 仍在通用 Trending，Swarm 并发模式 + OAuth 多 Provider，下一代 Coding Agent Harness，51 次发布

4. **simstudioai/sim**（28,243 ⭐）- 从昨日 Top 6 退出，但 261 次发布的可视化 Agent 编排平台仍值得关注，云托管 sim.ai 与本地 npx 并行

5. **nikopueringer/CorridorKey**（12,778 ⭐）- 从昨日 Top 10 退出，Corridor Crew 出品的 AI 绿幕抠像工具，VFX 标准 EXR 输出，仍是 VFX 领域最受关注的开源新项目
