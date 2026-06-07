---
name: constitution-check
description: A gate that self-reviews a plan or a diff against all twelve build principles before you build or before you call it done — the methodology's enforcement layer. Use this after drafting a plan and before executing it, before finalizing a change, or whenever the user says "check against the constitution / the principles," wants a principles review, or asks whether the work honors the twelve. Trigger before any substantial build proceeds and before declaring one complete; surface concrete violations by principle number with a recommended fix.
---

# Constitution Check

A constitution that isn't checked is decoration. This skill is the enforcement gate: it reviews a concrete plan or diff against the twelve principles and flags real violations before they ship. It fires at two moments — **after a plan is drafted, before you build it**, and **before you call a build done**.

Read `PRINCIPLES.md` at the plugin root for the twelve, then review the work in front of you against each. Be concrete: a principle you can't point at a specific line or choice for is a principle you can't enforce.

## How to run the check
Go principle by principle. For each, decide: does this plan/diff **honor it, violate it, or not apply**?

- **0 · Operating Contract** — Am I about to escalate something I should own, or own something I should escalate?
- **1 Amplify / own** — Am I handing the human work they shouldn't have to bless?
- **2 Different plane · 3 Durable thesis** — Does this serve the durable goal, or just a local win?
- **4 Reality-graded · 5 Honesty** — Is every claim of success something I actually verified? Any vanity metric? Any fake pass?
- **6 Grill · 7 Delete** — Is there an unresolved CEO-line decision I'm assuming through? A requirement here I should delete rather than build?
- **8 Research · 9 Build-on-top · 10 Density · 11 Clean** — Did I read before writing? Am I co-opting the cleanest substrate or hand-rolling? Am I diluting scope? Is this clean, or a Frankenstein patch?

## Output format
Report only what's load-bearing:

```
Constitution Check
✅ Honored:  <principles that clearly pass — one line>
⚠️  Violations:
   - P<n> <name>: <the specific line/choice that violates it> → <recommended fix>
🚪 Escalate:  <any CEO-line decision surfaced by P6/P7 that needs the human>
```

If there are no violations, say so plainly — do not manufacture findings to look thorough (that would itself violate Principle 5). A clean plan is a clean plan.

## The test
> Every principle must be checkable against something concrete in the plan or diff. If you can't point to the line, you can't enforce the principle — sharpen the principle or sharpen the plan.
