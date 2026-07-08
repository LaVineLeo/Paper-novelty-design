---
name: paper-novelty-design-v1
description: Design, audit, and rewrite academic paper novelty claims into defensible contributions. Use when Codex needs to help with 论文创新点设计, novelty evaluation, contribution drafting, Problem-Method-Insight rewriting, 可证伪性/falsifiability checks, reviewer pressure tests, pseudo-innovation diagnosis, or innovation evolution logs for papers, theses, proposals, and technical reports.
---

# Paper Novelty Design V1

Use this skill to turn a rough research idea, proposal note, abstract, or introduction draft into a bounded and review-resistant contribution. Prefer this skill when novelty is vague, claims feel inflated, or a paper needs contributions tied to evidence rather than adjectives.

## Default Workflow

1. Build the minimum research context.
   - Identify field, task, venue or thesis context, current idea, closest known work, evidence, and constraints.
   - If the user provides a draft, extract candidate `Problem`, `Method`, and `Insight` before rewriting.
   - If the user wants a "first" claim or strong literature positioning, state that external literature verification is required.

2. Rewrite the idea as a three-layer novelty statement.
   - `Problem`: a bounded unresolved gap, contradiction, or limitation.
   - `Method`: the specific intervention chosen because it addresses that problem.
   - `Insight`: the portable takeaway the field can reuse if the evidence holds.
   - Reject "our method performs better" as an `Insight`; treat it as evidence.

3. Diagnose pseudo-innovation risk.
   - Check for missing motivation, engineering-stack storytelling, domain transplant without adaptation, metric-only narrative, and fragile "first" claims.
   - Read [references/review-checks-v1.md](./references/review-checks-v1.md) when you need the full trap checklist or example rewrites.

4. Convert the core claim into falsifiable propositions.
   - Write 1-3 claims that evidence could support or refute.
   - For each claim, specify support conditions, failure conditions, and the concrete test or evidence needed.
   - If a claim cannot be falsified, narrow its scope until it can.

5. Run pressure tests.
   - Repetition test: has adjacent work already done this?
   - Motivation test: does the method logically target the problem?
   - Falsifiability test: what result would force revision or rejection?
   - Differentiation test: what differs at the Problem, Method, detail, evidence, and Insight layers?
   - Story test: can the contribution be stated in 1 sentence, 3 sentences, and 1 short paragraph?
   - Use [references/review-checks-v1.md](./references/review-checks-v1.md) for detailed prompts and reviewer-style checks.

6. Produce paper-facing output.
   - Give a revised three-layer statement.
   - Give contribution bullets suitable for an introduction, proposal, or thesis section.
   - Give falsifiable hypotheses with a matching evidence plan.
   - Give likely reviewer attack points and concrete repairs.
   - Read [references/writing-templates-v1.md](./references/writing-templates-v1.md) when drafting formal contribution statements or evolution logs.

7. Manage iteration honestly.
   - If evidence supports the claim, narrow the claim and state its boundary conditions.
   - If evidence is weak, shrink the scope or recast the contribution as a tested limitation or empirical finding.
   - If experiments reveal a stable unexpected pattern, consider making that pattern the new `Insight`.
   - Maintain a versioned evolution log with evidence, revision reason, and next falsification test.

## Output Modes

### Rough idea or proposal stage

```markdown
## Novelty Diagnosis
Verdict: [strong / promising but underspecified / mostly engineering / too close to prior work]

## Three-Layer Statement
| Layer | Draft |
|---|---|
| Problem | ... |
| Method | ... |
| Insight | ... |

## Falsifiable Propositions
| Proposition | Supporting evidence | Refuting evidence | Required test |
|---|---|---|---|
| ... | ... | ... | ... |

## Reviewer Pressure Points
| Risk | Likely reviewer question | Repair |
|---|---|---|
| ... | ... | ... |

## Next Revision
- ...
```

### Mature manuscript or contribution section

```markdown
## Revised Contributions
1. ...
2. ...
3. ...

## What Each Contribution Must Prove
| Contribution | Evidence needed | Weakest link |
|---|---|---|
| ... | ... | ... |
```

### Ongoing project tracking

```markdown
## Novelty Evolution Log
| Version | Current insight | New evidence | Revision reason | Next falsification test |
|---|---|---|---|---|
| v1 | ... | ... | ... | ... |
```

## Resource Routing

- Read [references/review-checks-v1.md](./references/review-checks-v1.md) for trap diagnosis, falsifiability framing, and pressure-test prompts.
- Read [references/writing-templates-v1.md](./references/writing-templates-v1.md) for three-layer templates, contribution statements, and evolution-log formats.
- Avoid loading both reference files unless the task spans both diagnosis and final writing.

## Writing Rules

- State novelty through bounded claims, not adjectives such as "novel", "advanced", or "state-of-the-art".
- Treat performance improvements as evidence, not as the novelty itself.
- Do not invent citations, baselines, datasets, mechanisms, or results.
- When using "first", narrow the scope and mark it as requiring literature verification.
- Preserve the user's research direction before proposing a different project.
- Prefer 3-4 contribution bullets; merge weaker items.
- Be direct if the idea is mostly engineering or too close to prior work.
- Keep terminology aligned with the user's source language when rewriting.
