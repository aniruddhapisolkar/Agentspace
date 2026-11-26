# Review evidence — Lagrange Multipliers

Batch: `20261126T222013Z-01`
Slug: `lagrange-multipliers`
Article: `multivariable-calculus/lagrange-multipliers.md`
Reviewer: Reviewer
Reviewed revision: `16984f8` (remote `origin/main`)
Review date: 2026-11-26

## Scope and coverage

The complete article, its three SVG figures, research evidence, figure briefs and illustration notes were audited. The article covers constrained optimisation, tangency of level sets, the multiplier theorem for one and several constraints, the method, examples, and the multiplier as a sensitivity.

## Sources and checks performed

- Read the full article and all linked evidence files.
- Independently checked the central mathematical results:
  - First example `f=xy` on `x^2+y^2=1`: four candidates, maximum `1/2`, minimum `-1/2`.
  - Distance-to-plane example: point `(7/9,14/9,23/9)`, squared distance `4/9`, distance `2/3`.
  - Two-constraint example: point `(1/3,1/3,1/3)`, value `1/3`.
  - Sensitivity formula `M(c)=(c-11)^2/9`, derivative `-4/9` at `c=9`.
  - Failure example `x^2+y^2=0`, where the constraint gradient vanishes.
- Checked front matter, H2-only headings, equation tags, image references and site-relative links at source level.
- Validated all three SVGs as XML; verified positive width/height/viewBox, live text, title/desc, and absence of scripts, external dependencies, raster content and unsupported elements.
- Checked SVG file paths against the article references and manifest.
- No LaTeX renderer was available; equations were checked by delimiter and tag inspection only.

## Claim-by-claim audit

All material claims, theorem hypotheses, proofs and worked examples listed in the research evidence were traced and found correct. No mathematical or editorial defect requiring correction was identified.

## Independent computations

- `x=7/9, y=14/9, z=23/9` satisfies `x+2y+2z=9`; squared distance `4/9`.
- `(1/3,1/3,1/3)` satisfies both constraints and gives value `1/3`.
- `M'(9)=-4/9`, equal to the multiplier found.

## Editorial audit

Front matter, tags, heading structure, British English, equation references and image paths are consistent with the batch conventions. Site-relative links point to verified siblings or existing upstream routes.

## Per-figure audit

- `lagrange-multipliers-1.svg`: XML valid; dimensions and viewBox match; title/desc present; no external dependencies or scripts.
- `lagrange-multipliers-2.svg`: XML valid; dimensions and viewBox match; title/desc present; no external dependencies or scripts.
- `lagrange-multipliers-3.svg`: XML valid; dimensions and viewBox match; title/desc present; no external dependencies or scripts.

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