---
title: Vector Fields
source: https://algebrica.org/vector-fields/
license: CC BY-NC 4.0
tags:
  - conservative-fields
  - field-lines
  - gradient
  - multivariable-calculus
  - potential-function
  - vector-fields
---

## A vector at every point

A vector-valued function of one parameter traces a curve: one vector for each value of the parameter. A vector field assigns a vector to every point of a region. The input is a point of the plane or of space, and the output is a vector attached at that point. This change of domain turns a collection of arrows into a description of a force, a velocity or a gradient over a whole region.

Let $D\subseteq\mathbb{R}^2$ be a set. A vector field on $D$ is a map

$$\mathbf{F}:D\to\mathbb{R}^2$$

which assigns to each point $(x,y)\in D$ a two-dimensional vector $\mathbf{F}(x,y).$ In components,

$$\mathbf{F}(x,y)=P(x,y)\,\mathbf{i}+Q(x,y)\,\mathbf{j}=\langle P(x,y),Q(x,y)\rangle \tag{1}$$

where $P$ and $Q$ are real-valued functions on $D,$ called the component functions. In space, a vector field is a map $\mathbf{F}:D\to\mathbb{R}^3$ with

$$\mathbf{F}(x,y,z)=P(x,y,z)\,\mathbf{i}+Q(x,y,z)\,\mathbf{j}+R(x,y,z)\,\mathbf{k}=\langle P,Q,R\rangle \tag{2}$$

The domain $D$ is part of the definition. The field $\mathbf{F}(x,y)=\langle x,y\rangle$ is defined on all of $\mathbb{R}^2,$ while

$$\mathbf{F}(x,y)=\left\langle\frac{x}{x^2+y^2},\frac{y}{x^2+y^2}\right\rangle$$

is defined only on $\mathbb{R}^2\setminus\{(0,0)\}.$ The missing point is not a cosmetic detail: it changes which loops in the domain can be contracted to a point, and therefore which fields with zero curl are conservative.

A vector field is continuous, differentiable or of class $C^k$ when all its component functions have that property. These notions are defined pointwise, exactly as for scalar functions, because the vector structure adds no new analytic difficulty.

The distinction between a vector field and a vector-valued function is one of domain, not of notation. Both produce vectors, and both may be written with angle brackets. A vector-valued function $\mathbf{r}(t)$ has an interval of parameters as its domain; a vector field $\mathbf{F}(x,y,z)$ has a region of space as its domain. The first describes a curve, the second a distribution of arrows over a region.

## Reading a field from its arrows

A vector field is visualized by drawing, at selected points of its domain, an arrow representing the vector at that point. The direction of the arrow is the direction of the field, and its length represents the magnitude. A complete picture would require an arrow at every point, so a diagram samples finitely many points and relies on the eye to interpolate.

Two conventions are common. In a true-length plot, arrow lengths are proportional to $\lVert\mathbf{F}\rVert,$ which makes regions of large magnitude visually dominant. In a direction plot, every arrow is drawn with the same length and only the direction is shown, which is the unit vector field

$$\widehat{\mathbf{F}}=\frac{\mathbf{F}}{\lVert\mathbf{F}\rVert} \tag{3}$$

where $\mathbf{F}\neq\mathbf{0}.$ Direction plots are preferable when the magnitude varies over several orders, as in gravitational or electrostatic fields.

Scaling arrow lengths by a constant changes the appearance but not the field. A diagram that is too dense obscures the pattern, and one that is too sparse fails to show it; the choice of sample points is part of the visualization, not part of the mathematics.

## Standard examples

Four families of fields recur throughout vector calculus.

A constant field assigns the same vector to every point:

$$\mathbf{F}(x,y)=\langle a,b\rangle$$

Its arrows are parallel and equally long. It has no preferred centre and no rotation.

A radial field points directly away from or toward a fixed point, and its magnitude depends only on the distance from that point. With the centre at the origin,

$$\mathbf{F}(x,y)=g(r)\,\langle x,y\rangle \qquad r=\sqrt{x^2+y^2} \tag{4}$$

for a scalar function $g.$ The unit radial field is $\langle x,y\rangle/r,$ and the inverse-square field in space is

$$\mathbf{F}(x,y,z)=\frac{\langle x,y,z\rangle}{(x^2+y^2+z^2)^{3/2}}=\frac{\mathbf{r}}{r^3} \tag{5}$$

which is defined away from the origin. Gravitational and electrostatic fields have this form, up to a constant and a sign.

A rotational field turns around a point. The standard example is

$$\mathbf{F}(x,y)=\langle-y,x\rangle \tag{6}$$

At $(1,0)$ the vector is $\langle0,1\rangle,$ at $(0,1)$ it is $\langle-1,0\rangle,$ and at $(-1,0)$ it is $\langle0,-1\rangle.$ The arrows circulate counterclockwise around the origin, and their length grows linearly with the distance from it.

A gradient field is the gradient of a scalar function:

$$\mathbf{F}=\nabla f=\left\langle\frac{\partial f}{\partial x},\frac{\partial f}{\partial y}\right\rangle \qquad \text{or} \qquad \mathbf{F}=\nabla f=\left\langle\frac{\partial f}{\partial x},\frac{\partial f}{\partial y},\frac{\partial f}{\partial z}\right\rangle \tag{7}$$

For $f(x,y)=x^2y+y^3,$

$$\nabla f=\langle2xy,\,x^2+3y^2\rangle$$

which is a vector field on $\mathbb{R}^2.$ At $(1,2)$ the field is $\langle4,13\rangle.$

Not every field is a gradient field. The rotational field (6) is not: if $\langle-y,x\rangle=\nabla f,$ then $\partial f/\partial x=-y$ and $\partial f/\partial y=x.$ Integrating the first equation gives $f=-xy+\phi(y),$ and differentiating with respect to $y$ gives $-x+\phi'(y)=x,$ which would require $\phi'(y)=2x.$ The left side depends only on $y$ and the right side only on $x,$ so no such function exists. The field (6) therefore has no potential function on $\mathbb{R}^2.$

## Gradient fields and potentials

A vector field $\mathbf{F}$ is conservative on an open connected domain $D$ if there exists a scalar function $f$ on $D$ such that

$$\mathbf{F}=\nabla f \qquad \text{on } D \tag{8}$$

The function $f$ is a potential function for $\mathbf{F}.$ It is determined only up to an additive constant, since $\nabla(f+C)=\nabla f.$

The definition is not merely algebraic. If $\mathbf{r}(t)$ is a differentiable curve in $D,$ then by the chain rule

$$\frac{d}{dt}f(\mathbf{r}(t))=\nabla f(\mathbf{r}(t))\cdot\mathbf{r}'(t)=\mathbf{F}(\mathbf{r}(t))\cdot\mathbf{r}'(t) \tag{9}$$

Integrating from $t=a$ to $t=b$ gives

$$\int_C\mathbf{F}\cdot d\mathbf{r}=f(\mathbf{r}(b))-f(\mathbf{r}(a)) \tag{10}$$

so the line integral of a conservative field depends only on the endpoints of the curve, not on the path between them. This is the fundamental theorem for line integrals, developed in the entry on [line integrals](../line-integrals/). A closed curve has equal endpoints, so its integral is zero.

Conversely, a field whose line integral is path-independent on an open connected domain is conservative, provided the field is continuous. One fixes a base point $P_0$ and defines $f(P)$ as the integral from $P_0$ to $P;$ path-independence makes $f$ well defined, and a difference-quotient argument shows that $\nabla f=\mathbf{F}.$ The potential is therefore not an extra structure imposed on the field but a consequence of path-independence.

The level curves of a potential are the sets $f(x,y)=c.$ Where the gradient does not vanish, it is orthogonal to the level curve through the point: if $\mathbf{r}(t)$ stays on a level curve, then $f(\mathbf{r}(t))$ is constant and (9) gives $\nabla f\cdot\mathbf{r}'=0.$ The arrows of a gradient field therefore cross the level curves at right angles. Where the level curves are close together, the gradient is large; where they are far apart, it is small. A topographic map and its steepest-ascent arrows illustrate the same relation.

## Field lines

A field line, also called an integral curve or a streamline, is a curve whose tangent at every point is parallel to the field at that point. If the curve is $\mathbf{r}(t),$ the condition is

$$\mathbf{r}'(t)=\lambda(t)\,\mathbf{F}(\mathbf{r}(t)) \tag{11}$$

for a positive scalar function $\lambda.$ When $\lambda=1,$ the parameter is chosen so that the curve is traversed with velocity equal to the field; this is the natural choice for a velocity field. Reparameterizing a field line changes $\lambda$ but not its image.

In the plane, field lines are solutions of the differential equation

$$\frac{dy}{dx}=\frac{Q(x,y)}{P(x,y)} \tag{12}$$

where the right side is defined and $P\neq0.$ In space, the corresponding system is

$$\frac{dx}{P}=\frac{dy}{Q}=\frac{dz}{R} \tag{13}$$

The field lines of the radial field (4) are rays from the origin, since the field is parallel to the position vector at every point. The field lines of the rotational field (6) are circles centred at the origin: along $\mathbf{r}(t)=\langle R\cos t,R\sin t\rangle,$ we have $\mathbf{r}'(t)=\langle-R\sin t,R\cos t\rangle=\mathbf{F}(\mathbf{r}(t)).$ The arrows and the field lines therefore agree, but they encode different information: the arrows give the local vector, the field lines give the global paths.

A point where $\mathbf{F}=\mathbf{0}$ is an equilibrium of the field. No field line passes through it with a well-defined tangent, and the local pattern near it can be a source, a sink, a centre or a saddle. The classification of these patterns belongs to the qualitative theory of differential equations; for the present purpose it is enough to note that zeros require separate treatment.

## Conservative fields and the curl test

The rotational field (6) has no potential, and this can be detected locally. For a $C^1$ field $\mathbf{F}=\langle P,Q\rangle,$ the scalar curl is

$$\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y} \tag{14}$$

For (6) it equals $1-(-1)=2,$ which is nonzero everywhere. A gradient field always has zero scalar curl, because equality of the mixed partials gives

$$\frac{\partial Q}{\partial x}=\frac{\partial^2 f}{\partial x\,\partial y}=\frac{\partial^2 f}{\partial y\,\partial x}=\frac{\partial P}{\partial y} \tag{15}$$

provided $f$ is of class $C^2.$ Hence a nonzero curl certifies that a field is not conservative.

The converse requires a topological hypothesis. If $D$ is simply connected, meaning that every closed curve in $D$ can be contracted continuously to a point within $D,$ and $\mathbf{F}$ is $C^1$ with zero curl on $D,$ then $\mathbf{F}$ is conservative on $D.$ On a domain with a hole the implication can fail.

The standard counterexample is

$$\mathbf{F}(x,y)=\left\langle-\frac{y}{x^2+y^2},\ \frac{x}{x^2+y^2}\right\rangle \tag{16}$$

on $D=\mathbb{R}^2\setminus\{(0,0)\}.$ A direct computation gives zero curl for every point of $D.$ Nevertheless, on the unit circle $\mathbf{r}(t)=\langle\cos t,\sin t\rangle,$

$$\int_C\mathbf{F}\cdot d\mathbf{r}=\int_0^{2\pi}\frac{(-\sin t)(-\sin t)+(\cos t)(\cos t)}{\cos^2t+\sin^2t}\,dt=\int_0^{2\pi}dt=2\pi \tag{17}$$

The integral around a closed curve is nonzero, so the field is not conservative on the punctured plane. The hole at the origin is exactly what prevents the loop from contracting, and the test fails because its hypothesis fails. On a simply connected subdomain that does not enclose the origin, the same formula defines a potential, namely a branch of the polar angle.

In space the corresponding test uses the full [curl](../curl/): a $C^1$ field on a simply connected domain is conservative if and only if $\operatorname{curl}\mathbf{F}=\mathbf{0}.$ The [divergence](../divergence/) gives a different local invariant, measuring the tendency of the field to spread out rather than to rotate.

## A field with zero divergence and zero curl

The field (16) is instructive because both of its first-order differential invariants vanish away from the origin. Its divergence is

$$\operatorname{div}\mathbf{F}=\frac{\partial}{\partial x}\left(\frac{-y}{x^2+y^2}\right)+\frac{\partial}{\partial y}\left(\frac{x}{x^2+y^2}\right)$$

A direct differentiation gives

$$\frac{\partial}{\partial x}\left(\frac{-y}{x^2+y^2}\right)=\frac{2xy}{(x^2+y^2)^2} \qquad \frac{\partial}{\partial y}\left(\frac{x}{x^2+y^2}\right)=\frac{-2xy}{(x^2+y^2)^2}$$

so the sum is zero. The field is both divergence-free and curl-free on the punctured plane, yet it is not conservative. The example shows that local differential conditions do not determine global behaviour when the domain has a hole.

The same phenomenon occurs in three dimensions with the inverse-square field (5). Its divergence is zero away from the origin, and its curl is zero because it is a gradient, $\mathbf{r}/r^3=\nabla(-1/r).$ The potential $-1/r$ is defined on $\mathbb{R}^3\setminus\{0\},$ which is simply connected, so the field is conservative there. The singularity at the origin carries the flux that would otherwise contradict the divergence theorem.

## Combining fields

Vector fields on a common domain form a vector space: sums and scalar multiples are defined pointwise,

$$(\mathbf{F}+\mathbf{G})(P)=\mathbf{F}(P)+\mathbf{G}(P) \qquad (c\mathbf{F})(P)=c\,\mathbf{F}(P) \tag{18}$$

The dot and cross products of two fields are defined pointwise as well, and they produce a scalar field and a vector field respectively. These operations allow a complicated field to be decomposed into simpler parts, such as a radial part and a rotational part.

A useful decomposition in two dimensions separates a field into a gradient and a rotated gradient. Under suitable regularity and decay conditions, a planar field can be written as

$$\mathbf{F}=\nabla\phi+\langle-\partial_y\psi,\partial_x\psi\rangle \tag{19}$$

where $\phi$ is a scalar potential and $\psi$ a stream function. The first term is curl-free and the second is divergence-free. The decomposition is the two-dimensional case of the Helmholtz decomposition; it is stated here to indicate how the two local invariants organize the field, not as a construction for arbitrary domains.

## Worked example

Consider

$$\mathbf{F}(x,y)=\langle x^2-y,\ x+y^2\rangle$$

Its components are polynomials, so the field is $C^\infty$ on $\mathbb{R}^2.$ The divergence and scalar curl are

$$\operatorname{div}\mathbf{F}=2x+2y \qquad \operatorname{curl}\mathbf{F}=\frac{\partial}{\partial x}(x+y^2)-\frac{\partial}{\partial y}(x^2-y)=1-(-1)=2$$

At $(1,2)$ the divergence is $6$ and the curl is $2.$ The positive divergence says that a small region around $(1,2)$ has more outward flow than inward flow; the positive curl says that a small paddlewheel placed there turns counterclockwise. Since the curl is nonzero everywhere, the field is not conservative on $\mathbb{R}^2.$

The field lines satisfy

$$\frac{dy}{dx}=\frac{x+y^2}{x^2-y}$$

which is not separable in elementary terms. This is typical: field lines of a polynomial field need not have closed-form equations. The arrows still determine the qualitative picture, and numerical integration can approximate individual trajectories.

## Pitfalls and scope

+ A vector field is not a vector. At each point it has a value, but the field as a whole is a function. Writing $\mathbf{F}=\langle P,Q\rangle$ without specifying the domain omits part of the definition.
+ The unit field $\mathbf{F}/\lVert\mathbf{F}\rVert$ is defined only where $\mathbf{F}\neq\mathbf{0}.$ Normalizing at a zero would divide by zero and can obscure the local structure.
+ A zero curl does not imply a potential on every domain. The punctured plane is the standard obstruction, and the hypothesis of simple connectedness cannot be dropped.
+ A nonzero curl is a conclusive obstruction to being a gradient, but a zero curl is not by itself a constructive formula for the potential. The potential must be found by integration, and the constant of integration is fixed only by a value at one point.
+ Field lines are not the same as the arrows. The arrows show the direction and magnitude at sample points; the field lines are the curves tangent to those arrows everywhere.
+ The sign convention for potentials varies. In physics, a conservative force is often written $\mathbf{F}=-\nabla U,$ where $U$ is potential energy; in mathematics, $\mathbf{F}=\nabla f.$ The two conventions differ by a sign and should not be mixed within a calculation.

## Related notions

The gradient produces the simplest vector fields and links them to level sets. The [divergence](../divergence/) and the [curl](../curl/) measure the local spreading and rotation of a field, and the [Laplacian](../laplacian/) is the divergence of a gradient. Integrating a field along a curve gives a [line integral](../line-integrals/), whose path-independence characterizes conservative fields. The [double integral](../double-integrals/) and [triple integral](../triple-integrals/) integrate scalar functions over regions; their vector analogues integrate fluxes over surfaces and are the subject of the divergence theorem.
