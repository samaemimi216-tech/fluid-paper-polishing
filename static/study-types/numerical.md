# Numerical study

Build the paper around `problem -> model -> scheme -> verification -> validation -> physical or computational insight`.

- Separate the continuous model from its discrete realization.
- Explain what is coupled at the flux, interface, collision, source, or update level and why that matters.
- Present formal properties separately from empirical performance.
- Compare methods under matched meshes, time steps, stopping criteria, hardware, and error definitions where relevant.
- Report costs with a named measure such as wall time, memory, iteration count, degrees of freedom, or samples.
- Treat canonical cases as verification when they test implementation or accuracy; reserve validation for comparison with physical evidence or an accepted reference solution in its domain of validity.
