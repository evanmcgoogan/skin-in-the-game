<div align="center">

# 🤝 Skin in the Game

### The Operating Contract. Give AI agents Skin in the Game.

Twelve build principles that turn your coding agent from a yes-man into a **COO/CTO with skin in the game** — it owns the technical calls, escalates only what's truly yours, and grills you *before* it builds the wrong thing.

**MIT licensed · for Claude Code**

</div>

---

## The problem

Your coding agent has two failure modes, and you've hit both:

- **The yes-man** — it agrees with your half-formed idea and confidently builds it, flaws and all.
- **The runaway** — it asks permission for trivia, or charges through a one-way door it should have flagged.

The fix isn't a cleverer prompt. It's a **contract** — an explicit division of labor that tells the agent what to own and what to bring to you.

## Install

```text
/plugin marketplace add evanmcgoogan/skin-in-the-game
/plugin install skin-in-the-game@skin-in-the-game
```

That's it. The operating contract loads at the start of every session.

## What you get

This isn't a `CLAUDE.md` you paste once and forget. It's a **methodology** — twelve principles plus six composable skills and a session-start hook that *enforce* them:

| Skill | What it enforces |
|---|---|
| **operating-contract** | #0 — the spine: own technical/reversible calls, escalate only taste/strategy/one-way-doors |
| **grill-me** | #6 — sharp multiple-choice questions at the CEO line, *before* building |
| **delete-the-requirement** | #7 — question every requirement, then try to delete it |
| **research-first** | #8 — read before you write; verify before "done" |
| **reality-check** | #4 & #5 — kill fake passes, vanity metrics, and performed rigor |
| **constitution-check** | the gate — self-review any plan or diff against all twelve |

## How it works — the altitude line

The whole system turns on one line:

> **Below the strategy/taste line, the agent replaces you. Above it, it amplifies you.**

- **Below the line** (architecture, libraries, naming, anything reversible) → the agent decides and proceeds. No rubber-stamping.
- **Above the line** (taste, strategy, one-way doors) → it escalates as a *decision*: plain-English options, pros/cons, a recommendation. Never a status update.

Because you're rate-limited by exactly one resource — your time and attention — and it should be spent only where it's irreplaceable.

## Before / after

**Without a contract:**
> **You:** Add caching to the API.
> **Agent:** Great idea! Adding a Redis cache now. *[builds it — never asks if the data's even cacheable, invents a config layer nobody needs]*

**With Skin in the Game:**
> **You:** Add caching to the API.
> **Agent:** Two of these are one-way doors, so before I build — *[grill-me: invalidation strategy? acceptable staleness?]*. I'm dropping the per-route config (#7 — flexibility you don't need yet). Building the rest, then I'll run constitution-check before I call it done.

## The twelve

The full constitution lives in **[`PRINCIPLES.md`](PRINCIPLES.md)**. In brief:

**The North Star** — 1. Amplify above the line; own below it · 2. Compete on a different plane · 3. Build for the durable thesis
**Intellectual Honesty** — 4. Measure only what reality grades · 5. Honesty over performance
**Engineering Discipline** — 6. Grill me at the CEO line · 7. Delete the requirement · 8. Research first · 9. Build on top, not next to · 10. Density over breadth · 11. Clean over Frankenstein

*(0 · The Operating Contract sits above all eleven.)*

## Why this is different

Every other framework makes your agent better at *doing* — TDD, debugging, planning. **Skin in the Game governs the *relationship*** — who decides what, when to escalate, how to stay honest. It's the first operating contract for building with an AI agent. That's the category.

## License

MIT © evanmcgoogan. Adopt the principles, fork them, make them yours.
