# Research evidence — Fundamental Theorem for Line Integrals

Batch: `20261127T144139Z-01`
Slug: `fundamental-theorem-for-line-integrals`
Article: `multivariable-calculus/fundamental-theorem-for-line-integrals.md`
Category: `multivariable-calculus` (provisional)
Research date: 2026-11-27

## Coverage check

Upstream `antoniolupetti/algebrica` was searched by filename and body text for "fundamental theorem for line integrals", "path independent", "conservative" and "potential". No upstream article covers the theorem.

The staging repository already has `multivariable-calculus/line-integrals.md`, which states the theorem in a section and uses it once, and `multivariable-calculus/conservative-vector-fields.md`, written in this batch, which treats the equivalence and the curl test. This article is the dedicated theorem treatment: full hypothesis audit, complete proof, the converse construction, the higher-dimensional analogy, the gravitational sign conventions and a path-dependence counterexample with both semicircles computed.

Conclusion: not a duplicate. Upstream issues and pull requests were not inspected.

## Scope and reader contract

After reading the article, the reader can:

+ state the theorem with the correct regularity, curve and domain hypotheses;
+ explain the role of each hypothesis and the effect of reversing orientation;
+ prove the theorem for smooth and piecewise smooth curves;
+ derive path independence and zero circulation as corollaries;
+ prove the converse by constructing a potential from the line integral;
+ recover a potential by integrating along coordinate axes on a rectangular domain;
+ evaluate a conservative line integral by endpoints and verify it by direct parameterization;
+ compute both semicircle integrals for the rotational field and conclude non-conservation;
+ derive the gravitational work formula and reconcile the signs of potential and potential energy;
+ explain the analogy with the one-variable fundamental theorem and with exact one-forms;
+ identify the cases in which the theorem does not apply.

Assumed prerequisites: [line integrals](../line-integrals/), [conservative vector fields](../conservative-vector-fields/), the chain rule, the fundamental theorem of calculus and the [curl](../curl/).

Exclusions: a full proof of Stokes' theorem, differential-form integration on manifolds, and the topological classification of domains beyond the role of simple connectedness.

## Sources consulted

1. OpenStax, *Calculus Volume 3*, §6.3 "Conservative Vector Fields", Theorem 6.7.
   URL: https://openstax.org/books/calculus-volume-3/pages/6-3-conservative-vector-fields
   Accessed: 2026-11-27. Full text read.
   Supports: the exact statement of the Fundamental Theorem for Line Integrals, its chain-rule proof, path independence (Theorem 6.8), the constructive converse (Theorem 6.9), and the warning that a continuous vector field need not have a potential.
   Use: theorem statement, hypotheses and proof.

2. Paul Dawkins, *Paul's Online Math Notes*, Calculus III, "Fundamental Theorem for Line Integrals".
   URL: https://tutorial.math.lamar.edu/Classes/CalcIII/FundThmLineIntegrals.aspx
   Accessed: 2026-11-27. Full text read.
   Supports: an independent proof, the equivalence of conservative and path-independent fields, the base-point construction of a potential, and the orientation convention.
   Use: independent confirmation and the potential-from-integral construction.

3. OpenStax, *Calculus Volume 3*, §6.2 "Line Integrals".
   URL: https://openstax.org/books/calculus-volume-3/pages/6-2-line-integrals
   Accessed: 2026-11-27.
   Supports: the definition of the vector line integral, orientation reversal and the component notation.
   Use: notational consistency.

4. Algebrica upstream `derivatives/partial-derivatives.md`.
   URL: https://algebrica.org/partial-derivatives/
   Accessed through the upstream clone, 2026-11-27.
   Supports: gradient and partial-derivative notation.
   Use: house notation.

## Definitions and conventions selected

+ $C$ is piecewise smooth and oriented from $A$ to $B$; $f$ is $C^1$ on an open set containing $C$.
+ The theorem is stated for $\int_C\nabla f\cdot d\mathbf{r}$ and specialised to $\mathbf{F}=\nabla f$.
+ Reversing orientation multiplies the integral by $-1$.
+ The gravitational potential function is $GMm/r$; the potential energy is $-GMm/r$, with $\mathbf{F}=-\nabla U$.
+ The rotational field is $\langle-y,x\rangle$, with scalar curl $2$.

## Proofs and scope

+ The smooth case is proved completely by the chain rule and the fundamental theorem of calculus.
+ The piecewise case is proved completely by summation and telescoping; the corner argument is explicit.
+ The converse is proved completely for a continuous field on an open connected domain, using a horizontal difference quotient and continuity.
+ The potential formula (12) is justified by differentiating under the integral and using the equality of cross partials; the article states the rectangular scope rather than claiming it for every domain.
+ The gravitational work formula is derived from the theorem with the sign conventions checked.

## Independent example checks

All computations were repeated by hand and checked with exact symbolic differentiation in Python.

+ (14) $f=x^2y$: $f_x=2xy=P$, $f_y=x^2=Q$.
+ (15)–(17) $f=xyz$: $f_x=yz$, $f_y=xz$, $f_z=xy$; $f(4,5,6)-f(1,2,3)=120-6=114$.
+ (18)–(21) direct computation along the segment: $\mathbf{F}(\mathbf{r}(t))=\langle6+15t+9t^2,3+12t+9t^2,2+9t+9t^2\rangle$, dot with $\langle3,3,3\rangle$ gives $33+108t+81t^2$, integral $114$.
+ (24) upper semicircle: integrand $1$, integral $\pi$.
+ (25) lower semicircle with decreasing parameter: integral $-\pi$.
+ (28) gravitational work: $GMm(1/r_2-1/r_1)$; for $GMm=1$, $r_1=1$, $r_2=2$ the value is $-1/2$, consistent with inward force and outward displacement.
+ The scalar curl of $\langle-y,x\rangle$ is $2$, so the field cannot be conservative on $\mathbb{R}^2$.

## Checks performed and limitations

+ UTF-8/LF encoding, front matter, H2-only headings, `+` bullets and `- - -` separators were checked against the staging corpus.
+ Internal links point to files present in the staging repository at the commit, not to live site routes.
+ LaTeX was not rendered; no TeX renderer is installed. Delimiters and environments were inspected manually.
+ No upstream prose or figures were copied; the upstream repository has no corresponding entry.
+ Upstream issues and pull requests were not inspected.
