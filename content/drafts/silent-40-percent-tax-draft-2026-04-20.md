---
title: "The Silent 40% Tax"
format: linkedin-post
idea_source: content/ideas/backlog/silent-40-percent-tax-opus-4.7.md
created: 2026-04-20
status: draft
---

Opus 4.7 uses ~1.46x more tokens than 4.6 for the same prompt.

Same price per token. Nobody changed the pricing page. But your bill just went up 40%.

Simon Willison ran the numbers this weekend. Identical inputs, new tokenizer, significantly more tokens consumed. If your team upgraded to 4.7 without adjusting anything else, you're paying more for the same work.

Now multiply that across an org.

500 employees. Each running 50 prompts a day. Most of those prompts are routine stuff that Haiku handles fine. But nobody set up routing tiers. Nobody capped model selection. Everyone defaults to the biggest model because that's what the dropdown shows.

🎯 The math nobody's doing

Take a team spending $15k/month on Claude API calls. Upgrade to 4.7 without changing routing, that's $21k. Same output. Same quality on 80% of tasks. Extra $6k/month evaporating into tokenizer overhead.

Over a quarter that's $18k. For one team.

This is what I mean when I talk about AI operations. It's not a model problem. It's a governance problem. And most orgs don't even have visibility into per-team spend, let alone per-model routing logic.

Here's what cost governance without bureaucracy looks like in practice:

• Tier 1: Haiku for summarization, formatting, simple Q&A (pennies)
• Tier 2: Sonnet for analysis, drafting, code review (dollars)
• Tier 3: Opus for complex reasoning, architecture decisions (tens of dollars)
• Tier 4: Extended thinking for novel problems only (budget requires approval)

I run this exact routing for my own work. Routine tasks hit Haiku. General work goes to Sonnet. Opus only when the problem actually demands it. My costs are a fraction of what they'd be running everything through the top model.

The teams getting 10x returns from AI aren't using better models. They're routing smarter.

How many of you actually know what your org spends per model tier?
