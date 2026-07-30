# 2026-07-30 Project Architecture Analysis Index

## Stage Status

- Stage: Project Architecture Analyst
- Status: SUCCESS
- Source Ranking: GitHub Trending / Repositories / Any language / Today
- Candidates: Top 12，严格保留当日原始排名
- Selected: 3
- Successful: 3
- Failed: 0
- Skipped: 9
- Business Scenarios Completed: 3 / 3

## Selected Projects

| Trending Rank | Project | Why Selected | Business Scenario | Architecture | Flow | Innovation | Result |
|---:|---|---|---|---|---|---|---|
| 2 | [moeru-ai/airi](./moeru-ai__airi.md) | 跨端 TypeScript monorepo，具备实际语音输入、Provider 适配、状态管理、测试和角色产品边界 | 浏览器端语音输入自动提交 | High | Medium | Medium | SUCCESS |
| 6 | [grokability/snipe-it](./grokability__snipe-it.md) | 成熟 Laravel 业务系统，资产领用链路能从路由、校验、控制器追到模型、事件与签收 | 单台硬件领用与现场签收 | High | High | Medium | SUCCESS |
| 9 | [different-ai/openwork](./different-ai__openwork.md) | React/Electron + openwork-server + OpenCode 的实际工作台系统，分层、会话与错误恢复证据完整 | 远程工作区代码任务的会话创建与 Provider 错误恢复 | High | Medium | Medium | SUCCESS |

## Confidence Distribution

- Architecture Confidence:
  - High: 3
  - Medium: 0
  - Low: 0
- Flow Confidence:
  - High: 1
  - Medium: 2
  - Low: 0
- Innovation Confidence:
  - High: 0
  - Medium: 3
  - Low: 0

## Business Scenario Checklist

| Project | 场景定义 | Mermaid 时序图 | 逐步追踪表 | 状态变化 | 失败/重试分支 | 最终结果 | 最小复现 | Status |
|---|---|---|---|---|---|---|---|---|
| AIRI | PASS | PASS | PASS | PASS | PASS | PASS | PASS | COMPLETE |
| Snipe-IT | PASS | PASS | PASS | PASS | PASS | PASS | PASS | COMPLETE |
| OpenWork | PASS | PASS | PASS | PASS | PASS | PASS | PASS | COMPLETE |

三份逐步追踪表均包含：输入、执行组件、关键代码位置、状态变化、输出、失败分支与证据级别。示意请求、ID、日期、Prompt 和样例文本均已明确标注为“示意”。

## Skipped Projects

| Trending Rank | Project | Decision | Reason |
|---:|---|---|---|
| 1 | `opengeos/GeoLibre` | SKIPPED | 具备实际 GIS 架构，但已在 `analysis/2026-07-28/opengeos__GeoLibre.md` 深度分析；避免短期重复创建同类报告。 |
| 3 | `affaan-m/ECC` | SKIPPED | 主要价值集中在 agents、skills、commands、hooks 与规则资产，运行时业务系统调用链不如本轮入选项目清晰。 |
| 4 | `huggingface/speech-to-speech` | SKIPPED | 具备模块化语音管线，但已在 `analysis/2026-07-29/huggingface__speech-to-speech.md` 深度分析。 |
| 5 | `1jehuang/jcode` | SKIPPED | 具备 Rust Agent Runtime，但已在 `analysis/2026-07-20/1jehuang__jcode.md` 深度分析。 |
| 7 | `deepfakes/faceswap` | SKIPPED | 有完整 Extract/Train/Convert 系统，但合成媒体滥用风险高；在同等分析预算下优先选择业务边界更明确的项目。 |
| 8 | `microsoft/VibeVoice` | SKIPPED | 以模型家族、权重与研究推理为主，部分 TTS 代码曾因责任使用问题移除；不适合作为本轮完整软件系统案例。 |
| 10 | `obra/superpowers` | SKIPPED | 以开发方法论、Markdown Skills 和多 Harness 安装适配为主，不属于需要追踪复杂运行时架构的独立业务系统。 |
| 11 | `MoonshotAI/FlashKDA` | SKIPPED | 高价值 CUDA Kernel 工程，但属于单一计算内核和后端集成，不具备本任务要求的完整业务端到端场景。 |
| 12 | `NanmiCoder/MediaCrawler` | SKIPPED | 有实际多平台采集系统，但许可证限定非商业学习，且平台协议、隐私和法律风险较高；本轮不扩展为操作链分析。 |

## Evidence Discipline

- 没有依据目录名虚构调用关系。
- 没有为 AIRI 或 OpenWork 虚构数据库、缓存、队列或微服务必经链路。
- Snipe-IT 的关系数据库由 Eloquent/PDO 与模型持久化直接支撑，但未虚构具体数据库产品或生产拓扑。
- 可选通知、Den、第三方 Provider、MCP 和部署组件均明确标注为可选或未动态验证。
- 所有性能、规模、模型质量和生产使用声明均保留项目方口径与 Honest Caveat。

## Failures and Degradation

- Project analysis failures: 0
- Skipped due to tool failure: 0
- Degraded reports: 0
- Stage status: SUCCESS

## Reading Order

1. [AIRI：语音输入与跨端角色平台](./moeru-ai__airi.md)
2. [Snipe-IT：资产领用与现场签收](./grokability__snipe-it.md)
3. [OpenWork：代理会话与错误恢复](./different-ai__openwork.md)

## Honest Caveat

这些报告均为公开源码、依赖清单、文档和测试的静态阅读结果，没有声称完成生产部署、独立安全审计、性能压测或外部服务的真实故障注入。可信度只描述“当前证据对架构、流程和创新判断的支撑程度”，不是项目质量评分。
