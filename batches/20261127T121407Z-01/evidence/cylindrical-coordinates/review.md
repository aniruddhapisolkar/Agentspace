# Review evidence — Cylindrical Coordinates

Batch: `20261127T121407Z-01`
Slug: `cylindrical-coordinates`
Article: `multivariable-calculus/cylindrical-coordinates.md`
Reviewed revision: `636ab4d`
Review date: 2026-11-27

## Gate statuses

| Gate | Status |
|---|---|
| Verified scope and credible source evidence | PASS |
| Correctness of all material claims/proofs | PASS |
| All examples independently verified | PASS |
| Notation/domain consistency | PASS |
| Required files/metadata | PASS |
| Image paths and SVG XML integrity (figures) | PASS |
| Actual SVG rendering and visual inspection (figures) | NOT_RUN |
| Prose/LaTeX structure | PASS |
| Exact remote persistence | PENDING |

Overall disposition: **BLOCKED** — visual gate NOT_RUN.

## Scope and coverage

- Article reviewed in full (218 lines). Research, figure briefs, illustration notes read.
- 3 figures: point coordinates triad, volume element, paraboloid cap.
- Not a duplicate (no upstream cylindrical article; polar article gives a different 3D convention).

## Sources and checks

- Sources: MAT237 §4.4, OpenStax §5.5, Algebrica polar. Locators consistent.
- Structure: YAML, H2-only, tags (1)–(7) sequential.
- Math: conversion (1)(2), ranges (3), non-uniqueness on axis/periodicity, coordinate surfaces (r=a cylinder, θ=α half-plane, z=c plane, z=r cone, z=r² paraboloid), Jacobian determinant r (4), volume element r dr dθ dz (5), integral reduction (6), setup procedure, examples: cylinder πR²H, paraboloid 8π, cone 8π/3, density mass 2π/centroid 4/3, sphere-cut-by-cylinder 4π/3(8−3√3), pitfalls, relation to spherical (7).
- Independent computations:
  - cylinder, paraboloid 8π, cone 8π/3 ✓
  - density mass 2π, first moment 8π/3, z̄=4/3 ✓
  - sphere cut by cylinder ≈11.7447 ✓
- Jacobian r verified (block triangular polar block).
- SVG structural audit (all 3): XML OK, dims 330×250, 336×268, 340×288, viewBox match, unique IDs, aria-labelledby resolve, live text (10/4/5), no scripts/rasters/externals. Chrome render OK.

## Per-figure

- cylindrical-coordinates-1.svg: point P, projection Q, r, θ, z. Rendered.
- cylindrical-coordinates-2.svg: curvilinear box, dr, r dθ, dz. Rendered.
- cylindrical-coordinates-3.svg: paraboloid cap, vertical limits, r=2 circle. Rendered.
- Visual inspection: NOT_RUN.

## Changes made

None.

## Limitations

- Visual gate NOT_RUN.
- LaTeX renderer unavailable.
- Live route proposed.

## Final disposition

BLOCKED — visual gate NOT_RUN. AI-reviewed staging content; not human-approved or authorized for upstream publication.
