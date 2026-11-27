---
title: Parametric Surfaces
source: https://algebrica.org/parametric-surfaces/
license: CC BY-NC 4.0
tags:
  - multivariable-calculus
  - parametric-surfaces
  - surface-area
  - surface-integrals
  - vector-calculus
---

## Two parameters instead of one

A curve is described by a vector function of one parameter. A surface requires two. A **parametric surface** is a continuous map

$$\mathbf{r}(u,v)=\langle x(u,v),\ y(u,v),\ z(u,v)\rangle \qquad (u,v)\in D \tag{1}$$

where $D$ is a region in the $uv$-plane. The image of $\mathbf{r}$ is the surface, and $D$ is its parameter domain. The variables $u$ and $v$ are coordinates on the surface, not on the surface's ambient space.

The simplest example is the graph of a function of two variables. If $z=g(x,y),$ then

$$\mathbf{r}(x,y)=\langle x,\ y,\ g(x,y)\rangle \tag{2}$$

with $D$ the domain of $g.$ Here the parameters are the original $x$ and $y,$ and the surface is the graph itself. The parameterization adds nothing geometrically, but it places the graph in the general framework and supplies the normal vector and area element.

A plane is also a parametric surface. The plane through a point $\mathbf{r}_0$ spanned by two independent vectors $\mathbf{a}$ and $\mathbf{b}$ is

$$\mathbf{r}(u,v)=\mathbf{r}_0+u\mathbf{a}+v\mathbf{b} \tag{3}$$

with $(u,v)$ ranging over a region of the plane. If the region is all of $\mathbb{R}^2,$ the parameterization covers the whole plane; if it is a rectangle, it covers a parallelogram.

A cylinder is best described with an angle and a height:

$$\mathbf{r}(\theta,z)=\langle R\cos\theta,\ R\sin\theta,\ z\rangle \qquad 0\le\theta\le2\pi,\quad 0\le z\le h \tag{4}$$

The parameter $\theta$ goes around the circular cross-section and $z$ moves along the axis. A sphere uses two angles:

$$\mathbf{r}(\theta,\varphi)=\langle R\sin\varphi\cos\theta,\ R\sin\varphi\sin\theta,\ R\cos\varphi\rangle \tag{5}$$

with $0\le\theta\le2\pi$ and $0\le\varphi\le\pi.$ Here $\varphi$ is measured from the positive $z$-axis, so it is a polar angle rather than a latitude; $\theta$ is the azimuthal angle in the $xy$-plane. The distinction matters: using a latitude measured from the equator changes the sine and cosine factors.

## Coordinate curves and the parameter grid

Fix $v=v_0$ and let $u$ vary. The image is a curve on the surface, called a $u$-curve. Fix $u=u_0$ and let $v$ vary; the image is a $v$-curve. The two families form a grid on the surface, and the grid is the image of the rectangular grid in the parameter domain.

For the sphere (5), the $u$-curves with $\varphi$ fixed are circles of latitude, and the $v$-curves with $\theta$ fixed are meridians. For the cylinder (4), the $\theta$-curves are horizontal circles and the $z$-curves are vertical lines. The grid is not merely a drawing aid: its spacing records how the parameterization stretches the surface, and the area element is the local area of a grid cell.

A parameterization need not be one-to-one. The sphere (5) with $0\le\theta<2\pi$ is one-to-one on the interior except along the poles, where every $\theta$ gives the same point, and the two edges $\theta=0$ and $\theta=2\pi$ are glued to the same meridian. If $\theta$ is allowed to run from $0$ to $4\pi,$ the same map traces the sphere twice, and an area integral computed from it counts the sphere twice. A parameterized surface is a map, not just a set of points; multiplicity is part of the data unless it is excluded by hypothesis.

## Smoothness and regular points

The partial derivatives

$$\begin{aligned}
\mathbf{r}_u&=\left\langle\frac{\partial x}{\partial u},\frac{\partial y}{\partial u},\frac{\partial z}{\partial u}\right\rangle\\[6pt]
\mathbf{r}_v&=\left\langle\frac{\partial x}{\partial v},\frac{\partial y}{\partial v},\frac{\partial z}{\partial v}\right\rangle
\end{aligned} \tag{6}$$

are the tangent vectors to the $u$-curves and $v$-curves. If both exist and are continuous, and if

$$\mathbf{r}_u\times\mathbf{r}_v\neq\mathbf{0} \tag{7}$$

at a point, the parameterization is **regular** there. The cross product is then a normal vector to the surface, and $\mathbf{r}_u,\mathbf{r}_v$ span the tangent plane.

A parameterization is **smooth** on $D$ if $\mathbf{r}_u$ and $\mathbf{r}_v$ are continuous and the cross product is nonzero at every interior point of $D.$ A surface is **piecewise smooth** if it is a finite union of smooth parameterized patches, joined along curves. The joins may have corners or edges, just as a piecewise smooth curve may have corners.

Regularity is a property of the parameterization, not of the geometric surface. The sphere (5) is a smooth surface, but its standard parameterization fails (7) at the poles $\varphi=0$ and $\varphi=\pi,$ where $\sin\varphi=0$ and both tangent vectors degenerate. The poles are not geometric singularities; they are coordinate singularities. The sphere can be covered by two overlapping patches, each omitting one pole, with a different chart near each pole. For integration, the failure at isolated points does not affect the value, because the area element contains the factor $\sin\varphi$ and the contribution of the poles is zero.

A point where the cross product vanishes for every parameterization is a genuine singular point of the surface. A cone has such a point at its vertex: the tangent plane is not defined there, and no regular parameterization can cover a neighbourhood of the vertex. The cone minus its vertex is a smooth surface.

## The tangent plane

At a regular point $(u_0,v_0),$ the tangent plane is spanned by $\mathbf{r}_u$ and $\mathbf{r}_v.$ A point $\mathbf{X}$ lies in the plane if

$$(\mathbf{X}-\mathbf{r}(u_0,v_0))\cdot(\mathbf{r}_u\times\mathbf{r}_v)=0 \tag{8}$$

The normal vector need not be a unit vector. The unit normal is

$$\mathbf{n}=\pm\frac{\mathbf{r}_u\times\mathbf{r}_v}{\lVert\mathbf{r}_u\times\mathbf{r}_v\rVert} \tag{9}$$

and the sign chooses one of the two sides of the surface.

For the paraboloid $\mathbf{r}(u,v)=\langle u,v,u^2+v^2\rangle$ at $(u,v)=(1,1),$ the point is $(1,1,2)$ and

$$\mathbf{r}_u=\langle1,0,2\rangle \qquad \mathbf{r}_v=\langle0,1,2\rangle \qquad \mathbf{r}_u\times\mathbf{r}_v=\langle-2,-2,1\rangle \tag{10}$$

The tangent plane is therefore

$$-2(x-1)-2(y-1)+(z-2)=0 \qquad \text{or} \qquad z=2x+2y-2 \tag{11}$$

The normal $\langle-2,-2,1\rangle$ points upward, since its $z$-component is positive.

## Surface area

The area element comes from the linearization of the map. A small rectangle of sides $\Delta u$ and $\Delta v$ in the parameter domain is mapped approximately to the parallelogram spanned by $\mathbf{r}_u\Delta u$ and $\mathbf{r}_v\Delta v.$ The area of that parallelogram is

$$\lVert\mathbf{r}_u\times\mathbf{r}_v\rVert\,\Delta u\,\Delta v \tag{12}$$

Summing over a partition of $D$ and passing to the limit gives the surface area

$$A(S)=\iint_D\lVert\mathbf{r}_u\times\mathbf{r}_v\rVert\,du\,dv \tag{13}$$

and the surface area element

$$dS=\lVert\mathbf{r}_u\times\mathbf{r}_v\rVert\,du\,dv \tag{14}$$

The formula is the two-dimensional analogue of the arc length element $ds=\lVert\mathbf{r}'(t)\rVert\,dt.$ In one dimension the linearization is a tangent vector and its length; in two dimensions it is a parallelogram and its area.

The value does not depend on the parameterization. A change of parameters $(u,v)=\Phi(s,t)$ divides the norm of the cross product by the absolute value of the Jacobian determinant of $\Phi,$ while the parameter area element is multiplied by that same value; the two factors cancel. This is the change-of-variables formula in the parameter plane, and it is why the area is a geometric quantity rather than an artefact of the chosen coordinates.

For a graph $z=g(x,y),$ the parameterization (2) gives

$$\mathbf{r}_x\times\mathbf{r}_y=\langle-g_x,\ -g_y,\ 1\rangle \qquad \lVert\mathbf{r}_x\times\mathbf{r}_y\rVert=\sqrt{1+g_x^2+g_y^2} \tag{15}$$

so

$$A(S)=\iint_D\sqrt{1+g_x^2+g_y^2}\,dx\,dy \tag{16}$$

This is the form used when the surface is already described as a graph.

## Standard parameterizations

The following table collects the parameterizations and area elements used most often. In each row, the parameters range over the stated domain and the surface is traced once, except possibly on its boundary.

| Surface | Parameterization | $\lVert\mathbf{r}_u\times\mathbf{r}_v\rVert$ |
|---|---|---|
| Graph $z=g(x,y)$ | $\langle x,y,g(x,y)\rangle$ | $\sqrt{1+g_x^2+g_y^2}$ |
| Cylinder $x^2+y^2=R^2$ | $\langle R\cos\theta,R\sin\theta,z\rangle$ | $R$ |
| Sphere $x^2+y^2+z^2=R^2$ | $\langle R\sin\varphi\cos\theta,R\sin\varphi\sin\theta,R\cos\varphi\rangle$ | $R^2\sin\varphi$ |
| Cone $z=\sqrt{x^2+y^2}$ | $\langle r\cos\theta,r\sin\theta,r\rangle$ | $\sqrt2\,r$ |
| Torus | $\langle(a+b\cos\varphi)\cos\theta,(a+b\cos\varphi)\sin\theta,b\sin\varphi\rangle$ | $b(a+b\cos\varphi)$ |

For the torus, $0<b<a,$ $0\le\theta\le2\pi$ and $0\le\varphi\le2\pi.$ The parameter $b$ is the radius of the tube and $a$ the distance from the centre of the tube to the axis. The area element is positive because $a+b\cos\varphi>0.$

The cylinder's area element is constant, so its lateral area is $R$ times the area of the parameter rectangle $2\pi h,$ giving $2\pi Rh.$ The sphere's area element depends on $\varphi,$ and the torus's depends on both the tube angle and the position around the axis.

## The sphere

For the sphere (5), the tangent vectors are

$$\mathbf{r}_\theta=\langle-R\sin\varphi\sin\theta,\ R\sin\varphi\cos\theta,\ 0\rangle \tag{17}$$

$$\mathbf{r}_\varphi=\langle R\cos\varphi\cos\theta,\ R\cos\varphi\sin\theta,\ -R\sin\varphi\rangle \tag{18}$$

Their cross product is

$$\mathbf{r}_\theta\times\mathbf{r}_\varphi=-R^2\sin\varphi\,\langle\sin\varphi\cos\theta,\ \sin\varphi\sin\theta,\ \cos\varphi\rangle \tag{19}$$

and its norm is $R^2\sin\varphi,$ since $\sin\varphi\ge0$ on $0\le\varphi\le\pi.$ The area is therefore

$$A=\int_0^{2\pi}\int_0^\pi R^2\sin\varphi\,d\varphi\,d\theta=2\pi R^2\bigl[-\cos\varphi\bigr]_0^\pi=4\pi R^2 \tag{20}$$

The sign in (19) is worth noting. The vector $\mathbf{r}_\theta\times\mathbf{r}_\varphi$ points toward the centre of the sphere, because the bracket is the outward unit radial vector and the coefficient is negative. Reversing the order gives the outward normal. The area uses the norm, so the sign does not matter there, but a vector surface integral would require the correct orientation.

At the poles, $\sin\varphi=0$ and the cross product vanishes. The integral still converges, because the integrand is bounded and the singular set has measure zero in the parameter domain. This is the standard treatment of coordinate singularities: they are excluded from the regular set and included in the integral by a limiting argument.

## The cone

For the cone $\mathbf{r}(r,\theta)=\langle r\cos\theta,r\sin\theta,r\rangle$ with $0\le r\le R$ and $0\le\theta\le2\pi,$

$$\mathbf{r}_r=\langle\cos\theta,\sin\theta,1\rangle \qquad \mathbf{r}_\theta=\langle-r\sin\theta,r\cos\theta,0\rangle \tag{21}$$

and

$$\mathbf{r}_r\times\mathbf{r}_\theta=\langle-r\cos\theta,-r\sin\theta,r\rangle \qquad \lVert\mathbf{r}_r\times\mathbf{r}_\theta\rVert=\sqrt2\,r \tag{22}$$

Hence

$$A=\int_0^{2\pi}\int_0^R\sqrt2\,r\,dr\,d\theta=\sqrt2\,\pi R^2 \tag{23}$$

The result agrees with the elementary formula $\pi R\ell,$ where $\ell=\sqrt2R$ is the slant height. The vertex $r=0$ is a genuine singular point, and the parameterization is not regular there; the area integral is unaffected because the Jacobian factor $r$ vanishes.

## The torus

For the torus, differentiating with respect to $\theta$ and $\varphi$ gives

$$\mathbf{r}_\theta=\langle-(a+b\cos\varphi)\sin\theta,\ (a+b\cos\varphi)\cos\theta,\ 0\rangle \tag{24}$$

$$\mathbf{r}_\varphi=\langle-b\sin\varphi\cos\theta,\ -b\sin\varphi\sin\theta,\ b\cos\varphi\rangle \tag{25}$$

and

$$\lVert\mathbf{r}_\theta\times\mathbf{r}_\varphi\rVert=b(a+b\cos\varphi) \tag{26}$$

The area is

$$A=\int_0^{2\pi}\int_0^{2\pi}b(a+b\cos\varphi)\,d\varphi\,d\theta=4\pi^2ab \tag{27}$$

The term involving $\cos\varphi$ integrates to zero over a full turn, so the area is the product of the circumference $2\pi a$ of the central circle and the circumference $2\pi b$ of the tube. This is plausible but not a proof: the tube is bent, and the outer side stretches while the inner side compresses. The two effects cancel in the integral, which is why the product formula is exact.

## Orientation

A regular parameterization gives two unit normals, $\mathbf{n}$ and $-\mathbf{n}.$ Choosing one continuously over the surface is an **orientation**. Swapping the parameters $u$ and $v$ reverses the sign of $\mathbf{r}_u\times\mathbf{r}_v,$ so it reverses the orientation; reparameterizing with a map of negative Jacobian does the same.

Not every surface is orientable. The Möbius band has only one side: a normal transported once around the band returns pointing in the opposite direction, so no continuous choice of normal exists. Vector surface integrals are therefore not defined on a Möbius band without further structure, while scalar surface integrals are. A regular parametric patch is always orientable, because the parameter domain chooses a side; the obstruction appears only when patches are glued with a twist.

For a closed surface, the standard orientation is **outward**, with the unit normal pointing away from the enclosed solid. For a graph $z=g(x,y),$ the upward normal is proportional to $\langle-g_x,-g_y,1\rangle,$ whose $z$-component is positive. For a sphere with the parameterization (5), the outward normal is $-\mathbf{r}_\theta\times\mathbf{r}_\varphi/\lVert\mathbf{r}_\theta\times\mathbf{r}_\varphi\rVert,$ not the cross product in the order written.

## Implicit surfaces

A surface can also be given implicitly by

$$F(x,y,z)=0 \tag{28}$$

with $\nabla F\neq\mathbf{0}.$ The implicit function theorem guarantees that, near a point where some partial derivative of $F$ is nonzero, the surface can be written as a graph of the remaining two variables. The gradient $\nabla F$ is normal to the surface: if $\mathbf{r}(t)$ is a curve in the surface, then $F(\mathbf{r}(t))=0$ and

$$\frac{d}{dt}F(\mathbf{r}(t))=\nabla F(\mathbf{r}(t))\cdot\mathbf{r}'(t)=0 \tag{29}$$

so the gradient is orthogonal to every tangent vector.

When the surface is written as $z=g(x,y),$ the implicit function $F(x,y,z)=z-g(x,y)$ has gradient $\langle-g_x,-g_y,1\rangle,$ in agreement with (15). The implicit form is convenient when the surface has a symmetry that makes a graph awkward, such as a sphere or a cylinder, but an area integral still requires either a parameterization or a projection formula.

## What a parameterization does not determine

+ The parameterization is not unique. A plane, a sphere and a cylinder each have infinitely many, and the area integral gives the same value for all regular parameterizations that trace the surface once.
+ The image is not the whole data. A non-injective parameterization counts points with multiplicity; the area integral then counts area with multiplicity, which may not be the geometric area of the image set.
+ A vanishing cross product does not always signal a geometric singularity. The sphere's poles are coordinate singularities, while the cone's vertex is a genuine one. The difference is whether a regular parameterization exists near the point.
+ The parameter domain is part of the specification. Changing the domain changes the patch, even if the formula for $\mathbf{r}$ is unchanged.
+ Orientation is a choice, not a consequence of the surface. For an open surface, both signs are legitimate; for a closed surface, the outward choice is a convention.
+ A regular parameterization does not make every surface orientable. It orients one patch. Gluing patches can produce a one-sided surface.

- - -

A parametric surface turns a two-dimensional integration problem into a double integral over a parameter rectangle or region. The next step is to integrate scalar functions and vector fields over such a surface, using the area element and the normal vector developed here.

## Related notions

Parametric surfaces extend [vector-valued functions](../vector-valued-functions/) from one parameter to two. Their area element is the basis of [surface integrals](../surface-integrals/), and the normal vector is what makes [flux integrals](../flux-integrals/) meaningful. The sphere and cylinder parameterizations connect to [spherical coordinates](../spherical-coordinates/) and [cylindrical coordinates](../cylindrical-coordinates/); the tangent plane generalizes [tangent planes and linear approximations](../tangent-planes-and-linear-approximations/). The implicit description uses the gradient and the implicit function theorem.
