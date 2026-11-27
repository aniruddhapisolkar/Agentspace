# Research evidence — Curl

Batch: `20261127T134100Z-01`
Slug: `curl`
Article: `multivariable-calculus/curl.md`
Category: `multivariable-calculus` (provisional)
Research date: 2026-11-27

## Coverage check

Upstream `antoniolupetti/algebrica` was searched by filename and body text for "curl", "circulation", "irrotational", "Stokes' theorem" and "rotational field".

+ No upstream article defines the curl or proves Stokes' theorem.
+ `derivatives/partial-derivatives.md` introduces the Jacobian and mixed partials but not the curl.
+ `vectors-and-matrices/vectors.md` supplies the cross product used in the determinant mnemonic.
+ No upstream article treats the shear field, rigid rotation, or the punctured-plane obstruction.

Conclusion: not a duplicate. Open issues and pull requests were not inspected; no claim is made about planned upstream work.

## Scope and reader contract

After reading the article, the reader can:

+ define the curl by the determinant mnemonic and in expanded components;
+ derive the scalar curl as circulation per unit area and explain the right-hand rule;
+ compute the curl of rigid rotation, shear, radial and polynomial fields;
+ prove that a $C^2$ gradient field has zero curl;
+ state Stokes' theorem with the induced boundary orientation and reduce it to Green's theorem;
+ evaluate both sides of Stokes' theorem for a simple surface;
+ state the curl test for conservative fields and explain the role of simple connectedness;
+ write the curl in cylindrical and spherical coordinates;
+ use the product rules and the identity $\operatorname{curl}\operatorname{curl}\mathbf{F}=\nabla(\operatorname{div}\mathbf{F})-\Delta\mathbf{F}.$

Assumed prerequisites: [vector fields](../vector-fields/), [partial derivatives](../partial-derivatives/), the cross product, [line integrals](../line-integrals/) and [double integrals](../double-integrals/). Exclusions: a full proof of Stokes' theorem for arbitrary surfaces, de Rham cohomology, the Biot–Savart law, and the differential-form formulation.

## Sources consulted

1. OpenStax, *Calculus Volume 3*, §6.5 "Divergence and Curl" and §6.7 "Stokes' Theorem".
   URLs: https://openstax.org/books/calculus-volume-3/pages/6-5-divergence-and-curl and https://openstax.org/books/calculus-volume-3/pages/6-7-stokes-theorem
   Accessed: 2026-11-27. Full text read.
   Supports: the curl definition, the paddlewheel interpretation, the curl of a rotational field, the curl test for conservative fields (Theorem 6.18), the orientation convention for Stokes' theorem, and the statement relating the surface integral of curl to the boundary circulation.
   Use: definitions, interpretation, theorem statement and orientation.

2. Paul Dawkins, *Paul's Online Math Notes*, Calculus III, "Curl and Divergence".
   URL: https://tutorial.math.lamar.edu/Classes/CalcIII/CurlDivergence.aspx
   Accessed: 2026-11-27. Full text read.
   Supports: the determinant mnemonic, the component expansion, the facts about curl, the product rules, and the vector form of Green's theorem.
   Use: independent confirmation of signs, the shear example and the product rules.

3. Algebrica upstream `derivatives/partial-derivatives.md`.
   URL: https://algebrica.org/partial-derivatives/
   Accessed through the upstream clone, 2026-11-27.
   Supports: the notation for partial derivatives and the mixed-partial equality used in $\operatorname{curl}(\nabla f)=\mathbf{0}.$
   Use: notational consistency.

## Definitions and conventions selected

+ $\operatorname{curl}\mathbf{F}=\nabla\times\mathbf{F}$ with components as in (2).
+ Planar scalar curl $\partial_xQ-\partial_yP.$
+ Positive orientation: counterclockwise when viewed from the tip of the normal, consistent with the right-hand rule.
+ Stokes' theorem: $\iint_S(\operatorname{curl}\mathbf{F})\cdot\mathbf{n}\,dS=\oint_{\partial S}\mathbf{F}\cdot d\mathbf{r}.$
+ Cylindrical $(r,\theta,z)$ and spherical $(\rho,\theta,\varphi)$ conventions as in the batch.
+ British spelling: "centre", "recognise", "artefact" avoided; "clockwise", "counterclockwise".

## Mathematical claims and justification

+ **Determinant expansion (2).** Formal expansion of the symbolic determinant; each component is a difference of partial derivatives. The mnemonic is valid when the operators act on the third row.
+ **Planar reduction (3).** Setting $R=0$ and dropping $z$-dependence leaves only the third component.
+ **Circulation density (4)–(5).** The four edge integrals of a small counterclockwise rectangle are combined; the difference quotients tend to $Q_x$ and $P_y.$ Dividing by area gives the limit. This is a derivation for the $xy$-plane; the other components follow by cyclic permutation of the axes.
+ **Rigid rotation (7).** $\operatorname{curl}\langle-\omega y,\omega x,0\rangle=\langle0,0,2\omega\rangle.$ Direct differentiation.
+ **General rigid motion (8).** For $\mathbf{v}=\boldsymbol{\omega}\times\mathbf{r},$ the curl is $2\boldsymbol{\omega}.$ This follows by expanding $\boldsymbol{\omega}\times\mathbf{r}$ and differentiating, or from the antisymmetric part of the velocity gradient.
+ **Shear (10).** $\operatorname{curl}\langle y,0,0\rangle=\langle0,0,-1\rangle.$ The field has parallel arrows and nonzero curl; this is the standard warning that curl is not the same as visible circular motion.
+ **Radial field.** For $\mathbf{F}=g(r)\mathbf{r},$ each curl component is a difference of terms $g'(r)r_jr_k/r$ that cancel in pairs, and $\operatorname{curl}\mathbf{r}=\mathbf{0}.$ Hence the curl vanishes away from the origin.
+ **Gradient identity (11).** Componentwise equality of mixed partials for a $C^2$ function.
+ **Converse and counterexample (12).** The punctured-plane field has zero scalar curl, but its unit-circle integral is $2\pi;$ hence no global potential exists. The local potential is a polar angle, which has no single-valued branch on the punctured plane.
+ **Compatibility identities (13).** $\operatorname{curl}\nabla f=\mathbf{0}$ and $\operatorname{div}\operatorname{curl}\mathbf{F}=0,$ both by mixed partials.
+ **Stokes' theorem (14).** Statement with oriented piecewise smooth surface, induced boundary orientation, and $C^1$ field. The proof sketch partitions a graph surface, applies Green's theorem to projected patches, and cancels interior edges.
+ **Green reduction (15).** For a flat surface with normal $\mathbf{k},$ the curl flux is the scalar curl and the boundary circulation is the planar line integral.
+ **Stokes example.** $\mathbf{F}=\langle z,x,y\rangle$ has constant curl $\langle1,1,1\rangle;$ the unit disk has flux $\pi;$ the boundary integral is $\int_0^{2\pi}\cos^2t\,dt=\pi.$ The same boundary spanned by the upper hemisphere gives the same flux because the field is constant and only the projected area contributes.
+ **Cylindrical formula (16).** Standard formula; the $z$-component is $(1/r)\partial_r(rF_\theta)-(1/r)\partial_\theta F_r.$
+ **Spherical formula (17).** Standard formula in the $(\rho,\theta,\varphi)$ convention. The $e_\rho$ term carries $1/(\rho\sin\varphi)$ and differentiates $\sin\varphi\,F_\theta$ with respect to $\varphi.$
+ **Product rules (18)–(19).** Componentwise differentiation and collection; the cross product in (18) is not commutative. The identity (20) is the standard vector Laplacian relation, valid with the componentwise Laplacian in Cartesian coordinates.
+ **Polynomial example.** $\operatorname{curl}\langle x^2y,yz,x+z^2\rangle=\langle-y,-1,-x^2\rangle;$ at $(1,2,3)$ this is $\langle-2,-1,-1\rangle$ with magnitude $\sqrt6.$
+ **Planar example.** $\operatorname{curl}\langle x^2+y,xy\rangle=(y-1)\mathbf{k};$ at $(2,3)$ the value is $2.$

## Independent checks

Python 3 finite-difference script (ad hoc, outside the repository, step $10^{-6}$):

+ spherical formula (17) applied to $\mathbf{F}=\langle z^2,x^2,y^2\rangle$ at $(\rho,\theta,\varphi)=(1.7,0.8,1.1)$: formula components $(3.2932001884,-0.6926689517,-0.4848115542)$ against the Cartesian curl transformed to the spherical basis $(3.2932001883,-0.6926689517,-0.4848115539);$
+ cylindrical formula (16) applied to $\mathbf{F}=\langle-y,x,0\rangle$ at $(r,\theta,z)=(1.3,0.7,0.4)$: $(0,0,1.9999999998),$ agreeing with $2\omega=2;$
+ Stokes example: $\int_0^{2\pi}\cos^2t\,dt=\pi.$

All checks passed. The component formulas and the Stokes example are exact; the coordinate checks are numerical.

## Limitations

+ No LaTeX renderer, Pandoc or TeX installation is available (`pandoc` and `pdflatex` not found); the Markdown was checked structurally but not rendered.
+ The proposed route `https://algebrica.org/curl/` is not known to be live.
+ Stokes' theorem is proved only for graph patches and sketched for general surfaces; the article states the scope.
+ The differential-form formulation and the general de Rham theory are outside scope.
+ Open issues and pull requests in the upstream repository were not inspected.
+ Links to sibling batch articles are unpublished dependencies until this batch is merged.
