# Illustration notes — Surface Integrals

Batch `20261127T144139Z-01`. Article `multivariable-calculus/surface-integrals.md`.

## Figure 1 — `svg/surface-integrals-1.svg`

- Claim: the scalar surface integral is the limit of Σ f(P_ij) ΔS_ij over a partition into surface patches.
- Anchor: after the definition paragraph ending "leaves a scalar surface integral unchanged" (the brief's suggested anchor, the additivity sentence, is three paragraphs later and would separate the figure from the partition it illustrates).
- Construction: the curved sheet r(u, v) = (u, v, 0.35u + 0.12u²) on [−0.9, 0.9]² in a cabinet axonometric, divided into a 3 by 3 grid; the centre patch is shaded, with P_ij on it and a dashed leader to ΔS_ij. The sheet is monotone in both parameters so the projected cells stay visible and do not fold.
- Departure: the surface is a curved sheet rather than a dome; a dome folds in this projection and hides the interior patch. No normal is drawn, as the scalar integral is orientation-independent.
- Check: nine patches from four grid curves in each direction; the sample point lies inside the shaded patch.

## Figure 2 — `svg/surface-integrals-2.svg`

- Claim: for a graph z = g(x, y), dS = dx dy / cos γ = √(1 + g_x² + g_y²) dx dy.
- Anchor: after "For a horizontal plane it equals 1; for a steep surface it is large."
- Construction: the plane g = 0.55 + 0.32x + 0.18y over a 0.9 by 0.9 rectangle, the tilted element filled darker than its projection, two dashed vertical connectors, the upward normal (−0.32, −0.18, 1), the angle γ to the vertical, and the formula.
- Departure: none of substance; a linear g makes the surface element exactly planar, which is the case the formula illustrates.
- Check: the normal is proportional to (−g_x, −g_y, 1), and the projected rectangle is the vertical projection of the element.

## Figure 3 — `svg/surface-integrals-3.svg`

- Claim: the vector surface integral counts only F · n, so the sign follows the normal component and a tangent field contributes zero.
- Anchor: after the sentence contrasting the scalar integral of ||F|| with the flux.
- Construction: a gently curved patch r(u, v) = (u, v, 0.3u + 0.08u² + 0.05v), the normal at the centre (dashed), and three arrows of equal length at separate points: along n, against n, and along r_u.
- Departure: the arrows are placed at different points so that they do not overlap; the brief's equal-length condition is preserved.
- Check: the tangent arrow is parallel to r_u at its base point, and the two normal arrows are antiparallel.

## Checks

- XML parsed and structure validated: positive `width`/`height`, matching `viewBox`, unique ids, `aria-labelledby` targets present, `<title>` and `<desc>` present, live `<text>` only, no scripts, event handlers, `foreignObject`, raster images or remote URLs.
- Rendered with headless Chrome at the intrinsic width and at 240 px; both renders inspected visually. PNG evidence is under `work/render/b8/` outside the repository.
- Geometry computed from the stated equations or from an explicit projection; arrow directions and normals checked against the text.
- Monochrome palette (`#312F2F`, `#BEB8B7`, `#636060`, `#E9E3E2`, `#E2DFDD`, `#979797`); no gradients, shadows or decorative colour.
