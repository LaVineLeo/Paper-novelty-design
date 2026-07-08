# Writing Templates V1

Use this reference when the task is to rewrite ideas into paper-facing text, formal contribution bullets, or versioned novelty logs.

## Three-Layer Template

```markdown
## Three-Layer Statement
| Layer | Draft |
|---|---|
| Problem | [specific, bounded unresolved issue] |
| Method | [specific intervention and key mechanism] |
| Insight | [portable takeaway that survives beyond "better performance"] |
```

Rewrite rules:

- Make `Problem` concrete enough that a reviewer can see the boundary.
- Make `Method` specific enough that another researcher can tell what changed.
- Make `Insight` reusable enough that it still matters if the model name is forgotten.

## Contribution Statement Template

Use 3-4 bullets. Put the insight before the model name when possible.

```markdown
## Revised Contributions

1. We identify [specific gap/problem] and show that [portable insight], which has not been explicitly studied in prior work.
2. We propose [method name], whose key design choice is [distinctive mechanism], motivated by [insight from contribution 1].
3. We evaluate [method name] on [scope of evidence] and show [specific result], while ablations support [insight from contribution 1].
4. Optional: We release/provide [benchmark, dataset, code, taxonomy, or analysis] that is genuinely reusable.
```

## What Each Contribution Must Prove

```markdown
## What Each Contribution Must Prove
| Contribution | Evidence needed | Weakest link |
|---|---|---|
| ... | ... | ... |
```

Use this table to stop contribution bullets from becoming unsupported slogans.

## Story Compression Template

```markdown
## One-Sentence Version
[<= 30 words; focus on the key takeaway]

## Three-Sentence Version
1. Problem: ...
2. Method: ...
3. Insight: ...

## One-Paragraph Version
[<= 120 words; include the key evidence]
```

Rules:

- Avoid filler phrases such as "novel", "extensive experiments", or "state-of-the-art".
- Make the one-sentence version carry a real takeaway, not only a model name.

## Novelty Evolution Log

```markdown
## Novelty Evolution Log
| Version | Current insight | New evidence | Revision reason | Next falsification test |
|---|---|---|---|---|
| v1 | ... | ... | ... | ... |
```

Recommended use:

1. Update the log whenever the insight changes materially.
2. Record what evidence triggered the revision.
3. Keep the next falsification test concrete and small enough to execute soon.

## Reviewer Pressure Points Template

```markdown
## Reviewer Pressure Points
| Risk | Likely reviewer question | Repair |
|---|---|---|
| Similar to adjacent work | What is fundamentally different beyond implementation detail? | Re-state the difference at the Problem and Insight layers, then add a focused comparison. |
| Weak motivation | Why should this mechanism solve the stated problem? | Add the missing causal or mechanistic link and design an ablation for it. |
| Overclaiming | Which settings does this fail in? | Bound the claim and state the failure condition directly. |
```

## Final Writing Rules

- Prefer bounded verbs such as "show", "find", "suggest", or "is effective under".
- Include specific settings, conditions, or evidence scope whenever possible.
- Move routine items such as visualizations or hyperparameter sensitivity out of the main contribution list unless they are the actual research contribution.
