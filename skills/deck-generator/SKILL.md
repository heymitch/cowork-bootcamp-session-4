---
name: deck-generator
description: Generate a presentation or slide deck from meeting content or a proposal. Say "make a presentation", "build a deck", "create slides from meeting", "presentation for [client]", or "slide deck from this proposal".
user-invocable: true
---

# Deck Generator

Turn meeting content or a proposal into a client-ready presentation.

## How to Run

- "Make a presentation from my meeting"
- "Build a deck for [client]"
- "Create slides from this proposal"
- "Turn this into a pitch deck"

## What the Agent Does

### Step 1: Gather inputs

Use whatever's available:
- Meeting transcript (from transcript-extractor or pasted)
- Proposal (from proposal-builder or provided)
- Loose notes or bullet points from the user

Read `config.md` for business name, services, and branding details.

### Step 2: Check tools

**Gamma tools available?**
- Generate a full, designed presentation via Gamma API.
- Use Gamma's theme options. Ask the user for color preference if config.md doesn't specify.

**Gamma not available?**
- Generate a detailed markdown outline with slide-by-slide content.
- Each slide has everything needed to build it manually.

### Step 3: Build the deck

Follow this structure (adjust based on content):

**Slide 1 — Title**
- Project name
- Client name + your name
- Date

**Slide 2 — The Problem**
- What the client is dealing with (use their words)
- Why it matters / what it's costing them

**Slide 3 — The Solution**
- What you'll do (one clear sentence)
- 3-4 key deliverables

**Slide 4 — The Approach**
- How you work (your process, phases, methodology)
- What makes your approach different

**Slide 5 — Timeline**
- Visual phase breakdown
- Key milestones and dates

**Slide 6 — Investment**
- Pricing tiers or flat rate
- What's included at each level

**Slide 7 — Next Steps**
- One clear action: sign, schedule, reply
- Your contact info

For each slide, include:
- **Headline**: One sentence that makes the point
- **Content**: 3-5 bullet points or a key visual concept
- **Speaker notes**: What to say when presenting this slide (2-3 sentences)

### Step 4: Review

Show the full deck outline or Gamma preview. Ask:
- "Does the story flow make sense?"
- "Anything missing or out of order?"
- "Want me to adjust the tone — more formal or more casual?"

### Step 5: Save

On approval:
- If Gamma: save/share the generated presentation.
- If markdown: save the outline to the project directory.
- Mention: "You can paste this into Google Slides, Keynote, or any deck tool."

## Rules

- Keep it to 7-10 slides. Nobody likes a 30-slide deck.
- One idea per slide. If a slide has more than 5 bullet points, split it.
- Headlines should be statements, not labels. "We'll launch in 8 weeks" not "Timeline."
- Speaker notes are required for every slide — this deck should be presentable by anyone.
- Never put pricing on a slide without the user's explicit approval.
- Show for review before saving or generating.
- If both meeting content and a proposal exist, use the proposal as the primary source (it's already structured).
