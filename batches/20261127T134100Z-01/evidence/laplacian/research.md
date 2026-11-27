# Research evidence — Laplacian

Batch: `20261127T134100Z-01`
Slug: `laplacian`
Article: `multivariable-calculus/laplacian.md`
Category: `multivariable-calculus` (provisional)
Research date: 2026-11-27

## Coverage check

Upstream `antoniolupetti/algebrica` was searched by filename and body text for "Laplacian", "Laplace equation", "harmonic function", "mean value property" and "Green's identities".

+ No dedicated upstream article on the Laplacian, Laplace's equation or harmonic functions was found.
+ `derivatives/partial-derivatives.md` defines second partial derivatives and the Hessian, but does not compose divergence with gradient or treat harmonic functions.
+ The multiple-integral entries supply the integral theorems used in Green's identities but not the identities themselves.
+ No upstream article treats the coordinate expressions or the fundamental solutions.

Conclusion: not a duplicate. Open issues and pull requests were not inspected; no claim is made about planned upstream work.

## Scope and reader contract

After reading the article, the reader can:

+ define the Laplacian as the divergence of the gradient and as the trace of the Hessian;
+ interpret it as the second-order deviation of a function from its spherical average;
+ identify harmonic, subharmonic and superharmonic functions;
+ verify harmonicity of polynomial, exponential and radial examples;
+ state the mean value property and the maximum principle;
+ derive and use the first and second Green identities;
+ write the Laplacian in cylindrical and spherical coordinates;
+ solve a radial Dirichlet problem on an annulus;
+ state the vector Laplacian identity and explain why componentwise application fails in curvilinear coordinates.

Assumed prerequisites: [partial derivatives](../partial-derivatives/), [vector fields](../vector-fields/), [divergence](../divergence/), [triple integrals](../triple-integrals/) and the divergence theorem. Exclusions: existence and regularity theory for Laplace's equation, Green's functions for general domains, spectral theory, Sobolev spaces, and the full proof of the maximum principle.

## Sources consulted

1. OpenStax, *Calculus Volume 3*, §6.5 "Divergence and Curl".
   URL: https://openstax.org/books/calculus-volume-3/pages/6-5-divergence-and-curl
   Accessed: 2026-11-27. Full text read.
   Supports: the Laplace operator as $\nabla^2f=\operatorname{div}(\nabla f),$ the component formula $f_{xx}+f_{yy}+f_{zz},$ Laplace's equation for harmonic functions, and the electrostatic interpretation.
   Use: the definition, notation and harmonic-function terminology.

2. Wikipedia, "Laplace operator".
   URL: https://en.wikipedia.org/wiki/Laplace_operator
   Accessed: 2026-11-27. Full text read.
   Supports: the divergence-of-gradient definition, the informal spherical-average interpretation, the cylindrical and spherical coordinate formulas, the mean value property, the maximum principle for harmonic functions, and the distributional fundamental solutions in two and three dimensions.
   Use: the average interpretation, the coordinate formulas, and the statements of the mean value and maximum principles. Treated as an encyclopedic cross-check, not as the sole source for any proof.

3. Paul Dawkins, *Paul's Online Math Notes*, Differential Equations, "The Heat Equation".
   URL: https://tutorial.math.lamar.edu/Classes/DE/TheHeatEquation.aspx
   Accessed: 2026-11-27. Section read.
   Supports: the definition of the Laplacian and its role in the heat equation.
   Use: independent confirmation of the operator and the diffusion interpretation.

## Definitions and conventions selected

+ $\Delta f=\operatorname{div}(\nabla f)=\sum_i f_{x_ix_i}$ with the positive sign convention.
+ Harmonic: $\Delta f=0$; subharmonic: $\Delta f>0$; superharmonic: $\Delta f<0.$
+ Mean value over the sphere $S_r(P)$ with surface measure.
+ Green identities with outward normal $\mathbf{n}$ and normal derivative $\partial f/\partial n=\nabla f\cdot\mathbf{n}.$
+ Vector Laplacian $\Delta\mathbf{F}=\nabla(\operatorname{div}\mathbf{F})-\operatorname{curl}(\operatorname{curl}\mathbf{F}).$
+ British spelling: "centre", "recognise", "neighbourhood"; "nonnegative" without hyphen.

## Mathematical claims and justification

+ **Definition (1)–(3).** Divergence of the gradient; in Cartesian coordinates the mixed terms cancel because the gradient has no cross components, leaving the pure second derivatives.
+ **Linearity (4).** Linearity of partial derivatives.
+ **Trace identity (5).** The Hessian is symmetric for a $C^2$ function (equality of mixed partials); its trace is the sum of the pure second derivatives and is invariant under orthogonal changes of coordinates.
+ **Mean value expansion (7)–(8).** Taylor expansion to second order and averaging over the unit sphere. If $u$ is uniform on the unit sphere, $\mathbb{E}[u_iu_j]=\delta_{ij}/n,$ so the average of the quadratic term is $r^2\Delta f/(2n).$ In three dimensions this is $r^2\Delta f/6.$ The limit (8) follows.
+ **Maximum principle.** At an interior maximum of a $C^2$ function, the Hessian is negative semidefinite, so its trace is at most zero. Hence a function with positive Laplacian cannot have an interior maximum. The minimum statement is analogous.
+ **Harmonic examples.** Direct second derivatives: $x^2-y^2$ gives $2-2=0;$ $e^x\cos y$ gives $e^x\cos y-e^x\cos y=0;$ $xyz$ gives $0;$ $x^2+y^2+z^2$ gives $6.$
+ **Radial fundamental solutions (11)–(12).** For $f(r),$ the radial Laplacian is $(1/r^2)(r^2f')'$ in three dimensions and $(1/r)(rf')'$ in two. Substituting $1/r$ and $\ln r$ gives zero. The constants in the distributional formulas are fixed by the flux through a small sphere or circle: $\Delta(-1/(4\pi r))=\delta_0$ and $\Delta((1/2\pi)\ln r)=\delta_0.$
+ **Mean value property (13).** Standard theorem for harmonic functions; stated, not proved. It is consistent with (7): if $\Delta f=0,$ the first nonconstant term in the spherical average vanishes.
+ **Green identities (14)–(16).** Apply the divergence theorem to $f\nabla g$ and use $\operatorname{div}(f\nabla g)=f\Delta g+\nabla f\cdot\nabla g.$ The second identity follows by antisymmetrization. The uniqueness argument uses $\lVert\nabla f\rVert^2\ge0.$
+ **Cylindrical formula (17).** Divergence of the gradient in cylindrical coordinates; the radial term is $(1/r)\partial_r(rf_r),$ not $f_{rr}$ alone.
+ **Spherical formula (18).** Divergence of the gradient in the $(\rho,\theta,\varphi)$ convention; the polar term carries $\sin\varphi$ and the azimuthal term carries $1/\sin^2\varphi.$
+ **Radial ODEs (19)–(21).** Setting the angular terms to zero. In three dimensions $\rho^2f'=A$ gives $f=B+C/\rho;$ in two dimensions $rf'=A$ gives $f=A\ln r+B.$
+ **Annulus solution (22).** $B+C=1$ and $B+C/2=0$ give $C=2,$ $B=-1.$ Check at both radii and $\Delta f=0$ by (20). Uniqueness follows from the maximum principle applied to the difference of two solutions.
+ **Vector Laplacian (23)–(24).** In Cartesian coordinates, applying the scalar Laplacian componentwise agrees with the vector identity. In curvilinear coordinates the basis vectors vary, so the componentwise scalar Laplacian is not the vector Laplacian; the identity (24) must be used.

## Independent checks

Python 3 finite-difference script (ad hoc, outside the repository, step $10^{-5}$):

+ $\Delta(x^2-y^2)=-1.1\times10^{-6},$ $\Delta(xyz)=-1.1\times10^{-6},$ $\Delta(e^x\cos y)=-1.1\times10^{-6}$ at $(0.7,1.1,0.9),$ all zero to numerical precision;
+ $\Delta(x^2+y^2+z^2)=6.0000004964$ against $6;$
+ $\Delta(1/r)=-3.3\times10^{-6}$ at the same point, zero to numerical precision;
+ annulus values $f(1)=1,$ $f(1.5)=1/3,$ $f(2)=0;$
+ spherical average of $x^2$ over a sphere of radius $0.2$ is $0.0133333333,$ equal to $r^2/3$ and to the expansion $(r^2/6)\Delta(x^2).$

All checks passed. The annulus and mean value identities are exact.

## Limitations

+ No LaTeX renderer, Pandoc or TeX installation is available (`pandoc` and `pdflatex` not found); the Markdown was checked structurally but not rendered.
+ The proposed route `https://algebrica.org/laplacian/` is not known to be live.
+ The mean value property and the maximum principle are stated with their standard hypotheses, not proved in full; the article says so.
+ The distributional fundamental solutions are mentioned without a development of distribution theory.
+ The vector Laplacian identity is stated for Cartesian components and used to explain the curvilinear caveat; no full derivation in general coordinates is given.
+ Open issues and pull requests in the upstream repository were not inspected.
+ Links to sibling batch articles are unpublished dependencies until this batch is merged.
