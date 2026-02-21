---
name: proposal-builder
description: Build a complete proposal or SOW from meeting context. Say "build a proposal", "write the SOW", "create proposal from meeting", "write up the scope of work", or "proposal for [client]".
user-invocable: true
---

# Proposal Builder

Take meeting content and turn it into a ready-to-send proposal or SOW.

## How to Run

- "Build a proposal from my meeting with [person]"
- "Write the SOW"
- "Create a proposal from this transcript"
- "Write up the scope of work for [project]"

## What the Agent Does

### Step 1: Gather inputs

Check for meeting content first:
- If transcript-extractor already ran this session, use that output.
- If not, ask: "Do you have meeting notes or a transcript? Paste them here, or say 'pull my transcript' and I'll find it."

Read `config.md` from the project root for:
- Business name, contact info
- Services and pricing
- Voice profile

### Step 2: Choose format

Based on the project size:
- **Under $3,000 or simple scope** — Use the one-pager format from `../project-kit/references/proposal-template.md`
- **$3,000+ or multi-phase** — Use the full proposal format from `../project-kit/references/proposal-template.md`

If unsure, ask: "Is this a quick project or a bigger engagement? I'll format the proposal to match."

### Step 3: Build the proposal

Fill in every section from the template:

1. **Cover**: Project name, client name, date, your info (from config.md)
2. **Executive Summary**: Use the client's own words from the transcript. What they need, why it matters, what you'll deliver.
3. **Scope of Work**: Break into deliverables with descriptions and timelines. Be specific — "5-page website" not "website."
4. **Timeline**: Map to phases. Be realistic. Add buffer.
5. **Pricing**: Three tiers if config.md has pricing data. If no pricing info, ask: "What are you thinking for pricing? Give me a ballpark and I'll build three tiers around it."
6. **Payment Terms**: Default to 50/50 unless the user specifies otherwise.
7. **Included / Not Included**: Draw clear lines. The "not included" section prevents scope creep later.
8. **Next Steps**: One clear action for the client.
9. **Terms**: Brief working agreement language.

### Step 4: Review

Show the complete proposal. Ask:
- "Does the scope match what you discussed?"
- "Is the pricing right?"
- "Anything to add or cut?"

### Step 5: Save

On approval:
- Save as markdown in the current project directory.
- If the user wants PDF format, output clean markdown with a note: "Copy this into your PDF tool or say 'make this a PDF' if you have a converter set up."

## Rules

- Never guess pricing. If config.md has no pricing and the user doesn't provide it, ask.
- Always use three-tier pricing unless the user explicitly wants flat rate.
- Use the client's language from the transcript in the executive summary and scope descriptions.
- Keep proposals under 2 pages for one-pager format, under 4 pages for full format.
- Show for review before saving. Never save or send without approval.
- Reference `../project-kit/references/proposal-template.md` for structure.
- Run the deliverable checklist (`../project-kit/references/deliverable-checklist.md`) mentally before presenting.
