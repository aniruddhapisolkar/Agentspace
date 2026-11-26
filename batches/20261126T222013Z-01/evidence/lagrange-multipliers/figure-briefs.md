# Figure briefs — Lagrange Multipliers

Article: `multivariable-calculus/lagrange-multipliers.md`
Batch: `20261126T222013Z-01`
Order: F1, F2, F3 (reading order)

## F1 — Tangency of a level curve and the constraint

+ **Target heading:** "Tangency of level sets".
+ **Insertion anchor:** after the paragraph ending "The tangency picture is a guide, not a proof." Insert before the heading "## The multiplier theorem".
+ **Mathematical claim:** At a constrained extremum, the level curve of $f$ through $p$ is tangent to the constraint curve, so the gradients $\nabla f(p)$ and $\nabla g(p)$ are parallel.
+ **Equations and domain:** Use the circle example $f(x,y)=xy$ and $g(x,y)=x^2+y^2-1=0$ on $-1.6\le x,y\le1.6$. Draw several level curves $xy=c$ for $c=-0.5,-0.25,0,0.25,0.5$ and the unit circle. Mark the maximum at $(1/\sqrt2,1/\sqrt2)$ and the minimum at $(1/\sqrt2,-1/\sqrt2)$; optionally mark the other two symmetric candidates with lighter dots.
+ **Scale and style:** Two-dimensional plot with equal aspect ratio; thin smooth level curves; the circle drawn thicker.
+ **Objects and labels:** The unit circle labelled $g=0$; the level curves labelled with their $c$ values; the two extrema marked $p_{\max}$ and $p_{\min}$; at $p_{\max}$, draw the gradient vectors $\nabla f$ and $\nabla g$ as arrows from the point, parallel and in the same direction; at $p_{\min}$, draw them parallel and in opposite directions. Label the arrows.
+ **Shading and visibility:** Use one colour for the level curves of $f$ and a contrasting colour for the circle and the gradient arrows. Do not shade the regions; keep the intersection points visible.
+ **Orientation:** Standard Cartesian orientation, $x$ horizontal, $y$ vertical, equal scales.
+ **Coordinates and parameters:** Mark the origin and the unit tick marks $-1$ and $1$ on both axes; the extrema are at $(\pm1/\sqrt2,\pm1/\sqrt2)$.
+ **Alt text:** "Level curves of x y crossing the unit circle tangentially at the constrained maximum and minimum, with the gradients of the objective and the constraint drawn parallel at those points."

## F2 — A constraint curve lifted onto the objective surface

+ **Target heading:** "A first example".
+ **Insertion anchor:** after the sentence "The maximum is $\frac12$ at the two points with equal signs, and the minimum is $-\frac12$ at the two points with opposite signs." Insert before the heading "## Distance to a plane".
+ **Mathematical claim:** The constrained extrema of $f(x,y)=xy$ on $x^2+y^2=1$ are the highest and lowest points of the curve obtained by lifting the unit circle onto the surface $z=xy$.
+ **Equations and domain:** Surface $z=xy$ over $-1.4\le x,y\le1.4$; the lifted constraint curve $(x,y,xy)$ with $x^2+y^2=1$. Mark the highest points at $(\pm1/\sqrt2,\pm1/\sqrt2,1/2)$ and the lowest at $(\pm1/\sqrt2,\mp1/\sqrt2,-1/2)$.
+ **Scale and style:** Three-dimensional axonometric view; the surface translucent, the lifted curve solid and thick enough to read against the surface.
+ **Objects and labels:** The surface $z=xy$; the lifted circle labelled "constraint $x^2+y^2=1$"; the maximum and minimum points marked and labelled with their values $z=1/2$ and $z=-1/2$; the $x$, $y$ and $z$ axes with arrowheads.
+ **Shading and visibility:** Shade the surface lightly; use a contrasting colour for the lifted curve. Hidden portions of the surface may be transparent, but the entire lifted curve must be visible. No drop shadows.
+ **Orientation:** $z$-axis vertical; view from slightly above the $xy$-plane so that both the surface and the closed curve are visible; the saddle shape of $z=xy$ should be recognisable.
+ **Coordinates and parameters:** Mark $z=1/2$ and $z=-1/2$ on the vertical axis; no dense tick labels.
+ **Alt text:** "The saddle surface z equals x y with the unit circle lifted onto it; the lifted curve reaches its highest points at z equals one half and its lowest points at z equals minus one half."

## F3 — Two constraints and the span of the normals

+ **Target heading:** "Two constraints".
+ **Insertion anchor:** after the sentence "The point found is the orthogonal projection of the origin onto that line, so it is the global minimum." Insert before the heading "## The multiplier as a sensitivity".
+ **Mathematical claim:** With two independent constraints $g_1=0$ and $g_2=0$, the feasible set is their intersection curve, and at a constrained extremum $\nabla f$ lies in the plane spanned by the two constraint normals $\nabla g_1$ and $\nabla g_2$.
+ **Equations and domain:** Use $g_1=x+y+z-1=0$ (a plane) and $g_2=x-y=0$ (a vertical plane) in the box $-0.5\le x,y,z\le1.5$. The intersection is the line $x=y$, $z=1-2x$. Mark the minimiser $(1/3,1/3,1/3)$.
+ **Scale and style:** Three-dimensional schematic with two translucent planes intersecting in a line; true relative orientation, but the planes may be clipped to the box for clarity.
+ **Objects and labels:** Plane $g_1=0$ and plane $g_2=0$ in two light colours; the intersection line drawn solid and labelled "feasible line"; the point $(1/3,1/3,1/3)$ marked; from that point, draw $\nabla f$, $\nabla g_1$ and $\nabla g_2$ as arrows, with $\nabla f$ shown as a linear combination of the other two. Label all three vectors.
+ **Shading and visibility:** Keep both planes translucent so the line and vectors remain visible; use distinct colours for the two normals and a third colour for $\nabla f$. No opaque fills that hide the intersection.
+ **Orientation:** View from a direction that shows both planes and the intersection line clearly; the $z$-axis vertical.
+ **Coordinates and parameters:** Mark the origin and the intercepts $1$ on the axes; no other tick labels. State in the caption that $\nabla f=\frac23\nabla g_1+0\nabla g_2$ at the minimiser, or give the numerical vector relation.
+ **Alt text:** "Two planes intersecting in a line, with the minimising point marked and the gradient of the objective drawn as a combination of the two constraint normals."
