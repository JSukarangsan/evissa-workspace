---
title: "AGENTS.md is the New README"
type: linkedin-post
idea_ref: content/ideas/backlog/agents-md-new-readme-idea-2026-04-16.md
stage: draft
created: 2026-04-17
pillar: "Context Over Tools"
angles: [portability, enterprise-governance, contrarian]
---

OpenAI and Anthropic now both use a file called AGENTS.md to give AI agents their operating instructions.

If you're not deep in the agent world, here's why that matters.

When you set up an AI agent today, you have to tell it how to behave. What it's allowed to do, what to avoid, how to approach the work. Until now, those instructions lived in vendor-specific config files. CLAUDE.md for Claude. .cursorrules for Cursor. Each tool had its own format, its own syntax, its own rules.

That meant your agent instructions were fused to the tool running them. The what ("here's how to do the job") was tangled up with the where ("and it only works in this one product").

AGENTS.md separates those two things.

It's a single file that describes what you want the agent to do, independent of which platform runs it. One set of instructions. Any runtime. Your operational intent is no longer locked to a vendor.

This is the same shift that happened with USB. Before USB, every device had its own proprietary connector. Printers, keyboards, cameras, all different. USB didn't make those devices better. It just meant you could plug anything into anything. AGENTS.md is doing that for AI agents. One standard interface for operational instructions.

👉 Here's where it gets strategic

Most teams building agents right now don't realize they're making an architecture decision every time they write a config file. They're encoding operational knowledge in a format that only works with one tool. That's lock-in. Not the dramatic kind. The slow kind that costs you six months of rework when you switch providers.

Teams writing AGENTS.md files are making a different bet. They're investing in portable context. Instructions that travel with the project, not the tool. That's not just a developer convenience. It has real implications for procurement, governance, and how you evaluate AI vendors.

The bigger signal here: the industry is standardizing how we control agents, not which model powers them. That's a meaningful shift. It means the operational layer — the rules, boundaries, and behaviors you define — is becoming the durable part of your AI investment. The model underneath can change.

README.md started as a convention and became the universal way software projects communicate what they are. AGENTS.md is on the same path. Except this time the audience isn't developers. It's agents.

The teams that get this right early will build context architecture that compounds. Everyone else will be rewriting configs every time they switch tools.

Context over tools. Always.
