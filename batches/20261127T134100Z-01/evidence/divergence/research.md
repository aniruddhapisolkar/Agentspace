# Research evidence — Divergence

Batch: `20261127T134100Z-01`
Slug: `divergence`
Article: `multivariable-calculus/divergence.md`
Category: `multivariable-calculus` (provisional)
Research date: 2026-11-27

## Coverage check

Upstream `antoniolupetti/algebrica` was searched by filename and body text for "divergence", "divergence theorem", "flux", "incompressible", "solenoidal" and "source-free".

+ No dedicated upstream article on divergence or the divergence theorem was found.
+ `derivatives/partial-derivatives.md` introduces partial derivatives but not the divergence.
+ `integrals/definite-integrals.md` and the multiple-integral entries treat scalar integration, not flux.
+ No upstream article uses the divergence theorem or the inverse-square singularity.

Conclusion: not a duplicate. Open issues and pull requests were not inspected; no claim is made about planned upstream work.

## Scope and reader contract

After reading the article, the reader can:

+ define the divergence in Cartesian coordinates and as the trace of the Jacobian;
+ derive the coordinate formula from the flux through an infinitesimal box;
+ read the sign of the divergence as a source, sink or volume-preserving flow;
+ compute divergence for polynomial, rotational, shear, radial and inverse-square fields;
+ state the divergence theorem with its hypotheses and orientation;
+ evaluate flux through a sphere and a cube both directly and by the theorem;
+ use the product rules and the identity $\operatorname{div}\operatorname{curl}\mathbf{F}=0$;
+ write the divergence in cylindrical and spherical coordinates;
+ explain why the inverse-square field has zero divergence away from the origin but nonzero flux through a sphere around it.

Assumed prerequisites: [vector fields](../vector-fields/), [partial derivatives](../partial-derivatives/), [double integrals](../double-integrals/), [triple integrals](../triple-integrals/) and the idea of a surface integral. Exclusions: a full proof of the divergence theorem for arbitrary piecewise smooth regions, distributional divergence, the heat equation and electrostatics beyond the inverse-square example.

## Sources consulted

1. OpenStax, *Calculus Volume 3*, §6.5 "Divergence and Curl" and §6.8 "The Divergence Theorem".
   URLs: https://openstax.org/books/calculus-volume-3/pages/6-5-divergence-and-curl and https://openstax.org/books/calculus-volume-3/pages/6-8-the-divergence-theorem
   Accessed: 2026-11-27. Full text read.
   Supports: the definition $\operatorname{div}\mathbf{F}=P_x+Q_y+R_z,$ the source/sink interpretation, the source-free field theorems, the statement of the divergence theorem (Theorem 6.20) with outward orientation, and worked flux examples.
   Use: the definition, the interpretation, the theorem statement and the exercise structure.

2. Paul Dawkins, *Paul's Online Math Notes*, Calculus III, "Curl and Divergence".
   URL: https://tutorial.math.lamar.edu/Classes/CalcIII/CurlDivergence.aspx
   Accessed: 2026-11-27. Full text read.
   Supports: the divergence formula and notation, the dot-product mnemonic, the product rules, and the vector forms of Green's theorem in terms of divergence.
   Use: independent confirmation of the formula, sign conventions and product rules.

3. Paul Dawkins, *Paul's Online Math Notes*, Differential Equations, "The Heat Equation".
   URL: https://tutorial.math.lamar.edu/Classes/DE/TheHeatEquation.aspx
   Accessed: 2026-11-27. Section read for the Laplacian definition.
   Supports: the definition of the Laplacian and its appearance in the heat equation.
   Use: cross-check for the relation $\Delta f=\operatorname{div}(\nabla f),$ developed in the Laplacian entry.

## Definitions and conventions selected

+ Open domain $D\subseteq\mathbb{R}^3$; $\mathbf{F}=\langle P,Q,R\rangle$ of class $C^1.$
+ $\operatorname{div}\mathbf{F}=P_x+Q_y+R_z=\nabla\cdot\mathbf{F}.$
+ Planar divergence $P_x+Q_y.$
+ Outward unit normal $\mathbf{n}$ and flux $\iint_S\mathbf{F}\cdot\mathbf{n}\,dS.$
+ Cylindrical coordinates $(r,\theta,z)$ and spherical coordinates $(\rho,\theta,\varphi)$ with $\varphi$ the polar angle, matching the batch convention.
+ British spelling: "centre", "recognise", "nonnegative"; "volume-preserving" hyphenated.

## Mathematical claims and justification

+ **Coordinate formula (1).** Definition; the trace identity (3) follows from the matrix of first partial derivatives.
+ **Box derivation (4)–(5).** For each pair of opposite faces, the difference of the normal components is approximately the corresponding partial derivative times the side length; divide by the volume. The mean value theorem makes the approximation exact at an intermediate point, and continuity of the partial derivatives gives the limit. This is a derivation of the coordinate formula from flux, not a proof of the divergence theorem.
+ **Source/sink sign.** Positive divergence means net outward flux from small surfaces; negative means net inward flux. Stated as an interpretation, with the limit (5) as the precise content.
+ **Examples.** $\operatorname{div}\langle x,y,z\rangle=3;$ $\operatorname{div}\langle-y,x,0\rangle=0;$ $\operatorname{div}\langle x^2,y^2,z^2\rangle=2(x+y+z);$ $\operatorname{div}\langle y,0,0\rangle=0.$ All are direct partial differentiation.
+ **Inverse-square field (6).** $\partial_x(x/r^3)=1/r^3-3x^2/r^5;$ summing gives $3/r^3-3r^2/r^5=0.$ The field is undefined at the origin, so the divergence theorem cannot be applied to a ball containing the origin. The flux through a sphere is $4\pi,$ independent of radius. The article states this as the reason the zero divergence does not contradict the theorem.
+ **Divergence theorem (7).** Statement with $S$ piecewise smooth, closed, outward oriented, and $\mathbf{F}$ $C^1$ on an open set containing $E.$ The proof sketch for a box uses the fundamental theorem of calculus along lines parallel to each axis; the general case partitions into boxes and cancels interior faces. The sketch is labelled as such, not presented as a complete proof for arbitrary regions.
+ **Sphere flux.** $\mathbf{F}=\mathbf{r},$ $\mathbf{n}=\mathbf{r}/R,$ $\mathbf{F}\cdot\mathbf{n}=R,$ flux $4\pi R^3;$ volume integral $3\cdot4\pi R^3/3=4\pi R^3.$
+ **Unit radial flux.** $\mathbf{F}=\mathbf{r}/r,$ $\operatorname{div}\mathbf{F}=2/r,$ flux $4\pi R^2;$ volume integral $8\pi\int_0^Rr\,dr=4\pi R^2.$ The integrand is integrable at the origin in three dimensions, so the volume integral converges even though the divergence is unbounded.
+ **Cube fluxes.** For $\langle0,0,z\rangle,$ only the top face contributes, giving $1,$ equal to the volume integral of $1.$ For $\langle x^2,y^2,z^2\rangle,$ each of the three faces at coordinate $1$ contributes $1,$ total $3,$ equal to $2(1/2+1/2+1/2).$
+ **Product rules (8)–(9).** Componentwise product rule and collection. The cross-product rule was checked against a concrete field: $\mathbf{F}=\langle0,0,x\rangle,$ $\mathbf{G}=\langle0,y,0\rangle$ gives $\operatorname{div}(\mathbf{F}\times\mathbf{G})=-y$ and $\mathbf{G}\cdot\operatorname{curl}\mathbf{F}-\mathbf{F}\cdot\operatorname{curl}\mathbf{G}=-y.$
+ **Identity (10).** $\operatorname{div}\operatorname{curl}\mathbf{F}=0$ by equality of mixed partials for a $C^2$ field.
+ **Cylindrical formula (11).** Standard formula; the radial term is $(1/r)\partial_r(rF_r),$ not $\partial_rF_r.$
+ **Spherical formula (12).** Standard formula in the $(\rho,\theta,\varphi)$ convention; the polar-angle term carries $\sin\varphi$ and the azimuthal term carries $1/(\rho\sin\varphi).$
+ **Planar Green flux form (13).** For positively oriented $C,$ the outward normal is the right normal, and $\mathbf{F}\cdot\mathbf{n}\,ds=P\,dy-Q\,dx;$ Green's theorem then gives the divergence integral. The orientation convention is stated.
+ **Two divergence-free planar fields.** $\langle y,-x\rangle$ circulates; $\langle x,-y\rangle$ is a saddle with expansion along $x$ and contraction along $y.$ Both have zero divergence by direct differentiation.

## Independent checks

Python 3 finite-difference script (ad hoc, outside the repository, step $10^{-6}$):

+ inverse-square divergence at $(1,2,3)$ and $(0.3,-0.7,1.1)$: $0.0$ and $-2.8\times10^{-11};$
+ unit radial field at $(1,2,3)$: computed $0.534522483858213$ against $2/\sqrt{14}=0.534522483824849;$
+ $\operatorname{div}\operatorname{curl}\mathbf{F}$ for $\mathbf{F}=\langle zx,yz,xy\rangle$ at $(0.4,1.2,-0.7)$: $0.0,$ with $\operatorname{curl}\mathbf{F}\approx\langle-0.8,-0.8,0\rangle;$
+ cube divergence integral for $\langle x^2,y^2,z^2\rangle$: $3.0.$

All checks passed. The sphere and cube flux identities are exact computations, not numerical approximations.

## Limitations

+ No LaTeX renderer, Pandoc or TeX installation is available (`pandoc` and `pdflatex` not found); the Markdown was checked structurally but not rendered.
+ The proposed route `https://algebrica.org/divergence/` is not known to be live.
+ The divergence theorem is proved only for boxes and sketched for general regions; the article says so explicitly.
+ Distributional divergence and the delta-function interpretation of the inverse-square singularity are mentioned only qualitatively, not developed.
+ Open issues and pull requests in the upstream repository were not inspected.
+ Links to sibling batch articles are unpublished dependencies until this batch is merged.
