# Research evidence — Tangent Planes and Linear Approximations

Batch: `20261126T193918Z-01`
Slug: `tangent-planes-and-linear-approximations`
Article: `multivariable-calculus/tangent-planes-and-linear-approximations.md`
Category: `multivariable-calculus` (provisional)
Research date: 2026-11-26

## Coverage check

Upstream `antoniolupetti/algebrica` was searched by filename and body text.

+ `derivatives/partial-derivatives.md` defines partial derivatives, the gradient, the Hessian and the Jacobian, and links to `../planes/`, but does not treat tangent planes or linear approximation.
+ `lines-planes-conic-sections/planes.md` treats the equation of a plane in space, not tangent planes to graphs or level surfaces.
+ `derivatives/differential-of-a-function.md` treats the one-variable differential.
+ No article with "tangent plane", "linear approximation" or "total differential" in a multivariable sense was found.
+ Conclusion: the topic is not a duplicate. It connects the existing partial-derivative entry, the one-variable differential entry and the new multivariable Taylor entry.

Open issues and pull requests were not inspected; no claim is made about planned upstream work.

## Scope and reader contract

After reading the article, the reader can:

+ define differentiability of a function of two variables and explain why it is stronger than the existence of partial derivatives;
+ prove that differentiability forces the coefficients to be the partial derivatives, and that it implies continuity;
+ prove that continuous partial derivatives imply differentiability;
+ write the tangent plane and normal line of a graph, and the tangent plane of a level surface;
+ use the tangent plane for a numerical linear approximation and estimate its error from second derivatives;
+ use the total differential and interpret it as the first-order Taylor expansion;
+ recognise a continuous function whose partial derivatives exist but which has no tangent plane.

Assumed prerequisites: limits and continuity of several variables, partial derivatives, the gradient, the one-variable mean value theorem, and the one-variable differential. The level-surface section uses the chain rule along a curve. Exclusions: the implicit function theorem as a general theorem, tangent planes to parametrised surfaces, and constrained optimisation.

## Sources consulted

1. OpenStax, *Calculus Volume 3*, §4.4 "Tangent Planes and Linear Approximations".
   URL: https://openstax.org/books/calculus-volume-3/pages/4-4-tangent-planes-and-linear-approximations
   Accessed: 2026-11-26. Full text read.
   Supports: the definition of the tangent plane to a graph; the formula $z=f(x_0,y_0)+f_x(x_0,y_0)(x-x_0)+f_y(x_0,y_0)(y-y_0)$; the normal vector derived by a cross product; the definition of differentiability with the error term $E$ and $\lim E/\sqrt{(x-x_0)^2+(y-y_0)^2}=0$; the linear approximation; the total differential; the theorem that continuity of the first partials implies differentiability; the non-differentiable examples; the extension to three variables.
   Use: primary definition, terminology and the normal-vector derivation. All prose is rewritten; no passages copied.

2. LibreTexts, "14.4: Tangent Planes and Linear Approximations".
   URL: https://math.libretexts.org/Bookshelves/Calculus/Calculus_(OpenStax)/14%3A_Differentiation_of_Functions_of_Several_Variables/14.04%3A_Tangent_Planes_and_Linear_Approximations
   Accessed: 2026-11-26. A substantial extract was returned by web search; a direct fetch of a guessed alternate URL returned 404.
   Supports: the same statements as OpenStax, since this page mirrors the OpenStax chapter.
   Use: cross-check of wording and of the differentiability definition. It is not an independent mathematical source, because it reproduces the same text.

3. Algebrica upstream `derivatives/partial-derivatives.md`, `derivatives/differential-of-a-function.md` and `lines-planes-conic-sections/planes.md`.
   URLs: https://algebrica.org/partial-derivatives/, https://algebrica.org/differential-of-a-function/, https://algebrica.org/planes/
   Accessed through the upstream clone, 2026-11-26.
   Supports: house notation, British-English register, heading style, display style, and the site-relative links reused in the article.
   Use: editorial conventions only.

4. Independent proofs (this batch).
   The equivalence of the coefficients with the partial derivatives, the continuity implication, the sufficient condition via the mean value theorem, the gradient-normal argument for level surfaces, and the error bound from the second-order remainder were written out and checked. The numerical examples were verified with Python (see below).

Limitation: only one independent external treatment (OpenStax) was read for the differentiability theory; the LibreTexts page is a mirror. The central implications were therefore proved in the article rather than accepted from a single source.

## Definitions and conventions selected

+ Differentiability at $(x_0,y_0)$: there exist $a,b$ with
  $f(x_0+h,y_0+k)=f(x_0,y_0)+ah+bk+E(h,k)$ and $E(h,k)=o(\sqrt{h^2+k^2})$.
+ The linear approximation is $L(x,y)=f(x_0,y_0)+f_x(x_0,y_0)(x-x_0)+f_y(x_0,y_0)(y-y_0)$.
+ Tangent plane to the graph: $z=L(x,y)$.
+ Normal vector: $(f_x,f_y,-1)$, with $(-f_x,-f_y,1)$ also acceptable.
+ Level surface: $F(x,y,z)=c$ with $\nabla F(P)\neq0$; tangent plane $\nabla F(P)\cdot((x,y,z)-P)=0$.
+ Total differential: $dz=f_x\,dx+f_y\,dy$ with $dx=h$, $dy=k$.
+ Error bound: $|f-L|\le M(h^2+k^2)$ on a convex neighbourhood, where $M$ bounds $|f_{xx}|$, $|f_{xy}|$, $|f_{yy}|$ on the segment. This is a convenient non-sharp bound derived from the Lagrange remainder; the article states it as such.

## Mathematical claims and justification

+ **Coefficients are the partial derivatives.** Set $k=0$, divide by $h$, and use $E(h,0)/|h|\to0$; similarly for $b$. Complete proof in the article.
+ **Differentiability implies continuity.** Bound the increment by $(|a|+|b|)r+|E|$ and let $r\to0$. Complete proof.
+ **Continuous partials imply differentiability.** Split the increment into one-variable changes, apply the mean value theorem in each variable, subtract the linear part, and use continuity at the point. Complete proof.
+ **Partial derivatives alone are insufficient.** $f=xy/\sqrt{x^2+y^2}$ with $f(0,0)=0$ is continuous, has both partials zero at the origin, but $f(h,k)/\sqrt{h^2+k^2}=hk/(h^2+k^2)$ has no limit. The article also gives $xy/(x^2+y^2)$ as a discontinuous example.
+ **Tangent plane to a graph.** Cross product of the coordinate tangent vectors; normal $(f_x,f_y,-1)$. Complete derivation.
+ **Tangent plane to a level surface.** Differentiate $F(\gamma(t))=c$ along a curve on the surface; the gradient is orthogonal to every tangent vector. Complete argument, conditional on the level set being a smooth surface at a regular point.
+ **Error bound.** From the second-order Lagrange remainder, $|R|\le\frac12 M(h^2+2|hk|+k^2)\le M(h^2+k^2)$. Complete derivation, relying on the Taylor remainder proved in the sibling article.
+ **Total differential.** $\Delta z=dz+o(r)$ is the first-order expansion; the rectangle example is exact arithmetic.

## Worked examples and independent checks

Run on 2026-11-26 with Python 3; script `work/checks/verify_articles.py` in the agent workspace, not committed.

+ $f=x^2+3xy-y^2$ at $(1,2)$: $f=3$, $f_x=8$, $f_y=-1$; the plane $z=8x-y-3$ gives $3$ at $(1,2)$. The linearization error at $(0.01,-0.02)$ was $-0.0009$, equal to the quadratic remainder $h^2+3hk-k^2$; at $(0.1,0.05)$ the error was $0.0225$, again equal to the quadratic remainder.
+ $\sqrt{x^2+y^2}$ at $(4,4)$: the linear approximation at $(3.98,4.03)$ was $5.6639253173$, the exact value $5.6640356637$, and the error $1.1035\times10^{-4}$.
+ Sphere $x^2+y^2+z^2=14$ at $(1,2,3)$: $x+2y+3z=14$ at the point, consistent with the gradient $(2,4,6)$.
+ The quotient $xy/(x^2+y^2)$ along $y=x$ is $1/2$; the counterexample's quotient $xy/\sqrt{x^2+y^2}$ divided by $r$ is also $1/2$ along $y=x$ and $0$ along an axis.
+ $e^{x+y}$ error bound at $|x|,|y|\le0.1$: $e^{0.2}(0.02)\approx0.02443$; the exact error at $(0.1,0.1)$ is $e^{0.2}-1.2\approx0.02140$, below the bound.
+ Rectangle: $dA=0.01$, exact $\Delta A=0.0098$.

These checks support the arithmetic; the proofs in the article are the basis for the general statements.

## Editorial checks

+ Front matter with proposed canonical URL and CC BY-NC 4.0.
+ Only H2 headings, sentence case; no H1 in the body.
+ Four tagged equations, each referenced once.
+ British spellings: "behaviour", "recognise" (not used), "neighbourhood", "parametrised" (not used in the final text).
+ Site-relative links: `../multivariable-taylor-expansions/` (sibling in this batch, unpublished dependency disclosed) and `../partial-derivatives/` (existing route).
+ No SVG or image placeholders.

## Limitations

+ Only one independent external treatment was read; LibreTexts mirrors OpenStax.
+ No LaTeX renderer was available; rendering was checked by delimiter inspection.
+ The level-surface tangent-plane statement assumes the regular-point condition and does not prove the implicit function theorem.
+ The sibling Taylor link is unpublished at the time of writing.

## Tool checks actually performed

+ Searched upstream filenames and bodies for duplicate coverage.
+ Fetched and read the OpenStax §4.4 page; attempted a LibreTexts page and recorded the 404.
+ Ran the Python checks above.
+ Checked headings, delimiters, tags and front matter by script.
