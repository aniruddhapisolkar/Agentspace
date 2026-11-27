# Review evidence — Curl

Batch: `20261127T134100Z-01`
Slug: `curl`
Article: `multivariable-calculus/curl.md`
Reviewed revision: `2912bb1`
Reviewer: AI reviewer (algebrica-reviewer skill)
Review date: 2026-11-27

## Scope and coverage

- Writer `WRITTEN`, Illustrator `ILLUSTRATED`, 3 figures.
- Research, figure briefs, illustration notes present and read.

## Sources and actual checks

- Independent arithmetic:
  - Rigid rotation (6): curl = ⟨0,0,2ω⟩. Verified.
  - Shear (9): curl = ⟨0,0,−1⟩. Verified.
  - Stokes example: curl F=⟨1,1,1⟩ for F=⟨z,x,y⟩; flux over unit disk = π; boundary integral ∫₀²π cos²t dt = π. Verified.
  - Worked example F=⟨x²y, yz, x+z²⟩: curl = ⟨−y, −1, −x²⟩; at (1,2,3) = ⟨−2,−1,−1⟩. Verified.
  - Planar G=⟨x²+y, xy⟩: scalar curl = y−1; at (2,3)=2. Verified.
  - Punctured-plane field (12): curl=0; unit-circle circulation 2π. Verified.
  - Cylindrical formula check on rigid rotation: z-component (1/r)∂(r·rω)/∂r = 2ω. Verified.

## Claim-by-claim audit

- Definition (1)–(2): determinant mnemonic explained; expansion correct.
- Planar curl (3): correct.
- Circulation density (4)–(5): correct.
- Rigid rotation/shear (6)–(10): correct.
- Gradient has zero curl (11): correct.
- Converse requires simple connectedness: stated.
- Stokes' theorem (14): hypotheses stated; orientation via right-hand rule.
- Green's theorem as flat case (15): correct.
- Curvilinear formulas (16)–(17): metric factors present and correct.
- Product rules (18)–(19): correct.
- Identity (20): correct.

## Counterexamples / edge cases

- Parallel arrows ≠ zero curl (shear): stated.
- Circular arrows ≠ nonzero curl: stated.
- Domain topology obstruction: stated.

## Editorial audit

- YAML, H2-only, tags (1)–(20) sequential, LaTeX consistent.
- Links to vector fields, divergence, Laplacian, line integrals: present.

## SVG audit (structural + geometry)

Files: `curl-{1,2,3}.svg`.

- XML parse OK; dims/viewBox match; IDs; aria-labelledby resolves; live text; no scripts/rasters.
- Palette monochrome.
- Fig 1: small counterclockwise rectangle with field arrows on four edges. Matches.
- Fig 2: paddlewheel in circular and shear flow. Matches.
- Fig 3: closed curve bounding flat disk and curved cap with consistent normals. Matches.
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
