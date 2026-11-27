# Figure briefs — Parametric Surfaces

Article: `multivariable-calculus/parametric-surfaces.md`
Batch: `20261127T144139Z-01`
Figures: F1–F3

House monochrome style: black strokes on white, light-grey fills only where needed for depth, no colour dependence. Each figure carries one mathematical relationship.

## F1 — From a parameter rectangle to a surface patch

+ Target heading: `## Surface area`
+ Insertion anchor: the sentence `In one dimension the linearization is a tangent vector and its length; in two dimensions it is a parallelogram and its area.`
+ Mathematical claim: a small rectangle of sides $\Delta u,\Delta v$ in the parameter domain maps approximately to the parallelogram spanned by $\mathbf{r}_u\Delta u$ and $\mathbf{r}_v\Delta v,$ whose area is $\lVert\mathbf{r}_u\times\mathbf{r}_v\rVert\Delta u\Delta v.$
+ Equations and domain: a generic smooth patch $\mathbf{r}(u,v)$ over a rectangular parameter domain; one interior base point $(u_0,v_0)$; sides $\Delta u,\Delta v.$
+ Scale: schematic. Two panels side by side, the left panel the $uv$-plane and the right panel the surface in perspective. The rectangle is drawn small relative to the patch.
+ Objects and labels: left panel axes $u,v,$ rectangle with corners $(u_0,v_0)$ and $(u_0+\Delta u,v_0+\Delta v);$ right panel the patch, the base point $\mathbf{r}(u_0,v_0),$ the tangent vectors $\mathbf{r}_u\Delta u$ and $\mathbf{r}_v\Delta v,$ the shaded parallelogram they span, and the normal $\mathbf{r}_u\times\mathbf{r}_v.$ A curved arrow maps the rectangle to the parallelogram.
+ Shading and visibility: parallelogram filled light grey; hidden parts of the patch dashed; tangent vectors solid with filled arrowheads; normal solid.
+ Orientation: $\mathbf{r}_u$ and $\mathbf{r}_v$ consistent with the right-hand rule for the normal shown.
+ Alt text: `A small rectangle in the uv-plane mapped to a surface patch, with tangent vectors spanning a shaded parallelogram whose area is the surface element.`

## F2 — Sphere coordinate grid and the pole degeneracy

+ Target heading: `## The sphere`
+ Insertion anchor: the sentence `At the poles, $\sin\varphi=0$ and the cross product vanishes.`
+ Mathematical claim: the standard sphere parameterization has coordinate curves of constant $\theta$ and constant $\varphi,$ and the tangent vectors degenerate at $\varphi=0$ and $\varphi=\pi,$ so the parameterization is not regular there.
+ Equations and domain: unit sphere; meridians at $\theta=0,\pi/2,\pi,3\pi/2;$ parallels at $\varphi=\pi/6,\pi/3,\pi/2,2\pi/3,5\pi/6.$
+ Scale: perspective view of the sphere, equal axis scaling, with the $z$-axis vertical.
+ Objects and labels: the sphere outline; selected meridians and parallels; labels $\theta$ on the equator and $\varphi$ at the north pole measured from the positive $z$-axis; the two poles marked $N$ and $S;$ a small note that $\mathbf{r}_\theta\times\mathbf{r}_\varphi=\mathbf{0}$ at both poles.
+ Shading and visibility: front grid lines solid, back grid lines dashed or omitted; the sphere unfilled; poles as filled dots.
+ Orientation: $\theta$ increasing counterclockwise seen from above; $\varphi$ increasing from $N$ toward $S.$
+ Alt text: `A sphere with meridians and parallels, the polar angle marked from the north pole, and a note that the tangent vectors vanish at both poles.`

## F3 — A Möbius band has no continuous normal

+ Target heading: `## Orientation`
+ Insertion anchor: the sentence `A regular parametric patch is always orientable, because the parameter domain chooses a side; the obstruction appears only when patches are glued with a twist.`
+ Mathematical claim: transporting a normal once around a Möbius band returns it pointing to the opposite side, so no continuous unit normal field exists and the band is nonorientable.
+ Equations and domain: a Möbius band obtained from a rectangle with a half-twist; one normal arrow at the starting point and its transported copy after one full circuit.
+ Scale: schematic perspective drawing; the band is a narrow strip with a visible half-twist, not a physical rendering.
+ Objects and labels: the band; a starting point $P$ with normal $\mathbf{n};$ a dashed path along the band; the transported normal at $P$ after one circuit labelled $-\mathbf{n};$ a short caption `one circuit reverses the normal.`
+ Shading and visibility: the band drawn with two tones of grey or with hatching to show the twist; the reverse side indicated by a dashed edge; normals solid black.
+ Orientation: the circuit direction marked with an arrow; $\mathbf{n}$ and $-\mathbf{n}$ drawn on opposite sides of the strip at the same point.
+ Alt text: `A Möbius band with a normal transported once around the strip returning as its negative, showing that the surface has only one side.`
