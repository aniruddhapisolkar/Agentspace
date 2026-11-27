---
title: Fundamental Theorem for Line Integrals
source: https://algebrica.org/fundamental-theorem-for-line-integrals/
license: CC BY-NC 4.0
tags:
  - conservative-fields
  - fundamental-theorem
  - line-integrals
  - multivariable-calculus
  - path-independence
  - vector-calculus
---

## The theorem

The fundamental theorem of calculus evaluates an integral of a derivative at the endpoints of an interval. The fundamental theorem for line integrals does the same for a gradient along a curve: the integral of a gradient field depends only on the values of the potential at the two endpoints.

Let $C$ be a piecewise smooth curve in $\mathbb{R}^2$ or $\mathbb{R}^3,$ parameterized by $\mathbf{r}(t)$ for $a\le t\le b,$ oriented from $A=\mathbf{r}(a)$ to $B=\mathbf{r}(b).$ Let $f$ be a scalar function of class $C^1$ on an open set containing $C.$ Then

$$\int_C\nabla f\cdot d\mathbf{r}=f(B)-f(A) \tag{1}$$

The integral is the vector line integral of the gradient field. If $\mathbf{F}=\nabla f$ is a conservative field with potential $f,$ the theorem reads

$$\int_C\mathbf{F}\cdot d\mathbf{r}=f(B)-f(A) \tag{2}$$

The right side contains no parameter, no speed and no description of the route. Two travellers who start at $A$ and finish at $B$ obtain the same value, however different their paths, provided both paths lie in the domain of $f.$

The theorem is the reason potentials are useful. Computing a line integral directly requires a parameterization, the chain rule and an ordinary integral, and the result may depend on the parameterization in appearance. With a potential, the computation reduces to two evaluations and a subtraction. The potential plays the role of an antiderivative, and the endpoints play the role of the limits of integration.

## Hypotheses and orientation

Each hypothesis has a function.

+ $f$ must be differentiable on an open set containing the curve, with continuous gradient, so that the chain rule applies along the whole curve. Differentiability at the endpoints alone would not control the interior.
+ The curve must be piecewise smooth, so that it has a tangent almost everywhere and can be integrated piece by piece. A curve with infinitely many corners accumulating inside the interval is excluded.
+ The curve must lie in the domain of $f.$ If the path passes through a point where the potential is undefined, the theorem does not apply, even if the integral can be computed by another method.
+ The orientation matters. Reversing the curve from $B$ to $A$ changes the sign, because $d\mathbf{r}$ changes sign while the potential values at the endpoints are interchanged.

The theorem is stated for a potential of class $C^1.$ It does not require $f$ to be $C^2;$ the chain rule needs only first derivatives. The curl enters when one asks whether a given field is a gradient, which is a separate question.

## Proof

For a smooth curve, the proof is a single application of the chain rule followed by the fundamental theorem of calculus. Define the scalar function

$$g(t)=f(\mathbf{r}(t)) \qquad a\le t\le b \tag{3}$$

By the chain rule,

$$g'(t)=\nabla f(\mathbf{r}(t))\cdot\mathbf{r}'(t) \tag{4}$$

Therefore

$$\int_C\nabla f\cdot d\mathbf{r}=\int_a^b\nabla f(\mathbf{r}(t))\cdot\mathbf{r}'(t)\,dt=\int_a^b g'(t)\,dt=g(b)-g(a) \tag{5}$$

and $g(b)=f(\mathbf{r}(b))=f(B),$ $g(a)=f(A).$ This proves (1) for a smooth curve.

For a piecewise smooth curve, write $C=C_1+\cdots+C_n,$ where the endpoint of $C_i$ is the initial point of $C_{i+1}.$ Applying the smooth case to each piece,

$$\int_C\nabla f\cdot d\mathbf{r}=\sum_{i=1}^{n}\bigl(f(P_i)-f(P_{i-1})\bigr) \tag{6}$$

where $P_0=A$ and $P_n=B.$ The sum telescopes, because every intermediate value appears once with a plus sign and once with a minus sign:

$$\sum_{i=1}^{n}\bigl(f(P_i)-f(P_{i-1})\bigr)=f(P_n)-f(P_0)=f(B)-f(A) \tag{7}$$

A corner contributes nothing, since a single point has zero length. The derivative may fail at the corner, but the integral is unaffected.

The proof also shows why the result is independent of the parameterization. A different parameterization composes $\mathbf{r}$ with an increasing function of the new parameter; the chain rule produces the same derivative $g'$ up to the change of variable, and the endpoints are unchanged. A decreasing reparameterization reverses the orientation and changes the sign, in agreement with the orientation rule.

## Path independence

The first consequence is that the line integral of a conservative field is independent of path. If $C_1$ and $C_2$ are two piecewise smooth curves in the domain of $f,$ both from $A$ to $B,$ then

$$\int_{C_1}\mathbf{F}\cdot d\mathbf{r}=f(B)-f(A)=\int_{C_2}\mathbf{F}\cdot d\mathbf{r} \tag{8}$$

The second consequence concerns closed curves. If $C$ is closed, its initial and terminal points coincide, so $f(B)-f(A)=f(A)-f(A)=0$ and

$$\oint_C\mathbf{F}\cdot d\mathbf{r}=0 \tag{9}$$

Conversely, if a continuous field on an open connected domain has zero integral around every closed piecewise smooth curve, then it is path-independent: two paths from $A$ to $B$ form a closed loop when one is traversed forward and the other backward, and the zero circulation forces the two integrals to agree.

The three properties are therefore equivalent on an open connected domain:

+ $\mathbf{F}$ is conservative, that is, $\mathbf{F}=\nabla f$ for some $C^1$ potential $f.$
+ The line integral of $\mathbf{F}$ is path-independent.
+ The line integral of $\mathbf{F}$ around every closed piecewise smooth curve is zero.

The implication from the first to the other two is the fundamental theorem. The equivalence of the second and third is the loop argument just given. The remaining implication, from path independence to a potential, is proved by construction.

## Recovering a potential from the integral

Suppose that $\mathbf{F}$ is continuous and path-independent on an open connected domain $D.$ Fix a base point $P_0\in D$ and define

$$f(P)=\int_{P_0}^{P}\mathbf{F}\cdot d\mathbf{r} \tag{10}$$

along any piecewise smooth path in $D$ from $P_0$ to $P.$ Path independence makes the value independent of the chosen path, so $f$ is a function of $P$ alone.

To compute its gradient, take $P=(x,y)$ and a small horizontal displacement to $(x+h,y).$ The difference is the integral along the horizontal segment, so

$$\frac{f(x+h,y)-f(x,y)}{h}=\frac1h\int_0^h P(x+t,y)\,dt \tag{11}$$

As $h\to0,$ the right side tends to $P(x,y)$ by continuity of the field. Hence $f_x=P.$ The same argument with a vertical displacement gives $f_y=Q,$ and in space the third coordinate gives $f_z=R.$ Therefore $\nabla f=\mathbf{F},$ and the path-independent field is conservative.

This construction is also a practical algorithm when the domain is a rectangle containing the origin, so that the coordinate-axis path stays inside it. On $\mathbb{R}^2,$ integrate from the origin along the coordinate axes:

$$f(x,y)=\int_0^x P(t,0)\,dt+\int_0^y Q(x,t)\,dt \tag{12}$$

The first integral reaches $(x,0),$ and the second moves vertically to $(x,y).$ The result is a potential, provided the field is conservative. For

$$\mathbf{F}(x,y)=\langle 2xy,\ x^2\rangle \tag{13}$$

the first integral is zero and the second is

$$f(x,y)=\int_0^y x^2\,dt=x^2y \tag{14}$$

and indeed $\nabla(x^2y)=\langle2xy,x^2\rangle.$ On a more general domain, the same idea works with any convenient path from a base point, but the path must stay inside the domain.

## A worked example

Consider

$$\mathbf{F}(x,y,z)=\langle yz,\ xz,\ xy\rangle \tag{15}$$

with potential

$$f(x,y,z)=xyz \tag{16}$$

as a direct differentiation confirms. The field is conservative on $\mathbb{R}^3,$ so the integral from $A=(1,2,3)$ to $B=(4,5,6)$ is

$$\int_C\mathbf{F}\cdot d\mathbf{r}=f(4,5,6)-f(1,2,3)=120-6=114 \tag{17}$$

The value does not depend on the path. As a check, take the straight segment

$$\mathbf{r}(t)=\langle1+3t,\ 2+3t,\ 3+3t\rangle \qquad 0\le t\le1 \tag{18}$$

which also runs from $A$ to $B.$ Along it,

$$\mathbf{F}(\mathbf{r}(t))=\langle(2+3t)(3+3t),\ (1+3t)(3+3t),\ (1+3t)(2+3t)\rangle \tag{19}$$

with $\mathbf{r}'(t)=\langle3,3,3\rangle.$ Expanding the three products gives

$$\mathbf{F}(\mathbf{r}(t))=\langle6+15t+9t^2,\ 3+12t+9t^2,\ 2+9t+9t^2\rangle \tag{20}$$

so the dot product is $3(11+36t+27t^2)=33+108t+81t^2,$ and

$$\int_0^1(33+108t+81t^2)\,dt=33+54+27=114 \tag{21}$$

The direct computation requires expanding three products; the endpoint evaluation requires only two products. The agreement is a check on the potential, not a proof that the field is conservative; the proof is the identity $\mathbf{F}=\nabla f.$

## A field that is not a gradient

The theorem does not apply to every field, and a failed application is instructive. Let

$$\mathbf{F}(x,y)=\langle-y,x\rangle \tag{22}$$

and integrate from $A=(1,0)$ to $B=(-1,0)$ along the upper semicircle $C_+.$ With $\mathbf{r}(t)=\langle\cos t,\sin t\rangle$ for $0\le t\le\pi,$

$$\mathbf{F}(\mathbf{r}(t))=\langle-\sin t,\cos t\rangle \qquad \mathbf{r}'(t)=\langle-\sin t,\cos t\rangle \tag{23}$$

so the integrand is $\sin^2t+\cos^2t=1$ and

$$\int_{C_+}\mathbf{F}\cdot d\mathbf{r}=\int_0^\pi dt=\pi \tag{24}$$

Along the lower semicircle $C_-,$ parameterized by $\mathbf{r}(t)=\langle\cos t,\sin t\rangle$ for $0\le t\le-\pi,$ the same integrand is $1,$ but the parameter decreases, so

$$\int_{C_-}\mathbf{F}\cdot d\mathbf{r}=\int_0^{-\pi}dt=-\pi \tag{25}$$

The two paths have the same endpoints and different integrals. The field is not conservative on $\mathbb{R}^2.$ Its scalar curl is $1-(-1)=2,$ which is nonzero everywhere, so no potential exists.

## The gravitational case

For a point mass $M$ at the origin, the force on a particle of mass $m$ is

$$\mathbf{F}(\mathbf{r})=-\frac{GMm}{r^3}\,\mathbf{r} \qquad r=\lVert\mathbf{r}\rVert \tag{26}$$

with potential

$$f(\mathbf{r})=\frac{GMm}{r} \tag{27}$$

The work done by gravity in moving the particle from $r=r_1$ to $r=r_2$ along any path is

$$W=\int_C\mathbf{F}\cdot d\mathbf{r}=GMm\left(\frac1{r_2}-\frac1{r_1}\right) \tag{28}$$

If $r_2>r_1,$ the work is negative: gravity pulls inward while the particle moves outward. If $r_2<r_1,$ the work is positive. Around a closed orbit the work is zero, which is the statement that gravity is conservative. The result depends only on the two radii, not on the shape of the orbit or on the angular motion.

The potential energy is $U=-GMm/r,$ and $W=U(r_1)-U(r_2),$ in agreement with the general relation between work and potential energy. The sign conventions are the most common source of error in this calculation: the potential function $f=GMm/r$ is positive and decreases outward, while the potential energy is negative and increases outward.

## The theorem as a higher-dimensional fundamental theorem

The one-variable fundamental theorem of calculus states

$$\int_a^b g'(x)\,dx=g(b)-g(a) \tag{29}$$

The fundamental theorem for line integrals replaces the interval by a curve, the ordinary derivative by the gradient and the endpoints by the endpoints of the curve:

$$\int_C\nabla f\cdot d\mathbf{r}=f(B)-f(A) \tag{30}$$

The analogy is exact, not merely visual. In one variable the integral is taken with respect to the parameter $x,$ and $g'$ is the derivative in the direction of increasing $x.$ Along a curve the parameter is $t,$ and $\nabla f\cdot\mathbf{r}'$ is the derivative of $f$ in the direction of the tangent. The fundamental theorem of calculus then supplies the endpoint difference.

In the language of differential forms, the integrand is the exact one-form $df,$ and the theorem says that the integral of an exact form over a curve depends only on the boundary of the curve, which is the pair of endpoints with opposite signs. This is the one-dimensional case of the general Stokes theorem, and it explains why the curl, which measures the local obstruction to exactness, is the relevant local object.

## What the theorem does not say

+ It does not apply to a field that is not a gradient. The rotational field (22) has the same endpoints along two paths and different integrals, so no potential exists on $\mathbb{R}^2.$
+ It does not say that a field with zero curl is conservative on every domain. The punctured-plane field has zero curl and nonzero circulation around the origin; a potential exists only locally, as a branch of the angle, and the endpoint difference is ambiguous for a path that winds around the hole.
+ It does not apply to a path that leaves the domain of the potential. A potential defined on a slit plane cannot be used along a curve that crosses the slit.
+ It does not give the value of a scalar line integral. The scalar integral $\int_C f\,ds$ depends on the length and shape of the curve; there is no endpoint formula for a general scalar density.
+ It does not prove that a field is conservative from a single pair of paths with equal integrals. Path independence requires every pair of paths in the domain to agree.
+ It does not require the curve to be simple or non-self-intersecting. A curve that crosses itself is still piecewise smooth, and the endpoint formula remains valid, although the integral counts the traversal of each piece.

- - -

The theorem converts a potential into a computational device and converts path independence into a test for conservatism. Its limitation is equally important: the endpoint formula exists only because the field is a gradient, and the obstruction to a gradient on a domain with a hole is measured by circulation around the hole.

## Related notions

The theorem is the central property of [conservative vector fields](../conservative-vector-fields/), where the equivalence with path independence and the curl test are developed. The line integral itself, including its scalar and vector forms, is treated in [line integrals](../line-integrals/); the local obstruction to a potential is the [curl](../curl/). The one-variable prototype is the fundamental theorem of calculus, and the higher-dimensional generalizations are Green's theorem and Stokes' theorem. Work and potential energy connect the result to mechanics, and the gradient is the normal vector to level surfaces in [tangent planes and linear approximations](../tangent-planes-and-linear-approximations/).
