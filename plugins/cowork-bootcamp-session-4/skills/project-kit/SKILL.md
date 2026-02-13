---
name: project-kit
description: Generate a complete project kit from a single input — meeting transcript, brief, or voice memo becomes a proposal, presentation, social posts, and follow-up email. Say "Build a project kit from my last meeting" or "Turn this call into a proposal".
---

# Project Kit

One input. Multiple outputs. Drop a meeting recording, brief, or voice memo — get a full project kit back.

## How to Run
- "Build a project kit from my last meeting with [person]"
- "Turn this call into a proposal and presentation"
- "I just finished a call — generate everything I need to send"

---

## Preflight Check (Run Every Time)

Run through this silently. Only speak up if something is missing.

### 1. Does config.md exist?
Read `config.md` from the project root.
- **If missing:** Stop. Say: "I need to know about you and your business first — especially your pricing and services. Say **'Run my business blueprint'** — it takes 5 minutes."
- **If exists:** Continue. Load business context (pricing, services, voice).

### 2. Scan available tools
Check what's connected and build a capability list:
- **Gmail tools** → can search for meeting transcript emails (Fireflies, Fathom, Zoom, Otter, etc.)
- **Fireflies tools** → can pull full meeting transcripts directly (richer than email summaries)
- **Gamma tools** → can generate presentations (not just outlines)
- **Notion tools** → can save deliverables to Notion
- **Voice profile in config.md** → can write in user's voice

For each connector found, update config.md Setup Status if unchecked.

No connectors required — the user can always paste notes, drop a file, or provide a voice memo. More connectors = more automation.

### 3. All clear — proceed silently.

---

## What the Agent Does

Step 1: Get the input.
- If Fireflies is connected: offer to pull a recent transcript.
- If Gmail is connected but not Fireflies: search Gmail for meeting transcript emails (from Fireflies, Fathom, Zoom, Otter, Read.ai, etc.) about this person/project. These services email summaries after every call — Gmail is often enough.
- If neither: ask the user to paste notes, drop a file, or provide a voice memo.
- Extract: who was involved, what was discussed, what was agreed, what's next.

Step 2: Generate the deliverables (adapt based on what's connected):

**Output 1 — Proposal/SOW** (always)
- Scope of work based on what was discussed.
- Timeline, deliverables, and pricing (pulls from config.md if available).
- Written in user's voice if voice profile exists, professional tone if not.

**Output 2 — Presentation** (if Gamma connected: full deck. If not: markdown outline.)
- Key points structured for slides.
- Client-ready: the story of what you'll do and why.

**Output 3 — Social Content** (always)
- 1-2 posts about the project, lesson learned, or insight from the conversation.
- Platform-ready for LinkedIn or X.

**Output 4 — Follow-Up Email** (always)
- Thanks for the meeting, here's what we discussed, here's the proposal.
- Ready to send.

Step 3: Show all outputs for review before saving or sending.

Step 4: On approval, save to Notion (if connected) or local files.

Step 5: If key connectors are missing, mention once what could improve: "This kit would be stronger with [Gamma for real slides / voice training for your tone]. Want me to help set any of those up?"

## Rules
- Always show all outputs before saving or sending anything.
- Never send emails without explicit approval.
- If information is missing for the proposal (pricing, timeline), ask — don't guess.
- Each output should be independent — the proposal doesn't reference the social post.
- Apply voice profile and human writing rules to all text outputs.
- If a connector isn't available, produce the best version possible without it — don't skip the output entirely.
