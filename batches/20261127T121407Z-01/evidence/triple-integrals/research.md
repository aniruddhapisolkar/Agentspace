# Research evidence — Triple Integrals

Batch: `20261127T121407Z-01`
Slug: `triple-integrals`
Article: `multivariable-calculus/triple-integrals.md`
Category: `multivariable-calculus` (provisional)
Research date: 2026-11-27

## Coverage check

Upstream `antoniolupetti/algebrica` was searched by filename and body text for "triple integral", "volume integral", "mass", "centre of mass" and "Fubini".

+ `integrals/definite-integrals.md` and the other files under `integrals/` treat one-dimensional integration only.
+ `integrals/volumes-from-parallel-cross-sections.md` computes volumes by slicing with a single integral. It does not define an integral over a solid.
+ No article with "triple integral", "volume integral" or a three-dimensional Riemann sum in its title or body was found.
+ No article treats centres of mass of solids.

Conclusion: not a duplicate. The closest material is volume by slicing, which the present entry derives as a consequence of the triple integral rather than assuming. Open issues and pull requests were not inspected; no claim is made about planned upstream work.

## Scope and reader contract

After reading the article, the reader can:

+ define the triple integral over a box by Riemann sums and by lower and upper Darboux sums;
+ state the oscillation criterion and the continuity and zero-boundary sufficiency conditions;
+ use linearity, monotonicity, additivity, the mean value inequality and the product rule over a box;
+ define the integral over a general solid by extension with an indicator function;
+ recognise a $z$-simple solid, identify its shadow and set up the iterated integral;
+ evaluate integrals over a cube and a tetrahedron, and recover a centroid from first moments;
+ compute mass and centre of mass for a solid with variable density;
+ explain why an unbounded integrand and a highly oscillatory integrand are not Riemann integrable, and why iterated integrals can disagree without integrability.

Assumed prerequisites: the [double integral](../multivariable-calculus/double-integrals.md), one-dimensional integration, continuity and uniform continuity on compact sets, and the geometry of planes, spheres and cylinders. Exclusions: the proof of Fubini's theorem (sibling entry), the change-of-variables formula (sibling entry), improper multiple integrals, and vector surface integrals.

## Sources consulted

1. University of Toronto, MAT237, *Multivariable Calculus*, §4.2 "Integration in Two and More Dimensions", subsection "Integration in Three or More Dimensions".
   URL: https://www.math.toronto.edu/courses/mat237y1/20199/notes/Chapter4/S4.2.html
   Accessed: 2026-11-27. Full text read, including the three-dimensional subsection.
   Supports: the definition of a partition of a box, sub-boxes and their volumes, lower and upper sums, the integrability criterion, the properties of the integral, integration over general sets by extension, and the zero-content condition on the boundary.
   Use: definition (1), criterion (2), properties, and the indicator definition (3). Prose rewritten.

2. University of Toronto, MAT237, *Multivariable Calculus*, §4.3 "Iterated Integrals".
   URL: https://www.math.toronto.edu/courses/mat237y1/20199/notes/Chapter4/S4.3.html
   Accessed: 2026-11-27. Full text read.
   Supports: the iterated-integral theorem in $n$ dimensions, the choice of integration order over a solid described by three sets of inequalities, and a worked ball computation.
   Use: formula (5), the $z$-simple reduction (6), and the tetrahedron setup.

3. OpenStax, *Calculus Volume 3*, §5.4 "Triple Integrals".
   URL: https://openstax.org/books/calculus-volume-3/pages/5-4-triple-integrals
   Accessed: 2026-11-27. Full text read.
   Supports: the triple Riemann sum, the definition over a box, the properties, the reduction to iterated integrals for continuous functions, the volume interpretation, and the extension to general regions.
   Use: independent confirmation of the definition, the properties and the volume interpretation.

4. Algebrica upstream `integrals/definite-integrals.md` and `integrals/volumes-from-parallel-cross-sections.md`.
   URLs: https://algebrica.org/definite-integrals/, https://algebrica.org/volumes-from-parallel-cross-sections/
   Accessed through the upstream clone, 2026-11-27.
   Supports: house notation, British-English register, and the existing volume-by-slicing language.

## Definitions and conventions selected

+ Box: $B=[a,b]\times[c,d]\times[e,g]$ with $a<b$, $c<d$, $e<g$.
+ Partition: independent partitions of the three intervals; sub-boxes $B_{ijk}$; mesh equal to the largest diameter.
+ Integral: limit of Riemann sums as the mesh tends to zero, independent of sample points; equivalently the common lower and upper Darboux integral.
+ General solid: $\iiint_D f=\iiint_B f\chi_D$ for a box $B\supseteq D$.
+ $z$-simple solid: $(x,y)\in\Omega$, $\varphi_1(x,y)\le z\le\varphi_2(x,y)$.
+ Volume element: $dV=dx\,dy\,dz$ in Cartesian coordinates; no Jacobian factor until the coordinate change is made.
+ British spelling: "centre of mass", "recognise", "emphasises" where used.

## Mathematical claims and justification

+ **Equivalence of Riemann and Darboux definitions.** Every Riemann sum lies between $L(f,P)$ and $U(f,P)$; the common limit exists exactly when the lower and upper integrals coincide. Stated; the one-dimensional proof transfers with triple indices and is given in MAT237 §4.2.
+ **Boundedness is necessary.** An unbounded sub-box makes $M_{ijk}=+\infty$ or $m_{ijk}=-\infty$, so no finite Darboux sum can satisfy (2). Explained.
+ **Continuous implies integrable.** Uniform continuity on the compact box gives $M_{ijk}-m_{ijk}<\varepsilon/\operatorname{vol}(B)$ on a fine partition. Argument stated.
+ **Boundary of zero volume.** A finite union of continuous graph surfaces has zero content; enclosing it in boxes of small total volume and using boundedness elsewhere gives the criterion. Stated as the standard consequence.
+ **Additivity.** Splitting along a plane face gives two integrals whose sum is the integral over the union; the common face has zero volume. Justified by the indicator definition.
+ **Product formula.** For $f=g(x)h(y)k(z)$ the triple sum separates into a product of three one-dimensional sums. Stated, with the iterated-integral alternative.
+ **Volume by slicing.** Integrating $1$ over a $z$-simple solid and performing the inner $z$-integral gives $\iint_\Omega(\varphi_2-\varphi_1)\,dA$. This is a direct computation, not an independent assumption.
+ **Cube example.** Each of $\iiint x$, $\iiint y$, $\iiint z$ equals $1/2$, so the integral of $x+y+z$ is $3/2$.
+ **Tetrahedron example.** $\int_0^{1-x-y}z\,dz=(1-x-y)^2/2$; integrating over the triangular shadow gives $\frac12\cdot\frac1{12}=\frac1{24}$. The volume is $\int_0^1(1-x)^2/2\,dx=1/6$, so $\bar z=(1/24)/(1/6)=1/4$, matching the symmetry value.
+ **Density example.** Mass $\int_0^1(1+z)\,dz=3/2$; first moment $\int_0^1(z+z^2)\,dz=5/6$; hence $\bar z=5/9>1/2$, consistent with density increasing upwards.
+ **Non-integrable examples.** $1/(x+y+z)$ is unbounded near the origin. The function $1_{\mathbb{Q}}(x)$ has lower sum $0$ and upper sum equal to the box volume on every partition.
+ **Disagreeing iterated integrals.** For $f=(x^2-y^2)/(x^2+y^2)^2$ on the unit square, $\int_0^1 f\,dx=-1/(1+y^2)$ and $\int_0^1 f\,dy=1/(1+x^2)$; the two iterated integrals are $-\pi/4$ and $\pi/4$. The function is unbounded near the origin, hence not Riemann integrable. This is presented as a warning and referred to the Fubini entry.

## Independent checks

Python 3 script `work/checks/verify_batch6.py` (outside the repository), nested composite Simpson quadrature with $n=120$ per variable:

+ cube $x+y+z$: computed $1.5$, exact $3/2$;
+ tetrahedron $z$: computed $0.0416666666667$, exact $1/24$;
+ tetrahedron volume: computed $0.166666666667$, exact $1/6$;
+ density mass: computed $1.5$, exact $3/2$;
+ density first moment: computed $0.833333333333$, exact $5/6$.

All five checks passed. The displayed antiderivative computations give the same values exactly; the quadrature is supporting evidence.

## Limitations

+ No LaTeX renderer, Pandoc or TeX installation is available (`pandoc` and `pdflatex` not found), so the Markdown was checked structurally but not rendered.
+ The live route `https://algebrica.org/triple-integrals/` is proposed, not known to exist.
+ The proof of Fubini's theorem in three dimensions is not reproduced; the article invokes it and links to the sibling entry.
+ Open issues and pull requests in the upstream repository were not inspected.
+ Links to sibling batch articles are unpublished dependencies until this batch is merged.

## Figure briefs

See `figure-briefs.md` in this directory.
