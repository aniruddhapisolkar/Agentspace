# Review evidence — Multivariable Extrema and Saddle Points

Batch: `20261126T222013Z-01`
Slug: `multivariable-extrema-and-saddle-points`
Article: `multivariable-calculus/multivariable-extrema-and-saddle-points.md`
Reviewer: Reviewer
Reviewed revision: `16984f8` (remote `origin/main`)
Review date: 2026-11-26

## Scope and coverage

The complete article, its three SVG figures, research evidence, figure briefs and illustration notes were audited. The article is a focused multivariable treatment of local/global extrema, critical and saddle points, the second-derivative test, the two-variable determinant form, degenerate cases, compact-domain extrema and convexity.

## Sources and checks performed

- Read the full article and all linked evidence files.
- Independently checked the central mathematical results:
  - Fermat's theorem proof by coordinate restriction.
  - Second-derivative test proof from the second-order Taylor expansion.
  - Determinant classification for a symmetric 2x2 Hessian.
  - Worked example `f=x^3+y^3-3xy`: critical points `(0,0)` and `(1,1)`; Hessians and determinants `-9` and `27`; values `0` and `-1`.
  - Degenerate examples and their behaviour at the origin.
  - Compact-disk example `f=x^2+y^2-xy`: interior critical point at the origin; boundary values in `[1/2,3/2]`.
  - Convexity example `f=x^2+y^2+xy`.
- Checked front matter, H2-only headings, equation tags, image references and site-relative links at source level.
- Validated all three SVGs as XML; verified positive width/height/viewBox, live text, title/desc, and absence of scripts, external dependencies, raster content and unsupported elements.
- Checked SVG file paths against the article references and manifest.
- No LaTeX renderer was available; equations were checked by delimiter and tag inspection only.

## Claim-by-claim audit

All material claims, theorem hypotheses, proofs and worked examples listed in the research evidence were traced and found correct. No mathematical or editorial defect requiring correction was identified.

## Independent computations

- Critical-point equations for `x^3+y^3-3xy` give `x=x^4`, hence real critical points `(0,0)` and `(1,1)`.
- `f(1,1)=-1`; determinant at `(1,1)` is `27>0` with `f_xx=6>0`, so local minimum.
- `f(0,0)=0`; determinant at `(0,0)` is `-9<0`, so saddle point.
- On the unit disk, boundary values are `1-(1/2) sin 2t`, range `[1/2,3/2]`; interior value is `0`.

## Editorial audit

Front matter, tags, heading structure, British English, equation references and image paths are consistent with the batch conventions. Site-relative links point to verified siblings or existing upstream routes.

## Per-figure audit

- `multivariable-extrema-and-saddle-points-1.svg`: XML valid; dimensions and viewBox match; title/desc present; no external dependencies or scripts.
- `multivariable-extrema-and-saddle-points-2.svg`: XML valid; dimensions and viewBox match; title/desc present; no external dependencies or scripts.
- `multivariable-extrema-and-saddle-points-3.svg`: XML valid; dimensions and viewBox match; title/desc present; no external dependencies or scripts.

Source-level SVG geometry was checked only for XML and reference integrity. Rendered appearance, overlap, clipping, label legibility and visual accuracy were not verified.

## Changes made

None. No defect in the article or SVGs was found during this audit.

## Gate statuses

| Gate | Status |
|---|---|
| Verified scope and credible source evidence | PASS |
| Correctness of all material claims/proofs | PASS |
| All examples independently verified | PASS |
| Notation/domain consistency | PASS |
| Required files/metadata | PASS |
| Image path and SVG XML integrity | PASS |
| Actual SVG rendering and visual inspection | NOT_RUN |
| Prose/LaTeX structure | PASS |
| LaTeX rendering | NOT_RUN |
| Exact remote persistence | PASS |

## Limitations

The mandatory actual SVG rendering and visual-inspection gate could not be run: no image-capable model or tool is available in this environment, so no rendered figure was seen. The LaTeX rendering gate was also not run; equations were checked by source inspection only.

## Final disposition

BLOCKED. Mathematical, editorial and SVG structural gates pass, but the mandatory visual-inspection gate is `NOT_RUN`, so reviewer PASS cannot be granted. Remaining work: render and visually inspect all three figures at intrinsic size and 240 px width in an image-capable environment, then re-run affected gates and upgrade this topic to PASS.

AI-reviewed staging content; not human-approved or authorized for upstream publication.
PY
echo done