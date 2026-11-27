# Illustration notes — Conservative Vector Fields

Batch `20261127T144139Z-01`. Article `multivariable-calculus/conservative-vector-fields.md`.

## Figure 1 — `svg/conservative-vector-fields-1.svg`

- Claim: for f = x² + 2y² the level curves are ellipses, ∇f = (2x, 4y) is normal to them, and the arrows lengthen as the level curves crowd together.
- Anchor: after the topographic-map sentence at the end of "Potentials are unique up to a constant".
- Construction: ellipses x² + 2y² = c for c = 1, 2, 3, 4 at 44 px per unit with equal axis scaling, so perpendicularity is visible. Eight gradient arrows on c = 2 (one of them at P, at θ = 65°) and four on c = 4; every arrow is drawn at 7 px per unit of |∇f|, so the c = 4 arrows are longer. A dashed tangent at P, a right-angle mark against the level curve, and a second right angle at the projected gradient are included.
- Departure: P replaces one of the eight sample arrows instead of duplicating it, and the four ellipse labels were replaced by one note, "f = 1, 2, 3, 4 outward", because per-curve labels collided with the arrows.
- Check: the gradient is orthogonal to the tangent at P by construction (dot product zero), and the arrow length at c = 4 exceeds that at c = 2.

## Figure 2 — `svg/conservative-vector-fields-2.svg`

- Claim: two paths from A on f = c₁ to B on f = c₃ cross f = c₂ once each and give the same integral.
- Anchor: after the sentence on piecewise smooth curves and cancelling intermediate values.
- Construction: three local contour arcs x = c + 5 sin((y − 30)/45) for c = 76, 160, 244 px; A and B on the outer two curves; each path is a Catmull-Rom curve sampled and stroked, with an arrowhead at 87–89% of its length. Both cross the middle contour once.
- Departure: the contours are near-parallel local arcs rather than closed nested ovals, which makes the single crossing of each path explicit.
- Check: path counts against the middle contour were checked visually; neither path recrosses it.

## Figure 3 — `svg/conservative-vector-fields-3.svg`

- Claim: F = (−y, x)/(x² + y²) has zero scalar curl on the punctured plane but circulation 2π on the unit circle.
- Anchor: after "The integral around a closed curve is nonzero...".
- Construction: equal axis scaling, unit circle r = 60 px and a second circle r = 110 px. Field arrows are tangent, counterclockwise, length proportional to 1/r (18 px and 10 px). The origin is an open circle with a leader to "O"; a heavier arrowhead at 22° marks the orientation of C.
- Departure: no grey annulus fill, because the domain is the whole punctured plane and a filled annulus would suggest otherwise.
- Check: the tangent direction at each sample lies along (−sin θ, cos θ); the circulation sign is counterclockwise.

## Checks

- XML parsed and structure validated: positive `width`/`height`, matching `viewBox`, unique ids, `aria-labelledby` targets present, `<title>` and `<desc>` present, live `<text>` only, no scripts, event handlers, `foreignObject`, raster images or remote URLs.
- Rendered with headless Chrome at the intrinsic width and at 240 px; both renders inspected visually. PNG evidence is under `work/render/b8/` outside the repository.
- Geometry computed from the stated equations or from an explicit projection; arrow directions and normals checked against the text.
- Monochrome palette (`#312F2F`, `#BEB8B7`, `#636060`, `#E9E3E2`, `#E2DFDD`, `#979797`); no gradients, shadows or decorative colour.
