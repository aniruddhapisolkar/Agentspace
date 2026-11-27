# Illustration notes — Change of Variables in Multiple Integrals

Article: `multivariable-calculus/change-of-variables-in-multiple-integrals.md`

## change-of-variables-in-multiple-integrals-1.svg — the polar area element

- **Claim:** a coordinate cell $[r,r+dr]\times[\theta,\theta+d\theta]$ has area approximately $r\,dr\,d\theta$.
- **Anchor:** after "Hence $dx\,dy=r\,dr\,d\theta$, the area element used in the entry on polar coordinates."
- **Construction:** equal scale 118 px per unit; cell with $r\in[1.02,1.52]$, $\theta\in[24°,48°]$; inner and outer arcs sampled at 20 points, radial sides straight; rays extended as dashed guides; $\theta$ arc from the $x$-axis to the first ray and a separate $d\theta$ arc between the rays; $dr$ on the lower radial side, $r\,d\theta$ outside the outer arc.
- **Departure:** the brief's right-angle mark was removed: at this scale a square at the corner reads as a stray tick and the arcs already establish the right angle. The two angle labels were separated so $\theta$ and $d\theta$ denote different arcs.
- **Checks:** the cell closes on two circular arcs and two radii; $r\,d\theta$ is placed at radius $r_1$, where the arc length is measured.

## change-of-variables-in-multiple-integrals-2.svg — a linear map

- **Claim:** $\Phi(u,v)=(u+v,u-v)$ maps the unit square to a square of area $|\det D\Phi|=2$.
- **Anchor:** after "Its side length is $\sqrt2$, so its area is $2$."
- **Construction:** two panels at the same scale (48 px per unit); left the unit square $T$ with vertices labelled; right the image with vertices $(0,0),(1,1),(2,0),(1,-1)$; the images of $e_1$ and $e_2$ drawn as arrows from the origin; $\Phi$ between the panels; $|\det D\Phi|=2$ below.
- **Checks:** image vertices computed from $\Phi$; the drawn quadrilateral is the image square, side $\sqrt2$ and area 2.

## change-of-variables-in-multiple-integrals-3.svg — the disc to ellipse

- **Claim:** $x=au$, $y=bv$ sends the unit disc to the ellipse $x^2/a^2+y^2/b^2\le1$ and multiplies area by $ab$.
- **Anchor:** after "The area of the ellipse is therefore $\pi ab$…"
- **Construction:** two panels at the same scale (44 px per unit); left the unit disc with one inner circle and four radial guides; right the ellipse with $a=1.6$, $b=0.9$, the same guides mapped, semi-axes marked; areas $\pi$ and $\pi ab$ under the panels; $\Phi$ between them.
- **Checks:** every right-panel curve is the image under $(u,v)\mapsto(1.6u,0.9v)$ of the corresponding left-panel curve; the inner circle maps to the inner ellipse.

## Checks

- XML parsed; width/height match the viewBox; every `aria-labelledby` target exists; all IDs unique; no scripts, external references, embedded rasters or non-finite geometry; live `<text>` throughout.
- Rendered in headless Chrome at 2× intrinsic size and again at 240 px width; each render was inspected for clipping, overlap, legibility and agreement with the article's equations.
- Palette: the skill's canonical monochrome (`#312F2F`, `#BEB8B7`, `#636060`, `#E9E3E2`, `#E2DFDD`, `#979797`). The briefs' "one accent colour" line predates that palette; the accent is carried by weight and tone instead of hue.
- 3D figures use one shared cabinet axonometric (`u = x + 0.55y`, `v = z + 0.30y`, x right, y receding up-right, z up). The briefs' "x lower right, y lower left" was not used because it puts the origin at the back-top corner and hides the first octant; the cabinet view keeps the labelled faces visible. This is recorded per figure below where it matters.
