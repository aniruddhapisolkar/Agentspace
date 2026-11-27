# Illustration notes — Vector-Valued Functions

Batch `20261127T134100Z-01`. Article `multivariable-calculus/vector-valued-functions.md`.

## Figure 1 — `svg/vector-valued-functions-1.svg`

- Claim: for r(t) = (a cos t, a sin t, b t), the xy-projection is the circle x^2 + y^2 = a^2 and one turn rises by 2 pi b.
- Anchor: end of the paragraph defining the helix and the pitch, before the discussion of plane curves.
- Construction: cabinet axonometric (x right, y receding up-right, z up), a = 1, b = 0.2, two turns t in [0, 4 pi]. The projection circle is dashed in the plane z = 0 with two vertical drop lines. The pitch bar is placed at t = pi (left side) to avoid the y-axis; it joins the first and second turns at the same angular position.
- Departure: the brief suggested the pitch at t = 0; it was moved to t = pi so the bar and its label do not collide with the y-axis and the point (a, 0, 0).

## Figure 2 — `svg/vector-valued-functions-2.svg`

- Claim: the difference quotient is a secant direction which tends to the tangent r'(t) as h -> 0.
- Anchor: after the tangent-line equation (5), before the unit tangent vector.
- Construction: a concave arc y = 210 - 160((x-70)/200)^2. P at t = 0.35, two secants to points at t = 0.5 and t = 0.7, the tangent line at P, and an increasing-t arrow near the left end. The tangent arrow points along increasing t.
- Departure: no second accent colour; the secants use the comparison grey.

## Figure 3 — `svg/vector-valued-functions-3.svg`

- Claim: one turn of the helix has length 2 pi sqrt(a^2 + b^2), the hypotenuse of a right triangle with legs 2 pi a and 2 pi b.
- Anchor: after the sentence introducing the unrolled turn.
- Construction: left panel, one turn of the same helix with its projection circle; right panel, the unrolled turn drawn as the hypotenuse of a right triangle. The triangle's leg ratio is b/a = 0.4, matching the drawn helix's pitch, and the angle alpha satisfies tan alpha = b/a. A dashed curved arrow connects the helix to the start of the hypotenuse.
- Departure: the scale of the triangle is not the same as the helix's, but the b/a ratio is; this is stated as schematic in the caption prose.

## Checks

- XML parsed and structure validated: positive `width`/`height`, matching `viewBox`, unique ids, `aria-labelledby` targets present, `<title>` and `<desc>` present, live `<text>` only, no scripts, event handlers, `foreignObject`, raster images or remote URLs.
- Rendered with headless Chrome at the intrinsic width and at 240 px; both renders inspected visually.
- Geometry computed from the stated equations or from an explicit projection; arrow directions and normals checked against the text.
- Monochrome Algebrica palette (`#312F2F`, `#BEB8B7`, `#636060`, `#E9E3E2`, `#E2DFDD`, `#979797`); no gradients, shadows or decorative colour.
