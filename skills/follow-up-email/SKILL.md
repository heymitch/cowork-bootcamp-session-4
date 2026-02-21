---
name: follow-up-email
description: Write a ready-to-send follow-up email after a meeting. Say "write follow-up email", "send meeting recap", "email after meeting", "follow up with [person]", or "write the recap email".
user-invocable: true
---

# Follow-Up Email

Write a follow-up email that references the meeting, summarizes key points, and gives a clear next step.

## How to Run

- "Write a follow-up email for my meeting with [person]"
- "Send the meeting recap"
- "Email after my call with [person]"
- "Follow up with [person] about [topic]"

## What the Agent Does

### Step 1: Gather inputs

Check for existing content from this session:
- Meeting transcript or structured summary (from transcript-extractor)
- Proposal or SOW (from proposal-builder)
- Presentation (from deck-generator)

If nothing exists, ask: "Tell me about the meeting — who was it with, what did you discuss, and what's the next step?"

Read `config.md` for voice profile and contact info.

### Step 2: Pick the template

Reference `../project-kit/references/email-templates.md`. Choose based on context:

| Situation | Template |
|-----------|----------|
| First meeting with potential client | New Client Follow-Up |
| Check-in with existing client | Existing Client Check-In |
| Exploratory / partnership call | Partner / Collaboration |
| After a pitch or presentation | Post-Presentation |
| Reconnecting after a gap | Warm Re-engagement |

If unsure, ask: "Is this a new prospect, existing client, or something else?"

### Step 3: Write the email

Include:
- **Subject line**: Clear, specific, under 60 characters
- **Opening**: Reference something specific from the meeting (not "I hope this email finds you well")
- **Key takeaways**: 3-5 bullets of what was discussed or decided
- **Attachments mentioned**: If a proposal, deck, or other deliverable was created, reference it
- **Next step**: One clear action — what you want them to do
- **Sign-off**: Matches the relationship stage (formal/casual per tone guide)

Apply the voice profile from config.md if it exists. If not, default to professional and direct.

### Step 4: Quality check

Before showing the email, run through `../project-kit/references/deliverable-checklist.md`:
- Names spelled correctly
- No placeholder text remaining
- No AI-tell phrases
- Tone matches relationship stage
- One clear CTA
- Under 200 words

### Step 5: Review

Show the complete email. Ask:
- "Ready to send, or want to adjust anything?"
- "Should I change the tone — more formal or more casual?"

### Step 6: Output

On approval:
- Display the final email ready to copy-paste.
- If Gmail tools are connected, offer to draft it (never send without explicit "send it" confirmation).

## Rules

- NEVER send an email without the user saying "send it" or "yes, send."
- Keep emails under 200 words. Shorter is almost always better.
- One call to action per email. Not three options.
- Always reference something specific from the meeting — generic follow-ups get ignored.
- If attaching deliverables, mention them in the body ("I attached the proposal we discussed").
- Never use: "I hope this email finds you well", "Per our conversation", "Just circling back."
- Read the email as the recipient before presenting it. Would you reply?
