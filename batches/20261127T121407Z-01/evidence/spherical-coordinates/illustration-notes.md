# Illustration notes — Spherical Coordinates

Article: `multivariable-calculus/spherical-coordinates.md`

## spherical-coordinates-1.svg — a point in spherical coordinates

- **Claim:** $P$ is described by $\rho=OP$, the azimuth $\theta$ of its projection $Q$, and the polar angle $\varphi$ from the positive $z$-axis to $OP$.
- **Anchor:** after "The azimuth $\theta$ is undefined on the $z$-axis, and both angles are undefined at the origin, where $\rho=0$."
- **Construction:** cabinet view, 86 px per unit; $P$ at $\rho=1.75$, $\theta=33°$, $\varphi=46°$; $OP$ heavy, $QP$ dashed, $OQ$ dashed; $\theta$ arc of radius 0.5 in the $xy$-plane; $\varphi$ arc of radius 0.62 in the vertical half-plane containing $P$, from the $z$-axis to $OP$.
- **Checks:** both arcs are sampled from the same spherical formula as $P$; the $\varphi$ arc ends on $OP$; the $\theta$ arc ends on $OQ$.

## spherical-coordinates-2.svg — the volume element

- **Claim:** a coordinate box with increments $d\rho,d\varphi,d\theta$ has edge lengths $d\rho$, $\rho\,d\varphi$, $\rho\sin\varphi\,d\theta$ and volume $\rho^2\sin\varphi\,d\rho\,d\varphi\,d\theta$.
- **Anchor:** after the display for $dV$ that follows "the volume is their product:".
- **Construction:** cabinet view, 200 px per unit; cell with $\rho\in[0.82,1.22]$, $\varphi\in[30°,54°]$, $\theta\in[16°,56°]$; outer spherical patch, the $\theta$-patch and the $\varphi$-patch shaded at three tones; all twelve edges sampled from the spherical map; three labels outside the cell with short leaders.
- **Departure:** the brief asks for the two spheres, two cones and two half-planes to be visible as surfaces. At the scale of a differential cell those surfaces would swamp the cell, so the cell is drawn as a wireframe patch with its bounding faces shaded and the three edge lengths labelled; the article supplies the algebra of the three surfaces. This is the weakest figure of the batch at 240 px.
- **Checks:** every edge is a segment of constant two of the three coordinates; the three labelled edges meet at one corner; the volume formula matches the edge labels.

## spherical-coordinates-3.svg — the ice-cream cone

- **Claim:** the solid inside $\rho=2$ and $\varphi=\pi/4$ is $0\le\rho\le2$, $0\le\varphi\le\pi/4$.
- **Anchor:** after "The cone opens around the positive $z$-axis and has half-angle $\pi/4$."
- **Construction:** cabinet view; the sphere drawn as its silhouette circle with a dashed equator; the rim is the circle $\rho=2$, $\varphi=\pi/4$, i.e. $r=z=\sqrt2$; the cone's two generators run from the origin to the rim's projected extremes (which are at $45°$ to the vertical, matching the half-angle); the cap is filled between the rim's front arc and the sphere's silhouette, and the hidden half of the rim is dashed.
- **Departure:** the brief says "sphere drawn as a circle outline with a light equator"; that is what is used, with the rim computed from the spherical map rather than drawn by eye.
- **Checks:** the rim lies on both $\rho=2$ and $\varphi=\pi/4$; the filled cap boundary closes on the sphere circle; the generators meet the rim at its silhouette points.

## Checks

- XML parsed; width/height match the viewBox; every `aria-labelledby` target exists; all IDs unique; no scripts, external references, embedded rasters or non-finite geometry; live `<text>` throughout.
- Rendered in headless Chrome at 2× intrinsic size and again at 240 px width; each render was inspected for clipping, overlap, legibility and agreement with the article's equations.
- Palette: the skill's canonical monochrome (`#312F2F`, `#BEB8B7`, `#636060`, `#E9E3E2`, `#E2DFDD`, `#979797`). The briefs' "one accent colour" line predates that palette; the accent is carried by weight and tone instead of hue.
- 3D figures use one shared cabinet axonometric (`u = x + 0.55y`, `v = z + 0.30y`, x right, y receding up-right, z up). The briefs' "x lower right, y lower left" was not used because it puts the origin at the back-top corner and hides the first octant; the cabinet view keeps the labelled faces visible. This is recorded per figure below where it matters.
