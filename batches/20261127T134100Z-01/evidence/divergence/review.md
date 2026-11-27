# Review evidence — Divergence

Batch: `20261127T134100Z-01`
Slug: `divergence`
Article: `multivariable-calculus/divergence.md`
Reviewed revision: `2912bb1`
Reviewer: AI reviewer (algebrica-reviewer skill)
Review date: 2026-11-27

## Scope and coverage

- Writer `WRITTEN`, Illustrator `ILLUSTRATED`, 3 figures.
- Research, figure briefs, illustration notes present and read.

## Sources and actual checks

- Independent arithmetic:
  - Radial field F=⟨x,y,z⟩: div=3. Correct.
  - Rotational F=⟨−y,x,0⟩: div=0. Correct.
  - F=⟨x²,y²,z²⟩: div=2(x+y+z). Correct.
  - Inverse-square field: ∂/∂x(x/r³)=1/r³−3x²/r⁵; summing gives 3/r³−3/r³=0. Verified.
  - Flux through sphere radius R for F=⟨x,y,z⟩: F·n=R, flux=R·4πR²=4πR³; volume integral 3·4πR³/3=4πR³. Verified.
  - Unit radial field div=2/r; flux=4πR²; volume integral ∫₀^R (2/r)4πr² dr = 8π·R²/2 = 4πR². Verified.
  - Product rules (8)–(9): verified by component expansion.
  - Divergence of curl = 0: verified.
  - Cylindrical/spherical formulas: metric factors present and correct.

## Claim-by-claim audit

- Definition (1)–(3): correct.
- Infinitesimal box (4)–(5): correct, C¹ limit.
- Examples: correct.
- Divergence theorem (7): hypotheses (C¹ on open set containing E, piecewise smooth boundary, outward normal) stated.
- Proof for box via FTC: correct.
- Singularity caveat: stated.
- Curvilinear formulas (11)–(12): correct.
- Product rules: correct.
- Planar Green's theorem flux form (13): correct.

## Counterexamples / edge cases

- Singularity inside surface invalidates theorem: inverse-square field. Stated.
- Inward normal reverses sign: stated.
- Metric factors mandatory in curvilinear coords: stated.

## Editorial audit

- YAML, H2-only, tags (1)–(13) sequential, LaTeX consistent.
- Links to curl, Laplacian, vector fields, triple integrals: present.

## SVG audit (structural + geometry)

Files: `divergence-{1,2,3}.svg`.

- XML parse OK; dims/viewBox match; IDs; aria-labelledby resolves; live text; no scripts/rasters.
- Palette monochrome.
- Fig 1: small box with outward normals on x-faces, field arrows entering/leaving. Matches.
- Fig 2: three regions (positive/negative/zero divergence). Matches.
- Fig 3: solid partitioned into boxes, interior face normals cancel. Matches.
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
