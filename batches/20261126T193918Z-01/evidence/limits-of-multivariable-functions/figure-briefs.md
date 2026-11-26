# Figure briefs — Limits of Multivariable Functions

Article: `multivariable-calculus/limits-of-multivariable-functions.md`
Batch: `20261126T193918Z-01`
Prepared by: Writer. Illustrator inserts final image links; this file does not contain SVG source.

## F1 — Two paths, two limits

+ Target heading: `## Approaching a point in several variables`
+ Insertion anchor (exact sentence, insert after it): `The two approaches give different values, $0$ and $1/2$, so no single number can be the limit.`
+ Mathematical claim: for $f(x,y)=xy/(x^2+y^2)$ on $\mathbb{R}^2\setminus\{(0,0)\}$, the path $y=0$ gives $f\to0$ while the path $y=x$ gives $f\to1/2$; hence the limit at the origin does not exist.
+ Equations and domain: $f(x,y)=\dfrac{xy}{x^2+y^2}$, $(x,y)\neq(0,0)$; parametric paths $\gamma_1(t)=(t,0)$ and $\gamma_2(t)=(t,t)$, $t>0$.
+ Scale: schematic, two panels side by side, not to scale.
+ Left panel: the punctured plane near the origin with the two paths drawn as distinct coloured curves; label $\gamma_1$ on the $x$-axis and $\gamma_2$ on the bisector $y=x$; mark the origin as an open point; indicate the approach direction with arrowheads pointing to the origin.
+ Right panel: a schematic graph of the two restricted one-variable functions, $f(\gamma_1(t))=0$ as a horizontal line and $f(\gamma_2(t))=1/2$ as a second horizontal line, with a vertical dashed line at the origin; label the heights $0$ and $1/2$.
+ Shading/visibility: light grey punctured disc in the left panel; the two paths in contrasting solid colours carried consistently into the right panel.
+ Orientation: standard $x$ to the right, $y$ upward in the domain; $t$ to the right and $f$ upward in the right panel.
+ Alt text: "Two approaches to the origin in the domain of f(x,y)=xy/(x^2+y^2): along the x-axis the value is 0, while along the line y=x it is 1/2."

## F2 — The epsilon–delta condition

+ Target heading: `## Definition of limit`
+ Insertion anchor (exact sentence, insert after it): `so the punctured ball is a disc with its centre removed.`
+ Mathematical claim: $\lim_{x\to x_0}f(x)=L$ means that every punctured $\delta$-disc around $x_0$ is mapped into the interval $(L-\varepsilon,L+\varepsilon)$.
+ Equations and domain: $0<\|x-x_0\|<\delta\Rightarrow|f(x)-L|<\varepsilon$; illustrate in $\mathbb{R}^2$ with $x_0=(x_0,y_0)$, $L\in\mathbb{R}$.
+ Scale: schematic cross-section, not to scale; the vertical axis is the value axis.
+ Objects and labels: a punctured disc of radius $\delta$ in the $xy$-plane with centre $x_0$ removed; a point $x$ inside it; the corresponding point $(x,f(x))$ on a curve above; a horizontal band of half-width $\varepsilon$ around $L$; labels $\delta$, $\varepsilon$, $x_0$, $L$, $f(x)$.
+ Shading/visibility: shade the punctured $\delta$-disc and the $\varepsilon$-band in the same light colour, with dashed boundary circles/lines; the excluded centre marked with a small open circle.
+ Orientation: $x$ horizontal, $y$ into the page or vertical in a separate small plane; $z$ vertical. If a full 3D layout is too crowded, use a 2D graph of a one-variable restriction with a shaded $\delta$-interval and an $\varepsilon$-band, and a small inset of the punctured disc.
+ Alt text: "The epsilon-delta definition: every point inside the punctured delta-disc around x0 has its value inside the epsilon-band around L."

## F3 — A ridge along a parabola defeats every line

+ Target heading: `## Proving that a limit does not exist`
+ Insertion anchor (exact sentence, insert after it): `Hence the limit does not exist, even though all linear approaches agree.`
+ Mathematical claim: the surface $z=xy^2/(x^2+y^4)$ tends to $0$ along every line through the origin but tends to $1/2$ along the parabola $x=y^2$, so no tangent limit value exists at the origin.
+ Equations and domain: $z=\dfrac{xy^2}{x^2+y^4}$ for $(x,y)\neq(0,0)$; the parabola $x=y^2$; two representative lines $y=mx$.
+ Scale: 3D schematic with a cut-away near the origin; not to scale.
+ Objects and labels: the surface as a translucent sheet with a pronounced ridge above the parabola $x=y^2$; the parabolic ridge projected onto the $xy$-plane as a dashed curve; two straight lines through the origin projected in another colour; label the ridge height $1/2$ and the flat line limits $0$.
+ Shading/visibility: the ridge highlighted with a warmer colour; hidden parts of the surface dashed or faded; the vertical axis labelled $z$.
+ Orientation: standard right-handed axes, $x$ and $y$ in the horizontal plane, $z$ upward; view from an angle that shows both the ridge and the flat directions. The singularity at the origin should be visible as a pinch, not smoothed away.
+ Alt text: "Surface z=xy^2/(x^2+y^4) with a ridge above the parabola x=y^2 reaching height 1/2, while all straight lines through the origin stay at height 0."
