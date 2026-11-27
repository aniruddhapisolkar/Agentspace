# Review evidence — Change of Variables in Multiple Integrals

Batch: `20261127T121407Z-01`
Slug: `change-of-variables-in-multiple-integrals`
Article: `multivariable-calculus/change-of-variables-in-multiple-integrals.md`
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

- Article reviewed in full (233 lines). Research, figure briefs, illustration notes read.
- 3 figures: polar area element, linear map of unit square, disc-to-ellipse map.
- Not a duplicate (1D substitution and polar area element are prerequisites/special cases).

## Sources and checks

- Sources: MAT237 §4.4, OpenStax §5.7, Spivak, Algebrica. Locators consistent (Spivak chapter cited, not numbered — matches research limitation).
- Structure: YAML, H2-only, tags (1)–(9) sequential.
- Math: 1D substitution (1); theorem (2)–(5) with C¹ bijection, nonvanishing Jacobian, compact measurable sets, boundary negligible; hypotheses discussion (bijection on open sets, local diffeomorphism via inverse function theorem, piecewise C¹); why Jacobian (6) linear volume scaling; local linearisation sketch (labelled sketch, error controlled by uniform continuity); polar determinant r; cylindrical r (7); spherical −ρ² sinφ (8) absolute value; affine map area 2/moment 2; ellipse area πab/moment πa³b/4; failure modes: non-injectivity (u²,v) multiplicity 2 vs area 1, vanishing Jacobian on u=0, missing absolute value (u,−v)→−1, C¹ regularity; relation to inverse function theorem and chain rule for determinants; procedure summary.
- Independent computations:
  - affine map area |det|=2, first moment 2 ✓
  - ellipse area πab (a=2,b=3→6π), second moment πa³b/4 (→6π) ✓
  - disc moment ∫∫ u² = π/4 ✓
  - non-injective multiplicity ∫_{-1}^1 2|u| du = 2 ✓
  - polar Gaussian over unit disc π(1−e⁻¹) ✓
- SVG structural audit (all 3): XML OK, dims 320×276, 340×248, 340×232, viewBox match, unique IDs, aria-labelledby resolve, live text (8/19/12), no scripts/rasters/externals. Chrome render OK.

## Per-figure

- change-of-variables-in-multiple-integrals-1.svg: curvilinear polar cell, dr, r dθ. Rendered.
- change-of-variables-in-multiple-integrals-2.svg: unit square → rotated square area 2, basis images. Rendered.
- change-of-variables-in-multiple-integrals-3.svg: unit disc → ellipse, areas π and πab. Rendered.
- Visual inspection: NOT_RUN.

## Changes made

None.

## Limitations

- Visual gate NOT_RUN.
- LaTeX renderer unavailable.
- Live route proposed.

## Final disposition

BLOCKED — visual gate NOT_RUN. AI-reviewed staging content; not human-approved or authorized for upstream publication.
