---
title: Cylindrical Coordinates
source: https://algebrica.org/cylindrical-coordinates/
license: CC BY-NC 4.0
tags:
  - coordinate-systems
  - cylindrical-coordinates
  - jacobian
  - multivariable-calculus
  - triple-integral
  - volume-element
---

## From polar to cylindrical coordinates

Polar coordinates describe a point in the plane by its distance from the origin and its angle from a fixed ray. Cylindrical coordinates add a third coordinate that measures height above or below the plane. The result is a coordinate system adapted to solids with rotational symmetry about an axis.

Let $P=(x,y,z)$ be a point in space and let $Q=(x,y,0)$ be its projection onto the $xy$-plane. The cylindrical coordinates of $P$ are

$$(r,\theta,z)$$

where $r$ is the distance from $Q$ to the origin, $\theta$ is the angle from the positive $x$-axis to the segment $OQ$, measured anticlockwise, and $z$ is the signed height of $P$ above the plane. Equivalently, $r$ is the distance from $P$ to the $z$-axis.

The Cartesian coordinates are recovered by the map

$$x=r\cos\theta \qquad y=r\sin\theta \qquad z=z \tag{1}$$

and the inverse relations are

$$r=\sqrt{x^2+y^2} \qquad \theta=\operatorname{atan2}(y,x) \qquad z=z \tag{2}$$

where $\operatorname{atan2}(y,x)$ is the angle in $(-\pi,\pi]$ determined by the signs of $x$ and $y$. The standard range is

$$r\ge0 \qquad 0\le\theta<2\pi \qquad z\in\mathbb{R} \tag{3}$$

The representation is not unique on the $z$-axis: there $r=0$ and every value of $\theta$ gives the same point. It is also periodic in $\theta$, since $\theta$ and $\theta+2\pi$ describe the same half-plane. These ambiguities do not affect integrals, because the axis and a half-plane have zero volume, but they matter when a region is described by inequalities.

Cylindrical coordinates are the three-dimensional extension of the [polar coordinates](../polar-coordinates/) of the plane. Setting $z=0$ recovers the polar description of the $xy$-plane. The new coordinate is not the distance from the origin; that distance is $\sqrt{r^2+z^2}$ and belongs to [spherical coordinates](../spherical-coordinates/).

## Coordinate surfaces

Holding one coordinate fixed produces a surface, and these surfaces explain which solids are easy to describe.

+ $r=a$ is the cylinder of radius $a$ about the $z$-axis, consisting of the points whose distance from the axis is $a$.
+ $\theta=\alpha$ is the half-plane bounded by the $z$-axis, containing the ray at angle $\alpha$ in the $xy$-plane.
+ $z=c$ is the horizontal plane at height $c$.
+ $z=r$ is the cone with vertex at the origin and axis the positive $z$-axis, since $r=\sqrt{x^2+y^2}$.
+ $z=r^2$ is the paraboloid of revolution opening upward.

A solid is described in cylindrical coordinates by inequalities on $r,\theta,z$. A circular cylinder of radius $R$ and height $H$ is $0\le r\le R$, $0\le\theta<2\pi$, $0\le z\le H$. A cone of base radius $R$ and height $H$ with vertex at the origin is $0\le r\le R$, $0\le z\le H(1-r/R)$, or equivalently $0\le r\le H-z$ when $R=H$. A ball of radius $R$ is $0\le r\le R$, $0\le z\le\sqrt{R^2-r^2}$ together with the symmetric lower half; the description is possible but less natural than in spherical coordinates.

The angle $\theta$ is often absent from the inequalities because the solid is invariant under rotation. In that case the $\theta$-integral simply contributes a factor $2\pi$, or the angular width of the sector if the solid occupies only part of the full turn.

## The volume element

The map (1) has Jacobian matrix

$$D\Phi(r,\theta,z)=\begin{pmatrix}\cos\theta&-r\sin\theta&0\\ \sin\theta&r\cos\theta&0\\ 0&0&1\end{pmatrix}$$

Its determinant is

$$\det D\Phi=r\cos^2\theta+r\sin^2\theta=r \tag{4}$$

The determinant is nonnegative on the standard range $r\ge0$, so the absolute value is $r$. By the [change of variables](../change-of-variables-in-multiple-integrals/) theorem,

$$dx\,dy\,dz=r\,dr\,d\theta\,dz \tag{5}$$

The factor $r$ has a direct geometric meaning. Consider the small volume spanned by increments $dr$, $d\theta$ and $dz$. The radial increment contributes a length $dr$; the angular increment contributes an arc length $r\,d\theta$ at distance $r$ from the axis; the vertical increment contributes $dz$. The three directions are mutually perpendicular, so the volume is the product

$$dV=(dr)(r\,d\theta)(dz)=r\,dr\,d\theta\,dz$$

At the axis $r=0$ the arc length vanishes, which is why the factor $r$ suppresses the contribution of the axis and of small neighbourhoods around it.

For a solid $D$ with cylindrical description $D'$, the integral of a function $f$ is

$$\iiint_D f(x,y,z)\,dV=\iiint_{D'} f(r\cos\theta,r\sin\theta,z)\,r\,dr\,d\theta\,dz \tag{6}$$

The integrand must be expressed in the new variables; the factor $r$ is part of the volume element, not part of the function.

## Setting up an integral

The procedure has four steps.

+ Sketch the solid and its projection onto the $xy$-plane.
+ Describe the projection in polar coordinates: the range of $\theta$ and, for each $\theta$, the range of $r$.
+ For each $(r,\theta)$ in the projection, determine the lower and upper values of $z$ from the bounding surfaces.
+ Write the integral with the volume element $r\,dr\,d\theta\,dz$ and evaluate, usually in the order $z$, then $r$, then $\theta$.

The order can be changed if the region is easier to describe another way, but the factor $r$ remains. A common error is to integrate $r$ from a function of $z$ while treating $z$ as the outer variable and then omit the Jacobian; the two mistakes can cancel numerically in special cases, which makes the error hard to detect.

## A cylinder

The volume of a circular cylinder of radius $R$ and height $H$ is

$$\int_0^{2\pi}\int_0^R\int_0^H r\,dz\,dr\,d\theta=2\pi\cdot\frac{R^2}{2}\cdot H=\pi R^2H$$

The same result follows from the elementary formula for the volume of a cylinder. The computation is a check on the volume element: without the factor $r$, the integral would give $2\pi RH$, which is an area, not a volume.

## A paraboloid

Find the volume of the solid bounded below by the paraboloid $z=x^2+y^2$ and above by the plane $z=4$.

In cylindrical coordinates the paraboloid is $z=r^2$. The two surfaces meet where $r^2=4$, so $r=2$. The solid is

$$0\le\theta<2\pi \qquad 0\le r\le2 \qquad r^2\le z\le4$$

Hence

$$V=\int_0^{2\pi}\int_0^2\int_{r^2}^{4}r\,dz\,dr\,d\theta=2\pi\int_0^2r(4-r^2)\,dr$$

The inner integral is

$$\int_0^2(4r-r^3)\,dr=\left[2r^2-\frac{r^4}{4}\right]_0^2=8-4=4$$

so

$$V=8\pi$$

As a check, the solid is the region under the plane $z=4$ minus the region under the paraboloid. The latter has volume

$$\int_0^{2\pi}\int_0^2\int_0^{r^2}r\,dz\,dr\,d\theta=2\pi\int_0^2r^3\,dr=2\pi\cdot4=8\pi$$

and the cylinder of radius $2$ and height $4$ has volume $16\pi$. The difference is $8\pi$, which agrees.

## A cone

The solid bounded below by the cone $z=\sqrt{x^2+y^2}$ and above by the plane $z=2$ has

$$0\le\theta<2\pi \qquad 0\le r\le2 \qquad r\le z\le2$$

Therefore

$$V=\int_0^{2\pi}\int_0^2\int_r^2 r\,dz\,dr\,d\theta=2\pi\int_0^2r(2-r)\,dr$$

$$=2\pi\left[r^2-\frac{r^3}{3}\right]_0^2=2\pi\left(4-\frac83\right)=\frac{8\pi}{3}$$

The cone has base radius $2$ and height $2$, so the elementary formula gives $\frac13\pi(2^2)(2)=8\pi/3$, in agreement.

## Mass with variable density

Let a solid cylinder be described by $0\le r\le1$, $0\le z\le2$, $0\le\theta<2\pi$, and let its density be $\rho(x,y,z)=z$. The mass is

$$M=\int_0^{2\pi}\int_0^1\int_0^2 z\,r\,dz\,dr\,d\theta$$

The integrals separate:

$$M=\left(\int_0^{2\pi}d\theta\right)\left(\int_0^1r\,dr\right)\left(\int_0^2z\,dz\right)=2\pi\cdot\frac12\cdot2=2\pi$$

The density increases with height, so the centre of mass lies above the mid-height $z=1$. The first moment in $z$ is

$$\int_0^{2\pi}\int_0^1\int_0^2 z^2\,r\,dz\,dr\,d\theta=2\pi\cdot\frac12\cdot\frac83=\frac{8\pi}{3}$$

and the centroid height is

$$\bar z=\frac{8\pi/3}{2\pi}=\frac43$$

which is indeed above the geometric centre.

## A sphere cut by a cylinder

Find the volume of the solid inside the sphere $x^2+y^2+z^2\le4$ and inside the cylinder $x^2+y^2\le1$.

The cylinder is $r\le1$. For each $(r,\theta)$ with $0\le r\le1$, the sphere gives

$$-\sqrt{4-r^2}\le z\le\sqrt{4-r^2}$$

so

$$V=\int_0^{2\pi}\int_0^1\int_{-\sqrt{4-r^2}}^{\sqrt{4-r^2}}r\,dz\,dr\,d\theta=2\pi\int_0^1 2r\sqrt{4-r^2}\,dr$$

The substitution $u=4-r^2$, $du=-2r\,dr$ gives

$$\int_0^1 2r\sqrt{4-r^2}\,dr=\int_3^4u^{1/2}\,du=\frac23\left(4^{3/2}-3^{3/2}\right)=\frac23(8-3\sqrt3)$$

Hence

$$V=\frac{4\pi}{3}(8-3\sqrt3)$$

The result is positive and less than the volume of the sphere, $\frac{32\pi}{3}$, as it must be. The example shows that cylindrical coordinates handle a solid whose top and bottom are graphs over a disc, even when the solid is not itself a cylinder.

## When to use cylindrical coordinates

Cylindrical coordinates are natural when the solid or the integrand is invariant under rotation about the $z$-axis and the boundary is expressed in terms of distance from that axis. Typical signals are:

+ the region is a cylinder, a cone, a paraboloid or a solid of revolution about the $z$-axis;
+ the integrand contains $x^2+y^2$ or $\sqrt{x^2+y^2}$;
+ the projection onto the $xy$-plane is a disc, an annulus or a circular sector;
+ the boundary surfaces are given by equations in $r$ and $z$.

If the boundary is naturally described by distance from the origin rather than distance from the axis, [spherical coordinates](../spherical-coordinates/) are usually simpler. A ball centred at the origin, for instance, has the compact spherical description $0\le\rho\le R$, whereas its cylindrical description requires a square root for $z$. If the solid has no rotational symmetry, Cartesian coordinates may be preferable.

## Pitfalls

Three errors recur in cylindrical integration.

**Omitting the Jacobian.** The volume element is $r\,dr\,d\theta\,dz$, not $dr\,d\theta\,dz$. The factor is not optional; it is the determinant of the coordinate map. In an integral whose integrand already contains an $r$, it is easy to absorb the wrong factor or to cancel one that should remain.

**Using the wrong radius.** In cylindrical coordinates $r$ is the distance from the $z$-axis. The distance from the origin is $\sqrt{r^2+z^2}$. A sphere centred at the origin is not $r=R$; that equation describes a cylinder. Confusing the two produces a solid with the wrong boundary.

**Ignoring the angular range.** The full turn $0\le\theta<2\pi$ applies only when the solid is rotationally symmetric. A half-cylinder or a sector has a shorter angular range, and using the full turn multiplies the volume by the wrong factor.

A fourth, subtler issue is the behaviour at $r=0$. The map is not one-to-one on the axis, and the inverse relation for $\theta$ is undefined there. Integrals are unaffected because the axis has zero volume, but a coordinate description that divides by $r$ or by $\sin\theta$ may fail on the axis even when the integral is finite.

## Relation to the other coordinate systems

Cylindrical coordinates sit between Cartesian and spherical coordinates. In the $xy$-plane they reduce to polar coordinates; in space they keep the vertical coordinate $z$ and measure horizontal distance from the axis. The spherical coordinates are related by

$$r=\rho\sin\varphi \qquad z=\rho\cos\varphi \qquad \theta=\theta \tag{7}$$

so a spherical description can be converted to a cylindrical one, and conversely. The volume elements reflect the different geometry: $r\,dr\,d\theta\,dz$ in cylindrical coordinates and $\rho^2\sin\varphi\,d\rho\,d\varphi\,d\theta$ in spherical coordinates.

Both elements are special cases of the [change of variables](../change-of-variables-in-multiple-integrals/) formula, and both integrals are evaluated by [Fubini's theorem](../fubinis-theorem/) after the coordinate change. The entry on [triple integrals](../triple-integrals/) develops the general reduction to iterated integrals; the present entry supplies the coordinate description and the factor that the reduction requires.
