---
title: "Stop Investing in the AI Layer"
format: newsletter
idea_source: content/ideas/backlog/invest-underneath-ai-layer-idea-2026-04-30.md
created: 2026-04-30
stage: draft
style: benedict-evans-analytical
---

## Stop Investing in the AI Layer

Every leadership team I'm talking to right now is being pitched the same thing: agent platforms, AI orchestration tools, autonomous workflow vendors. The instinct is to pick one and commit before you fall behind. That instinct is wrong.

The AI tooling layer is churning faster than any procurement cycle can keep up with. Whatever you commit to in Q2 will look dated by Q4. The defensible move is the opposite of what the market is pushing: invest in the layers that don't change, and keep the AI layer swappable.

The AI layer is where the noise is. The infrastructure underneath it is where the durable value lives.

## 📊 The Four Layers

There's a useful way to think about this. Every AI-enabled operation, regardless of industry or team size, sits on a four-layer stack. Bottom to top:

**Layer 1: Data spine.** A canonical record for the thing your business actually runs on. Campaign, customer, project, deal — whatever your unit of work is. Single source of truth. Referenced by everything downstream. This is the layer most organizations skip because it's unglamorous, and it's the layer whose absence makes everything above it fragile.

**Layer 2: Context engine.** Structured and unstructured knowledge made accessible to AI. This is where organizational memory lives — stable reference data (brand guidelines, process documentation, product specs) combined with dynamic retrieval (recent conversations, live project state, customer history). The quality of this layer determines whether your AI tools produce generic output or contextually aware work.

**Layer 3: Orchestration.** The automation and routing that moves work between people and systems. Triggers, handoffs, approval flows, scheduling. This is the coordination layer — it doesn't do the thinking, but it determines what gets thought about, when, and by whom.

**Layer 4: Agent layer.** The AI that actually reads, writes, and acts. The models, the interfaces, the agent frameworks. This is where all the venture capital is flowing and all the marketing noise is concentrated.

Here's the critical distinction: Layers 1 and 2 are infrastructure. Layers 3 and 4 are tools. Tools change. Infrastructure shouldn't.

## 🔧 Why This Is the Only Strategy That Survives

The useful exercise is to stress-test this architecture against every plausible future scenario and see what breaks.

A new model provider opens up enterprise access. The agent layer gets better overnight. Your data spine doesn't change. Your context engine doesn't change. Your integrations plug into the new provider directly. You upgrade in days, not quarters.

Your orchestration platform gets acquired or pivots. You swap it out. The triggers fire from the same data layer. The handoffs route to the same systems. The disruption is contained to one layer.

A new agent framework eats the current category. You adopt it. Your context retrieval patterns transfer. Your data model is unchanged. The investment in layers 1 and 2 compounds rather than resets.

Every plausible future change is absorbed by the top two layers. The bottom two are the investment. This isn't a theoretical preference for clean architecture. It's a practical observation about where the volatility actually lives in the current market.

The obvious objection is timing: "I need an AI capability now." Right — and you can have one. Composable architecture doesn't mean delayed value. It means the agent you ship in Q2 doesn't become technical debt in Q4 because the layers underneath it are stable. The work compounds instead of getting redone.

## 💡 MCP Is What Makes This Real

Composability has been an architectural ideal forever. The reason it's actually achievable now is MCP — the Model Context Protocol — and the ecosystem emerging around it.

Without a standard protocol, every agent integration is bespoke. Migration costs are enormous. Switching AI providers means rebuilding your entire integration surface. With MCP, the agent layer becomes genuinely swappable because the integration plumbing is portable.

The MCP servers you build today are an asset that survives whatever model or agent platform wins. They expose your data and context to any compliant agent. That's the mechanism that turns composable architecture from a whiteboard diagram into something you can actually build and ship against.

This is what I'm spending the most time on in my own client work right now. Not because MCP is the most exciting technology in the stack, but because it's the layer that makes everything above it interchangeable. The boring infrastructure decision turns out to be the highest-leverage one.

## 🎯 What This Means for Who You Hire

If your AI capability lives in the swappable layer, the hiring implications follow directly. You don't hire for a specific platform. You hire for the layers that persist.

Three skill categories that pay off regardless of which AI tools win:

**Data modeling and schema design.** Someone who can design your spine — the canonical record and how it relates to everything else. This is unsexy and underrated. It's also the highest-leverage hire you'll make. The person who gets your data model right saves every downstream team months of rework when the agent layer inevitably shifts.

**Context engineering.** Someone who knows how to structure organizational knowledge so AI can actually use it. This is less about prompting and more about taxonomy, retrieval design, and the boundary between curated stable context and dynamic retrieval. It's a new discipline, and the people who are good at it are currently being hired as "prompt engineers" — which undersells the role by an order of magnitude.

**Integration architecture.** Someone who thinks in protocols, APIs, and webhooks. The person who builds your MCP servers and your downstream sync. This role gets more valuable every quarter, not less, because the number of systems that need to talk to AI is only growing.

The job title that won't age well: "Head of [specific AI platform]." If your AI org chart is built around a vendor, you've inherited their lifespan.

## The Takeaway

The teams that win the next 18 months won't be the ones with the best AI tools. They'll be the ones whose AI tools are the most easily replaced.

The market is pushing you to commit to the top of the stack. The durable strategy is to invest at the bottom and keep the top interchangeable. Data spine. Context engine. Portable integrations. Everything else is a feature, not a foundation.

What are you investing in right now that you'd struggle to swap out in six months?

Jon
