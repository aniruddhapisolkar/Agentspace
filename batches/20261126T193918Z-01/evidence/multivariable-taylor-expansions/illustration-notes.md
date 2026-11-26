# Illustration notes — Multivariable Taylor Expansions

Batch `20261126T193918Z-01`. Illustrator evidence. Article:
`multivariable-calculus/multivariable-taylor-expansions.md`.

Figures are numbered in the order they occur in the article. Standalone SVG 1.1,
UTF-8, live text, house palette (`#312F2F`, `#BEB8B7`, `#636060`, `#E9E3E2`,
`#979797`), no external references. Rendered with headless Chrome at intrinsic size
(2×) and inside a 240 px-wide page; inspected visually.

## Figure 1 — `svg/multivariable-taylor-expansions-1.svg`

- Claim: the first-order Taylor polynomial is the tangent plane, the second-order
  polynomial matches value, gradient and Hessian, so it follows the curvature.
- Anchor: after “The factor $2$ in the mixed term appears because the two mixed
  derivatives are equal, so the entries $(1,2)$ and $(2,1)$ of the Hessian
  contribute identical terms.”
- Construction: the section t ↦ f(a+th) with a=0, h=(1,1), f(x,y)=e^(x+y). The
  curves are g(t)=e^(√2 t) (dark, 2.2 px), P₂(t)=1+√2t+t² (dashed, `#636060`) and
  P₁(t)=1+√2t (solid `#979797`). Axes: t ∈ [−0.60,0.86] over 276 px, z ∈ [0,3.55]
  over 162 px. The common point at t=0 is marked P; a dashed vertical at t=0.55
  marks the two gaps between the curves.
- Departures: the brief asked for a 3D surface with a tangent plane and a
  paraboloid. This is the exact section along h=(1,1), the same reduction used in
  the article's Lagrange-remainder proof; it shows the matching of value, slope and
  curvature without hidden-surface ambiguity. The 3D objects are represented by
  their traces in this section.
- Checks: all three curves pass through (0,1); P₂ has the same slope as g at 0
  (both √2) and the same curvature (2·1²); P₁ is the tangent line; labels P, P₁,
  P₂, f are unambiguous at 240 px.

## Figure 2 — `svg/multivariable-taylor-expansions-2.svg`

- Claim: f(x,y)=e^(−1/(x²+y²)) for (x,y)≠0 and 0 at the origin has every partial
  derivative zero at 0, so every Taylor polynomial there vanishes, yet f>0 away
  from the origin.
- Anchor: after “Smoothness alone does not imply real analyticity in several
  variables, just as in one variable.”
- Construction: left, the radially symmetric surface over r≤2.2 drawn as rings at
  r=0.55,1.0,1.5,2.05 (z=e^(−1/r²)=0.036,0.368,0.640,0.786) and twelve radial
  generators, over the plane z=0 which is the zero Taylor polynomial; right, the
  section e^(−1/t²) for |t|≤2.45 with the axis z=0 dashed and the point at t=0
  filled (the function is defined there as 0).
- Correction to the brief: the brief described a “bump peaked at the origin above
  z=0”. That is not this function: f(0,0)=0 and f increases with r, so the graph is
  a flat-bottomed crater that rises above the plane z=0, touching it only at the
  origin. The figure shows the correct geometry; the article text is consistent
  with it. Flagged for the Reviewer as a brief defect, not an article defect.
- Checks: all derivatives at 0 vanish, so the tangent plane is z=0 and it is drawn
  as the contact plane; the surface lies above it except at the origin; the section
  hugs the axis near 0.

## Figure 3 — `svg/multivariable-taylor-expansions-3.svg`

- Claim: definiteness of the Hessian determines minimum, maximum or saddle.
- Anchor: after “if $H_f(a)$ is singular, the second-order term is inconclusive and
  higher-order terms decide.”
- Construction: three square panels, equal scale 38 px per unit, level curves of
  x²+y² (rings r=0.28,0.52,0.76), −x²−y² (same rings) and x²−y² (hyperbolas
  x²−y²=±0.12,±0.32,±0.52 with asymptotes y=±x dashed). Arrows on the curves point
  in the direction of increase: outward for the minimum, inward for the maximum;
  for the saddle outward along x and toward the origin along y, matching
  ∇q=(2x,−2y). The origin is filled in each panel.
- Checks: the saddle's asymptotes are y=±x; arrows are consistent with the gradient;
  the three panels share scale and axis positions.
- Note: the figure is a level-set diagram; no 3D inset is used, because at this
  size the curves carry the classification alone.
