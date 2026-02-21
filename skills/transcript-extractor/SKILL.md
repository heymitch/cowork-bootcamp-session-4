---
name: transcript-extractor
description: Pull and structure a meeting transcript from Fireflies, Gmail, or pasted notes. Say "pull my meeting transcript", "get transcript from [person]", "find my last call", or "get my meeting notes".
user-invocable: true
---

# Transcript Extractor

Find or accept a meeting transcript, then extract structured data ready for other skills.

## How to Run

- "Pull my meeting transcript"
- "Get the transcript from my call with [person]"
- "Find my last call"
- "Here are my meeting notes" (paste directly)

## What the Agent Does

### Step 1: Find the transcript

Try sources in this order. Stop at the first one that works.

**Fireflies connected?**
- Search for recent transcripts matching the person or topic.
- Pull the full transcript.

**Gmail connected but not Fireflies?**
- Search Gmail for transcript emails. Look for messages from: Fireflies, Fathom, Otter, Zoom, Read.ai, Grain, Avoma.
- Search terms: "meeting summary", "transcript", "call recording", the person's name.
- Pull the email body as the source.

**Nothing connected?**
- Ask the user: "Paste your meeting notes, transcript, or key points below. Even rough notes work — I'll structure them."
- Also accept: uploaded files, voice memo transcriptions, or bullet points.

### Step 2: Extract structured data

From whatever source you got, pull out:

- **Attendees**: Who was in the meeting (names, roles if mentioned)
- **Context**: What kind of meeting (sales call, project check-in, partner intro, etc.)
- **Key Discussion Points**: The 3-5 main topics covered
- **Decisions Made**: Anything that was agreed on
- **Action Items**: Who owes what, with deadlines if mentioned
- **Next Steps**: What happens after this meeting
- **Quotes**: 2-3 direct quotes that capture the client's words (useful for proposals)

### Step 3: Output

Present the structured summary in clean markdown. This output feeds directly into:
- proposal-builder (for SOW generation)
- deck-generator (for presentation content)
- follow-up-email (for recap emails)
- social-content (for post ideas)

Ask: "Ready to build something from this? I can create a proposal, deck, follow-up email, or social posts."

### Step 4: No transcript found

If nothing comes back from search and the user can't paste notes, help them recall:
1. "Who was in the meeting?"
2. "What did you talk about — even just the topic?"
3. "Did you agree on anything or discuss pricing?"
4. "What's the next step with them?"

Build the structured summary from their answers.

## Rules

- Never fabricate transcript content. Only use what was found or provided.
- If the transcript is long (over 2000 words), summarize but keep all action items and decisions verbatim.
- Always preserve the client's exact words in the Quotes section — these matter for voice matching.
- If multiple transcripts match, show the list and ask which one.
- Output should be clean enough to copy-paste into another tool.
