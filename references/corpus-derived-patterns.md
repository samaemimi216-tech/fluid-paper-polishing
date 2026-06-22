# Corpus-derived patterns

This skill was calibrated against 69 local PDF artifacts: the original 29-paper kinetic/heat-transfer collection plus 40 newly added top-journal papers.

## Corpus coverage

- *Journal of Computational Physics*: UGKS/UGKWP, DUGKS/LBM comparison, stochastic BGK, high-order and property-preserving schemes.
- *Journal of Fluid Mechanics*: turbulence and heat transfer, discrete-Boltzmann multiphase flow, gas-kinetic boundaries, closures, and porous-media evaporation.
- *Physics of Fluids* and *Physical Review Fluids/E*: well-balanced and simplified LBM, rarefied gas-surface interaction, immersed boundaries, pore-scale flow, flow-radiation coupling, and particle heat transfer.
- *International Journal of Heat and Mass Transfer*: multiscale reviews, thermal LBM/HPC, radiative transfer, porous transport, interfacial area, and phase change.
- *Progress in Energy and Combustion Science*: critical reviews of multiphase/phase-change LBM, pore-scale transport, and combustion machine learning.

## Recurring argument patterns

### Method development

1. identify a discrete or modeling defect;
2. locate its algorithmic cause;
3. introduce one operative correction;
4. state the property expected from that correction;
5. verify the property separately from benchmark accuracy;
6. report the accuracy, stability, cost, or regime trade-off.

### Physical investigation

1. define the physical question and controlling parameters;
2. describe a diagnostic-quality setup;
3. report the dominant trend or structure quantitatively;
4. identify the controlling balance or mechanism;
5. reduce the result to a regime map, scaling, or model where justified;
6. bound the interpretation.

### Comparison study

1. place methods in one mathematical framework;
2. isolate the exact difference in flux, quadrature, collision, boundary, or update;
3. compare under matched conditions;
4. separate accuracy, stability, and cost;
5. recommend by regime instead of declaring an unconditional winner.

### Review article

1. define scope and terminology;
2. construct a taxonomy;
3. compare approaches on repeated axes;
4. synthesize applications and evidence;
5. identify causes of persistent limitations;
6. derive a prioritized outlook.

Use these as rhetorical moves, not reusable sentences. Do not copy wording from the corpus or treat frequency as proof of scientific correctness.
