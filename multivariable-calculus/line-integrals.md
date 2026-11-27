---
title: Line Integrals
source: https://algebrica.org/line-integrals/
license: CC BY-NC 4.0
tags:
  - circulation
  - conservative-fields
  - line-integrals
  - multivariable-calculus
  - path-independence
  - work
---

## Two integrals along a curve

An ordinary integral adds values of a function along an interval. A line integral adds values along a curve. The values may be scalars, such as a density or a temperature, or they may be the tangential components of a vector field. These two cases produce the scalar line integral and the vector line integral. They are related, but they are not the same object, and confusing them is the most common source of sign and factor errors.

Throughout, $C$ is a piecewise smooth curve in the plane or in space, parameterized by

$$\mathbf{r}(t)=\langle x(t),y(t),z(t)\rangle \qquad a\le t\le b \tag{1}$$

with $\mathbf{r}'$ continuous and nonzero except possibly at finitely many points. The curve is oriented by increasing $t.$ A piecewise smooth curve is a finite union of smooth pieces, joined end to end.

## The scalar line integral

Let $f$ be a continuous scalar function defined on $C.$ Partition $C$ into $n$ consecutive arcs of lengths $\Delta s_1,\ldots,\Delta s_n,$ choose a sample point $P_i^*$ on the $i$-th arc, and form the sum

$$\sum_{i=1}^{n}f(P_i^*)\,\Delta s_i$$

As the partition is refined so that the largest arc length tends to zero, the sums converge to the scalar line integral of $f$ over $C,$ written

$$\int_C f\,ds \tag{2}$$

The element $ds$ is arc length, not the parameter increment. It is nonnegative, and it measures distance along the curve.

If $C$ is parameterized by (1), then

$$ds=\lVert\mathbf{r}'(t)\rVert\,dt \tag{3}$$

and therefore

$$\int_C f\,ds=\int_a^b f(\mathbf{r}(t))\,\lVert\mathbf{r}'(t)\rVert\,dt \tag{4}$$

The integrand is evaluated on the curve, and the speed of the parameterization supplies the conversion from $dt$ to $ds.$ The value does not depend on the parameterization: a different parameterization traverses the same arcs, and the chain rule changes $dt$ and $\lVert\mathbf{r}'\rVert$ in compensating ways. Reversing the orientation also leaves the integral unchanged, because $ds$ is nonnegative and the set of arcs is the same.

The simplest case is $f=1,$ for which

$$\int_C ds=\int_a^b\lVert\mathbf{r}'(t)\rVert\,dt \tag{5}$$

is the arc length of $C.$ The scalar line integral therefore generalizes arc length in the same way that a weighted integral generalizes ordinary length.

For example, let $C$ be the unit circle traversed counterclockwise and let $f(x,y)=x^2.$ With $\mathbf{r}(t)=\langle\cos t,\sin t\rangle$ and $0\le t\le2\pi,$

$$\int_C x^2\,ds=\int_0^{2\pi}\cos^2t\,dt=\pi \tag{6}$$

since $\lVert\mathbf{r}'(t)\rVert=1.$ Traversing the circle clockwise gives the same value, because the integrand is unchanged and $ds$ is unchanged. The result is half the circumference, which is plausible: $x^2$ averages to $1/2$ over the circle.

## Mass, centre of mass and average value

The scalar line integral has a direct physical reading. If a wire has the shape $C$ and linear density $\rho(x,y,z),$ then its mass is

$$M=\int_C\rho\,ds \tag{7}$$

and its centre of mass has coordinates

$$\bar{x}=\frac{1}{M}\int_C x\,\rho\,ds \qquad \bar{y}=\frac{1}{M}\int_C y\,\rho\,ds \qquad \bar{z}=\frac{1}{M}\int_C z\,\rho\,ds \tag{8}$$

The average value of $f$ over the curve is

$$f_{\mathrm{avg}}=\frac{1}{L}\int_C f\,ds \qquad L=\int_C ds \tag{9}$$

These formulas are the one-dimensional analogues of the corresponding formulas for double and triple integrals. The curve has no area, so the integrals are weighted by length rather than by area or volume.

For a semicircular wire of radius $R$ in the upper half-plane with constant density $\rho_0,$ the mass is $\rho_0\pi R.$ By symmetry $\bar{x}=0,$ and

$$\bar{y}=\frac{1}{\pi R}\int_0^\pi R\sin t\,R\,dt=\frac{R}{\pi}\left[-\cos t\right]_0^\pi=\frac{2R}{\pi}$$

The centre of mass lies above the centre of the circle, at height $2R/\pi,$ which is less than $R$ as expected.

## The vector line integral

Let $\mathbf{F}$ be a continuous vector field defined on $C.$ The vector line integral of $\mathbf{F}$ along $C$ is

$$\int_C\mathbf{F}\cdot d\mathbf{r}=\int_a^b\mathbf{F}(\mathbf{r}(t))\cdot\mathbf{r}'(t)\,dt \tag{10}$$

The integrand is the dot product of the field with the velocity of the parameterization. Only the component of $\mathbf{F}$ along the tangent contributes, and the sign depends on the direction of travel. If $\mathbf{F}$ is a force, the integral is the work done by the force along the curve. If $\mathbf{F}$ is a velocity field, the integral is the circulation along the curve.

The vector line integral is often written with the coordinate differentials:

$$\int_C P\,dx+Q\,dy+R\,dz=\int_a^b\left(P\frac{dx}{dt}+Q\frac{dy}{dt}+R\frac{dz}{dt}\right)dt \tag{11}$$

This is the same integral as (10), with $\mathbf{F}=\langle P,Q,R\rangle$ and $d\mathbf{r}=\langle dx,dy,dz\rangle.$ The notation is convenient when the curve is given by relations among $x,y,z$ rather than by a parameter.

Reversing the orientation of $C$ changes the sign:

$$\int_{-C}\mathbf{F}\cdot d\mathbf{r}=-\int_C\mathbf{F}\cdot d\mathbf{r} \tag{12}$$

because $d\mathbf{r}$ changes sign while the field values are unchanged. This is the essential difference from the scalar line integral, which is orientation-independent. The two integrals are related by

$$\int_C\mathbf{F}\cdot d\mathbf{r}=\int_C(\mathbf{F}\cdot\mathbf{T})\,ds \tag{13}$$

where $\mathbf{T}=\mathbf{r}'/\lVert\mathbf{r}'\rVert$ is the unit tangent in the direction of orientation. The right side is a scalar line integral of the tangential component, and it makes the orientation dependence explicit: reversing the curve replaces $\mathbf{T}$ by $-\mathbf{T}.$

## A path-dependent example

Let $\mathbf{F}(x,y)=\langle x^2,xy\rangle$ and let $C_1$ be the parabola $y=x^2$ from $(0,0)$ to $(1,1).$ Parameterize it by

$$\mathbf{r}(t)=\langle t,t^2\rangle \qquad 0\le t\le1$$

Then $\mathbf{F}(\mathbf{r}(t))=\langle t^2,t^3\rangle$ and $\mathbf{r}'(t)=\langle1,2t\rangle,$ so

$$\int_{C_1}\mathbf{F}\cdot d\mathbf{r}=\int_0^1(t^2+2t^4)\,dt=\frac13+\frac25=\frac{11}{15} \tag{14}$$

Now let $C_2$ be the straight segment from $(0,0)$ to $(1,1),$ parameterized by $\mathbf{r}(t)=\langle t,t\rangle.$ Then $\mathbf{F}=\langle t^2,t^2\rangle$ and $\mathbf{r}'=\langle1,1\rangle,$ so

$$\int_{C_2}\mathbf{F}\cdot d\mathbf{r}=\int_0^1 2t^2\,dt=\frac23 \tag{15}$$

The two curves have the same endpoints, but the integrals differ. The field is therefore not conservative on $\mathbb{R}^2,$ and the integral depends on the path. The difference is not a computational error: it reflects the fact that the field does positive work along one route and a different amount along another.

The same field has nonzero scalar curl:

$$\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}=y-0=y$$

which is nonzero except on the $x$-axis. A nonzero curl rules out a potential function, in agreement with the path dependence.

## The fundamental theorem for line integrals

A vector field $\mathbf{F}$ is conservative on an open connected domain $D$ if $\mathbf{F}=\nabla f$ for some scalar function $f.$ In that case the vector line integral depends only on the endpoints.

Let $C$ be a piecewise smooth curve in $D$ from $A$ to $B,$ parameterized by $\mathbf{r}(t)$ for $a\le t\le b,$ and let $\mathbf{F}=\nabla f$ be continuous on $D.$ Then

$$\int_C\mathbf{F}\cdot d\mathbf{r}=f(B)-f(A) \tag{16}$$

For a smooth curve, the proof is the chain rule:

$$\frac{d}{dt}f(\mathbf{r}(t))=\nabla f(\mathbf{r}(t))\cdot\mathbf{r}'(t)=\mathbf{F}(\mathbf{r}(t))\cdot\mathbf{r}'(t)$$

Integrating from $a$ to $b$ and applying the fundamental theorem of calculus gives (16). For a piecewise smooth curve, the same argument is applied to each piece and the values at the intermediate points cancel.

Three statements are equivalent for a continuous field on an open connected domain:

+ $\mathbf{F}$ is conservative, that is, $\mathbf{F}=\nabla f$ for some potential $f.$
+ The line integral of $\mathbf{F}$ is path-independent: any two piecewise smooth curves in $D$ with the same endpoints give the same integral.
+ The line integral of $\mathbf{F}$ around every closed piecewise smooth curve in $D$ is zero.

The implication from the first to the second is (16). The second implies the third because a closed curve starts and ends at the same point. The third implies the second by joining two paths from $A$ to $B$ into a closed loop. The third also implies the first: fix a base point $P_0$ and define $f(P)$ as the integral from $P_0$ to $P;$ path-independence makes $f$ well defined, and a difference-quotient argument shows that $\nabla f=\mathbf{F}.$ The last step requires the field to be continuous, so that the integral varies smoothly with the endpoint.

For the potential

$$f(x,y)=x^2y+y^3 \qquad \mathbf{F}=\nabla f=\langle2xy,\,x^2+3y^2\rangle$$

the integral from $(0,0)$ to $(1,1)$ along any piecewise smooth path is

$$f(1,1)-f(0,0)=2-0=2$$

The parabola and the straight segment used above both give $2$ for this field, even though they gave different values for $\langle x^2,xy\rangle.$ The potential removes the path dependence entirely.

## Finding a potential

On a simply connected domain, a $C^1$ field with zero curl is conservative. In the plane, the condition is

$$\frac{\partial Q}{\partial x}=\frac{\partial P}{\partial y} \tag{17}$$

In space, it is $\operatorname{curl}\mathbf{F}=\mathbf{0}.$

To find a potential for $\mathbf{F}=\langle P,Q\rangle,$ integrate $P$ with respect to $x$:

$$f(x,y)=\int P(x,y)\,dx+\phi(y)$$

The “constant” of integration may depend on $y,$ because the derivative with respect to $x$ treats $y$ as constant. Differentiating the result with respect to $y$ and setting it equal to $Q$ determines $\phi'(y),$ and one more integration determines $\phi$ up to an additive constant.

For $\mathbf{F}=\langle2xy,x^2+3y^2\rangle,$

$$f=\int2xy\,dx=x^2y+\phi(y)$$

Then

$$\frac{\partial f}{\partial y}=x^2+\phi'(y)=x^2+3y^2$$

so $\phi'(y)=3y^2$ and $\phi(y)=y^3+C.$ Hence $f=x^2y+y^3+C,$ as claimed.

The potential is determined only up to a constant. Changing the constant changes $f$ but not $\nabla f,$ and it cancels in the difference $f(B)-f(A).$ A value at one point fixes the constant if a numerical potential is required.

## Closed curves and circulation

For a closed curve $C,$ the vector line integral is called the circulation of $\mathbf{F}$ around $C$ and is often written

$$\oint_C\mathbf{F}\cdot d\mathbf{r} \tag{18}$$

The circle on the integral sign emphasizes that the curve is closed. The orientation matters: the same geometric loop traversed in the opposite direction gives the negative circulation.

A conservative field has zero circulation around every closed curve, by (16) with $A=B.$ The converse holds on a simply connected domain, as discussed above. On a domain with a hole, a field can have zero curl everywhere and still have nonzero circulation around a loop that encloses the hole. The standard example is

$$\mathbf{F}(x,y)=\left\langle-\frac{y}{x^2+y^2},\ \frac{x}{x^2+y^2}\right\rangle$$

on the punctured plane. Its circulation around the unit circle is $2\pi,$ even though its scalar curl vanishes away from the origin. The loop cannot contract to a point without crossing the missing origin, so the local condition does not integrate to a global potential.

For a closed curve that bounds a plane region $D,$ Green's theorem expresses the circulation as a double integral:

$$\oint_C P\,dx+Q\,dy=\iint_D\left(\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}\right)dA \tag{19}$$

with $C$ oriented counterclockwise. In space, Stokes' theorem expresses the circulation around the boundary of a surface as the flux of the curl through the surface. These theorems convert a line integral into an integral over a region of higher dimension, and they are the reason the curl is called the circulation density.

## A helical work integral

Let

$$\mathbf{F}(x,y,z)=\langle-y,x,z\rangle \qquad \mathbf{r}(t)=\langle\cos t,\sin t,t\rangle \qquad 0\le t\le2\pi$$

The curve is one turn of a helix. Along it,

$$\mathbf{F}(\mathbf{r}(t))=\langle-\sin t,\cos t,t\rangle \qquad \mathbf{r}'(t)=\langle-\sin t,\cos t,1\rangle$$

so

$$\mathbf{F}\cdot\mathbf{r}'=\sin^2t+\cos^2t+t=1+t$$

and the work is

$$\int_C\mathbf{F}\cdot d\mathbf{r}=\int_0^{2\pi}(1+t)\,dt=2\pi+2\pi^2 \tag{20}$$

The first term $2\pi$ is the circulation of the rotational part $\langle-y,x,0\rangle$ around the unit circle; the second term $2\pi^2$ is the work done by the vertical component $z$ against the rise of the helix. The decomposition is not a coincidence: the field is the sum of a rotational field and a vertical field, and the line integral is additive.

## Scalar and vector integrals compared

The two line integrals answer different questions.

| Integral | Integrand | Element | Orientation |
|---|---|---|---|
| $\displaystyle\int_C f\,ds$ | scalar $f$ | arc length $ds$ | independent |
| $\displaystyle\int_C\mathbf{F}\cdot d\mathbf{r}$ | vector $\mathbf{F}$ | displacement $d\mathbf{r}$ | changes sign |

The scalar integral is appropriate for densities, masses and averages along a wire. The vector integral is appropriate for work, circulation and flow along a path. The scalar integral of $f=1$ is the length of $C;$ the vector integral of a unit tangent field along $C$ is also the length, by (13), but this is a special case.

A third integral, the flux across a curve, uses the normal component:

$$\int_C\mathbf{F}\cdot\mathbf{n}\,ds \tag{21}$$

where $\mathbf{n}$ is a chosen unit normal. In the plane, the flux across a closed curve is related to the divergence by Green's theorem, just as the circulation is related to the curl. The normal must be specified; for a closed curve, the outward normal is the standard choice. The flux integral is not the same as the vector line integral, and replacing one by the other changes the geometric meaning.

## Piecewise curves and parameterizations

A piecewise smooth curve is integrated piece by piece:

$$\int_C=\int_{C_1}+\cdots+\int_{C_n} \tag{22}$$

with the endpoint of each piece equal to the initial point of the next. The orientation of the whole curve is the orientation induced by the order of the pieces. A corner does not contribute to the integral, because a single point has zero length; the value is unaffected by the corner, although the derivative may fail there.

The parameterization may be changed without changing a scalar line integral, and without changing a vector line integral if the reparameterization preserves orientation. If $t=\phi(u)$ with $\phi'>0,$ then

$$\int_{C}\mathbf{F}\cdot d\mathbf{r}=\int_{\alpha}^{\beta}\mathbf{F}(\mathbf{r}(\phi(u)))\cdot\mathbf{r}'(\phi(u))\,\phi'(u)\,du \tag{23}$$

by the chain rule. If $\phi'<0,$ the orientation reverses and the integral changes sign. The scalar integral is unaffected in either case, because the absolute value of $\phi'$ appears through $ds.$

A parameterization that is not one-to-one complicates the interpretation. If the curve is traced twice, the vector integral counts the work twice, while the scalar integral counts the mass twice. The geometric curve may be the same, but the parameterized curve is not.

## What line integrals do not say

+ The scalar line integral is not the integral of $f$ with respect to $x$ or $y.$ The element $ds$ is arc length, and substituting $dx$ or $dy$ changes the value and the geometric meaning.
+ The vector line integral is not the integral of $\lVert\mathbf{F}\rVert.$ Only the tangential component contributes; a field perpendicular to the curve does no work.
+ Path independence is a property of the field and the domain, not of a particular pair of paths. A single pair of paths with equal integrals does not prove that a field is conservative.
+ A zero curl on a domain with a hole does not imply path independence. The punctured-plane field is the standard counterexample.
+ Green's theorem requires a closed curve with the correct orientation and a region to which it applies. A curve that is not closed has no enclosed region, and reversing the orientation reverses the sign.
+ The choice of parameterization affects the computation but not the value of a scalar integral, and it does not affect a vector integral unless the orientation is reversed. A negative speed or a decreasing parameter is a common source of sign errors.

## Related notions

Line integrals are the one-dimensional case of integration over a parameterized set. Their scalar form generalizes [arc length](../arc-length-of-a-curve/), and their vector form is the circulation that appears in the fundamental theorem for line integrals, Green's theorem and Stokes' theorem. Conservative fields and potentials are introduced in the entry on [vector fields](../vector-fields/); the local obstruction to a potential is the [curl](../curl/), and the corresponding flux obstruction is the [divergence](../divergence/). The [double integral](../double-integrals/) supplies the area integrals used in Green's theorem.
