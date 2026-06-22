# Fluid-science integrity

Check these before sentence polishing:

- Regime: Reynolds, Mach, Knudsen, Prandtl, Rayleigh, Peclet, optical thickness, or other controlling parameters are defined and used consistently.
- Model scope: continuum versus kinetic, compressible versus incompressible, steady versus transient, gray versus non-gray, single- versus multiphase.
- Assumptions: dimensionality, constitutive law, collision model, local equilibrium, property variation, body forces, radiation or reaction coupling.
- Conditions: geometry, initial and boundary conditions, reference scales, material properties, and normalization.
- Numerics: mesh, time step, velocity/angular/frequency discretization, reconstruction, quadrature, convergence tolerance, and implementation details.
- Evidence: order of accuracy, conservation error, stability/positivity, asymptotic behavior, grid and time-step independence, benchmark or experimental agreement, efficiency, and limitations.

Do not convert `agrees with`, `is consistent with`, or `recovers` into `proves`. Do not call a method conservative, asymptotic-preserving, positive-preserving, high-order, stable, or efficient unless the manuscript supplies the corresponding analysis or test.
