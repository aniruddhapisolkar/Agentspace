# Figure briefs — Conservative Vector Fields

Article: `multivariable-calculus/conservative-vector-fields.md`
Batch: `20261127T144139Z-01`
Figures: F1–F3

All three figures are two-dimensional schematic diagrams. They use the house monochrome line style: black strokes, white or light-grey fills, no gradients, no colour dependence. Text labels are set in the same sans-serif as the article figures. Each figure carries one mathematical idea only.

## F1 — Gradient arrows crossing level curves

+ Target heading: `## Potentials are unique up to a constant`
+ Insertion anchor: the sentence `A topographic map with its steepest-ascent arrows is the two-dimensional picture.`
+ Mathematical claim: for $f(x,y)=x^2+2y^2,$ the level curves $f=c$ are ellipses, and $\nabla f=\langle2x,4y\rangle$ is orthogonal to the level curve through each point; the arrow length grows where the ellipses are closer.
+ Equations and domain: $f(x,y)=x^2+2y^2$; level curves at $c=1,2,3,4$; arrows drawn at eight points on the ellipse $c=2$ and at four points on $c=4.$
+ Scale: schematic, equal axis scaling so that right angles appear as right angles. The $x$ and $y$ axes are labelled with tick marks but no numerical grid.
+ Objects and labels: four nested ellipses centred at the origin; one representative point $P$ on the second ellipse with the position vector omitted; gradient arrow at $P$ labelled $\nabla f(P)$; a short tangent segment to the level curve at $P$ labelled $T$; right-angle marker between the arrow and the tangent.
+ Shading and visibility: level curves solid black, gradient arrows solid black with filled arrowheads, tangent segment dashed. No shading.
+ Orientation: all gradient arrows point away from the origin, toward increasing $f.$
+ Alt text: `Elliptical level curves with gradient arrows crossing them at right angles, the arrows longer where the curves are closer together.`

## F2 — Two paths with the same potential difference

+ Target heading: `## Path independence`
+ Insertion anchor: the sentence `For a piecewise smooth curve the argument is applied to each smooth piece, and the values at the intermediate points cancel.`
+ Mathematical claim: for a conservative field, the line integral along either path from $A$ to $B$ equals $f(B)-f(A),$ so the two paths give the same value even though their lengths and shapes differ.
+ Equations and domain: a schematic potential with three level curves $f=c_1<c_2<c_3$; path $C_1$ crosses them once each in order, path $C_2$ crosses them once each in order; both run from $A$ on $c_1$ to $B$ on $c_3.$
+ Scale: schematic, not to scale. The two paths are drawn with comparable visual weight; $C_1$ is a gentle arc above $C_2,$ which dips below before rising.
+ Objects and labels: points $A$ and $B$; paths $C_1$ and $C_2$ with arrowheads at $B$; level curves labelled $f=c_1,$ $f=c_2,$ $f=c_3$; a small annotation $\int_{C_1}\mathbf{F}\cdot d\mathbf{r}=\int_{C_2}\mathbf{F}\cdot d\mathbf{r}=f(B)-f(A).$
+ Shading and visibility: level curves thin solid grey; paths solid black, distinguished by one being slightly thicker; no fill.
+ Orientation: both paths oriented from $A$ to $B.$
+ Alt text: `Two differently shaped paths from A to B crossing the same three level curves, annotated with equal line integrals.`

## F3 — Zero curl with nonzero circulation

+ Target heading: `## The punctured plane`
+ Insertion anchor: the sentence `The integral around a closed curve is nonzero, so the field is not conservative on the punctured plane.`
+ Mathematical claim: the field $\mathbf{F}=\langle-y,x\rangle/(x^2+y^2)$ has zero scalar curl on $\mathbb{R}^2\setminus\{(0,0)\},$ yet its circulation around the unit circle is $2\pi$; the excluded origin is the obstruction.
+ Equations and domain: $D=\mathbb{R}^2\setminus\{(0,0)\};$ field arrows on two circles of radius $1$ and $2;$ the unit circle oriented counterclockwise.
+ Scale: schematic with equal axis scaling. The hole at the origin is marked but not drawn to physical scale.
+ Objects and labels: origin marked with a small open circle and label $O$ (excluded); unit circle with arrowhead and label $C;$ several tangent field arrows on both circles, all counterclockwise; a short note $\operatorname{curl}\mathbf{F}=0$ on $D$ and $\oint_C\mathbf{F}\cdot d\mathbf{r}=2\pi.$
+ Shading and visibility: excluded point as an open circle; field arrows solid black; the loop $C$ thicker; a light grey annulus between the two circles may indicate the domain, with the hole left white.
+ Orientation: field arrows and $C$ both counterclockwise; the right-hand rule would put the positive normal out of the page.
+ Alt text: `A counterclockwise circulating field around a missing origin, with a closed loop encircling the hole and a note that the curl vanishes but the circulation is 2 pi.`
