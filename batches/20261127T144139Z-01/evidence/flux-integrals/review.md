# Review — Flux Integrals

Batch: `20261127T144139Z-01`
Article: `multivariable-calculus/flux-integrals.md`
Figures: `multivariable-calculus/svg/flux-integrals-{1,2,3}.svg`
Reviewed revision: `04e2511` (remote `origin/main`, clean checkout)
Reviewer: AI review (staging only)

## Scope and coverage

Audited the complete article, research evidence, figure briefs, illustration notes and all three SVGs. The article covers flux as signed flow, the definition, parameterization and graph formulas, constant field, radial field, inverse-square field, cube and cylinder, divergence theorem, open surface orientation and divergence as flux density. No verified upstream duplicate exists. No article or figure was changed during this review.

## Sources and checks

- Research evidence and cited sources were checked for flux formulas, divergence theorem hypotheses and example computations.
- All relative article links resolve to files present in the repository.
- All three SVG references resolve to files present in the repository.
- UTF-8/LF; YAML front matter present; H2-only body headings.
- LaTeX delimiters, `\tag{n}` labels and environments inspected manually. No TeX renderer is installed.

## Claim-by-claim proof audit

- Flow cylinder volume (1)-(3): `ΔV=(v·n) ΔS Δt`; flux as limit; correct.
- Definition (4)-(8): `∫∫_S F·dS = ∫∫_S F·n dS`; parameterization and graph formulas; sign conventions correct.
- Constant vertical field through a disk (9): flux `cπR^2`; tilt cancellation remark correct.
- Radial field through a sphere (10)-(12): `F·n=R`, flux `4πR^3`; divergence theorem check `div F=3` times volume; correct.
- Inverse-square field (13)-(16): `F·n=1/R^2`, flux `4π`; divergence zero away from origin; source strength and surface-enclosure distinction correct.
- Cube (17): divergence theorem gives `3`; face-by-face check gives `3`; correct.
- Cylinder (18): side flux `2πR^2 h`, top `πR^2 h`, bottom `0`, total `3πR^2 h`; correct.
- Divergence theorem (19)-(20): standard hypotheses; divergence as flux density limit; correct.
- Solenoidal-field consequence: flux through closed surface zero; flux through surfaces with same boundary equal when divergence-free in between; correct.
- Paraboloid example (21)-(27): cross product `<-2r^2 cos θ, -2r^2 sin θ, r>`, dot product `-2r^3`, integral `-π`; divergence-theorem consistency with outward flux `π`; correct.

## Independent computations

- Radial field flux: `R·4πR^2 = 4πR^3`.
- Inverse-square flux: `(1/R^2)·4πR^2 = 4π`.
- Paraboloid: `∫_0^{2π}∫_0^1 (-2r^3) dr dθ = -π`.
- Divergence-theorem check: solid volume `π/2`, `div F=2`, outward flux `π`; top disk contributes `0`.

## Counterexamples and edge cases

- Zero flux does not imply zero field: correctly stated.
- Sign dependence on orientation: correctly stated.
- Divergence theorem limitations with singularities: correctly stated.
- Open-surface dependence on surface and orientation: correctly stated.

## Editorial audit

No editorial defect found. The article has one coherent conceptual spine, consistent notation, and appropriate links to `parametric-surfaces`, `surface-integrals`, `divergence`, `curl` and `conservative-vector-fields`. No copied prose was identified; authorship is AI-assisted staging content.

## Per-figure audit

- `flux-integrals-1.svg`: XML parses; positive `width`/`height` matching `viewBox`; title and desc present; `aria-labelledby` targets present; unique IDs; live text only; no scripts, event handlers, foreignObject, raster images or external URLs. Geometry matches the signed flow-cylinder claim. Structural gate PASS.
- `flux-integrals-2.svg`: same structural checks PASS. Two concentric spheres labelled flux `4π` and a separate closed surface labelled zero flux match the inverse-square discussion.
- `flux-integrals-3.svg`: same structural checks PASS. Small box with stronger field leaving than entering matches the divergence-as-flux-density claim.

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
