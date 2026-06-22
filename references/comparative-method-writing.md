# Comparative method writing

## Required comparison frame

State:

- governing model and boundary conditions;
- mesh, time step/CFL, velocity or angular discretization;
- convergence criterion and error norm;
- implementation, precision, hardware, and parallel setup when cost is compared;
- reference solution and parameter range.

## Paragraph order

1. identify the property being compared;
2. explain the algorithmic difference relevant to that property;
3. report the matched result;
4. quantify advantage and penalty;
5. state the regime-dependent implication.

Avoid mixing accuracy, stability, and efficiency into one adjective. A method may be more accurate on the same mesh but slower per step, or cheaper in one regime and noisier in another.
