# 2026-07-14 GitHub Trending 项目架构分析索引

- 日报底稿：[../../md/github_trending_report_2026-07-14.md](../../md/github_trending_report_2026-07-14.md)
- 数据范围：GitHub Trending 官方页面 11 项；Explore 补位不参与架构项目选择。
- 架构分析状态：**SUCCESS**
- 入选项目：3
- 典型业务案例完成数：3 / 3
- 成功：3
- 失败：0
- 跳过：8
- 降级：0（日报数据层面存在“官方榜单仅 11 项”的明确说明，不影响 3 个架构报告的证据完整性）

## 入选项目

| Trending 排名 | 项目 | 入选原因 | 深度解析 | Architecture | Flow | Innovation |
|---:|---|---|---|---|---|---|
| 02 | `Dicklesworthstone/destructive_command_guard` | 高权限 AI Agent 的命令执行安全边界；源码中可追踪 hook、规则评估、白名单、审计与拒绝协议 | [查看解析](Dicklesworthstone__destructive_command_guard.md) | High | High | Medium |
| 08 | `Graphify-Labs/graphify` | detect→extract→build→cluster→analyze→report→export 管线清楚，适合研究代码知识图谱与证据标签 | [查看解析](Graphify-Labs__graphify.md) | High | High | Medium |
| 10 | `github/spec-kit` | CLI、打包资产、Agent integration、manifest 和 SDD workflow 形成完整工程系统 | [查看解析](github__spec-kit.md) | High | High | Medium |

## 典型业务场景

| 项目 | 端到端案例 | 成功判定 |
|---|---|---|
| destructive_command_guard | Claude Code 准备执行危险 `git reset --hard`，DCG 在 Shell 执行前拒绝 | Agent 收到 deny；目标命令未执行；Git 工作区无变化；可选 history 有记录 |
| graphify | 开发者对 Python/TypeScript 仓库生成知识图与架构报告 | 输出图与报告存在；抽样关系可回溯到源文件位置；证据标签正确保留 |
| spec-kit | 开发者初始化 Codex 的 SDD 项目骨架 | Agent 集成、`.specify` 资产、constitution、workflow、manifest 与 init options 均落盘 |

## 未入选项目

| Trending 排名 | 项目 | 跳过原因 |
|---:|---|---|
| 01 | `OpenCut-app/OpenCut` | 有架构研究价值，但当前仓库为重写中的下一代版本，多项 Editor API/Rust core/MCP 能力仍在规划；本日优先选择已有主链路更可验证的项目 |
| 03 | `HKUDS/Vibe-Trading` | 系统复杂且可分析，但涉及数据源、Agent、回测和多渠道，完整验证成本较高；本日名额优先给安全、知识图谱和 SDD 三类基础设施 |
| 04 | `moeru-ai/airi` | 大型多端 monorepo，适合单独专题；本日没有足够时间完成语音、角色状态、服务与多端链路的源码级闭环验证 |
| 05 | `Shubhamsaboo/awesome-llm-apps` | 示例与资源集合，不是一套统一系统架构；不同目录需要分别分析 |
| 06 | `Nutlope/hallmark` | 核心是设计 Skill 与参考材料，软件运行架构较轻，不满足本日深度系统分析优先级 |
| 07 | `Raphire/Win11Debloat` | 以 PowerShell 脚本和配置为主，架构复杂度低于入选项目；更适合安全选项与系统变更专题审计 |
| 09 | `hasaneyldrm/exercises-dataset` | 数据集与静态浏览资产，缺少可分析的端到端软件系统架构 |
| 11 | `coreyhaines31/marketingskills` | 营销 Skill 集合，核心价值是方法论和提示资产，不是复杂运行时系统 |

## 可信度分布

| 维度 | High | Medium | Low |
|---|---:|---:|---:|
| Architecture | 3 | 0 | 0 |
| Flow | 3 | 0 | 0 |
| Innovation | 0 | 3 | 0 |

Innovation 统一标记为 Medium，并非项目缺乏价值，而是“创新性”包含与传统方案的比较判断；源码能确认实现方式，却不能单独证明市场首创或在所有替代方案中更优。

## Evidence Notes

- DCG：读取 `Cargo.toml`、`src/main.rs` 关键 hook/评估/判定分支，并结合 `src/hook.rs`、`src/evaluator.rs`、packs、allowlist、history 模块边界。
- Graphify：读取 `ARCHITECTURE.md`、`pyproject.toml`、`graphify/__main__.py` 和源码目录，确认核心管线、Schema、置信标签、CLI/MCP 入口和可选 extras。
- spec-kit：读取 `pyproject.toml`、`src/specify_cli/__init__.py`、`src/specify_cli/commands/init.py`，确认 CLI、离线资产、integration、manifest、shared infra、workflow 和失败清理。

## Honest Caveat

本次架构分析是静态源码与官方文档研究，没有在任务环境中克隆、编译或运行三个项目。因此没有声称独立验证性能、误报率、图谱准确率或 SDD 对缺陷率的改善。每份报告都给出了最小复现路径，实际采用前应在隔离环境执行。
