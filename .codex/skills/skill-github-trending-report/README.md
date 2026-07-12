# skill-github-trending-report

Generate a GitHub Trending daily report with a fixed-template workflow:

- fetch GitHub Trending / Explore and repo evidence
- create a local Markdown source document first
- reuse `reference/fixedBaseTemplate_2026-03-16.html` as the HTML base
- keep the accepted UI/theme/detail layout intact
- only replace daily content and data

## Core References

- `reference/user-rules.md`
- `reference/fixedBaseTemplate_2026-03-16.html`
- `reference/uiEngineeringSpec.md`
- `reference/reportMarkdownTemplate.md`

## Agent Flow

- `agents/markdown-report-writer-agent.md`: writes the local Markdown draft
- `agents/ui-ux-designer-agent.md`: guards template fidelity and density
- `agents/frontend-engineer-agent.md`: maps the Markdown draft into the fixed HTML base

## Non-Negotiables

- generate Markdown before HTML
- do not redesign the page
- do not replace the accepted `03-16` layout or naming
- do not use Python or a local renderer to author the final HTML
- keep the expandable Top 12 detail structure
- keep user-facing Chinese project interpretation specific and easy to understand

See `SKILL.md` for the full workflow and acceptance rules.
