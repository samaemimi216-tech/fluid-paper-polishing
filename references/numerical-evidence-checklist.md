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
| well-balanced/equilibrium-preserving | discrete balance analysis plus equilibrium residual or spurious-velocity test |
| entropy-stable/entropic | stated entropy functional, admissibility conditions, and nonlinear stress test |
| form-invariant/physics-constrained learning | invariant basis or constraint plus unseen-state and a-posteriori tests |
| scalable/parallel-efficient | hardware, workload, communication strategy, strong/weak scaling, and efficiency definition |
| generalizable data-driven model | leakage-safe split and tests across unseen regime, geometry, or realization |

Also check spatial, temporal, velocity/angular/frequency, and statistical convergence separately when they coexist.
