# Figure briefs — Multivariable Extrema and Saddle Points

Article: `multivariable-calculus/multivariable-extrema-and-saddle-points.md`
Batch: `20261126T222013Z-01`
Order: F1, F2, F3 (reading order)

## F1 — The saddle surface

+ **Target heading:** "Critical points".
+ **Insertion anchor:** after the paragraph ending "along the $y$-axis it falls." Insert immediately before the paragraph "Fermat's theorem shows that differentiability moves every interior local extremum into the list of critical points."
+ **Mathematical claim:** The graph of $z=x^2-y^2$ has a critical point at the origin that is neither a maximum nor a minimum: the $x$-section is an upward parabola and the $y$-section is a downward parabola.
+ **Equations and domain:** $z=x^2-y^2$ for $-1.5\le x\le1.5$, $-1.5\le y\le1.5$, with the surface drawn as a smooth translucent sheet.
+ **Scale and style:** Three-dimensional axonometric view, true relative scales in $x$ and $y$, vertical scale compressed if needed to fit the frame; schematic but quantitatively correct traces.
+ **Objects and labels:** The surface; the origin marked $O$ and labelled "saddle point"; the trace in the plane $y=0$, drawn as a solid parabola opening upward, labelled $z=x^2$; the trace in the plane $x=0$, drawn as a solid parabola opening downward, labelled $z=-y^2$; the $x$, $y$ and $z$ axes with arrowheads.
+ **Shading and visibility:** Shade the two traces in distinct colours; keep the surface light enough that both traces remain visible. Hidden parts of the surface may be rendered with reduced opacity, but the two traces must be fully visible. No drop shadows or decorative gradients.
+ **Orientation:** The $z$-axis vertical, the $x$-axis to the right and slightly toward the viewer, the $y$-axis into the page and to the left. View from slightly above the $xy$-plane so both parabolic traces read clearly.
+ **Coordinates and parameters:** Mark the origin only; no arbitrary tick labels beyond $-1$, $0$, $1$ on each axis.
+ **Alt text:** "Graph of z equals x squared minus y squared, with an upward parabola in the plane y equals zero and a downward parabola in the plane x equals zero meeting at the saddle point at the origin."

## F2 — Contour map of a cubic with a minimum and a saddle

+ **Target heading:** "A worked example".
+ **Insertion anchor:** after the sentence "The example also shows why both critical points must be examined. The gradient vanishes at both, but the Hessian assigns them different characters." Insert before the heading "When the determinant vanishes".
+ **Mathematical claim:** The level curves of $f(x,y)=x^3+y^3-3xy$ show a saddle at $(0,0)$ and a local minimum at $(1,1)$; the level curve through the saddle crosses itself, while the level curves around $(1,1)$ are closed.
+ **Equations and domain:** $f(x,y)=x^3+y^3-3xy$ on $-1.8\le x\le2.4$, $-1.8\le y\le2.4$. Level values chosen symmetrically around the critical values $0$ and $-1$, for example $c=-3,-2,-1,-0.5,0,0.5,1,2,3,5$.
+ **Scale and style:** Two-dimensional contour plot with equal aspect ratio; thin level curves; a small marker at each critical point.
+ **Objects and labels:** The two critical points marked and labelled "$(0,0)$ saddle" and "$(1,1)$ minimum"; the self-intersecting level curve $f=0$ drawn slightly thicker; a few level curves labelled with their $c$ values; axes with arrowheads.
+ **Shading and visibility:** Use a single colour for level curves, with the $f=0$ curve in a contrasting colour. Mark the minimum with a filled dot and the saddle with an open dot. Do not shade regions.
+ **Orientation:** Standard Cartesian orientation, $x$ horizontal to the right, $y$ vertical upward.
+ **Coordinates and parameters:** Label the ticks $-1$, $0$, $1$, $2$ on both axes; mark the critical points at their exact coordinates.
+ **Alt text:** "Contour map of x cubed plus y cubed minus 3 x y, showing a self-crossing level curve at the saddle point at the origin and closed level curves around the local minimum at (1,1)."

## F3 — Degenerate critical points

+ **Target heading:** "When the determinant vanishes".
+ **Insertion anchor:** after the table and before the paragraph "For $x^4+y^4$, the function is non-negative and vanishes only at the origin". Insert a single figure with four panels.
+ **Mathematical claim:** A zero or semidefinite Hessian does not determine the character of a critical point: the four functions $x^4+y^4$, $-x^4-y^4$, $x^4-y^4$ and $x^2+y^3$ all have a critical point at the origin with a degenerate Hessian, but they are respectively a minimum, a maximum, a saddle and a saddle.
+ **Equations and domain:** Four square panels on $-1.2\le x,y\le1.2$. Panel (a): $z=x^4+y^4$; panel (b): $z=-x^4-y^4$; panel (c): $z=x^4-y^4$; panel (d): $z=x^2+y^3$.
+ **Scale and style:** A $2\times2$ grid of small three-dimensional surface plots, all with the same axis orientation and the same vertical scale where possible; schematic but correct in sign and qualitative shape.
+ **Objects and labels:** Each panel labelled (a), (b), (c), (d) and titled with its formula; the origin marked in each panel; a short caption inside or below each panel: "minimum", "maximum", "saddle", "saddle". The $x$ and $y$ axes visible; the $z$-axis may be omitted to reduce clutter if the orientation is clear.
+ **Shading and visibility:** Light grey surface with a thin wireframe or contour overlay to reveal the shape; no colour gradients. In panel (d), make the cubic rise in $y$ and the parabolic rise in $x$ visible.
+ **Orientation:** Same viewpoint in all four panels, looking from slightly above and to the side, so that up and down are visually comparable.
+ **Coordinates and parameters:** No numeric tick labels; the origin is the only marked point. State in the caption that all four Hessians at the origin have determinant zero.
+ **Alt text:** "Four small surface plots: x to the fourth plus y to the fourth has a minimum at the origin, its negative has a maximum, x to the fourth minus y to the fourth has a saddle, and x squared plus y cubed also has a saddle, although all four Hessians are degenerate at the origin."
