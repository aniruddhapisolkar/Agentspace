---
title: Curl
source: https://algebrica.org/curl/
license: CC BY-NC 4.0
tags:
  - circulation
  - conservative-fields
  - curl
  - irrotational-fields
  - multivariable-calculus
  - stokes-theorem
  - vector-calculus
---

## Circulation around a point

The divergence measures how a field spreads out from a point. The curl measures how it turns around a point. A field can flow steadily from left to right and still have curl, because the speed changes from one layer to the next; a paddlewheel placed in such a flow turns even though the arrows are parallel. The curl is the vector that records this local rotation, with both an axis and a magnitude.

Let $\mathbf{F}(x,y,z)=\langle P,Q,R\rangle$ be a vector field of class $C^1$ on an open set $D\subseteq\mathbb{R}^3.$ The curl of $\mathbf{F}$ is the vector field

$$\operatorname{curl}\mathbf{F}=\nabla\times\mathbf{F}=\begin{vmatrix}\mathbf{i}&\mathbf{j}&\mathbf{k}\\[2pt]\dfrac{\partial}{\partial x}&\dfrac{\partial}{\partial y}&\dfrac{\partial}{\partial z}\\[6pt]P&Q&R\end{vmatrix} \tag{1}$$

Expanding the determinant along the first row gives

$$\operatorname{curl}\mathbf{F}=\left\langle\frac{\partial R}{\partial y}-\frac{\partial Q}{\partial z},\ \frac{\partial P}{\partial z}-\frac{\partial R}{\partial x},\ \frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}\right\rangle \tag{2}$$

The determinant is a mnemonic, not a literal determinant: the entries of the first row are vectors and the entries of the second row are operators. The expansion is valid because the operators act on the components in the third row in the order indicated.

In the plane, with $\mathbf{F}=\langle P(x,y),Q(x,y)\rangle,$ the curl has only a $z$-component:

$$\operatorname{curl}\mathbf{F}=\left( \frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y} \right)\mathbf{k} \tag{3}$$

The scalar factor is often called the scalar curl or the two-dimensional curl. It is a real-valued function, while the three-dimensional curl is a vector field. The two are related by embedding the planar field as $\langle P,Q,0\rangle$ in space, for which (2) gives exactly (3) in the third component and zero in the other two.

The curl is defined for a vector field, not for a scalar function. The gradient is defined for a scalar function, and the two operations are linked by the identity $\operatorname{curl}(\nabla f)=\mathbf{0},$ discussed below.

## Circulation density

The coordinate formula has a circulation interpretation. Consider a small rectangle in the $xy$-plane with corners $(x,y),$ $(x+\Delta x,y),$ $(x+\Delta x,y+\Delta y)$ and $(x,y+\Delta y),$ traversed counterclockwise. The circulation of $\mathbf{F}=\langle P,Q,R\rangle$ around its boundary is approximately

$$\begin{aligned}
&\int_{\text{bottom}}P\,dx+\int_{\text{right}}Q\,dy-\int_{\text{top}}P\,dx-\int_{\text{left}}Q\,dy\\[4pt]
&\approx \left[P(x,y)-P(x,y+\Delta y)\right]\Delta x+\left[Q(x+\Delta x,y)-Q(x,y)\right]\Delta y\\[4pt]
&\approx \left(\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}\right)\Delta x\,\Delta y
\end{aligned} \tag{4}$$

Dividing by the area $\Delta x\,\Delta y$ and letting the rectangle shrink gives

$$\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}=\lim_{\Delta A\to0}\frac{1}{\Delta A}\oint_{\partial R}\mathbf{F}\cdot d\mathbf{r} \tag{5}$$

The scalar curl is therefore the circulation per unit area in the $xy$-plane, with counterclockwise orientation viewed from the positive $z$-axis. The other two components of (2) are the corresponding circulation densities in the $yz$- and $zx$-planes. The vector (2) combines the three plane densities, and its direction is the axis about which the local circulation is greatest.

The sign is fixed by the right-hand rule. If the fingers of the right hand curl in the direction of positive circulation, the thumb points along the curl vector. Reversing the orientation of the loop reverses the sign of the circulation and hence of the corresponding component.

## Rigid rotation and shear

For a rigid rotation about the $z$-axis with angular velocity $\omega,$ the velocity field is

$$\mathbf{F}(x,y,z)=\langle-\omega y,\ \omega x,\ 0\rangle \tag{6}$$

Its curl is

$$\operatorname{curl}\mathbf{F}=\left\langle0,\,0,\,\frac{\partial(\omega x)}{\partial x}-\frac{\partial(-\omega y)}{\partial y}\right\rangle=\langle0,0,2\omega\rangle \tag{7}$$

The curl points along the axis of rotation and its magnitude is twice the angular velocity. More generally, for a rigid body with angular velocity vector $\boldsymbol{\omega},$ the velocity is $\mathbf{v}=\boldsymbol{\omega}\times\mathbf{r},$ and a direct computation gives

$$\operatorname{curl}\mathbf{v}=2\boldsymbol{\omega} \tag{8}$$

The factor $2$ is a convention of the curl. The antisymmetric part of the velocity gradient is the angular velocity of the local rigid motion, and the curl is twice that angular velocity. A small element of the body therefore contributes circulation at twice its rate of rotation.

The shear field

$$\mathbf{F}(x,y,z)=\langle y,0,0\rangle \tag{9}$$

has parallel horizontal arrows whose length increases with $y.$ Its curl is

$$\operatorname{curl}\mathbf{F}=\left\langle0,\,0,\,\frac{\partial(0)}{\partial x}-\frac{\partial y}{\partial y}\right\rangle=\langle0,0,-1\rangle \tag{10}$$

The field has no closed orbits, yet its curl is nonzero. A paddlewheel with its axis along $z$ turns clockwise: the upper arrows push harder than the lower ones. This example shows that curl is not the same as the presence of circular arrows. It measures the antisymmetric part of the local linear approximation, not the global shape of the trajectories.

A radial field $\mathbf{F}=g(r)\langle x,y,z\rangle$ with $g$ depending only on $r=\lVert\mathbf{r}\rVert$ has zero curl away from the origin. Each component of the curl is a difference of terms such as $g'(r)yz/r-g'(r)zy/r,$ which cancel. The field points away from or toward the origin, and a paddlewheel placed in it does not turn.

## Gradient fields have zero curl

Let $f$ be a scalar function of class $C^2$ on an open set. Then

$$\operatorname{curl}(\nabla f)=\mathbf{0} \tag{11}$$

For the first component,

$$\frac{\partial}{\partial y}\left(\frac{\partial f}{\partial z}\right)-\frac{\partial}{\partial z}\left(\frac{\partial f}{\partial y}\right)=f_{zy}-f_{yz}=0$$

by equality of mixed partials, and the other components vanish in the same way. Hence every gradient field is irrotational.

The converse is not automatic. If $\operatorname{curl}\mathbf{F}=\mathbf{0}$ on a simply connected domain, then $\mathbf{F}$ is a gradient field on that domain. The standard obstruction is the punctured plane. The field

$$\mathbf{F}(x,y)=\left\langle-\frac{y}{x^2+y^2},\ \frac{x}{x^2+y^2}\right\rangle \tag{12}$$

has zero scalar curl on $\mathbb{R}^2\setminus\{(0,0)\},$ but its integral around the unit circle is $2\pi,$ so it cannot be a gradient there. The hole prevents the local potentials from patching into a single global one. On a simply connected domain, no such obstruction exists, and the converse holds.

The two identities

$$\operatorname{curl}(\nabla f)=\mathbf{0} \qquad \operatorname{div}(\operatorname{curl}\mathbf{F})=0 \tag{13}$$

are the fundamental compatibility conditions of vector calculus. The first says that a gradient has no rotation; the second, discussed in the entry on [divergence](../divergence/), says that a curl has no expansion. They are the reason potential functions and vector potentials exist locally, and they organize the hypotheses of the integral theorems.

## Stokes' theorem

The global form of the circulation density is Stokes' theorem. Let $S$ be an oriented piecewise smooth surface whose boundary $C=\partial S$ is a simple closed piecewise smooth curve. Give $C$ the orientation induced by the normal $\mathbf{n}$ of $S$ through the right-hand rule. Let $\mathbf{F}$ be a $C^1$ vector field on an open set containing $S.$ Then

$$\iint_S(\operatorname{curl}\mathbf{F})\cdot\mathbf{n}\,dS=\oint_C\mathbf{F}\cdot d\mathbf{r} \tag{14}$$

The left side integrates the normal component of the curl over the surface; the right side integrates the tangential component of the field around the boundary. The theorem says that the total circulation around the boundary equals the total flux of curl through any surface spanning it.

For a planar region in the $xy$-plane with normal $\mathbf{k}$ and counterclockwise boundary, (14) reduces to Green's theorem:

$$\iint_D\left(\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}\right)dA=\oint_C P\,dx+Q\,dy \tag{15}$$

Stokes' theorem therefore contains Green's theorem as the flat case. It also shows that the surface integral depends only on the boundary: two surfaces with the same oriented boundary give the same flux of curl, provided both satisfy the hypotheses.

The proof for a graph surface partitions the surface into small patches, applies the planar Green theorem to the projection of each patch, and sums. The boundary terms on interior edges cancel, leaving the integral over the outer boundary. The general case follows by patching graph surfaces together. The partition argument requires the surface to be piecewise smooth and the field to be $C^1$ on a neighbourhood of it.

## A Stokes calculation

Let $S$ be the unit disk in the plane $z=0,$ oriented with normal $\mathbf{k},$ and let

$$\mathbf{F}(x,y,z)=\langle z,x,y\rangle$$

The curl is

$$\operatorname{curl}\mathbf{F}=\left\langle\frac{\partial y}{\partial y}-\frac{\partial x}{\partial z},\ \frac{\partial z}{\partial z}-\frac{\partial y}{\partial x},\ \frac{\partial x}{\partial x}-\frac{\partial z}{\partial y}\right\rangle=\langle1,1,1\rangle$$

On the disk, $\mathbf{n}=\mathbf{k},$ so $(\operatorname{curl}\mathbf{F})\cdot\mathbf{n}=1$ and

$$\iint_S(\operatorname{curl}\mathbf{F})\cdot\mathbf{n}\,dS=\pi$$

The boundary is the unit circle, oriented counterclockwise when viewed from above:

$$\mathbf{r}(t)=\langle\cos t,\sin t,0\rangle \qquad 0\le t\le2\pi$$

Along the curve, $\mathbf{F}(\mathbf{r}(t))=\langle0,\cos t,\sin t\rangle$ and $\mathbf{r}'(t)=\langle-\sin t,\cos t,0\rangle,$ so

$$\mathbf{F}\cdot\mathbf{r}'=\cos^2t$$

and

$$\oint_C\mathbf{F}\cdot d\mathbf{r}=\int_0^{2\pi}\cos^2t\,dt=\pi$$

The two sides agree. The same boundary can be spanned by the upper hemisphere; the flux of $\langle1,1,1\rangle$ through the hemisphere is also $\pi,$ because the vector field is constant and the flux depends only on the projected area. Stokes' theorem guarantees the agreement without a separate surface integral.

## Curl in curvilinear coordinates

In cylindrical coordinates $(r,\theta,z),$ with $\mathbf{F}=F_r\,\mathbf{e}_r+F_\theta\,\mathbf{e}_\theta+F_z\,\mathbf{e}_z,$

$$\operatorname{curl}\mathbf{F}=\left(\frac{1}{r}\frac{\partial F_z}{\partial\theta}-\frac{\partial F_\theta}{\partial z}\right)\mathbf{e}_r+\left(\frac{\partial F_r}{\partial z}-\frac{\partial F_z}{\partial r}\right)\mathbf{e}_\theta+\frac{1}{r}\left(\frac{\partial(rF_\theta)}{\partial r}-\frac{\partial F_r}{\partial\theta}\right)\mathbf{e}_z \tag{16}$$

In spherical coordinates $(\rho,\theta,\varphi),$ with the convention of the [spherical coordinates](../spherical-coordinates/) entry, $\mathbf{F}=F_\rho\,\mathbf{e}_\rho+F_\varphi\,\mathbf{e}_\varphi+F_\theta\,\mathbf{e}_\theta$ and

$$\begin{aligned}
\operatorname{curl}\mathbf{F}={}&\frac{1}{\rho\sin\varphi}\left(\frac{\partial(\sin\varphi\,F_\theta)}{\partial\varphi}-\frac{\partial F_\varphi}{\partial\theta}\right)\mathbf{e}_\rho\\[4pt]
&+\frac{1}{\rho}\left(\frac{1}{\sin\varphi}\frac{\partial F_\rho}{\partial\theta}-\frac{\partial(\rho F_\theta)}{\partial\rho}\right)\mathbf{e}_\varphi\\[4pt]
&+\frac{1}{\rho}\left(\frac{\partial(\rho F_\varphi)}{\partial\rho}-\frac{\partial F_\rho}{\partial\varphi}\right)\mathbf{e}_\theta
\end{aligned} \tag{17}$$

The factors reflect the changing directions of the basis vectors. As with the divergence, substituting the Cartesian partial derivatives into (2) after expressing the field in the new coordinates does not give the displayed formulas unless the derivatives of the basis vectors are included.

The formulas can be checked on the rigid rotation (6). In cylindrical coordinates, $F_\theta=r\omega$ and the other components vanish, so the $z$-component of (16) is

$$\frac{1}{r}\frac{\partial(r\cdot r\omega)}{\partial r}=\frac{1}{r}\cdot2r\omega=2\omega$$

which agrees with (7).

## Product rules

For a scalar function $f$ and a vector field $\mathbf{F},$

$$\operatorname{curl}(f\mathbf{F})=f\operatorname{curl}\mathbf{F}+\nabla f\times\mathbf{F} \tag{18}$$

The order of the cross product matters. For two vector fields,

$$\operatorname{curl}(\mathbf{F}\times\mathbf{G})=\mathbf{F}(\operatorname{div}\mathbf{G})-\mathbf{G}(\operatorname{div}\mathbf{F})+(\mathbf{G}\cdot\nabla)\mathbf{F}-(\mathbf{F}\cdot\nabla)\mathbf{G} \tag{19}$$

where $(\mathbf{G}\cdot\nabla)\mathbf{F}$ denotes the directional derivative of $\mathbf{F}$ along $\mathbf{G}.$ Both rules require the relevant second derivatives to exist when they are iterated.

A useful consequence is the identity

$$\operatorname{curl}(\operatorname{curl}\mathbf{F})=\nabla(\operatorname{div}\mathbf{F})-\Delta\mathbf{F} \tag{20}$$

where $\Delta\mathbf{F}$ is the vector Laplacian, applied componentwise in Cartesian coordinates. The identity is the reason the vector Laplacian can be written as the gradient of the divergence minus the curl of the curl, and it is used in the entry on the [Laplacian](../laplacian/).

## Worked example

Consider

$$\mathbf{F}(x,y,z)=\langle x^2y,\ yz,\ x+z^2\rangle$$

The components are polynomials, so the field is smooth. The curl is

$$\operatorname{curl}\mathbf{F}=\left\langle\frac{\partial(x+z^2)}{\partial y}-\frac{\partial(yz)}{\partial z},\ \frac{\partial(x^2y)}{\partial z}-\frac{\partial(x+z^2)}{\partial x},\ \frac{\partial(yz)}{\partial x}-\frac{\partial(x^2y)}{\partial y}\right\rangle$$

which simplifies to

$$\operatorname{curl}\mathbf{F}=\langle-y,\,-1,\,-x^2\rangle$$

At $(1,2,3)$ this is $\langle-2,-1,-1\rangle.$ A paddlewheel placed there with its axis along $\langle-2,-1,-1\rangle$ would turn fastest; the magnitude $\sqrt6$ gives the maximum circulation density.

For the planar field $\mathbf{G}(x,y)=\langle x^2+y,\ xy\rangle,$ the scalar curl is

$$\frac{\partial(xy)}{\partial x}-\frac{\partial(x^2+y)}{\partial y}=y-1$$

At $(2,3)$ it is $2,$ so the field circulates counterclockwise there. At points with $y<1$ the local circulation is clockwise.

## What curl does not say

+ The curl is a vector in space and a scalar in the plane. The planar scalar curl is not a component to be added to a two-dimensional vector; it is the whole curl, pointing out of the plane.
+ A field with zero curl need not be conservative unless the domain is simply connected. The punctured-plane field (12) is the standard counterexample.
+ A field with nonzero curl is definitely not a gradient on any domain containing the point, since (11) would be violated.
+ Parallel arrows do not imply zero curl. The shear field (9) has parallel arrows and constant nonzero curl.
+ Circular arrows do not imply nonzero curl. A radial field can have curved-looking trajectories in a diagram while its curl vanishes.
+ Stokes' theorem requires a consistent orientation of surface and boundary. Reversing the normal reverses the sign of the surface integral and of the boundary circulation; using opposite conventions for the two sides produces a sign error, not a contradiction.
+ In curvilinear coordinates, the metric factors in (16) and (17) are part of the operator. Dropping them gives an expression that is not the curl.

## Related notions

The curl is the circulation density of a [vector field](../vector-fields/); its companion is the [divergence](../divergence/), the flux density. A field with zero curl is irrotational, and on a simply connected domain it has a potential function. Stokes' theorem relates the curl to [line integrals](../line-integrals/) around the boundary, while the divergence theorem relates the divergence to flux through a closed surface. The [Laplacian](../laplacian/) combines the two operators through $\Delta\mathbf{F}=\nabla(\operatorname{div}\mathbf{F})-\operatorname{curl}(\operatorname{curl}\mathbf{F}).$
