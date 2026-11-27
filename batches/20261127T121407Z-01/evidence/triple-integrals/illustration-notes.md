# Illustration notes — Triple Integrals

Article: `multivariable-calculus/triple-integrals.md`

## triple-integrals-1.svg — partition of a box

- **Claim:** a partition of $B=[a,b]\times[c,d]\times[e,g]$ into sub-boxes with one sample point each gives $\sum f\,\Delta V_{ijk}$.
- **Anchor:** after the paragraph ending "the limit is the triple integral", before (1).
- **Construction:** cabinet view, 92 px per unit; box $1.6\times1.2\times1.1$; grid lines on the three visible faces only, hidden edges from the far bottom corner dashed; highlighted sub-box at $x\in[2b/3,b]$, $y\in[0,d/2]$, $z\in[g/2,g]$ with the top and right faces shaded and the front face left open so the sample dot reads as interior; dimension marks for $\Delta x_i$, $\Delta y_j$, $\Delta z_k$ on the cell's front, depth and vertical edges.
- **Departure:** $a$, $c$ and $e$ are all the same corner in this convention, so only $a$ is placed there; the full interval is given by the caption $B=[a,b]\times[c,d]\times[e,g]$ rather than by three overlapping corner labels. The brief's full label set is otherwise present ($b,d,g$ at the far ends).
- **Checks:** all 12 edges drawn, the three hidden ones dashed; the sample dot is inside the cell's projected quad; dimension marks parallel to the edges they measure.

## triple-integrals-2.svg — a $z$-simple solid and its shadow

- **Claim:** a $z$-simple solid is the union of vertical segments over $\Omega$ from $z=\varphi_1(x,y)$ to $z=\varphi_2(x,y)$.
- **Anchor:** after "where $\Omega$ is a plane region and $\varphi_1,\varphi_2$ are continuous on $\Omega$."
- **Construction:** cabinet view; $\Omega$ a disc of radius 1, drawn hatched at $z=0$; upper and lower surfaces taken as surfaces of revolution, $\varphi_2=2.05-0.38r^2$ and $\varphi_1=0.55+0.30r^2$, so the same functions are used for the rims, the wireframe and the representative segment; a vertical segment at $(0.52,-0.38)$ with endpoint dots, dashed drop to the shadow point, and labels $\varphi_1(x,y)$, $\varphi_2(x,y)$.
- **Departure:** the brief shows generic smooth sheets; surfaces of revolution are used so every drawn rim and wireframe curve is the actual graph of the stated $\varphi_i$, not decoration. The $z$-axis pierces the solid because the ball is centred at the origin; it is drawn thin and muted.
- **Checks:** the segment's length is $\varphi_2-\varphi_1$ at its own $(x,y)$; rims close; the shadow point is the vertical projection of the segment's foot.

## triple-integrals-3.svg — the standard tetrahedron

- **Claim:** $T=\{x,y,z\ge0,\ x+y+z\le1\}$ is $z$-simple over $\Omega=\{x,y\ge0,\ x+y\le1\}$ with $0\le z\le1-x-y$.
- **Anchor:** after "This is the standard tetrahedron with vertices $(0,0,0)$, $(1,0,0)$, $(0,1,0)$ and $(0,0,1)$."
- **Construction:** isometric octant view with the viewer at $(1,1,1)$: the silhouette is the slanted face $ABC$, and the interior edges $OA$, $OB$, $OC$ are drawn through it in the transparent-solid convention. A dashed slice at $z=0.6$ has vertices $(0.8,0,0.6)$, $(0,0.8,0.6)$, $(0,0,0.6)$ on the three edges, with the axis dot at $(0,0,0.6)$. $\Omega$ is labelled in the base wedge with $x+y\le1$.
- **Departure:** from $(1,1,1)$ only the slanted face is outward-facing, so the tetrahedron is drawn as a transparent wireframe; hatching the base separately would suggest a shadow that is not there. The base is labelled as the region $\Omega$ instead. This is the standard textbook convention for this solid.
- **Checks:** every slice vertex lies on the correct edge by construction ($f=1-z/1.4$); labels avoid the slice.

## Checks

- XML parsed; width/height match the viewBox; every `aria-labelledby` target exists; all IDs unique; no scripts, external references, embedded rasters or non-finite geometry; live `<text>` throughout.
- Rendered in headless Chrome at 2× intrinsic size and again at 240 px width; each render was inspected for clipping, overlap, legibility and agreement with the article's equations.
- Palette: the skill's canonical monochrome (`#312F2F`, `#BEB8B7`, `#636060`, `#E9E3E2`, `#E2DFDD`, `#979797`). The briefs' "one accent colour" line predates that palette; the accent is carried by weight and tone instead of hue.
- 3D figures use one shared cabinet axonometric (`u = x + 0.55y`, `v = z + 0.30y`, x right, y receding up-right, z up). The briefs' "x lower right, y lower left" was not used because it puts the origin at the back-top corner and hides the first octant; the cabinet view keeps the labelled faces visible. This is recorded per figure below where it matters.
