# Governing equations and methods

Present material in this order when applicable:

`physical configuration -> assumptions -> governing equations -> constitutive or collision model -> initial/boundary conditions -> nondimensionalization -> discretization -> algorithm -> implementation settings`

- Use present tense for equations and method definitions; use past tense for the performed setup.
- State what each distribution function, source term, flux, closure, or correction represents.
- Explain the purpose of transformations and auxiliary variables before algebraic detail.
- Distinguish spatial, temporal, velocity-space, angular, spectral, and stochastic discretizations.
- Separate physical modeling error from discretization, sampling, optimization, and surrogate-model error.
- For parallel implementations, describe domain decomposition, communication, overlap, precision, hardware, and workload.
- For data-driven methods, define data generation, preprocessing, split strategy, architecture or basis, loss, constraints, and inference coupling.
- Name convergence criteria and reproducibility-critical parameters.
- Describe algorithm steps in causal order, not equation-number order.
