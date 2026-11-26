# Figure briefs — Tangent Planes and Linear Approximations

Article: `multivariable-calculus/tangent-planes-and-linear-approximations.md`
Batch: `20261126T193918Z-01`
Prepared by: Writer. Illustrator inserts final image links; this file contains no SVG source.

## F1 — Tangent plane and normal line to a graph

+ Target heading: `## Equation of the tangent plane`
+ Insertion anchor (exact sentence, insert after it): `The vector $(-f_x,-f_y,1)$ is also normal; the two differ only by sign.`
+ Mathematical claim: at a point $P=(x_0,y_0,f(x_0,y_0))$, the tangent plane is $z=f(x_0,y_0)+f_x(x_0,y_0)(x-x_0)+f_y(x_0,y_0)(y-y_0)$, and $(f_x,f_y,-1)$ is normal to it.
+ Equations and domain: a smooth graph $z=f(x,y)$ near $(x_0,y_0)$; the plane (3) of the article.
+ Scale: 3D schematic, not to scale.
+ Objects and labels: the surface as a curved sheet; the tangent plane as a translucent rectangle through $P$; the normal vector drawn from $P$; the two coordinate tangent lines in the sections $x=x_0$ and $y=y_0$; labels $P$, $f_x$, $f_y$, $\mathbf n$.
+ Shading/visibility: surface in a neutral colour, plane in blue with transparency, normal arrow in a contrasting colour; hidden parts of the normal dashed.
+ Orientation: standard right-handed axes; view chosen so that both coordinate tangent lines are visible and the normal points towards the viewer without foreshortening to a point.
+ Alt text: "A surface with its tangent plane at a point P, the two coordinate tangent lines in the plane, and a normal vector."

## F2 — The error of a linear approximation

+ Target heading: `## A numerical linear approximation`
+ Insertion anchor (exact sentence, insert after it): `The approximation is useful because the increments are small compared with the distance from the origin, and because the second derivatives are bounded near $(4,4)$.`
+ Mathematical claim: near $(4,4)$, the tangent plane to $z=\sqrt{x^2+y^2}$ stays close to the surface, and the vertical gap grows quadratically with the distance from the point of tangency.
+ Equations and domain: $f(x,y)=\sqrt{x^2+y^2}$; $L(x,y)=4\sqrt{2}+\frac{1}{\sqrt{2}}(x-4)+\frac{1}{\sqrt{2}}(y-4)$; the specific point $(3.98,4.03)$ with $f\approx5.664036$ and $L\approx5.663925$.
+ Scale: two panels. Left: a 3D view of the cone-like surface near $(4,4)$ with the tangent plane. Right: a 2D cross-section along the radial line through $(4,4)$, showing the curve, the tangent line, and the vertical error at the displaced point.
+ Objects and labels: $P=(4,4,4\sqrt{2})$; the tangent plane; the exact point $Q=(3.98,4.03,f(3.98,4.03))$; the corresponding point on the plane; the vertical segment between them labelled "error $\approx1.1\times10^{-4}$".
+ Shading/visibility: the plane translucent; the error segment exaggerated in length and marked as exaggerated; the surface grid fine enough to show curvature.
+ Orientation: left panel standard axes; right panel horizontal axis along the radial direction, vertical axis $z$.
+ Alt text: "The surface z=sqrt(x^2+y^2), its tangent plane at (4,4), and the small vertical error at (3.98,4.03)."

## F3 — Gradient normal to a level surface

+ Target heading: `## Tangent planes to level surfaces`
+ Insertion anchor (exact sentence, insert after it): `The gradient is normal to the surface.`
+ Mathematical claim: for $F(x,y,z)=x^2+y^2+z^2$ and $P=(1,2,3)$ on the level surface $F=14$, the gradient $\nabla F(P)=(2,4,6)$ is normal to the surface, and the tangent plane is $x+2y+3z=14$.
+ Equations and domain: the sphere $x^2+y^2+z^2=14$; the plane $x+2y+3z=14$; the normal direction $(1,2,3)$.
+ Scale: 3D schematic; the sphere drawn as a translucent wireframe so that the tangent plane and normal remain visible.
+ Objects and labels: the sphere; the point $P$; the tangent plane touching at $P$; the gradient arrow from $P$ along $(1,2,3)$; a curve $\gamma$ on the sphere through $P$ with its tangent vector, to indicate the orthogonality argument; labels $\nabla F(P)$, $\gamma'(0)$, $P$.
+ Shading/visibility: sphere wireframe in grey, tangent plane in blue, gradient arrow in a warm colour, curve and tangent vector in green; the right angle between the gradient and $\gamma'(0)$ marked.
+ Orientation: standard right-handed axes; the view should show the sphere as a sphere, not as a circle, and the plane as a plane.
+ Alt text: "A sphere with its tangent plane at P=(1,2,3), the gradient (2,4,6) normal to the plane, and a curve on the sphere whose tangent is orthogonal to the gradient."

## F4 — A continuous graph with no tangent plane

+ Target heading: `## When partial derivatives are not enough`
+ Insertion anchor (exact sentence, insert after it): `Its graph has no tangent plane there, even though both coordinate sections are flat.`
+ Mathematical claim: $f(x,y)=xy/\sqrt{x^2+y^2}$ is continuous at the origin, has both partial derivatives zero there, but the quotient $f(h,k)/\sqrt{h^2+k^2}=hk/(h^2+k^2)$ depends on the direction, so no tangent plane exists.
+ Equations and domain: the piecewise function of the article; the two coordinate sections $f(x,0)=0$ and $f(0,y)=0$; the diagonal section $f(t,t)=t/\sqrt{2}$ up to sign.
+ Scale: 3D schematic with a cut-away near the origin; not to scale.
+ Objects and labels: the surface, flat along both coordinate axes but rising and falling along the diagonals; the two axis sections highlighted; the diagonal directions marked; a small inset of the level curves $xy/(x^2+y^2)=\text{constant}$ near the origin, showing the four sectors.
+ Shading/visibility: the surface translucent near the origin so the saddle-like behaviour is visible; the diagonal ridges in a warmer colour; the axes in a contrasting colour.
+ Orientation: standard right-handed axes, viewed from above the diagonal so that both the flat axes and the diagonal rise are visible.
+ Alt text: "The continuous surface z=xy/sqrt(x^2+y^2), flat along both coordinate axes but with different slopes along the diagonals, so no tangent plane exists at the origin."
