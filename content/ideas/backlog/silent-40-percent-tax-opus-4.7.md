# The Silent 40% Tax — What Happens When 500 Employees Upgrade to Opus 4.7 Without Guardrails

- **Priority:** NOW
- **Type:** Thought leadership
- **Source:** [Simon Willison's Claude token counter analysis](https://simonwillison.net/2026/Apr/20/claude-token-counts/) (Apr 20)
- **Created:** 2026-04-20

## Hook

Opus 4.7's new tokenizer uses ~1.46x more tokens than 4.6 for identical prompts. Same price per token. Teams upgrading without model routing are paying 40% more and nobody's flagging it.

## Angle

Most orgs rolling out Claude to large employee populations have zero cost visibility at the individual level. No routing tiers, no usage caps, no model selection guidance. A team of 500 casual users each running 50 prompts/day on Opus 4.7 instead of Haiku for routine tasks = potentially tens of thousands/month in unnecessary spend.

The post walks through the math, shows what "cost governance without bureaucracy" looks like in practice, and gives teams a 4-tier model routing framework they can implement in a week.

## Why It Works

Specific numbers (Willison's 1.46x data), a problem every scaling team will hit, and a practical framework — not just "be careful with costs." Positions Jon as the person who thinks about AI operations at the team level, not just the model level.
