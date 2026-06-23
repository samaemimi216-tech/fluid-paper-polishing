# Section architecture for fluid papers

Use this when rewriting a complete section or when the draft has a structural
problem that sentence-level polishing cannot fix.

## Architecture rule

For each section, identify:

1. `purpose` - the job the section must perform for the reader;
2. `core claim` - the main statement the section supports;
3. `evidence` - equations, validation cases, figures, experiments, references, or error/cost metrics;
4. `boundary` - assumptions, regimes, geometries, parameter ranges, and failure cases;
5. `handoff` - what the next section can assume after this section.

If any item is absent, preserve the defensible prose and add an author query.

## Title

The title should expose the method, phenomenon, or bounded finding. In the local
corpus, strong titles usually combine a technical object with a defining
property or regime: multiscale, asymptotic-preserving, positive-preserving,
non-gray, pore-scale, rarefied, particle-laden, or radiative. Do not add such
properties unless the manuscript proves or tests them.

## Abstract

Use the contribution-specific move order:

- Method paper: `context -> precise defect -> operative change -> property -> tests -> quantified result -> scope`.
- Physical paper: `phenomenon -> unresolved question -> setup/regime -> observation -> mechanism -> boundary -> implication`.
- Data-driven paper: `prediction/closure problem -> data -> model constraints -> held-out test -> generalization -> interpretation -> limits`.
- Review paper: `area need -> synthesis need -> taxonomy -> comparison axes -> mature findings -> open challenges -> user value`.

Compress benchmark lists. Keep only the tests needed to support the claims.

## Introduction

Build a funnel with five paragraph jobs:

1. physical or engineering relevance and controlling regime;
2. model hierarchy or method families;
3. prior limitations grouped by cause, not by paper order;
4. unresolved gap stated as a precise limitation;
5. contribution and evidence plan.

For method papers, the gap should name the failure source: stiffness, scale
separation, discrete force imbalance, geometric complexity, velocity-space
resolution, angular/frequency discretization, conservation error, positivity,
data scarcity, or cost.

## Formulation and methods

Order the material as:

`configuration -> assumptions -> governing equations -> constitutive/collision/closure model -> initial and boundary conditions -> nondimensionalization -> discretization -> algorithm -> implementation settings`.

Do not let equation-number order override conceptual order. Define what each
distribution function, source term, correction, closure, or flux represents
before discussing algebraic details.

## Verification and validation

Separate evidence layers:

- mathematical recovery or limiting behavior;
- formal or observed order of accuracy;
- grid, time-step, velocity-space, angular, frequency, stochastic, or sample convergence;
- conservation, boundedness, positivity, stability, or equilibrium preservation;
- benchmark, DSMC/DNS, analytical, manufactured, or experimental agreement;
- difficult-regime tests;
- cost, memory, iteration count, or parallel efficiency under fair conditions.

Do not call grid independence `validation`. Do not call one benchmark `robust`.

## Results

Each result unit should answer:

`question -> conditions -> observation -> quantitative support -> comparison -> local boundary`.

Name the quantity, location, averaging operation, time, and nondimensional
range. Describe what a figure shows before proposing why it occurs.

## Discussion

Move from finding to interpretation:

`principal finding -> mechanism or balance -> comparison with prior work -> implication -> limitation -> next question`.

Use causal verbs only when the evidence supports causality. Otherwise use
`is consistent with`, `is attributed to`, or `may arise from`.

## Conclusion

Do not recap the paper section by section. State the final answer, the strongest
evidence, the usable boundary, and the next technical consequence. Avoid
`future work will focus on` unless the direction follows from a limitation.
