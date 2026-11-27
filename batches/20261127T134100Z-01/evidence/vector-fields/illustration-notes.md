# Illustration notes — Vector Fields

Batch `20261127T134100Z-01`. Article `multivariable-calculus/vector-fields.md`.

## Figure 1 — `svg/vector-fields-1.svg`

- Claim: F_rad = (x, y) points away from O along rays, while F_rot = (-y, x) is perpendicular to the position vector and circulates counterclockwise; both have length proportional to distance.
- Anchor: after the sentence on counterclockwise circulation and linear growth.
- Construction: two square panels on the same data scale (26 px per unit) and the same arrow scale (7.4 px per unit of field). Grid of 5 x 5 sample points excluding O. Faint rays on the left and concentric circles on the right carry the guide geometry.
- Departure: the brief asked for one colour per field; the monochrome palette uses the same ink for both, with guide geometry in the muted grey.

## Figure 2 — `svg/vector-fields-2.svg`

- Claim: for f = x^2 + 2y^2, grad f = (2x, 4y) is orthogonal to the level ellipses and grows where the ellipses are closer.
- Anchor: after the topographic-map sentence.
- Construction: level ellipses c = 1, 2, 3, 4 at equal x/y scale. The band between c = 3 and c = 4 is tinted, the others are white. Gradient arrows are drawn at generic points on c = 2 and c = 3, not on the axes. A dashed tangent and a right-angle mark at one point on c = 2 show that the tangential component of the gradient is zero.
- Departure: the brief asked for a light tint between successive curves; only the outer band is tinted so that the labels and arrows stay legible.

## Figure 3 — `svg/vector-fields-3.svg`

- Claim: F = (-y, x)/(x^2 + y^2) has zero curl on the punctured plane but circulation 2 pi around the unit circle.
- Anchor: after the paragraph explaining that the hole prevents contraction.
- Construction: the annulus between r = 1 and r = 2 is tinted, the disk inside C is white, and the origin is a small open circle marked as excluded. Arrows on both circles are tangent and counterclockwise with length proportional to 1/r (26 px at r = 1, 13 px at r = 2). The unit circle C is a strong stroke; the outer reference circle is dashed.

## Checks

- XML parsed and structure validated: positive `width`/`height`, matching `viewBox`, unique ids, `aria-labelledby` targets present, `<title>` and `<desc>` present, live `<text>` only, no scripts, event handlers, `foreignObject`, raster images or remote URLs.
- Rendered with headless Chrome at the intrinsic width and at 240 px; both renders inspected visually.
- Geometry computed from the stated equations or from an explicit projection; arrow directions and normals checked against the text.
- Monochrome Algebrica palette (`#312F2F`, `#BEB8B7`, `#636060`, `#E9E3E2`, `#E2DFDD`, `#979797`); no gradients, shadows or decorative colour.
