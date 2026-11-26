# Review evidence — Limits of Multivariable Functions

Batch: `20261126T193918Z-01`
Slug: `limits-of-multivariable-functions`
Article: `multivariable-calculus/limits-of-multivariable-functions.md`
Reviewed revision (pre-commit): `0107660189e377b2b6ddcbc43da724b5a9fdc031`
Reviewer: Reviewer (AI), 2026-11-26

## Scope and coverage

- Upstream duplicate check: no multivariable-limits article found in `antoniolupetti/algebrica` (shallow clone searched by filename and body terms "multivariable"/"several variables"/"path"). Verified duplicate status: not a duplicate.
- Single-variable limit, continuity, sequences, norm and inequalities assumed as prerequisites; exclusions (uniform continuity, general topology, vector-valued maps, differentiability) stated in research.md.
- Three figures (F1 two-path diagram, F2 epsilon-delta disc/band, F3 contour map of `xy^2/(x^2+y^4)`) present and anchored in the article.

## Sources and actual checks

- OpenStax Calculus Volume 3 §4.2 read in full; used for definition, path dependence, iterated limits, continuity, compactness.
- Upstream `derivatives/partial-derivatives.md` and `limits/limits.md` consulted for conventions only.
- Independent proofs written out for uniqueness, sequential criterion, path test, iterated-limit proposition, polar criterion.
- Python `fractions.Fraction` checks recorded in research.md: `xy/(x^2+y^2)` path values 0 and 1/2; inequalities `|x^2 y/(x^2+y^2)| <= |y|` and `x^2 y^2/(x^2+y^2) <= (x^2+y^2)/4` in 20,000 trials; `xy^2/(x^2+y^4)` along `(t^2,t)` = 0.5 and along `y=1.7x` -> 0.
- SVG structural validation: all 3 files parse as XML, positive width/height/viewBox, live text elements, no scripts/external hrefs/raster. Chrome headless rendered all 3 to PNG without error (intrinsic size).

## Claim-by-claim proof audit

- Definition (1): correct epsilon-delta formulation with accumulation-point hypothesis. PASS.
- Uniqueness: epsilon = |L-M|/3 argument valid; triangle inequality contradiction correct. PASS.
- Sequential criterion: both directions valid; construction of x_k with 0<||x_k-x0||<1/k valid. PASS.
- Limit laws and composition: standard, supported by OpenStax. PASS.
- Polar criterion with uniformity warning: valid; counterexample `xy^2/(x^2+y^4)` correctly shows angular dependence. PASS.
- `xy/(x^2+y^2)` nonexistence: path values 0 vs 1/2 correct. PASS.
- `x^2-y^2` over `x^2+y^2`: 1 vs -1 correct. PASS.
- `xy^2/(x^2+y^4)`: lines give 0; parabola x=y^2 gives 1/2. Verified: f(t^2,t)=t^4/(t^4+t^4)=1/2. PASS.
- Iterated limits: simultaneous 0 for xy/(x^2+y^2) with both iterated limits 0 (verified); `x sin(1/y)` simultaneous 0 (bounded by |x|) with non-existent inner limit for x≠0. PASS.
- Compactness statement: standard extreme value theorem. PASS.
- Inequality `|x^2 y/(x^2+y^2)| <= |y|`: since x^2 <= x^2+y^2, yes. PASS.
- `x^2 y^2/(x^2+y^2) <= (x^2+y^2)/4`: from 4x^2 y^2 <= (x^2+y^2)^2, yes. PASS.

## Edge cases / counterexamples attempted

- Attempted falsification of polar criterion by varying theta; angular dependence correctly blocks proof. PASS.
- Boundary/accumulation-point and isolated-point remarks checked. PASS.

## Editorial audit

- Front matter: title/source/license/tags present; source is proposed canonical route. PASS.
- H2-only body headings; sentence case. PASS.
- `$$...$$` displays and `$...$` inline; one tagged equation `\tag{1}` referenced once. PASS.
- British spellings (neighbourhood, centre, parametrised) consistent. PASS.
- Site-relative links `../partial-derivatives/` (published) and `../tangent-planes-and-linear-approximations/` (unpublished sibling, disclosed in research.md). PASS with disclosed dependency.
- No images inserted outside SVG anchors; alt-text equivalent in figure files. PASS.

## Per-figure geometry and render checks

- F1: paths y=0 and y=x; values 0 and 1/2 placed on correct axes; open origin not a value. SVG XML valid; Chrome render succeeded (7852 bytes).
- F2: punctured disc with open centre; epsilon band; f(x) inside band. SVG XML valid; Chrome render succeeded (9271 bytes).
- F3: level curves are exact parabolas x=k y^2; ridge x=y^2 labelled 1/2; dashed straight lines through origin; inset peak at x=0.36 value 0.5. SVG XML valid; Chrome render succeeded (18075 bytes).

## Gate statuses

| Gate | Status | Notes |
|---|---|---|
| Verified scope & credible source evidence | PASS | OpenStax §4.2 read; upstream checked |
| Correctness of material claims/proofs | PASS | All proofs traced |
| All examples independently verified | PASS | Python exact checks recorded |
| Notation/domain consistency | PASS | |
| Required files/metadata | PASS | |
| Image path & SVG XML integrity (figures exist) | PASS | 3/3 resolve; XML valid |
| Actual SVG rendering & visual inspection | NOT_RUN | Chrome headless rendered all 3 to PNG without error, but this model has no image input, so pixel content was not visually inspected. Mandatory visual gate therefore not satisfied. |
| Prose/LaTeX structure | PASS | Delimiter balance checked by inspection |
| Markdown/LaTeX renderer availability | NOT_RUN | No renderer available; source-level check only |
| Exact remote persistence | PENDING | To be verified after commit |

## Changes made

- None to article or SVGs; no mathematical or structural defect found. Review evidence added.

## Limitations

- Visual inspection of rendered PNGs not possible in this environment (no image-capable model). This is the sole unresolved mandatory gate.
- Second full textbook treatment not retrieved; central results independently proved (recorded in research.md).

## Final disposition

BLOCKED — mandatory visual-inspection gate NOT_RUN. Mathematical, editorial and SVG-structural gates PASS. Remote persistence to be verified after commit.

AI-reviewed staging content; not human-approved or authorized for upstream publication.
PY