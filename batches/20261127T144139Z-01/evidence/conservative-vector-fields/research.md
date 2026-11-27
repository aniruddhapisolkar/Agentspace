# Research evidence — Conservative Vector Fields

Batch: `20261127T144139Z-01`
Slug: `conservative-vector-fields`
Article: `multivariable-calculus/conservative-vector-fields.md`
Category: `multivariable-calculus` (provisional)
Research date: 2026-11-27

## Coverage check

The upstream repository `antoniolupetti/algebrica` was searched by filename and body text for "conservative", "potential function", "path independent" and "gradient field".

+ No upstream article is titled or devoted to conservative vector fields.
+ Upstream has no multivariable-calculus category at all; the nearest material is in `vectors-and-matrices`, which treats finite-dimensional vectors and matrices, not fields.
+ The local staging repository already has `multivariable-calculus/line-integrals.md` and `multivariable-calculus/vector-fields.md`, which introduce path independence and the curl test briefly. This article is a focused complement: it develops the equivalence, the potential-construction algorithm, the punctured-plane obstruction and the energy interpretation in full, and links back rather than repeating their worked examples.

Conclusion: not a duplicate. Open issues and pull requests were not inspected; no claim is made about planned upstream work.

## Scope and reader contract

After reading the article, the reader can:

+ define a conservative field and a potential function on an open connected domain;
+ prove that two potentials differ by a constant and interpret level sets as equipotentials;
+ derive the fundamental theorem for line integrals from the chain rule and use it to prove path independence;
+ prove the converse on an open connected domain by constructing a potential from the line integral;
+ derive the curl and cross-partial tests as necessary conditions;
+ state the sufficiency theorem on simply connected domains and explain what its proof uses;
+ compute the circulation of the punctured-plane field and explain why zero curl does not give a potential there;
+ construct potentials in two and three variables by integration;
+ interpret conservative forces through potential energy and conservation of total energy;
+ distinguish zero curl, zero divergence, path independence and simple connectedness.

Assumed prerequisites: [vector fields](../vector-fields/), [line integrals](../line-integrals/), [curl](../curl/), partial derivatives and the chain rule.

Exclusions: de Rham cohomology, the full topological proof of the Poincaré lemma, the Helmholtz decomposition, and non-conservative forces such as friction that are not functions of position.

## Sources consulted

1. OpenStax, *Calculus Volume 3*, §6.3 "Conservative Vector Fields".
   URL: https://openstax.org/books/calculus-volume-3/pages/6-3-conservative-vector-fields
   Accessed: 2026-11-27. Full text read.
   Supports: the definition of conservative field and potential; Theorem 6.7 (Fundamental Theorem for Line Integrals); Theorem 6.8 (path independence of conservative fields); Theorem 6.9 (path-independence test, with the constructive proof); the cross-partial test for simply connected domains; the potential-construction algorithm; the gravitational example and the energy interpretation.
   Use: theorem statements, hypotheses, proof strategy and the potential algorithm.

2. Paul Dawkins, *Paul's Online Math Notes*, Calculus III, "Fundamental Theorem for Line Integrals".
   URL: https://tutorial.math.lamar.edu/Classes/CalcIII/FundThmLineIntegrals.aspx
   Accessed: 2026-11-27. Full text read.
   Supports: independent statement and proof of the fundamental theorem; the equivalence of conservative, path-independent and zero-circulation conditions; the construction of a potential by integrating from a base point; worked examples of conservative and non-conservative fields.
   Use: independent confirmation of the equivalence and the sign conventions.

3. OpenStax, *Calculus Volume 3*, §6.1 "Vector Fields" and §6.5 "Divergence and Curl".
   URLs: https://openstax.org/books/calculus-volume-3/pages/6-1-vector-fields and https://openstax.org/books/calculus-volume-3/pages/6-5-divergence-and-curl
   Accessed: 2026-11-27.
   Supports: the gradient-field examples, the circulation interpretation and the component form of the curl.
   Use: notational consistency with the existing staging articles.

4. Algebrica upstream `derivatives/partial-derivatives.md` and `vectors-and-matrices/vectors.md`.
   URLs: https://algebrica.org/partial-derivatives/ and https://algebrica.org/vectors/
   Accessed through the upstream clone, 2026-11-27.
   Supports: partial-derivative notation, equality of mixed partials, and vector notation.
   Use: house notation.

## Definitions and conventions selected

+ $D$ is open and connected; "simply connected" means every closed curve in $D$ contracts to a point inside $D$.
+ $\mathbf{F}=\nabla f$; $f$ is determined up to an additive constant on a connected domain.
+ The scalar curl in the plane is $Q_x-P_y$; the spatial curl is $\nabla\times\mathbf{F}$.
+ The gravitational field is $\mathbf{F}=-GM\mathbf{r}/r^3$ and the potential function is $f=GM/r$; the potential energy is $U=-GMm/r$.
+ Positive circulation is counterclockwise in the plane, consistent with the right-hand rule.

## Proofs and scope

+ The fundamental theorem is proved for a smooth curve by the chain rule and the fundamental theorem of calculus, then extended to piecewise smooth curves by summation. This is a complete proof of the theorem as stated.
+ The converse (path independence implies a potential) is proved by the horizontal-segment difference quotient. The proof is complete for a $C^0$ field on an open connected domain; continuity is used when passing to the limit.
+ The sufficiency of zero curl on a simply connected domain is stated, with the Green's-theorem argument for a region bounded by two paths and an explicit note that the general topological extension is quoted. It is not presented as a complete proof for arbitrary simply connected domains.
+ The punctured-plane computation is exact: $Q_x=P_y=(y^2-x^2)/(x^2+y^2)^2$ and the circulation is $2\pi$.

## Independent example checks

All arithmetic was recomputed by hand and cross-checked with a short Python script using finite-difference gradients and composite Simpson quadrature.

+ (18) $f=e^x\sin y$: $f_x=e^x\sin y=P$, $f_y=e^x\cos y=Q$; $Q_x=P_y=e^x\cos y$.
+ (19)–(22) $\mathbf{F}=\langle2xy+z^2,x^2+3y^2,2xz\rangle$: $f=x^2y+y^3+xz^2$; all three partials reproduce the components; all three cross partials vanish.
+ (23) $f(1,1,1)-f(0,0,0)=3$; direct evaluation along $\mathbf{r}(t)=\langle t,t,t\rangle$ gives $\int_0^1 9t^2\,dt=3$.
+ (25) $\int_0^1(t^4+2t^2)\,dt=1/5+2/3=13/15$.
+ (26) $\int_0^1(t^2+t)\,dt=1/3+1/2=5/6$.
+ (15) the integrand is identically $1$ on the unit circle, so the integral is $2\pi$.
+ The curl of $\langle y^2,x\rangle$ is $1-2y$, which vanishes only on $y=1/2$.

Numerical agreement supports the algebra but is not offered as a proof of any theorem.

## Checks performed and limitations

+ File encoding is UTF-8 with LF endings; front matter, H2-only headings, `+` bullets and `- - -` separators follow the staging corpus.
+ All links were checked against files present in the staging repository at the batch commit, not against live site routes.
+ LaTeX was not rendered: no TeX renderer is installed in this environment. Delimiters and environments were inspected manually.
+ The upstream repository has no corresponding article, so no upstream prose or figures were copied.
+ Open issues and pull requests in the upstream repository were not inspected.
