# Research evidence — Parametric Surfaces

Batch: `20261127T144139Z-01`
Slug: `parametric-surfaces`
Article: `multivariable-calculus/parametric-surfaces.md`
Category: `multivariable-calculus` (provisional)
Research date: 2026-11-27

## Coverage check

Upstream `antoniolupetti/algebrica` was searched by filename and body text for "parametric surface", "surface area", "parameterization" and "surface integral". No upstream article covers parametric surfaces or surface area in three dimensions.

The staging repository has `multivariable-calculus/vector-valued-functions.md`, which treats parameterized curves and curvature, and `multivariable-calculus/cylindrical-coordinates.md` and `spherical-coordinates.md`, which give coordinate transformations but not a general surface parameterization. This article supplies the missing two-parameter theory.

Conclusion: not a duplicate. Upstream issues and pull requests were not inspected.

## Scope and reader contract

After reading the article, the reader can:

+ define a parametric surface and its parameter domain;
+ describe coordinate curves and the parameter grid;
+ define regularity through $\mathbf{r}_u\times\mathbf{r}_v\neq\mathbf{0}$;
+ distinguish a coordinate singularity from a geometric singularity;
+ write the tangent plane and unit normal at a regular point;
+ derive the area element $\lVert\mathbf{r}_u\times\mathbf{r}_v\rVert\,du\,dv$ from the linearized parallelogram;
+ compute the area of a sphere, cone and torus from their standard parameterizations;
+ explain why surface area is invariant under reparameterization;
+ choose an orientation and explain why the Möbius band has none;
+ pass between graph, implicit and parametric descriptions.

Assumed prerequisites: [vector-valued functions](../vector-valued-functions/), partial derivatives, the cross product and double integrals.

Exclusions: the full implicit function theorem, the classification of surfaces, Gauss–Bonnet, and the convergence proof of the area integral for arbitrary continuous parameterizations.

## Sources consulted

1. OpenStax, *Calculus Volume 3*, §6.6 "Surface Integrals", subsections on parametric surfaces and surface area.
   URL: https://openstax.org/books/calculus-volume-3/pages/6-6-surface-integrals
   Accessed: 2026-11-27. Full text read.
   Supports: the definition of a parametric surface, smooth and regular parameterizations, the surface area definition, the cone and sphere area computations, surfaces of revolution, and the orientation of a surface.
   Use: definitions, theorem scope and the standard examples.

2. Paul Dawkins, *Paul's Online Math Notes*, Calculus III, "Parametric Surfaces".
   URL: https://tutorial.math.lamar.edu/Classes/CalcIII/ParametricSurfaces.aspx
   Accessed: 2026-11-27. Full text read.
   Supports: the tangent vectors $\mathbf{r}_u,\mathbf{r}_v,$ the normal $\mathbf{r}_u\times\mathbf{r}_v,$ the surface area formula, and worked parameterizations of planes, cylinders, spheres and surfaces of revolution.
   Use: independent confirmation of the area formula and the tangent-plane construction.

3. OpenStax, *Calculus Volume 3*, §6.6, "Surface Area of a Parametric Surface" and "Surface Integrals of Vector Fields".
   URL: https://openstax.org/books/calculus-volume-3/pages/6-6-surface-integrals
   Accessed: 2026-11-27.
   Supports: the orientation convention for closed surfaces and the distinction between orientable and nonorientable surfaces.
   Use: orientation section.

4. Algebrica upstream `functions/` and `vectors-and-matrices/` material for notation.
   Accessed through the upstream clone, 2026-11-27.
   Supports: vector notation and function notation.
   Use: house notation only.

## Definitions and conventions selected

+ $\mathbf{r}:D\subset\mathbb{R}^2\to\mathbb{R}^3$ is a parametric surface; $D$ is the parameter domain.
+ Regular: $\mathbf{r}_u,\mathbf{r}_v$ continuous and $\mathbf{r}_u\times\mathbf{r}_v\neq\mathbf{0}.$
+ Smooth: regular at every interior point of $D.$
+ $dS=\lVert\mathbf{r}_u\times\mathbf{r}_v\rVert\,du\,dv.$
+ The standard sphere uses $\varphi$ measured from the positive $z$-axis, $0\le\varphi\le\pi.$
+ The outward normal of a closed surface is the positive orientation.
+ The torus uses $0<b<a.$

## Proofs and scope

+ The area element is derived by linearization and a Riemann-sum argument. The article presents this as the geometric basis and does not claim a full convergence proof for arbitrary continuous maps.
+ Invariance under reparameterization is stated via the change-of-variables Jacobian; the determinant's absolute value is identified explicitly.
+ The sphere, cone and torus areas are computed in full from the parameterizations.
+ The tangent plane example is computed from the cross product and checked by substitution.
+ The Möbius band is described qualitatively; no formal proof of nonorientability is attempted.

## Independent example checks

All cross products and integrals were recomputed by hand and checked symbolically in Python.

+ Sphere: $\mathbf{r}_\theta\times\mathbf{r}_\varphi=-R^2\sin\varphi\,\hat{\mathbf{r}};$ norm $R^2\sin\varphi;$ area $4\pi R^2.$
+ Cone: $\mathbf{r}_r\times\mathbf{r}_\theta=\langle-r\cos\theta,-r\sin\theta,r\rangle;$ norm $\sqrt2\,r;$ area $\sqrt2\pi R^2=\pi R\ell$ with $\ell=\sqrt2R.$
+ Torus: norm $b(a+b\cos\varphi);$ area $4\pi^2ab.$
+ Paraboloid tangent plane at $(1,1,2)$: normal $\langle-2,-2,1\rangle,$ equation $z=2x+2y-2;$ the point satisfies it.
+ Cylinder: norm $R;$ lateral area $2\pi Rh.$
+ Graph: $\mathbf{r}_x\times\mathbf{r}_y=\langle-g_x,-g_y,1\rangle;$ norm $\sqrt{1+g_x^2+g_y^2}.$

## Checks performed and limitations

+ UTF-8/LF encoding, front matter, H2-only headings, `+` bullets, `- - -` separators and a three-column table were checked against the staging corpus.
+ Internal links point to files present in the staging repository at the commit, not to live site routes.
+ LaTeX was not rendered; no TeX renderer is installed. Delimiters, equation tags and the table were inspected manually.
+ No upstream prose or figures were copied.
+ Upstream issues and pull requests were not inspected.
