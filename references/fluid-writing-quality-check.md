# Fluid writing-quality check

Use this as an on-demand diagnostic when prose is technically correct but reads
as generic, inflated, or AI-like.

## Flag and repair

| Pattern | Repair |
|---|---|
| `remarkable`, `excellent`, `superior`, `promising` | Replace with the metric, baseline, condition, and tested range. |
| `robust` | Specify robust to what: grid, time step, Knudsen number, geometry, Reynolds number, noise, or training split. |
| `significant` | Use only for quantified magnitude or statistical testing. Otherwise state `large`, `measurable`, `non-negligible`, or the actual value. |
| `comprehensive` | Name the included regimes, methods, or evidence classes. |
| `novel` | Replace with the actual distinction from prior work. |
| `good agreement` | Report the error, uncertainty band, or the exact compared feature. |
| `validate correctness` | State the reference case, quantity, norm, and outcome. |
| `mechanism` | Use only when the causal chain is supported; otherwise write `behavior`, `trend`, or `interpretation`. |

## Rhythm and structure

- Do not make every paragraph 4-5 sentences. Short result paragraphs can carry a single finding; longer discussion paragraphs can carry conditions and caveats.
- Avoid repeated paragraph openings such as `The results show`, `It can be seen`, and `This indicates`.
- Let technical nouns repeat. Repetition of `distribution function`, `radiative intensity`, `Knudsen number`, or `Nusselt number` is clearer than synonym cycling.
- Keep a single dominant job per paragraph. If a paragraph introduces prior work, states the new method, reports results, and explains a mechanism, split it.

## Chinese-influenced English repairs

- `The influence law of X was studied` -> name the trend and controlling parameter.
- `The correctness of the model was verified` -> name the verification case and metric.
- `The simulation results are in good agreement` -> identify the reference and error/uncertainty.
- `The method has high accuracy and efficiency` -> state the order, error, cost, hardware, or baseline.
- `The mechanism was revealed` -> state the supported balance or hedge the mechanism.
