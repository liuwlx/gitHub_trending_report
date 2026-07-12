# GitHub Trending Report Example

## 典型调用

**用户输入：**

```text
帮我生成今日日报，输出到 github 目录下。先生成本地 md 文档，再基于 2026-03-16 成品模板生成 html，不要改 UI。
```

**预期行为：**

1. 先读取 `reference/user-rules.md`
2. 再读取 `reference/fixedBaseTemplate_2026-03-16.html`
3. 再读取 `reference/uiEngineeringSpec.md`
4. 再读取 `reference/reportMarkdownTemplate.md`
5. 抓取 GitHub Trending、Explore 与重点仓库公开信息
6. 如果仓库描述不足，继续看官网、文档页或公开资料
7. 启动 `agents/markdown-report-writer-agent.md`，先生成本地 Markdown 底稿
8. 再读取 `agents/ui-ux-designer-agent.md`，只做固定模板内的信息层级与长度把关
9. 再读取 `agents/frontend-engineer-agent.md`，基于 `03-16` 固定模板生成最终 HTML
10. 交付前按 `reference/user-rules.md` 验收

## 页面层面的预期

最终页面应继续保留：

1. 右上角主题切换按钮
2. Header / Hero
3. 4 张统计卡
4. 今日洞察
5. 今日热门 Top 12
6. 编程语言分布
7. GitHub Explore 精选
8. Footer

## Top 详情区的预期

每个项目的展开详情应继续保持：

1. `项目摘要`
2. `核心特性`
3. `技术栈`
4. `适用场景`
5. `一句话推荐`

并且这些内容必须忠实来自 Markdown 底稿，不能在 HTML 阶段被二次压缩成空话。

## 反例

下面这些都不符合当前 skill：

- 先设计一张新的日报页面，再把数据塞进去
- 没有本地 Markdown 底稿，直接边想边拼 HTML
- 跳过 `user-rules.md` 和固定模板，按自己理解改 UI
- 调用 Python、本地脚本或固定渲染器去生成最终 HTML
- 把 Explore 区改成卡片墙
- 把详细解读区改成新的命名或新的展开结构
