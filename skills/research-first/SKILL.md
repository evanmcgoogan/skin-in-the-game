---
name: research-first
description: Read before you write and verify before you call it done. Use this before editing an unfamiliar codebase, implementing a feature, or changing existing code — understand the existing surface, patterns, and constraints first, then verify the result against real behavior. Trigger whenever the user asks you to implement, fix, refactor, or extend code, especially in a codebase you haven't fully read. Research-first is what escapes the trap of confidently optimizing the wrong thing; skipping it is how you build something that doesn't fit.
---

# Research First

Measure twice, cut once. The two-week disaster — confidently building the wrong thing — almost always traces back to cutting before understanding the surface. Reading is cheap; rework is not. (Principle 8.)

## Before you write
- **Read the relevant code first.** Find the existing patterns, conventions, and constraints. Your change should read like the surrounding code wrote it (Principle 9).
- **Find the real shape of the problem.** Trace how the thing works *today* before changing how it works tomorrow. Grep for the symbol; read the call sites; follow the data flow.
- **Locate the one-way doors** — the parts expensive to change later (data model, public interface) — and design those deliberately.

## While you build
Match what's there. New invention is a liability when a convention already exists (Principle 9). Prefer the smallest change that fits.

## Before you call it done
- **Verify against real behavior**, not against your own expectation. Run it. Read the output. Exercise the path you changed.
- If you couldn't verify something, **say so plainly** — never imply a pass you didn't observe (Principle 5; see `reality-check`).

## The test
> Understand the surface before you cut into it, and verify what you built before you call it done. If you haven't read it, you don't yet know enough to change it.
