---
title: "Stop Investing in the AI Layer. Invest in What's Underneath It."
source: original thought (Jon dictated)
formats: [linkedin-post]
stage: backlog
created: 2026-04-30
tags: [ai-operations, composable-architecture, mcp, data-infrastructure, context-engineering, hiring, ai-strategy]
priority: NOW
q2_pillar: "Context Over Tools / Leverage Architecture"
---

## Raw Content (Jon's Draft)

Stop investing in the AI layer. Invest in what's underneath it.

Every leadership team I'm talking to right now is being pitched the same thing: agent platforms, AI orchestration tools, autonomous workflow vendors. The instinct is to pick one and commit before you fall behind.

That's the wrong move.

The AI tooling layer is churning faster than any procurement cycle can keep up with. Whatever you commit to in Q2 will look dated by Q4. The defensible move is the opposite of what the market is pushing — invest in the layers that don't change, and keep the AI layer swappable.

The AI layer is where the noise is. The infrastructure underneath it is where the durable value lives.

The four layers, bottom to top:

Layer 1 — Data spine. A canonical record for the thing your business actually runs on. Campaign, customer, project, deal — whatever your unit of work is. Single source of truth. Referenced by everything downstream.

Layer 2 — Context engine. Structured and unstructured knowledge made accessible to AI. Stable reference data plus dynamic retrieval.

Layer 3 — Orchestration. The automation and routing that moves work between people and systems.

Layer 4 — Agent layer. The AI that actually reads, writes, and acts.

Layers 1 and 2 are infrastructure. Layers 3 and 4 are tools. Tools change. Infrastructure shouldn't.

Why this is the only strategy that survives

Stress-test it against any plausible scenario.

A new model provider opens up enterprise access. The agent layer gets better overnight. Your data spine doesn't change. Your context engine doesn't change. Your integrations plug into the new provider directly.

Your orchestration platform gets acquired or pivots. You swap it out. The triggers fire from the same data layer. The handoffs route to the same systems.

A new agent framework eats the current category. You adopt it. Your context retrieval patterns transfer. Your data model is unchanged.

Every plausible future change is absorbed by the top two layers. The bottom two are the investment.

The obvious objection: "but I need an AI capability now." Right — and you can have one. Composable architecture doesn't mean delayed value. It means the agent you ship in Q2 doesn't become technical debt in Q4 because the layers underneath it are stable. The work compounds instead of getting redone.

MCP is what makes this real

Composability has been an architectural ideal forever. The reason it's actually achievable now is MCP and the protocols emerging around it.

Without a standard protocol, every agent integration is bespoke and migration costs are huge. With MCP, the agent layer becomes genuinely swappable because the integration plumbing is portable.

The MCP servers you build today are an asset that survives whatever model or agent platform wins. They expose your data and context to any compliant agent. That's the mechanism that turns composable architecture from a whiteboard diagram into something you can actually build against.

This is why I'm spending so much time on MCP work specifically. It's the layer that makes everything above it interchangeable.

What this means for who you hire

If your AI capability lives in the swappable layer, you don't hire for a specific platform. You hire for the layers that persist.

Three skill categories that pay off regardless of which AI tools win:

Data modeling and schema design. Someone who can design your spine — the canonical record and how it relates to everything else. This is unsexy and underrated. It's also the highest-leverage hire you'll make.

Context engineering. Someone who knows how to structure organizational knowledge so AI can use it. Less about prompting, more about taxonomy, retrieval design, and the boundary between curated stable context and dynamic retrieval.

Integration architecture. Someone who thinks in protocols, APIs, and webhooks. The person who builds your MCP servers and your downstream sync. This role gets more valuable every quarter, not less.

The job title that won't age well: "Head of [specific AI platform]." If your AI org chart is built around a vendor, you've inherited their lifespan.

The teams that win the next 18 months won't be the ones with the best AI tools. They'll be the ones whose AI tools are the most easily replaced.

What are you investing in right now that you'd struggle to swap out in six months?

## Notes

- This is nearly post-ready as-is. Jon wrote this directly.
- Strong framework piece (4-layer model). Could become signature framework.
- MCP section ties directly to Jon's NYT work and daily practice.
- Hiring section adds practical dimension beyond architecture.
- Consider: LinkedIn post as-is, or split into LinkedIn (shorter) + newsletter (full version)?
- The 4-layer diagram is a strong visual candidate.

## Strategic Alignment

- Core Q2 thesis: Context Over Tools, Leverage Architecture
- Directly supports "context is the new infrastructure" positioning
- Build-in-public angle: Jon's MCP work is the proof
- Target: Product leaders, VPs Eng, CTOs making AI infrastructure decisions
