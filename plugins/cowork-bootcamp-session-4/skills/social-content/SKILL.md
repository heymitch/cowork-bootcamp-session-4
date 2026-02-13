---
name: social-content
description: Generate social media posts for LinkedIn and X in your voice — thought leadership, threads, carousels. Say "Write a LinkedIn post about [topic]" or "Turn this into an X thread".
---

# Social Content

Give it a topic, idea, or raw note — it writes platform-specific posts that sound like you. LinkedIn thought leadership, X singles, threads, carousels, or a full week of content.

## How to Run

- "Write a LinkedIn post about [topic]"
- "Turn this idea into an X thread: [idea]"
- "Create a week of social posts from my recent notes"

---

## Preflight Check (Run Silently)

### 1. Config check
Read `config.md` from project root.
- **Missing:** Stop. Say: "Say **'Run my business blueprint'** first — takes 5 minutes."
- **Exists:** Continue.

### 2. Voice check
Check config.md for `- [x] Voice Training completed`.
- **Unchecked:** Stop. Say: "Say **'Train on my voice'** first so this sounds like you."
- **Checked:** Load Voice Profile. Wrap all content generation with `<VOICE>{profile}</VOICE>`.

### 3. Notion check (silent)
- **Notion tools found:** Save drafts to Notion content calendar. Update checkbox if unchecked.
- **No Notion tools:** Save as local files. Don't mention Notion.

### 4. All clear — proceed without announcing.

---

## The Process

### Step 1: Get the Input
Takes: a topic, idea, raw notes, or "scan my recent Notion notes" if connected.
If the topic is vague, ask one clarifying question before writing.

### Step 2: Pick the Platform + Format
If user didn't specify, match to content:
- Deep insight or teaching → **LinkedIn post** (1,500-2,200 chars)
- Punchy take → **X single** (≤280 chars)
- Multi-point idea → **X thread** (5-12 posts) or **LinkedIn carousel**
- "Give me a week" → **Weekly batch** (3-5 posts, mixed platforms)
Confirm choice before writing. See `references/platform-rules.md`.

### Step 3: Pick the Format Style
For LinkedIn, select from 5 proven styles in `references/linkedin-formats.md`:
- Process/how-to → **Steps**
- Data/results → **Stats**
- Pitfalls/warnings → **Mistakes**
- Reflections/experience → **Lessons**
- Proof/case studies → **Examples**
If unclear, present top 2 with sample hooks and let user choose.

### Step 4: Write the Draft
Using voice profile + platform rules + format style:
- Apply `<VOICE>{Voice Template}</VOICE>` wrapper
- Hook in first 2 lines (before the fold)
- One idea per post
- End with engagement prompt or CTA

### Step 5: Quality Check (Silent)
Before showing: run the Surprise Test. Would this surprise someone who's read 10 posts on this topic? If not, sharpen the angle. Check for AI patterns — zero tolerance.

### Step 6: Show Draft
Present with platform, format style, and character count labeled.
**Do not save yet.** Wait for approval or edits.

### Step 7: Save
On approval: save to Notion content calendar or local `content/YYYY-MM/DD-[slug].md`.

## Rules

- Always use the voice profile. Generic = you skipped something.
- Human writing rules: no AI patterns, vary sentence length, specific over vague.
- Never post directly — draft only, user reviews and publishes.
- No fabricated stats, fake testimonials, or hallucinated examples.
- For weekly batches: 40% thought leadership, 35% tactical, 25% story.
