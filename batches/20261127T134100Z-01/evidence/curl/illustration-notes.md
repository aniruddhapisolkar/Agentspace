# Illustration notes — Curl

Batch `20261127T134100Z-01`. Article `multivariable-calculus/curl.md`.

## Figure 1 — `svg/curl-1.svg`

- Claim: for a counterclockwise rectangle, the circulation is approximately (Q_x - P_y) dx dy, so the scalar curl is the circulation per unit area.
- Anchor: after the sentence identifying the direction of the curl vector.
- Construction: rectangle with a tinted interior and a dashed shrinking copy. Four counterclockwise arrows are inset from the edges. Field arrows outside show P increasing with y (top longer than bottom) and Q increasing with x (right longer than left).
- Departure: the circulation arrows are inset from the boundary rather than lying on it, so that their shafts are visible against the rectangle's stroke.

## Figure 2 — `svg/curl-2.svg`

- Claim: the rigid rotation (-omega y, omega x, 0) has curl 2 omega k, while the shear (y, 0, 0) has curl -k; both turn a paddlewheel, in opposite senses.
- Anchor: after the shear-field paragraph.
- Construction: left panel, circular arrows of true length increasing with radius, with a four-vane paddlewheel and a counterclockwise rotation arc. Right panel, five horizontal arrows whose length increases upward, the same paddlewheel, and a clockwise rotation arc. A circled dot marks z out of the page.
- Departure: the brief's 3D paddlewheel is drawn as a plan view (axis along z out of the page), which is the view in which the two circulations are compared.

## Figure 3 — `svg/curl-3.svg`

- Claim: the flux of curl F through any oriented surface spanning C equals the circulation around C, with the orientation induced by the right-hand rule.
- Anchor: after the sentence on the surface integral depending only on the boundary.
- Construction: a perspective ellipse for C, a flat disk S1 and a dome S2 sharing the same boundary. The dome is shown as a cutaway crescent so S1 remains visible. Both normals point upward; the boundary arrows on the front half move to the right, consistent with the upward normal.
- Departure: the cap is drawn as a cutaway rather than an opaque dome, so that the flat disk with the same boundary can be seen in one figure.

## Checks

- XML parsed and structure validated: positive `width`/`height`, matching `viewBox`, unique ids, `aria-labelledby` targets present, `<title>` and `<desc>` present, live `<text>` only, no scripts, event handlers, `foreignObject`, raster images or remote URLs.
- Rendered with headless Chrome at the intrinsic width and at 240 px; both renders inspected visually.
- Geometry computed from the stated equations or from an explicit projection; arrow directions and normals checked against the text.
- Monochrome Algebrica palette (`#312F2F`, `#BEB8B7`, `#636060`, `#E9E3E2`, `#E2DFDD`, `#979797`); no gradients, shadows or decorative colour.
