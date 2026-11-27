# Research evidence — Cylindrical Coordinates

Batch: `20261127T121407Z-01`
Slug: `cylindrical-coordinates`
Article: `multivariable-calculus/cylindrical-coordinates.md`
Category: `multivariable-calculus` (provisional)
Research date: 2026-11-27

## Coverage check

Upstream `antoniolupetti/algebrica` was searched by filename and body text for "cylindrical", "coordinate system", "volume element" and "triple integral".

+ `lines-planes-conic-sections/polar-coordinates.md` develops planar polar coordinates and, in §"Polar coordinates in space", introduces a spherical-type system with radial distance $\rho$, angle $\psi$ from the $z$-axis and azimuth $\theta$. It does not define cylindrical coordinates $(r,\theta,z)$.
+ No article with "cylindrical" in its title or body was found.
+ No upstream article develops triple integrals or the Jacobian factor $r$.

Conclusion: not a duplicate. The polar article supplies the planar prerequisite and a different three-dimensional convention; the present entry defines the standard cylindrical system, derives its volume element and applies it. Open issues and pull requests were not inspected; no claim is made about planned upstream work.

## Scope and reader contract

After reading the article, the reader can:

+ convert between Cartesian and cylindrical coordinates and state the standard ranges;
+ identify the coordinate surfaces $r=a$, $\theta=\alpha$, $z=c$, and the graphs $z=r$ and $z=r^2$;
+ derive the volume element $r\,dr\,d\theta\,dz$ from the Jacobian and geometrically;
+ set up a triple integral over a solid described by cylindrical inequalities;
+ compute volumes of a cylinder, a paraboloid cap, a cone, and a sphere cut by a cylinder;
+ compute a mass and a centroid height for a density depending on $z$;
+ decide when cylindrical coordinates are preferable to Cartesian or spherical coordinates;
+ avoid the common errors of omitting the Jacobian, confusing $r$ with the distance from the origin, and using the full angular range for a sector.

Assumed prerequisites: polar coordinates, partial derivatives, determinants, the [change of variables](../multivariable-calculus/change-of-variables-in-multiple-integrals.md) theorem, and the [triple integral](../multivariable-calculus/triple-integrals.md). Exclusions: spherical coordinates (sibling entry), general curvilinear coordinates, and vector calculus in cylindrical components.

## Sources consulted

1. University of Toronto, MAT237, *Multivariable Calculus*, §4.4 "Change of Variables".
   URL: https://www.math.toronto.edu/courses/mat237y1/20199/notes/Chapter4/S4.4.html
   Accessed: 2026-11-27. Full text read.
   Supports: the cylindrical map $(r,\theta,z)\mapsto(r\cos\theta,r\sin\theta,z)$, its Jacobian determinant $r$, the resulting volume element, and examples of volumes of revolution computed with it.
   Use: the Jacobian computation, the volume element, and the general change-of-variables justification.

2. OpenStax, *Calculus Volume 3*, §5.5 "Triple Integrals in Cylindrical and Spherical Coordinates".
   URL: https://openstax.org/books/calculus-volume-3/pages/5-5-triple-integrals-in-cylindrical-and-spherical-coordinates
   Accessed: 2026-11-27. Full text read.
   Supports: the definition of cylindrical coordinates, the conversion formulas, the coordinate surfaces, the volume element, the description of typical solids, and worked examples of volumes and masses.
   Use: independent confirmation of the definitions, ranges, volume element and integration procedure.

3. Algebrica upstream `lines-planes-conic-sections/polar-coordinates.md`.
   URL: https://algebrica.org/polar-coordinates/
   Accessed through the upstream clone, 2026-11-27.
   Supports: house notation, the planar polar relations, the polar area element, and the existing three-dimensional convention with $\rho$ and $\psi$.
   Use: the link to polar coordinates and the note that the upstream three-dimensional convention differs from the standard $(\rho,\theta,\varphi)$ used in this batch.

## Definitions and conventions selected

+ Coordinates: $(r,\theta,z)$ with $r\ge0$ the distance from the $z$-axis, $\theta\in[0,2\pi)$ the azimuth from the positive $x$-axis, and $z\in\mathbb{R}$ the height.
+ Map: $x=r\cos\theta$, $y=r\sin\theta$, $z=z$.
+ Inverse: $r=\sqrt{x^2+y^2}$, $\theta=\operatorname{atan2}(y,x)$, $z=z$.
+ Jacobian determinant: $r$; volume element $r\,dr\,d\theta\,dz$.
+ Coordinate surfaces: $r=a$ cylinder, $\theta=\alpha$ half-plane, $z=c$ plane; $z=r$ cone, $z=r^2$ paraboloid.
+ British spelling: "centre of mass", "recognise", "anticlockwise" where used.

## Mathematical claims and justification

+ **Conversion formulas.** Direct from the right triangle in the $xy$-plane: $x=r\cos\theta$, $y=r\sin\theta$, and $r^2=x^2+y^2$. The angle is recovered by $\operatorname{atan2}$ because the principal value of $\arctan(y/x)$ loses the quadrant.
+ **Non-uniqueness.** On the $z$-axis $r=0$ and $\theta$ is arbitrary; $\theta$ and $\theta+2\pi$ give the same point. The axis and a half-plane have zero volume, so integrals are unaffected. Stated.
+ **Coordinate surfaces.** Setting one coordinate constant in (1) gives the stated surfaces; $z=r$ is equivalent to $z=\sqrt{x^2+y^2}$, the upper nappe of a cone. Direct substitution.
+ **Jacobian determinant.** The matrix is block triangular with the polar $2\times2$ block and the entry $1$; the determinant is $r\cos^2\theta+r\sin^2\theta=r$. Complete computation.
+ **Volume element (5).** Change-of-variables theorem applied to the map (1); the determinant is nonnegative for $r\ge0$, so no absolute-value subtlety. The geometric derivation multiplies the three orthogonal side lengths $dr$, $r\,d\theta$, $dz$.
+ **Cylinder volume.** $\int_0^{2\pi}\int_0^R\int_0^H r\,dz\,dr\,d\theta=2\pi\cdot R^2/2\cdot H=\pi R^2H$.
+ **Paraboloid volume.** The surfaces meet at $r=2$. $\int_0^2r(4-r^2)\,dr=[2r^2-r^4/4]_0^2=4$; multiplying by $2\pi$ gives $8\pi$. Cross-check: cylinder $16\pi$ minus the volume under the paraboloid $2\pi\int_0^2r^3\,dr=8\pi$, giving $8\pi$.
+ **Cone volume.** $\int_0^2r(2-r)\,dr=4-8/3=4/3$; multiplying by $2\pi$ gives $8\pi/3$, matching $\frac13\pi R^2H$ with $R=H=2$.
+ **Density example.** Mass $2\pi\cdot\frac12\cdot2=2\pi$; first moment $2\pi\cdot\frac12\cdot\frac83=8\pi/3$; centroid height $\bar z=4/3>1$. Correct.
+ **Sphere–cylinder example.** The sphere is $r^2+z^2\le4$, so $|z|\le\sqrt{4-r^2}$ for $r\le1$. The inner integral gives $2r\sqrt{4-r^2}$; with $u=4-r^2$, the $r$-integral is $\frac23(8-3\sqrt3)$; multiplying by $2\pi$ gives $\frac{4\pi}{3}(8-3\sqrt3)$. Positive and less than $32\pi/3$. Correct.
+ **Pitfalls.** Omitting $r$ changes the value by a length factor; using $r=R$ for a sphere gives a cylinder; using $0\le\theta<2\pi$ for a sector multiplies by the wrong angular factor. Each is illustrated by a computation or a surface identification.

## Independent checks

Python 3 script `work/checks/verify_batch6.py` (outside the repository), nested composite Simpson quadrature with $n=120$ per variable:

+ cylinder $r\le2$, $0\le z\le3$: computed $12\pi=37.6991118431$;
+ paraboloid $r^2\le z\le4$: computed $8\pi=25.1327412287$;
+ cone $r\le z\le2$: computed $8\pi/3=8.37758040957$;
+ density mass: computed $2\pi=6.28318530718$;
+ density first moment: computed $8\pi/3=8.37758040957$;
+ sphere cut by cylinder: computed $11.7447292669$, exact $\frac{4\pi}{3}(8-3\sqrt3)=11.7447292675$ (difference $6\times10^{-10}$, within quadrature error).

All checks passed. The exact antiderivative computations in the article give the same values independently.

## Limitations

+ No LaTeX renderer, Pandoc or TeX installation is available (`pandoc` and `pdflatex` not found); the Markdown was checked structurally but not rendered.
+ The live route `https://algebrica.org/cylindrical-coordinates/` is proposed, not known to exist.
+ The change-of-variables theorem is invoked, not reproved; the sibling entry supplies the proof sketch.
+ Open issues and pull requests in the upstream repository were not inspected.
+ Links to sibling batch articles are unpublished dependencies until this batch is merged.

## Figure briefs

See `figure-briefs.md` in this directory.
