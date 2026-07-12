# GitHub Trending 日报

## Meta

- 日期：2026-05-02
- 数据来源：https://github.com/trending + https://github.com/trending/python?since=daily
- 文件名：github_trending_report_2026-05-02.md
- 编码：UTF-8
- 语言：中文简体

---

## Page Intent

本报告记录 2026-05-02 GitHub Trending 全语言与 Python 频道的热门项目。与上期（2026-04-30）对比，今日共 **7 个新上榜项目**，5 个持续上榜项目。今日最大亮点：GitHub 官方 awesome-copilot（31k）首次入榜，与 obra/superpowers + mattpocock/skills 形成"Claude Code + Codex + Copilot 三大平台 Skills 生态同日在场"的格局；simstudioai/sim 以 261 次发布首次出现；TRELLIS + TimesFM 标志大模型范式渗透至 3D 生成与时序预测；而 Flowseal/zapret 则是全局 Trending 中罕见的俄语互联网自由工具。

---

## Stats

- 今日关注项目总数：12
- 今日新上榜：7
- 今日持续上榜：5
- 本期最高 Stars：obra/superpowers（175,987 ⭐）
- 语言分布：Python 5 / TypeScript 3 / Rust 1 / Markdown+Shell 2 / Batchfile 1

---

## Editorial Insights

### 洞察一：三大 AI 编程平台 Skills 生态同日在场

obra/superpowers（176k）代表"方法论层"：TDD + Subagent-Driven Dev，支持 Claude Code / Codex / Cursor / Gemini CLI。mattpocock/skills（53k）代表"TypeScript 工程师真实日常层"，直接来自 Matt 个人 .claude 目录。github/awesome-copilot（32k）代表"平台官方维护层"：GitHub 官方直接维护社区贡献的 instructions / agents / skills / plugins / hooks / agentic workflows，并内置到 Copilot CLI 的 marketplace（`copilot plugin install <name>@awesome-copilot`）。三个项目同日在场意味着 Claude Code / Codex / GitHub Copilot 的 Skills 生态正同步走向"基础设施化"。

### 洞察二：Sim 以 261 次发布首次登榜，Agent 编排进入高速工程化

simstudioai/sim（28k）是一个可视化 AI Agent 编排平台：画布拖拽连接 agents / tools / blocks + Copilot 自然语言辅助生成节点 + 向量数据库集成。Tech Stack 高度现代化：Next.js App Router + Bun + Drizzle ORM + ReactFlow + Socket.io + Trigger.dev + E2B（沙箱代码执行）。261 次发布节奏说明其已进入高速迭代，是目前开源 Agent 编排平台中最活跃项目之一。云托管版 sim.ai 与 npx simstudio 本地自托管并行提供。

### 洞察三：Flowseal/zapret 以 27k Stars 进入全语言 Trending，区域性互联网自由工具全球化

Flowseal/zapret-discord-youtube（27k）是一个俄语 Windows 工具，通过 DPI（深度包检测）绕过技术解决 Discord / YouTube 访问受限问题，使用 WinDivert 驱动在 Windows 内核层拦截并修改数据包。39 次发布、42 位贡献者。README 全俄文，但 Stars 达到 27k 的量级让它登上全语言全球 Trending，是区域性互联网限制工具全球化这一趋势的最新代表。

### 洞察四：TRELLIS + TimesFM 标志大模型范式渗透至传统专用领域

microsoft/TRELLIS（CVPR'25 Spotlight，12k）将文本/图像 → 3D 生成统一到"结构化 3D 潜变量"空间，支持 Radiance Fields / 3D Gaussians / Mesh 三种输出，可自由切换。google-research/timesfm（19k）时序基础模型 2.5 版：200M 参数 + 16k 上下文 + 连续分位数预测 + LoRA 微调 + 新增 SKILL.md Agent 接入。两个项目都代表"大模型统一预训练范式"对 3D 生成和时序预测这两个传统上由专用手工模型主导领域的渗透与颠覆。

---

## Top 12 Projects

### 01 obra/superpowers

- 仓库：https://github.com/obra/superpowers
- Stars：175,987 | Forks：15,565
- 语言：Shell / Markdown
- 许可：MIT
- 标签：agent-skills, claude-code, codex, cursor, tdd, subagent-driven-development
- 是否新上榜：**否（持续上榜）**

**核心摘要**

Superpowers 是一套 Agentic Skills 框架 + 软件开发方法论。当你启动 coding agent，它先从对话中提炼出规格说明，逐段确认后生成清晰实现计划，再启动 subagent-driven development 流程——多个子 agent 依次完成任务、互相 inspect 和 review，Claude 通常可以无干预连续自主工作数小时。

**主要特性**

- 自动触发：无需手动激活，skill 在你开始构建时自动介入
- test-driven-development：RED-GREEN-REFACTOR 完整循环 + 测试反模式参考
- systematic-debugging：4 阶段根因分析（根因追踪 + 纵深防御 + 条件等待）
- subagent-driven-development：两阶段 review（规格合规 + 代码质量）
- 跨平台：Claude Code 官方 Marketplace / Codex CLI / Cursor / OpenCode / Gemini CLI
- 作者：Jesse（obra）

**技术栈**

Shell / Markdown / Claude Code SKILL 格式

**适用场景**

AI agent 长时间自主完成复杂工程任务；将 TDD、YAGNI、DRY 内置到 Agent 工作流；多平台统一 Agent Skills 管理。

**推荐语**

> "不是 Skills 合集，而是方法论。176k Stars 背后是：让 agent 真正可以自主工作几小时而不偏离方向。"

---

### 02 TauricResearch/TradingAgents

- 仓库：https://github.com/TauricResearch/TradingAgents
- Stars：60,475 | Forks：11,656
- 语言：Python
- 许可：Apache-2.0
- 标签：llm, multi-agent, trading, finance, langgraph, deepseek
- 是否新上榜：**否（持续上榜）**

**核心摘要**

模拟真实交易公司架构的多 Agent LLM 金融交易框架：四路分析师（基本面 / 情绪 / 新闻 / 技术）+ 多头空头研究员对抗辩论 + 交易 Agent + 风险管理与组合经理。v0.2.4 支持 DeepSeek/Qwen/GLM/Azure，具备 LangGraph checkpoint 断点续跑与持久化决策日志。

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

> "分析师、研究员、交易员、风控全班人马到齐——LLM 量化仿真的最完整框架之一。"

---

### 03 mattpocock/skills

- 仓库：https://github.com/mattpocock/skills
- Stars：53,426 | Forks：4,496
- 语言：TypeScript
- 许可：MIT
- 标签：agent-skills, claude-code, typescript, real-engineers
- 是否新上榜：**否（持续上榜）**

**核心摘要**

TypeScript 专家 Matt Pocock 把自己日常工作真实使用的 .claude 目录直接开源，"Skills for Real Engineers"。非演示项目，而是经过生产环境检验的 AI 编程工作流指令集，一键 npx 安装即可使用。

**主要特性**

- 真实性：直接来自 Matt 个人 .claude 目录
- 覆盖 TypeScript 工程师核心日常场景
- npx 一键安装

**技术栈**

TypeScript / Claude Code SKILL 格式 / npx

**适用场景**

TypeScript 工程师日常 AI 辅助开发；参考真实工程师如何设计 Agent 工作流。

**推荐语**

> "Matt Pocock 是 TypeScript 社区标杆，他真实用的 skills 值得每个 TS 开发者看一遍。"

---

### 04 warpdotdev/warp

- 仓库：https://github.com/warpdotdev/warp
- Stars：51,977 | Forks：3,526
- 语言：Rust
- 许可：AGPL-3.0 / MIT
- 标签：terminal, agent, rust, openai, open-source
- 是否新上榜：**否（持续上榜）**

**核心摘要**

Warp 已开源，定位从"专有 AI 终端"升级为"开源 Agentic 开发环境"。OpenAI 为创始赞助商，新 agentic 工作流由 GPT 模型驱动。支持接入 Claude Code / Codex / Gemini CLI，build.warp.dev 提供数千 Oz Agent 实时施工看板。

**主要特性**

- build.warp.dev：实时查看 Agent 处理 issues / 写规格 / 实现 / review 的过程
- UI 框架开源：warpui_core + warpui crate（MIT 许可）
- 多外部 Agent 接入
- AGPL-3.0 + MIT 双许可

**技术栈**

Rust / TypeScript / AGPL-3.0 + MIT

**适用场景**

把 AI agent 工作流集成进终端；团队共享 Agent 操作可视化看板。

**推荐语**

> "Warp 开源不只是代码可见，而是把'AI Agent 在做什么'变成了公开可见的仪表盘。"

---

### 05 github/awesome-copilot

- 仓库：https://github.com/github/awesome-copilot
- Stars：31,943 | Forks：3,866
- 语言：Markdown
- 许可：MIT
- 标签：copilot, agent-skills, instructions, plugins, hooks, agentic-workflows
- 是否新上榜：**是（今日新上榜）**

**核心摘要**

GitHub 官方维护的社区贡献 Copilot 扩展合集，涵盖 instructions / agents / skills / plugins / hooks / agentic workflows 六大类目。内置到 Copilot CLI 的 marketplace，一条命令安装：`copilot plugin install <name>@awesome-copilot`。配套 Learning Hub 提供从核心概念到上手指南的完整文档。

**主要特性**

- GitHub 官方维护，可信度高
- 六大类目：Agents / Instructions / Skills / Plugins / Hooks / Agentic Workflows
- 内置 marketplace：Copilot CLI 直接 install
- Learning Hub：覆盖 agents / skills / MCP servers / agentic workflows 全链路
- 网站：awesome-copilot.github.com

**技术栈**

Markdown / Copilot CLI / MCP / GitHub Actions

**适用场景**

GitHub Copilot 用户快速接入社区扩展；了解 Copilot agent 生态全貌；参考官方维护的 Skill 组织方式。

**推荐语**

> "GitHub 官方直接下场维护，awesome-copilot 是 Copilot 生态的'官方应用市场'——质量和可信度远超社区散装合集。"

---

### 06 simstudioai/sim

- 仓库：https://github.com/simstudioai/sim
- Stars：28,243 | Forks：3,562
- 语言：TypeScript
- 许可：Apache-2.0
- 标签：agent, orchestration, visual-canvas, copilot, vector-db, next.js
- 是否新上榜：**是（今日新上榜）**

**核心摘要**

可视化 AI Agent 编排平台，定位为"AI 劳动力的中央智能层"。在可视化画布上设计 agent 工作流（拖拽连接 agents / tools / blocks），Copilot 功能支持用自然语言生成节点和修复错误，向量数据库集成让 agent 能基于你的内容回答问题。261 次发布节奏极快。

**主要特性**

- 可视化画布：拖拽设计工作流，连接 agents / tools / blocks
- Copilot 辅助：自然语言生成节点、修复错误、迭代流程
- 向量数据库集成：上传文档，agent 基于内容问答
- 支持 Ollama / vLLM 本地模型
- 云托管（sim.ai）+ 本地（npx simstudio / Docker）

**技术栈**

TypeScript / Next.js App Router / Bun / Drizzle ORM / PostgreSQL+pgvector / ReactFlow / Socket.io / Trigger.dev / E2B

**适用场景**

构建并部署 AI Agent 工作流；低代码/无代码 Agent 编排；团队级 AI Agent 操作化。

**推荐语**

> "261 次发布的 Sim 把'可视化编排 AI agents'做成了生产级工具——ReactFlow 画布 + E2B 沙箱的组合是现阶段开源 Agent 平台里最完整的工程架构。"

---

### 07 Flowseal/zapret-discord-youtube

- 仓库：https://github.com/Flowseal/zapret-discord-youtube
- Stars：27,005 | Forks：2,109
- 语言：Batchfile
- 许可：未明确（个人项目）
- 标签：dpi-bypass, discord, youtube, windows, network-freedom
- 是否新上榜：**是（今日新上榜）**

**核心摘要**

俄语 Windows 工具，通过 DPI（深度包检测）绕过技术解决 Discord / YouTube 在特定地区（主要是俄罗斯）访问受限问题。使用 WinDivert 驱动在 Windows 内核层拦截并修改数据包，绕过 ISP 的流量检测与封锁。39 次发布，42 位贡献者，27k Stars 让它登上全语言全球 Trending。

**主要特性**

- DPI 绕过：通过 WinDivert 在内核层修改数据包，绕过 ISP 封锁
- 支持 Discord（语音聊天）/ YouTube 视频访问
- 需要在浏览器中启用 Secure DNS（DoH）配合使用
- Windows 专用，Batch 脚本一键启动

**技术栈**

Batchfile / WinDivert / Windows 内核驱动

**适用场景**

在互联网访问受限地区恢复 Discord / YouTube 正常使用；了解 DPI 绕过技术原理。

**推荐语**

> "27k Stars 的 Batch 脚本——网络自由需求的力量，让一个全俄文 README 的项目登上了 GitHub 全语言全球 Trending。"

---

### 08 soxoj/maigret

- 仓库：https://github.com/soxoj/maigret
- Stars：21,968 | Forks：1,548
- 语言：Python
- 许可：MIT
- 标签：osint, username, social-media, recon, dossier
- 是否新上榜：**是（今日新上榜）**

**核心摘要**

OSINT 用户名情报收集工具，通过用户名在 3000+ 网站上搜集完整数字足迹，生成关于某人的档案报告（dossier）。相比只查找账号是否存在，maigret 还会提取个人信息并分析标识符关联，是目前最全面的开源用户名 OSINT 工具之一。

**主要特性**

- 3000+ 网站支持，覆盖社交媒体、论坛、专业平台、游戏平台等
- 提取关联个人信息（邮箱、电话、真实姓名等）
- 生成 HTML / PDF / JSON / CSV 格式报告
- 标识符关联分析，从一个用户名串联更多账号

**技术栈**

Python / 异步 HTTP / 正则表达式 / OSINT 数据源

**适用场景**

安全研究与渗透测试；数字足迹审查（检查自己的暴露面）；OSINT 学习与工具链集成。

**推荐语**

> "Sherlock 的进化版——maigret 不只找账号，还分析关联，3000+ 站点的覆盖范围让它成为用户名 OSINT 的首选工具。"

---

### 09 google-research/timesfm

- 仓库：https://github.com/google-research/timesfm
- Stars：19,241 | Forks：1,861
- 语言：Python
- 许可：Apache-2.0
- 标签：time-series, forecasting, foundation-model, google, llm, lora
- 是否新上榜：**是（今日新上榜）**

**核心摘要**

Google Research 开发的时序预测基础模型。TimesFM 2.5 使用 200M 参数，支持最长 16k 上下文和 1k 预测步长，2026年4月新增 LoRA 微调示例（HuggingFace Transformers + PEFT）和 Agent SKILL.md 支持，2026年3月新增 XReg 协变量支持。

**主要特性**

- 200M 参数基础模型，支持 16k 上下文、1k 预测步长
- 连续分位数预测（可选 30M 分位数头）
- XReg 协变量支持（exogenous covariates）
- LoRA 微调：HuggingFace Transformers + PEFT
- Agent 接入：SKILL.md 已发布（2026-03）
- 双框架：PyTorch + Flax（Flax 版推理更快）

**技术栈**

Python / PyTorch / Flax / HuggingFace Transformers / PEFT / XReg

**适用场景**

工业时序预测（能源、金融、零售需求）；无需从头训练的 zero-shot 时序预测；垂直领域 LoRA 微调定制。

**推荐语**

> "TimesFM 给时序预测装上了'基础模型引擎'——zero-shot 就能用，LoRA 微调随时定制，还能通过 SKILL.md 直接接入 Agent 工作流。"

---

### 10 nikopueringer/CorridorKey

- 仓库：https://github.com/nikopueringer/CorridorKey
- Stars：12,778 | Forks：757
- 语言：Python
- 许可：MIT（分段，部分组件另有许可）
- 标签：green-screen, chroma-key, vfx, compositing, ai-video
- 是否新上榜：**是（今日新上榜）**

**核心摘要**

AI 精准绿幕/蓝幕抠像工具，物理精确的颜色分离 + 线性 alpha 通道提取，保留头发、运动模糊和半透明细节。支持 4K 分辨率，输出 VFX 标准的 16/32-bit 线性浮点 EXR，可直接导入 Nuke / Fusion / DaVinci Resolve。Corridor Crew（知名 VFX YouTube 频道）背景项目。

**主要特性**

- 物理精确分离：保留头发、运动模糊、半透明度的直色前景 + 线性 alpha
- 绿/蓝幕：自动检测屏幕颜色（--screen-color auto）或手动指定
- 分辨率无关：动态缩放推理处理 4K 素材
- VFX 标准输出：16/32-bit 线性浮点 EXR（Nuke / Fusion / Resolve 兼容）
- 跨平台：NVIDIA CUDA / AMD ROCm / Apple Silicon MPS
- 自动清除追踪标记

**技术栈**

Python / PyTorch / CUDA 12.8 / ROCm / Apple Silicon MPS / MLX / EXR

**适用场景**

专业 VFX 合成工作流（Nuke / Fusion / Resolve）；AI 辅助绿幕内容制作；独立影片制作者替代商业抠像软件。

**推荐语**

> "Corridor Crew 出品，CorridorKey 把专业 VFX 绿幕抠像变成了开源工具——保留头发和运动模糊的物理精确分离，让每个人都能做 Hollywood 级别的合成。"

---

### 11 microsoft/TRELLIS

- 仓库：https://github.com/microsoft/TRELLIS
- Stars：12,407 | Forks：1,176
- 语言：Python
- 许可：MIT
- 标签：3d-generation, structured-latents, radiance-fields, gaussian, mesh, cvpr25
- 是否新上榜：**是（今日新上榜）**

**核心摘要**

微软研究院开源的 3D 生成基础模型，CVPR'25 Spotlight 论文代码。将文本/图像 → 3D 生成统一到"结构化 3D 潜变量"空间（SLAT），支持从同一潜变量生成 Radiance Fields / 3D Gaussians / Mesh 三种输出格式，无需为不同下游任务重新生成。支持对象变体生成（同一物体的多种外观变体）和局部编辑。

**主要特性**

- 统一结构化潜变量（SLAT）：一次生成，多种格式输出
- 输出格式：Radiance Fields / 3D Gaussians / Mesh（可自由选择）
- 文本/图像条件：支持 text-to-3D 和 image-to-3D
- 对象变体生成：同一物体生成多种外观变体
- 局部编辑：对已生成 3D 资产进行局部修改
- Gradio web demo 可本地运行

**技术栈**

Python / PyTorch / Radiance Fields / 3D Gaussians / Gradio / TRELLIS-500K 数据集

**适用场景**

游戏/影视资产快速 3D 生成；从参考图像生成 3D 模型；3D 内容生成研究。

**推荐语**

> "TRELLIS 把'3D 生成'和'大模型统一潜变量'这两件事合到了一起——CVPR'25 Spotlight 不只是论文荣誉，而是一套真正可用的生成工程框架。"

---

### 12 1jehuang/jcode

- 仓库：https://github.com/1jehuang/jcode
- Stars：2,502 | Forks：224
- 语言：TypeScript
- 许可：MIT
- 标签：coding-agent, multi-session, swarm, oauth, browser-automation
- 是否新上榜：**否（持续上榜）**

**核心摘要**

下一代 Coding Agent Harness，专注于多会话工作流、极致可定制化和高性能。支持 Swarm 模式（并发子 agent 协同）、OAuth 多 Provider、浏览器自动化、多 LLM Provider，已发布 51 个版本。

**主要特性**

- Multi-Session 工作流：并发多会话管理
- Swarm 模式：并发子 agent 协同，分布式任务执行
- OAuth 多 Provider 内置登录流 + 自托管端点 + MCP
- 浏览器自动化集成
- 高性能：Time to first frame / first input 极低延迟

**技术栈**

TypeScript / OAuth / MCP / Swarm / Browser Automation

**适用场景**

多 session / 多 agent 并发工作场景；高定制化 coding agent 工具链构建。

**推荐语**

> "51 次发布的高迭代速度 + Swarm 并发模式，jcode 正在快速成长为面向高级工程师的 agent 框架工具。"

---

## Language Distribution

| 语言 | 项目数 | 代表项目 |
|---|---|---|
| Python | 5 | TradingAgents, maigret, timesfm, CorridorKey, TRELLIS |
| TypeScript | 3 | mattpocock/skills, sim, jcode |
| Rust | 1 | warpdotdev/warp |
| Markdown/Shell | 2 | obra/superpowers, awesome-copilot |
| Batchfile | 1 | Flowseal/zapret |

---

## GitHub Explore Highlights

以下项目出现在 Python Trending 或全语言 Trending 后半段，未进入 Top 12，但具有关注价值：

1. **Lightricks/LTX-2**（6,257 ⭐）- 首个 DiT 音视频基础模型，同时生成同步音视频，8 种生成 Pipeline（A2V / HDR / LoRA / 关键帧插值 / Retake 等），ComfyUI 集成就绪，19B 参数

2. **NVlabs/GR00T-WholeBodyControl**（1,798 ⭐）- NVIDIA 人形机器人全身控制平台，本周新增 MotionBricks 预览（交互式 G1 demo + 142K+ 人体动作数据集 BONES-SEED），支持 VR 全身遥操作

3. **hugohe3/ppt-master**（10,559 ⭐）- AI 从任意文档生成原生可编辑 PPTX，使用真实 PowerPoint 形状 + 原生动画，而非图片嵌入，是办公场景 AI 自动化的代表方向

4. **AIDC-AI/Pixelle-Video**（8,826 ⭐）- AI 全自动短视频引擎，基于 ComfyUI 流水线，脚本 → 图像 → 语音全自动生成，适合内容批量生产

5. **browserbase/skills**（1,273 ⭐）- 为 Claude Code 提供完整浏览器自动化能力（browser / browserbase-cli / fetch / search / ui-test / browser-trace），让 Claude Code 具备真正的"眼睛"，npx skills add 一键安装
