# Research evidence — Vector Fields

Batch: `20261127T134100Z-01`
Slug: `vector-fields`
Article: `multivariable-calculus/vector-fields.md`
Category: `multivariable-calculus` (provisional)
Research date: 2026-11-27

## Coverage check

Upstream `antoniolupetti/algebrica` was searched by filename and body text for "vector field", "gradient field", "conservative field", "potential function", "field line", "streamline" and "radial field".

+ No upstream article defines vector fields, plots them, or treats conservative fields and potentials.
+ `derivatives/partial-derivatives.md` defines the gradient and the Jacobian but does not develop the gradient as a field, field lines, or path-independence.
+ `vectors-and-matrices/vectors.md` supplies vector notation and operations only.
+ No article treats the rotation field, the inverse-square field or the punctured-plane counterexample.

Conclusion: not a duplicate. The gradient definition is linked as a prerequisite. Open issues and pull requests were not inspected; no claim is made about planned upstream work.

## Scope and reader contract

After reading the article, the reader can:

+ define a vector field on a plane or space domain and identify its component functions;
+ distinguish a vector field from a vector-valued function of one parameter;
+ read a true-length plot and a direction plot;
+ recognise constant, radial, rotational and gradient fields;
+ test whether a planar field is a gradient field and find a potential by integration;
+ explain why the line integral of a conservative field is path-independent;
+ write and interpret the differential equations for field lines;
+ state the curl test for conservative fields and explain why simple connectedness is needed;
+ reproduce the punctured-plane field with zero curl and nonzero circulation;
+ compute divergence and scalar curl of a polynomial field.

Assumed prerequisites: [vectors](../vectors/), [partial derivatives](../partial-derivatives/), the gradient, and one-variable integration. Exclusions: the general Helmholtz decomposition and its regularity hypotheses, surface integrals, the divergence theorem and Stokes' theorem beyond statements, and the qualitative classification of equilibria.

## Sources consulted

1. OpenStax, *Calculus Volume 3*, §6.1 "Vector Fields".
   URL: https://openstax.org/books/calculus-volume-3/pages/6-1-vector-fields
   Accessed: 2026-11-27. Full text read.
   Supports: the definition of a vector field in $\mathbb{R}^2$ and $\mathbb{R}^3,$ the domain, radial and rotational fields, unit vector fields, gradient fields, level curves and the definition of a conservative field with potential function.
   Use: the definition, the radial and rotational examples, the gradient-field discussion and the conservative-field definition.

2. Paul Dawkins, *Paul's Online Math Notes*, Calculus III, "Vector Fields".
   URL: https://tutorial.math.lamar.edu/Classes/CalcIII/VectorFields.aspx
   Accessed: 2026-11-27. Full text read.
   Supports: the definition, sketching by evaluating sample points, gradient vector fields, orthogonality of gradient arrows to contours, and the conservative-field definition with the example $\langle y,x\rangle=\nabla(xy)$ and the non-example $\langle-y,x\rangle.$
   Use: independent confirmation of the example/non-example pair and the level-curve relation.

3. Algebrica upstream `derivatives/partial-derivatives.md`.
   URL: https://algebrica.org/partial-derivatives/
   Accessed through the upstream clone, 2026-11-27.
   Supports: the gradient notation and the mixed-partial equality used in the curl test.
   Use: notational consistency and the internal link.

## Definitions and conventions selected

+ Domain $D\subseteq\mathbb{R}^2$ or $\mathbb{R}^3$; field $\mathbf{F}=\langle P,Q\rangle$ or $\langle P,Q,R\rangle.$
+ Component functions are scalar functions on $D.$
+ Unit field $\widehat{\mathbf{F}}=\mathbf{F}/\lVert\mathbf{F}\rVert$ where $\mathbf{F}\neq\mathbf{0}.$
+ Conservative field: $\mathbf{F}=\nabla f$ on an open connected domain; $f$ is a potential.
+ Scalar curl in the plane: $\partial_x Q-\partial_y P.$
+ Field line: $\mathbf{r}'(t)=\lambda(t)\mathbf{F}(\mathbf{r}(t))$ with $\lambda>0.$
+ British spelling: "recognise", "centre", "behaviour"; "nonnegative" without hyphen.

## Mathematical claims and justification

+ **Definition and domain.** A vector field is a function whose codomain is $\mathbb{R}^2$ or $\mathbb{R}^3.$ The domain is part of the data. The field $\langle x,y\rangle/(x^2+y^2)$ is undefined at the origin; removing that point changes the topology of the domain.
+ **Vector field versus vector-valued function.** The domain of a vector-valued function is an interval of parameters; the domain of a vector field is a region of points. The codomains coincide, which is why the notation can look identical.
+ **Radial field.** $\mathbf{F}=g(r)\langle x,y\rangle$ is parallel to the position vector at every point, so its field lines are rays from the origin. The inverse-square field $\mathbf{r}/r^3$ is the three-dimensional case with $g(r)=1/r^3.$
+ **Rotational field (6).** $\langle-y,x\rangle$ is perpendicular to $\langle x,y\rangle$ and has magnitude $r,$ so the arrows circulate counterclockwise and grow linearly. Along the circle of radius $R,$ $\mathbf{r}'=\langle-R\sin t,R\cos t\rangle=\mathbf{F}(\mathbf{r}),$ so the circles are field lines with unit parameter speed.
+ **Non-conservative proof for (6).** If $\nabla f=\langle-y,x\rangle,$ then $f_x=-y$ gives $f=-xy+\phi(y).$ Then $f_y=-x+\phi'(y)=x,$ so $\phi'(y)=2x,$ impossible because the left side is independent of $x.$ This is a complete obstruction on any domain containing the point; in fact the curl is $2\neq0$ everywhere.
+ **Potential example.** For $f=x^2y+y^3,$ $\nabla f=\langle2xy,x^2+3y^2\rangle.$ At $(1,2)$ this is $\langle4,13\rangle.$
+ **Path independence (9)–(10).** Chain rule along the curve, then the fundamental theorem of calculus. This is the fundamental theorem for line integrals; the full statement and examples are in the line-integrals entry.
+ **Converse.** Path-independence plus continuity gives a potential by integrating from a fixed base point. The difference-quotient argument is standard and is only summarized, not reproduced line by line.
+ **Gradient orthogonal to level curves.** If $\mathbf{r}(t)$ lies on $f=c,$ then $f(\mathbf{r}(t))$ is constant, so $\nabla f\cdot\mathbf{r}'=0.$ This requires $\nabla f\neq\mathbf{0}$ for a nonzero normal; at critical points the level set may be singular.
+ **Field-line equations (12)–(13).** Eliminating the parameter from $\mathbf{r}'=\lambda\mathbf{F}$ gives $dy/dx=Q/P$ in the plane and the symmetric system in space, valid where the denominators do not vanish.
+ **Curl test.** For $C^2$ $f,$ equality of mixed partials gives $\partial_x Q=\partial_y P,$ so a gradient field has zero scalar curl. A nonzero curl therefore proves that no potential exists. The converse requires simple connectedness; the punctured plane is the standard counterexample.
+ **Punctured-plane field (16).** With $P=-y/r^2$ and $Q=x/r^2,$ $\partial_x P=2xy/r^4$ and $\partial_y Q=-2xy/r^4,$ so the divergence is zero; $\partial_x Q=(r^2-2x^2)/r^4$ and $\partial_y P=(-r^2+2y^2)/r^4,$ so the scalar curl is zero. On the unit circle, $\mathbf{F}\cdot\mathbf{r}'=1,$ hence the integral is $2\pi.$ The field equals $\nabla\theta$ locally, where $\theta$ is a polar angle, but no single-valued branch of $\theta$ exists on the punctured plane.
+ **Inverse-square field.** $\nabla(-1/r)=\mathbf{r}/r^3.$ Its divergence is $3/r^3-3r^2/r^5=0$ away from the origin. Since $\mathbb{R}^3\setminus\{0\}$ is simply connected, the field is conservative there; the singularity carries the flux.
+ **Polynomial example.** $\mathbf{F}=\langle x^2-y,x+y^2\rangle$ has divergence $2x+2y$ and scalar curl $2.$ At $(1,2)$ these are $6$ and $2.$
+ **Helmholtz decomposition (19).** The rotated gradient $\langle-\psi_y,\psi_x\rangle$ is divergence-free and the gradient is curl-free. The formula is stated as an orientation device; no existence theorem for general domains is claimed.

## Independent checks

Python 3 finite-difference script (ad hoc, outside the repository):

+ field (16) at $(1,0.3),$ $(0.4,-0.8)$ and $(2,1)$: scalar curl $-8.3\times10^{-11},$ $-5.6\times10^{-11},$ $-4.2\times10^{-11}$ and divergence $0,$ $-2.8\times10^{-11},$ $-1.4\times10^{-11},$ all zero to numerical precision;
+ unit-circle integral of (16) by midpoint rule with $200000$ intervals: $6.283185307165095$ against $2\pi=6.283185307179586$;
+ potential example at $(1,2)$: $\langle4,13\rangle$;
+ polynomial example at $(1,2)$: divergence $6,$ scalar curl $2.$

All checks passed. The non-conservation proof for $\langle-y,x\rangle$ is exact, not numerical.

## Limitations

+ No LaTeX renderer, Pandoc or TeX installation is available (`pandoc` and `pdflatex` not found); the Markdown was checked structurally but not rendered.
+ The proposed route `https://algebrica.org/vector-fields/` is not known to be live.
+ The Helmholtz decomposition is stated without proof and without precise decay hypotheses; the article explicitly says it is orientation only.
+ The qualitative classification of equilibria is mentioned but not developed.
+ Open issues and pull requests in the upstream repository were not inspected.
+ Links to sibling batch articles are unpublished dependencies until this batch is merged.
