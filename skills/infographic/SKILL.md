# Skill: Infographic Creation

Generate infographics as HTML → screenshot PNG for LinkedIn posts and content.

## When to Use
- User asks for an infographic, diagram, or visual to accompany content
- Content needs a visual explainer (timelines, comparisons, frameworks, flows)

## Visual Style: "Academic Diagram"

The style is intentionally unpolished. It should feel like a smart person's whiteboard sketch that got cleaned up just enough to share. First impression = insight, not design.

### Core Principles
1. **Less polish, more meaning.** Never look "designed." Look like a diagram from a great textbook.
2. **One idea per image.** Don't cram everything in. Pick the single most powerful visual concept.
3. **Whitespace is the main element.** Let things breathe. Generous margins and spacing.
4. **Simple geometric shapes only.** Circles, rectangles with thin borders, lines, arrows. No rounded cards, no shadows, no gradients.

### Color Palette
- **Background:** Warm cream/off-white (`#f5f2eb` or similar paper tone)
- **Primary text:** Near-black (`#1a1a1a`)
- **Secondary text:** Warm gray (`#888` to `#999`)
- **Accent 1 (primary):** Terracotta/warm red-orange (`#c85a3a` or similar) — use sparingly for the key element
- **Accent 2 (optional):** Muted blue (`#5b7fbf`) or black — only when a second category is needed
- **Lines/borders:** Light warm gray (`#ccc` to `#ddd`), thin (1-2px)
- **Rule:** Maximum 2 accent colors per infographic. Often just 1.

### Typography
- **Font:** System sans-serif (`-apple-system, 'Helvetica Neue', Arial, sans-serif`) — or a clean serif for titles when appropriate
- **Title:** Large, bold, simple. Can be centered or left-aligned. No eyebrow text, no subtitles unless essential.
- **Labels:** Clean, often lowercase or sentence case. Never all-caps shouting. Italic for secondary descriptors.
- **Weight contrast:** Bold for primary labels, regular/light for descriptions. Let weight do the hierarchy work, not size.
- **Size range:** Keep it tight. Title 28-36px, labels 16-20px, descriptions 13-15px. Don't use huge display sizes.

### Layout Patterns
- **Flow diagrams:** Boxes connected with thin arrows (→), dashed lines for indirect relationships
- **Venn diagrams:** Simple circle outlines (2-3px stroke), labels inside, minimal fill (just the key intersection)
- **Timelines:** Horizontal line with labeled points, vertical dashed dividers for phases
- **Curves/charts:** Simple SVG lines, labeled phases above, no grid, no axes unless essential
- **Comparisons:** Side-by-side boxes or a simple table with thin rules

### Shape Rules
- Rectangles: Thin border (1-2px), slight rounding (4-6px max, not 12-16px), mostly no fill or very light fill
- Circles: Stroke only (2-3px), no fill unless highlighting an intersection
- Arrows: Simple, thin. Use `→` character or SVG lines with small arrowheads. Dashed for indirect relationships.
- One element gets the accent fill (solid background) — this is the focal point

### What to Avoid
- ❌ Card-based layouts (looks like a dashboard/webapp)
- ❌ Dark themes
- ❌ Gradients, shadows, glows
- ❌ Multiple font sizes competing for attention
- ❌ Icons or emoji
- ❌ Stats grids or "metric cards"
- ❌ Rounded corners > 6px
- ❌ More than 2 accent colors
- ❌ Dense text — if you need paragraphs, it's not an infographic

## Technical Process

### Step 1: Choose the Diagram Type
Pick ONE visual concept from the content:
- A flow/progression → flow diagram
- Overlapping concepts → venn diagram
- Evolution over time → timeline or curve
- Comparison → side-by-side
- System/architecture → boxes + arrows

### Step 2: Write the HTML
- Create at `content/drafts/YYYY-wWW/<slug>-infographic.html`
- Size: 1080px wide (LinkedIn optimal), height auto based on content
- Use inline CSS, no external dependencies except Google Fonts if needed
- Keep the DOM simple — the fewer elements, the better

### Step 3: Screenshot with Puppeteer
```javascript
const puppeteer = require('puppeteer-core');
(async () => {
  const browser = await puppeteer.launch({
    headless: true,
    executablePath: '/usr/bin/chromium',
    args: ['--no-sandbox', '--disable-setuid-sandbox', '--disable-gpu']
  });
  const page = await browser.newPage();
  await page.setViewport({ width: 1080, height: 1600 });
  await page.goto('file:///path/to/infographic.html', { waitUntil: 'networkidle0' });
  const body = await page.$('body');
  const bbox = await body.boundingBox();
  const h = Math.ceil(bbox.height);
  await page.screenshot({
    path: '/path/to/infographic.png',
    clip: { x: 0, y: 0, width: 1080, height: h }
  });
  await browser.close();
})();
```

### Step 4: Upload
Upload the PNG to the appropriate Slack thread using message tool with `upload-file`.

## Style Reference
Reference images saved at: `skills/infographic/references/`
- Anthropic "advisor strategy" flow diagram (boxes + arrows, cream bg, terracotta accent)
- Venn diagram (circle strokes, lowercase labels, cream bg, blue/orange/black)
- Leverage curve (simple SVG curves, labeled phases, gray + terracotta)
- Simple venn (thin circle strokes, peach bg, one blue highlight fill)

## Style Modes

Two visual modes available. Default to light unless Jon specifies.

### Light Mode (default)
The academic diagram style described above. Cream background, terracotta accent, thin borders, textbook feel.

### Dark Mode
A darker, more technical feel. Use when Jon asks for "dark mode" or when the content skews more developer/infrastructure-oriented.

#### Dark Mode Palette
- **Background:** Near-black (`#0F1117`)
- **Card backgrounds:** Dark slate (`#1E293B` to `#1a2332`)
- **Primary text:** Light gray (`#E2E8F0`, `#CBD5E1`)
- **Secondary text:** Muted gray (`#94A3B8`)
- **Accent:** Blue (`#3B82F6` to `#60A5FA`) — used for the focal layer, borders, highlights
- **Accent text:** Light blue (`#93C5FD`, `#BFDBFE`)
- **Borders:** Subtle white (`rgba(255,255,255,0.06-0.08)`)
- **Tags:** Pill-shaped, subtle fill (`rgba(255,255,255,0.06)` or `rgba(96,165,250,0.15)` for accent)

#### Dark Mode Principles
- Cards/layers with subtle background fills, not bordered boxes
- Blue glow/accent lines on the focal element (top + bottom borders)
- Badges for status labels (e.g. "✦ DURABLE", "↕ SWAPPABLE")
- Tags as rounded pills with low-opacity fills
- Generous padding inside cards
- Footer attribution in muted color
- Still follows the core rule: one focal point, minimal elements, whitespace

#### Dark Mode Reference
See first-pass v1 of the AGENTS.md infographic: `content/drafts/2026-w16/agents-md-infographic-dark-v1.html`

## Quality Checklist
Before delivering:
- [ ] Could this be a page from a textbook? (yes = good)
- [ ] Is there one clear focal point with the accent color?
- [ ] Would removing any element make it worse? (if not, remove it)
- [ ] Is there enough whitespace that it feels calm?
- [ ] Does it communicate the idea in <3 seconds?
