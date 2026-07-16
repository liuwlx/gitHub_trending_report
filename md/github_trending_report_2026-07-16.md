# GitHub Trending Report — 2026-07-16

> 报告日期按 Asia/Tokyo 计算。榜单口径为 GitHub Trending：Repositories / Any language / Today。排名严格保留抓取时 GitHub 页面原始顺序；“累计 Stars”与“Stars Today”分列，绝不拿祖传家底冒充今天挣的。

## 1. 今日概览

| 指标 | 数值 |
|---|---:|
| Trending 项目数 | 12 |
| Stars Today 合计 | 9,377 |
| 主要语言数 | 7 |
| AI 相关项目 | 10 |

### 今日洞察

1. **Agent 技能包继续占据头部。** `mattpocock/skills`、`Nutlope/hallmark` 和 `coreyhaines31/marketingskills` 都在把经验整理成可安装、可组合的 Agent 工作流，说明竞争点正从“模型会不会写”转向“流程能不能稳定复用”。
2. **低成本模型的工程化正在升温。** `openinterpreter/openinterpreter` 明确转向 Rust 版、Codex 派生架构和多 Harness 切换，目标不是换个聊天皮肤，而是让便宜模型也能借助更强的执行框架干活。
3. **自托管 AI 产品开始长成完整系统。** `moeru-ai/airi` 与 `HKUDS/DeepTutor` 都包含前端、运行时、工具、状态、部署和多端入口；这类仓库已经不是一份 Prompt 配三张截图。
4. **第一名也要看成熟度。** `OpenCut-app/OpenCut` 热度最高，但当前仓库是重写中的新架构，经典版本仍单独维护。热榜第一是“大家都在看”，不等于“今晚就该替换生产工具”。

## 2. GitHub Trending Top 12

## 01. OpenCut-app/OpenCut

- **仓库：** https://github.com/OpenCut-app/OpenCut
- **原始排名：** 1
- **主要语言：** TypeScript
- **累计 Stars：** 72,271
- **Stars Today：** 1,664
- **Forks：** 7,380
- **许可证：** MIT
- **项目摘要：** 开源视频编辑器，目标覆盖 Web、桌面和移动端，并以 Rust 核心统一媒体处理能力。当前仓库是从头重写的新版本，旧版仍在独立仓库维护。
- **核心特性：** Web 前端使用 React/TanStack/Vite；API 使用 Elysia 与 Cloudflare Workers；桌面工作区采用 Rust 与 GPUI。路线图还包括 Editor API、插件优先架构、MCP、无头模式和脚本能力。
- **技术栈：** TypeScript、React 19、TanStack Start/Router、Vite、Cloudflare Workers、Elysia、Rust、GPUI。
- **适用场景：** 研究跨端视频编辑器、浏览器媒体工具和插件式编辑器架构；目前更适合评估和参与开发，不宜仅凭热度替换成熟剪辑生产链。
- **一句话推荐：** 热度像火箭，成熟度还在搭发射台——值得盯代码，不宜只看星星就搬家。

### Evidence Notes

- GitHub Trending 明确给出原始排名、TypeScript、累计 Stars、Forks 与 Stars Today。
- 仓库 README 明确说明当前代码库为 ground-up rewrite，并列出 Web/API/Desktop 开发入口及未来架构方向。
- `apps/web/package.json`、`apps/api/package.json` 与根 `Cargo.toml` 验证了 Web、Workers API 和 Rust Desktop 三条技术路径。

### Honest Caveat

Editor API、插件优先、MCP 和统一 Rust 核心中的部分能力仍属于路线图或重写阶段，不能写成已经完整稳定交付。

---

## 02. Nutlope/hallmark

- **仓库：** https://github.com/Nutlope/hallmark
- **原始排名：** 2
- **主要语言：** CSS
- **累计 Stars：** 8,996
- **Stars Today：** 1,277
- **Forks：** 461
- **许可证：** MIT
- **项目摘要：** 面向 Claude Code、Cursor 与 Codex 的设计 Skill，专门治理 AI 页面常见的模板味、同质化和“看着就像机器批发”的视觉问题。
- **核心特性：** 提供 Build、Audit、Redesign、Study 四种动作；从 20 套主题和不同宏观结构中选择方案；通过 57 项反模式门槛与输出前自检约束结果。
- **技术栈：** Agent Skill 文档协议、Markdown 规则集、自包含 HTML/CSS 示例、Node 技能安装器。
- **适用场景：** 让编码 Agent 生成更有辨识度的营销页、活动页和品牌页；不适合把审美判断完全甩给工具，也不等于现成设计系统。
- **一句话推荐：** 它卖的不是“再来一套渐变卡片”，而是先把 AI 最爱犯的审美毛病列成黑名单。

### Evidence Notes

- README 定义四个动词、20 个主题、57 个检查门槛和自包含 HTML/CSS 产物。
- 安装方式为 `npx skills add nutlope/hallmark`，规则主体位于 Skill 与 references 目录。

### Honest Caveat

“拒绝 AI 味”带有主观评价；门槛可以减少常见套路，但不能替代品牌研究、用户测试和专业设计评审。

---

## 03. mattpocock/skills

- **仓库：** https://github.com/mattpocock/skills
- **原始排名：** 3
- **主要语言：** Shell
- **累计 Stars：** 172,618
- **Stars Today：** 2,130
- **Forks：** 14,820
- **许可证：** MIT
- **项目摘要：** 一组面向真实软件工程的可组合 Agent Skills，重点覆盖需求澄清、规格拆解、TDD、排错、领域建模、架构改进和代码审查。
- **核心特性：** 区分用户主动调用和模型自动调用的技能；支持 skills.sh 与 Claude Code 插件安装；强调先澄清、再做小步反馈、最后审查，而不是一个大 Prompt 从天亮写到天黑。
- **技术栈：** Agent Skills 规范、Shell 安装入口、Markdown 工作流、Claude Code 插件清单。
- **适用场景：** 想给 Claude Code、Codex 等编码 Agent 加上可复用工程纪律的团队；不适合把技能文档当成质量保证书，仍需项目自己的测试和权限边界。
- **一句话推荐：** 这是工程习惯工具箱，不是“按一下按钮，祖传代码自动成仙”。

### Evidence Notes

- README 列出 setup、grill、to-spec、implement、TDD、diagnosing-bugs、code-review 等技能及调用边界。
- LICENSE 为 MIT。

### Honest Caveat

仓库本质是技能集合，不是单体软件系统；效果高度依赖宿主 Agent、项目上下文和团队是否真执行反馈闭环。

---

## 04. moeru-ai/airi

- **仓库：** https://github.com/moeru-ai/airi
- **原始排名：** 4
- **主要语言：** TypeScript
- **累计 Stars：** 42,593
- **Stars Today：** 110
- **Forks：** 4,252
- **许可证：** MIT
- **项目摘要：** 自托管、用户自有的 AI 虚拟角色平台，支持实时语音聊天、Web/桌面/移动端舞台，以及 Minecraft、Factorio 等外部交互方向。
- **核心特性：** Monorepo 拆分 apps、packages、plugins、services、engines；聊天编排层管理会话、上下文、流式消息、工具和遥测；LLM 层支持多 Provider，并对工具调用和消息格式不兼容做自动降级。
- **技术栈：** TypeScript、Vue、Pinia、pnpm/Turbo、xsAI、Live2D/VRM、Electron/Capacitor、Hono、MCP、OpenTelemetry。
- **适用场景：** 研究 AI Companion、虚拟角色、实时语音和多端 Agent 运行时；生产使用前要评估模型成本、隐私、角色资产授权、音视频延迟与复杂依赖。
- **一句话推荐：** 不是给聊天框戴个二次元头像，而是在做一套“角色、声音、工具、舞台”都能插拔的运行时。

### Evidence Notes

- 根 `package.json` 和 `pnpm-workspace.yaml` 验证多端应用、服务、引擎、插件和工作区结构。
- `packages/stage-ui/src/stores/chat.ts` 将会话、上下文、前台流、LLM、工具、云同步与遥测接入统一编排。
- `packages/core-agent/src/runtime/llm-service.ts` 验证流式模型调用、工具执行、错误捕获与 Provider 兼容降级。

### Honest Caveat

仓库规模大、变化快，不同舞台和集成的成熟度不一致；本报告确认的是代码结构和关键聊天链路，不代表所有游戏、语音和角色能力都已独立实测。

---

## 05. Dicklesworthstone/destructive_command_guard

- **仓库：** https://github.com/Dicklesworthstone/destructive_command_guard
- **原始排名：** 5
- **主要语言：** Rust
- **累计 Stars：** 4,826
- **Stars Today：** 471
- **Forks：** 181
- **许可证：** 以仓库 LICENSE 为准
- **项目摘要：** 给 AI Agent 和开发者命令行加一道危险操作拦截层，重点阻止高风险 Git 与 Shell 命令在无人看管时直接执行。
- **核心特性：** 规则匹配、危险命令分类、CLI/Hook 接入、可解释拒绝；适合作为 Agent 权限体系中的前置保险丝。
- **技术栈：** Rust、CLI、Git/Shell 命令解析、规则与测试体系。
- **适用场景：** 编码 Agent、本地自动化、CI 辅助任务；不能替代操作系统沙箱、最小权限账户、备份和人工审批。
- **一句话推荐：** 它不是保镖公司，是门口那根保险丝——不包天下太平，但能少炸几回锅。

### Honest Caveat

命令规则无法覆盖所有脚本变体、间接调用和业务语义；允许列表与绕过策略配置不当，同样会留下空档。

---

## 06. HKUDS/Vibe-Trading

- **仓库：** https://github.com/HKUDS/Vibe-Trading
- **原始排名：** 6
- **主要语言：** Python
- **累计 Stars：** 23,819
- **Stars Today：** 915
- **Forks：** 4,051
- **许可证：** 以仓库 LICENSE 为准
- **项目摘要：** 面向自然语言量化研究、策略生成与回测的个人交易 Agent，强调多 Agent、MCP 和研究工作流。
- **核心特性：** 会话式策略研究、工具调用、回测产物与结果汇总；适合把研究步骤串起来，不等于替用户承担投资决策。
- **技术栈：** Python、LLM Agent、MCP、多 Agent、量化数据与回测工具。
- **适用场景：** 策略原型、研究教学、数据管线实验；不建议未经独立验证直接连接真实资金执行。
- **一句话推荐：** 可以帮你把研究流程跑顺，不能把市场变成开卷考试。

### Honest Caveat

收益展示、回测结果和模型建议都不构成投资承诺；必须处理数据偏差、过拟合、滑点、费用和风控。

---

## 07. openinterpreter/openinterpreter

- **仓库：** https://github.com/openinterpreter/openinterpreter
- **原始排名：** 7
- **主要语言：** Rust
- **累计 Stars：** 65,579
- **Stars Today：** 299
- **Forks：** 5,657
- **许可证：** Apache-2.0
- **项目摘要：** 新版 Open Interpreter 是基于 OpenAI Codex 分叉的 Rust 编码 Agent，重点通过多种 Harness 模拟与本地执行能力，提高低成本模型完成软件任务的稳定性。
- **核心特性：** TUI 中切换模型和 Harness；支持本地沙箱、审批、Shell、补丁、MCP、Skills、Hooks、AGENTS.md 与 ACP 编辑器接入；会话和配置保存在本地目录。
- **技术栈：** Rust、Tokio、Codex 派生多 crate 工作区、TUI、Responses/兼容模型接口、MCP、ACP、原生沙箱。
- **适用场景：** 使用 Qwen、DeepSeek、Kimi 等低成本模型做本地编码任务和 Harness 对比；不适合在未审查权限、沙箱和密钥配置时直接放任执行。
- **一句话推荐：** 新版不是旧 Python 项目换了件衣服，而是把 Codex 的发动机拆来，专门研究便宜油怎么跑得稳。

### Evidence Notes

- README 明确说明当前版本为 Codex fork、Rust 新版，并列出 Harness、沙箱、ACP、MCP、Skills 与本地状态路径。
- `codex-rs/Cargo.toml` 验证 core、tui、exec、apply-patch、sandboxing、mcp、acp、protocol、hooks、skills 等工作区模块。
- `core/src/session/handlers.rs` 与 `core/src/session/turn.rs` 验证用户输入进入 Session、启动 RegularTask，以及模型输出工具调用后执行并回送结果的循环。

### Honest Caveat

当前仓库与历史 Python 版架构不同；旧教程和插件不能默认兼容。它具备高权限执行能力，安全性取决于沙箱、审批策略、运行账户和用户对每次动作的理解。

---

## 08. HKUDS/DeepTutor

- **仓库：** https://github.com/HKUDS/DeepTutor
- **原始排名：** 8
- **主要语言：** Python
- **累计 Stars：** 26,403
- **Stars Today：** 172
- **Forks：** 3,580
- **许可证：** Apache-2.0
- **项目摘要：** 面向长期个性化学习的开源 AI 教学平台，包含聊天、知识库、RAG、Web 搜索、记忆、学习路径、Partner Agent、多用户与多端入口。
- **核心特性：** FastAPI 后端与 Next.js 前端；WebSocket 流式聊天；统一 LLM 配置；RAG 与 Web Search 可选增强；会话和回答来源可落盘；支持容器化和多用户隔离。
- **技术栈：** Python 3.11+、FastAPI、WebSocket、Next.js 16、LLM Provider、RAG、PocketBase、Docker/Compose。
- **适用场景：** 自托管学习助手、课程知识库问答、研究型辅导和教学 Agent 实验；涉及未成年人或正式教学评估时，需要额外的隐私、内容安全和教师监督。
- **一句话推荐：** 它不是“问一句答一句”的作业机，而是在往会话、知识、记忆和学习路径一体化的教学平台走。

### Evidence Notes

- README 与 Release 记录验证 Chat、RAG、Memory、Partner、Guided Learning、多用户和容器化能力。
- `deeptutor/api/main.py` 验证 FastAPI、鉴权依赖、路由、EventBus、Partner、Cron、PocketBase 与受限静态输出。
- `deeptutor/api/routers/chat.py` 和 `deeptutor/agents/chat/chat_agent.py` 验证 WebSocket 鉴权、会话创建、历史截断、RAG/Web 检索、流式 LLM、来源返回和消息持久化。

### Honest Caveat

功能面很宽，部署复杂度和攻击面也随之上升；“个性化”和“终身学习”是产品目标，本报告未独立验证教学效果、知识正确率或长期记忆质量。

---

## 09. HenryNdubuaku/maths-cs-ai-compendium

- **仓库：** https://github.com/HenryNdubuaku/maths-cs-ai-compendium
- **原始排名：** 9
- **主要语言：** TypeScript
- **累计 Stars：** 6,010
- **Stars Today：** 725
- **Forks：** 748
- **许可证：** Apache-2.0
- **项目摘要：** 面向 AI/ML 研究工程师的数学、计算机科学与人工智能开放教材，内容覆盖线代、概率、算法、机器学习、视觉、NLP 和强化学习。
- **核心特性：** 文档型学习路径、在线站点、本地可克隆内容，以及供 AI 助手检索教材的 MCP Server。
- **技术栈：** TypeScript、文档站点、Markdown/MDX、MCP。
- **适用场景：** 系统补课、教学资料索引、给本地 Agent 提供结构化知识；不应把教材仓库当作经过同行评审的全部学术结论。
- **一句话推荐：** 像一本会接 MCP 的厚教材，适合查缺补漏，不适合拿 Star 数当毕业证。

### Honest Caveat

这是内容与学习工具项目，不是完整业务系统；章节质量、推导严谨度和更新一致性需要逐篇核验。

---

## 10. Shubhamsaboo/awesome-llm-apps

- **仓库：** https://github.com/Shubhamsaboo/awesome-llm-apps
- **原始排名：** 10
- **主要语言：** Python
- **累计 Stars：** 122,059
- **Stars Today：** 1,236
- **Forks：** 18,012
- **许可证：** 以仓库 LICENSE 为准
- **项目摘要：** 100 多个可运行的 AI Agent 与 RAG 示例集合，覆盖不同模型、数据库、工具和业务演示。
- **核心特性：** 按场景分类的独立示例、可克隆代码和快速实验入口；价值在广度和启发，不在统一架构。
- **技术栈：** Python、主流 LLM SDK、Agent 框架、向量数据库与 RAG 工具，具体依示例而异。
- **适用场景：** 原型选型、教学、对比 SDK；不适合整仓直接视作生产平台，也不能假设每个示例都达到同等安全和维护水平。
- **一句话推荐：** 菜谱很多，厨房不是一个——挑一道试，别整本书连锅倒进生产环境。

### Honest Caveat

这是示例合集，项目间没有统一运行时、状态模型或部署边界，因此不纳入当日架构深析。

---

## 11. coreyhaines31/marketingskills

- **仓库：** https://github.com/coreyhaines31/marketingskills
- **原始排名：** 11
- **主要语言：** JavaScript
- **累计 Stars：** 39,871
- **Stars Today：** 340
- **Forks：** 6,326
- **许可证：** 以仓库 LICENSE 为准
- **项目摘要：** 给 Claude Code 和其他 AI Agent 使用的营销技能集合，覆盖 CRO、文案、SEO、分析和增长工程。
- **核心特性：** 将营销检查清单、工作流和输出规范封装成可调用 Skill，方便在产品页面、内容和增长任务中复用。
- **技术栈：** JavaScript、Agent Skills、Markdown 规则与模板。
- **适用场景：** 营销团队给 Agent 增加结构化工作方法；不适合绕过事实核查、品牌审批、隐私规则和广告合规。
- **一句话推荐：** 它能把营销流程列明白，不能替产品凭空变好，更不能给虚假宣传开免检章。

### Honest Caveat

营销建议的有效性依赖行业、受众、渠道和实验数据；技能模板不是可普遍复制的增长承诺。

---

## 12. YimMenu/YimMenuV2

- **仓库：** https://github.com/YimMenu/YimMenuV2
- **原始排名：** 12
- **主要语言：** C++
- **累计 Stars：** 1,444
- **Stars Today：** 38
- **Forks：** 356
- **许可证：** 以仓库 LICENSE 为准
- **项目摘要：** 面向 GTA 5 Enhanced 的实验性菜单项目，属于游戏运行时修改和社区工具范畴。
- **核心特性：** C++ 原生实现、游戏进程集成与菜单功能；仓库明确标注实验性。
- **技术栈：** C++、Windows/游戏运行时相关原生组件。
- **适用场景：** 研究游戏 Mod、原生注入和 UI 框架；使用前必须核对游戏条款、在线模式风险、安全软件告警和下载来源。
- **一句话推荐：** 技术上可以研究，使用上得踩刹车——游戏封禁可不跟你讲开源情怀。

### Honest Caveat

本报告未运行该项目，也不对在线游戏使用、账号安全或第三方二进制分发作任何保证。

## 3. 编程语言分布

按 Top 12 项目数量统计：

| 语言 | 项目数 | 占比 |
|---|---:|---:|
| TypeScript | 3 | 25.0% |
| Python | 3 | 25.0% |
| Rust | 2 | 16.7% |
| CSS | 1 | 8.3% |
| Shell | 1 | 8.3% |
| JavaScript | 1 | 8.3% |
| C++ | 1 | 8.3% |

## 4. GitHub Explore 精选

Explore 抓取成功。该区域只作为补充发现，不改变 Trending 原始排名，也不计入上面的 12 项统计。

- **OpenCut-app/OpenCut** — Explore Trending repository；开源 CapCut 替代方案。
- **Nutlope/hallmark** — Explore Trending repository；面向编码 Agent 的反同质化设计 Skill。
- **moeru-ai/airi** — Explore Trending repository；自托管 AI 虚拟角色与多端舞台。
- **Pull Assistant** — GitHub staff recommendation；为 Pull Request 提供审查辅助信息。
- **Game Engines** — GitHub 推荐 Collection；跨平台游戏引擎集合。
- **injaneity/pi-computer-use** — Explore 补充项目；让 Pi 在 macOS/Windows 控制应用，未进入本次 Trending Top 12。

## 5. Rendering Notes

- HTML 必须继续沿用 `reference/fixedBaseTemplate_2026-03-16.html` 的布局、主题变量、卡片、展开详情与交互。
- Top 3 只按 GitHub Trending 原始位置高亮，不按累计 Stars 二次排序。
- 每个项目详情顺序固定为：项目摘要 → 核心特性 → 技术栈 → 适用场景 → 一句话推荐。
- Explore 使用紧凑列表，不做卡片墙。
- 保留 `toggleDetail(btn)` 与 `toggleTheme()`。

## 6. Evidence Notes

- **Trending：** https://github.com/trending?since=daily ，抓取口径为 Repositories / Any language / Today，报告日期 2026-07-16。
- **Explore：** https://github.com/explore ，抓取日期 2026-07-16。
- **仓库证据：** 各项目 GitHub README、LICENSE、依赖清单、入口文件和必要关键源码；架构深析项目另见 `analysis/2026-07-16/`。
- Stars 与 Stars Today 是抓取时快照，页面后续变化不回写本报告。

## 7. Honest Caveat

- 本日报是公开页面与源码的静态分析，不声称已逐个编译、部署或压测 Top 12。
- GitHub Trending 是动态榜单；同一天不同时间访问，项目顺序和数字可能变化。
- 项目自述、路线图和维护者性能数据均按来源属性表述，没有包装成第三方独立验证。
- 涉及交易、游戏 Mod、高权限 Agent、教育和生成式 AI 的项目，使用前仍需单独做安全、合规、许可证和业务风险评估。
