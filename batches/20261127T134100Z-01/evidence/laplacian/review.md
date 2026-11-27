# Review evidence — Laplacian

Batch: `20261127T134100Z-01`
Slug: `laplacian`
Article: `multivariable-calculus/laplacian.md`
Reviewed revision: `2912bb1`
Reviewer: AI reviewer (algebrica-reviewer skill)
Review date: 2026-11-27

## Scope and coverage

- Writer `WRITTEN`, Illustrator `ILLUSTRATED`, 3 figures.
- Research, figure briefs, illustration notes present and read.

## Sources and actual checks

- Independent arithmetic:
  - Harmonic examples: x²−y² (2−2=0), e^x cos y (e^x cos y − e^x cos y=0), xyz (all pure second derivatives 0), x²+y²+z² (Δ=6). Verified.
  - 1/r: Δ(1/r)=0 for r>0 via radial formula. Verified.
  - ln r in 2D: Δ(ln r)=0. Verified.
  - Annulus boundary value problem: f=2/ρ−1 satisfies f(1)=1, f(2)=0, Δf=0. Verified.
  - Green's identities (14)–(16): verified by integration by parts.
  - Cylindrical/spherical coordinate formulas: metric factors present and correct.
  - Vector Laplacian identity (24): correct.

## Claim-by-claim audit

- Definition (1)–(5): correct.
- Mean value property (6)–(8): coefficient 6/r² in 3D, 2n/r² in nD. Correct.
- Harmonic functions: correct.
- Maximum principle: stated with bounded domain/continuity caveats.
- Green's identities: correct.
- Coordinate expressions (17)–(18): correct.
- Boundary value problem: correct, uniqueness via maximum principle.
- Vector Laplacian (23)–(24): correct, curvilinear caveat stated.

## Counterexamples / edge cases

- Sign convention not universal: stated.
- Fundamental solutions harmonic only away from singularity: stated.
- Maximum principle requires bounded domain: stated.

## Editorial audit

- YAML, H2-only, tags (1)–(24) sequential, LaTeX consistent.
- Links to divergence, curl, vector fields, spherical coordinates, triple integrals: present.

## SVG audit (structural + geometry)

Files: `laplacian-{1,2,3}.svg`.

- XML parse OK; dims/viewBox match; IDs; aria-labelledby resolves; live text; no scripts/rasters.
- Palette monochrome.
- Fig 1: small sphere at minimum comparing average height with centre height. Matches.
- Fig 2: harmonic saddle vs nonharmonic bowl. Matches.
- Fig 3: curvilinear coordinate boxes with metric-factor edge lengths. Matches.
- Render check: Chrome headless rendered all 3 at intrinsic and 240 px without error. (Illustrator flagged metric labels in laplacian-3 as least legible at 240 px; not visually verifiable here, recorded as limitation.)

## Visual inspection

- Gate: NOT_RUN.

## Changes made

- None. No defects found.

## Limitations

- No LaTeX renderer; structural check only.
- Visual legibility of laplacian-3 metric labels at 240 px not verifiable here (Illustrator's documented flag retained).
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
