# Illustration notes — Tangent Planes and Linear Approximations

Batch `20261126T193918Z-01`. Illustrator evidence. Article:
`multivariable-calculus/tangent-planes-and-linear-approximations.md`.

All figures are standalone SVG 1.1, UTF-8, live text, house palette, no external
references. Rendered with headless Chrome at intrinsic size (2×) and inside a
240 px-wide page; inspected visually.

## Figure 1 — `svg/tangent-planes-and-linear-approximations-1.svg`

- Claim: at P=(x₀,y₀,f(x₀,y₀)) the tangent plane contains the two coordinate
  tangent lines and (f_x,f_y,−1) is normal to it.
- Anchor: after “The vector $(-f_x,-f_y,1)$ is also normal; the two differ only by
  sign.”
- Construction: graph of f(x,y)=0.25(x²+y²) with f_x=0.6, f_y=0.5 at (1.2,1.0,0.61).
  Surface wireframe (9×8 curves) over [0.2,2.2]×[0,2.0]; tangent plane as the
  parallelogram P±0.7(1,0,f_x)±0.7(0,1,f_y), filled `#E9E3E2`; the two coordinate
  tangent lines in `#312F2F`; the normal drawn along −(f_x,f_y,−1)/‖·‖ so that it
  points out of the surface and remains visible (the article notes both signs are
  normal). Projection: fixed oblique axonometric, x to the lower right, y to the
  lower left, z vertical; 85 px per unit, z scale 1:1.
- Checks: the plane passes through P and contains both tangent lines; f_x and f_y
  label the correct traces; the normal is perpendicular to both traces (checked
  numerically: (0.6,0.5,−1)·(1,0,0.6)=0 and ·(0,1,0.5)=0).
- Limitation: the patch is a wireframe scene and is dense at 240 px; the plane is
  labelled with a leader at its right edge.

## Figure 2 — `svg/tangent-planes-and-linear-approximations-2.svg`

- Claim: for z=√(x²+y²) at (4,4), the error f−L is zero at the point of tangency
  and grows quadratically; at (3.98,4.03) it is about 1.1×10⁻⁴.
- Anchor: after “The approximation is useful because the increments are small
  compared with the distance from the origin, and because the second derivatives
  are bounded near $(4,4)$.”
- Construction: exact error along the displacement direction
  h=(−0.02,0.03), |h|=0.03606: e(s)=√((4+sdx)²+(4+sdy)²)−(4√2+s(dx+dy)/√2),
  sampled 200 times over s∈[−0.062,0.062]; vertical axis in units of 10⁻⁴. Q is
  marked at s=|h| with e=1.11×10⁻⁴.
- Departures: the brief asked for a two-panel figure with a 3D cone and a radial
  cross-section. A radial section of this cone is exactly straight — the tangent
  line coincides with the surface along the ray — so it cannot show the error. The
  figure therefore plots the error along the actual displacement direction, which
  is where the 1.1×10⁻⁴ arises. The 3D panel was dropped because the gap (10⁻⁴ on
  a height of 5.66) cannot be drawn at any honest scale.
- Checks: e(0)=0; e(|h|)=1.11×10⁻⁴ (5.664036−5.663925); curve is tangent to the
  axis at s=0 and locally quadratic.

## Figure 3 — `svg/tangent-planes-and-linear-approximations-3.svg`

- Claim: for F=x²+y²+z² and P=(1,2,3) on F=14, ∇F(P)=(2,4,6) is normal to the
  surface and to the tangent plane x+2y+3z=14.
- Anchor: after “The gradient is normal to the surface.”
- Construction: isometric projection (unit axes at 120°, scale 18 px per unit), so
  the sphere x²+y²+z²=14 projects to a circle of radius 3.742·√1.5·18≈82.5 px. Four
  latitude circles and three meridians in `#BEB8B7`; tangent-plane patch
  P±1.95e₁±1.95e₂ with e₁=(2,−1,0)/√5 and e₂=n×e₁, filled `#E9E3E2`; gradient arrow
  from P along (1,2,3)/√14 of length 5.4; curve γ(t)=R(p cos t+e₁ sin t) on the
  sphere with R=√14; tangent γ′(0) along e₁ at 1.35 units; right-angle mark at P
  between the normal and γ′(0).
- Checks: |P|=√14; n·e₁=0; the plane contains P (1+4+9=14); the right angle is
  drawn in the plane spanned by n and e₁; the sphere remains a circle (not an
  ellipse) under the chosen projection.

## Figure 4 — `svg/tangent-planes-and-linear-approximations-4.svg`

- Claim: f(x,y)=xy/√(x²+y²) is continuous at 0 with both partials zero, but
  f(h,k)/√(h²+k²)=hk/(h²+k²) depends on direction, so no tangent plane exists.
- Anchor: after “Its graph has no tangent plane there, even though both coordinate
  sections are flat.”
- Construction: left, the domain disc with the axes y=0, x=0 and the diagonals
  y=±x; the four sectors carry f>0 / f<0 signs (f=xy/r has the sign of xy). Right,
  the three sections z against r: z=0 along y=0, z=r/2 along y=x, z=−r/2 along
  y=−x, drawn from the origin with the same scale (62 px per r-unit, 88 px per
  z-unit). The different slopes 0, ±1/2 are the directional derivatives.
- Departures: the brief asked for a 3D surface with an inset of level curves. The
  function is homogeneous, so its level sets are rays and a 3D rendering adds no
  information about the failure of differentiability; the domain sectors plus the
  three radial sections state it exactly and read at 240 px.
- Checks: f=0 on both axes; f(±r/√2,±r/√2)=±r/2; the signs in the four sectors
  match xy; the origin is drawn open (the function is defined there but has no
  tangent plane).
