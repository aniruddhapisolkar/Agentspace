# Illustration notes — Cylindrical Coordinates

Article: `multivariable-calculus/cylindrical-coordinates.md`

## cylindrical-coordinates-1.svg — a point in cylindrical coordinates

- **Claim:** $P=(x,y,z)$ is described by the distance $r$ from $Q$ to the origin, the azimuth $\theta$ of $Q$, and the height $z=QP$.
- **Anchor:** after "Equivalently, $r$ is the distance from $P$ to the $z$-axis."
- **Construction:** cabinet view, 88 px per unit; $P=(1.35,0.80,1.15)$; $OQ$ heavy, $QP$ dashed, projections from $Q$ to both axes dashed; $\theta$ arc of radius 0.5 at the origin between the $x$-axis and $OQ$; $r$ beside $OQ$, $z$ beside $QP$.
- **Departure:** the brief places the $\theta$ arc "at $Q$"; the azimuth is the angle at the origin between the positive $x$-axis and $OQ$, so the arc and label are at $O$. This is a correction of the brief, not of the mathematics.
- **Checks:** $QP$ is exactly vertical; $Q$ is the orthographic projection of $P$; the $\theta$ arc ends on $OQ$.

## cylindrical-coordinates-2.svg — the volume element

- **Claim:** the coordinate box $[r,r+dr]\times[\theta,\theta+d\theta]\times[z,z+dz]$ has volume $r\,dr\,d\theta\,dz$.
- **Anchor:** after the display $dV=(dr)(r\,d\theta)(dz)=r\,dr\,d\theta\,dz$.
- **Construction:** cabinet view, 110 px per unit; cell with $r\in[0.75,1.35]$, $\theta\in[15°,60°]$, $z\in[0.55,1.15]$; the outer curved face and the top face shaded; dimension marks for $dr$ on the lower radial edge, $dz$ on the front-left vertical edge, and $r\,d\theta$ beside the outer top arc.
- **Departure:** the rays from the origin were dropped; at this zoom they add two long near-parallel lines without helping to read the cell. The labels sit outside the cell with short leaders instead of on the faces.
- **Checks:** the drawn edges are the four radial, four vertical and four arc segments of the stated ranges; the $dr$ and $dz$ marks are parallel to the edges they measure.

## cylindrical-coordinates-3.svg — a paraboloid cap

- **Claim:** the solid $r^2\le z\le4$ over $r\le2$ is bounded below by $z=r^2$ and above by $z=4$.
- **Anchor:** after "The two surfaces meet where $r^2=4$, so $r=2$."
- **Construction:** cabinet view, 44 px per unit vertically so the full height $z=4$ fits; paraboloid drawn as rings at $r=0.55,1.05,1.55,1.95$ and eight meridians, all sampled from $z=r^2$; the top disc at $z=4$ drawn semi-transparent with a dashed plane ellipse beyond it; the intersection circle at $r=2$ heavy; a vertical segment at $r=1.3$, $\theta=-55°$ from $z=r^2$ to $4$.
- **Departure:** the brief asks for a projection disc on the $xy$-plane; in plan it coincides with the top disc, so drawing it again would be a second disk in the same place. The labelled limits and the intersection circle carry the projection instead.
- **Checks:** every ring lies at $z=r^2$; the segment's lower dot is on $z=r^2$; the top disc and the heavy circle share the radius 2.

## Checks

- XML parsed; width/height match the viewBox; every `aria-labelledby` target exists; all IDs unique; no scripts, external references, embedded rasters or non-finite geometry; live `<text>` throughout.
- Rendered in headless Chrome at 2× intrinsic size and again at 240 px width; each render was inspected for clipping, overlap, legibility and agreement with the article's equations.
- Palette: the skill's canonical monochrome (`#312F2F`, `#BEB8B7`, `#636060`, `#E9E3E2`, `#E2DFDD`, `#979797`). The briefs' "one accent colour" line predates that palette; the accent is carried by weight and tone instead of hue.
- 3D figures use one shared cabinet axonometric (`u = x + 0.55y`, `v = z + 0.30y`, x right, y receding up-right, z up). The briefs' "x lower right, y lower left" was not used because it puts the origin at the back-top corner and hides the first octant; the cabinet view keeps the labelled faces visible. This is recorded per figure below where it matters.
