# Research evidence — Surface Integrals

Batch: `20261127T144139Z-01`
Slug: `surface-integrals`
Article: `multivariable-calculus/surface-integrals.md`
Category: `multivariable-calculus` (provisional)
Research date: 2026-11-27

## Coverage check

Upstream `antoniolupetti/algebrica` was searched by filename and body text for "surface integral", "surface area", "flux integral" and "parametric surface". No upstream article covers scalar or vector surface integrals.

The staging repository has `multivariable-calculus/parametric-surfaces.md`, written in this batch, which supplies the area element and orientation, and `multivariable-calculus/double-integrals.md`, which supplies the flat-domain background. This article is the integration theory over those surfaces, with scalar and vector forms, worked computations and applications.

Conclusion: not a duplicate. Upstream issues and pull requests were not inspected.

## Scope and reader contract

After reading the article, the reader can:

+ define the scalar surface integral as a limit of Riemann sums over surface patches;
+ evaluate it with a parameterization and with a graph formula;
+ derive the implicit-surface area element $\lVert\nabla F\rVert/|F_z|\,dx\,dy$;
+ compute scalar integrals over a hemisphere, sphere and conical shell;
+ compute mass, centre of mass and average value over a shell;
+ define the vector surface integral, its orientation and its flux interpretation;
+ evaluate a flux through a hemisphere both parametrically and as a graph;
+ split a piecewise surface and orient each patch;
+ explain the difference between $dS$ and $dx\,dy,$ and between scalar and vector integrals.

Assumed prerequisites: [parametric surfaces](../parametric-surfaces/), [double integrals](../double-integrals/), partial derivatives, polar coordinates and the cross product.

Exclusions: the divergence theorem (mentioned only as the next result), Stokes' theorem, differential forms, and the general theory of integration on manifolds.

## Sources consulted

1. OpenStax, *Calculus Volume 3*, §6.6 "Surface Integrals".
   URL: https://openstax.org/books/calculus-volume-3/pages/6-6-surface-integrals
   Accessed: 2026-11-27. Full text read.
   Supports: the definition of the scalar surface integral by Riemann sums; the surface area definition; the parametric evaluation formula; the definition of an oriented surface; the vector surface integral and its identification as flux; the mass interpretation; the sphere, cylinder and cone examples.
   Use: definitions, theorem statements and orientation conventions.

2. Paul Dawkins, *Paul's Online Math Notes*, Calculus III, "Surface Integrals".
   URL: https://tutorial.math.lamar.edu/Classes/CalcIII/SurfaceIntegrals.aspx
   Accessed: 2026-11-27. Full text read.
   Supports: the graph formula, the parametric formula, the hemisphere example $\iint z\,dS=8\pi$ for radius $2,$ the cylinder example and the piecewise-surface technique.
   Use: independent confirmation of the formulas and the worked hemisphere value.

3. Paul Dawkins, *Paul's Online Math Notes*, Calculus III, "Surface Integrals of Vector Fields".
   URL: https://tutorial.math.lamar.edu/Classes/CalcIII/SurfIntVectorField.aspx
   Accessed: 2026-11-27. Full text read.
   Supports: oriented surfaces, the positive orientation of a closed surface, the unit normal for graphs and parameterizations, and the formula $\iint\mathbf{F}\cdot d\mathbf{S}=\iint\mathbf{F}\cdot(\mathbf{r}_u\times\mathbf{r}_v)\,du\,dv.$
   Use: vector form, orientation and the sign convention.

4. Algebrica upstream `integrals/` for notation and the staging `multivariable-calculus/double-integrals.md` for house conventions.
   Accessed through the upstream clone and the staging repository, 2026-11-27.
   Supports: integral notation, region descriptions and polar coordinates.
   Use: notational consistency only.

## Definitions and conventions selected

+ Scalar surface integral: limit of $\sum f(P_{ij})\Delta S_{ij}$ over partitions of $S.$
+ $dS=\lVert\mathbf{r}_u\times\mathbf{r}_v\rVert\,du\,dv$ for a regular parameterization.
+ Graph: $dS=\sqrt{1+g_x^2+g_y^2}\,dx\,dy.$
+ Implicit: $dS=\lVert\nabla F\rVert/|F_z|\,dx\,dy$ when $F_z\neq0.$
+ Vector: $d\mathbf{S}=\mathbf{n}\,dS$; for parameterizations $d\mathbf{S}=(\mathbf{r}_u\times\mathbf{r}_v)\,du\,dv.$
+ Closed surfaces are oriented outward.
+ The upper hemisphere uses $\varphi\in[0,\pi/2]$ and $z=R\cos\varphi.$

## Proofs and scope

+ The scalar integral is defined by Riemann sums; the evaluation formula is stated as the parameterization theorem and derived geometrically through the area element, not proved from first principles for arbitrary continuous maps.
+ The graph and implicit formulas are derived from the area element and the angle between the normal and the $z$-axis.
+ The hemisphere scalar integral, the sphere $x^2$ integral, the cone mass and the hemisphere flux are computed in full.
+ The vector formula is derived from $\mathbf{n}\,dS=(\mathbf{r}_u\times\mathbf{r}_v)\,du\,dv$ and the orientation convention.
+ The equality of the parametric and graph flux computations is checked explicitly.

## Independent example checks

All computations were repeated by hand and checked symbolically in Python.

+ (13)–(15) $\iint z\,dS$ over the upper hemisphere of radius $2$: inner integral $4,$ total $8\pi.$
+ (16) area: $8\pi=2\pi R^2$ with $R=2.$
+ (17)–(18) $\iint x^2\,dS$ over the unit sphere: $\pi\cdot4/3=4\pi/3;$ the three coordinate squares sum to $4\pi.$
+ (20) cone mass with $\rho=z$: $2\pi\sqrt2R^3/3.$
+ Hemisphere centroid: $\iint z\,dS=\pi R^3,$ area $2\pi R^2,$ quotient $R/2.$
+ (28)–(29) flux of $\langle0,0,z\rangle$ through the upper hemisphere: $2\pi R^3/3.$
+ (30) graph computation: $2\pi\int_0^R r\sqrt{R^2-r^2}\,dr=2\pi R^3/3.$

## Checks performed and limitations

+ UTF-8/LF encoding, front matter, H2-only headings, `+` bullets and `- - -` separators were checked against the staging corpus.
+ Internal links point to files present in the staging repository at the commit, not to live site routes.
+ LaTeX was not rendered; no TeX renderer is installed. Delimiters and equation tags were inspected manually.
+ No upstream prose or figures were copied.
+ Upstream issues and pull requests were not inspected.
