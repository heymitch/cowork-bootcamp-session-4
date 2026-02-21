---
name: project-kit
description: One meeting becomes everything you need to send. Say "build a project kit", "turn this meeting into everything", "pull transcript", "get my meeting", "write proposal", "build SOW", "make presentation", "build deck", "follow-up email", "meeting recap email", "social posts from meeting".
user-invocable: false
---

# Project Kit — Router

One meeting. Everything you need to send. This skill routes to the right sub-skill based on what you ask for.

## Routing

| You say | Runs |
|---------|------|
| "Build a project kit" / "turn this meeting into everything" | Full flow (see below) |
| "Pull transcript" / "get my meeting" / "find my last call" | `../transcript-extractor/SKILL.md` |
| "Write proposal" / "build SOW" / "scope of work" | `../proposal-builder/SKILL.md` |
| "Make presentation" / "build deck" / "create slides" | `../deck-generator/SKILL.md` |
| "Follow-up email" / "meeting recap email" | `../follow-up-email/SKILL.md` |
| "Social posts from meeting" / "post about this project" | `../social-content/SKILL.md` |

## Preflight (Run Silently)

1. **config.md exists?** If not, stop: "I need your business details first. Say 'Run my business blueprint' — it takes 5 minutes."
2. **Scan connectors:** Fireflies, Gmail, Gamma, Notion. Note what's available. No connectors required — the user can always paste notes.
3. **Proceed.**

## Full Flow

When running the complete kit, execute in order. Each step feeds the next:

1. **transcript-extractor** — Get and structure the meeting content.
2. **proposal-builder** — Build the SOW from structured content.
3. **deck-generator** — Create the presentation from the proposal.
4. **follow-up-email** — Write the recap email referencing all deliverables.
5. **social-content** — Extract one insight for social posts.

Show each output for review before moving to the next step.

## Rules

- Route based on intent. Don't run the full flow if they only asked for an email.
- Every sub-skill shows output for review before saving or sending.
- Never send anything without explicit approval.
- If a sub-skill needs input from a previous step that wasn't run, run that step first or ask for the input directly.
