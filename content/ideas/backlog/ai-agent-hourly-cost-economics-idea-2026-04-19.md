---
title: "The Number Nobody's Tracking: What AI Agents Actually Cost Per Hour"
source: "https://www.tobyord.com/writing/hourly-costs-for-ai-agents"
formats: [linkedin-post, newsletter]
stage: backlog
created: 2026-04-19
tags: [ai-economics, ai-agents, cost-analysis, ai-operations, metr, time-horizons, roi]
priority: NOW
q2_pillar: "AI Operations for Product Teams"
---

## Key Concepts
- Toby Ord's analysis reveals a critical blind spot: while METR time horizons (how long a task an AI can handle) grow exponentially, the *cost* of running agents at those horizons is also growing — and possibly faster
- Each model has a "sweet spot" — the hourly rate where you get the best cost-per-capability. Ranges wildly: $0.40/hr (Grok 4, Sonnet 3.5) to $40/hr (o3). But at their maximum capability, models can cost $120-350/hr — more than a human engineer
- The F1 analogy is sharp: METR benchmarks show what's *possible*, not what's *practical*. Cutting-edge performance requires lavish compute spend that doesn't reflect real-world economics
- Diminishing returns are real. Every model plateaus. Throwing more tokens at a task doesn't linearly improve outcomes — it hits a wall, and the marginal cost per capability unit explodes
- For product teams: this means model selection and task routing aren't just technical decisions, they're economic ones. The "best" model is often not the right model for the job

## Content Angles
- Angle 1: *The economics nobody's doing.* Everyone tracks model capability. Almost nobody tracks cost-per-hour-of-useful-work. Product teams making AI decisions without this math are flying blind
- Angle 2: *Why "just use the best model" is bad strategy.* GPT-5 at $13/hr for 45-min tasks vs $120/hr for 2-hr tasks. Same model, 10x cost difference depending on task. This is an operations problem, not a model problem
- Angle 3: *The cost routing discipline.* This is exactly why Jon routes Haiku for routine, Sonnet for general, Opus sparingly. Build-in-public angle: show the actual cost discipline behind real AI operations
- Angle 4: *When AI agents cost more than humans.* o3 at $350/hr for tasks at its ceiling — and it fails 50% of the time. That's the headline nobody wants to publish

## Possible Hooks
- Hook 1 (direct): "AI agents can cost $350 per hour. And fail half the time. We need to talk about economics, not just capability."
- Hook 2 (practical): "I route routine tasks to a $0.40/hr model and complex work to a $40/hr model. Most teams don't even know there's a 100x cost difference."
- Hook 3 (framework): "There's a number that should be on every product team's dashboard: cost per hour of useful AI work. Almost nobody tracks it."

## Strategic Alignment
- Q2 pillar: AI Operations for Product Teams — cost routing and model economics are core operational disciplines
- Target audience: Product leaders, eng managers, ops leads making AI infrastructure decisions
- Content type: Thought leadership + framework (with specific numbers)
- Reinforces Jon's "specific numbers and outcomes" brand — this is exactly the kind of analysis that separates operators from commentators
- Build-in-public opportunity: Jon's own cost routing discipline (Haiku/Sonnet/Opus) is a micro-example of this macro trend
