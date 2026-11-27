# Review evidence — Line Integrals

Batch: `20261127T134100Z-01`
Slug: `line-integrals`
Article: `multivariable-calculus/line-integrals.md`
Reviewed revision: `2912bb1`
Reviewer: AI reviewer (algebrica-reviewer skill)
Review date: 2026-11-27

## Scope and coverage

- Writer `WRITTEN`, Illustrator `ILLUSTRATED`, 3 figures.
- Research, figure briefs, illustration notes present and read.

## Sources and actual checks

- Independent arithmetic:
  - Circle example (6): ∫₀²π cos²t dt = π. Verified.
  - Semicircular wire centre of mass: ȳ = 2R/π. Verified.
  - Path-dependent example (14): ∫₀¹ (t²+2t⁴) dt = 1/3+2/5 = 11/15. Verified.
  - Straight segment (15): ∫₀¹ 2t² dt = 2/3. Verified.
  - Potential example: f=x²y+y³, f(1,1)−f(0,0)=2. Verified.
  - Helical work (20): ∫₀²π (1+t) dt = 2π+2π². Verified.
  - Finding potential for F=⟨2xy,x²+3y²⟩ → f=x²y+y³+C. Verified.

## Claim-by-claim audit

- Scalar line integral definition (2)–(4): correct, orientation-independent.
- Vector line integral (10)–(13): correct, orientation-dependent; relation via unit tangent.
- FTC for line integrals (16): correct, chain rule proof.
- Equivalence of conservative/path-independent/zero circulation: correct.
- Finding potential procedure: correct.
- Green's theorem circulation form (19): correct.
- Piecewise/reparameterization (22)–(23): correct.

## Counterexamples / edge cases

- Punctured-plane field: zero curl but circulation 2π. Stated.
- Non-one-to-one parameterization counts twice: stated.
- ds vs dx/dy distinction: stated.

## Editorial audit

- YAML, H2-only, tags (1)–(23) sequential, LaTeX consistent.
- Table comparing scalar/vector integrals: well-formed.
- Links to arc-length, vector fields, divergence, curl, double integrals: present.

## SVG audit (structural + geometry)

Files: `line-integrals-{1,2,3}.svg`.

- XML parse OK; dims/viewBox match; IDs; aria-labelledby resolves; live text; no scripts/rasters.
- Palette monochrome.
- Fig 1: field vector resolved into tangential component weighted by arc length plus normal component. Matches.
- Fig 2: parabola and straight segment between same points with different integrals. Matches.
- Fig 3: two paths between level curves of a potential with gradient arrows. Matches.
- Render check: Chrome headless rendered all 3 at intrinsic and 240 px without error.

## Visual inspection

- Gate: NOT_RUN.

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
