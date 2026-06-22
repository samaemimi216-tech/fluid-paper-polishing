---
name: fluid-paper-polishing
description: Polish, restructure, or translate fluid-mechanics, computational-fluid-dynamics, kinetic-theory, multiphase-flow, heat-and-mass-transfer, and radiative-transport manuscripts into publication-quality English. Use for titles, abstracts, introductions, governing equations, numerical or experimental methods, verification and validation, results, discussions, conclusions, captions, and Chinese-to-English revision, especially when claims must follow field conventions for flow regimes, nondimensional parameters, conservation, accuracy, stability, benchmark agreement, uncertainty, and physical interpretation.
---

# Fluid Paper Polishing

This skill follows a static/dynamic split:

- `static/` stores reusable core rules and narrowly scoped fragments.
- this router plus `manifest.yaml` detects the request and loads only the necessary fragments.

Do not polish from the router alone. Update fragments rather than expanding the router when adding a journal, study type, section, or physical domain.

## Route the request

1. Read [manifest.yaml](manifest.yaml).
2. Read every file under `always_load`.
3. Detect and state one short routing line:
   `study_type | section | language | journal | physics`.
4. Load only the matching axis fragments. If the user supplies a standalone paragraph, omit `section` only when its function cannot be inferred.
5. Load an on-demand reference only when its condition in the manifest applies.

Default to `numerical`, `generic`, and `general-fluids` when evidence is insufficient. Do not ask about an axis unless the choice would materially change the revision.

## Revise in scientific order

Apply the loaded guidance in this order:

1. Preserve the scientific meaning, symbols, data, citations, and contribution boundary.
2. Diagnose `study type -> section job -> paragraph logic -> claim/evidence/boundary -> sentence`.
3. Repair the section's rhetorical job and paragraph logic.
4. Check claim-evidence alignment and fluid-mechanics validity.
5. Lock terminology, notation, tense, and comparison baselines.
6. Improve sentence economy and journal fit.

Never invent equations, parameter values, boundary conditions, validation cases, uncertainty estimates, mechanisms, citations, or novelty. Flag missing scientific support instead of hiding it with fluent prose.

## Handle equations and symbols

- Preserve equation content unless the user explicitly requests a derivation or correction.
- Define every symbol at first use and keep scalar, vector, tensor, dimensional, and nondimensional notation consistent.
- Distinguish model assumptions, governing equations, constitutive closures, boundary conditions, discretization, and solver settings.
- Keep dimensionless numbers and regimes attached to the conditions they characterize.
- Treat a suspected dimensional, physical, or numerical inconsistency as a query, not a silent edit.

## Deliver

Follow the loaded output format. Return polished prose outside code blocks. Keep LaTeX notation intact. If support is missing, use an explicit author query such as `[Author query: report the grid-refinement criterion.]`.

## Why this split

- A new journal, physical domain, or section requires one fragment and one manifest entry.
- Core integrity rules remain reviewable and always loaded.
- A routine paragraph edit does not consume the full domain library.
