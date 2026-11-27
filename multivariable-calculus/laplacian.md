---
title: Laplacian
source: https://algebrica.org/laplacian/
license: CC BY-NC 4.0
tags:
  - harmonic-functions
  - laplace-equation
  - laplacian
  - multivariable-calculus
  - partial-differential-equations
  - vector-calculus
---

## The divergence of a gradient

The gradient turns a scalar function into a vector field. The divergence turns a vector field into a scalar function. Composing the two produces a single second-order operator that measures how a function differs from its average over small spheres. This operator, the Laplacian, is the principal second-order operator of mathematical physics.

Let $D\subseteq\mathbb{R}^n$ be open and let $f:D\to\mathbb{R}$ be of class $C^2.$ The Laplacian of $f$ is the scalar function

$$\Delta f=\operatorname{div}(\nabla f)=\nabla\cdot\nabla f=\sum_{i=1}^{n}\frac{\partial^2 f}{\partial x_i^2} \tag{1}$$

In three dimensions, with Cartesian coordinates $(x,y,z),$

$$\Delta f=\frac{\partial^2 f}{\partial x^2}+\frac{\partial^2 f}{\partial y^2}+\frac{\partial^2 f}{\partial z^2} \tag{2}$$

and in two dimensions,

$$\Delta f=\frac{\partial^2 f}{\partial x^2}+\frac{\partial^2 f}{\partial y^2} \tag{3}$$

The notation $\nabla^2f$ is also common. The Laplacian is a scalar operator: it takes a scalar function and returns a scalar function. It is linear,

$$\Delta(af+bg)=a\,\Delta f+b\,\Delta g \tag{4}$$

for constants $a,b,$ and it is invariant under rotations and translations of the coordinate system. The invariance is not obvious from the coordinate sum, but it follows from the coordinate-free definition as the divergence of the gradient.

If $H_f$ is the Hessian matrix of second partial derivatives,

$$H_f=\begin{pmatrix}f_{xx}&f_{xy}&f_{xz}\\f_{yx}&f_{yy}&f_{yz}\\f_{zx}&f_{zy}&f_{zz}\end{pmatrix}$$

then

$$\Delta f=\operatorname{tr}(H_f) \tag{5}$$

The trace is the sum of the eigenvalues of the Hessian, and it does not depend on the orthonormal basis in which the matrix is expressed. This gives a basis-independent reading: the Laplacian is the sum of the second derivatives in any three mutually orthogonal directions. In particular, the coordinate formula is not tied to the $x,y,z$ axes.

The sign convention varies. Some authors, especially in geometry, define the Laplacian as $-\operatorname{div}(\nabla f),$ so that it is a nonnegative operator on a closed manifold. In this entry $\Delta f$ denotes the divergence of the gradient, the convention used in most treatments of partial differential equations and in the entries on [divergence](../divergence/) and [curl](../curl/). A sign change flips harmonic functions to their negatives but does not otherwise change the theory.

## What the Laplacian measures

The Laplacian compares the value of $f$ at a point with the average of $f$ over a small sphere centred there. Let $P$ be a point and let $S_r(P)$ be the sphere of radius $r$ centred at $P,$ with surface average

$$A_f(P,r)=\frac{1}{4\pi r^2}\iint_{S_r(P)}f\,dS \tag{6}$$

For a $C^2$ function, Taylor's formula gives

$$A_f(P,r)=f(P)+\frac{r^2}{6}\Delta f(P)+O(r^4) \tag{7}$$

in three dimensions, so

$$\Delta f(P)=\lim_{r\to0}\frac{6}{r^2}\left(A_f(P,r)-f(P)\right) \tag{8}$$

In $n$ dimensions the limit coefficient is $2n/r^2,$ because the second-order term in the expansion is $r^2\Delta f/(2n).$ The formula says that $\Delta f(P)$ is positive when the average of $f$ on a small sphere exceeds $f(P),$ negative when it falls below, and zero when the two agree to second order.

This is the reason the Laplacian appears in diffusion. If $u(x,t)$ is a temperature, then a point that is colder than its neighbourhood has a positive Laplacian and tends to warm up; a point that is hotter has a negative Laplacian and tends to cool. The heat equation

$$\frac{\partial u}{\partial t}=k\,\Delta u \qquad k>0 \tag{9}$$

makes this precise: the rate of change of temperature is proportional to the difference between the temperature at the point and the average around it.

The same comparison gives the maximum principle. A function with $\Delta f>0$ is subharmonic, and it cannot have an interior maximum: at an interior maximum the average over a small sphere is at most the value at the centre, so $\Delta f\le0.$ Similarly, a function with $\Delta f<0$ is superharmonic and cannot have an interior minimum. A harmonic function, with $\Delta f=0,$ can have neither, and on a bounded domain its maximum and minimum occur on the boundary.

## Harmonic functions

A function is harmonic on an open set if

$$\Delta f=0 \tag{10}$$

there. Harmonic functions are the solutions of Laplace's equation, and they are the equilibrium states of the heat equation and the electrostatic potential in a charge-free region.

Several examples are immediate from the definition.

+ $f(x,y)=x^2-y^2$ has $f_{xx}=2$ and $f_{yy}=-2,$ so $\Delta f=0.$ It is harmonic on $\mathbb{R}^2.$
+ $f(x,y)=e^x\cos y$ has $f_{xx}=e^x\cos y$ and $f_{yy}=-e^x\cos y,$ so $\Delta f=0.$
+ $f(x,y,z)=xyz$ has all three pure second derivatives equal to zero, so it is harmonic.
+ $f(x,y,z)=x^2+y^2+z^2$ has $\Delta f=6,$ so it is not harmonic. It is the square of the distance from the origin, and it is strictly subharmonic.
+ $f(x,y,z)=1/r,$ with $r=\sqrt{x^2+y^2+z^2},$ is harmonic on $\mathbb{R}^3\setminus\{0\}.$ A direct computation gives
  $$\Delta\left(\frac1r\right)=\frac{1}{r^2}\frac{d}{dr}\left(r^2\frac{d}{dr}\frac1r\right)=\frac{1}{r^2}\frac{d}{dr}(-1)=0 \tag{11}$$
  The singularity at the origin is essential: no value at the origin can make the function harmonic there in the classical sense.

The last example is the fundamental solution of the Laplacian in three dimensions. In two dimensions the corresponding radial solution is $\ln r,$ since

$$\Delta(\ln r)=\frac{1}{r}\frac{d}{dr}\left(r\frac{d}{dr}\ln r\right)=\frac{1}{r}\frac{d}{dr}(1)=0 \tag{12}$$

A distributional formulation replaces the singularity by a delta function: $\Delta(-1/(4\pi r))=\delta_0$ in $\mathbb{R}^3,$ and $\Delta((1/2\pi)\ln r)=\delta_0$ in $\mathbb{R}^2.$ The constants are chosen so that the flux through a small sphere or circle is one.

Harmonic functions have strong regularity and rigidity properties. They are smooth, indeed real analytic, even if initially assumed only twice differentiable. They satisfy the mean value property

$$f(P)=\frac{1}{4\pi r^2}\iint_{S_r(P)}f\,dS \tag{13}$$

for every sphere contained in the domain, and the maximum principle stated above. Conversely, a continuous function with the mean value property on every sufficiently small sphere is harmonic, so the property characterizes harmonic functions among continuous functions.

## Green's identities

The Laplacian interacts with integration by parts through Green's identities. Let $\Omega$ be a bounded domain with piecewise smooth boundary $\partial\Omega$ and outward normal $\mathbf{n},$ and let $f,g$ be $C^2$ on a neighbourhood of the closure. The divergence theorem applied to the field $f\nabla g$ gives

$$\iiint_\Omega\left(f\,\Delta g+\nabla f\cdot\nabla g\right)dV=\iint_{\partial\Omega}f\frac{\partial g}{\partial n}\,dS \tag{14}$$

where $\partial g/\partial n=\nabla g\cdot\mathbf{n}$ is the normal derivative. Interchanging $f$ and $g$ and subtracting gives

$$\iiint_\Omega\left(f\,\Delta g-g\,\Delta f\right)dV=\iint_{\partial\Omega}\left(f\frac{\partial g}{\partial n}-g\frac{\partial f}{\partial n}\right)dS \tag{15}$$

These are the first and second Green identities. They are the integration-by-parts formulas for the Laplacian, and they underlie the variational formulation of Laplace's equation, uniqueness of boundary value problems, and the method of Green's functions.

A consequence of (14) with $f=g$ is that

$$\iiint_\Omega\left(\lVert\nabla f\rVert^2+f\,\Delta f\right)dV=\iint_{\partial\Omega}f\frac{\partial f}{\partial n}\,dS \tag{16}$$

If $f$ is harmonic and vanishes on the boundary, then the right side is zero and the first term is nonnegative, so $\nabla f=\mathbf{0}$ and $f=0.$ This proves uniqueness for the Dirichlet problem: a harmonic function is determined by its boundary values.

## Coordinate expressions

The Cartesian sum (2) is not the whole story. In cylindrical coordinates $(r,\theta,z),$ with $f=f(r,\theta,z),$

$$\Delta f=\frac{1}{r}\frac{\partial}{\partial r}\left(r\frac{\partial f}{\partial r}\right)+\frac{1}{r^2}\frac{\partial^2 f}{\partial\theta^2}+\frac{\partial^2 f}{\partial z^2} \tag{17}$$

In spherical coordinates $(\rho,\theta,\varphi),$ with $\varphi$ the polar angle measured from the positive $z$-axis and $\theta$ the azimuth,

$$\Delta f=\frac{1}{\rho^2}\frac{\partial}{\partial\rho}\left(\rho^2\frac{\partial f}{\partial\rho}\right)+\frac{1}{\rho^2\sin\varphi}\frac{\partial}{\partial\varphi}\left(\sin\varphi\frac{\partial f}{\partial\varphi}\right)+\frac{1}{\rho^2\sin^2\varphi}\frac{\partial^2 f}{\partial\theta^2} \tag{18}$$

The factors are metric factors, not optional corrections. A coordinate box in cylindrical coordinates has side lengths $dr,$ $r\,d\theta$ and $dz;$ in spherical coordinates its sides are $d\rho,$ $\rho\,d\varphi$ and $\rho\sin\varphi\,d\theta.$ The divergence of the gradient in these coordinates produces the displayed factors.

For a radially symmetric function in three dimensions, $f=f(\rho),$ the angular terms vanish and

$$\Delta f=\frac{1}{\rho^2}\frac{d}{d\rho}\left(\rho^2f'(\rho)\right)=f''(\rho)+\frac{2}{\rho}f'(\rho) \tag{19}$$

Setting this equal to zero gives

$$\rho^2f'(\rho)=A \qquad f(\rho)=B+\frac{C}{\rho} \tag{20}$$

which recovers the harmonic radial functions. In two dimensions the corresponding equation is

$$\frac{1}{r}\frac{d}{dr}\left(rf'(r)\right)=0 \qquad f(r)=A\ln r+B \tag{21}$$

The difference between $\ln r$ and $1/r$ is the difference between the planar and spatial fundamental solutions, and it explains why two-dimensional potential theory has logarithmic rather than inverse-distance potentials.

## A boundary value problem

Consider the annulus $1\le\rho\le2$ in $\mathbb{R}^3,$ with boundary values

$$f=1 \quad \text{on } \rho=1 \qquad f=0 \quad \text{on } \rho=2$$

and no dependence on the angles. A radial harmonic function has the form $f(\rho)=B+C/\rho.$ The boundary conditions give

$$B+C=1 \qquad B+\frac{C}{2}=0$$

Subtracting the second equation from the first gives $C/2=1,$ so $C=2$ and $B=-1.$ Hence

$$f(\rho)=\frac{2}{\rho}-1 \tag{22}$$

At $\rho=1$ the value is $1,$ at $\rho=2$ it is $0,$ and $\Delta f=0$ for $\rho>0$ by (20). The solution is unique by the maximum principle: two harmonic functions with the same boundary values would have a difference that is harmonic, continuous on the closed annulus and zero on both boundary components, so its maximum and minimum are both zero.

The example shows how the Laplacian selects a function from its boundary data. The differential equation alone has infinitely many solutions, since $B$ and $C$ are free; the boundary conditions fix the two constants. On an unbounded domain, a condition at infinity would replace one of the boundary conditions.

## The vector Laplacian

For a vector field $\mathbf{F}=\langle P,Q,R\rangle$ of class $C^2,$ the vector Laplacian is defined in Cartesian coordinates by applying the scalar Laplacian to each component:

$$\Delta\mathbf{F}=\langle\Delta P,\Delta Q,\Delta R\rangle \tag{23}$$

It is related to the first-order operators by

$$\Delta\mathbf{F}=\nabla(\operatorname{div}\mathbf{F})-\operatorname{curl}(\operatorname{curl}\mathbf{F}) \tag{24}$$

The identity is a vector analogue of the scalar identity $\Delta f=\operatorname{div}(\nabla f),$ and it is the reason the vector Laplacian cannot be computed by applying the scalar Laplacian to the components in curvilinear coordinates. In Cartesian coordinates the two definitions agree; in curvilinear coordinates the componentwise formula (23) must be replaced by (24), because the basis vectors themselves vary from point to point.

The identity also shows that a vector field with both zero divergence and zero curl is harmonic in the vector sense. In a simply connected region such a field is the gradient of a harmonic function and, locally, the curl of a vector potential, a structure that appears in the decomposition of fields into longitudinal and transverse parts.

## Where the Laplacian appears

The Laplacian is the spatial part of the most common linear partial differential equations.

+ Laplace's equation $\Delta f=0$ describes equilibrium temperature, electrostatic potential in a charge-free region, and irrotational incompressible flow.
+ Poisson's equation $\Delta f=\rho$ describes the same potentials with a source density $\rho.$
+ The heat equation $u_t=k\Delta u$ describes diffusion of heat or of a concentration.
+ The wave equation $u_{tt}=c^2\Delta u$ describes propagation of sound, light and vibrations.
+ The Schrödinger equation contains $-\Delta$ as the kinetic energy operator.

In each case the Laplacian is the coordinate-invariant second-order operator that compares a point with its surroundings. The boundary conditions, not the operator alone, determine the solution, and the maximum principle and Green's identities are the basic tools for studying them.

## Pitfalls

+ The sign convention is not universal. A harmonic function satisfies $\Delta f=0$ in either convention, but subharmonic and superharmonic are reversed if the sign is changed.
+ The Laplacian is a scalar operator. Applying it to a vector field requires either the componentwise definition in Cartesian coordinates or the vector identity (24); the two are not interchangeable in curvilinear coordinates.
+ The coordinate formulas (17) and (18) include metric factors. The expression $f_{rr}+f_{\theta\theta}+f_{zz}$ is not the Laplacian in cylindrical coordinates.
+ A harmonic function need not be constant. The maximum principle says that a nonconstant harmonic function on a bounded domain attains its extrema on the boundary, not that it has no variation.
+ The maximum principle requires a bounded domain and continuity on the closure. On an unbounded domain, growth conditions at infinity are needed.
+ The equation $\Delta f=0$ alone does not determine $f.$ Boundary values, or conditions at infinity, are part of the problem.
+ The fundamental solutions $1/r$ and $\ln r$ are harmonic only away from the singularity. Extending them to the singular point requires a distributional interpretation.

## Related notions

The Laplacian is the divergence of the gradient, so it combines the two operators developed in the entries on [divergence](../divergence/) and [vector fields](../vector-fields/). Its curl relation (24) connects it to the [curl](../curl/). Harmonic functions are the solutions of Laplace's equation, and the mean value property links them to integrals over spheres, which are evaluated with [spherical coordinates](../spherical-coordinates/). The [triple integral](../triple-integrals/) and the divergence theorem supply the integral identities used above.
