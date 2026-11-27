# Illustration notes — Line Integrals

Batch `20261127T134100Z-01`. Article `multivariable-calculus/line-integrals.md`.

## Figure 1 — `svg/line-integrals-1.svg`

- Claim: the vector line integral sums only the tangential component F . T weighted by ds; the normal component contributes nothing.
- Anchor: after the paragraph relating the vector and scalar integrals.
- Construction: an oriented curve with P and a second sample point Q. At P the field F points upward, its projection on the tangent gives F . T, and a dashed perpendicular with a right-angle mark gives the normal component. A short thick arc marks ds.
- Departure: the unit tangent T is drawn as a labelled tangent guide rather than a second arrow, because T and the tangential component are collinear and two overlapping arrows would be ambiguous.

## Figure 2 — `svg/line-integrals-2.svg`

- Claim: for F = (x^2, xy), the parabola y = x^2 from (0,0) to (1,1) gives 11/15, while the straight segment gives 2/3.
- Anchor: after the paragraph noting that the field does different work along the two routes.
- Construction: the parabola and the line share the endpoints; sample field arrows are drawn at x = 0.4, 0.6, 0.8 on the parabola and x = 0.3, 0.5, 0.7 on the line, so no arrow overshoots (1,1). The values are printed below the axes.
- Departure: only the area under the parabola is tinted; the two regions are nested, so tinting both would overprint. The brief's "two colours" becomes ink versus comparison grey.

## Figure 3 — `svg/line-integrals-3.svg`

- Claim: for F = grad f, the integral from A to B equals f(B) - f(A) along either path.
- Anchor: after the sentence on the potential removing path dependence.
- Construction: three level ellipses of a potential, with A on c1 and B on c3. Two paths join them; gradient arrows on c2 cross the level curves at right angles. The level labels are placed just outside their curves.
- Departure: the paths leave the outer level ellipse, which is allowed (a path need not stay between level curves); the endpoints, not the region, are what the theorem fixes.

## Checks

- XML parsed and structure validated: positive `width`/`height`, matching `viewBox`, unique ids, `aria-labelledby` targets present, `<title>` and `<desc>` present, live `<text>` only, no scripts, event handlers, `foreignObject`, raster images or remote URLs.
- Rendered with headless Chrome at the intrinsic width and at 240 px; both renders inspected visually.
- Geometry computed from the stated equations or from an explicit projection; arrow directions and normals checked against the text.
- Monochrome Algebrica palette (`#312F2F`, `#BEB8B7`, `#636060`, `#E9E3E2`, `#E2DFDD`, `#979797`); no gradients, shadows or decorative colour.
