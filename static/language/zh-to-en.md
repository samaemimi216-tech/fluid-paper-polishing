# Chinese-to-English revision

Reconstruct the science before translating.

1. Extract the subject, action, condition, evidence, and boundary of each claim.
2. Restore omitted logical relations and explicit comparison baselines.
3. Replace Chinese topic-comment chains with physical subjects and verbs.
4. Split comma chains; keep conditions adjacent to the result they qualify.
5. Translate established technical terms consistently rather than literally.

Common repairs:

- `研究了` -> specify `examined`, `simulated`, `measured`, `derived`, or `evaluated`.
- `结果表明` -> state the result directly when the figure or data already provide attribution.
- `具有较高精度/效率` -> report the error, order, cost, or comparison conditions.
- `验证了正确性` -> specify what was verified and against which reference.
- `变化规律` -> name the trend and controlling parameter.
- `流动机理` -> use `mechanism` only when causal support exists; otherwise use `flow behavior` or `underlying dynamics`.
