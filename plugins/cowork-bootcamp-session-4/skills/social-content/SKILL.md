---
name: social-content
description: Generate social media posts for X and LinkedIn in your voice. Say "Write me a LinkedIn post about [topic]" or "Turn this into an X thread".
---

# Social Content

## What This Does

Creates social media posts that sound like you. Give it a topic, a note, or just an idea — it writes platform-specific posts for X and LinkedIn in your voice.

## How to Run

- "Write me a LinkedIn post about [topic]"
- "Turn this idea into an X thread: [idea]"
- "Create a week of social posts from my recent notes"

---

## Preflight Check (Run Every Time)

Before writing anything, run through this silently. Only speak up if something is missing.

### 1. Does config.md exist?
Read `config.md` from the project root.
- **If missing:** Stop. Say: "I need to know about you and your business first. Say **'Run my business blueprint'** — it takes 5 minutes and makes everything I write sound like you, not generic AI."
- **If exists:** Continue.

### 2. Is Voice Training complete?
Check config.md for `- [x] Voice Training completed` in the Setup Status section.
- **If unchecked or missing:** Stop. Say: "I can write posts, but they won't sound like you yet. Say **'Train on my voice'** first — I only need to do it once. Then come back."
- **If checked:** Load the Voice Samples / voice profile section from config.md.

### 3. Is Notion connected?
Check your available tools for Notion tools.
- **If found:** Use Notion for saving drafts. If config.md has `- [ ] Notion connected`, update it to `- [x] Notion connected`.
- **If not found:** Save drafts as local files. Don't mention Notion.

### 4. All clear — proceed silently.

---

## What the Agent Does

1. Takes your input — a topic, idea, note, or scans recent Notion notes if asked
2. Picks the platform — X (280 chars for singles, 5-12 posts for threads) or LinkedIn (2,800 chars max)
3. Applies your voice profile and human writing rules
4. For LinkedIn: uses hook, body, CTA structure with thought leadership formatting
5. For X: uses a scroll-stopping hook, punchy rhythm, no hashtags unless asked
6. Shows you the draft for review
7. On approval, saves to Notion content calendar (if connected) or a local file

## Platform Rules

### LinkedIn

- Max 2,800 characters
- Hook in first 2 lines (before the "see more" fold)
- Use line breaks for readability
- Thought leadership tone — teach, don't sell
- End with a question or soft CTA

### X (Twitter)

- Single posts: 280 characters or less, punchy and complete
- Threads: 5-12 connected posts, each stands alone but builds
- First post is the hook — must stop the scroll
- No hashtags unless you ask for them
- Conversational, not polished

## Content Formats Available

- Single post (either platform)
- Thread (X)
- Carousel outline (LinkedIn — text for slides, not images)
- Weekly batch (3-5 posts across platforms)

## Rules

- Always use the voice profile
- Apply human writing rules — no AI-tell patterns, vary sentence length, specific details over generic
- Never post directly — draft only, you review and publish
- If the topic is vague, ask one clarifying question before writing
- No fabricated stats, fake testimonials, or hallucinated examples
