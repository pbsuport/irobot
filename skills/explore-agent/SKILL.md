---
name: explore-agent
description: Deep research agent for exploring topics thoroughly. Use when: (1) user asks to "research", "explore", "investigate", or "dig into" a topic, (2) user needs comprehensive information on a subject, (3) user wants to understand something in depth with multiple sources, (4) user says "explore agent" or "research this". Provides structured, multi-source research with citations.
---

# Explore Agent

Deep-dive research agent that gathers comprehensive information on any topic.

## Workflow

1. **Understand the query** - Identify the core topic and research angles
2. **Multi-source fetch** - Gather information from multiple authoritative sources in parallel
3. **Synthesize findings** - Combine and analyze information from all sources
4. **Structured output** - Present findings in a clear, organized format with citations

## Research Strategy

### Step 1: Identify Sources

Based on the topic, select 3-5 relevant sources:
- **Tech/AI topics**: The Verge, Ars Technica, TechCrunch, Wired, official docs
- **General news**: Reuters, AP News, BBC, NPR
- **Science**: Nature, Science, arXiv, university sites
- **Business**: Bloomberg, Financial Times, WSJ
- **Documentation**: Official project sites, GitHub, MDN, Stack Overflow

### Step 2: Parallel Fetch

Use `web_fetch` in parallel for all sources:

```bash
# Example: researching a tech topic
web_fetch "https://source1.com/topic" --maxChars 8000
web_fetch "https://source2.com/topic" --maxChars 8000
web_fetch "https://source3.com/topic" --maxChars 8000
```

If `web_search` is available, use it first to find the best URLs:

```bash
web_search "topic query" --count 5
```

### Step 3: Deep Dive (Optional)

If initial sources aren't sufficient:
- Follow links mentioned in fetched content
- Search for specific aspects that need clarification
- Look for primary sources (papers, official announcements)

## Output Format

```markdown
# 🔍 Research: [Topic]

## Overview
[2-3 paragraph executive summary of findings]

## Key Findings

### [Finding 1 Title]
[Details with specific facts, data, quotes]
📎 Source: [Source Name]

### [Finding 2 Title]
[Details]
📎 Source: [Source Name]

[Continue for all major findings...]

## Analysis
[Your synthesis - connections between findings, implications, what it means]

## Open Questions
[What remains unclear or needs further research]

## Sources
- [Source 1 with URL]
- [Source 2 with URL]
- [Source 3 with URL]
```

## Research Principles

- **Verify claims** - Cross-reference important facts across sources
- **Note conflicts** - If sources disagree, highlight the discrepancy
- **Date awareness** - Note publication dates; prefer recent information
- **Primary over secondary** - Prefer original sources over aggregators
- **Cite everything** - Always attribute information to its source
- **Acknowledge gaps** - Be clear about what you couldn't find

## Parameters

- **Depth**: shallow (3 sources) | normal (5 sources) | deep (8+ sources)
- **Focus**: broad overview | specific aspect | comparison
- **Output length**: brief | standard | comprehensive
