# Research evidence — Double Integrals

Batch: `20261127T121407Z-01`
Slug: `double-integrals`
Article: `multivariable-calculus/double-integrals.md`
Category: `multivariable-calculus` (provisional)
Research date: 2026-11-27

## Coverage check

Upstream `antoniolupetti/algebrica` was searched by filename and body text for "double integral", "multiple integral", "Fubini", "Riemann sum" and "iterated integral".

+ `integrals/definite-integrals.md` develops the one-dimensional Riemann integral, Darboux-style lower and upper sums, and the fundamental theorem. It does not define an integral over a plane region.
+ `lines-planes-conic-sections/polar-coordinates.md` §"Integration in polar coordinates" states the formula $\iint_D f\,dx\,dy=\iint_{D'}f(\rho\cos\theta,\rho\sin\theta)\rho\,d\rho\,d\theta$. It gives no definition of the double integral, no integrability theory and no iterated-integral theorem.
+ `functions/gaussian-function.md` uses the identity $I^2=\iint_{\mathbb{R}^2}e^{-(x^2+y^2)}\,dx\,dy$ to compute the Gaussian integral. The double integral is invoked, not developed.
+ No article with "double integral", "multiple integral", "Fubini" or "iterated integral" in its title was found.

Conclusion: not a duplicate. The polar article is partial coverage of one computational formula; the present entry supplies the definition, integrability, properties, general regions and evaluation that it presupposes. Open issues and pull requests were not inspected; no claim is made about planned upstream work.

## Scope and reader contract

After reading the article, the reader can:

+ define the double integral over a rectangle by Riemann sums and by lower and upper Darboux sums;
+ state and use the oscillation criterion for integrability;
+ explain why boundedness is required and why continuity, or continuity off a negligible set, is sufficient;
+ use linearity, monotonicity, additivity and the mean value inequality;
+ define the integral over a general region by extension with an indicator function and identify type I and type II regions;
+ evaluate double integrals over rectangles and triangles in either order, and reverse the order after redrawing the region;
+ interpret the integral as area, signed volume, average value and mass;
+ give examples of an unbounded non-integrable function and a bounded nowhere-integrable function.

Assumed prerequisites: the one-dimensional Riemann integral and its properties, continuity and uniform continuity on compact sets, and the notion of area for elementary plane regions. Exclusions: the proof of Fubini's theorem (sibling entry), the change-of-variables formula (sibling entry), improper multiple integrals, and the Lebesgue integral.

## Sources consulted

1. University of Toronto, MAT237, *Multivariable Calculus*, §4.2 "Integration in Two and More Dimensions".
   URL: https://www.math.toronto.edu/courses/mat237y1/20199/notes/Chapter4/S4.2.html
   Accessed: 2026-11-27. Full text read.
   Supports: the rectangle partition, subrectangles and boxes, lower and upper sums, the definition of integrability, the oscillation criterion, linearity and order properties, zero content, integration over non-rectangular sets by extension, and the theorem that a bounded function discontinuous only on a set of zero content is integrable.
   Use: the formal definition, criterion (2), the zero-content sufficiency statement, and the treatment of general regions. Prose is rewritten; no passages copied.

2. University of Toronto, MAT237, *Multivariable Calculus*, §4.3 "Iterated Integrals".
   URL: https://www.math.toronto.edu/courses/mat237y1/20199/notes/Chapter4/S4.3.html
   Accessed: 2026-11-27. Full text read.
   Supports: the iterated-integral theorem for an integrable function whose sections are integrable, the reduction of integrals over non-rectangular regions to iterated integrals, and worked examples including integration over a ball.
   Use: the rectangular and type I/II formulas (5) and (6), presented here as the computational form of Fubini's theorem.

3. OpenStax, *Calculus Volume 3*, §5.1 "Double Integrals over Rectangular Regions".
   URL: https://openstax.org/books/calculus-volume-3/pages/5-1-double-integrals-over-rectangular-regions
   Accessed: 2026-11-27. Full text read.
   Supports: the double Riemann sum and the definition (5.1), the list of properties, the statement of Fubini's theorem for continuous functions on a rectangle (Theorem 5.2), the volume and average-value interpretations, and the integrability of bounded functions with discontinuities on finitely many smooth curves.
   Use: independent confirmation of the definition, properties and the continuous-case Fubini statement. The article's Darboux formulation and zero-content discussion come from MAT237 rather than OpenStax.

4. Algebrica upstream `integrals/definite-integrals.md`, `lines-planes-conic-sections/polar-coordinates.md` and `functions/gaussian-function.md`.
   URLs: https://algebrica.org/definite-integrals/, https://algebrica.org/polar-coordinates/, https://algebrica.org/gaussian-function/
   Accessed through the upstream clone, 2026-11-27.
   Supports: house notation, British-English register, heading style, the one-variable Riemann-sum presentation, and the existing polar area element.

## Definitions and conventions selected

+ Rectangle: $R=[a,b]\times[c,d]$ with $a<b$, $c<d$.
+ Partition: independent partitions of the two sides; subrectangles $R_{ij}$; mesh equal to the largest diameter.
+ Integral: limit of Riemann sums as the mesh tends to zero, independent of sample points; equivalently the common value of the lower and upper Darboux integrals.
+ Integrability criterion: for every $\varepsilon>0$ there is a partition with $U-L<\varepsilon$.
+ General region: $\iint_D f=\iint_R f\chi_D$ for a rectangle $R\supseteq D$.
+ Type I: $a\le x\le b$, $g_1(x)\le y\le g_2(x)$; type II: $c\le y\le d$, $h_1(y)\le x\le h_2(y)$.
+ British spelling: "optimisation", "emphasises", "behaviour" where used.

## Mathematical claims and justification

+ **Equivalence of Riemann and Darboux definitions.** Every Riemann sum lies between $L(f,P)$ and $U(f,P)$; a common limit independent of samples exists exactly when the lower and upper integrals coincide. Stated, not proved in full; the one-dimensional proof transfers verbatim and MAT237 gives it.
+ **Boundedness is necessary.** On a subrectangle where $f$ is unbounded above, $M_{ij}=+\infty$, so the upper sum is not finite; the Darboux criterion cannot hold. Explained in the text.
+ **Continuous implies integrable.** Uniform continuity on the compact rectangle makes $M_{ij}-m_{ij}<\varepsilon/(\text{area}(R))$ on a fine enough partition, so $U-L<\varepsilon$. Argument stated in one paragraph.
+ **Discontinuities on a finite union of curves are harmless.** Such a set has zero area; enclosing it in rectangles of total area $<\varepsilon$ and using boundedness elsewhere gives $U-L<C\varepsilon$. Stated as a standard consequence, not expanded into a full proof.
+ **Additivity (4).** Both sides equal the integral of the extension over a common containing rectangle; the shared boundary has zero area. Justified by the indicator definition.
+ **Iterated formula (5).** Quoted as the continuous special case of Fubini's theorem; the proof is deferred to the sibling entry. This is an explicitly scoped invocation, not a claimed proof.
+ **Rectangle example.** $\int_0^2(2x+3y)\,dy=4x+6$ and $\int_0^1(4x+6)\,dx=8$. Checked both orders.
+ **Triangle example.** $\int_0^1\int_0^x xy\,dy\,dx=\int_0^1x^3/2\,dx=1/8$; the type II computation $\int_0^1\int_y^1 xy\,dx\,dy=1/8$ verifies it independently.
+ **Reversed-order example.** On $0\le x\le y\le1$, $\int_0^1\int_0^y e^{y^2}\,dx\,dy=\int_0^1ye^{y^2}\,dy=(e-1)/2$.
+ **Average example.** $\int_0^1\int_0^1(x^2+y^2)\,dy\,dx=1/3+1/3=2/3$, within $[0,2]$.
+ **Non-integrable examples.** $1/(x+y)$ is unbounded near the origin. The function $f=1$ when $x\in\mathbb{Q}$ and $0$ otherwise has $L=0$, $U=1$ on every partition, and its inner integral is the Dirichlet function, so no iterated Riemann integral exists.
+ **Diagonal example.** $f=1$ on $x=y$ and $0$ elsewhere is discontinuous on a set of zero area, hence integrable with integral $0$.

## Independent checks

Python 3 script `work/checks/verify_batch6.py` (outside the repository), composite Simpson quadrature with $n=400$ per direction (2000 in one dimension):

+ rectangle $2x+3y$ over $[0,1]\times[0,2]$: computed $8$, exact $8$;
+ triangle $xy$: computed $0.125$, exact $1/8$;
+ reversed order $e^{y^2}$: computed $0.859140914230$, exact $(e-1)/2=0.859140914230$;
+ average $x^2+y^2$: computed $0.666666666667$, exact $2/3$.

All four checks passed. The exact polynomial values were also computed by hand from the antiderivatives shown in the article. Numerical quadrature is supporting evidence only; the displayed antiderivative computations are the proof.

## Limitations

+ No LaTeX renderer, Pandoc or TeX installation is available on this machine (`pandoc` and `pdflatex` not found), so the Markdown was checked structurally but not rendered. No claim of rendered verification is made.
+ The live route `https://algebrica.org/double-integrals/` is proposed, not known to exist; the upstream repository has no such article.
+ The proof of Fubini's theorem is not reproduced here; the article says so and links to the sibling entry.
+ Open issues and pull requests in the upstream repository were not inspected.
+ Links to sibling batch articles are unpublished dependencies until this batch is merged.

## Figure briefs

See `figure-briefs.md` in this directory.
