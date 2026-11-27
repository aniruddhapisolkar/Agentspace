# Figure briefs — Line Integrals

Article: `multivariable-calculus/line-integrals.md`
Batch: `20261127T134100Z-01`

## F1 — Scalar and vector line integrals on one curve

+ Target heading: "The vector line integral"
+ Insertion anchor: after "The right side is a scalar line integral of the tangential component, and it makes the orientation dependence explicit: reversing the curve replaces $\mathbf{T}$ by $-\mathbf{T}.$"
+ Mathematical claim: the vector line integral sums only the tangential component $\mathbf{F}\cdot\mathbf{T},$ weighted by $ds;$ a normal component contributes nothing.
+ Objects: a smooth oriented curve $C$ with a point $P;$ a field vector $\mathbf{F}$ at $P$ decomposed into a tangential component $(\mathbf{F}\cdot\mathbf{T})\mathbf{T}$ and a normal component; a short arc element $ds$ with unit tangent $\mathbf{T}.$
+ Labels: $C,$ $P,$ $\mathbf{T},$ $\mathbf{F},$ $\mathbf{F}\cdot\mathbf{T},$ $ds,$ and a right angle between the tangent and normal components.
+ Construction: draw the decomposition as a right triangle based at $P.$ Show two nearby points with different field vectors to indicate that the integrand varies along the curve.
+ Distinction: the tangential projection is signed; if $\mathbf{F}$ points against $\mathbf{T},$ the contribution is negative. Include one arrow pointing backward on a second highlighted arc.
+ Shading: none; use one colour for $\mathbf{F}$ and a muted colour for its tangential projection.
+ Alt text: "A vector field at a point on a curve resolved into tangential and normal components, with the tangential component weighted by arc length."

## F2 — Two paths with the same endpoints and different integrals

+ Target heading: "A path-dependent example"
+ Insertion anchor: after "The two curves have the same endpoints, but the integrals differ. The field is therefore not conservative on $\mathbb{R}^2,$ and the integral depends on the path."
+ Mathematical claim: for $\mathbf{F}=\langle x^2,xy\rangle,$ the parabola $y=x^2$ from $(0,0)$ to $(1,1)$ gives $11/15,$ while the straight segment gives $2/3.$
+ Objects: the points $(0,0)$ and $(1,1);$ the parabolic arc $y=x^2;$ the straight segment $y=x;$ several sample arrows of $\mathbf{F}$ along each path; a label with each integral.
+ Labels: $C_1:y=x^2,$ $C_2:y=x,$ $(1,1),$ $\int_{C_1}\mathbf{F}\cdot d\mathbf{r}=11/15,$ $\int_{C_2}\mathbf{F}\cdot d\mathbf{r}=2/3.$
+ Construction: draw both paths between the same two marked points, with arrows on each path indicating the common orientation. The field arrows should be tangent-ish near the start and more horizontal near the end, but the figure must not imply that the field is tangent everywhere.
+ Distinction: the two paths must share endpoints exactly; the difference in values is the point, not a drawing error.
+ Shading: light tint under each path in different colours; no fill between them.
+ Alt text: "A parabola and a straight segment joining the same two points, labelled with different line integrals of the same field."

## F3 — A conservative field, level curves and path independence

+ Target heading: "The fundamental theorem for line integrals"
+ Insertion anchor: after "The potential removes the path dependence entirely."
+ Mathematical claim: for $\mathbf{F}=\nabla f,$ the integral along any path from $A$ to $B$ equals $f(B)-f(A),$ so two paths with the same endpoints give the same value.
+ Objects: level curves $f=c_1,c_2,c_3$ of a potential; two different paths from $A$ on $f=c_1$ to $B$ on $f=c_3;$ gradient arrows crossing the level curves orthogonally; labels $f(A)$ and $f(B).$
+ Labels: $A,$ $B,$ $f(A),$ $f(B),$ $f(B)-f(A),$ and two paths $C_1,$ $C_2.$
+ Construction: draw the paths as curves that stay within the region and do not cross; the gradient arrows should point from lower to higher level. Mark that both paths start on the same level curve and end on the same level curve.
+ Distinction: the field is conservative, so the figure should not suggest that the integral depends on the path length. The level curves do the explanatory work.
+ Shading: light tint between successive level curves to suggest the potential's increase.
+ Alt text: "Two paths between the same two level curves of a potential, with gradient arrows crossing the curves orthogonally."
