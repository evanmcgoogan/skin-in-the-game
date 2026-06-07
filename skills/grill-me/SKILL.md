---
name: grill-me
description: Before building at the CEO line, interrogate intent with a tight set of sharp, first-principles multiple-choice questions — each option carrying pros, cons, and long-term implications, recommendation first. Use this whenever a substantial build hinges on a taste, strategy, or direction decision that is genuinely the human's, or when ambiguity would otherwise be filled by your own assumptions. Trigger whenever the user asks you to build or design something with unresolved high-level choices, says "grill me," "ask me first," or wants to be interrogated before you start — even if not named explicitly. Do NOT grill over technical or reversible calls you should own.
---

# Grill Me

The most expensive failure in agent-assisted building is confidently building the wrong thing — filling ambiguity with your own assumptions instead of the human's intent. Grilling is the antidote, but it's a scalpel, not a hammer: it fires only at the **CEO line** — taste, strategy, direction, one-way doors. Below that line, asking is a breach of the contract; decide and move. (See `operating-contract`.)

## When to grill
Grill when a substantial build hinges on a decision that is genuinely the human's:
- **Taste** — product feel, voice, identity
- **Strategy** — what to build, what to cut, positioning, priorities
- **One-way doors** — irreversible or expensive-to-reverse choices

Do NOT grill on architecture, library choices, naming, or anything reversible. If you can change it cheaply later, just decide.

## How to grill well
The questions carry the value, so craft them from first principles:

- **The options carry the insight.** A weak question is *"How should I handle errors?"* A first-principles one is: *"Failures here are either (a) recoverable → retry, (b) fatal → halt loudly, or (c) silent → log-and-continue. Which is acceptable?"* The second forces a decision the human would otherwise discover at 2am.
- **Aim at the one-way doors.** Prioritize questions whose wrong answer is expensive to reverse — data model, public interface, what *not* to build.
- **Each option states pros, cons, and long-term implications** in plain English, and you **lead with your recommendation** and why.
- **3–5 questions, then build.** It's not an interview; it's removing the top sources of rework.

Use the `AskUserQuestion` tool to present these as multiple choice — low friction for the human, and it forces you to enumerate the real, mutually-exclusive paths rather than asking an open "what do you want?"

## Pair every grill with ownership

Grilling must never read as punting. Whenever you raise CEO-line questions, say in the same breath what you're **already owning and proceeding on**: *"I'm owning the schema, the library, and the layout — I only need you on these two."* A grill without that boundary is a runaway asking permission for everything; a grill *with* it is a COO bringing you the one decision that's actually yours. Decide the reversible, escalate the irreversible, and make both halves visible.

## The test
> A good grill question deletes a whole branch of wasted work before a line is written. If the answer wouldn't change what you build, don't ask it.
