# Figure briefs — Laplacian

Article: `multivariable-calculus/laplacian.md`
Batch: `20261127T134100Z-01`

## F1 — Value at the centre and average over a small sphere

+ Target heading: "What the Laplacian measures"
+ Insertion anchor: after "The formula says that $\Delta f(P)$ is positive when the average of $f$ on a small sphere exceeds $f(P),$ negative when it falls below, and zero when the two agree to second order."
+ Mathematical claim: for small $r,$ the spherical average satisfies $A_f(P,r)-f(P)\approx (r^2/6)\Delta f(P)$ in three dimensions.
+ Objects: a point $P$ with a small sphere $S_r(P)$ around it; a graph of $f$ as a surface above the plane, with the value $f(P)$ marked and the average level drawn as a horizontal plane; a vertical bar showing the gap between the two levels.
+ Labels: $P,$ $S_r(P),$ $f(P),$ $A_f(P,r),$ $r,$ and the sign of $A_f-f.$
+ Construction: choose a function with positive Laplacian at $P$ so that the average level lies above $f(P),$ and show the gap growing with $r.$ A second small inset can show the negative case with the average below.
+ Distinction: schematic; the sphere is small relative to the variation of $f,$ and the gap is exaggerated for visibility.
+ Shading: light tint on the sphere and a faint horizontal disk at the average level.
+ Alt text: "A small sphere around a point on a surface, with the average height over the sphere compared to the height at the centre."

## F2 — Harmonic saddle and nonharmonic bowl

+ Target heading: "Harmonic functions"
+ Insertion anchor: after "It is the square of the distance from the origin, and it is strictly subharmonic."
+ Mathematical claim: $f=x^2-y^2$ is harmonic, with level curves that are hyperbolas and a saddle at the origin; $g=x^2+y^2$ is not harmonic, with circular level curves and a minimum at the origin.
+ Objects: two square panels. Left: the saddle surface of $x^2-y^2$ with two families of level hyperbolas and arrows of $\nabla f;$ label $\Delta f=0.$ Right: the bowl of $x^2+y^2$ with concentric circular level curves and outward gradient arrows; label $\Delta g=4.$
+ Labels: $x,$ $y,$ $z,$ $\Delta f=0,$ $\Delta g=4,$ and the origin as a saddle or minimum.
+ Construction: use the same vertical scale. On the left, show one direction curving up and the perpendicular direction curving down, so the two curvatures cancel in the trace. On the right, show both directions curving up.
+ Distinction: the level curves alone do not determine harmonicity; the second derivatives do. The figure should make the cancellation visible through the surface shape, not only through the labels.
+ Shading: light surface shading with a neutral palette; no colour gradient that suggests magnitude of the Laplacian.
+ Alt text: "A harmonic saddle surface with opposite curvatures and a nonharmonic bowl with both curvatures upward."

## F3 — Coordinate boxes and metric factors

+ Target heading: "Coordinate expressions"
+ Insertion anchor: after "A coordinate box in cylindrical coordinates has side lengths $dr,$ $r\,d\theta$ and $dz;$ in spherical coordinates its sides are $d\rho,$ $\rho\,d\varphi$ and $\rho\sin\varphi\,d\theta.$"
+ Mathematical claim: the Laplacian in curvilinear coordinates contains the metric factors because the coordinate box has edge lengths $dr,$ $r\,d\theta,$ $dz$ in cylindrical coordinates and $d\rho,$ $\rho\,d\varphi,$ $\rho\sin\varphi\,d\theta$ in spherical coordinates.
+ Objects: two panels. Left: a cylindrical coordinate box bounded by $r,$ $r+dr,$ $\theta,$ $\theta+d\theta,$ $z,$ $z+dz,$ with edge labels. Right: a spherical coordinate box bounded by $\rho,$ $\rho+d\rho,$ $\varphi,$ $\varphi+d\varphi,$ $\theta,$ $\theta+d\theta,$ with edge labels.
+ Labels: $dr,$ $r\,d\theta,$ $dz$ on the left; $d\rho,$ $\rho\,d\varphi,$ $\rho\sin\varphi\,d\theta$ on the right; the axes and the angles.
+ Construction: draw the boxes as curvilinear cells, not as Cartesian cubes. On the right, show the parallel edge shortening near the pole by making the top edge visibly shorter. Use dashed lines for the hidden edges.
+ Distinction: schematic; the cells are finite but labelled with differentials to indicate the infinitesimal limit.
+ Shading: light tint on the visible faces; no attempt to show volume numerically.
+ Alt text: "Curvilinear coordinate boxes in cylindrical and spherical coordinates with edge lengths showing the metric factors."
