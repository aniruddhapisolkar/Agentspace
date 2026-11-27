# Illustration notes — Flux Integrals

Batch `20261127T144139Z-01`. Article `multivariable-calculus/flux-integrals.md`.

## Figure 1 — `svg/flux-integrals-1.svg`

- Claim: in time Δt the fluid crossing a patch fills a slanted prism of volume (v · n) ΔS Δt, so only the normal component contributes.
- Anchor: after "Reversing n reverses the sign of every contribution and therefore of the total."
- Construction: a patch spanned by a = (0.55, 0, 0.12) and b = (0, 0.55, 0.10) at p₀, extruded along w = v Δt; four side faces in two light tones, top and base white. The normal is the computed a × b, the velocity is w, and a dashed perpendicular is dropped from the v tip to the n line to show the projection. The angle θ is drawn at the base centre.
- Departure: the prism is tall relative to the patch so the construction is visible; the brief's schematic scale is preserved.
- Check: n ⟂ a and n ⟂ b; v · n > 0 in the drawing, matching the text.

## Figure 2 — `svg/flux-integrals-2.svg`

- Claim: the inverse-square field has flux 4π through every sphere centred at the origin and zero through a closed surface that does not enclose it.
- Anchor: after "The contrast between 4π and 0 is entirely a question of what the surface encloses."
- Construction: two concentric spheres R₁ = 44 px and R₂ = 82 px, each a circle with an equator ellipse (front solid, back dashed), eight short radial arrows outside the outer sphere, outward normals at 45° on both, a dashed radius at 160° carrying R₁ and R₂, and a separate closed blob with Φ = 0.
- Departure: the field arrows are drawn only outside the outer sphere to keep the annulus legible; both flux labels are placed one above the outer sphere and one inside the inner sphere.
- Check: both spheres are centred on O, so both enclose the source; the separate surface does not.

## Figure 3 — `svg/flux-integrals-3.svg`

- Claim: div F(P) is the limit of net outward flux per unit volume, with more leaving than entering when the divergence is positive.
- Anchor: after the sentence on positive, negative and zero divergence.
- Construction: a unit box in a cabinet axonometric with the top face tinted and three hidden edges dashed. Arrows enter through the left and bottom faces and leave through the right and top, with the outgoing arrows longer; outward normals are drawn on the left and top faces; P is at the centre. The limit is written with V → 0.
- Departure: the top and bottom arrows are not labelled, to keep the two principal labels F_in and F_out legible.
- Check: both normals point away from the solid; F_out is longer than F_in.

## Checks

- XML parsed and structure validated: positive `width`/`height`, matching `viewBox`, unique ids, `aria-labelledby` targets present, `<title>` and `<desc>` present, live `<text>` only, no scripts, event handlers, `foreignObject`, raster images or remote URLs.
- Rendered with headless Chrome at the intrinsic width and at 240 px; both renders inspected visually. PNG evidence is under `work/render/b8/` outside the repository.
- Geometry computed from the stated equations or from an explicit projection; arrow directions and normals checked against the text.
- Monochrome palette (`#312F2F`, `#BEB8B7`, `#636060`, `#E9E3E2`, `#E2DFDD`, `#979797`); no gradients, shadows or decorative colour.
