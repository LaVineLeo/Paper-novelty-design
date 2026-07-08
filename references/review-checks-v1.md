# Review Checks V1

Use this reference when the task is to diagnose novelty quality, expose weak claims, or design falsifiability and reviewer pressure tests.

## Three-Layer Diagnosis

Start by forcing the idea into three layers:

| Layer | Question to answer |
|---|---|
| Problem | What specific and bounded problem is unresolved? |
| Method | What specific intervention addresses it? |
| Insight | What portable takeaway can the field reuse if the evidence holds? |

Two immediate checks:

1. Does `Method` truly serve `Problem`?
2. Can `Insight` stand independently, or is it only "our model works better"?

If `Insight` cannot be written without a metric claim, either narrow the `Problem` or design ablations that can reveal a real insight.

## Pseudo-Innovation Traps

### 1. Innovation without motivation

- Symptom: "We replaced module A with module B and gained 2%."
- Risk: The work explains what changed, not why the change solves a concrete problem.
- Repair: Tie each design choice to a specific limitation in the baseline and a visible mechanism.

### 2. Engineering stack disguised as research

- Symptom: Multiple known tricks are combined and the paper presents the sum as novelty.
- Risk: The reader learns no reusable principle.
- Repair: Either position the work as a stable general enhancer, or identify one core component and explain the interaction logic around it.

### 3. Cross-domain transplant as the whole story

- Symptom: "Method X worked in field A, so we moved it to field B."
- Risk: The paper reads as an application note unless the target field exposes a new failure mode or requires a new adaptation.
- Repair: Explain what breaks when copied directly, what was adapted, and what that adaptation reveals.

### 4. Metric-only storytelling

- Symptom: The main claim is a small benchmark gain.
- Risk: Reviewers can attribute the gain to tuning, seeds, or reproduction noise.
- Repair: Make the insight the claim and let the metric be supporting evidence.

### 5. Fragile "first" claim

- Symptom: The novelty depends heavily on "we are the first".
- Risk: A single earlier paper can collapse the positioning.
- Repair: Narrow the scope of the "first" claim and pair it with an insight that remains valuable even if priority is challenged.

## Falsifiability

Convert the core insight into 1-3 propositions that could be contradicted.

Good proposition pattern:

- Scoped setting: specify task, horizon, data type, condition, or population.
- Observable effect: state what should improve, degrade less, or behave differently.
- Failure condition: state what result would force revision.

Examples:

| Weak claim | Stronger falsifiable claim |
|---|---|
| Our method is better than all baselines. | For long-horizon settings with input length >= X, our method outperforms the strongest baseline on Y of Z datasets. |
| Frequency information is important. | The frequency branch provides larger gains on strongly periodic datasets than on weakly periodic datasets. |
| Our module is robust. | Under 10% missingness, the degradation in MSE is smaller than the strongest baseline by at least X. |

For each proposition, define:

1. Supporting evidence
2. Refuting evidence
3. Required ablation, contrast, robustness test, or qualitative check

## Pressure Tests

Use these prompts internally or adapt them for the user.

### Repetition test

Question: Has adjacent work already done this, or is this only a small variant?

Ask for:

- 3-5 closest works
- overlap and difference for each work
- a verdict: already done / adjacent but distinct / likely novel but needs literature verification

### Motivation test

Question: Why does this method solve that problem?

Ask for:

- at least 3 logic jumps
- reviewer-style wording for each challenge
- an overall coherence rating

### Falsifiability test

Question: What result would force the claim to be revised?

Ask for:

- 1-3 falsifiable propositions
- one experiment plan for each
- explicit support and rejection criteria

### Differentiation test

Question: How different is this from adjacent work?

Compare across:

1. Problem
2. Method
3. Technical details
4. Evidence or experimental setup
5. Insight

Mark each layer as no difference / weak difference / strong difference.

### Story test

Question: Can the work be explained clearly at three compression levels?

Require:

1. One-sentence version
2. Three-sentence version with Problem, Method, Insight
3. One short paragraph with the key evidence

## Integrity Rules

- Do not relax the claim after seeing weak evidence without stating the revision clearly.
- If experiments do not support the initial insight, say so and narrow the scope honestly.
- Prefer a smaller true claim over a broad fragile claim.
