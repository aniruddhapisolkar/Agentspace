# Illustration notes — Fubini's Theorem

Article: `multivariable-calculus/fubinis-theorem.md`

## fubinis-theorem-1.svg — a slice at fixed $x$

- **Claim:** the volume under $z=f(x,y)$ over $R$ is $\int_a^b A(x)\,dx$, where $A(x)=\int_c^d f(x,y)\,dy$.
- **Anchor:** after the display of equation (1).
- **Construction:** cabinet view; surface $f=1.35-0.35((x-0.9)^2+(y-0.7)^2)$ over $[0,1.8]\times[0,1.4]$; the solid is cut open at $x_0=0.72$, so the retained mesh, the two rims and the cut curve are all the actual surface; the cross-section under the cut curve is shaded, with dashed verticals at its ends and the label $A(x)$.
- **Departure:** the brief's full surface with a translucent cutting plane was replaced by a cutaway. With an opaque slice the front half of the surface would either hide the slice or be hidden by it, and the intersection is clearer when the solid is opened at the plane. The cut is at $x=x_0$, which is exactly the slice the formula integrates.
- **Checks:** the cut curve is sampled from $f$ at $x_0$; the shaded area sits between that curve and the base segment; the $y$-axis was dropped after it crossed the cut face, and $c$/$d$ on the base still identify the $y$ interval.

## fubinis-theorem-2.svg — inner and outer limits

- **Claim:** for a type I region the inner integral runs from $\varphi_1(x)$ to $\varphi_2(x)$ and the outer integral from $a$ to $b$.
- **Anchor:** after "For a type II region the inner integral is in $x$ and the outer limits are functions of $y$."
- **Construction:** equal scale 74 px per unit; one lens-shaped region; a single representative vertical segment at $x=1.58$ with arrowheads at both boundary points, labelled $\varphi_1(x)$, $\varphi_2(x)$; the word "inner" beside the segment and an "outer integral" bracket under the $x$-axis from $a$ to $b$.
- **Departure:** the brief's second boundary labels sit directly on the segment ends; the words "inner"/"outer" were added because the point of the figure is which limit belongs to which integral.
- **Checks:** the segment endpoints are on both boundary curves; the bracket spans exactly $[a,b]$.

## fubinis-theorem-3.svg — reversing the order over a parabolic region

- **Claim:** $D=\{0\le x\le1,\ x^2\le y\le1\}=\{0\le y\le1,\ 0\le x\le\sqrt y\}$.
- **Anchor:** after the display defining $D$, before "Integrating first in $y$ is not feasible".
- **Construction:** equal scale 180 px; region sampled between $y=1$ and $y=x^2$; horizontal strip at $y=0.62$ from $x=0$ (open dot) to $x=\sqrt{0.62}$ with an arrow; parabola label rotated along the curve.
- **Checks:** strip length equals $\sqrt y$ to the pixel; strip labels clear of the arrowhead.

## Checks

- XML parsed; width/height match the viewBox; every `aria-labelledby` target exists; all IDs unique; no scripts, external references, embedded rasters or non-finite geometry; live `<text>` throughout.
- Rendered in headless Chrome at 2× intrinsic size and again at 240 px width; each render was inspected for clipping, overlap, legibility and agreement with the article's equations.
- Palette: the skill's canonical monochrome (`#312F2F`, `#BEB8B7`, `#636060`, `#E9E3E2`, `#E2DFDD`, `#979797`). The briefs' "one accent colour" line predates that palette; the accent is carried by weight and tone instead of hue.
- 3D figures use one shared cabinet axonometric (`u = x + 0.55y`, `v = z + 0.30y`, x right, y receding up-right, z up). The briefs' "x lower right, y lower left" was not used because it puts the origin at the back-top corner and hides the first octant; the cabinet view keeps the labelled faces visible. This is recorded per figure below where it matters.
