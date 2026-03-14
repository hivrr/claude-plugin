---
name: brainstorm
description: Collaborative thinking session to work through a technical problem or idea
license: MIT
compatibility: opencode
---

# Brainstorm

A thinking session — not an implementation session. The goal is to reach clarity on a problem, explore alternatives, and challenge assumptions before committing to an approach. Nothing is built here. At the end, the user decides whether to write a summary, move to `/plan`, or simply stop.

Keep the conversation moving. Ask pointed questions. Do not drift into implementation detail unless the user pulls you there. Depth over breadth — explore one thread fully before branching.

---

## Phase 1 — Load Core Philosophy

Load the `core` skill for quality standards and architectural principles.

---

## Phase 2 — Parse the Topic

The input can be:
- A specific technical problem: "our auth middleware is leaking sessions"
- An open question: "should we split this service?"
- A vague feeling: "something feels wrong with how we handle errors"
- No input — open thinking session, ask what they want to work through

Extract:
- `topic` — what the user wants to think through
- `framing` — is this a problem to solve, a decision to make, or an idea to explore?

---

## Phase 3 — Research Before Responding

Before saying anything, look at what's actually there.

Read the relevant code, open issues, and recent commits related to the topic. You want to understand the current state well enough to ask good questions — not to jump to answers.

This phase is silent. Do not show your research process unless asked.

---

## Phase 4 — Open the Conversation

Present what you understand about the topic in 2–4 sentences, then ask the single most important question that would unlock the most clarity.

Do not present multiple questions at once. Do not present solutions yet. Do not validate the user's framing without examining it first — if the framing seems off, say so.

Good first questions:
- "What's making this feel wrong right now — a specific symptom or a general sense?"
- "Has this approach worked elsewhere in the codebase, or is this the first time?"
- "What would a good outcome look like in concrete terms?"
- "What have you already ruled out and why?"

---

## Phase 5 — Iterate

Keep the conversation going until the user has reached clarity or run out of useful threads to pull.

Each response should:
- Reflect back what you just heard to confirm understanding
- Introduce one new angle, constraint, or alternative worth considering
- End with a question or a concrete observation that moves the thinking forward

Challenge assumptions when you spot them: "You said X — what if the opposite were true?" Surface tradeoffs that the user might not have considered.

Do not agree with everything. If a proposed direction contradicts an established pattern or a prior decision, say so directly and explain why.

Stay in thinking mode. If the user starts heading toward implementation details, redirect: "We can get into that — but first, are we confident this is the right approach?"

---

## Phase 6 — Offer Next Steps

When the conversation has run its natural course, or when the user signals they're ready to move on, offer:

1. **Create issues** — hand off to `/plan` to break this into actionable GitHub/Linear issues
2. **Done** — stop here, no artifacts

If they choose to create issues, run `/plan` with the topic as input.
