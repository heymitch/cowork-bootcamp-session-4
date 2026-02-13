---
name: project-kit
description: Turn one meeting into a full deliverable package — proposal, presentation, social posts, and follow-up email. Say "Build a project kit from my last call" or "Turn this meeting into a proposal".
---

# Project Kit

One input. Four outputs. Drop a meeting transcript, brief, or voice memo — get a proposal, presentation, social post, and follow-up email back. Everything you need to close, packaged in minutes.

## How to Run

- "Build a project kit from my last meeting with [person]"
- "Turn this call into a proposal and presentation"
- "I just finished a call — generate everything I need to send"

---

## Preflight Check (Run Silently)

### 1. Config check
Read `config.md` from project root.
- **Missing:** Stop. Say: "Say **'Run my business blueprint'** first — I need your pricing and services."
- **Exists:** Load business context (pricing, services, one-liner).

### 2. Voice check
Check config.md for `- [x] Voice Training completed`.
- **Unchecked:** Continue — but note outputs will be professional-generic, not voice-matched.
- **Checked:** Load Voice Profile. Wrap all text generation with `<VOICE>{profile}</VOICE>`.

### 3. Connector inventory (silent)
Check available tools:
- **Fireflies** → can pull full transcripts directly
- **Gmail** → can search for meeting transcript emails (Fireflies/Fathom/Zoom/Otter/Read.ai)
- **Gamma** → can generate real presentations (not just outlines)
- **Notion** → can save deliverables

No connectors required — user can always paste notes or drop a file.

### 4. All clear — proceed without announcing.

---

## The Process

### Step 1: Get the Input
- If Fireflies connected: offer to pull a recent transcript
- If Gmail connected: search for meeting transcript emails about this person/company
- Otherwise: ask user to paste notes, drop a file, or provide a voice memo
- Extract: who was involved, what was discussed, what was agreed, what's next

### Step 2: Generate Proposal/SOW
Using `references/proposal-template.md`: scope, deliverables, timeline, pricing.
Pull pricing from config.md. If pricing not found, ask — never guess.

### Step 3: Generate Presentation
Using `references/presentation-structure.md`: 5-7 slide client-ready deck.
- **Gamma connected:** Generate real designed slides via Gamma API
- **No Gamma:** Clean markdown outline ready for any slide tool

### Step 4: Generate Social Content
1-2 posts about the project, lesson learned, or insight from the conversation.
Pick a format from the social-content skill's LinkedIn styles. Platform-ready.

### Step 5: Generate Follow-Up Email
Using `references/follow-up-email.md`: specific opening line (not generic), summary, attachments, clear next step. Under 200 words.

### Step 6: Show All Outputs
Present all 4 deliverables. **Do not save or send.** Wait for approval or edits.
Each output is independent — the proposal doesn't reference the social post.

### Step 7: Save
On approval: save to Notion (if connected) or local files.
If key connectors missing, mention once: "This kit would be stronger with [Gamma/voice training]."

## Rules

- Always show all outputs before saving or sending.
- Never send emails without explicit approval.
- If pricing info is missing, ask — don't guess. Leave as `$[TBD]` and flag it.
- Each output stands alone. The proposal doesn't reference the social post.
- If a connector isn't available, produce the best version without it — never skip an output.
- Apply voice profile and human writing rules to all text outputs.
