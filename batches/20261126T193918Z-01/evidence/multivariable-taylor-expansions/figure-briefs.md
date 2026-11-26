# Figure briefs — Multivariable Taylor Expansions

Article: `multivariable-calculus/multivariable-taylor-expansions.md`
Batch: `20261126T193918Z-01`
Prepared by: Writer. Illustrator inserts final image links; this file contains no SVG source.

## F1 — Tangent plane and quadratic approximation

+ Target heading: `## The second-order expansion`
+ Insertion anchor (exact sentence, insert after it): `The factor $2$ in the mixed term appears because the two mixed derivatives are equal, so the entries $(1,2)$ and $(2,1)$ of the Hessian contribute identical terms.`
+ Mathematical claim: at a point $a$, the first-order Taylor polynomial is the tangent plane, while the second-order polynomial has the same value, the same gradient and the same Hessian, so it follows the curvature of the surface to second order.
+ Equations and domain: a smooth $f(x,y)$ near $a=(x_0,y_0)$; $P_{a,1}(x,y)=f(a)+f_x(a)(x-x_0)+f_y(a)(y-y_0)$; $P_{a,2}=P_{a,1}+\tfrac12\bigl(f_{xx}(a)(x-x_0)^2+2f_{xy}(a)(x-x_0)(y-y_0)+f_{yy}(a)(y-y_0)^2\bigr)$.
+ Scale: 3D schematic, not to scale; one surface and two approximating surfaces near one point.
+ Objects and labels: the graph of $f$ as a curved sheet; the tangent plane as a flat translucent plane; the quadratic approximation as a shallow paraboloid; the common point $P=(x_0,y_0,f(a))$; labels $P_{a,1}$ and $P_{a,2}$.
+ Shading/visibility: the surface in a neutral colour, the plane in cool blue, the paraboloid in warm orange with transparency; hidden lines dashed; a small vertical segment at a nearby test point indicating the error of the linear approximation and the smaller error of the quadratic one.
+ Orientation: standard right-handed axes; a viewing angle that separates the plane and the paraboloid without hiding the contact point.
+ Alt text: "A surface with its tangent plane and its second-order Taylor paraboloid, both touching at the same point; the paraboloid follows the surface curvature more closely."

## F2 — Three quadratic forms at a critical point

+ Target heading: `## Consequences and related notions`
+ Insertion anchor (exact sentence, insert after it): `if $H_f(a)$ is singular, the second-order term is inconclusive and higher-order terms decide.`
+ Mathematical claim: the definiteness of the Hessian determines whether a critical point is a local minimum, a local maximum or a saddle.
+ Equations and domain: the model quadratic forms $q(x,y)=x^2+y^2$ (positive definite), $q(x,y)=-x^2-y^2$ (negative definite), $q(x,y)=x^2-y^2$ (indefinite), with the origin as the critical point.
+ Scale: schematic, three equal square panels in one row, not to scale.
+ Objects and labels: in each panel, level curves of the quadratic form and a small local surface inset; label the panels "positive definite: local minimum", "negative definite: local maximum", "indefinite: saddle"; mark the origin in each.
+ Shading/visibility: level curves in one colour, with arrows indicating increase; the saddle panel must show the two crossing directions clearly; no shading that obscures the level sets.
+ Orientation: $x$ horizontal, $y$ vertical in each panel; consistent scaling across panels so that the three shapes are comparable.
+ Alt text: "Level curves of x^2+y^2, -x^2-y^2 and x^2-y^2, showing a minimum, a maximum and a saddle at the origin."

## F3 — A flat bump with a zero Taylor series

+ Target heading: `## When the Taylor series does not represent the function`
+ Insertion anchor (exact sentence, insert after it): `Smoothness alone does not imply real analyticity in several variables, just as in one variable.`
+ Mathematical claim: $f(x,y)=e^{-1/(x^2+y^2)}$ for $(x,y)\neq(0,0)$ and $f(0,0)=0$ has every partial derivative zero at the origin, so all its Taylor polynomials there vanish, yet $f$ is positive away from the origin.
+ Equations and domain: the displayed piecewise function; a cross-section along any line through the origin reduces to $e^{-1/t^2}$.
+ Scale: schematic, two panels. Left: a 3D graph of the bump with the plane $z=0$ as the would-be Taylor approximation. Right: the one-variable cross-section $e^{-1/t^2}$ against $t$, with the horizontal axis $z=0$ as its Taylor polynomial.
+ Objects and labels: the bump peaked at the origin or, if the peak is too steep for the chosen scale, truncated with a note; the zero plane; the cross-section curve; labels $f(x,y)$, $z=0$, $t$, $e^{-1/t^2}$.
+ Shading/visibility: the bump in a solid colour above a translucent zero plane; the cross-section curve with the flat tangent at $t=0$ emphasised; indicate that all derivatives at the origin vanish.
+ Orientation: standard axes; the vertical scale may be exaggerated, and the exaggeration should be stated in the caption rather than drawn to scale.
+ Alt text: "A positive bump e^{-1/(x^2+y^2)} above the plane z=0, whose Taylor polynomial at the origin is identically zero."
