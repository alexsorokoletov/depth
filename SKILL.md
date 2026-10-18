---
name: smartup
description: Turn a shallow task request into the version a top professional in that field would do — deeper, not bigger. Names what the pro would add, the rawest source material, the specific methods/tools, and an external check (not the user, not Claude) that proves the result right; then rewrites the user's prompt to ask for exactly that. Use when the user says "smartup", "/smartup", "deeper version", "what would a pro do here", "rewrite my prompt", "level up this prompt", or "make this ask smarter".
---

# smartup — deeper version of a task, then a rewritten prompt

Goal: make the task **deeper, not bigger**. Do not add scope for its own sake. Add only what makes
the result more true, more checkable, or more fit for its audience.

Do NOT start the task itself. Output the analysis and the rewritten prompt, then stop and wait.

## Steps

1. **Ground it first (cheap).** If the task touches the current repo or files, spend 1–3 quick reads
   to find facts that change the answer (constraints, docs, permissions, existing scripts, policies).
   Example: a "100% local" claim vs an `INTERNET` permission and an SDK that sends diagnostics.
   A pro catches the claim that would not survive scrutiny.
2. **Resolve ambiguity in one line.** If a term is unclear (typo, a style or creator name), state
   your reading and ask the user to correct it. Do not block on it.
3. **Answer the four questions**, short and specific to this task (no generic advice):
   1. **What a top professional would do that the user did not ask for.** Framing, the one claim or
      outcome that matters, the objection to answer first, audience/platform fit, plan before execution.
   2. **Rawest material.** The primary source a pro starts from instead of digested summaries:
      raw recordings, logs, real user screens, traffic counters, original data, real people's reactions.
      Note privacy/safety limits on that material (project rules, PII).
   3. **Specific methods and tools.** Named techniques and tools (CLI commands, libraries, frameworks,
      formats). Prefer tools already in the repo or on the machine.
   4. **What, other than you or me, shows the result is right.** External, checkable signals:
      measurements, tests, fresh users who were not briefed, domain owners, platform metrics,
      policy/doc consistency. Give a pass condition for each.
4. **Rewrite the prompt.** A blockquote the user can paste back. It must:
   - state the one goal/claim and the audience;
   - put the plan/approval gate before execution;
   - name the raw inputs, the tools, and where outputs go (respect "never commit" rules);
   - list the verification steps with pass conditions;
   - mark outward-facing actions (posting, sending, publishing) as confirm-first;
   - end with the deliverable: files + a short report with measured numbers and the claim's limits.
5. **Offer the next step** in one line (e.g. "Start with step 1?"). Do not execute without a yes.

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

- Dense and concise. Bullets, not paragraphs. Follow the user's global style rules (e.g. TL;DR for
  long replies, Simplified Technical English for long text).
- Be specific to the domain and the project. Cite file paths for facts you found.
- Honesty over hype: if a claim the user wants to make is not fully true, say so and give the
  exact wording that is true.
- Deeper, not bigger: every addition must raise correctness, proof, or audience fit.
