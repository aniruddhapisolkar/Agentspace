# Figure briefs — Vector Fields

Article: `multivariable-calculus/vector-fields.md`
Batch: `20261127T134100Z-01`

## F1 — Radial and rotational fields side by side

+ Target heading: "Standard examples"
+ Insertion anchor: after "The arrows circulate counterclockwise around the origin, and their length grows linearly with the distance from it."
+ Mathematical claim: $\mathbf{F}_{\mathrm{rad}}=\langle x,y\rangle$ points away from the origin along rays, while $\mathbf{F}_{\mathrm{rot}}=\langle-y,x\rangle$ is perpendicular to the position vector and circulates counterclockwise.
+ Objects: two square panels with the same scale. Left: arrows at a grid of points for $\langle x,y\rangle,$ pointing radially outward with length proportional to distance. Right: arrows for $\langle-y,x\rangle,$ tangent to concentric circles and circulating counterclockwise.
+ Labels: $x,$ $y,$ origin $O,$ and the field formulas above each panel.
+ Construction: draw two or three faint concentric circles in the right panel to make the circulation evident; draw two or three faint rays in the left panel.
+ Distinction: both panels drawn to the same arrow-length scale so that magnitudes can be compared. The right field should visibly grow with radius.
+ Shading: none; use one colour for radial and one for rotational.
+ Alt text: "Two vector fields compared: a radial field pointing away from the origin and a rotational field circulating counterclockwise."

## F2 — Gradient field crossing level curves orthogonally

+ Target heading: "Gradient fields and potentials"
+ Insertion anchor: after "A topographic map and its steepest-ascent arrows illustrate the same relation."
+ Mathematical claim: for $f(x,y)=x^2+2y^2,$ the gradient $\nabla f=\langle2x,4y\rangle$ is orthogonal to the level ellipses $x^2+2y^2=c,$ and its magnitude grows as the ellipses become closer.
+ Objects: several level ellipses $x^2+2y^2=c$ for $c=1,2,3,4;$ gradient arrows based at points on two of the ellipses, pointing outward and normal to the ellipse; one arrow decomposed into its normal and tangential components to show the tangential component is zero.
+ Labels: $x,$ $y,$ $f=1,$ $f=2,$ $f=3,$ $\nabla f.$
+ Construction: choose sample points on the ellipses, not on the axes only, so that the orthogonality is visible at a generic point. The arrows should be longer where the ellipses are closer.
+ Distinction: schematic; the ellipses are not circles, which prevents the misleading impression that the gradient is radial in general.
+ Shading: light tint between successive level curves to suggest elevation.
+ Alt text: "Gradient arrows perpendicular to elliptical level curves, growing longer where the curves are closer."

## F3 — Zero curl on a punctured plane with nonzero circulation

+ Target heading: "Conservative fields and the curl test"
+ Insertion anchor: after "The hole at the origin is exactly what prevents the loop from contracting, and the test fails because its hypothesis fails."
+ Mathematical claim: on $\mathbb{R}^2\setminus\{0\},$ the field $\mathbf{F}=\langle-y,x\rangle/(x^2+y^2)$ has zero scalar curl everywhere, yet its integral around the unit circle is $2\pi.$
+ Objects: the punctured plane with the origin marked as a small open circle; sample arrows of $\mathbf{F}$ on two or three concentric circles, tangent and counterclockwise; the unit circle highlighted as the closed path $C$ with an orientation arrow; the origin labelled "hole."
+ Labels: $C,$ $O$ (excluded), $\operatorname{curl}\mathbf{F}=0$ near a sample point, $\oint_C\mathbf{F}\cdot d\mathbf{r}=2\pi.$
+ Construction: draw the arrows with length decreasing like $1/r$ so that the field is visible on both the unit circle and an outer circle. Mark the excluded point with a hollow dot, not a filled one.
+ Distinction: the loop must be drawn as a closed curve that cannot shrink to a point without crossing the hole. Do not shade the interior as if it were part of the domain.
+ Shading: very light grey in the annulus between the two circles; the disk inside the unit circle is part of the domain but the origin is not.
+ Alt text: "A circulating field on the punctured plane, with a closed loop around the excluded origin and zero curl away from the hole."
