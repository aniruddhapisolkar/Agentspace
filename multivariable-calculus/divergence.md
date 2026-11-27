---
title: Divergence
source: https://algebrica.org/divergence/
license: CC BY-NC 4.0
tags:
  - divergence
  - divergence-theorem
  - flux
  - incompressible-fields
  - multivariable-calculus
  - vector-calculus
---

## From flux to a local quantity

A vector field can be pictured as the velocity of a fluid. At a point where more fluid leaves a small region than enters it, the region acts as a source; at a point where more enters than leaves, it acts as a sink. The divergence is the scalar that measures this imbalance per unit volume. It converts a statement about flow across a closed surface into a statement about the field at a point.

Let $D\subseteq\mathbb{R}^3$ be an open set and let

$$\mathbf{F}(x,y,z)=P(x,y,z)\,\mathbf{i}+Q(x,y,z)\,\mathbf{j}+R(x,y,z)\,\mathbf{k}=\langle P,Q,R\rangle$$

be a vector field on $D.$ If the partial derivatives of the components exist, the divergence of $\mathbf{F}$ is the scalar field

$$\operatorname{div}\mathbf{F}=\frac{\partial P}{\partial x}+\frac{\partial Q}{\partial y}+\frac{\partial R}{\partial z} \tag{1}$$

The notation $\nabla\cdot\mathbf{F}$ is also standard, since the divergence is the formal dot product of the operator

$$\nabla=\mathbf{i}\frac{\partial}{\partial x}+\mathbf{j}\frac{\partial}{\partial y}+\mathbf{k}\frac{\partial}{\partial z}$$

with the field. In two dimensions, with $\mathbf{F}=\langle P,Q\rangle,$

$$\operatorname{div}\mathbf{F}=\frac{\partial P}{\partial x}+\frac{\partial Q}{\partial y} \tag{2}$$

The divergence is a scalar, not a vector. It takes a vector field and returns a real-valued function on the same domain. This is the first structural difference from the gradient, which takes a scalar function and returns a vector field.

If $\mathbf{F}$ is differentiable at a point, its Jacobian matrix is

$$D\mathbf{F}=\begin{pmatrix}P_x&P_y&P_z\\Q_x&Q_y&Q_z\\R_x&R_y&R_z\end{pmatrix}$$

and the divergence is the trace of this matrix:

$$\operatorname{div}\mathbf{F}=\operatorname{tr}(D\mathbf{F}) \tag{3}$$

The trace is independent of the orthonormal basis in which the matrix is written, so the divergence has a basis-independent meaning. It measures the total rate at which the linear approximation of $\mathbf{F}$ stretches volumes, with rotations contributing nothing to the trace.

## The infinitesimal box

The coordinate formula has a flux interpretation. Consider a small rectangular box centred at $P=(x,y,z),$ with side lengths $\Delta x,$ $\Delta y$ and $\Delta z.$ The flux of $\mathbf{F}$ through the two faces perpendicular to the $x$-axis is approximately

$$\left[P\left(x+\frac{\Delta x}{2},y,z\right)-P\left(x-\frac{\Delta x}{2},y,z\right)\right]\Delta y\,\Delta z \approx \frac{\partial P}{\partial x}\,\Delta x\,\Delta y\,\Delta z$$

where the normal is outward on both faces: positive in the $+x$ direction on the right face and negative on the left. The other two pairs of faces contribute the analogous terms with $Q_y$ and $R_z.$ Adding them and dividing by the volume $\Delta V=\Delta x\,\Delta y\,\Delta z$ gives

$$\frac{1}{\Delta V}\iint_{\partial B}\mathbf{F}\cdot\mathbf{n}\,dS\approx \frac{\partial P}{\partial x}+\frac{\partial Q}{\partial y}+\frac{\partial R}{\partial z} \tag{4}$$

As the box shrinks, the approximation improves, and for a field of class $C^1$ the limit is the divergence:

$$\operatorname{div}\mathbf{F}(P)=\lim_{\Delta V\to0}\frac{1}{\Delta V}\iint_{\partial B}\mathbf{F}\cdot\mathbf{n}\,dS \tag{5}$$

This is the coordinate-free definition: the divergence is the outward flux per unit volume in the limit of shrinking closed surfaces around the point. The mean value theorem makes the one-dimensional approximation exact at some intermediate point, and the continuity of the partial derivatives gives the limit.

The sign has a direct reading. A positive divergence at $P$ means that the field points away from $P$ on average, so $P$ is a source. A negative divergence means that the field points toward $P,$ so $P$ is a sink. Zero divergence means that the outward flux through every sufficiently small closed surface is negligible relative to its volume; the field neither creates nor destroys volume at that point.

## Examples

For the radial field $\mathbf{F}(x,y,z)=\langle x,y,z\rangle,$

$$\operatorname{div}\mathbf{F}=1+1+1=3$$

Every point is a source, and the field expands uniformly. For the rotational field $\mathbf{F}(x,y,z)=\langle-y,x,0\rangle,$

$$\operatorname{div}\mathbf{F}=0+0+0=0$$

The field circulates without spreading: what enters any small region leaves it. For the field $\mathbf{F}=\langle x^2,y^2,z^2\rangle,$

$$\operatorname{div}\mathbf{F}=2x+2y+2z$$

which changes sign across the plane $x+y+z=0.$ The field is a source where the sum is positive and a sink where it is negative.

The inverse-square field

$$\mathbf{F}(x,y,z)=\frac{\langle x,y,z\rangle}{(x^2+y^2+z^2)^{3/2}}=\frac{\mathbf{r}}{r^3}$$

has divergence zero away from the origin. Indeed, with $r=\sqrt{x^2+y^2+z^2},$

$$\frac{\partial}{\partial x}\left(\frac{x}{r^3}\right)=\frac{1}{r^3}-\frac{3x^2}{r^5}$$

and summing the three analogous terms gives

$$\operatorname{div}\mathbf{F}=\frac{3}{r^3}-\frac{3(x^2+y^2+z^2)}{r^5}=\frac{3}{r^3}-\frac{3}{r^3}=0 \tag{6}$$

The result is striking: the field points radially outward everywhere, yet its divergence vanishes at every point where it is defined. The resolution is that all of the source is concentrated at the origin, where the field is not defined. The flux through a sphere centred at the origin is $4\pi,$ independent of the radius, while the divergence integral over the region between two spheres is zero. The divergence theorem does not apply to a solid that contains the origin, because the field is not $C^1$ there.

A shear field such as $\mathbf{F}=\langle y,0,0\rangle$ also has zero divergence. Its arrows are horizontal, with length increasing with $y,$ and the flow slides layers past one another without compressing or expanding any small volume.

## The divergence theorem

The local information carried by the divergence and the global information carried by the flux through a closed surface are related by the divergence theorem.

Let $E$ be a solid whose boundary $S=\partial E$ is a piecewise smooth closed surface, oriented with outward normal $\mathbf{n}.$ Let $\mathbf{F}$ be a vector field of class $C^1$ on an open set containing $E.$ Then

$$\iiint_E\operatorname{div}\mathbf{F}\,dV=\iint_S\mathbf{F}\cdot\mathbf{n}\,dS \tag{7}$$

The left side integrates a scalar over a volume; the right side integrates the normal component of the field over the boundary. The theorem says that the total source strength inside $E$ equals the net outward flux through its boundary. It is the three-dimensional analogue of the fundamental theorem of calculus, with the divergence playing the role of the derivative and the boundary flux the role of the endpoint difference.

The proof for a box follows from the fundamental theorem of calculus. For the $x$-term,

$$\iiint_E\frac{\partial P}{\partial x}\,dV=\iint_{\partial E}P\,n_x\,dS$$

because integrating $\partial P/\partial x$ along each line parallel to the $x$-axis gives the difference of $P$ at the two endpoints, which are exactly the intersections with the boundary; the outward normal contributes the correct sign. Summing the three components gives (7) for a box. A general solid is partitioned into small boxes, the integrals over interior faces cancel because the outward normals are opposite, and the boundary integrals converge to the integral over $S.$ The partition argument requires the boundary to be piecewise smooth and the field to be $C^1$ on the solid.

The theorem fails if the field has a singularity inside $E.$ For the inverse-square field, the flux through any sphere centred at the origin is $4\pi,$ while the divergence integral over the ball minus the origin is zero. The missing contribution is concentrated at the singular point, and the theorem must be applied to the punctured solid, whose boundary has two components.

## Flux through a sphere

Let $S$ be the sphere of radius $R$ centred at the origin, with outward normal, and let $\mathbf{F}(x,y,z)=\langle x,y,z\rangle.$ On $S,$ the outward unit normal is $\mathbf{n}=\mathbf{r}/R,$ so

$$\mathbf{F}\cdot\mathbf{n}=\mathbf{r}\cdot\frac{\mathbf{r}}{R}=\frac{R^2}{R}=R$$

The flux is therefore

$$\iint_S\mathbf{F}\cdot\mathbf{n}\,dS=R\cdot4\pi R^2=4\pi R^3$$

The divergence theorem gives the same value:

$$\iiint_E\operatorname{div}\mathbf{F}\,dV=\iiint_E3\,dV=3\cdot\frac{4\pi R^3}{3}=4\pi R^3$$

The direct computation uses the geometry of the sphere; the theorem uses only the constant divergence. The agreement is a check on both.

For the unit radial field $\mathbf{F}=\mathbf{r}/r,$ the divergence is $2/r$ away from the origin. The flux through the sphere of radius $R$ is $4\pi R^2,$ since $\mathbf{F}\cdot\mathbf{n}=1.$ The volume integral is

$$\iiint_E\frac{2}{r}\,dV=\int_0^R\frac{2}{r}\,4\pi r^2\,dr=8\pi\int_0^Rr\,dr=4\pi R^2$$

which agrees. The integrand $2/r$ is unbounded at the origin but integrable in three dimensions, so the volume integral converges.

## Flux through a cube

Let $E=[0,1]^3$ and $\mathbf{F}=\langle0,0,z\rangle.$ Then $\operatorname{div}\mathbf{F}=1,$ so the divergence theorem gives flux $1.$

Directly, the only face with nonzero flux is the top face $z=1,$ where $\mathbf{n}=\langle0,0,1\rangle$ and $\mathbf{F}=\langle0,0,1\rangle,$ so $\mathbf{F}\cdot\mathbf{n}=1$ and the flux is $1.$ On the bottom face $\mathbf{F}=\mathbf{0};$ on the four side faces $\mathbf{n}$ is horizontal and $\mathbf{F}$ is vertical, so the dot product is zero. The two computations agree.

For $\mathbf{F}=\langle x^2,y^2,z^2\rangle$ on the same cube, $\operatorname{div}\mathbf{F}=2(x+y+z),$ and

$$\iiint_E2(x+y+z)\,dV=2\left(\frac12+\frac12+\frac12\right)=3$$

On the face $x=1,$ $\mathbf{F}\cdot\mathbf{n}=1;$ on $x=0$ it is $0.$ The same holds for the $y$ and $z$ faces, so the total flux is $3.$ Again the two sides agree.

## Product rules

The divergence satisfies a product rule for multiplication by a scalar function:

$$\operatorname{div}(f\mathbf{F})=f\operatorname{div}\mathbf{F}+\nabla f\cdot\mathbf{F} \tag{8}$$

For a scalar function $f$ and a vector field $\mathbf{F},$ the term $\nabla f\cdot\mathbf{F}$ is the directional derivative of $f$ along $\mathbf{F}.$ The rule follows by applying the ordinary product rule to each component and collecting terms.

For the cross product of two fields,

$$\operatorname{div}(\mathbf{F}\times\mathbf{G})=\mathbf{G}\cdot\operatorname{curl}\mathbf{F}-\mathbf{F}\cdot\operatorname{curl}\mathbf{G} \tag{9}$$

The signs are not symmetric, because the cross product is antisymmetric. Both rules require the relevant derivatives to exist and be continuous.

A useful consequence is that the divergence of a curl vanishes:

$$\operatorname{div}(\operatorname{curl}\mathbf{F})=0 \tag{10}$$

for a field of class $C^2,$ by equality of mixed partials. This identity is the companion of $\operatorname{curl}(\nabla f)=\mathbf{0}.$ Together they show that the gradient and curl form a complex, and that the complex is exact on suitable simply connected domains, which is the local reason potential functions and vector potentials exist.

## Divergence in curvilinear coordinates

The coordinate formula (1) is specific to Cartesian coordinates. In cylindrical coordinates $(r,\theta,z),$ with field components $\mathbf{F}=F_r\,\mathbf{e}_r+F_\theta\,\mathbf{e}_\theta+F_z\,\mathbf{e}_z,$

$$\operatorname{div}\mathbf{F}=\frac{1}{r}\frac{\partial}{\partial r}(rF_r)+\frac{1}{r}\frac{\partial F_\theta}{\partial\theta}+\frac{\partial F_z}{\partial z} \tag{11}$$

In spherical coordinates $(\rho,\theta,\varphi),$ with $\rho$ the distance from the origin, $\theta$ the azimuth and $\varphi$ the polar angle, and with components $\mathbf{F}=F_\rho\,\mathbf{e}_\rho+F_\varphi\,\mathbf{e}_\varphi+F_\theta\,\mathbf{e}_\theta,$

$$\operatorname{div}\mathbf{F}=\frac{1}{\rho^2}\frac{\partial}{\partial\rho}(\rho^2F_\rho)+\frac{1}{\rho\sin\varphi}\frac{\partial}{\partial\varphi}(\sin\varphi\,F_\varphi)+\frac{1}{\rho\sin\varphi}\frac{\partial F_\theta}{\partial\theta} \tag{12}$$

The factors are not optional. They arise because the coordinate basis vectors change direction from point to point, and because a coordinate box has side lengths $dr,$ $r\,d\theta$ and $dz$ in cylindrical coordinates, and $d\rho,$ $\rho\,d\varphi$ and $\rho\sin\varphi\,d\theta$ in spherical coordinates. Omitting them produces an expression that is not the divergence, even though it may look like a sum of partial derivatives.

The formulas can be recovered from the divergence theorem by applying it to a curvilinear box and letting the box shrink. For example, the radial term in (11) comes from the flux through the two cylindrical faces, whose areas are proportional to $r;$ differentiating $rF_r$ and dividing by $r$ gives the displayed factor.

## A two-dimensional reading

In the plane, the divergence of $\mathbf{F}=\langle P,Q\rangle$ is $P_x+Q_y.$ The flux form of Green's theorem states that for a plane region $D$ with positively oriented boundary $C,$

$$\iint_D\left(\frac{\partial P}{\partial x}+\frac{\partial Q}{\partial y}\right)dA=\oint_C\mathbf{F}\cdot\mathbf{n}\,ds \tag{13}$$

where $\mathbf{n}$ is the outward normal to $C.$ This is the two-dimensional divergence theorem. It is often written with the normal derivative, and it shows that the planar theory has the same structure as the spatial one.

A planar field can be divergence-free without being constant. The field $\mathbf{F}=\langle y,-x\rangle$ has divergence $0$ and circulates around the origin. The field $\mathbf{F}=\langle x,-y\rangle$ has divergence $1-1=0$ and forms a saddle: it expands along the $x$-axis and contracts along the $y$-axis. In both cases the local expansion and contraction balance exactly.

## What divergence does not say

Several distinctions are easy to lose.

+ The divergence is a scalar. It cannot be added to a vector field, and it has no direction. The gradient, by contrast, is a vector field.
+ A zero divergence does not mean that the field is zero, constant or irrotational. It means only that the field is volume-preserving to first order. The rotational field and the shear field both have zero divergence and are not constant.
+ A nonzero divergence does not by itself determine the field. Many fields share the same divergence and differ by a divergence-free field.
+ The divergence theorem requires a closed surface with outward orientation and a field of class $C^1$ on the enclosed solid. An open surface has no enclosed volume, and an inward normal reverses the sign.
+ A singularity inside the surface invalidates the theorem on the full solid. The inverse-square field is the standard example: its divergence vanishes away from the origin, but its flux through a sphere is nonzero.
+ In curvilinear coordinates, the metric factors must be included. The Cartesian sum $F_{r,r}+F_{\theta,\theta}+F_{z,z}$ is not the divergence in cylindrical coordinates.

## Related notions

The divergence is one of two first-order differential operators on a vector field. The other is the [curl](../curl/), which measures rotation rather than expansion. The [Laplacian](../laplacian/) is the divergence of a gradient, $\Delta f=\operatorname{div}(\nabla f),$ and harmonic functions are those with zero Laplacian. The divergence theorem converts a [triple integral](../triple-integrals/) of a divergence into a flux integral over a surface; its planar analogue is the flux form of Green's theorem. Vector fields, gradient fields and potentials are introduced in the entry on [vector fields](../vector-fields/).
