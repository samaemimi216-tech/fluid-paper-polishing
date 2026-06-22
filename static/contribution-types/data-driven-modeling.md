# Contribution type: data-driven modeling

Build the argument as:

`physical target -> data provenance -> model and constraints -> validation split -> generalization test -> interpretation/uncertainty -> deployment boundary`

- State how training, validation, and test data were generated and separated.
- Prevent leakage across time, geometry, Reynolds number, or simulation realization.
- Report baselines and metrics with dimensional or normalized meaning.
- Distinguish interpolation from out-of-distribution generalization.
- Preserve invariance, conservation, realizability, or other physical constraints when claimed.
- Treat feature maps, sparse terms, or learned correlations as physical insight only when independently tested.
