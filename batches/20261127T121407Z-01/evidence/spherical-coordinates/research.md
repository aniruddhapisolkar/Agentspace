# Research evidence — Spherical Coordinates

Batch: `20261127T121407Z-01`
Slug: `spherical-coordinates`
Article: `multivariable-calculus/spherical-coordinates.md`
Category: `multivariable-calculus` (provisional)
Research date: 2026-11-27

## Coverage check

Upstream `antoniolupetti/algebrica` was searched by filename and body text for "spherical", "polar coordinates in space", "volume element" and "triple integral".

+ `lines-planes-conic-sections/polar-coordinates.md` §"Polar coordinates in space" introduces a three-dimensional system with radial distance $\rho$, polar angle $\psi$ measured from the $z$-axis, and azimuth $\theta$. It states the coordinate relations but does not develop the Jacobian, the volume element, or integration in the system.
+ No article with "spherical coordinates" in its title was found.
+ No upstream article treats spherical volumes, caps or cones.

Conclusion: not a duplicate. The polar article gives a short coordinate introduction with a different letter for the polar angle; the present entry gives the standard $(\rho,\theta,\varphi)$ system, derives the Jacobian, and applies it. Open issues and pull requests were not inspected; no claim is made about planned upstream work.

## Scope and reader contract

After reading the article, the reader can:

+ convert between Cartesian and spherical coordinates and state the standard ranges;
+ identify the coordinate surfaces $\rho=R$, $\theta=\alpha$ and $\varphi=\beta$, and describe balls, shells, cones and caps;
+ derive the volume element $\rho^2\sin\varphi\,d\rho\,d\varphi\,d\theta$ from the Jacobian and geometrically;
+ set up and evaluate integrals over a ball, an ice-cream cone, a spherical cap and a radially symmetric density;
+ compute the second moment $\iiint z^2$ and check it by symmetry;
+ decide when spherical coordinates are preferable to cylindrical or Cartesian coordinates;
+ avoid the common errors of using the wrong polar angle, omitting the Jacobian, confusing $\rho$ with $r$, and using the full angular range for a sector.

Assumed prerequisites: polar and [cylindrical coordinates](../multivariable-calculus/cylindrical-coordinates.md), partial derivatives, determinants, the [change of variables](../multivariable-calculus/change-of-variables-in-multiple-integrals.md) theorem, and the [triple integral](../multivariable-calculus/triple-integrals.md). Exclusions: spherical harmonics, vector calculus in spherical components, and the general theory of orthogonal curvilinear coordinates.

## Sources consulted

1. University of Toronto, MAT237, *Multivariable Calculus*, §4.4 "Change of Variables".
   URL: https://www.math.toronto.edu/courses/mat237y1/20199/notes/Chapter4/S4.4.html
   Accessed: 2026-11-27. Full text read.
   Supports: the spherical map, the Jacobian determinant $\rho^2\sin\varphi$, the volume element, and worked volume computations in spherical coordinates.
   Use: the Jacobian matrix and determinant, the volume element, and the general change-of-variables justification.

2. OpenStax, *Calculus Volume 3*, §5.5 "Triple Integrals in Cylindrical and Spherical Coordinates".
   URL: https://openstax.org/books/calculus-volume-3/pages/5-5-triple-integrals-in-cylindrical-and-spherical-coordinates
   Accessed: 2026-11-27. Full text read.
   Supports: the definition of spherical coordinates with $\rho$ the distance from the origin, $\theta$ the azimuth and $\varphi$ the angle from the positive $z$-axis; the ranges; the coordinate surfaces; the volume element; and examples of volumes and masses.
   Use: independent confirmation of the convention, ranges, surfaces and volume element.

3. Algebrica upstream `lines-planes-conic-sections/polar-coordinates.md` §"Polar coordinates in space".
   URL: https://algebrica.org/polar-coordinates/
   Accessed through the upstream clone, 2026-11-27.
   Supports: the existing three-dimensional convention with $\rho$ and $\psi$, the coordinate relations, and the house style.
   Use: the note on notational variation and the link to the planar polar entry. The upstream convention is explicitly distinguished from the one used here.

## Definitions and conventions selected

+ Coordinates: $(\rho,\theta,\varphi)$ with $\rho\ge0$ the distance from the origin, $\theta\in[0,2\pi)$ the azimuth from the positive $x$-axis, and $\varphi\in[0,\pi]$ the angle from the positive $z$-axis.
+ Map: $x=\rho\sin\varphi\cos\theta$, $y=\rho\sin\varphi\sin\theta$, $z=\rho\cos\varphi$.
+ Inverse: $\rho=\sqrt{x^2+y^2+z^2}$, $\theta=\operatorname{atan2}(y,x)$, $\varphi=\arccos(z/\rho)$.
+ Jacobian determinant with columns ordered $(\rho,\theta,\varphi)$: $-\rho^2\sin\varphi$; absolute value $\rho^2\sin\varphi$.
+ Volume element: $\rho^2\sin\varphi\,d\rho\,d\varphi\,d\theta$.
+ Relation to cylindrical: $r=\rho\sin\varphi$, $z=\rho\cos\varphi$.
+ British spelling: "centre of mass", "recognise", "meridional" where used.

## Mathematical claims and justification

+ **Conversion formulas (1)–(2).** Direct from the right triangle with hypotenuse $\rho$, vertical leg $z=\rho\cos\varphi$ and horizontal leg $r=\rho\sin\varphi$, combined with the planar polar relations. The inverse for $\varphi$ uses $\arccos(z/\rho)$; the inverse for $\theta$ needs $\operatorname{atan2}$ to recover the quadrant.
+ **Ranges (3).** $\rho\ge0$ by definition; $\theta$ is periodic; $\varphi\in[0,\pi]$ covers the whole sphere because $\sin\varphi\ge0$ there. Values outside the range duplicate points or change the sign of $\sin\varphi$.
+ **Non-uniqueness.** At $\rho=0$ both angles are undefined; on the $z$-axis $\theta$ is undefined and $\varphi$ is $0$ or $\pi$; $\theta$ and $\theta+2\pi$ agree. The exceptional sets have zero volume. Stated.
+ **Coordinate surfaces.** $\rho=R$ is a sphere; $\theta=\alpha$ a half-plane; $\varphi=\beta$ a cone. For $\varphi=\beta$, $z=\rho\cos\beta$ and $r=\rho\sin\beta$, so $z=\cot\beta\,r$; at $\beta=\pi/2$ this is $z=0$, and at $\beta=0$ it degenerates to the positive $z$-axis. Direct substitution.
+ **Jacobian determinant (4).** Expansion of the displayed $3\times3$ matrix gives $-\rho^2\sin\varphi$ for the column order $(\rho,\theta,\varphi)$. The ordering is left-handed, hence the negative sign; the absolute value is $\rho^2\sin\varphi$. The sign and magnitude were checked numerically at three random points.
+ **Geometric volume element.** The sides are $d\rho$, $\rho\,d\varphi$ and $\rho\sin\varphi\,d\theta$; the coordinate directions are orthogonal, so the volume is their product. Explained.
+ **Ball volume.** $\int_0^{2\pi}d\theta\cdot\int_0^\pi\sin\varphi\,d\varphi\cdot\int_0^R\rho^2\,d\rho=2\pi\cdot2\cdot R^3/3=4\pi R^3/3$.
+ **Second moment.** $\iiint_B z^2=\int\rho^4\cos^2\varphi\sin\varphi\,d\rho\,d\varphi\,d\theta=(1/5)(2/3)(2\pi)=4\pi/15$. Cross-check: $\iiint(x^2+y^2+z^2)=\iiint\rho^2\,dV=2\pi\cdot2\cdot1/5=4\pi/5$, and symmetry divides by $3$.
+ **Ice-cream cone.** $\rho\le2$, $0\le\varphi\le\pi/4$; the integral is $2\pi\cdot(8/3)\cdot(1-\sqrt2/2)=(16\pi/3)(1-\sqrt2/2)$.
+ **Radial density.** $\int_0^1(1+\rho)\rho^2\,d\rho=1/3+1/4=7/12$; multiplying by $4\pi$ gives $7\pi/3$. Greater than the unit ball volume $4\pi/3$, as an increasing density requires.
+ **Spherical cap.** The cap $z\ge a$ is not star-shaped from the origin for $a>0$: along a ray at angle $\varphi$, the plane is reached at $\rho=a/\cos\varphi$. Hence the radial limits are $a\sec\varphi\le\rho\le R$ and $0\le\varphi\le\arccos(a/R)$. The integral is
  $$V=\frac{2\pi}{3}\int_0^{\arccos(a/R)}(R^3-a^3\sec^3\varphi)\sin\varphi\,d\varphi=\frac{\pi}{3}(2R^3-3R^2a+a^3).$$
  At $a=0$ this is $2\pi R^3/3$; at $a=R$ it is $0$. The first draft of this section incorrectly used $0\le\rho\le R$, which computes a cone, not the cap; the correction was checked numerically against the exact formula and against the one-dimensional slice integral $\pi\int_a^R(R^2-z^2)\,dz$.
+ **Pitfalls.** The wrong polar angle changes $z$ from $\rho\cos\varphi$ to $\rho\sin\varphi$; omitting $\sin\varphi$ multiplies the ball volume by $\pi/2$; $\rho=R$ is a sphere while $r=R$ is a cylinder; using the full $\theta$-range for a sector multiplies by the wrong angular factor. Each is stated with its consequence.

## Independent checks

Python 3 script `work/checks/verify_batch6.py` (outside the repository), nested composite Simpson quadrature with $n=120$ per variable (tolerance $10^{-6}$ for the three-dimensional spherical checks):

+ ball radius $2$: computed $33.5103217258$, exact $32\pi/3=33.5103216383$;
+ unit ball $z^2$: computed $0.837758089597$, exact $4\pi/15=0.837758040957$;
+ ice-cream cone: computed $4.90747298411$, exact $(16\pi/3)(1-\sqrt2/2)=4.90747298406$;
+ radial density mass: computed $7.33038287751$, exact $7\pi/3=7.33038285838$;
+ spherical cap with $R=1$, $a=0.5$: computed $0.654498469498$, exact $\pi/3(2-3a+a^3)=0.654498469498$.

All checks passed. The cap was also checked by the independent slice formula $\pi\int_{0.5}^1(1-z^2)\,dz=0.6544984695$. The spherical determinant was evaluated numerically at random points; the computed value was $-\rho^2\sin\varphi$ each time.

## Limitations

+ No LaTeX renderer, Pandoc or TeX installation is available (`pandoc` and `pdflatex` not found); the Markdown was checked structurally but not rendered.
+ The live route `https://algebrica.org/spherical-coordinates/` is proposed, not known to exist.
+ The change-of-variables theorem is invoked, not reproved; the sibling entry supplies the proof sketch.
+ The spherical cap example was corrected during drafting; the erroneous star-shaped description was removed rather than left as an alternative.
+ Open issues and pull requests in the upstream repository were not inspected.
+ Links to sibling batch articles are unpublished dependencies until this batch is merged.

## Figure briefs

See `figure-briefs.md` in this directory.
