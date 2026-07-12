# GitHub Trending 日报 · 2026-05-12

## Meta
- **日期**：2026-05-12
- **数据来源**：GitHub Trending（全语言）+ Python Trending
- **今日 Top 12**：12 个项目 | 累计 Stars：~582k | 编程语言：2 | 今日新上榜：7 | 持续上榜：5

---

## 今日洞察

### 🌊 从"Agent Skills 密集周"到"AI Foundations 日"：SD-webui（162.9k）+ LLMs-from-scratch（93.2k）今日领衔转换主题

前 6 日（05-06~05-11）Trending 以 Claude Code / Agent Skills / LLM 教育工具为主线，连续出现 spec-kit / agent-skills / everything-claude-code / anthropics-skills 等"AI coding 工具层"项目。今日出现了转折：AUTOMATIC1111/stable-diffusion-webui（162.9k，图像生成领域元老，Stable Diffusion 官方 Web UI）和 rasbt/LLMs-from-scratch（93.2k，"从 PyTorch 零开始手写 ChatGPT-like LLM"）同时领衔 Top 12。这两个都是沉淀多年的"AI Foundations"经典工具，与前几日"新出现的 Agent 工具/Skills 生态"形成鲜明对比。今日 Trending 转向说明：当 AI coding 工具层密集爆发一周后，基础工具层和学习资源层作为"背景辐射"被再次激活——大量新进入 AI 圈的开发者从 Agent 工具入手后，开始寻找基础工具和学习资源。

### 📚 三层 LLM 学习资源今日同框：LLMs-from-scratch（93.2k）+ hello-agents（47.7k，Day 3）+ dive-into-llms（37.4k，重返）

今日 Trending Top 12 里有 3 个纯粹的学习教程项目：rasbt/LLMs-from-scratch（"从 PyTorch 逐步手写 ChatGPT-like LLM"，理论原理层）+ datawhalechina/hello-agents（"从零构建智能体"，Day 3，Agent 应用层）+ Lordog/dive-into-llms（"《动手学大模型》实践教程"，实践操作层）。三者合计 178.3k Stars，分别覆盖 LLM/AI 学习的三个层次：原理→实践→应用。这种"学习资源三层同框"在本周日报中是第一次，说明今日的 Trending 用户构成以学习型开发者为主——区别于前几日"工具型开发者"主导的格局。

### 🐉 ByteDance 双项目同框：UI-TARS（10.5k，模型层，今日新）+ UI-TARS-desktop（33.2k，应用层，Day 3）——AI 产品"模型→应用"双层结构首次完整呈现

今日首次出现同一公司"核心模型 + 应用封装"双项目同时上 Trending：bytedance/UI-TARS（"Pioneering Automated GUI Interaction with Native Agents"，10.5k，底层多模态模型/算法）与 bytedance/UI-TARS-desktop（"The Open-Source Multimodal AI Agent Stack"，33.2k，Day 3，基于 UI-TARS 模型构建的桌面 Agent 应用层）同日出现。这揭示了 2026 年 AI 产品的典型"双层架构"：模型开源（UI-TARS）→ 应用封装开源（UI-TARS-desktop）→ 用户分别从两个维度访问同一技术栈，两个仓库彼此引流。今日 UI-TARS-desktop 已是 Day 3（05-10→05-11→05-12），与 UI-TARS 模型今日首次同框，是这个技术栈最完整的一次呈现。

### 🤝 huggingface/skills（10.5k）今日上榜——AI Agent Skills 标准格局从"Anthropic 一家"扩展为"Anthropic + HuggingFace 双极"

昨日（05-11）anthropics/skills（131.9k，Anthropic 官方 SKILL.md 规范）上榜。今日 huggingface/skills（10.5k，"Give your agents the power of the Hugging Face ecosystem"）上榜。huggingface/skills 明确声称"interoperable with all major coding agent tools like OpenAI Codex, Anthropic's Claude Code, Google DeepMind's Gemini CLI, and Cursor"，且遵循 agentskills.io 标准格式。两家定位不同：anthropics/skills 是"平台官方规范层"（SKILL.md 标准 + Claude.ai 生产级 skills），huggingface/skills 是"生态整合中立层"（跨模型/跨工具兼容，覆盖 HuggingFace AI/ML 任务如 dataset creation / model training / evaluation）。今日的对比让"AI Agent Skills 生态"首次出现"双极竞争"格局，而不是 Anthropic 独大。

---

## 今日热门 Top 12（按总 Stars 排序）

### #01 AUTOMATIC1111/stable-diffusion-webui ⭐ 162,938 [新上榜]
- **仓库**：https://github.com/AUTOMATIC1111/stable-diffusion-webui
- **语言**：Python | **License**：AGPL-3.0 | **Forks**：30,339
- **描述**：Stable Diffusion web UI. 162,938 ⭐ + 30,339 forks，图像生成领域最著名的开源 Web UI，今日领衔 Top 12，是本系列日报中非 Agent/Skills 类的最高单项目 Stars（超越 05-11 的 178.8k 是 Agent harness 类）。
- **核心特性**：
  - 完整的 Stable Diffusion Web 界面：txt2img / img2img / inpainting / outpainting
  - 扩展生态：数百个社区插件（ControlNet / ADetailer / Lora 管理等）
  - 支持多种 SD 模型：SD1.5 / SDXL / SD3 / Flux 等
  - 脚本系统：X/Y/Z 网格批量对比 / 图像批处理
  - API 接口：REST API 供外部调用
  - 社区最大：30k+ forks，数十万安装用户
- **技术栈**：Python / Gradio / PyTorch / ONNX
- **适用场景**：Stable Diffusion 本地化生图；图像生成工作流自动化；SD 模型研究和 A/B 测试。
- **推荐语**："162.9k Stars 今日第一——SD-webui 今日回归 Trending 是'AI 基础工具层复苏'的最强信号。前 6 日 Agent Skills 工具密集爆发后，今日的用户潮开始寻找'AI 图像生成'的入口，SD-webui 作为图像生成领域的元老自然首先浮出水面。"

---

### #02 NousResearch/hermes-agent ⭐ 145,333 [持续 Day 2]
- **仓库**：https://github.com/NousResearch/hermes-agent
- **语言**：Python | **License**：Apache-2.0 | **Forks**：22,735
- **描述**：The agent that grows with you. 连续第 2 日上榜，Stars 从 05-11 的 143,269 增至今日 145,333（+2,064），22,735 forks。Nous Research 出品，唯一内置学习循环的自进化 AI Agent，与 everything-claude-code ECC v2.0 深度集成。
- **今日亮点**：Day 2，今日与 AUTOMATIC1111/SD-webui 同框——两者代表了 AI 生态的两条主线：Nous Research 的"Agent 自进化"（新工具层）vs AUTOMATIC1111 的"图像生成"（成熟基础层）。hermes-agent 保持 +2,064 Stars/日的增速（vs 昨日的 143.3k → 145.3k），说明 ECC v2.0 + Hermes operator 生态的联动引流仍在持续。
- **推荐语**："Day 2，+2,064 Stars/日增速保持。今日在'AI Foundations'为主的 Trending 中，hermes-agent 作为唯一的纯 Agent 系项目保持 Top 3，说明 Agent 自进化赛道在基础工具层复苏的大背景下依然维持强劲热度。"

---

### #03 rasbt/LLMs-from-scratch ⭐ 93,160 [新上榜]
- **仓库**：https://github.com/rasbt/LLMs-from-scratch
- **语言**：Python | **License**：MIT | **Forks**：14,353
- **描述**：Implement a ChatGPT-like LLM in PyTorch from scratch, step by step. 93,160 ⭐ + 14,353 forks，今日三层学习资源之一，"从零手写 LLM"的权威教程，今日 Top 12 学习资源组合中的"原理层"。
- **核心特性**：
  - 逐步手写 ChatGPT-like LLM：注意力机制 / Transformer / 预训练 / 微调全流程
  - 纯 PyTorch 实现，不依赖 HuggingFace 等高层框架
  - 配套书籍：Manning 出版《Build a Large Language Model (From Scratch)》
  - 章节式结构：每章独立 Jupyter notebook，可按需阅读
  - 覆盖 GPT-2 完整实现 + 指令微调（Instruction Fine-tuning）+ RLHF 基础
  - 14k+ forks，是 LLM 教育领域 fork 最多的仓库之一
- **技术栈**：Python / PyTorch / Jupyter Notebook
- **适用场景**：深度理解 LLM 架构；从零 PyTorch 实现 Transformer；LLM 科研入门与教学。
- **推荐语**："今日与 dive-into-llms + hello-agents 构成三层学习资源同框。LLMs-from-scratch 是'最深'的一层——如果 dive-into-llms 是'会用大模型'，hello-agents 是'能构建 Agent'，那么 LLMs-from-scratch 是'明白大模型怎么工作的'。三层今日同框，覆盖了 AI 学习者完整的知识进阶路径。"

---

### #04 datawhalechina/hello-agents ⭐ 47,720 [持续 Day 3]
- **仓库**：https://github.com/datawhalechina/hello-agents
- **语言**：Python | **License**：CC-BY-4.0 | **Forks**：5,746
- **描述**：📚《从零开始构建智能体》——从零开始的智能体原理与实践教程。连续第 3 日上榜，Stars 从 05-11 的 47,098 增至今日 47,720（+622），5,746 forks。
- **今日亮点**：Day 3，今日与 LLMs-from-scratch + dive-into-llms 构成"三层学习资源"。hello-agents 在三层中是"Agent 应用层"——适合已了解 LLM 基础，想进一步构建 Agent 应用的开发者。3 日总增 47,720 - 45,976（05-10）= +1,744 Stars。
- **推荐语**："连续 Day 3，今日三层学习资源同框中的 Agent 应用入口。LLMs-from-scratch（原理）→ dive-into-llms（实践）→ hello-agents（Agent 应用），恰好是一个完整的 AI 学习路径。"

---

### #05 Lordog/dive-into-llms ⭐ 37,429 [新上榜（重返）]
- **仓库**：https://github.com/Lordog/dive-into-llms
- **语言**：Python | **License**：CC-BY-4.0 | **Forks**：4,587
- **描述**：《动手学大模型 Dive into LLMs》系列编程实践教程。今日重返 Top 12（曾在 05-10 上榜，Stars 37,429，vs 05-10 的 36,657，+772），4,587 forks。今日三层学习资源之一，LLM 实践操作层。
- **今日亮点**：今日重返，与 LLMs-from-scratch + hello-agents 构成三层同框。在 05-10 上榜后退出 Top 12，今日再次回归，说明《动手学大模型》系列教程在今日"学习资源大爆发"背景下持续被新用户发现和分享。
- **推荐语**："重返 Top 12，今日三层学习资源中的'实践层'。《动手学大模型》已成为国内 LLM 编程实践领域的标杆教程，今日与 LLMs-from-scratch（原理）+ hello-agents（Agent）同框，构成了今日最完整的中文 AI 学习路径。"

---

### #06 bytedance/UI-TARS-desktop ⭐ 33,188 [持续 Day 3]
- **仓库**：https://github.com/bytedance/UI-TARS-desktop
- **语言**：TypeScript | **License**：Apache-2.0 | **Forks**：3,290
- **描述**：The Open-Source Multimodal AI Agent Stack: Connecting Cutting-Edge AI Models and Agent Infra. 连续第 3 日上榜，Stars 从 05-11 的 32,529 增至今日 33,188（+659），3,290 forks。
- **今日亮点**：Day 3，今日与 bytedance/UI-TARS（#12，10.5k，模型层）同框，构成"ByteDance AI Agent 双层架构"完整呈现：UI-TARS 底层多模态模型 + UI-TARS-desktop 桌面应用封装，今日双项目同时在 Trending 是本系列日报首次出现的"同公司模型层+应用层双框"现象。
- **推荐语**："Day 3 持续，今日与 UI-TARS（模型层）同框形成 ByteDance AI Agent 完整双层架构。这是本周 Trending 中最典型的'AI 产品模型→应用双层开源策略'案例。"

---

### #07 anthropics/financial-services ⭐ 20,631 [持续 Day 5 🏆]
- **仓库**：https://github.com/anthropics/financial-services
- **语言**：Python | **License**：MIT | **Forks**：2,721
- **描述**：Anthropic 官方金融服务示例库。连续第 5 日上榜！Stars 从 05-11 的 19,502 增至今日 20,631（+1,129），2,721 forks。5 日轨迹：05-07 Explore（9.4k）→ 05-08（12.9k）→ 05-10（17.9k）→ 05-11（19.5k）→ 05-12（20.6k），5 日累计 +11.2k Stars。
- **今日亮点**：Day 5（并列 agent-skills 的最长连续上榜纪录）！今日仍与 HKUDS/AI-Trader（#8，Day 3）同框，金融 AI 双项目连续多日同框。5 日累计 +11.2k Stars，每日增量保持 1k+ 级别，说明金融 AI 赛道的热度持续稳定。
- **推荐语**："连续 Day 5，并列本系列最长上榜纪录（与 agent-skills 并列）！5 日累计 +11.2k Stars，今日突破 20k 大关。这是本系列日报中连续上榜天数最多的 Anthropic 官方项目。"

---

### #08 HKUDS/AI-Trader ⭐ 16,185 [持续 Day 3]
- **仓库**：https://github.com/HKUDS/AI-Trader
- **语言**：Python | **License**：MIT | **Forks**：2,587
- **描述**："AI-Trader: 100% Fully-Automated Agent-Native Trading". 连续第 3 日上榜，Stars 从 05-11 的 15,887 增至今日 16,185（+298），2,587 forks。港大 HKUDS 实验室出品。
- **今日亮点**：Day 3，今日与 anthropics/financial-services（#7，Day 5）持续同框。但今日 +298 Stars 的增速明显低于之前（05-10→05-11 增 +760），可能说明 AI-Trader 的热度峰值已过，开始进入自然衰减阶段。
- **推荐语**："Day 3，今日增速 +298（vs 昨日 +760）——金融 AI 项目的 Trending 衰减曲线开始显现。与 financial-services（#7，Day 5，仍保持 +1k 级增速）对比，两者开始分化：Anthropic 官方项目维持高增速，港大 AI-Trader 开始进入常规热度。"

---

### #09 jundot/omlx ⭐ 13,682 [新上榜]
- **仓库**：https://github.com/jundot/omlx
- **语言**：Python | **License**：MIT | **Forks**：1,162
- **描述**：LLM inference server with continuous batching & SSD caching for Apple Silicon — managed from the macOS menu bar. 13,682 ⭐ + 1,162 forks，从昨日（05-11）Explore 晋升今日 Top 12，Apple Silicon 专属 LLM 推理服务器，macOS 菜单栏管理。
- **核心特性**：
  - Apple Silicon 专属优化：充分利用 M 系芯片的统一内存架构
  - 持续批处理（continuous batching）：高并发推理吞吐量优化
  - SSD 缓存：超大模型的 KV Cache 持久化，减少重复计算
  - macOS 菜单栏管理：GUI 管理 LLM 服务，无需命令行
  - 开箱即用：本地 LLM 推理无需云 API
- **技术栈**：Python / llama.cpp / Metal / macOS API
- **适用场景**：Mac 本地 LLM 推理服务；Apple Silicon 高性能 LLM 部署；菜单栏管理的零配置本地 AI。
- **推荐语**："从昨日 Explore 晋升今日 Top 12，omlx 代表了'Mac 本地 LLM'的专属方向。今日与 SD-webui（本地图像生成）+ LLMs-from-scratch（本地训练）同框，三者共同构建了'AI 本地化运行'今日最完整的场景覆盖：推理服务器（omlx）+ 图像生成 UI（SD-webui）+ 手写理解（LLMs-from-scratch）。"

---

### #10 yikart/AiToEarn ⭐ 11,086 [新上榜]
- **仓库**：https://github.com/yikart/AiToEarn
- **语言**：TypeScript | **License**：MIT | **Forks**：2,029
- **描述**：Let's use AI to Earn! "OPC（一人公司）的 AI 内容营销智能体"，11,086 ⭐ + 2,029 forks，AI 变现工具赛道今日代表，覆盖 Monetize / Publish / Engage / Create 四大 Agent 能力。
- **核心特性**：
  - Monetize（内容赚钱）：内容交易市场，变现任务执行 Agent
  - Publish（内容发布）：多平台一键发布（小红书 / 抖音 / 快手 / 视频号 / YouTube / TikTok / Facebook / Instagram 等）
  - Engage（内容互动）：自动化互动 Agent
  - Create（内容创作）：AI 图片/视频/标签生成
  - MCP 协议支持（v2.1）：在 Claude / Cursor 等 AI Agent 中使用
  - OpenClaw（龙虾）支持：直接接收并执行内容变现任务
  - 5 种使用方式：网站 / OpenClaw / Claude+Cursor / Docker / 源码
  - 26 次发布，持续迭代
- **技术栈**：TypeScript / Electron / MCP / Docker
- **适用场景**：内容创作者 AI 变现工具；多平台内容自动化发布；一人公司的 AI 内容营销工作流。
- **推荐语**："今日 Top 12 唯一的'AI + 变现'方向项目。'OPC（一人公司）+ AI'是 2026 年国内开发者最感兴趣的组合之一——AiToEarn 提供了从创作到发布到变现的完整 AI 工作流，今日以 11k Stars 进入 Top 12，是'AI 内容创作变现'需求在社区中的集中体现。"

---

### #11 huggingface/skills ⭐ 10,465 [新上榜]
- **仓库**：https://github.com/huggingface/skills
- **语言**：Python | **License**：Apache-2.0 | **Forks**：661
- **描述**：Give your agents the power of the Hugging Face ecosystem. 10,465 ⭐ + 661 forks，HuggingFace 官方 Agent Skills 仓库，今日 Agent Skills 生态"双极竞争"的 HuggingFace 一极，遵循 agentskills.io 标准，跨工具兼容（Claude Code / Codex / Gemini CLI / Cursor）。
- **核心特性**：
  - HuggingFace 生态 Agent Skills：dataset creation / model training / evaluation 等 AI/ML 任务
  - 跨工具兼容：OpenAI Codex / Anthropic Claude Code / Google Gemini CLI / Cursor 全覆盖
  - 遵循 agentskills.io 标准：与 addyosmani/agent-skills 生态标准兼容
  - Skills Marketplace：可扩展的 Skills 目录
  - 中立定位：不绑定任何特定 LLM 或工具，强调生态整合
- **技术栈**：Python / Markdown / SKILL.md
- **适用场景**：在任意 AI coding agent 中调用 HuggingFace 生态能力；HuggingFace 任务的 Skills 标准化；跨工具兼容的 AI/ML 工作流 Skills。
- **推荐语**："昨日 anthropics/skills（131.9k），今日 huggingface/skills（10.5k）——两家官方 Skills 仓库连续两日上 Trending。Anthropic 的'平台规范层'（SKILL.md 标准）vs HuggingFace 的'生态整合层'（跨工具兼容，agentskills.io 标准），Agent Skills 生态双极竞争格局今日正式呈现。"

---

### #12 bytedance/UI-TARS ⭐ 10,450 [新上榜]
- **仓库**：https://github.com/bytedance/UI-TARS
- **语言**：Python | **License**：Apache-2.0 | **Forks**：773
- **描述**：Pioneering Automated GUI Interaction with Native Agents. 10,450 ⭐ + 773 forks，UI-TARS-desktop（#6，Day 3）的底层核心模型和算法，今日与 UI-TARS-desktop 同框构成 ByteDance AI Agent 完整双层架构。
- **核心特性**：
  - Native Agent GUI 交互的先驱模型：专门设计用于自动化 GUI 操作的多模态模型
  - 原生 Agent 能力：视觉理解 + 操作规划 + 执行验证的端到端 Agent 流水线
  - UI-TARS-desktop 的底层：桌面 Agent 应用的核心算法支撑
  - 多模态理解：截图分析 + 元素定位 + 操作生成
  - 与 UI-TARS-desktop 生态集成
- **技术栈**：Python / PyTorch / 多模态模型 / GUI Automation
- **适用场景**：GUI 自动化底层模型研究；多模态 Agent 算法开发；UI-TARS-desktop 的定制和扩展。
- **推荐语**："今日与 UI-TARS-desktop（#6，Day 3）同框，构成 ByteDance 'GUI Agent 双层开源'的完整图景。模型层（UI-TARS）+ 应用层（UI-TARS-desktop）双项目同日 Trending，是本系列日报首次出现的同公司双层架构完整呈现，也是理解 ByteDance AI Agent 产品策略的最佳视角。"

---

## 语言分布

| 语言 | 项目数 | 占比 | 代表项目 |
|---|---|---|---|
| Python | 10 | 83% | AUTOMATIC1111/SD-webui / hermes-agent / LLMs-from-scratch / hello-agents / dive-into-llms / financial-services / AI-Trader / omlx / huggingface-skills / UI-TARS |
| TypeScript | 2 | 17% | UI-TARS-desktop / AiToEarn |

---

## GitHub Explore 精选

1. **datawhalechina/easy-vibe**（10,104 ⭐）— Python — 今日全语言 Trending，以 100 Stars 之差刚好落出 Top 12。"💻 vibe coding 2026 | Your first modern Coding course for beginners to master step by step." 960 forks，Datawhale 出品的 2026 年 vibe coding 入门课程。今日在三层学习资源（LLMs-from-scratch + hello-agents + dive-into-llms）同框的背景下，easy-vibe 是第 4 个学习资源——如果按 Top 13 算，今日将有 4 个中文学习资源同时上榜，是本系列日报的最高纪录。

2. **wanshuiyin/Auto-claude-code-research-in-sleep**（8,898 ⭐）— Python — 今日 Python Trending。"ARIS ⚔️ (Auto-Research-In-Sleep) — Lightweight Markdown-only skills for autonomous ML research: cross-model review loops, idea discovery, and experiment automation. No framework, no lock-in — works with Claude Code, Codex, OpenClaw, or any LLM agent." 833 forks，轻量级 Markdown-only Skills，在你睡觉时自主完成 ML 研究任务：跨模型 review 循环 + 想法发现 + 实验自动化。今日与 huggingface/skills（#11）同框，两者都是"Skills for AI research"方向的代表，一个是官方生态层，一个是个人创作的极简 ML 研究自动化。

3. **millionco/react-doctor**（8,214 ⭐）— TypeScript — 今日全语言 Trending。"Your agent writes bad React. This catches it." 267 forks，由 Million.js 团队出品（Million.js 是著名的 React 性能优化库）。专门用来检测和修复 AI coding agent 写出的"坏 React 代码"，是对 AI 生成代码质量问题的直接回应。今日与 everything-claude-code（昨日 #1）生态关联密切——当 ECC 这类工具让 AI coding agent 写大量代码时，react-doctor 成为"质量守门员"。

4. **decolua/9router**（8,571 ⭐）— TypeScript — 今日全语言 Trending，连续多日出现在 Trending（05-11 Explore 第 5）。"Unlimited FREE AI coding." 今日虽退出 Top 12，但仍是全语言 Trending 的常驻项目。与 AiToEarn（#10）同框，两者都是"降低 AI 使用成本"的代表：9router（降低 AI coding 工具成本 via 40+ 免费 providers）+ AiToEarn（用 AI 增加收入），成本↓ + 收益↑ 是今日 Trending 里两个"AI 经济学"方向的不同路径。

5. **CloakHQ/CloakBrowser**（6,529 ⭐）— Python — 今日全语言 + Python 双榜，连续第 3 日出现（05-10 首次 / 05-11 Explore / 05-12 Trending）。"Stealth Chromium that passes every bot detection test. Drop-in Playwright replacement with source-level fingerprint patches. 30/30 tests passed." 480 forks，Stars 持续增长（05-10: 5,207 → 05-11: 5,207 → 05-12: 6,529，+1,322 今日增长尤为突出），说明 Stealth 浏览器自动化赛道的需求持续旺盛，可能与 AI agent 浏览器控制场景的普及有关。
