# Illustration notes — Parametric Surfaces

Batch `20261127T144139Z-01`. Article `multivariable-calculus/parametric-surfaces.md`.

## Figure 1 — `svg/parametric-surfaces-1.svg`

- Claim: a small Δu by Δv rectangle maps to the parallelogram spanned by r_u Δu and r_v Δv, whose area is ||r_u × r_v|| Δu Δv.
- Anchor: after the two-dimensional linearization sentence in "Surface area".
- Construction: left panel, the uv-plane with a rectangle at (u₀, v₀) = (0.3, 0.2), Δu = 0.4, Δv = 0.2 and dimension lines. Right panel, the patch r(u, v) = (u, v, 0.3u + 0.15v − 0.25u²) on [−0.7, 0.7]² in a cabinet axonometric, with a 4 by 4 grid and the tangent parallelogram at (0, 0) with Δ = 0.5. The normal is the computed cross product, not a screen-vertical arrow.
- Departure: the two corner labels were moved to a single note under the panels, because the full second label did not fit beside the left panel; the parameter-corner identities are preserved by the filled base dot and the open far corner.
- Check: the parallelogram edges are the drawn r_uΔu and r_vΔv vectors; the normal is orthogonal to both by construction.

## Figure 2 — `svg/parametric-surfaces-2.svg`

- Claim: the standard sphere parameterization has a coordinate grid that degenerates at both poles.
- Anchor: after "At the poles, sin φ = 0 and the cross product vanishes."
- Construction: an isometric view with the viewer along (1, 1, 1); the sphere projects to a circle of radius 1.2247 s. Meridians at θ = 0, 90, 180, 270° and parallels at φ = π/6 … 5π/6. Each sampled curve is split by the visibility test x + y + z > 0: visible parts solid, hidden parts dashed. The polar angle φ is drawn at the origin between the +z radius and the radius at φ = π/6; θ is marked by an arc on the equator.
- Departure: the z-axis is drawn as a dashed vertical through the poles to make the polar reference explicit.
- Check: N and S are the images of (0, 0, ±1); the grid curves meet at both poles, where the tangent vectors vanish.

## Figure 3 — `svg/parametric-surfaces-3.svg`

- Claim: transporting a normal once around a Möbius band returns it as its negative, so the band is nonorientable.
- Anchor: after the sentence on gluing patches with a twist.
- Construction: the standard band r(u, v) = ((1 + 0.45v cos(u/2)) cos u, (1 + 0.45v cos(u/2)) sin u, 0.45v sin(u/2)) on u ∈ [0, 2π], v ∈ [−1, 1], drawn as 30 quads with alternating light tones, one solid and one dashed boundary edge, and a dashed centreline with a direction arrow. The normal at P is computed numerically from r_u × r_v; the chosen sign points upward, and the transported copy is drawn as −n.
- Departure: the normal sign was chosen so that n points up; the opposite choice is equally valid and the figure only asserts that the two differ.
- Check: the two boundary edges are the images of v = ±1, and the normal and its negative are collinear and opposite.

## Checks

- XML parsed and structure validated: positive `width`/`height`, matching `viewBox`, unique ids, `aria-labelledby` targets present, `<title>` and `<desc>` present, live `<text>` only, no scripts, event handlers, `foreignObject`, raster images or remote URLs.
- Rendered with headless Chrome at the intrinsic width and at 240 px; both renders inspected visually. PNG evidence is under `work/render/b8/` outside the repository.
- Geometry computed from the stated equations or from an explicit projection; arrow directions and normals checked against the text.
- Monochrome palette (`#312F2F`, `#BEB8B7`, `#636060`, `#E9E3E2`, `#E2DFDD`, `#979797`); no gradients, shadows or decorative colour.
