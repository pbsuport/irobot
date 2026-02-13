---
name: ai-news-brief-en
description: Get the latest AI news briefing in English. Fetches and summarizes the hottest artificial intelligence news with concise summaries and source links. Use when: (1) user asks for AI news, tech news, or AI updates, (2) user says "news brief", "AI news", "tech update", etc., (3) scheduled tasks need an AI news summary. Output in English.
---

# AI News Brief

Fetch and summarize the latest artificial intelligence news.

## Workflow

1. Use `web_fetch` to directly scrape reliable news sources (skip web_search)
2. Compile into a concise news brief format

## Fetching Strategy (Fast Mode)

Directly fetch from these news sources, **execute in parallel** for speed:

```bash
# Primary source - The Verge AI page (most comprehensive)
web_fetch "https://www.theverge.com/ai-artificial-intelligence" --maxChars 12000

# Secondary source - Platformer (many exclusives)
web_fetch "https://www.platformer.news/" --maxChars 4000
```

**Note**: Both web_fetch calls should be in the same tool call block for parallel execution.

## Output Format

```markdown
🤖 **AI News Brief (Month DD, YYYY)**

---

**1. 📌 [Headline]**
[2-3 sentence summary explaining the core content and impact]
🔗 Source: [Source Name]

---

**2. 💡 [Headline]**
[Summary content]
🔗 Source: [Source Name]

---

[Continue with 3-5 news items...]
```

## Icon Usage

Choose appropriate icons based on news type:
- 🇪🇺 🇺🇸 🇨🇳 🇮🇳 - Policy/Regional
- 💸 📈 - Investment/Business
- 📜 ⚖️ - Regulation/Copyright
- 🎵 🎨 🎬 - Creative/Entertainment applications
- 🔬 🧪 - Research/Technical breakthroughs
- 🚀 📱 - Product launches
- ⚠️ 🛡️ - Safety/Risk

## Parameters

- **Count**: Default 3-5 items, adjustable per user request
- **Language**: English output

## Quality Requirements

- Prioritize high-impact, high-credibility news
- Avoid duplicate reporting of the same event
- Summaries should be concise but informationally complete
- Always cite sources
