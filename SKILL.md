---
name: depth
description: Turn a shallow task request into the version a top professional in that field would do — deeper, not bigger. Names what the pro would add, the rawest source material, the specific methods/tools, and an external check (not the user, not Claude) that proves the result right; then rewrites the user's prompt to ask for exactly that. Use when the user says "depth", "/depth", "deeper version", "what would a pro do here", "rewrite my prompt", "level up this prompt", or "make this ask smarter".
---

# depth — deeper version of a task, then a rewritten prompt

Goal: make the task **deeper, not bigger**. Do not add scope for its own sake. Add only what makes
the result more true, more checkable, or more fit for its audience.

Do NOT start the task itself. Output the analysis and the rewritten prompt, then stop and wait.

## Steps

1. **Ground it first (cheap).** If the task touches the current repo or files, spend 1–3 quick reads
   to find facts that change the answer. A pro catches the claim that would not survive scrutiny.
2. **Resolve ambiguity in one line.** If a term is unclear, state your reading and ask the user to
   correct it. Do not block on it.
3. **Answer the four questions**, short and specific to this task (no generic advice):
   1. **What a top professional in this field would do here that the user is not asking for.**
   2. **The rawest material they would start from** instead of what has already been digested for
      the user. Note privacy/safety limits on that material.
   3. **The specific methods and tools they would use.** Prefer tools already in the repo or on the machine.
   4. **What, other than you or me, would show the result is right.** Give a pass condition for each.
4. **Rewrite the prompt to ask for exactly that.** A blockquote the user can paste back. It must:
   - state the one goal/claim and the audience;
   - put the plan/approval gate before execution;
   - name the raw inputs, the tools, and where outputs go;
   - list the verification steps with pass conditions;
   - mark outward-facing actions as confirm-first;
   - end with the deliverable: files + a short report with measured numbers and the claim's limits.
5. **Offer the next step** in one line. Do not execute without a yes.

## Output shape

```
**TL;DR:** <1–2 lines: the core insight a pro would add>

<one-line ambiguity note, if any>

**1. What a pro would do that you did not ask for**
- ...
**2. Rawest material**
- ...
**3. Methods and tools**
- ...
**4. What shows it is right (not you or me)**
- ...

---
**Rewritten prompt:**
> ...

<one-line offer of next step>
```

## Rules

- Dense and concise. Bullets, not paragraphs. Follow the user's global style rules.
- Be specific to the domain and the project. Cite file paths for facts you found.
- Honesty over hype: if a claim the user wants to make is not fully true, say so and give the
  exact wording that is true.
- Deeper, not bigger: every addition must raise correctness, proof, or audience fit.
