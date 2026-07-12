# skill-github-trending-report

这个 skill 现在采用固定模板工作流：

- 抓取 GitHub Trending / Explore 与重点仓库公开信息
- 先生成本地 Markdown 内容底稿
- 再复用 `reference/fixedBaseTemplate_2026-03-16.html` 生成 HTML
- 保持已经验收过的 UI、主题、展开详情布局不变
- 只替换当天内容和数据

## 核心参考

- `reference/user-rules.md`
- `reference/fixedBaseTemplate_2026-03-16.html`
- `reference/uiEngineeringSpec.md`
- `reference/reportMarkdownTemplate.md`

## Agent 流程

- `agents/markdown-report-writer-agent.md`：先写本地 Markdown 底稿
- `agents/ui-ux-designer-agent.md`：负责模板一致性与信息密度把关
- `agents/frontend-engineer-agent.md`：把 Markdown 底稿映射进固定 HTML 底板

## 不可违背的约束

- 必须先有 Markdown，再做 HTML
- 不允许重新设计页面
- 不允许替换 `03-16` 已验收布局和关键命名
- 不允许用 Python 或本地渲染器代写最终 HTML
- 必须保留 Top 12 的展开详情结构
- 重点项目中文解读必须具体、专业、说人话

完整流程与验收规则见 `SKILL.md`。
