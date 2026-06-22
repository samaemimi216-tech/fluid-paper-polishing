# Numerical evidence checklist

Match each claim to evidence:

| Claim | Minimum support |
|---|---|
| high-order accuracy | error norm, refinement sequence, observed order, smooth test |
| conservative | defined conserved quantities and discrete or measured balance error |
| positive-preserving | stated variable, conditions/CFL, proof or stress test |
| asymptotic-preserving | limiting analysis plus tests without resolving the small scale |
| stable/robust | parameter range and failure criterion, not successful runs alone |
| efficient | matched implementation conditions and a named cost metric |
| accurate | quantitative error against a suitable reference |
| multiscale | tests spanning the relevant nondimensional regimes |
| geometry-capable | boundary treatment plus curved/moving/complex-domain tests |

Also check spatial, temporal, velocity/angular/frequency, and statistical convergence separately when they coexist.
