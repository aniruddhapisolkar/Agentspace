# Research evidence — Inverse Function Theorem

Batch: `20261126T222013Z-01`
Slug: `inverse-function-theorem`
Article: `multivariable-calculus/inverse-function-theorem.md`
Category: `multivariable-calculus` (provisional)
Research date: 2026-11-26

## Coverage check

Upstream `antoniolupetti/algebrica` was searched by filename and body text for "inverse function theorem", "Jacobian", "local inverse" and "change of variables".

+ `functions/inverse-function.md` states and proves a one-dimensional inverse function theorem for a continuous differentiable function with non-vanishing derivative on an interval.
+ `derivatives/derivative-of-the-inverse-function.md` proves the one-variable derivative formula $(f^{-1})'(y_0)=1/f'(x_0)$ by the chain rule and the difference quotient.
+ `derivatives/partial-derivatives.md` defines the Jacobian matrix and the chain rule for maps of several variables, but contains no inverse function theorem.
+ No article with "inverse function theorem" for several variables in the title or body was found.
+ Conclusion: the topic is not a duplicate. It extends the one-dimensional result to maps of $\mathbb{R}^n$ and depends on the implicit function theorem, a sibling in this batch.

Open issues and pull requests were not inspected; no claim is made about planned upstream work.

## Scope and reader contract

After reading the article, the reader can:

+ state the inverse function theorem with the hypothesis that $Df(a)$ is invertible;
+ explain the linearisation and the meaning of a nonzero Jacobian determinant;
+ prove the theorem from the implicit function theorem by applying it to $F(x,y)=f(x)-y$;
+ derive the derivative formula $Dg(b)=[Df(a)]^{-1}$;
+ explain the one-dimensional case and the examples $x^2$ and $x^3$;
+ compute local inverses and their derivatives for a linear map, polar coordinates and the complex-square map;
+ distinguish local invertibility from global injectivity;
+ explain the equivalence of the inverse and implicit function theorems;
+ list the consequences for open mappings, local coordinates and change of variables.

Assumed prerequisites: differentiability and $C^k$ maps of several variables, the Jacobian matrix, the chain rule, matrix inversion, the implicit function theorem (proved in the sibling entry), and the one-variable inverse function rule. Exclusions: global inversion theorems, the analytic/holomorphic inverse theorem, the constant-rank theorem, degree theory, and the full change-of-variables theorem for integrals.

## Sources consulted

1. University of Toronto, MAT237, *Multivariable Calculus*, §3.3 "Transformations and the Inverse Function Theorem".
   URL: https://www.math.toronto.edu/courses/mat237y1/20199/notes/Chapter3/S3.3.html
   Accessed: 2026-11-26. Full text read.
   Supports: the statement of the inverse function theorem for $f:U\to V$ of class $C^1$ with $Df(a)$ invertible; existence of open $M,N$ with $f:M\to N$ a bijection and $C^1$ inverse; the derivative formula $D(f^{-1})(y)=[Df(x)]^{-1}$; the discussion of polar coordinates and the choice of a branch; the proof strategy by reduction to a contraction theorem; the equivalence with the implicit function theorem.
   Use: statement, notation, derivative formula, polar example and the equivalence. All prose is rewritten; no passages copied.

2. Jiří Lebl, *Basic Analysis I*, §8.5 "Inverse and implicit function theorems".
   URL: https://www.jirka.org/ra/html/sec_svinvfuncthm.html
   Accessed: 2026-11-26. Full text read.
   Supports: the inverse function theorem with a complete contraction-mapping proof; the estimate $\lVert A-f'(x)\rVert<1/(2\lVert A^{-1}\rVert)$; the map $\varphi_y(x)=x+A^{-1}(y-f(x))$; the proof that the image is open; the differentiability and continuity of the inverse; the examples $f(x)=x^3$ and $f(x,y)=(x^2-y^2,2xy)$; the open-mapping corollary.
   Use: independent confirmation and the direct contraction strategy. The article's main proof uses the implicit function theorem; the direct contraction map is summarised in one paragraph.

3. Algebrica upstream `functions/inverse-function.md`, `derivatives/derivative-of-the-inverse-function.md` and `derivatives/partial-derivatives.md`.
   URLs: https://algebrica.org/inverse-function/, https://algebrica.org/derivative-of-the-inverse-function/, https://algebrica.org/partial-derivatives/
   Accessed through the upstream clone, 2026-11-26.
   Supports: the one-dimensional theorem and derivative formula, house notation for the Jacobian, British-English register and heading style.
   Use: editorial conventions and the existing one-variable material.

4. Independent proof (this batch).
   The derivation from the implicit function theorem, the proof that $f|_V$ is bijective onto $W$, the differentiation of $f(g(y))=y$, the equivalence derivation of the implicit theorem from the inverse theorem, and the examples were written out and checked. The numerical examples were verified with Python (see below).

Limitation: both external sources prove the theorem rigorously, but the article's main proof is a reduction to the sibling implicit function theorem rather than a reproduction of either source's proof. The direct contraction argument is summarised, not written out in full; the full contraction proof appears in the implicit-function article.

## Definitions and conventions selected

+ Map: $f:U\subseteq\mathbb{R}^n\to\mathbb{R}^n$ of class $C^k$, $k\ge1$.
+ Point: $a\in U$, $b=f(a)$.
+ Hypothesis: $Df(a)$ invertible, equivalently $J_f(a)=\det Df(a)\neq0$.
+ Conclusion: open $V\subseteq U$ with $a\in V$ and open $W$ with $b\in W$ such that $f|_V:V\to W$ is a bijection with $C^k$ inverse $g:W\to V$.
+ Derivative: $Dg(y)=[Df(g(y))]^{-1}$, in particular $Dg(b)=[Df(a)]^{-1}$.
+ One-dimensional case: $g'(b)=1/f'(a)$.
+ Local coordinates: near $a$, the components of $f$ form an alternative coordinate system.

## Mathematical claims and justification

+ **Linear case.** For $f(x)=Ax+b$, invertibility is equivalent to invertibility of $A$, and the inverse derivative is $A^{-1}$. Complete.
+ **Proof from the implicit theorem.** $F(x,y)=f(x)-y$ satisfies $F(a,b)=0$ and $D_xF(a,b)=Df(a)$ invertible; the implicit theorem gives a unique $C^k$ map $\varphi$ with $f(\varphi(y))=y$. After shrinking $V$ so that $f(V)\subseteq W$, every $x\in V$ with $f(x)=y\in W$ equals $\varphi(y)$ by uniqueness. Hence $f|_V$ is bijective onto $W$. Complete.
+ **Derivative formula.** Differentiate $f(g(y))=y$: $Df(g(y))Dg(y)=I$. A square matrix with a right inverse is invertible, so $Dg(y)=[Df(g(y))]^{-1}$. Complete.
+ **Direct contraction map.** $T_y(x)=x+A^{-1}(y-f(x))$ has $DT_y(x)=A^{-1}(A-Df(x))$, whose norm is at most $1/2$ near $a$; for $y$ near $b$, $T_y$ maps a closed ball into itself and is a contraction. The fixed point is the unique solution. Summary only; the full contraction argument is in the implicit-function article.
+ **One-dimensional examples.** $f(x)=x^2$ at $1$ has local inverse $\sqrt y$ and derivative $1/2$; at $0$ it is not injective. $f(x)=x^3$ at $0$ is globally invertible with inverse $y^{1/3}$, which is not differentiable at $0$. Complete.
+ **Linear example.** $f(x,y)=(x+y,x-y)$ has $Df=\begin{pmatrix}1&1\\1&-1\end{pmatrix}$ and inverse $g(u,v)=((u+v)/2,(u-v)/2)$; $Dg\,Df=I$. Complete.
+ **Polar coordinates.** $Df=\begin{pmatrix}\cos\theta&-r\sin\theta\\ \sin\theta&r\cos\theta\end{pmatrix}$, determinant $r$; the inverse derivative is $\begin{pmatrix}\cos\theta&\sin\theta\\-\sin\theta/r&\cos\theta/r\end{pmatrix}$; the map is not globally injective because of $2\pi$-periodicity. Complete.
+ **Complex square.** $f(x,y)=(x^2-y^2,2xy)$ has determinant $4(x^2+y^2)$, nonzero away from the origin; $f(-x,-y)=f(x,y)$, so it is locally but not globally invertible. Complete.
+ **Equivalence.** The inverse theorem follows from the implicit theorem as above. Conversely, for $F$ with $D_yF$ invertible, $G(x,y)=(x,F(x,y))$ has invertible derivative and its local inverse gives the implicit function. Complete.
+ **Open mapping.** If $Df$ is invertible at every point, every point has a neighbourhood mapped onto an open set, so the image of an open set is open. Complete.

## Worked examples and independent checks

Run on 2026-11-26 with Python 3; script `work/checks/verify_batch4.py` in the agent workspace, not committed.

+ Linear map: $Dg\,Df=I$ for the matrices above; the inverse formula gives $x=(u+v)/2$, $y=(u-v)/2$.
+ Polar: the determinant is $r$; the inverse derivative matrix multiplied by $Df$ is the identity; at $(r,\theta)=(1,\pi/4)$ the point is $(1/\sqrt2,1/\sqrt2)$.
+ Complex square: the determinant is $4(x^2+y^2)$; $f(1,1)=(0,2)$ and $f(-1,-1)=(0,2)$.
+ $x^2$: at $a=1$, $b=1$, $g'(1)=1/2$; at $a=0$, $f$ is not injective near $0$.
+ $x^3$: $g(y)=y^{1/3}$; $g'(0)$ does not exist as a finite derivative.

These checks support the arithmetic; the proof in the article is the basis for the general statement.

## Editorial checks

+ Front matter with proposed canonical URL and CC BY-NC 4.0.
+ Only H2 headings, sentence case; no H1 in the body.
+ Four tagged equations, all referenced in the text.
+ British spellings: "neighbourhood", "linearisation", "behaviour" (not used).
+ Site-relative links: `../implicit-function-theorem/` (sibling in this batch, unpublished dependency) and `../derivative-of-the-inverse-function/` (existing route).
+ No SVG or image placeholders.

## Limitations

+ The main proof depends on the implicit function theorem, which is proved in a sibling article in the same batch; the article states the reduction explicitly rather than repeating the contraction proof.
+ The direct contraction argument is only summarised; the full proof is in the implicit-function article.
+ The change-of-variables consequence is stated, not proved; the integral formula is outside scope.
+ No LaTeX renderer was available; rendering was checked by delimiter inspection.

## Tool checks actually performed

+ Searched upstream filenames and bodies for duplicate coverage.
+ Fetched and read MAT237 §3.3 and Lebl §8.5.
+ Ran the Python checks above.
+ Checked headings, delimiters, tags and front matter by script.
