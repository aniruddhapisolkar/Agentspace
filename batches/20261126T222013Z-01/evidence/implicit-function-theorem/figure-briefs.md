# Figure briefs — Implicit Function Theorem

Article: `multivariable-calculus/implicit-function-theorem.md`
Batch: `20261126T222013Z-01`
Order: F1, F2, F3 (reading order)

## F1 — A circle as a graph, and where it fails

+ **Target heading:** "The scalar case".
+ **Insertion anchor:** after the paragraph ending "namely $x=\sqrt{1-y^2}$." Insert before the heading "## The general statement".
+ **Mathematical claim:** The circle $x^2+y^2=1$ is locally a graph $y=\varphi(x)$ near $(0,1)$, where $F_y\neq0$, but not near $(1,0)$, where $F_y=0$ and the tangent is vertical.
+ **Equations and domain:** The unit circle $x^2+y^2=1$ on $-1.4\le x,y\le1.4$. Two panels sharing the same circle.
+ **Scale and style:** Two side-by-side square panels with equal aspect ratio; the circle drawn as a solid curve; thin coordinate axes.
+ **Objects and labels:** Panel (a): the point $(0,1)$ marked, a short horizontal interval on the $x$-axis around $0$ shaded, the corresponding upper arc highlighted, and the label "$y=\sqrt{1-x^2}$, $F_y=2$". Panel (b): the point $(1,0)$ marked, the vertical tangent drawn as a dashed line, the label "$F_y=0$: no graph over $x$", and arrows indicating that a vertical line just left of $x=1$ meets the circle twice. Both panels should show the full circle for context.
+ **Shading and visibility:** Highlight the locally solved arc in a contrasting colour in panel (a); keep panel (b) unhighlighted except for the tangent and the two intersection dots. No region shading.
+ **Orientation:** Standard Cartesian orientation, equal scales, origin marked in both panels.
+ **Coordinates and parameters:** Tick marks at $-1$, $0$, $1$ on both axes; the marked points are exactly $(0,1)$ and $(1,0)$.
+ **Alt text:** "Two panels of the unit circle: near (0,1) the upper arc is the graph of y equals the square root of 1 minus x squared, while near (1,0) the tangent is vertical and the circle is not a graph over the x-axis."

## F2 — Three ways the hypothesis can fail

+ **Target heading:** "When the hypothesis fails".
+ **Insertion anchor:** after the paragraph ending "but its regularity or uniqueness is not controlled by the linear term." Insert before the heading "## Scope and limitations".
+ **Mathematical claim:** When $F_y(a,b)=0$, the zero set can be an isolated point, a pair of crossing branches, or a cusp; in none of these cases does the equation define a unique differentiable function $y=\varphi(x)$ near the point.
+ **Equations and domain:** Three square panels on $-1.2\le x,y\le1.2$. Panel (a): $F=x^2+y^2$ at $(0,0)$, zero set the single point. Panel (b): $F=x^2-y^2$ at $(0,0)$, zero set $y=\pm x$. Panel (c): $F=x^2-y^3$ at $(0,0)$, zero set $y=x^{2/3}$.
+ **Scale and style:** A row of three panels with equal aspect ratio; zero sets drawn as solid curves or dots; faint coordinate axes in each panel.
+ **Objects and labels:** Each panel labelled (a), (b), (c), with its formula and the condition "$F_y(0,0)=0$". Panel (a): the origin marked with a filled dot and labelled "isolated zero". Panel (b): the two lines labelled $y=x$ and $y=-x$, the origin marked. Panel (c): the cusp curve labelled $y=x^{2/3}$, with a short vertical tangent at the origin drawn dashed.
+ **Shading and visibility:** Use a single colour for the zero sets; make the origin markers clear. No filled regions.
+ **Orientation:** Standard Cartesian orientation, equal scales, origin marked in all panels.
+ **Coordinates and parameters:** Tick marks at $-1$ and $1$ on both axes; the critical point is the origin in every panel.
+ **Alt text:** "Three panels showing failure of the implicit function theorem at the origin: an isolated zero for x squared plus y squared, two crossing lines for x squared minus y squared, and a cusp for x squared minus y cubed."

## F3 — The contraction map

+ **Target heading:** "The contraction proof".
+ **Insertion anchor:** after the proof of the contraction mapping principle, ending "hence $u=v$." Insert before the paragraph "The function $\varphi$ is continuous."
+ **Mathematical claim:** For fixed $x$, the map $G_x(y)=y-F(x,y)$ is a contraction of the interval $[b-\delta,b+\delta]$ into itself; its graph crosses the diagonal at the unique fixed point $\varphi(x)$.
+ **Equations and domain:** A schematic interval on the vertical axis from $b-\delta$ to $b+\delta$, and the same interval on the horizontal axis. Draw the diagonal $y=z$ and a monotone curve $z=G_x(y)$ with slope between $0$ and $1/2$, starting above the diagonal at $y=b-\delta$ and ending below it at $y=b+\delta$, crossing once.
+ **Scale and style:** Two-dimensional schematic, not to numerical scale; the interval endpoints labelled $b-\delta$ and $b+\delta$; the diagonal dashed.
+ **Objects and labels:** The horizontal axis labelled "$y$"; the vertical axis labelled "$z$"; the diagonal labelled "$z=y$"; the curve labelled "$z=G_x(y)$"; the intersection labelled "$\varphi(x)$"; a few cobweb iteration segments from a starting point $y_0$ to $y_1=G_x(y_0)$, then to $y_2=G_x(y_1)$, converging to the fixed point.
+ **Shading and visibility:** The curve and diagonal in distinct colours; the cobweb in a lighter shade; the fixed point marked with a filled dot. No region shading.
+ **Orientation:** Standard Cartesian orientation; the square $[b-\delta,b+\delta]^2$ outlined lightly.
+ **Coordinates and parameters:** No numeric ticks beyond the symbolic endpoints; the diagram is schematic and should be labelled as such in the caption.
+ **Alt text:** "A contraction map on an interval: the graph of G sub x crosses the diagonal once at the fixed point phi of x, and a cobweb iteration converges to that point."
