---
title: Spherical Coordinates
source: https://algebrica.org/spherical-coordinates/
license: CC BY-NC 4.0
tags:
  - coordinate-systems
  - jacobian
  - multivariable-calculus
  - spherical-coordinates
  - triple-integral
  - volume-element
---

## Distance and two angles

Cylindrical coordinates describe a point by its distance from an axis and its height. Spherical coordinates describe it by its distance from the origin and two angles. The result is the coordinate system adapted to balls, spheres, cones and other regions with symmetry about a point.

Let $P=(x,y,z)$ be a point in space and let

$$\rho=\sqrt{x^2+y^2+z^2}$$

be its distance from the origin. Let $\theta$ be the azimuthal angle of the projection of $P$ onto the $xy$-plane, measured from the positive $x$-axis, and let $\varphi$ be the angle between the positive $z$-axis and the segment $OP$. The spherical coordinates of $P$ are

$$(\rho,\theta,\varphi)$$

The Cartesian coordinates are recovered by

$$x=\rho\sin\varphi\cos\theta \qquad y=\rho\sin\varphi\sin\theta \qquad z=\rho\cos\varphi \tag{1}$$

The inverse relations are

$$\rho=\sqrt{x^2+y^2+z^2} \qquad \theta=\operatorname{atan2}(y,x) \qquad \varphi=\arccos\left(\frac{z}{\rho}\right) \tag{2}$$

for $\rho>0$. The standard range is

$$\rho\ge0 \qquad 0\le\theta<2\pi \qquad 0\le\varphi\le\pi \tag{3}$$

The angle $\varphi$ is measured from the positive $z$-axis, not from the $xy$-plane. At $\varphi=0$ the point lies on the positive $z$-axis; at $\varphi=\pi/2$ it lies in the $xy$-plane; at $\varphi=\pi$ it lies on the negative $z$-axis. The azimuth $\theta$ is undefined on the $z$-axis, and both angles are undefined at the origin, where $\rho=0$.

The representation is not unique. The angle $\theta$ is periodic, so $(\rho,\theta,\varphi)$ and $(\rho,\theta+2\pi,\varphi)$ are the same point. On the $z$-axis every value of $\theta$ gives the same point. These ambiguities occur on sets of zero volume and do not affect integrals, but they must be respected when a region is described by inequalities.

The notation varies between subjects. In physics, $r$ often denotes the distance from the origin, $\theta$ the polar angle and $\varphi$ the azimuth; some texts use $\psi$ for the polar angle. In this entry $\rho$ is the distance from the origin, $\theta$ is the azimuth and $\varphi$ is the polar angle. The formulas below are stated for this convention, and the Jacobian is unchanged once the range of the polar angle is adjusted.

## Coordinate surfaces

Holding one coordinate fixed produces a surface.

+ $\rho=R$ is the sphere of radius $R$ centred at the origin.
+ $\theta=\alpha$ is the half-plane bounded by the $z$-axis, as in cylindrical coordinates.
+ $\varphi=\beta$ is the cone with vertex at the origin, axis the positive $z$-axis and half-angle $\beta$. In Cartesian coordinates its equation is $z=\rho\cos\beta$ together with $\rho\sin\beta=\sqrt{x^2+y^2}$, or $z=\cot(\beta)\sqrt{x^2+y^2}$ for $0<\beta<\pi/2$. For $\beta=\pi/2$ it is the $xy$-plane; for $\beta=0$ it degenerates to the positive $z$-axis.

A ball of radius $R$ is $0\le\rho\le R$, with the two angles free. A spherical shell is $R_1\le\rho\le R_2$. A solid cone with vertex at the origin and half-angle $\alpha$ is $0\le\varphi\le\alpha$. The region inside a cone and inside a sphere, often called an ice-cream cone, is described by a bound on $\varphi$ and a bound on $\rho$. These descriptions are compact because the bounding surfaces are coordinate surfaces.

A sphere not centred at the origin, or a plane that does not pass through the origin, does not have a simple spherical equation. Such a region may still be treated in spherical coordinates, but the limits become complicated; Cartesian or cylindrical coordinates are often better.

## The volume element

The map (1) has Jacobian matrix

$$D\Phi(\rho,\theta,\varphi)=\begin{pmatrix}\sin\varphi\cos\theta&-\rho\sin\varphi\sin\theta&\rho\cos\varphi\cos\theta\\ \sin\varphi\sin\theta&\rho\sin\varphi\cos\theta&\rho\cos\varphi\sin\theta\\ \cos\varphi&0&-\rho\sin\varphi\end{pmatrix}$$

Expanding the determinant gives

$$\det D\Phi=-\rho^2\sin\varphi \tag{4}$$

with the columns ordered $(\rho,\theta,\varphi)$. The negative sign reflects the fact that this ordering of the coordinates is left-handed. The absolute value is

$$|\det D\Phi|=\rho^2\sin\varphi \tag{5}$$

which is nonnegative on the range (3). By the [change of variables](../change-of-variables-in-multiple-integrals/) theorem,

$$dx\,dy\,dz=\rho^2\sin\varphi\,d\rho\,d\varphi\,d\theta \tag{6}$$

The order of the differentials is a convention; the product $\rho^2\sin\varphi\,d\rho\,d\theta\,d\varphi$ denotes the same volume element.

The factor has a geometric reading. A small coordinate box with increments $d\rho$, $d\varphi$ and $d\theta$ has sides of approximate lengths

$$d\rho \qquad \rho\,d\varphi \qquad \rho\sin\varphi\,d\theta$$

The first is radial, the second is along a meridian, and the third is along a parallel of latitude. The three directions are mutually perpendicular, so the volume is their product:

$$dV=(d\rho)(\rho\,d\varphi)(\rho\sin\varphi\,d\theta)=\rho^2\sin\varphi\,d\rho\,d\varphi\,d\theta$$

The factor $\sin\varphi$ suppresses the contribution near the poles, where the parallels shrink to a point. The factor $\rho^2$ reflects the quadratic growth of spherical area with radius.

For a solid $D$ with spherical description $D'$, the integral of $f$ is

$$\iiint_D f(x,y,z)\,dV=\iiint_{D'} f(\rho\sin\varphi\cos\theta,\rho\sin\varphi\sin\theta,\rho\cos\varphi)\,\rho^2\sin\varphi\,d\rho\,d\varphi\,d\theta \tag{7}$$

The integrand is expressed in the new variables, and the Jacobian factor multiplies the differentials.

## Setting up an integral

The usual procedure is:

+ Sketch the solid and identify the bounding surfaces.
+ Determine the range of $\theta$ from the projection onto the $xy$-plane.
+ Determine the range of $\varphi$ from the cones that bound the solid.
+ For each $(\theta,\varphi)$, determine the range of $\rho$ from the inner and outer surfaces.
+ Write the integral with the volume element and evaluate, often in the order $\rho$, then $\varphi$, then $\theta$.

If the solid is invariant under rotation about the $z$-axis, the $\theta$-integral contributes a factor $2\pi$ or the angular width of the sector. If the solid is a ball or a spherical shell, the $\rho$-limits are constants and the angular integrals separate. The order can be changed, but the factor $\rho^2\sin\varphi$ remains.

## A ball

The volume of the ball of radius $R$ is

$$V=\int_0^{2\pi}\int_0^\pi\int_0^R\rho^2\sin\varphi\,d\rho\,d\varphi\,d\theta$$

The integrals separate:

$$V=\left(\int_0^{2\pi}d\theta\right)\left(\int_0^\pi\sin\varphi\,d\varphi\right)\left(\int_0^R\rho^2\,d\rho\right)=2\pi\cdot2\cdot\frac{R^3}{3}=\frac{4\pi R^3}{3}$$

The result is the standard volume of a sphere. The Jacobian is not a cosmetic factor: omitting $\sin\varphi$ alone multiplies the value by $\pi/2$, and omitting $\rho^2$ leaves an expression with the dimensions of length rather than volume.

## A second moment

Evaluate

$$\iiint_B z^2\,dV$$

over the unit ball $B$. In spherical coordinates $z=\rho\cos\varphi$, so

$$\iiint_B z^2\,dV=\int_0^{2\pi}\int_0^\pi\int_0^1\rho^2\cos^2\varphi\cdot\rho^2\sin\varphi\,d\rho\,d\varphi\,d\theta$$

The integrals separate:

$$=\left(\int_0^{2\pi}d\theta\right)\left(\int_0^\pi\cos^2\varphi\sin\varphi\,d\varphi\right)\left(\int_0^1\rho^4\,d\rho\right)$$

The angular integral is

$$\int_0^\pi\cos^2\varphi\sin\varphi\,d\varphi=\left[-\frac{\cos^3\varphi}{3}\right]_0^\pi=\frac23$$

and the radial integral is $1/5$. Hence

$$\iiint_B z^2\,dV=2\pi\cdot\frac23\cdot\frac15=\frac{4\pi}{15}$$

As a check, symmetry gives

$$\iiint_B x^2\,dV=\iiint_B y^2\,dV=\iiint_B z^2\,dV$$

and the three sum to

$$\iiint_B(x^2+y^2+z^2)\,dV=\int_0^{2\pi}\int_0^\pi\int_0^1\rho^4\sin\varphi\,d\rho\,d\varphi\,d\theta=2\pi\cdot2\cdot\frac15=\frac{4\pi}{5}$$

so each individual moment is $\frac13\cdot\frac{4\pi}{5}=\frac{4\pi}{15}$, in agreement.

## An ice-cream cone

Find the volume of the solid inside the sphere $\rho=2$ and inside the cone $\varphi=\pi/4$.

The cone opens around the positive $z$-axis and has half-angle $\pi/4$. The solid is

$$0\le\theta<2\pi \qquad 0\le\varphi\le\frac{\pi}{4} \qquad 0\le\rho\le2$$

Hence

$$V=\int_0^{2\pi}\int_0^{\pi/4}\int_0^2\rho^2\sin\varphi\,d\rho\,d\varphi\,d\theta$$

$$=2\pi\cdot\frac{8}{3}\cdot\left[-\cos\varphi\right]_0^{\pi/4}=\frac{16\pi}{3}\left(1-\frac{\sqrt2}{2}\right)$$

The factor $1-\sqrt2/2$ is positive and less than $1$, so the volume is less than half the volume of the sphere, $\frac{16\pi}{3}$, as expected because the cone has half-angle $\pi/4<\pi/2$.

## Mass with radial density

Let a ball of radius $1$ have density $\rho(x,y,z)=1+\rho$, where $\rho$ is the distance from the origin. The mass is

$$M=\int_0^{2\pi}\int_0^\pi\int_0^1(1+\rho)\rho^2\sin\varphi\,d\rho\,d\varphi\,d\theta$$

$$=2\pi\cdot2\cdot\left(\frac13+\frac14\right)=4\pi\cdot\frac{7}{12}=\frac{7\pi}{3}$$

The density increases outward, so the mass is greater than the volume $\frac{4\pi}{3}$ of the unit ball, by the factor $7/4$. By symmetry the centre of mass is the origin; only the radial density contributes to the mass, and the angular integrals factor out.

## A spherical cap

The part of the ball of radius $R$ above the plane $z=a$, with $0\le a\le R$, is not star-shaped from the origin when $a>0$. Along a ray at angle $\varphi$, the plane $z=a$ is reached at $\rho=a/\cos\varphi$, and the sphere at $\rho=R$. The ray meets the cap only when $a/\cos\varphi\le R$, that is, when $\varphi\le\arccos(a/R)$. Hence the cap is described by

$$0\le\varphi\le\arccos\left(\frac{a}{R}\right) \qquad \frac{a}{\cos\varphi}\le\rho\le R$$

and its volume is

$$V=\int_0^{2\pi}\int_0^{\arccos(a/R)}\int_{a/\cos\varphi}^{R}\rho^2\sin\varphi\,d\rho\,d\varphi\,d\theta$$

$$=\frac{2\pi}{3}\int_0^{\arccos(a/R)}\left(R^3-a^3\sec^3\varphi\right)\sin\varphi\,d\varphi$$

Using $\int\sin\varphi\,d\varphi=-\cos\varphi$ and

$$\int\sec^3\varphi\sin\varphi\,d\varphi=\frac{1}{2}\sec^2\varphi$$

the integral becomes

$$V=\frac{2\pi}{3}\left[R^3\left(1-\frac{a}{R}\right)-\frac{a^3}{2}\left(\frac{R^2}{a^2}-1\right)\right]=\frac{\pi}{3}\left(2R^3-3R^2a+a^3\right)$$

At $a=0$ this is half the ball, $2\pi R^3/3$; at $a=R$ it is zero. The formula is continuous in $a$, as it must be. The non-constant lower limit is the point of the example: a region that is simple in Cartesian coordinates need not be star-shaped in spherical coordinates.

## When to use spherical coordinates

Spherical coordinates are natural when the solid or the integrand is organised around a point rather than an axis.

+ The region is a ball, a spherical shell, a spherical cap, a cone with vertex at the origin, or a union of such pieces.
+ The integrand contains $x^2+y^2+z^2$ or $\sqrt{x^2+y^2+z^2}$.
+ The boundary surfaces are given by equations in $\rho$, such as $\rho=R$, or by cones $\varphi=\alpha$.
+ The region has full rotational symmetry about the origin, so both angles can be integrated out.

If the region is a cylinder or is organised around the $z$-axis, [cylindrical coordinates](../cylindrical-coordinates/) are usually simpler. A vertical cylinder has the compact cylindrical description $r\le R$, while its spherical description requires a relation between $\rho$ and $\varphi$. If the region has no symmetry, Cartesian coordinates may be the only practical choice.

## Pitfalls

The following errors are common.

**Using the wrong angle.** If $\varphi$ is measured from the $xy$-plane instead of the $z$-axis, then $z=\rho\sin\varphi$ rather than $\rho\cos\varphi$, and the range of $\varphi$ changes. The Jacobian factor $\rho^2\sin\varphi$ is the same in form, but the limits are different. Mixing the two conventions produces wrong signs and wrong volumes.

**Omitting the Jacobian.** The volume element is $\rho^2\sin\varphi\,d\rho\,d\varphi\,d\theta$, not $d\rho\,d\varphi\,d\theta$. The ball computation shows the size of the error: omitting $\sin\varphi$ alone multiplies the volume by $\pi/2$, and omitting $\rho^2$ leaves an expression with the dimensions of length. The factor is the determinant of the coordinate map, not a convention.

**Confusing $\rho$ with $r$.** In cylindrical coordinates $r$ is the distance from the $z$-axis; in spherical coordinates $\rho$ is the distance from the origin. They are related by $r=\rho\sin\varphi$. A sphere centred at the origin is $\rho=R$, not $r=R$; the latter is a cylinder.

**Using the full angular range for a sector.** A wedge or a cone occupies only part of the $\theta$-range. Integrating $\theta$ from $0$ to $2\pi$ for a half-space or a sector multiplies the result by the wrong factor.

**Forgetting the pole behaviour.** At $\varphi=0$ and $\varphi=\pi$ the factor $\sin\varphi$ vanishes. Integrals are well defined there, but coordinate expressions that divide by $\sin\varphi$ or by $\rho$ may fail on the axis. The singularity is coordinate, not geometric.

## Relation to cylindrical coordinates

Spherical and cylindrical coordinates are related by

$$r=\rho\sin\varphi \qquad z=\rho\cos\varphi \qquad \theta=\theta \tag{8}$$

where $r$ is the distance from the $z$-axis. The cylindrical volume element is $r\,dr\,d\theta\,dz$. Substituting $r=\rho\sin\varphi$ and $z=\rho\cos\varphi$ gives $dr\,dz=\rho\,d\rho\,d\varphi$ up to sign, and hence

$$r\,dr\,d\theta\,dz=\rho\sin\varphi\cdot\rho\,d\rho\,d\varphi\,d\theta=\rho^2\sin\varphi\,d\rho\,d\varphi\,d\theta$$

which is the spherical volume element. The two Jacobians are consistent because one coordinate change is composed with the other.

Both are special cases of the [change of variables](../change-of-variables-in-multiple-integrals/) formula, and both integrals are evaluated by [Fubini's theorem](../fubinis-theorem/) after the change. The entry on [triple integrals](../triple-integrals/) develops the general reduction; the entry on [cylindrical coordinates](../cylindrical-coordinates/) treats the axisymmetric case. The spherical system is the point-symmetric case, and its volume element is the one that makes the ball and the cone as simple as the cylinder is in cylindrical coordinates.
