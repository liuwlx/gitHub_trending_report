# 2026-07-16 GitHub Trending 项目架构分析

> 本目录从当天 GitHub Trending Top 12 中选择具有实际软件系统实现、源码证据完整且值得研究的项目。选择依据不是“谁的 Star 多谁先上桌”，而是能否沿入口、模块、状态和失败分支追出一条可信链路。

## 执行结果

| 指标 | 数量 |
|---|---:|
| Trending Top 项目 | 12 |
| 入选深度分析 | 3 |
| 成功 | 3 |
| 失败 | 0 |
| 跳过 | 9 |
| 典型业务案例完成 | 3 / 3 |
| 阶段状态 | SUCCESS |

## 入选项目

| 项目 | 原始排名 | 入选原因 | 典型业务场景 | Architecture | Flow | Innovation | 文档 |
|---|---:|---|---|---|---|---|---|
| `moeru-ai/airi` | 4 | 多端 AI 角色平台，Chat Orchestrator、Provider 兼容和工具流代码证据完整 | Stage Web 文字聊天，Provider 内容格式不兼容时自动降级重试 | High | High | Medium | [查看解析](./moeru-ai__airi.md) |
| `openinterpreter/openinterpreter` | 7 | 当前 Rust/Codex 派生架构包含 Session、Turn、工具、安全与多 Harness，适合源码研究 | Agent 修改源文件并在审批与沙箱约束下运行测试 | High | High | Medium | [查看解析](./openinterpreter__openinterpreter.md) |
| `HKUDS/DeepTutor` | 8 | FastAPI、WebSocket、ChatAgent、RAG、会话和多用户边界清晰 | 学生在课程知识库上提问，系统检索并流式返回带来源回答 | High | High | Medium | [查看解析](./HKUDS__DeepTutor.md) |

## 可信度分布

| 维度 | High | Medium | Low |
|---|---:|---:|---:|
| Architecture | 3 | 0 | 0 |
| Flow | 3 | 0 | 0 |
| Innovation | 0 | 3 | 0 |

`Innovation` 没有标成 High，不是客气，是证据边界：我们能确认“代码怎么实现”，不代表已经证明“行业里绝无仅有”。

## 未入选项目

| 原始排名 | 项目 | 处理 | 原因 |
|---:|---|---|---|
| 1 | `OpenCut-app/OpenCut` | 跳过 | 是实际系统，但当前仓库正处于 ground-up rewrite，多项核心能力仍在路线图；日报已重点说明，今天把分析名额留给主线代码更完整的项目。 |
| 2 | `Nutlope/hallmark` | 跳过 | 设计 Skill 与规则集，价值高但不是完整运行时系统。 |
| 3 | `mattpocock/skills` | 跳过 | 工程 Skills 集合，没有统一业务运行时、状态或部署边界。 |
| 5 | `Dicklesworthstone/destructive_command_guard` | 跳过 | 是可分析软件，但已在 2026-07-14 做过深析；今日避免短期重复。 |
| 6 | `HKUDS/Vibe-Trading` | 跳过 | 是可分析系统，但已在 2026-07-15 做过深析；今日优先新的源码对象。 |
| 9 | `HenryNdubuaku/maths-cs-ai-compendium` | 跳过 | 以教材内容和 MCP 辅助为主，不是完整业务系统。 |
| 10 | `Shubhamsaboo/awesome-llm-apps` | 跳过 | 多个独立示例的合集，没有统一架构，不能拿目录大杂烩硬画一张“总系统图”。 |
| 11 | `coreyhaines31/marketingskills` | 跳过 | 营销 Skills 集合，不具备统一运行时。 |
| 12 | `YimMenu/YimMenuV2` | 跳过 | 有实际 C++ 系统，但实验性强且涉及在线游戏使用风险；当前分析价值和证据完整度低于入选三项。 |

## 业务案例验收

### moeru-ai/airi

- 已定义参与者、前置条件、输入、结果与成功判定。
- 已提供 Mermaid 端到端时序图。
- 已追踪会话、流式消息、Provider 兼容性 Map、自动重试和云同步边界。
- 失败分支：内容数组不兼容时降级为字符串并重试一次；第二次失败继续向上抛出。

### openinterpreter/openinterpreter

- 已定义开发者修改文件并运行测试的示意任务。
- 已提供 Session → RegularTask → Turn Loop → Tool Router → Approval/Sandbox 的时序图。
- 已追踪工作区 diff、工具结果、审批和 CancellationToken。
- 失败分支：补丁或测试命令被拒绝、测试失败、用户中断；未虚构自动 Git 回滚。

### HKUDS/DeepTutor

- 已定义课程知识库问答场景和示意 WebSocket Payload。
- 已提供鉴权、会话、历史截断、RAG、流式 LLM、来源与持久化的时序图。
- 已追踪用户消息和助手消息的落盘顺序。
- 失败分支：RAG 失败降级为普通回答；模型失败则发 error，未虚构事务回滚。

## Evidence Notes

- 每份解析均读取目标仓库 README、依赖或工作区清单、入口文件、核心运行时、配置或协议相关源码。
- Mermaid 图只包含源码或官方文档能够支持的组件。
- 所有非官方请求体、文件名和业务输入均明确标注为“示意”。
- 本目录是源码静态分析，没有声称已经编译、部署、压测或独立验证维护者的性能与产品效果。

## Honest Caveat

三份分析都选择了一条证据最完整的代表性链路，不等于覆盖整个仓库。AIRI 的游戏和音视频集成、Open Interpreter 的全部 OS 沙箱组合、DeepTutor 的全部学习功能与存储后端均未在本轮逐项运行。这里讲的是“源码能证明什么”，不演“目录名一念，微服务就显灵”。
