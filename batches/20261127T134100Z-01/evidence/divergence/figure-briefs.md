# Figure briefs — Divergence

Article: `multivariable-calculus/divergence.md`
Batch: `20261127T134100Z-01`

## F1 — Flux through the faces of an infinitesimal box

+ Target heading: "The infinitesimal box"
+ Insertion anchor: after "This is the coordinate-free definition: the divergence is the outward flux per unit volume in the limit of shrinking closed surfaces around the point."
+ Mathematical claim: the net outward flux through the six faces of a box of sides $\Delta x,\Delta y,\Delta z$ is approximately $(P_x+Q_y+R_z)\Delta x\Delta y\Delta z.$
+ Objects: a rectangular box centred at $P;$ the $x$-faces highlighted with outward normals $-\mathbf{i}$ and $+\mathbf{i};$ arrows of $\mathbf{F}$ crossing the box; labels $\Delta x,$ $\Delta y,$ $\Delta z.$
+ Labels: $P,$ $\Delta x,$ $\Delta y,$ $\Delta z,$ $\mathbf{n},$ and the two $x$-faces labelled $x-\Delta x/2$ and $x+\Delta x/2.$
+ Construction: show the flux difference on the $x$-faces explicitly with a short arrow entering the left face and a longer arrow leaving the right face. The other faces can be drawn in a lighter stroke.
+ Distinction: schematic; the box is small but not drawn as a point. Do not attempt to draw all six flux contributions with equal emphasis.
+ Shading: light tint on the two $x$-faces; the interior left unfilled.
+ Alt text: "A small box with outward normals on its two x-faces and field arrows entering one face and leaving the other."

## F2 — Source, sink and volume-preserving flow

+ Target heading: "The infinitesimal box"
+ Insertion anchor: after "Zero divergence means that the outward flux through every sufficiently small closed surface is negligible relative to its volume; the field neither creates nor destroys volume at that point."
+ Mathematical claim: positive divergence produces net outward flow, negative divergence net inward flow, and zero divergence a balance of inflow and outflow.
+ Objects: three panels of a small disk or sphere with arrows. Left: arrows pointing radially outward, labelled $\operatorname{div}\mathbf{F}>0.$ Centre: arrows pointing inward, labelled $\operatorname{div}\mathbf{F}<0.$ Right: arrows entering one side and leaving the other with equal strength, labelled $\operatorname{div}\mathbf{F}=0.$
+ Labels: the three signs, and the words source, sink, volume-preserving (or incompressible).
+ Construction: use the same number and length of arrows in all three panels so that only the pattern differs. In the right panel, the arrows should pass through the region rather than radiate from its centre.
+ Distinction: schematic; the region is a small control volume, not a level surface of the field.
+ Shading: light tint inside each control volume, with the boundary drawn as a thin closed curve.
+ Alt text: "Three small regions showing outward flow for positive divergence, inward flow for negative divergence, and balanced through-flow for zero divergence."

## F3 — Partition of a solid and cancellation on interior faces

+ Target heading: "The divergence theorem"
+ Insertion anchor: after "A general solid is partitioned into small boxes, the integrals over interior faces cancel because the outward normals are opposite, and the boundary integrals converge to the integral over $S.$"
+ Mathematical claim: in a partition of $E$ into boxes, each interior face is shared by two boxes with opposite outward normals, so its flux contributions cancel; only the boundary faces survive.
+ Objects: a solid $E$ with a curved boundary $S,$ cut into a grid of small boxes; one interior face enlarged in a callout, with the two opposite normals $\mathbf{n}$ and $-\mathbf{n};$ the outer boundary faces shaded.
+ Labels: $E,$ $S=\partial E,$ $\mathbf{n},$ $-\mathbf{n},$ and a note "interior faces cancel."
+ Construction: draw the grid in perspective, with the boundary boxes clipped by $S.$ The callout should show the same face seen from the two adjacent boxes.
+ Distinction: schematic; the grid is coarse enough to be legible, and the curved boundary is visibly approximated by the boundary faces.
+ Shading: boundary faces in one tint, interior faces in white, the solid body in very light grey.
+ Alt text: "A solid partitioned into small boxes, with opposite normals on a shared interior face cancelling and the outer boundary faces remaining."
