# Figure briefs — Surface Integrals

Article: `multivariable-calculus/surface-integrals.md`
Batch: `20261127T144139Z-01`
Figures: F1–F3

House monochrome style: black strokes on white, light-grey fills for patches, no colour dependence. Each figure carries one mathematical relationship.

## F1 — Partition of a surface into area patches

+ Target heading: `## Integrating over a surface`
+ Insertion anchor: the sentence `The intersection has zero area and contributes nothing.`
+ Mathematical claim: the scalar surface integral is the limit of $\sum f(P_{ij})\Delta S_{ij},$ where each $\Delta S_{ij}$ is the area of a small surface patch, not its projection.
+ Equations and domain: a curved patch $S$ over a parameter grid; a $3\times3$ partition drawn schematically; one patch highlighted with sample point $P_{ij}$ and area label $\Delta S_{ij}.$
+ Scale: schematic perspective. The patches are drawn with visibly curved edges, so that they are not mistaken for planar rectangles.
+ Objects and labels: surface boundary; grid curves subdividing it; the highlighted patch; point $P_{ij};$ label $\Delta S_{ij};$ a small annotation $\sum f(P_{ij})\Delta S_{ij}\to\iint_S f\,dS.$
+ Shading and visibility: highlighted patch light grey; the rest of the surface white; grid lines thin; boundary thick.
+ Orientation: none required, since the scalar integral is orientation-independent. Do not draw a normal.
+ Alt text: `A curved surface divided into small patches, one patch shaded and labelled with its area and a sample point, illustrating the Riemann sum for a surface integral.`

## F2 — Surface element and its projection

+ Target heading: `## Graphs and implicit surfaces`
+ Insertion anchor: the sentence `For a horizontal plane it equals $1;$ for a steep surface it is large.`
+ Mathematical claim: for a graph $z=g(x,y),$ a small surface element $dS$ projects to $dx\,dy,$ and $dS=\sqrt{1+g_x^2+g_y^2}\,dx\,dy;$ the factor is the secant of the angle between the normal and the vertical.
+ Equations and domain: a smooth graph over a small rectangle in the $xy$-plane; the tangent plane at one point; the normal $\langle-g_x,-g_y,1\rangle.$
+ Scale: schematic perspective, with the $xy$-plane drawn as a parallelogram in perspective and the vertical direction indicated by an arrow.
+ Objects and labels: the graph; the projection rectangle $dx\,dy$ on the $xy$-plane; the tilted parallelogram $dS$ on the graph; the normal $\mathbf{n};$ the angle $\gamma$ between $\mathbf{n}$ and the $z$-axis; the formula $dS=dx\,dy/\cos\gamma=\sqrt{1+g_x^2+g_y^2}\,dx\,dy.$
+ Shading and visibility: the projection rectangle light grey; the surface element a slightly darker grey; the vertical dashed line from the element to its projection; the normal solid.
+ Orientation: the normal points upward, with positive $z$-component.
+ Alt text: `A tilted surface element above its rectangular projection on the xy-plane, with the normal, the angle to the vertical, and the square-root area factor.`

## F3 — Normal component and flux sign

+ Target heading: `## Vector surface integrals`
+ Insertion anchor: the sentence `The scalar surface integral of $\lVert\mathbf{F}\rVert$ is a different quantity: it is nonnegative, and it bounds the magnitude of the flux without recording its sign.`
+ Mathematical claim: the vector surface integral counts only $\mathbf{F}\cdot\mathbf{n},$ so a field crossing the surface contributes with the sign of the normal component, while a tangential field contributes nothing.
+ Equations and domain: an oriented patch with unit normal $\mathbf{n};$ three field arrows: one crossing in the direction of $\mathbf{n},$ one crossing against it, and one tangent to the surface.
+ Scale: schematic perspective. The patch is a gently curved quadrilateral; the arrows are of equal length so that only direction varies.
+ Objects and labels: the patch; the normal $\mathbf{n}$ at its centre; field arrows $\mathbf{F}_1,\mathbf{F}_2,\mathbf{F}_3;$ labels $+\mathbf{F}\cdot\mathbf{n},$ $-\mathbf{F}\cdot\mathbf{n},$ and $0$ respectively; the annotation $\iint_S\mathbf{F}\cdot\mathbf{n}\,dS.$
+ Shading and visibility: patch light grey; normal dashed; field arrows solid; the tangent arrow drawn parallel to the patch surface.
+ Orientation: $\mathbf{n}$ points to the positive side; the sign labels must match the arrow directions relative to $\mathbf{n}.$
+ Alt text: `An oriented surface patch with three field arrows, one along the normal counted positive, one against it counted negative, and one tangent counted zero.`
