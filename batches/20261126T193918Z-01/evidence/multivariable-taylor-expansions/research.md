# Research evidence — Multivariable Taylor Expansions

Batch: `20261126T193918Z-01`
Slug: `multivariable-taylor-expansions`
Article: `multivariable-calculus/multivariable-taylor-expansions.md`
Category: `multivariable-calculus` (provisional)
Research date: 2026-11-26

## Coverage check

Upstream `antoniolupetti/algebrica` was searched by filename and body text.

+ `derivatives/taylor-formula-with-remainder.md` treats the one-variable Taylor formula, the Peano and Lagrange remainders, and the Taylor polynomial. It does not treat several variables.
+ `series/taylor-series.md` treats one-variable Taylor series and convergence.
+ `derivatives/partial-derivatives.md` introduces the Hessian matrix and mixed derivatives but contains no multivariable Taylor expansion.
+ No article with "multivariable Taylor", "Taylor in several variables" or a multi-index formula was found.
+ Conclusion: the topic is not a duplicate. The entry complements the existing one-variable entries and links to them.

Open issues and pull requests were not inspected; no claim is made about planned upstream work.

## Scope and reader contract

After reading the article, the reader can:

+ use multi-index notation and count the terms of a multivariable Taylor polynomial;
+ state the first-order and second-order expansions and identify the gradient and Hessian;
+ state the Peano and Lagrange forms with their different hypotheses;
+ prove the Lagrange form by reduction to one variable, and prove the quadratic Peano form from it;
+ compute Taylor polynomials by series multiplication and composition, using uniqueness;
+ bound the remainder on a box and interpret the result;
+ explain why a $C^\infty$ function need not equal its Taylor series;
+ connect the second-order expansion with the classification of critical points.

Assumed prerequisites: partial derivatives, the gradient, the Hessian, the one-variable Taylor formula, little-o notation, and linear algebra at the level of symmetric matrices and quadratic forms. Exclusions: a full proof of the general Peano theorem, Taylor series convergence theory in several variables, and analytic functions of several variables beyond the flat-function counterexample.

## Sources consulted

1. University of Toronto, MAT237Y1 notes, §2.6 "Taylor's Theorem".
   URL: https://www.math.toronto.edu/courses/mat237y1/20199/notes/Chapter2/S2.6.html
   Accessed: 2026-11-26. Full text read.
   Supports: the $C^k$ Peano form with remainder $o(\|\mathbf h\|^k)$; the $C^2$ Lagrange form with $\theta$; the multi-index formula $P_{\mathbf a,k}(\mathbf h)=\sum_{|\alpha|\le k}\mathbf h^\alpha\partial^\alpha f(\mathbf a)/\alpha!$; the count $\binom{n+k}{k}$; the reduction $\varphi(s)=f(\mathbf a+s\mathbf h)$ and the chain-rule identity for $\varphi^{(j)}$; uniqueness of the Taylor polynomial and the composition/series shortcut.
   Use: primary theorem statements and proof strategy. The article's Lagrange proof expands the induction in full; the wording is original.

2. LibreTexts, "Taylor Polynomials of Functions of Two Variables" (Paul Seeburger, Monroe Community College).
   URL: https://math.libretexts.org/Bookshelves/Calculus/Supplemental_Modules_(Calculus)/Multivariable_Calculus/3%3A_Topics_in_Partial_Derivatives/Taylor__Polynomials_of_Functions_of_Two_Variables
   Accessed: 2026-11-26. Full text read.
   Supports: the explicit first-, second- and third-degree formulas in two variables with denominators $i!j!$; the grouping of the two mixed terms into $f_{xy}(x-a)(y-b)$; the worked examples $\sin 2x+\cos y$ and $xe^y+1$; the statement that the first-degree polynomial is the tangent plane.
   Use: cross-check of the two-variable expansion and of the coefficient bookkeeping.

3. Algebrica upstream `derivatives/taylor-formula-with-remainder.md` and `derivatives/partial-derivatives.md`.
   URLs: https://algebrica.org/taylor-formula-with-remainder/ and https://algebrica.org/partial-derivatives/
   Accessed through the upstream clone, 2026-11-26.
   Supports: house notation for the gradient and Hessian, display style, equation tags, British-English register, and the site-relative links used in the article.
   Use: editorial conventions only.

4. MIT OpenCourseWare 18.022, Lecture 19 "Taylor's Theorem".
   URL located by search: https://ocw.mit.edu/courses/18-022-calculus-of-several-variables-fall-2010/4770b19ccce68d98f0417e9393317482_MIT18_022F10_l_19.pdf
   Status: not read. The fetch tool rejected the PDF content type and no PDF text extractor was installed. It is listed for transparency and was not used as evidence.

## Definitions and conventions selected

+ Multi-index: $\alpha\in\mathbb{N}_0^n$, $|\alpha|=\sum\alpha_i$, $\alpha!=\prod\alpha_i!$, $h^\alpha=\prod h_i^{\alpha_i}$, $\partial^\alpha f$ as in the article.
+ Taylor polynomial of order $k$ at $a$: $P_{a,k}(h)=\sum_{|\alpha|\le k}\partial^\alpha f(a)h^\alpha/\alpha!$.
+ Peano form: $f\in C^k$ on an open set, remainder $o(\|h\|^k)$.
+ Lagrange form: $f\in C^{k+1}$ and the segment $[a,a+h]$ in the domain; remainder evaluated at $a+\theta h$ with $\theta\in(0,1)$.
+ "Differentiable" means Fréchet differentiability, expressed by (1) in the article; the gradient is identified by taking $h=te_i$.

The LibreTexts page states the two-variable formula under the weaker hypothesis that the partials "exist". That hypothesis is sufficient to define the polynomial but not to assert the Peano remainder. The article follows the Toronto $C^k$ hypothesis, which is the standard sufficient condition, and does not repeat the weaker claim.

## Mathematical claims and justification

+ **Count of multi-indices.** The number with $|\alpha|=k$ is $\binom{n+k-1}{k}$ by stars and bars; summing over $0\le j\le k$ gives $\binom{n+k}{k}$. Checked for $n=2$, $k=2$: six terms.
+ **First-order expansion.** Definition of differentiability; the component identification follows from $h=te_i$.
+ **Second-order Lagrange form.** Reduction to $\varphi(t)=f(a+th)$ and the one-variable formula of order one. Complete proof in the article.
+ **Quadratic Peano form.** Subtract the Hessian at $a$ from the Hessian at $a+\theta h$; continuity of the second partials gives $\|H(a+\theta h)-H(a)\|\to0$, hence $R_2=o(\|h\|^2)$. Complete proof in the article.
+ **General Lagrange form.** Induction on $j$ for $\varphi^{(j)}$; the coefficient identity is
  $$\sum_{i:\beta_i\ge1}\frac{j!}{(\beta-e_i)!}=\frac{(j+1)!}{\beta!}$$
  for $|\beta|=j+1$. Complete proof in the article.
+ **General Peano form.** Stated for $f\in C^k$; the general induction is not reproduced. This is an explicitly scoped reliance on the Toronto notes, not a claim that the article proves it.
+ **Uniqueness.** If two polynomials of degree at most $k$ have the same derivatives up to order $k$ at $a$, their difference has all derivatives up to order $k$ zero at $a$. A polynomial of degree at most $k$ with this property is zero: restrict to each line $a+th$ and use the one-variable argument. The article uses uniqueness to justify the series-multiplication shortcut.
+ **Critical-point classification.** Positive definite Hessian gives a strict local minimum, negative definite a strict local maximum, an indefinite Hessian a saddle, and a singular Hessian is inconclusive. Stated as a consequence of the second-order expansion; the proof is standard and not reproduced.

## Worked examples and independent checks

Run on 2026-11-26 with Python 3 and exact `fractions.Fraction` arithmetic where applicable. Script: `work/checks/verify_articles.py` in the agent workspace, not committed.

+ $e^x\cos y$ to order $3$: truncated polynomial multiplication over $\mathbb{Q}$ gave coefficients
  $1,\ x,\ \tfrac12x^2,\ -\tfrac12y^2,\ \tfrac16x^3,\ -\tfrac12xy^2$, matching the direct derivative coefficients $D^\alpha f(0,0)/\alpha!$ computed from $e^x$ and the derivatives of $\cos y$. All other coefficients up to total degree $3$ vanished.
+ $x^2y+y^3$ at $(1,1)$: the identity
  $f(1+h,1+k)=2+2h+4k+h^2+2hk+3k^2+h^2k+k^3$
  held in 1,000 random trials to $10^{-12}$.
+ $e^{x+y}$ at the origin: the implied $\theta$ in $R_2=(x+y)^3e^{\theta(x+y)}/6$ lay in $(0,1)$ for $s=-0.15,0.1,0.2$ (values $0.247$, $0.252$, $0.254$), consistent with the Lagrange form. The bound at $|x|,|y|\le0.1$ is $e^{0.2}(0.2)^3/6\approx1.63\times10^{-3}$; the actual error at $(0.1,0.1)$ is $1.40\times10^{-3}$.
+ $\sqrt{1+x+y}$ at the origin: numeric residuals divided by $x^2+y^2$ tended to $0$ at sample points, consistent with the quadratic expansion.
+ The multi-index coefficient identity was checked exactly for $n=2,3,4$ and all $\beta$ with entries $0,\ldots,3$, with no mismatch.
+ The third-order residual of $e^x\cos y$, divided by $(x^2+y^2)^2$, tended to $0$ at sample points.

These checks support the computations; the proofs in the article are the basis for the general statements.

## Editorial checks

+ Front matter with proposed canonical URL and CC BY-NC 4.0.
+ Only H2 headings, sentence case; no H1 in the body.
+ Three tagged equations, each referenced once in the text.
+ British spellings: "behaviour", "recognise" (not used), "centre", "generalise" (not used), "practise" (not used).
+ Site-relative links: `../partial-derivatives/`, `../taylor-formula-with-remainder/`, and `../tangent-planes-and-linear-approximations/`. The first two are existing routes; the third is a sibling in this batch and is an unpublished dependency disclosed here.
+ No SVG or image placeholders.

## Limitations

+ The general Peano theorem is stated with a reliable reference but not proved in full; only the quadratic case is proved.
+ No LaTeX renderer was available, so rendering was checked by delimiter inspection and display-width judgement.
+ The LibreTexts weaker hypothesis was not adopted; the discrepancy is recorded above.
+ The link to the sibling tangent-plane article is unpublished at the time of writing.

## Tool checks actually performed

+ Searched upstream filenames and bodies for duplicate coverage.
+ Fetched and read the Toronto §2.6 page and the LibreTexts page.
+ Attempted the MIT 18.022 PDF; recorded the content-type failure.
+ Ran the Python checks above.
+ Checked headings, delimiters, tags and front matter by script.
