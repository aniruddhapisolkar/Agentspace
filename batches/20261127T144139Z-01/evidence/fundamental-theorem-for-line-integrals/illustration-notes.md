# Illustration notes — Fundamental Theorem for Line Integrals

Batch `20261127T144139Z-01`. Article `multivariable-calculus/fundamental-theorem-for-line-integrals.md`.

## Figure 1 — `svg/fundamental-theorem-for-line-integrals-1.svg`

- Claim: along an oriented curve from A to B the integral of ∇f is f(B) − f(A), independent of the route.
- Anchor: after the sentence comparing the potential to an antiderivative.
- Construction: three local level curves; a Catmull-Rom curve from A to B crossing the middle curve once at P. At P a dashed tangent, a horizontal gradient arrow, the perpendicular dropped from the gradient tip to the tangent (the projection), and right-angle marks at P and at the foot. Equal axis scaling is not required because the figure is explicitly schematic, but directions are computed, not guessed.
- Departure: the tangent was extended past the curve on both sides so that it separates visually from the curve it touches.
- Check: the drawn gradient is perpendicular to the local level curve to within the schematic tolerance; the projection foot lies on the tangent segment.

## Figure 2 — `svg/fundamental-theorem-for-line-integrals-2.svg`

- Claim: splitting a path at P₁, P₂ telescopes to f(B) − f(A).
- Anchor: after "The derivative may fail at the corner, but the integral is unaffected."
- Construction: a three-segment polygonal path P₀ = A → P₁ → P₂ → P₃ = B, with one arrowhead per segment. To its right the three potential differences are stacked in reading order, followed by the two endpoint forms; a thin bracket marks the three rows whose interior values cancel.
- Departure: the brief allowed strike-throughs or paired arrows; a bracket and the note "interior values cancel in pairs" were used instead, because they state the same cancellation without aligning thin strokes to variable-width text.
- Check: each labelled difference matches its segment, and the sum displayed is algebraically the endpoint difference.

## Figure 3 — `svg/fundamental-theorem-for-line-integrals-3.svg`

- Claim: for F = (−y, x) the upper semicircle from (1, 0) to (−1, 0) gives π and the lower one gives −π.
- Anchor: after "The two paths have the same endpoints and different integrals."
- Construction: the unit circle at 88 px radius with equal axis scaling; the upper arc is solid and the lower is dashed; large arrowheads at the top and bottom give the traversal directions. Field arrows at 30°, 60°, 120°, 150°, 210°, 240°, 300°, 330° are tangent and counterclockwise.
- Departure: the lower arc is dashed along its whole length rather than only at its midpoint, which distinguishes the two paths more clearly.
- Check: C₊ is counterclockwise and C₋ clockwise from A to B; the field arrows are counterclockwise on both arcs.

## Checks

- XML parsed and structure validated: positive `width`/`height`, matching `viewBox`, unique ids, `aria-labelledby` targets present, `<title>` and `<desc>` present, live `<text>` only, no scripts, event handlers, `foreignObject`, raster images or remote URLs.
- Rendered with headless Chrome at the intrinsic width and at 240 px; both renders inspected visually. PNG evidence is under `work/render/b8/` outside the repository.
- Geometry computed from the stated equations or from an explicit projection; arrow directions and normals checked against the text.
- Monochrome palette (`#312F2F`, `#BEB8B7`, `#636060`, `#E9E3E2`, `#E2DFDD`, `#979797`); no gradients, shadows or decorative colour.
