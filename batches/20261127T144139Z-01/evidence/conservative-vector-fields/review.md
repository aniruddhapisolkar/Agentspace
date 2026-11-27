# Review — Conservative Vector Fields

Batch: `20261127T144139Z-01`
Article: `multivariable-calculus/conservative-vector-fields.md`
Figures: `multivariable-calculus/svg/conservative-vector-fields-{1,2,3}.svg`
Reviewed revision: `b5c12a7` (remote `origin/main`, clean checkout)
Reviewer: AI review (staging only)

## Scope and coverage

Audited the complete article, research evidence, figure briefs, illustration notes and all three SVGs. The article is a standalone complement to the existing `vector-fields` and `line-integrals` articles; no verified upstream duplicate exists. No article or figure was changed during this review.

## Sources and checks

- Research packet cites OpenStax Calculus Volume 3 §§6.1, 6.3, 6.5 and Paul's Online Math Notes; definitions and hypotheses were checked against those cited sources.
- All relative article links resolve to files present in the repository.
- All three SVG references resolve to files present in the repository.
- UTF-8/LF; YAML front matter present; H2-only body headings; `+` bullets and `- - -` separators consistent with staging corpus.
- LaTeX delimiters, `\tag{n}` labels and environments inspected manually. No TeX renderer is installed, so rendered LaTeX was not checked.

## Claim-by-claim proof audit

- Definition (1) and potential uniqueness up to a constant on a connected open set: correct.
- Gravitational field (2)-(3): `∇(GM/r) = -GM r/r^3`; correct. Potential energy sign relation stated consistently.
- Non-conservative rotational field (4): the integration argument correctly shows no potential exists.
- Level-set orthogonality (5): correct by chain rule.
- Fundamental theorem for line integrals (6)-(7): correct.
- Converse construction (8): the horizontal-segment difference quotient tends to the component by continuity; correct.
- Curl/cross-partial tests (9)-(11): correct.
- Green's-theorem sufficiency argument (12): stated as an argument for a region bounded by two paths, with the general topological extension explicitly quoted; not overstated.
- Punctured-plane field (13)-(15): `Q_x = P_y = (y^2-x^2)/(x^2+y^2)^2`; circulation on the unit circle is `2π`; correct.
- Three-dimensional analogue (16): zero curl on `R^3` minus the `z`-axis and nonzero circulation; correct.
- Potential construction examples (17)-(22): all partial derivatives and cross partials checked; correct.
- Line-integral endpoint value (23): `f(1,1,1)-f(0,0,0)=3`; direct segment integral `∫_0^1 9t^2 dt = 3`; correct.
- Non-conservative example (24)-(26): integrals `13/15` and `5/6`; curl `1-2y`; correct.
- Energy relation (27): `W = U(A)-U(B)`; conservation statement correct.

## Independent computations

- `f=e^x sin y`: `f_x=e^x sin y`, `f_y=e^x cos y`, mixed partials equal.
- `F=<2xy+z^2, x^2+3y^2, 2xz>`: potential `x^2 y + y^3 + x z^2`; all three partials and all three cross partials verified.
- Rotational field: `curl = 2`, circulation signs `±π` checked in the related article.
- Punctured-plane circulation: integrand identically `1` on the unit circle.

## Counterexamples and edge cases

- Zero curl on a non-simply-connected domain does not imply conservatism: correctly handled by the punctured-plane example.
- Curl vanishing on a set of measure zero does not suffice: correctly stated.
- Disconnected domains and additive constants: correctly stated.
- Zero divergence distinguished from zero curl: correctly stated.

## Editorial audit

No editorial defect found. The article has one coherent conceptual spine, consistent notation, and appropriate links to `vector-fields`, `line-integrals`, `curl`, `divergence` and `tangent-planes-and-linear-approximations`. The "What the definition does not say" section is accurate. No copied prose was identified; authorship is AI-assisted staging content.

## Per-figure audit

- `conservative-vector-fields-1.svg`: XML parses; positive `width`/`height` matching `viewBox`; title and desc present; `aria-labelledby` targets present; unique IDs; live text only; no scripts, event handlers, foreignObject, raster images or external URLs. Geometry follows the brief: ellipses for `f=x^2+2y^2`, gradient arrows perpendicular to level curves, arrow lengths increasing on outer curves. Structural gate PASS.
- `conservative-vector-fields-2.svg`: same structural checks PASS. Two paths from `A` to `B` each cross the middle level curve once; endpoint annotation matches the theorem.
- `conservative-vector-fields-3.svg`: same structural checks PASS. Counterclockwise tangent arrows on two circles around an excluded origin; orientation consistent with circulation `2π`.

Chrome headless rendered all three files at intrinsic size without error. No visual inspection of the rendered pixels was performed in this environment.

## Changes made

None. No article, SVG or evidence file other than this review was modified.

## Limitations

- No image-capable visual inspection was available, so the mandatory visual gate is `NOT_RUN`.
- No TeX renderer was available, so rendered LaTeX was not checked; source-level LaTeX was inspected manually.
- Live site routes and GitHub's own SVG rendering were not checked.

## Gate statuses

| Gate | Status |
|---|---|
| Verified scope and credible source evidence | PASS |
| Correctness of material claims and proofs | PASS |
| All examples independently verified | PASS |
| Notation and domain consistency | PASS |
| Required files and metadata | PASS |
| Image paths and SVG XML integrity | PASS |
| Actual SVG rendering and visual inspection | NOT_RUN |
| Prose and LaTeX structure (source check) | PASS |
| Exact remote persistence | PENDING (commit in progress) |

## Final disposition

BLOCKED: mathematical, editorial and SVG structural gates pass, but the mandatory visual-inspection gate is `NOT_RUN` because no image-capable review was performed in this environment. No defect was found in the article or figures. Remaining work: visually inspect all three rendered SVGs at intrinsic size and at 240 px width in an image-capable environment, then re-run the visual gate and upgrade the topic to PASS.
