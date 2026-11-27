# Figure briefs — Flux Integrals

Article: `multivariable-calculus/flux-integrals.md`
Batch: `20261127T144139Z-01`
Figures: F1–F3

House monochrome style: black strokes on white, light-grey fills for surfaces and solids, no colour dependence. Each figure carries one mathematical claim.

## F1 — Flow through a small patch

+ Target heading: `## Flow across a surface`
+ Insertion anchor: the sentence `Reversing $\mathbf{n}$ reverses the sign of every contribution and therefore of the total.`
+ Mathematical claim: in time $\Delta t,$ the fluid crossing a patch of area $\Delta S$ fills a slanted cylinder of volume $(\mathbf{v}\cdot\mathbf{n})\Delta S\Delta t,$ so only the normal component of velocity contributes to the flux.
+ Equations and domain: a small planar patch with unit normal $\mathbf{n};$ a velocity vector $\mathbf{v}$ at an angle to the normal; the flow cylinder built on the patch; time increment $\Delta t.$
+ Scale: schematic, not to scale. The patch is drawn as a small parallelogram in perspective; the cylinder is short and slanted.
+ Objects and labels: the patch; the normal $\mathbf{n};$ the velocity $\mathbf{v};$ the angle $\theta$ between them; the slanted cylinder; labels $\Delta S,$ $\Delta t,$ and $(\mathbf{v}\cdot\mathbf{n})\Delta S\Delta t.$
+ Shading and visibility: cylinder shaded light grey; patch white with a black border; the component of $\mathbf{v}$ along $\mathbf{n}$ shown as a dashed projection.
+ Orientation: $\mathbf{v}\cdot\mathbf{n}>0$ in the drawing, so the flow crosses from the negative to the positive side.
+ Alt text: `A slanted flow cylinder through a small oriented patch, with velocity, normal, the angle between them, and the signed volume formula.`

## F2 — Equal flux through spheres of different radii

+ Target heading: `## An inverse-square field`
+ Insertion anchor: the sentence `The contrast between $4\pi$ and $0$ is entirely a question of what the surface encloses.`
+ Mathematical claim: the inverse-square field has flux $4\pi$ through every sphere centred at the origin, and zero flux through any closed surface that does not enclose the origin.
+ Equations and domain: two concentric spheres of radii $R_1<R_2$ around a point source at $O;$ a separate closed surface to one side, not containing $O.$
+ Scale: schematic perspective. The two spheres are drawn as circles with elliptical shading to suggest three dimensions; the separate surface is a small closed blob.
+ Objects and labels: point $O$ marked with a small filled dot and a radiating source symbol; inner sphere labelled $R_1,$ outer sphere $R_2;$ outward normals on both; annotations $\Phi=4\pi$ on both spheres; the separate closed surface labelled $\Phi=0.$
+ Shading and visibility: sphere surfaces unfilled, with front arcs solid and back arcs dashed; the separate surface light grey; field arrows radial, short and evenly spaced.
+ Orientation: normals point outward on all three surfaces.
+ Alt text: `Two concentric spheres of different radii around a point source, both labelled with flux 4 pi, and a separate closed surface away from the source labelled zero flux.`

## F3 — Divergence as net outward flux per volume

+ Target heading: `## Closed surfaces and the divergence theorem`
+ Insertion anchor: the sentence `A positive divergence is a net source per unit volume; a negative divergence is a sink; zero divergence means that whatever enters a small region leaves it.`
+ Mathematical claim: for a small box, the net outward flux divided by the volume tends to $\operatorname{div}\mathbf{F},$ with more flux leaving than entering when the divergence is positive.
+ Equations and domain: a small rectangular box centred at $P;$ arrows entering through the left and bottom faces and leaving through the right and top faces, with the outgoing arrows longer; annotation $\operatorname{div}\mathbf{F}(P)=\lim_{V\to0}\frac1V\iint_{\partial E}\mathbf{F}\cdot\mathbf{n}\,dS.$
+ Scale: schematic perspective, box drawn small relative to the page, with faces labelled only where needed.
+ Objects and labels: box; point $P;$ outward normals on two faces; incoming arrow labelled $\mathbf{F}_{\mathrm{in}};$ outgoing arrow labelled $\mathbf{F}_{\mathrm{out}};$ the divergence formula.
+ Shading and visibility: box edges solid, hidden edges dashed; one face light grey to show orientation; arrows solid.
+ Orientation: all face normals point outward.
+ Alt text: `A small box with a stronger field leaving than entering, illustrating divergence as net outward flux per unit volume.`
