# Review evidence — Vector Fields

Batch: `20261127T134100Z-01`
Slug: `vector-fields`
Article: `multivariable-calculus/vector-fields.md`
Reviewed revision: `2912bb1`
Reviewer: AI reviewer (algebrica-reviewer skill)
Review date: 2026-11-27

## Scope and coverage

- Writer `WRITTEN`, Illustrator `ILLUSTRATED`, 3 figures.
- Research, figure briefs, illustration notes present and read.
- No upstream duplicate (verified via research.md).

## Sources and actual checks

- Standard vector calculus references; upstream Algebrica `vectors.md` (notation/links).
- Independent arithmetic checks:
  - Gradient example f=x²y+y³ → ∇f=⟨2xy, x²+3y²⟩; at (1,2) = ⟨4,13⟩. Verified.
  - Rotational field (6) ∇f contradiction proof: φ'(y)=2x impossible. Correct.
  - Worked example F=⟨x²−y, x+y²⟩: div=2x+2y, curl=∂(x+y²)/∂x − ∂(x²−y)/∂y = 1 − (−1)=2. At (1,2): div=6, curl=2. Verified.
  - Counterexample (16): curl=0 on punctured plane; unit-circle integral ∫₀²π dt = 2π. Verified.
  - Divergence of (16): ∂/∂x(−y/(x²+y²)) = 2xy/(x²+y²)²; ∂/∂y(x/(x²+y²)) = −2xy/(x²+y²)²; sum 0. Verified.
  - Inverse-square field (5) is gradient of −1/r; conservative on simply connected domain. Verified.

## Claim-by-claim audit

- Definitions (1)–(2): correct.
- Unit field (3), radial (4), inverse-square (5), rotational (6), gradient (7): correct.
- Conservative definition (8), FTC for line integrals (9)–(10): correct.
- Field-line ODE (11)–(13): correct.
- Scalar curl (14)–(15): correct.
- Counterexample (16)–(17): correct.
- Vector-space operations (18), Helmholtz decomposition (19): stated with regularity/decay caveats. Acceptable.
- Worked example: correct.

## Counterexamples / edge cases

- Zero curl not sufficient without simple connectedness: stated with punctured-plane example.
- Potential sign convention physics vs math: stated.
- Unit field undefined at zeros: stated.

## Editorial audit

- YAML, H2-only, tags (1)–(19) sequential, inline/display LaTeX consistent.
- Links to divergence, curl, Laplacian, line-integrals, double/triple integrals: present.
- Prose style appropriate.

## SVG audit (structural + geometry)

Files: `vector-fields-{1,2,3}.svg`.

- XML parse OK; positive dims/viewBox match; IDs fig-title/fig-desc; aria-labelledby resolves; live text only; no scripts/rasters/externals.
- Palette monochrome.
- Fig 1: radial + rotational fields side by side to same scale; matches article.
- Fig 2: gradient arrows crossing elliptical level curves at right angles, denser where curves closer; matches article.
- Fig 3: circulating field on punctured plane with closed loop around excluded origin; matches article.
- Render check: Chrome headless rendered all 3 at intrinsic and 240 px without error.

## Visual inspection

- Gate: NOT_RUN (no image-capable tool in this environment).

## Changes made

- None. No defects found.

## Limitations

- No LaTeX renderer; structural check only.
- Live routes/upstream PRs not checked.

## Gate statuses

| Gate | Status |
|---|---|
| Verified scope and credible source evidence | PASS |
| Correctness of all material claims/proofs | PASS |
| All examples independently verified | PASS |
| Notation/domain consistency | PASS |
| Required files/metadata | PASS |
| Image path and SVG XML integrity (figures) | PASS |
| Actual SVG rendering (Chrome, no error) | PASS |
| Actual SVG visual inspection | NOT_RUN |
| Prose/LaTeX structure | PASS |
| Exact remote persistence | PENDING |

## Disposition

BLOCKED — mandatory visual-inspection gate NOT_RUN. All other mandatory gates PASS.
