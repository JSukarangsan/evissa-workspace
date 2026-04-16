---
name: draft-review
description: >
  Manages the content approval workflow in #drafts-review channel.
  Watches for Jon's reactions and replies to drafts, then takes appropriate action:
  approve and publish, revise based on feedback, archive killed ideas, or hold for later.
version: 1.0.0
metadata:
  openclaw:
    always: false
    emoji: "✅"
---

# Draft Review

You manage the approval workflow for content drafts in #drafts-review.

## Trigger

- Jon reacts to a draft message with an emoji
- Jon replies to a draft with text feedback
- Jon says "ship it", "revise", "kill", or "hold"

## Approval Actions

### Approved (👍 reaction, "ship it", "approved", "looks good")

1. Determine the target platform from the draft metadata
2. **LinkedIn**: Hand off to publish-content skill
3. **Newsletter**: Hand off to publish-content skill (Kit publishing)
4. **Twitter/X**: Hand off to publish-content skill (Typefully scheduling)
5. Move idea file from `ready/` to `archive/`
6. Move draft to `content/published/[platform]-[slug]-[YYYY-MM-DD].md`
7. Post confirmation to #published with platform and link
8. React to original draft with checkmark

### Revise ("revise: [feedback]", reply with changes)

1. Extract the specific feedback from Jon's message
2. Trigger draft-content skill with the original idea + Jon's feedback
3. Post revised draft as a **thread reply** (not a new message)
4. Note what changed in the revision

### Kill (❌ reaction, "kill it", "nah", "pass")

1. Move the idea file to `content/ideas/archive/`
2. React to the draft with ❌
3. Reply in thread: "Archived. Moving on."

### Hold ("hold", "save for later", "not yet")

1. Keep draft in `content/drafts/`
2. React with clock emoji
3. Reply in thread: "Holding. I'll resurface this in [X days]."
4. Add to a hold list to resurface during daily digest

## Slack Message Format

### For Published Content (#published)
```
✅ PUBLISHED

Platform: [LinkedIn / Newsletter / Twitter]
Title: [title]
Published: [timestamp]
Link: [URL if available]
```

### For Revisions (thread reply in #drafts-review)
```
✍️ REVISED DRAFT (v[N])

Changes made:
• [What changed based on feedback]

---
[Revised content]
---

React 👍 to approve this version.
```

## Rules

- Never publish without explicit approval
- Always confirm the action taken
- Track revision count (v1, v2, v3...)
- If 3+ revisions on same piece, ask Jon if he wants to rethink the angle entirely
- Keep #drafts-review clean - one active draft per thread
