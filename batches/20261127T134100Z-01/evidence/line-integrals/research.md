# Research evidence — Line Integrals

Batch: `20261127T134100Z-01`
Slug: `line-integrals`
Article: `multivariable-calculus/line-integrals.md`
Category: `multivariable-calculus` (provisional)
Research date: 2026-11-27

## Coverage check

Upstream `antoniolupetti/algebrica` was searched by filename and body text for "line integral", "work integral", "circulation", "path independent" and "conservative field".

+ No upstream article defines or computes line integrals.
+ `integrals/arc-length-of-a-curve.md` gives the arc-length integral for planar curves, which is the case $f=1$ of the scalar line integral; it does not treat densities, vector fields or orientation.
+ `vectors-and-matrices/vectors.md` and `derivatives/partial-derivatives.md` supply vector notation and the gradient but not the integration theory.
+ No upstream article treats the fundamental theorem for line integrals or the punctured-plane circulation.

Conclusion: not a duplicate. The arc-length entry is linked as a prerequisite. Open issues and pull requests were not inspected; no claim is made about planned upstream work.

## Scope and reader contract

After reading the article, the reader can:

+ define the scalar line integral by a partition of arc length and compute it from a parameterization;
+ use it for mass, centre of mass and average value of a wire;
+ define the vector line integral and compute work and circulation;
+ explain the orientation dependence and the relation between the two integrals;
+ evaluate a path-dependent example along two curves with the same endpoints;
+ state and prove the fundamental theorem for line integrals;
+ list the equivalent characterizations of a conservative field on an open connected domain;
+ find a potential by integration and use it to evaluate a line integral;
+ state the curl test on a simply connected domain and the punctured-plane obstruction;
+ integrate over piecewise smooth curves and reparameterize correctly.

Assumed prerequisites: [arc length](../arc-length-of-a-curve/), [partial derivatives](../partial-derivatives/), [vector fields](../vector-fields/), and one-variable integration. Exclusions: surface integrals, the full proofs of Green's theorem and Stokes' theorem, differential forms, and the general theory of line integrals of vector-valued functions with respect to arc length beyond the scalar case.

## Sources consulted

1. OpenStax, *Calculus Volume 3*, §6.2 "Line Integrals" and §6.3 "Conservative Vector Fields".
   URLs: https://openstax.org/books/calculus-volume-3/pages/6-2-line-integrals and https://openstax.org/books/calculus-volume-3/pages/6-3-conservative-vector-fields
   Accessed: 2026-11-27. Full text read.
   Supports: the partition definition of the scalar line integral, the parameterization formula, orientation independence of the scalar integral, the vector line integral, the work interpretation, the fundamental theorem for line integrals, path independence, the equivalence with conservative fields, the curl test on simply connected domains, and the flux/circulation discussion.
   Use: definitions, theorem statements, orientation conventions and the example structure.

2. Paul Dawkins, *Paul's Online Math Notes*, Calculus III, "Line Integrals — Part I" and "Line Integrals of Vector Fields".
   URLs: https://tutorial.math.lamar.edu/Classes/CalcIII/LineIntegralsPtI.aspx and https://tutorial.math.lamar.edu/Classes/CalcIII/LineIntegralsVectorFields.aspx
   Accessed: 2026-11-27. Full text read.
   Supports: the scalar line integral with respect to arc length, the evaluation formula, piecewise curves, the vector line integral, orientation reversal, and worked examples of work integrals.
   Use: independent confirmation of the formulas and sign conventions.

3. Algebrica upstream `integrals/arc-length-of-a-curve.md`.
   URL: https://algebrica.org/arc-length-of-a-curve/
   Accessed through the upstream clone, 2026-11-27.
   Supports: the arc-length element and the house notation for parameterized curves.
   Use: the internal link and the $f=1$ specialization.

## Definitions and conventions selected

+ Scalar line integral $\int_C f\,ds$ with $ds=\lVert\mathbf{r}'(t)\rVert\,dt.$
+ Vector line integral $\int_C\mathbf{F}\cdot d\mathbf{r}$ with $d\mathbf{r}=\mathbf{r}'(t)\,dt.$
+ Orientation by increasing parameter; reversing orientation changes the vector integral's sign and leaves the scalar integral unchanged.
+ Conservative field $\mathbf{F}=\nabla f$ on an open connected domain; potential $f.$
+ Circulation $\oint_C\mathbf{F}\cdot d\mathbf{r}$ for a closed curve.
+ British spelling: "centre", "recognise", "parameterization" (corpus form), "nonnegative".

## Mathematical claims and justification

+ **Partition definition (2).** Riemann sums with respect to arc length; existence for continuous $f$ on a piecewise smooth curve follows from uniform continuity and the convergence of arc-length sums.
+ **Parameterization formula (3)–(4).** The chain rule gives $ds=\lVert\mathbf{r}'(t)\rVert\,dt.$ The value is independent of an orientation-preserving or reversing reparameterization because the absolute value of the Jacobian appears.
+ **Arc length (5).** The case $f=1.$
+ **Circle example (6).** $\lVert\mathbf{r}'\rVert=1$ and $\int_0^{2\pi}\cos^2t\,dt=\pi.$
+ **Mass and centre of mass (7)–(9).** Standard weighted integrals with respect to arc length. The semicircle computation gives $\bar y=2R/\pi$; checked by direct integration.
+ **Vector integral (10)–(11).** Definition from the limit of $\sum\mathbf{F}(P_i^*)\cdot\Delta\mathbf{r}_i;$ the parameterized form follows by the mean value theorem and continuity.
+ **Orientation reversal (12).** Reversing the parameterization changes the sign of $d\mathbf{r}$ and preserves the field values.
+ **Relation (13).** $\mathbf{F}\cdot d\mathbf{r}=(\mathbf{F}\cdot\mathbf{T})\,ds$ with $\mathbf{T}=\mathbf{r}'/\lVert\mathbf{r}'\rVert.$
+ **Path-dependent example (14)–(15).** Parabola: $\int_0^1(t^2+2t^4)\,dt=1/3+2/5=11/15.$ Segment: $\int_0^1 2t^2\,dt=2/3.$ The values differ, so the field is not conservative. The scalar curl is $y,$ nonzero off the $x$-axis.
+ **Fundamental theorem (16).** Chain rule plus the fundamental theorem of calculus; the piecewise case telescopes.
+ **Equivalence of the three characterizations.** (i) $\Rightarrow$ (ii) is (16); (ii) $\Rightarrow$ (iii) because a closed curve has equal endpoints; (iii) $\Rightarrow$ (ii) by joining two paths into a loop; (iii) $\Rightarrow$ (i) by defining the potential as a path integral and differentiating. The article states the continuity requirement and summarizes the differentiation step rather than reproducing every estimate.
+ **Potential example.** $f=x^2y+y^3,$ $\nabla f=\langle2xy,x^2+3y^2\rangle,$ and $f(1,1)-f(0,0)=2.$
+ **Finding a potential.** Integrate $P$ in $x,$ differentiate in $y,$ match $Q,$ integrate $\phi'.$ The constant is arbitrary.
+ **Closed curves and Green (19).** Green's theorem for a positively oriented boundary; the orientation convention is stated. The punctured-plane field has zero curl but circulation $2\pi,$ so the simple-connectedness hypothesis is essential.
+ **Helix work (20).** $\mathbf{F}\cdot\mathbf{r}'=1+t,$ so the integral is $2\pi+2\pi^2.$
+ **Reparameterization (23).** Chain rule; the sign of $\phi'$ controls orientation.
+ **Flux integral (21).** Normal component with a chosen unit normal; for a closed curve the outward normal is standard. The article distinguishes it from the vector line integral.

## Independent checks

Python 3 numeric script (ad hoc, outside the repository):

+ scalar circle: midpoint rule with $200000$ intervals gives $\pi$ to machine precision;
+ parabola integral: $11/15=0.7333333333;$
+ straight segment: $2/3=0.6666666667;$
+ potential difference: $2;$
+ helix work: $2\pi+2\pi^2=26.02239447...;$ midpoint rule agrees;
+ semicircle centre: $2R/\pi$ for $R=1$ is $0.6366197724,$ and the direct integral gives the same.

All checks passed. The line integrals and potential differences are exact; the quadrature checks are numerical.

## Limitations

+ No LaTeX renderer, Pandoc or TeX installation is available (`pandoc` and `pdflatex` not found); the Markdown was checked structurally but not rendered.
+ The proposed route `https://algebrica.org/line-integrals/` is not known to be live.
+ The equivalence of the three characterizations of a conservative field is stated with a proof sketch, not a full $\varepsilon$-$\delta$ treatment.
+ Green's theorem and Stokes' theorem are stated only as context; their proofs are outside scope.
+ Surface integrals and differential forms are outside scope.
+ Open issues and pull requests in the upstream repository were not inspected.
+ Links to sibling batch articles are unpublished dependencies until this batch is merged.
