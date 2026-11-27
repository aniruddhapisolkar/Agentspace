# Research evidence — Change of Variables in Multiple Integrals

Batch: `20261127T121407Z-01`
Slug: `change-of-variables-in-multiple-integrals`
Article: `multivariable-calculus/change-of-variables-in-multiple-integrals.md`
Category: `multivariable-calculus` (provisional)
Research date: 2026-11-27

## Coverage check

Upstream `antoniolupetti/algebrica` was searched by filename and body text for "change of variables", "Jacobian", "substitution" and "coordinate transformation".

+ `integrals/integration-by-substitution.md` proves the one-dimensional substitution rule. It does not treat several variables.
+ `derivatives/partial-derivatives.md` defines the Jacobian matrix and the chain rule but contains no change-of-variables theorem.
+ `lines-planes-conic-sections/polar-coordinates.md` states the polar area element $dA=\rho\,d\rho\,d\theta$ and the resulting double-integral formula, without deriving the Jacobian or stating the general theorem.
+ No article with "change of variables", "Jacobian determinant" or "coordinate transformation" in its title was found.

Conclusion: not a duplicate. The one-dimensional substitution rule is a prerequisite, and the polar article is a special case. The present entry supplies the general theorem, its hypotheses, its proof strategy and its failure modes. Open issues and pull requests were not inspected; no claim is made about planned upstream work.

## Scope and reader contract

After reading the article, the reader can:

+ state the change-of-variables theorem for a $C^1$ bijection with nonvanishing Jacobian;
+ explain why the absolute value of the determinant is required;
+ explain the local-linearisation argument that produces the Jacobian factor;
+ derive the polar, cylindrical and spherical volume elements from their Jacobian determinants;
+ evaluate the area and a second moment of an ellipse by an affine change of variables;
+ compute an integral over a rotated square using a linear map;
+ explain how non-injectivity, a vanishing Jacobian, a missing absolute value and a lack of $C^1$ regularity can make the formula fail;
+ relate the theorem to the inverse function theorem and to the chain rule for determinants.

Assumed prerequisites: partial derivatives, the Jacobian matrix, the chain rule, determinants, the inverse function theorem (sibling entry), Fubini's theorem (sibling entry), and one-dimensional substitution. Exclusions: the full proof of the change-of-variables theorem (sketched, not completed), the theory of integration on manifolds, and the Lebesgue formulation.

## Sources consulted

1. University of Toronto, MAT237, *Multivariable Calculus*, §4.4 "Change of Variables", "Change of Variables Theorem".
   URL: https://www.math.toronto.edu/courses/mat237y1/20199/notes/Chapter4/S4.4.html
   Accessed: 2026-11-27. Full text read.
   Supports: the theorem with $U,V$ open, $G:U\to V$ a $C^1$ bijection, $\det DG(u)\neq0$ on $U$, $T\subseteq U$ and $S\subseteq V$ compact measurable with $G(T)=S$, and the formula $\int_S f=\int_T f(G(u))|\det DG(u)|\,du$; the polar, cylindrical and spherical Jacobians; the cone example; and the remark that the theorem extends to sets whose boundary is negligible.
   Use: the statement (3)–(5), the hypotheses, the coordinate-system Jacobians, and the structure of the local-linearisation explanation.

2. OpenStax, *Calculus Volume 3*, §5.7 "Change of Variables in Multiple Integrals".
   URL: https://openstax.org/books/calculus-volume-3/pages/5-7-change-of-variables-in-multiple-integrals
   Accessed: 2026-11-27. Full text read.
   Supports: the planar change-of-variables formula, the role of the Jacobian, the polar, cylindrical and spherical transformations, and worked examples of affine and polar changes.
   Use: independent confirmation of the formula and the coordinate Jacobians.

3. Michael Spivak, *Calculus on Manifolds*, Chapter 3 "Integration".
   Publisher: Benjamin, 1965. No stable open-access URL; consulted from the standard text.
   Supports: the change-of-variables theorem for a diffeomorphism, the role of the determinant, and the standard partition-of-unity proof strategy.
   Use: confirmation that the theorem is stated for a $C^1$ diffeomorphism and that the absolute determinant is the volume distortion. The article's proof sketch is independent and explicitly labelled a sketch.

4. Algebrica upstream `integrals/integration-by-substitution.md`, `lines-planes-conic-sections/polar-coordinates.md` and `derivatives/partial-derivatives.md`.
   URLs: https://algebrica.org/integration-by-substitution/, https://algebrica.org/polar-coordinates/, https://algebrica.org/partial-derivatives/
   Accessed through the upstream clone, 2026-11-27.
   Supports: house notation, the one-dimensional substitution formula, the polar area element, and the Jacobian matrix convention.

## Definitions and conventions selected

+ Map: $\Phi:U\to V$, $U,V\subseteq\mathbb{R}^n$ open, $C^1$ bijection, $\det D\Phi(u)\neq0$ on $U$.
+ Jacobian matrix: rows are the components of $\Phi$, columns are the derivatives with respect to the parameters.
+ Jacobian determinant: $\partial(x,y)/\partial(u,v)$ or $\partial(x,y,z)/\partial(u,v,w)$.
+ Formula: $\int_S f(x)\,dx=\int_T f(\Phi(u))|\det D\Phi(u)|\,du$.
+ Polar: $(r,\theta)\mapsto(r\cos\theta,r\sin\theta)$, determinant $r$.
+ Cylindrical: $(r,\theta,z)\mapsto(r\cos\theta,r\sin\theta,z)$, determinant $r$.
+ Spherical: $(\rho,\theta,\varphi)\mapsto(\rho\sin\varphi\cos\theta,\rho\sin\varphi\sin\theta,\rho\cos\varphi)$ with $\varphi$ from the positive $z$-axis.
+ British spelling: "linearisation", "parametrise" where used.

## Mathematical claims and justification

+ **One-dimensional case.** If $g$ is $C^1$ with $g'\neq0$ on $[a,b]$, then $g$ is strictly monotone, and the substitution formula holds with $|g'|$. Stated as motivation and as a special case of (3).
+ **Theorem (3)–(5).** Stated with the MAT237 hypotheses. The compact measurable sets ensure the integrals exist; the boundary is negligible for the usual regions.
+ **Linear volume scaling (6).** For an invertible linear $A$, $\operatorname{vol}(A(E))=|\det A|\operatorname{vol}(E)$. Standard; follows by changing basis to a diagonal or triangular form, or by the singular-value decomposition.
+ **Local linearisation.** On a small cube $C_k$ centred at $u_k$, $\Phi(u)\approx\Phi(u_k)+D\Phi(u_k)(u-u_k)$, and the image volume is approximately $|\det D\Phi(u_k)|\operatorname{vol}(C_k)$. Summing gives the Riemann sum for the right-hand side. The article labels this a sketch and states that a complete proof controls the error using uniform continuity of $D\Phi$ and shows the images cover $S$ without essential overlap.
+ **Polar determinant.** $x_r=\cos\theta$, $x_\theta=-r\sin\theta$, $y_r=\sin\theta$, $y_\theta=r\cos\theta$; determinant $r\cos^2\theta+r\sin^2\theta=r$.
+ **Cylindrical determinant.** The matrix is block triangular with a $2\times2$ polar block and a $1\times1$ block $(1)$; determinant $r$.
+ **Spherical determinant.** Developing the $3\times3$ determinant gives $-\rho^2\sin\varphi$ for the column order $(\rho,\theta,\varphi)$. The ordered coordinates are left-handed, so the determinant is negative; the absolute value is $\rho^2\sin\varphi$. This sign was checked numerically at three random points (see below). Many texts order the columns as $(\rho,\varphi,\theta)$ and obtain $+\rho^2\sin\varphi$; the absolute value is the same.
+ **Affine example.** $\Phi(u,v)=(u+v,u-v)$ has determinant $-2$, image the square with vertices $(0,0),(1,1),(2,0),(1,-1)$, area $2$; $\iint_S x=2$ both from the formula and from centroid times area.
+ **Ellipse example.** $x=au$, $y=bv$ has determinant $ab$; the unit disc has area $\pi$, so the ellipse has area $\pi ab$. For the second moment, $\iint_D u^2=\pi/4$ in polar coordinates, so $\iint_E x^2=a^3b\pi/4$.
+ **Non-injectivity.** $\Phi(u,v)=(u^2,v)$ on $[-1,1]\times[0,1]$ has determinant $2u$ and is two-to-one; $\int_T|2u|=2$ while the image area is $1$. The formula counts multiplicity; it does not apply to the ordinary integral over the image.
+ **Vanishing Jacobian.** The same map has $\det=0$ on $u=0$, where the inverse function theorem fails. A vanishing Jacobian on a negligible set does not by itself destroy the formula (the map $u\mapsto u^3$ is a one-dimensional example), but the theorem's hypothesis is not satisfied, so the conclusion must be checked separately.
+ **Missing absolute value.** $\Phi(u,v)=(u,-v)$ has determinant $-1$; omitting the absolute value would give a negative area.
+ **Regularity.** A continuous non-$C^1$ map can fail the formula; the $C^1$ hypothesis is essential. Stated without a constructed example, because the standard examples require Cantor-type sets and are outside the scope of the entry.

## Independent checks

Python 3 script `work/checks/verify_batch6.py` (outside the repository), composite Simpson quadrature and exact algebra:

+ linear map area: computed $2$, exact $|\det|=2$;
+ linear map first moment: computed $2$, exact centroid $\times$ area $=2$;
+ ellipse area for $a=2$, $b=3$: computed $6\pi=18.8495559215$, exact $\pi ab$;
+ disc moment $\iint_D u^2$: computed $\pi/4=0.785398163397$ from the polar factorization;
+ ellipse second moment: computed $6\pi=18.8495559215$, exact $\pi a^3b/4$;
+ polar Gaussian over the unit disc: computed $1.9858653038$, exact $\pi(1-e^{-1})$;
+ non-injective multiplicity: computed $2$, exact $\int_{-1}^1 2|u|\,du=2$.

All checks passed. The spherical determinant was also evaluated numerically at three random $(\rho,\theta,\varphi)$ points; the computed determinant was $-\rho^2\sin\varphi$ each time, confirming the sign in (8).

## Limitations

+ No LaTeX renderer, Pandoc or TeX installation is available (`pandoc` and `pdflatex` not found); the Markdown was checked structurally but not rendered.
+ The live route `https://algebrica.org/change-of-variables-in-multiple-integrals/` is proposed, not known to exist.
+ The full proof of the change-of-variables theorem is not reproduced; the article gives a local-linearisation sketch and says so.
+ Spivak's theorem numbering was not checked against a copy during this run; only the chapter is cited.
+ Open issues and pull requests in the upstream repository were not inspected.
+ Links to sibling batch articles are unpublished dependencies until this batch is merged.

## Figure briefs

See `figure-briefs.md` in this directory.
