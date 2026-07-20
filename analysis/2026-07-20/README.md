# 2026-07-20 项目架构分析索引

- 当日日报：[GitHub Trending 日报](../../md/github_trending_report_2026-07-20.md)
- 分析阶段状态：SUCCESS
- 入选项目：3
- 典型业务案例完成：3 / 3
- 成功：3
- 失败：0
- 跳过：9
- 降级：0

## 入选项目

| 项目 | Trending 排名 | 选择原因 | 解析文档 | Architecture | Flow | Innovation |
|---|---:|---|---|---|---|---|
| `KnockOutEZ/wigolo` | 4 | Stars Today 高、MCP/抓取/缓存/向量检索链路完整，适合研究 Agent 联网基础设施 | [查看解析](./KnockOutEZ__wigolo.md) | High | High | Medium |
| `1jehuang/jcode` | 10 | 大型 Rust 编码 Agent 工作区，Provider、TUI、工具、安全、记忆和 Swarm 边界明确 | [查看解析](./1jehuang__jcode.md) | High | Medium | Medium |
| `MoonshotAI/kimi-cli` | 12 | CLI、ACP、MCP 和 Flow Skill 均有官方实现证据，同时存在迁移风险，值得深入判断 | [查看解析](./MoonshotAI__kimi-cli.md) | High | High | Medium |

## 典型业务案例

| 项目 | 案例 | 关键失败分支 | 最小验证重点 |
|---|---|---|---|
| `wigolo` | 编码 Agent 搜索迁移说明并抓取关键页面 | HTTP 失败升级浏览器；搜索侧车不可用回退 Core；结构化错误返回 | 静态页、动态页、断网与 SearXNG 不可用 |
| `jcode` | 修改 Rust 文件并运行目标测试 | 权限拒绝、补丁冲突、Provider 错误、测试失败继续修复 | 临时 Git 仓库、拒绝权限、失败测试、会话恢复 |
| `kimi-cli` | 运行 Flow Skill，根据测试结果选择修复或结束 | Flow 解析失败、choice 缺失重试、max_moves 防死循环 | 最小 Mermaid Flow、无效 choice、循环上限 |

## 跳过项目

| 项目 | 排名 | 跳过原因 |
|---|---:|---|
| `kvcache-ai/ktransformers` | 1 | 具有分析价值，但异构内核和 SGLang 集成范围较大；今日优先保证三份 Agent 工具链分析深度 |
| `rohitg00/ai-engineering-from-scratch` | 2 | 以课程、提示词和学习材料为主，不符合本 Agent 的系统架构优先规则 |
| `jamiepine/voicebox` | 3 | 具备完整系统，但桌面、模型后端和多引擎范围较宽；本轮未纳入有限的三项目配额 |
| `andrewrabert/jellium-desktop` | 5 | 实际软件存在，但业务链路相对常规，今日架构研究优先级低于 Agent 基础设施 |
| `github/copilot-sdk` | 6 | 已在近期日报完成过深度分析，避免短期重复创建同类档案 |
| `PostHog/posthog` | 7 | 成熟大型平台，源码范围远超单次日报可可靠追踪的深度 |
| `microsoft/terminal` | 8 | 成熟基础设施且代码规模巨大，今日没有足够增量变化支撑重复深挖 |
| `AstrBotDevs/AstrBot` | 9 | 系统可分析，但消息平台与插件面较宽，本轮项目数量已达到质量上限 |
| `trycua/cua` | 11 | 多仓库/多环境 Computer-Use 基础设施，单次静态分析难完整验证跨 OS 运行链路 |

## 可信度分布

- Architecture Confidence：High 3 / Medium 0 / Low 0
- Flow Confidence：High 2 / Medium 1 / Low 0
- Innovation Confidence：High 0 / Medium 3 / Low 0

## Evidence Notes

- 所有项目均先从当天 Markdown 日报入选，再读取官方仓库代码、依赖、入口或实现文档。
- `wigolo` 的 MCP 分发、Provider 选择和子系统初始化已定位到源码。
- `jcode` 的启动组合与 workspace 边界证据充分，但具体文件工具循环未逐行覆盖全部分支，因此 Flow 为 Medium。
- `kimi-cli` 的 Flow Skill 有官方 `Status: Implemented` 设计文档与代码位置支撑。

## Honest Caveat

本阶段是源码与官方资料的静态研究，没有独立编译、安装或运行三个项目。所有示例输入均已在项目文档中标注为“示意”。性能、成本和维护者对产品优越性的表述没有被写成独立验证结论。
