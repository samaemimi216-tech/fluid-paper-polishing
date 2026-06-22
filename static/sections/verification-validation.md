# Verification and validation

Use the evidence ladder:

1. recover the intended limiting equation or analytical behavior;
2. demonstrate formal or observed order of accuracy;
3. establish mesh, time-step, and auxiliary-space convergence;
4. quantify conservation, boundedness, positivity, or stability where claimed;
5. compare with analytical, manufactured, benchmark, DSMC/DNS, or experimental references;
6. test the difficult regime targeted by the method;
7. report computational cost under fair conditions.

For equilibrium-preserving methods, test the equilibrium state and quantify residual/spurious motion. For data-driven closures, add held-out and out-of-distribution tests plus a-posteriori solver behavior. For parallel codes, distinguish throughput, strong scaling, weak scaling, and efficiency.

State the case, parameters, reference, error norm, and outcome. Replace `good agreement` with a quantitative error or a clearly specified visual agreement. Do not use `validated` when only grid independence was shown.
