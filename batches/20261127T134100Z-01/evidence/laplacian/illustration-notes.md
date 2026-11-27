# Illustration notes — Laplacian

Batch `20261127T134100Z-01`. Article `multivariable-calculus/laplacian.md`.

## Figure 1 — `svg/laplacian-1.svg`

- Claim: A_f(P, r) - f(P) is approximately (r^2/6) Delta f(P) in three dimensions, so a positive gap means a positive Laplacian.
- Anchor: after the sentence interpreting the sign of Delta f(P).
- Construction: a two-dimensional cross-section through P: the graph is a valley with a minimum at P, the sphere S_r(P) is a tinted disk, and the dashed levels f(P) and A_f(P, r) are compared by a vertical bar. The gap is exaggerated for visibility.
- Departure: a cross-section replaces a fully 3D sphere, and only the positive case is drawn; the negative case is the mirror image and is stated in the prose.

## Figure 2 — `svg/laplacian-2.svg`

- Claim: f = x^2 - y^2 is harmonic (Delta f = 0) with a saddle, while g = x^2 + y^2 has Delta g = 4 with a minimum; the two principal curvatures cancel in the first case and add in the second.
- Anchor: after the bulleted examples and the distributional paragraph that follows them.
- Construction: two wireframe surfaces at the same vertical scale, with the x = 0 and y = 0 cross-sections highlighted. Level hyperbolas are drawn on the saddle at z = +0.6 and z = -0.6; level circles are drawn on the bowl at z = 0.8 and z = 1.8.
- Departure: gradient arrows are omitted; the curvature comparison is carried by the highlighted cross-sections and the level curves, and the gradient-level relation is the subject of `vector-fields-2.svg`. The example g = x^2 + y^2 is the two-variable function, so Delta g = 4; the article's separate three-variable example x^2 + y^2 + z^2 has Delta = 6 and is not the function drawn.

## Figure 3 — `svg/laplacian-3.svg`

- Claim: the coordinate boxes in cylindrical and spherical coordinates have edge lengths dr, r d theta, dz and d rho, rho d phi, rho sin phi d theta, which are the metric factors in the Laplacian.
- Anchor: after the sentence on the divergence of the gradient producing the displayed factors.
- Construction: two oblique schematic cells. The cylindrical front face is flat (the r-z plane) and its depth edges are curved (the theta direction). The spherical front face has bowed vertical edges (the phi arcs) and curved depth edges (the theta direction). Each edge is labelled with its length, and a small x-y-z triad fixes the orientation.
- Departure: a single shared axonometric made the thin cells unreadable, so each cell is drawn as an oblique schematic with the three edge lengths encoded directly. The cells are finite but labelled with differentials to indicate the infinitesimal limit; they are not to scale.

## Checks

- XML parsed and structure validated: positive `width`/`height`, matching `viewBox`, unique ids, `aria-labelledby` targets present, `<title>` and `<desc>` present, live `<text>` only, no scripts, event handlers, `foreignObject`, raster images or remote URLs.
- Rendered with headless Chrome at the intrinsic width and at 240 px; both renders inspected visually.
- Geometry computed from the stated equations or from an explicit projection; arrow directions and normals checked against the text.
- Monochrome Algebrica palette (`#312F2F`, `#BEB8B7`, `#636060`, `#E9E3E2`, `#E2DFDD`, `#979797`); no gradients, shadows or decorative colour.
