# Figure briefs — Fundamental Theorem for Line Integrals

Article: `multivariable-calculus/fundamental-theorem-for-line-integrals.md`
Batch: `20261127T144139Z-01`
Figures: F1–F3

House monochrome style: black strokes on white, light-grey fills where shading is needed, no colour dependence. All figures are schematic and carry one claim each.

## F1 — The integral as an endpoint difference

+ Target heading: `## The theorem`
+ Insertion anchor: the sentence `The potential plays the role of an antiderivative, and the endpoints play the role of the limits of integration.`
+ Mathematical claim: along an oriented curve from $A$ to $B,$ the integral of $\nabla f$ accumulates the change in $f,$ so its value is $f(B)-f(A)$ and not the length of the curve.
+ Equations and domain: a smooth curve in the plane from $A$ on the level set $f=c_1$ to $B$ on $f=c_3,$ crossing $f=c_2$ once; the curve is not a gradient line, so it crosses the level sets obliquely.
+ Scale: schematic, equal axis scaling. The curve is drawn with two bends and no self-intersection.
+ Objects and labels: points $A$ and $B$; three level curves labelled $f=c_1<c_2<c_3$; the curve $C$ with an arrowhead at $B$; a tangent vector $\mathbf{r}'(t)$ and a gradient arrow $\nabla f$ at one interior point, with the projection of $\nabla f$ onto the tangent marked; an annotation $\int_C\nabla f\cdot d\mathbf{r}=f(B)-f(A).$
+ Shading and visibility: level curves thin grey; curve thick black; tangent dashed; gradient arrow solid with a small right-angle mark to the level curve.
+ Orientation: $C$ from $A$ to $B$; gradient arrows point toward increasing $f.$
+ Alt text: `An oriented curve from A to B crossing three level curves of a potential, with the tangent and gradient at one point and the endpoint-difference formula.`

## F2 — Telescoping over a piecewise curve

+ Target heading: `## Proof`
+ Insertion anchor: the sentence `The derivative may fail at the corner, but the integral is unaffected.`
+ Mathematical claim: splitting a piecewise smooth curve at $P_1,\ldots,P_{n-1}$ gives a sum of potential differences in which every interior value cancels, leaving $f(B)-f(A).$
+ Equations and domain: a polygonal curve $P_0\to P_1\to P_2\to P_3$ with three straight pieces and two corners; labels $P_0=A,$ $P_3=B.$
+ Scale: schematic, not to scale; corners are clearly visible and not smoothed.
+ Objects and labels: the four points; the three segments with arrowheads; next to each segment the corresponding difference $f(P_i)-f(P_{i-1})$; a bracket showing the cancellation of $f(P_1)$ and $f(P_2)$; final line $f(B)-f(A).$
+ Shading and visibility: segments solid black; points filled black dots; cancellation indicated by thin grey strike-throughs or paired arrows, not by colour.
+ Orientation: all segments oriented from $P_0$ toward $P_3.$
+ Alt text: `A three-segment polygonal path with intermediate points, annotated with potential differences that cancel in pairs to leave f of B minus f of A.`

## F3 — Two semicircles with opposite integrals

+ Target heading: `## A field that is not a gradient`
+ Insertion anchor: the sentence `The two paths have the same endpoints and different integrals.`
+ Mathematical claim: for $\mathbf{F}=\langle-y,x\rangle,$ the upper semicircle from $(1,0)$ to $(-1,0)$ gives $\pi$ and the lower semicircle gives $-\pi,$ so the integral is path-dependent.
+ Equations and domain: unit circle centred at the origin; $A=(1,0),$ $B=(-1,0)$; upper arc $C_+$ traversed counterclockwise; lower arc $C_-$ traversed clockwise from $A$ to $B.$
+ Scale: equal axis scaling, unit circle drawn as a circle. Axes shown with tick marks at $\pm1.$
+ Objects and labels: $A$ and $B$; $C_+$ with arrowhead near the top pointing left; $C_-$ with arrowhead near the bottom pointing right; several field arrows on both arcs, all counterclockwise; annotations $\int_{C_+}=\pi$ and $\int_{C_-}=-\pi.$
+ Shading and visibility: upper arc thick black, lower arc thick black but dashed at the midpoint to distinguish the two labels; field arrows thin; no fill.
+ Orientation: field arrows counterclockwise; $C_+$ counterclockwise; $C_-$ clockwise from $A$ to $B.$
+ Alt text: `Upper and lower semicircles between (1,0) and (-1,0), with counterclockwise field arrows and integrals pi and minus pi.`
