# Review evidence — Spherical Coordinates

Batch: `20261127T121407Z-01`
Slug: `spherical-coordinates`
Article: `multivariable-calculus/spherical-coordinates.md`
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

- Article reviewed in full (239 lines). Research, figure briefs, illustration notes read.
- 3 figures: point coordinates triad, volume element, ice-cream cone.
- Not a duplicate (polar article gives a different convention/letter; no spherical integration upstream).

## Sources and checks

- Sources: MAT237 §4.4, OpenStax §5.5, Algebrica polar. Locators consistent.
- Structure: YAML, H2-only, tags (1)–(8) sequential.
- Math: conversion (1)(2), ranges (3), non-uniqueness, convention note (ρ distance, θ azimuth, φ from +z), coordinate surfaces (ρ=R sphere, θ=α half-plane, φ=β cone z=cotβ r), Jacobian −ρ² sinφ (4), absolute value (5), volume element ρ² sinφ dρ dφ dθ (6), reduction (7), setup, examples: ball 4πR³/3, z² moment 4π/15 (checked by symmetry/ρ² integral), ice-cream cone 16π/3(1−√2/2), radial density mass 7π/3, spherical cap volume π/3(2R³−3R²a+a³) with non-star-shaped derivation and lower limit a secφ — derivation re-derived and verified (a=0→half ball, a=R→0), pitfalls, relation to cylindrical (8).
- Independent computations: ball, moment, cone, density, cap (R=1,a=0.5→0.6545) ✓. Cap also checked by slice formula π∫_a^R(R²−z²) dz.
- Jacobian sign verified: −ρ² sinφ for column order (ρ,θ,φ); absolute value ρ² sinφ.
- SVG structural audit (all 3): XML OK, dims 330×256, 340×300, 320×312, viewBox match, unique IDs, aria-labelledby resolve, live text (8/4/4), no scripts/rasters/externals. Chrome render OK. (Illustration notes flag spherical volume element as least legible at 240 px — to be confirmed by visual inspection.)

## Per-figure

- spherical-coordinates-1.svg: ρ, θ azimuth of projection, φ from +z. Rendered.
- spherical-coordinates-2.svg: curvilinear cell, dρ, ρ dφ, ρ sinφ dθ. Rendered.
- spherical-coordinates-3.svg: ice-cream cone, ρ=2, φ=π/4, pole marked. Rendered.
- Visual inspection: NOT_RUN.

## Changes made

None.

## Limitations

- Visual gate NOT_RUN (no image-capable model) — flagged 240 px legibility of spherical volume element remains unverified.
- LaTeX renderer unavailable.
- Live route proposed.

## Final disposition

BLOCKED — visual gate NOT_RUN. AI-reviewed staging content; not human-approved or authorized for upstream publication.
