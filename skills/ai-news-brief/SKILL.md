---
name: ai-news-brief
description: 获取最新 AI 新闻速报。搜索并汇总近期最热门的人工智能新闻，提供简洁摘要和来源链接。适用于：(1) 用户询问 AI 新闻、AI 动态、科技新闻时，(2) 用户说"新闻速报"、"AI 资讯"、"今日 AI"等，(3) 定时任务需要获取 AI 新闻摘要时。默认使用中文输出。
---

# AI 新闻速报

获取并汇总最新的人工智能领域新闻。

## 工作流程

1. 使用 `web_search` 搜索最新 AI 新闻
2. 对重要新闻使用 `web_fetch` 获取详细内容
3. 整理成简洁的新闻速报格式

## 搜索策略

```bash
# 主要搜索词（英文源，覆盖面广）
web_search "AI artificial intelligence news" --freshness pd --count 10

# 补充搜索（特定领域）
web_search "OpenAI Google DeepMind Anthropic news" --freshness pd --count 5
web_search "LLM GPT Claude Gemini news" --freshness pd --count 5
```

## 输出格式

```markdown
🤖 **AI 新闻速报 (YYYY年MM月DD日)**

---

**1. 📌 [新闻标题]**
[2-3句简洁摘要，说明核心内容和影响]
🔗 来源: [来源名称]

---

**2. 💡 [新闻标题]**
[摘要内容]
🔗 来源: [来源名称]

---

[继续3-5条新闻...]
```

## 图标使用

根据新闻类型选择合适的图标：
- 🇪🇺 🇺🇸 🇨🇳 🇮🇳 - 政策/地区相关
- 💸 📈 - 投资/商业
- 📜 ⚖️ - 法规/版权
- 🎵 🎨 🎬 - 创意/娱乐应用
- 🔬 🧪 - 研究/技术突破
- 🚀 📱 - 产品发布
- ⚠️ 🛡️ - 安全/风险

## 参数

- **数量**: 默认 3-5 条，可根据用户要求调整
- **时间范围**: 默认过去 24 小时 (`pd`)，可选过去一周 (`pw`)
- **语言**: 默认中文输出，可根据用户偏好调整

## 质量要求

- 优先选择高影响力、高可信度的新闻源 (The Verge, TechCrunch, Reuters, etc.)
- 避免重复报道同一事件
- 摘要要简洁但信息完整
- 始终注明来源
