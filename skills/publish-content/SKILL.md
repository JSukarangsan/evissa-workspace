---
name: publish-content
description: >
  Publishes approved content to external platforms. Handles LinkedIn posting,
  Kit newsletter publishing, and Typefully X/Twitter scheduling.
  Only runs after explicit approval in #drafts-review.
version: 1.0.0
metadata:
  openclaw:
    always: false
    emoji: "🚀"
---

# Publish Content

You handle the final step: publishing approved content to external platforms.

## Trigger

- Called by draft-review skill after Jon approves a draft
- Jon explicitly says "publish [draft]" or "schedule [draft]"

## Platform Handlers

### LinkedIn
1. Format the draft for LinkedIn (strip any markdown, ensure native formatting)
2. Confirm with Jon one final time: "Publishing to LinkedIn now. Go?"
3. Post via LinkedIn API or copy-paste confirmation
4. Capture the post URL
5. Post to #published with confirmation and link

### Newsletter (Kit)
1. Ensure draft has:
   - Subject line (ask Jon if missing)
   - Intro paragraph
   - Proper markdown formatting (## headers, **bold**, etc.)
2. Run the Kit publishing script: `node scripts/publish-to-kit.js [draft-path]`
   - Use template ID 4883052
   - Pass `--subject` and `--intro` flags if needed
3. Post to #published with Kit broadcast URL

### Twitter/X (Typefully)
1. Format thread for Typefully (separate tweets with `---`)
2. Schedule via Typefully API
3. Confirm scheduled time with Jon
4. Post to #published with scheduled time

## Post-Publish Actions

After any successful publish:
1. Move draft from `content/drafts/` to `content/published/[platform]-[slug]-[YYYY-MM-DD].md`
2. Add publish metadata to the file header:
   ```yaml
   published: YYYY-MM-DD
   platform: [platform]
   url: [post URL if available]
   ```
3. Archive the source idea file to `content/ideas/archive/`
4. Update any active weekly plan in `content/plans/` to mark as published

## Confirmation Message (#published)

```
🚀 PUBLISHED

Platform: [LinkedIn / Kit Newsletter / X/Twitter]
Title: [title]
Time: [timestamp or scheduled time]
URL: [link]
Source idea: [idea filename]

What's next in the pipeline: [next planned piece from weekly plan]
```

## Safety Rules

- NEVER publish without Jon's explicit approval
- NEVER auto-schedule without confirmation
- If any publish step fails, report the error in #drafts-review immediately
- Always save a local copy before publishing externally
- Double-check that the content matches what Jon approved (no silent edits)
