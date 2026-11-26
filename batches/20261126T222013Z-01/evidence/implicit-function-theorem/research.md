# Research evidence — Implicit Function Theorem

Batch: `20261126T222013Z-01`
Slug: `implicit-function-theorem`
Article: `multivariable-calculus/implicit-function-theorem.md`
Category: `multivariable-calculus` (provisional)
Research date: 2026-11-26

## Coverage check

Upstream `antoniolupetti/algebrica` was searched by filename and body text for "implicit", "inverse function theorem", "Jacobian" and "level surface".

+ `functions/inverse-function.md` states and proves a one-dimensional inverse function theorem for a continuous differentiable function with non-vanishing derivative on an interval. It does not treat several variables.
+ `derivatives/derivative-of-the-inverse-function.md` proves the one-variable derivative formula by the chain rule.
+ `derivatives/partial-derivatives.md` defines the Jacobian matrix and the chain rule, but contains no implicit function theorem.
+ No article with "implicit function theorem" in the title or body was found.
+ Conclusion: the topic is not a duplicate. It is a multivariable extension of the one-dimensional inverse-function material and a prerequisite for the Lagrange-multiplier and tangent-space entries.

Open issues and pull requests were not inspected; no claim is made about planned upstream work.

## Scope and reader contract

After reading the article, the reader can:

+ state the scalar implicit function theorem and compute $\varphi'=-F_x/F_y$;
+ state the general theorem for $F:\mathbb{R}^{n+m}\to\mathbb{R}^m$ with the hypothesis $\det D_yF(a,b)\neq0$;
+ explain the linearised equation and why invertibility of $D_yF$ is the natural condition;
+ follow a complete contraction-mapping proof of existence, uniqueness, continuity and differentiability;
+ derive the matrix formula $D\varphi(a)=-[D_yF(a,b)]^{-1}D_xF(a,b)$;
+ apply the theorem to a circle, to an equation without a closed-form solution, and to a system of two equations;
+ recognise the graph and level-surface interpretations, including $T_pF^{-1}(0)=\ker DF(p)$;
+ explain the failure of the hypothesis in isolated-zero, crossing and cusp examples.

Assumed prerequisites: continuity, differentiability and $C^k$ maps of several variables, the Jacobian matrix, the chain rule, matrix inversion, the mean value inequality or the fundamental theorem of calculus along a segment, and the contraction mapping principle. The article states and proves the contraction principle. Exclusions: the inverse function theorem as a separate theorem (sibling entry), analytic versions, global inversion, and the full regular-value theorem for manifolds.

## Sources consulted

1. University of Toronto, MAT237, *Multivariable Calculus*, §3.1 "The Implicit Function Theorem".
   URL: https://www.math.toronto.edu/courses/mat237y1/20199/notes/Chapter3/S3.1.html
   Accessed: 2026-11-26. Full text read.
   Supports: the general statement with $F:S\subseteq\mathbb{R}^{n+k}\to\mathbb{R}^k$, $F(a,b)=0$ and $\det D_yF(a,b)\neq0$; existence and uniqueness of a $C^1$ map on balls; the derivative formula $D_yF(a,b)Df(a)=-D_xF(a,b)$; the special cases $n=k=1$, $n=2,k=1$, and $n=1,k=2$; the interpretation by linearisation; the limitations (local, no formula, no size estimate).
   Use: statement, notation, derivative formula, and the linearisation explanation. All prose is rewritten; no passages copied.

2. Jiří Lebl, *Basic Analysis I*, §8.5 "Inverse and implicit function theorems".
   URL: https://www.jirka.org/ra/html/sec_svinvfuncthm.html
   Accessed: 2026-11-26. Full text read.
   Supports: the inverse function theorem via the contraction mapping principle; the proof that the implicit function theorem follows from the inverse function theorem by applying it to $F(x,y)=(x,f(x,y))$; the derivative formula $g'(p)=-(A_y)^{-1}A_x$; the scalar circle example and the failure at a vertical tangent; examples of local but not global invertibility.
   Use: independent confirmation of the statement and derivative formula, and an alternative proof strategy (inverse-function reduction). The article uses a direct contraction proof for the implicit theorem and cites this reduction only as the equivalence statement.

3. Algebrica upstream `functions/inverse-function.md`, `derivatives/derivative-of-the-inverse-function.md` and `derivatives/partial-derivatives.md`.
   URLs: https://algebrica.org/inverse-function/, https://algebrica.org/derivative-of-the-inverse-function/, https://algebrica.org/partial-derivatives/
   Accessed through the upstream clone, 2026-11-26.
   Supports: house notation, the one-dimensional inverse theorem, the Jacobian and chain-rule conventions, British-English register and heading style.
   Use: editorial conventions and the existing one-variable material.

4. Independent proof (this batch).
   The contraction estimate, the uniform-continuity argument for the continuity of $\varphi$, the little-o argument for differentiability, the induction for $C^k$, and the matrix derivative formula were written out and checked. The examples were verified with Python (see below).

Limitation: Trench's *Introduction to Real Analysis* §6.4 was located through LibreTexts, but the page returned only a metadata shell, so it was not used as a source. The two sources actually read are MAT237 and Lebl; both are university-level analysis texts and agree on the statement and formula. The direct contraction proof in the article is independent of Lebl's inverse-function reduction.

## Definitions and conventions selected

+ Coordinates: $(x,y)\in\mathbb{R}^n\times\mathbb{R}^m$; $x$ are the parameters, $y$ the solved variables.
+ $D_xF$ is the $m\times n$ matrix of partial derivatives with respect to $x$; $D_yF$ is the $m\times m$ matrix with respect to $y$.
+ Hypothesis: $F(a,b)=0$ and $\det D_yF(a,b)\neq0$.
+ Conclusion: unique $C^k$ map $\varphi:V\to W$ with $\varphi(a)=b$ and $F(x,\varphi(x))=0$; the zero set near $(a,b)$ is the graph of $\varphi$.
+ Derivative: $D\varphi(a)=-[D_yF(a,b)]^{-1}D_xF(a,b)$.
+ Scalar case: $\varphi'(x)=-F_x(x,\varphi(x))/F_y(x,\varphi(x))$.
+ Regular level set: $F^{-1}(0)$ near a point with $\operatorname{rank}DF(p)=m$ is a smooth $n$-dimensional submanifold with tangent space $\ker DF(p)$.

## Mathematical claims and justification

+ **Linearisation.** The linear equation $D_xF\,h+D_yF\,k=0$ has a unique solution $k$ for every $h$ exactly when $D_yF$ is invertible. The theorem transfers this to the nonlinear equation locally. Complete explanation.
+ **Contraction proof, existence and uniqueness.** Normalise $D_yF(a,b)=I$; define $G_x(y)=y-F(x,y)$; choose $\delta,\rho$ so that $\lVert D_yF-I\rVert\le1/2$ and $\lVert F(x,b)\rVert\le\delta/4$; show $G_x$ maps $\overline B(b,\delta)$ into itself and is a contraction with constant $1/2$; apply the contraction principle. Complete.
+ **Continuity.** Bound $\lVert\varphi(x)-\varphi(x')\rVert$ by $2\lVert F(x',\varphi(x'))-F(x,\varphi(x'))\rVert$ and use uniform continuity on the compact product. Complete.
+ **Differentiability.** Expand $0=F(x+h,\varphi(x+h))-F(x,\varphi(x))$; invert $D_yF$; use the estimate to show $\lVert k\rVert=O(\lVert h\rVert)$ and then $k=-[D_yF]^{-1}D_xF\,h+o(\lVert h\rVert)$. Complete.
+ **$C^k$ regularity.** Differentiate the identity and use the formula; the right-hand side is $C^{k-1}$ when $F$ is $C^k$ and $\varphi$ is $C^{k-1}$. Induction. Complete.
+ **Scalar formula.** Set $n=m=1$ in the matrix formula, or differentiate $F(x,\varphi(x))=0$. Complete.
+ **Circle.** At $(0,1)$, $F_y=2$ and $\varphi(x)=\sqrt{1-x^2}$; at $(1,0)$, $F_y=0$ and the tangent is vertical. Complete.
+ **System.** $F_1=u+v-x$, $F_2=uv-y$ at $(3,2,2,1)$: $D_{(u,v)}F=\begin{pmatrix}1&1\\1&2\end{pmatrix}$, determinant $1$; the derivative matrix is $\begin{pmatrix}2&-1\\-1&1\end{pmatrix}$; implicit differentiation gives the same values. Complete.
+ **Level surface.** For $F(x,y,z)=z-h(x,y)$, $F_z=1$ and the formula gives $(h_x,h_y)$. For general $F$, the tangent space is $\ker DF(p)$ under the rank condition. Complete for the graph case; the general tangent-space statement is the standard regular-level-set consequence.

## Worked examples and independent checks

Run on 2026-11-26 with Python 3; script `work/checks/verify_batch4.py` in the agent workspace, not committed.

+ Circle: $F(0,1)=0$, $F_y(0,1)=2$; $\varphi(0)=1$; $\varphi'(0)=0$.
+ Cubic: $F(0,0)=0$, $F_y(0,0)=1$; implicit differentiation gives $\varphi'(0)=-1$.
+ System: the point $(u,v)=(2,1)$ satisfies $u+v=3$ and $uv=2$; the Jacobian determinant at $(2,1)$ is $1$; the matrix inverse is $\begin{pmatrix}2&-1\\-1&1\end{pmatrix}$; the partial derivatives satisfy the differentiated equations.
+ Failures: $x^2+y^2=0$ has only the real solution $(0,0)$; $x^2-y^2=0$ gives $y=\pm x$; $x^2-y^3=0$ gives $y=x^{2/3}$, which is not differentiable at $0$.

These checks support the arithmetic; the proof in the article is the basis for the general statement.

## Editorial checks

+ Front matter with proposed canonical URL and CC BY-NC 4.0.
+ Only H2 headings, sentence case; no H1 in the body.
+ Seven tagged equations, all referenced in the text.
+ British spellings: "neighbourhood", "linearisation", "differentiating", "behaviour" (not used).
+ Site-relative links: `../inverse-function-theorem/` (sibling in this batch, unpublished dependency) and `../lagrange-multipliers/` (sibling in this batch, unpublished dependency). No link to a non-existent route.
+ No SVG or image placeholders.

## Limitations

+ The general regular-level-set tangent-space statement is stated as a consequence of the theorem and linear algebra, not proved as a separate manifold theorem.
+ The proof uses the contraction mapping principle and the mean value integral; it assumes the standard completeness of closed balls in $\mathbb{R}^m$.
+ The article does not discuss analytic or holomorphic versions.
+ No LaTeX renderer was available; rendering was checked by delimiter inspection.

## Tool checks actually performed

+ Searched upstream filenames and bodies for duplicate coverage.
+ Fetched and read MAT237 §3.1 and Lebl §8.5; attempted Trench §6.4 and recorded that only a metadata shell was returned.
+ Ran the Python checks above.
+ Checked headings, delimiters, tags and front matter by script.
