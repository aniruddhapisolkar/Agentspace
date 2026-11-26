# Research evidence — Multivariable Extrema and Saddle Points

Batch: `20261126T222013Z-01`
Slug: `multivariable-extrema-and-saddle-points`
Article: `multivariable-calculus/multivariable-extrema-and-saddle-points.md`
Category: `multivariable-calculus` (provisional)
Research date: 2026-11-26

## Coverage check

Upstream `antoniolupetti/algebrica` was searched by filename and body text.

+ `derivatives/partial-derivatives.md` defines partial derivatives, the gradient, the Hessian and the Jacobian. One paragraph states the second-derivative classification at a critical point and links to the one-variable entry, but it gives no proof, no determinant form, no saddle-point analysis and no compact-domain procedure.
+ `derivatives/maximum-minimum-and-inflection-points.md` treats the one-variable first- and second-derivative tests.
+ `differential-calculus-theorems/weierstrass-theorem.md` proves the extreme value theorem on a closed bounded interval of the real line, not on a subset of $\mathbb{R}^n$.
+ No article with "saddle point", "second derivative test" for several variables, or multivariable extrema in the title or body was found.
+ Conclusion: the topic is a focused complementary treatment, not a duplicate. It expands the single Hessian paragraph in the partial-derivatives entry.

Open issues and pull requests were not inspected; no claim is made about planned upstream work.

## Scope and reader contract

After reading the article, the reader can:

+ define local, strict and global extrema of a function of several variables, and distinguish interior from boundary points;
+ state and prove Fermat's theorem for several variables by restriction to coordinate lines;
+ define a critical point and a saddle point, and explain why a vanishing gradient is necessary but not sufficient;
+ state the second derivative test in terms of the Hessian, and prove the positive definite, negative definite and indefinite cases from the second-order Taylor expansion;
+ use the two-variable determinant form and explain why $\Delta=0$ is inconclusive;
+ classify the critical points of a cubic example and of several degenerate examples;
+ find global extrema on a compact set by combining interior critical points with a boundary analysis;
+ use positive semidefiniteness of the Hessian on a convex set to conclude global convexity, and positive definiteness to conclude uniqueness of a critical point.

Assumed prerequisites: limits and continuity of several variables, partial derivatives, the gradient, the Hessian, the second-order Taylor expansion with Peano remainder, eigenvalues of symmetric matrices, and the one-variable Fermat theorem. The article recalls the eigenvalue criterion and the one-variable reduction. Exclusions: constrained optimisation (separate entry), the general theory of convex functions, Morse theory, and numerical optimisation.

## Sources consulted

1. OpenStax, *Calculus Volume 3*, §4.7 "Maxima/Minima Problems".
   URL: https://openstax.org/books/calculus-volume-3/pages/4-7-maxima-minima-problems
   Accessed: 2026-11-26. Full text read.
   Supports: definitions of local and global extrema on a disk; critical points where both partial derivatives vanish or fail to exist; Fermat's theorem for two variables; the saddle-point definition; the second derivative test with $D=f_{xx}f_{yy}-f_{xy}^2$ and the four cases; the extreme value theorem on a closed bounded set in the plane; the procedure of comparing interior critical values with boundary values.
   Use: standard terminology, the determinant form, and the compact-domain procedure. All prose is rewritten; no passages copied.

2. Paul Dawkins, *Paul's Online Math Notes*, Calculus III, §14.3 "Relative Minimums and Maximums".
   URL: https://tutorial.math.lamar.edu/Classes/CalcIII/RelativeExtrema.aspx
   Accessed: 2026-11-26. Full text read.
   Supports: the same definitions of relative extrema and critical points; the proof that a relative extremum with existing first derivatives is a critical point, by restricting to $g(x)=f(x,b)$ and $h(y)=f(a,y)$; the $xy$ saddle example; the determinant test and the statement that $D=0$ is inconclusive.
   Use: independent confirmation of the definitions, the coordinate-line proof of Fermat's theorem, and the determinant classification.

3. Algebrica upstream `derivatives/partial-derivatives.md`, `derivatives/maximum-minimum-and-inflection-points.md` and `differential-calculus-theorems/weierstrass-theorem.md`.
   URLs: https://algebrica.org/partial-derivatives/, https://algebrica.org/maximum-minimum-and-inflection-points/, https://algebrica.org/weierstrass-theorem/
   Accessed through the upstream clone, 2026-11-26.
   Supports: house notation for the Hessian, British-English register, heading style, and the site-relative links reused in the article.
   Use: editorial conventions and the existing one-variable material. The upstream Hessian paragraph is expanded, not copied.

4. Independent proofs (this batch).
   The coordinate-line proof of Fermat's theorem, the eigenvalue proof of the definite and indefinite cases of the second derivative test, the Sylvester-equivalent determinant classification, the compact-disk computation, and the convexity argument were written out and checked. The numerical values were verified with Python (see below).

Limitation: only two independent external treatments were read (OpenStax and Paul's Notes), and both are standard calculus texts rather than research monographs. The central implications were therefore proved in the article rather than accepted from a single source. The general $n$-dimensional statement is not stated in either source in full; it is the natural coordinate-free form of the two-variable theorem and is proved directly from Taylor's theorem.

## Definitions and conventions selected

+ Local maximum at $a$: there is $r>0$ with $f(x)\le f(a)$ for all $x\in A\cap B(a,r)$. Strict if the inequality is strict for $x\neq a$.
+ Critical point: $\nabla f(a)=0$, or at least one first partial derivative fails to exist at $a$. Stationary point: the gradient exists and vanishes.
+ Saddle point: a critical point that is neither a local maximum nor a local minimum; equivalently, every neighbourhood contains points with values above and below $f(a)$.
+ Hessian: $H_f(a)=(\partial^2 f/\partial x_i\partial x_j(a))$, symmetric for $f\in C^2$.
+ Positive definite: $h^{T}Hh>0$ for all $h\neq0$. Negative definite: $h^{T}Hh<0$ for all $h\neq0$. Indefinite: both signs occur.
+ Two-variable discriminant: $\Delta=f_{xx}f_{yy}-f_{xy}^2$, the determinant of the Hessian.
+ Convexity: $f$ is convex on a convex set $A$ if $f((1-t)a+tb)\le(1-t)f(a)+tf(b)$ for $t\in[0,1]$. The article uses the equivalent second-derivative criterion along segments.

## Mathematical claims and justification

+ **Fermat's theorem.** If $a$ is an interior local extremum and $f$ is differentiable at $a$, then $\nabla f(a)=0$. Proof by restricting to $g_i(t)=f(a+te_i)$ and applying the one-variable theorem. Complete in the article.
+ **The converse fails.** $f(x,y)=xy$ has a vanishing gradient at the origin and takes both signs in every neighbourhood. Complete verification.
+ **Second derivative test, definite cases.** From $f(a+h)-f(a)=\frac12h^{T}Hh+o(\lVert h\rVert^2)$ and $h^{T}Hh\ge\lambda_{\min}\lVert h\rVert^2$, choose the little-o threshold below $\lambda_{\min}/4$. Complete proof.
+ **Second derivative test, indefinite case.** Unit eigenvectors with eigenvalues of opposite signs give two lines along which the increment has opposite signs for small nonzero parameter. Complete proof.
+ **Semidefinite case.** The quadratic term can vanish in a direction, so higher-order terms decide. The four examples $x^4+y^4$, $-x^4-y^4$, $x^4-y^4$ and $x^2+y^3$ have zero or semidefinite Hessians at the origin and exhibit minimum, maximum, saddle and saddle respectively. Direct verification.
+ **Determinant form.** For a $2\times2$ symmetric matrix, $\Delta=\lambda_1\lambda_2$ and $\operatorname{tr}=f_{xx}+f_{yy}=\lambda_1+\lambda_2$. If $\Delta>0$, the eigenvalues have the same sign, determined by $f_{xx}$; if $\Delta<0$, they have opposite signs; if $\Delta=0$, at least one eigenvalue is zero. The article states the equivalence and does not reprove Sylvester's criterion.
+ **Compact-domain example.** On the unit disk, $f=x^2+y^2-xy$ has the only interior critical point at the origin, with a positive definite Hessian and value $0$; on the boundary $f=1-\frac12\sin2t$, whose range is $[\frac12,\frac32]$. Complete computation.
+ **Convexity criterion.** For $g(t)=f(a+t(x-a))$, $g''(t)=(x-a)^{T}H_f(a+t(x-a))(x-a)$. Positive semidefiniteness makes $g$ convex, so $g(1)\ge g(0)+g'(0)$. At a critical point this gives $f(x)\ge f(a)$. Positive definiteness makes the inequality strict for $x\neq a$. Complete proof.

## Worked examples and independent checks

Run on 2026-11-26 with Python 3; script `work/checks/verify_batch4.py` in the agent workspace, not committed.

+ $f=x^3+y^3-3xy$: critical points $(0,0)$ and $(1,1)$; Hessians $\begin{pmatrix}0&-3\\-3&0\end{pmatrix}$ and $\begin{pmatrix}6&-3\\-3&6\end{pmatrix}$; determinants $-9$ and $27$; values $0$ and $-1$. The gradient at both points is zero to machine precision.
+ $f=x^2+y^2-xy$ on the unit disk: the origin has Hessian eigenvalues $1$ and $3$ and value $0$; the boundary expression $1-\frac12\sin2t$ has minimum $0.5$ and maximum $1.5$.
+ Degenerate examples: at the origin, $x^4+y^4\ge0$ with equality only at the origin; $-x^4-y^4\le0$; $x^4-y^4$ changes sign along the axes; $x^2+y^3$ changes sign along $x=0$.
+ $f=x^2+y^2+xy$: Hessian eigenvalues $1$ and $3$, positive; the only critical point is the origin.

These checks support the arithmetic; the proofs in the article are the basis for the general statements.

## Editorial checks

+ Front matter with proposed canonical URL and CC BY-NC 4.0.
+ Only H2 headings, sentence case; no H1 in the body.
+ Two tagged equations, both referenced in the text.
+ British spellings: "behaviour", "neighbourhood", "centred".
+ Site-relative links: `../multivariable-taylor-expansions/`, `../weierstrass-theorem/`, `../lagrange-multipliers/`. The Taylor and Lagrange entries are siblings in this batch and are unpublished dependencies at the time of writing; the Weierstrass route exists upstream.
+ No SVG or image placeholders.

## Limitations

+ Only two independent external treatments were read; the general $n$-dimensional theorem is proved locally rather than quoted from a research reference.
+ No LaTeX renderer was available; rendering was checked by delimiter inspection.
+ The compact-domain example uses an explicit boundary parametrisation rather than the Lagrange multiplier method, which is treated in the sibling entry.
+ The convexity criterion is stated for $C^2$ functions on convex sets; it does not cover non-smooth convex functions.

## Tool checks actually performed

+ Searched upstream filenames and bodies for duplicate coverage.
+ Fetched and read OpenStax §4.7 and Paul's Notes §14.3.
+ Ran the Python checks above.
+ Checked headings, delimiters, tags and front matter by script.
