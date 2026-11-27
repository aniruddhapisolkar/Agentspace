# Illustration notes — Divergence

Batch `20261127T134100Z-01`. Article `multivariable-calculus/divergence.md`.

## Figure 1 — `svg/divergence-1.svg`

- Claim: the net outward flux through the six faces of a box of sides dx, dy, dz is approximately (P_x + Q_y + R_z) dx dy dz.
- Anchor: after the coordinate-free definition (5).
- Construction: cabinet axonometric box centred at P. Both x-faces are tinted so the two flux faces can be compared; all twelve edges are drawn, so the box reads as transparent. Outward normals sit on the upper part of each x-face; field arrows sit lower, one entering the left face and a longer one leaving the right face. Side lengths are bracketed outside the box.
- Departure: a solid opaque box would hide one of the two x-faces, so the box is drawn as a transparent frame with tinted faces. The normals and the field arrows are at different heights to keep both readable.

## Figure 2 — `svg/divergence-2.svg`

- Claim: positive divergence gives net outward flow, negative divergence net inward flow, and zero divergence a balance of inflow and outflow.
- Anchor: after the paragraph on the sign of the divergence.
- Construction: three equal control volumes with exactly six arrows each, and the same arrow length. Source and sink arrows are radial; the zero-divergence panel uses parallel through-flow arrows.
- Departure: none of substance.

## Figure 3 — `svg/divergence-3.svg`

- Claim: in a partition of E into boxes, interior faces cancel because their outward normals are opposite; only boundary faces survive.
- Anchor: after the partition argument in the divergence theorem proof.
- Construction: a smooth blob E with a shaded boundary band S and a coarse rectangular grid clipped to E. One interior grid edge is highlighted and enlarged in a callout showing two adjacent cells with normals n and -n on the shared face.
- Departure: the grid is a planar schematic rather than a perspective 3D partition, because the cancellation is a statement about a shared face and its two opposite normals. The callout carries the 3D information.

## Checks

- XML parsed and structure validated: positive `width`/`height`, matching `viewBox`, unique ids, `aria-labelledby` targets present, `<title>` and `<desc>` present, live `<text>` only, no scripts, event handlers, `foreignObject`, raster images or remote URLs.
- Rendered with headless Chrome at the intrinsic width and at 240 px; both renders inspected visually.
- Geometry computed from the stated equations or from an explicit projection; arrow directions and normals checked against the text.
- Monochrome Algebrica palette (`#312F2F`, `#BEB8B7`, `#636060`, `#E9E3E2`, `#E2DFDD`, `#979797`); no gradients, shadows or decorative colour.
