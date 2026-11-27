# Review evidence — Vector-Valued Functions

Batch: `20261127T134100Z-01`
Slug: `vector-valued-functions`
Article: `multivariable-calculus/vector-valued-functions.md`
Reviewed revision: `2912bb1`
Reviewer: AI reviewer (algebrica-reviewer skill)
Review date: 2026-11-27

## Scope and coverage

- Writer status `WRITTEN`, Illustrator status `ILLUSTRATED`, 3 figures.
- Research evidence, figure briefs, illustration notes all present and read.
- No upstream duplicate: upstream has no vector-valued-functions article; `arc-length-of-a-curve.md` is a prerequisite, not a duplicate (verified via research.md coverage check).

## Sources and actual checks

- OpenStax Calculus Volume 3 §3.1–3.2 (full text read by Writer; claims verified here against the article).
- Paul's Online Math Notes, "Vector Functions" (independent confirmation).
- Upstream Algebrica `vectors.md`, `arc-length-of-a-curve.md` (notation/links).
- Independent numeric checks (pure Python, no SymPy/NumPy available):
  - Helix a=2, b=1: one-turn length 2π√5 = 14.049629462081453 (exact match).
  - Curvature at t=0.7: cross-product quotient 0.3999999999999999 vs exact 0.4.
  - Component integral: π²/8 = 1.2337005501361697; e^(π/2)-1 = 3.8104773809653514.
  - Circular helix a=b=1: tangential acceleration 0.0, ‖a‖=1.0.
- Tangent-line substitution and cusp one-sided unit-tangent limits checked by hand.

## Claim-by-claim audit

- Componentwise limit/continuity: equivalence via squared norm sum; correct.
- Componentwise derivative (4): correct.
- Tangent line (5): correct given r'(t₀)≠0.
- Product rules (7)–(8): correct; order preserved in cross product.
- Chain rule (9): correct.
- Constant distance/speed distinction: correctly separated; circle example correct.
- Arc length (11) and arc-length function (12): correct, C¹ assumption stated.
- Helix length: correct.
- Curvature formula (15) and helix curvature a/(a²+b²): verified; b=0 gives 1/a.
- Componentwise integral (16)–(17): correct.
- Acceleration decomposition (18): a_T, a_N formulas correct; a_N=κv².
- Circular helix check: κ=1/2, v²=2, a_N=1=‖a‖. Correct.
- Cusp example: differentiable everywhere, no tangent at origin. Correct.

## Counterexamples / edge cases

- Nonvanishing derivative condition for tangent line: stated.
- Arc length requires C¹; merely continuous may be non-rectifiable: stated.
- Retracing counts twice: stated.
- Curvature nonnegative and orientation-independent: stated.

## Editorial audit

- YAML title/source/license/tags: present; source is proposed canonical route.
- H2-only body headings: yes.
- Inline `$...$`, displays `$$...$$`: consistent.
- Tags (1)–(18): unique, sequential, referenced.
- British spelling ("centre", "orthogonal", "nonnegative"): consistent.
- Links to sibling batch articles (line-integrals, vector-fields, divergence, curl) are unpublished dependencies; noted in research limitations. No fabricated live URLs.
- Prose style: calm, impersonal, "reduce without distorting" preserved. No hype/filler detected.

## SVG audit (structural + geometry)

Files: `vector-valued-functions-{1,2,3}.svg`.

- XML: all parse (xmllint OK). Positive width/height/viewBox; viewBox matches dimensions.
- IDs: `fig-title`, `fig-desc` unique per file; aria-labelledby resolves (space-separated list).
- Live `<text>` only; no scripts, event handlers, foreignObject, raster, remote URLs.
- `<title>`/`<desc>` present.
- Palette: #312F2F, #BEB8B7, #636060, #E9E3E2 region etc. Monochrome; no gradients/shadows.
- Figure 1 geometry spot check: projection circle dashed in z=0 plane, two turns, pitch bar 2πb, point (a,0,0) labelled; matches brief and article. Cabinet axonometric.
- Figure 2: concave arc, P, two secants, tangent arrow along increasing t; matches brief.
- Figure 3: helix turn + unrolled right triangle with legs 2πa, 2πb, hypotenuse L, angle α with tan α=b/a; matches brief.
- Render check: Chrome headless rendered all 3 at intrinsic size and 240 px without error (PNGs saved under /tmp/scratchpad/render/b7/).

## Visual inspection

- Gate: NOT_RUN. No image-capable tool available in this environment (model does not accept image input; no rsvg/inkscape). Chrome renders succeeded but pixels were not visually inspected. Per skill, this gate is mandatory when figures exist and cannot be passed without actual visual inspection.

## Changes made

- None. No mathematical, editorial or SVG structural defect found. No article or figure changed.

## Limitations

- No LaTeX renderer available (pandoc/pdflatex not found); Markdown/LaTeX checked structurally only.
- GitHub's own SVG rendering, live site routes, upstream issue/PR intentions not checked.
- Proposed route https://algebrica.org/vector-valued-functions/ not known to be live.

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
| Exact remote persistence | PENDING (to be verified after commit) |

## Disposition

BLOCKED — mandatory visual-inspection gate NOT_RUN. All other mandatory gates PASS; no defects found. Requires visual inspection of the 3 rendered figures at intrinsic size and 240 px in an image-capable environment, then re-run visual gate and upgrade to PASS.
