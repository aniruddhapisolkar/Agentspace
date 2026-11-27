# Research evidence — Flux Integrals

Batch: `20261127T144139Z-01`
Slug: `flux-integrals`
Article: `multivariable-calculus/flux-integrals.md`
Category: `multivariable-calculus` (provisional)
Research date: 2026-11-27

## Coverage check

Upstream `antoniolupetti/algebrica` was searched by filename and body text for "flux", "flux integral", "divergence theorem" and "surface integral". No upstream article covers flux integrals or the divergence theorem.

The staging repository now has `multivariable-calculus/surface-integrals.md`, which defines the vector surface integral and one flux example, and `multivariable-calculus/divergence.md`, which introduces the divergence theorem. This article is the dedicated flux treatment: physical derivation, graph formula, sign conventions, closed surfaces, the divergence theorem as a flux identity, the inverse-square field, and the open-surface dependence.

Conclusion: not a duplicate. Upstream issues and pull requests were not inspected.

## Scope and reader contract

After reading the article, the reader can:

+ derive the flux of a velocity field from the slanted-cylinder picture;
+ define the flux integral and evaluate it with a parameterization and with a graph;
+ compute fluxes through a disk, sphere, cube, cylinder and paraboloid;
+ explain why the flux of a constant vertical field through a graph depends only on the projected area;
+ distinguish the flux of $\langle x,y,z\rangle,$ which grows with $R^3,$ from the flux of $\mathbf{r}/r^3,$ which is $4\pi$ for every enclosing sphere;
+ state the divergence theorem with its hypotheses and use it to check a flux computation;
+ explain divergence as flux per unit volume and the solenoidal case;
+ explain why flux through an open surface depends on the surface unless the field is divergence-free;
+ identify the orientation, singularity and closed-surface pitfalls.

Assumed prerequisites: [surface integrals](../surface-integrals/), [parametric surfaces](../parametric-surfaces/), [divergence](../divergence/), triple integrals and polar coordinates.

Exclusions: a full proof of the divergence theorem, Gauss's law in physical units, the general Stokes theorem, and electromagnetic applications beyond the flux interpretation.

## Sources consulted

1. OpenStax, *Calculus Volume 3*, §6.6 "Surface Integrals", subsection "Surface Integrals of Vector Fields".
   URL: https://openstax.org/books/calculus-volume-3/pages/6-6-surface-integrals
   Accessed: 2026-11-27. Full text read.
   Supports: the definition of an oriented surface, the positive orientation of a closed surface, the vector surface integral, its identification as flux, the mass-flow and heat-flow interpretations, the sphere examples and the orientation conventions.
   Use: definitions, physical interpretation and the sign convention.

2. OpenStax, *Calculus Volume 3*, §6.8 "The Divergence Theorem".
   URL: https://openstax.org/books/calculus-volume-3/pages/6-8-the-divergence-theorem
   Accessed: 2026-11-27. Full text read.
   Supports: the statement of the divergence theorem with the outward normal, its use to compute flux, the divergence as flux density, and the inverse-square example with the singularity at the origin.
   Use: theorem statement, hypotheses and the source interpretation.

3. Paul Dawkins, *Paul's Online Math Notes*, Calculus III, "Surface Integrals of Vector Fields".
   URL: https://tutorial.math.lamar.edu/Classes/CalcIII/SurfIntVectorField.aspx
   Accessed: 2026-11-27. Full text read.
   Supports: the oriented-surface definitions, the unit normal for graphs and parameterizations, the flux formula, and the worked closed-surface example with a paraboloid and its cap.
   Use: independent confirmation of the formulas and the outward-orientation convention.

4. Paul Dawkins, *Paul's Online Math Notes*, Calculus III, "Divergence Theorem".
   URL: https://tutorial.math.lamar.edu/Classes/CalcIII/DivergenceTheorem.aspx
   Accessed: 2026-11-27. Full text read.
   Supports: the divergence theorem statement, the flux-density interpretation and examples with cubes and cylinders.
   Use: independent confirmation.

## Definitions and conventions selected

+ Flux $=\iint_S\mathbf{F}\cdot\mathbf{n}\,dS$ with $\mathbf{n}$ a unit normal.
+ The orientation of a parameterized surface is the one induced by $\mathbf{r}_u\times\mathbf{r}_v.$
+ Closed surfaces are oriented outward.
+ For a graph $z=g(x,y),$ the upward area vector is $\langle-g_x,-g_y,1\rangle\,dx\,dy.$
+ The divergence theorem is stated for a compact solid with piecewise smooth boundary and a $C^1$ field on an open set containing it.
+ The inverse-square field is $\mathbf{r}/r^3,$ with flux $4\pi$ through every sphere centred at the origin.

## Proofs and scope

+ The flux formula is derived from the slanted-cylinder volume and then from the parameterization; this is a derivation of the integral formula, not a convergence proof.
+ The divergence theorem is stated and used; no proof is attempted. The article explicitly says the theorem is quoted.
+ The inverse-square flux is computed directly for a sphere and then compared with the divergence theorem, with the singularity excluded.
+ The paraboloid flux is computed twice: once from the parameterization and once from the divergence theorem applied to the solid between the paraboloid and its cap. The two agree.
+ The cube and cylinder fluxes are computed face by face and checked against three times the volume.

## Independent example checks

All computations were repeated by hand and checked symbolically in Python.

+ Disk: $\iint c\,dS=c\pi R^2.$
+ Sphere of radius $R$: $\mathbf{F}\cdot\mathbf{n}=R$ and flux $4\pi R^3.$
+ Inverse-square: $\mathbf{F}\cdot\mathbf{n}=1/R^2$ and flux $4\pi$ for every $R.$
+ Cube: three contributing faces of area $1$ with normal component $1;$ total $3.$
+ Cylinder: side $2\pi R^2h,$ top $\pi R^2h,$ bottom $0;$ total $3\pi R^2h.$
+ Paraboloid: $\mathbf{r}_r\times\mathbf{r}_\theta=\langle-2r^2\cos\theta,-2r^2\sin\theta,r\rangle;$ $\mathbf{F}\cdot(\mathbf{r}_r\times\mathbf{r}_\theta)=-2r^3;$ integral $-\pi.$
+ Enclosed solid: volume $\pi/2,$ divergence $2,$ outward flux $\pi;$ the outward normal on the paraboloid is the negative of the upward normal, so the paraboloid's outward flux is $\pi,$ and the cap contributes $0.$

## Checks performed and limitations

+ UTF-8/LF encoding, front matter, H2-only headings, `+` bullets and `- - -` separators were checked against the staging corpus.
+ Internal links point to files present in the staging repository at the commit, not to live site routes.
+ LaTeX was not rendered; no TeX renderer is installed. Delimiters and equation tags were inspected manually.
+ No upstream prose or figures were copied.
+ Upstream issues and pull requests were not inspected.
