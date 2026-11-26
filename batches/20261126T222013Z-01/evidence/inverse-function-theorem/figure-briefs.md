# Figure briefs — Inverse Function Theorem

Article: `multivariable-calculus/inverse-function-theorem.md`
Batch: `20261126T222013Z-01`
Order: F1, F2, F3 (reading order)

## F1 — A local bijection between neighbourhoods

+ **Target heading:** "The theorem".
+ **Insertion anchor:** after the paragraph ending "it produces." Insert before the paragraph "The condition is sufficient, not necessary."
+ **Mathematical claim:** If $Df(a)$ is invertible, a small neighbourhood $V$ of $a$ is mapped bijectively onto an open neighbourhood $W$ of $b=f(a)$, and the inverse map $g$ returns each point of $W$ to its unique preimage in $V$.
+ **Equations and domain:** A schematic nonlinear map $f:\mathbb{R}^2\to\mathbb{R}^2$, for example $f(x,y)=(x+y^2/4,\;y+x^2/4)$ at $a=(0,0)$, where $Df(a)=I$, shown on a small square neighbourhood. No numerical accuracy required; the grid should bend smoothly.
+ **Scale and style:** Two side-by-side square panels: the left panel shows the $(x,y)$-plane with a shaded square $V$ around $a$ and a fine Cartesian grid; the right panel shows the $(u,v)$-plane with the image $W=f(V)$ and the image of the grid as a curvilinear mesh.
+ **Objects and labels:** Left: point $a$, neighbourhood $V$, axes $x,y$. Right: point $b=f(a)$, neighbourhood $W$, axes $u,v$, and a few arrows labelled $f$ from the left panel to the right and $g=f^{-1}$ in the reverse direction. A single highlighted point $x\in V$ and its image $y=f(x)\in W$ with arrows both ways.
+ **Shading and visibility:** Shade $V$ and $W$ lightly in matching colours; draw the grid thin; keep the arrows and marked points clearly visible. No heavy 3D effects.
+ **Orientation:** Standard Cartesian orientation in both panels, equal aspect ratio.
+ **Coordinates and parameters:** Mark only $a$, $b$, $x$, $y$; no numeric tick labels. State in the caption that $f$ is a local bijection and $g$ its inverse.
+ **Alt text:** "Two panels showing a small neighbourhood V around a point a and its image W around b under a nonlinear map f, with a curvilinear grid in W and arrows for f and its local inverse g."

## F2 — Polar coordinates: local inverse, global repetition

+ **Target heading:** "Polar coordinates".
+ **Insertion anchor:** after the paragraph ending "and on that interval the map is injective." Insert before the paragraph "The derivative of the inverse can be read from (1)."
+ **Mathematical claim:** The polar-coordinate map $(r,\theta)\mapsto(r\cos\theta,r\sin\theta)$ is locally invertible for $r>0$ because its Jacobian determinant is $r$, but it is not globally injective because $\theta$ and $\theta+2\pi$ give the same point.
+ **Equations and domain:** Two panels. Left: the rectangle $0.5\le r\le1.5$, $-\pi/2<\theta<\pi/2$ in the $(r,\theta)$-plane, with a rectangular grid. Right: its image in the $(x,y)$-plane, the right half-annulus with $0.5\le\sqrt{x^2+y^2}\le1.5$ and $x>0$, with the images of the grid lines: circles $r=\text{constant}$ and rays $\theta=\text{constant}$.
+ **Scale and style:** Two panels with equal aspect ratio; the left panel uses a Cartesian $(r,\theta)$ grid, the right panel uses polar geometry. The right panel should show a faint duplicate sector for $\theta+2\pi$ or an arrow indicating periodicity.
+ **Objects and labels:** Left axes $r$ and $\theta$, with $\theta=-\pi/2,0,\pi/2$ marked and $r=0.5,1,1.5$ marked. Right axes $x,y$; label the half-annulus "image of $f$"; mark a point $(r_0,\theta_0)$ and its image; draw an arrow labelled "$+2\pi$" from the displayed sector to a faint repeated sector, with the label "same image".
+ **Shading and visibility:** Light shading for the source rectangle and its image; grid lines in a contrasting colour; the repeated sector faint and dashed. No opaque fills over the arrows.
+ **Orientation:** Standard orientation in both panels; the right panel shows the right half-plane sector.
+ **Coordinates and parameters:** The radial values $0.5$, $1$, $1.5$; angular endpoints $-\pi/2$, $0$, $\pi/2$. The point $(r_0,\theta_0)$ may be chosen at $(1,\pi/4)$.
+ **Alt text:** "A rectangle in the r-theta plane mapped to a half-annulus in the x-y plane by polar coordinates, with a faint repeated sector showing that theta and theta plus two pi give the same image."

## F3 — The one-dimensional inverse and its tangent

+ **Target heading:** "The one-dimensional case".
+ **Insertion anchor:** after the paragraph ending "so the conclusion of the theorem fails while a continuous inverse still exists." Insert before the heading "## A linear example".
+ **Mathematical claim:** The graph of the inverse is the reflection of the graph of $f$ in the line $y=x$, so the tangent slope of the inverse is the reciprocal of the tangent slope of $f$; at a point where $f'=0$, the reflected tangent is vertical and the inverse is not differentiable.
+ **Equations and domain:** Two panels. Panel (a): $f(x)=x^2$ on $0\le x\le1.6$, with the point $(1,1)$ marked and the tangent line of slope $2$; the reflected branch $g(y)=\sqrt y$ on $0\le y\le1.6$ with the reflected tangent of slope $1/2$. Panel (b): $f(x)=x^3$ on $-1.2\le x\le1.2$ with the point $(0,0)$ marked and the horizontal tangent; the inverse $g(y)=y^{1/3}$ with the vertical tangent at $0$.
+ **Scale and style:** Two side-by-side square panels, equal aspect ratio, with the line $y=x$ dashed in both.
+ **Objects and labels:** Panel (a): axes $x,y$; graph of $f$ and graph of $g$ in different colours; the point $(1,1)$; tangent lines with slope labels "$2$" and "$1/2$". Panel (b): axes $x,y$; graph of $x^3$ and its inverse; the origin marked; the horizontal tangent of $f$ and the vertical tangent of $g$ drawn dashed, with the label "not differentiable at $0$".
+ **Shading and visibility:** No region shading; graphs and tangents in distinct colours; the diagonal thin and dashed.
+ **Orientation:** Standard Cartesian orientation, equal scales so that the reflection is visually exact.
+ **Coordinates and parameters:** Panel (a) ticks at $0$ and $1$; panel (b) ticks at $-1$, $0$, $1$.
+ **Alt text:** "Two panels showing a graph and its inverse reflected across the line y equals x: for x squared at (1,1) the tangent slopes are 2 and one half, while for x cubed at the origin the inverse has a vertical tangent."
