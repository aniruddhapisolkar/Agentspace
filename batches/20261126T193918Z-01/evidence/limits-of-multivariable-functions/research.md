# Research evidence — Limits of Multivariable Functions

Batch: `20261126T193918Z-01`
Slug: `limits-of-multivariable-functions`
Article: `multivariable-calculus/limits-of-multivariable-functions.md`
Category: `multivariable-calculus` (provisional; upstream has no dedicated category)
Research date: 2026-11-26

## Coverage check

The upstream tree `antoniolupetti/algebrica` (shallow clone of the current default branch) was inspected.

+ `limits/` contains single-variable limit entries: `limits.md`, `indeterminate-forms.md`, `remarkable-limits.md`, `little-o-notation.md`, `big-o-notation.md`, `hierarchy-of-growth-rates.md`, `limits-using-taylor-expansions.md`, plus Italian translations.
+ No entry on limits of functions of several variables was found by filename or by searching article bodies for "multivariable", "several variables" and "path".
+ `derivatives/partial-derivatives.md` covers multivariable partial differentiation and already uses the `multivariable-calculus` tag, but it presupposes the limit concept rather than treating it.
+ Conclusion: the requested topic is not a duplicate; it is a missing prerequisite for multivariable differentiation.

No open issues or pull requests were inspected; the GitHub API was not queried for issue text. This limits the claim about planned upstream work, not the claim that no article file exists.

## Scope and reader contract

After reading the article, the reader can:

+ state the epsilon–delta definition of a limit for a function of $n$ real variables and explain why the point must be an accumulation point of the domain;
+ prove uniqueness of the limit and use the sequential criterion;
+ decide whether a given limit exists by algebraic bounds, uniform polar estimates, or two-path counterexamples;
+ distinguish simultaneous limits from iterated limits and explain why neither determines the other;
+ apply continuity, the algebra of limits and compactness on a domain.

Prerequisites assumed: the single-variable limit, continuity, sequences, the Euclidean norm, and elementary inequalities. These are recalled where used. Exclusions: uniform continuity, the general topology of $\mathbb{R}^n$ beyond open/closed/compact statements, limits of vector-valued maps, and differentiability, which is deferred to the linked tangent-plane article.

## Sources consulted

1. OpenStax, *Calculus Volume 3*, §4.2 "Limits and Continuity".
   URL: https://openstax.org/books/calculus-volume-3/pages/4-2-limits-and-continuity
   Accessed: 2026-11-26. Full text read.
   Supports: the $\delta$-disc definition, the punctured-disc condition, limit laws, path dependence and failure of limits along different paths, boundary-point limits, continuity in two and three variables, composition of continuous functions, and the extension to $n$ variables.
   Use: primary definition and terminology. The article rephrases everything and does not copy OpenStax prose.

2. Algebrica upstream entries `derivatives/partial-derivatives.md` and `limits/limits.md`.
   URL: https://algebrica.org/partial-derivatives/ and https://algebrica.org/limits/
   Accessed through the upstream clone, 2026-11-26.
   Supports: house notation ($\mathbb{R}^n$, open set $A$, partial derivative notation), British-English register, heading style, and the existing site-relative links reused here.
   Use: editorial conventions only, not mathematical evidence.

3. Independent derivation and verification (this batch).
   The uniqueness proof, sequential criterion, path-test proposition and iterated-limit proposition were written out and checked step by step. The example limits and inequalities were checked numerically with exact rational arithmetic where possible (see "Independent checks" below).

Limitation: a second full textbook treatment of the multivariable limit was not retrieved in accessible text form. OpenStax was the only complete external treatment read; the central statements were therefore independently proved rather than accepted from a single source. This is recorded as a source limitation, not as a correctness gap.

## Definitions and conventions selected

+ $A\subseteq\mathbb{R}^n$ is the domain; $x_0$ is an accumulation point of $A$; the limit is taken through points of $A$ only. This is the formulation needed at boundary points and is the one used by OpenStax for boundary limits.
+ The punctured condition is $0<\|x-x_0\|<\delta$. The value $f(x_0)$ is irrelevant.
+ The Euclidean norm is used for display; equivalence of norms is mentioned but not proved in the article.
+ Continuity at $x_0$ requires $x_0\in A$ and $\lim_{x\to x_0}f(x)=f(x_0)$.
+ "Path" means a continuous curve $\gamma$ with $\gamma(t)\neq x_0$ for $t\neq0$ and $\gamma(t)\to x_0$.
+ Iterated limits are written with explicit parentheses to avoid ambiguity.

## Mathematical claims and justification

+ **Uniqueness.** If two limits $L,M$ exist, choose $\varepsilon=|L-M|/3$, take the two $\delta$'s, and use an accumulation point inside both punctured balls. The triangle inequality gives $|L-M|<2|L-M|/3$, a contradiction. Complete proof in the article.
+ **Sequential criterion.** Forward direction from the definition; reverse direction by constructing $x_k$ with $0<\|x_k-x_0\|<1/k$ and $|f(x_k)-L|\ge\varepsilon_0$. Complete proof in the article.
+ **Limit laws.** Stated, not proved; they are the standard componentwise arguments and are supported by OpenStax Theorem 4.1.
+ **Path test.** If the simultaneous limit existed, composition with each path would force the two path limits to equal it. Complete proof in the article.
+ **Iterated-limit proposition.** If the simultaneous limit is $L$ and the inner limit exists near $x_0$, then the outer limit is $L$; proof by letting $y\to y_0$ in the simultaneous estimate. The converse is false: $xy/(x^2+y^2)$ has both iterated limits $0$ and no simultaneous limit. A simultaneous limit may exist while an iterated limit fails: $x\sin(1/y)$ has simultaneous limit $0$ but no inner limit for $x\neq0$.
+ **Polar criterion.** If $|g(r,\theta)-L|\le h(r)$ for all $\theta$ and $h(r)\to0$, then $|f(x)-L|\le h(\|x-x_0\|)$. The article explicitly warns that a polar expression without a uniform bound proves nothing, using $xy^2/(x^2+y^4)$.
+ **Compactness.** Continuous real-valued image of a compact set is compact, hence bounded and attaining extrema. Stated as a standard theorem; the disc example is checked directly.

## Worked examples and independent checks

All checks were run on 2026-11-26 with Python 3 and exact `fractions.Fraction` arithmetic where the quantities are rational. The script is at `work/checks/verify_articles.py` in the agent workspace (not committed to the repository). Recorded output:

+ $xy/(x^2+y^2)$ along $y=0$ gives $0$; along $y=x$ gives $1/2$ for every tested $t>0$.
+ The inequality $|x^2y/(x^2+y^2)|\le|y|$ held in 20,000 random rational/float trials on $[-3,3]^2$.
+ The inequality $x^2y^2/(x^2+y^2)\le(x^2+y^2)/4$ held in 20,000 random trials.
+ $xy^2/(x^2+y^4)$ along $(t^2,t)$ gave $0.5$ for $t=0.1,0.01,10^{-5}$; along $y=1.7x$ it gave values tending to $0$ ($0.2667$, $0.02888$, $2.89\times10^{-5}$), consistent with the displayed line formula.
+ The displayed bound for $x^2y/(x^2+y^2)$ and the epsilon choice $\delta=\varepsilon$ were checked symbolically by hand and numerically by the inequality test.

These are supporting checks, not proofs. The proofs in the article are the basis for the claims.

## Editorial checks

+ Front matter: title, proposed canonical source URL, CC BY-NC 4.0 licence, lowercase hyphenated tags.
+ Only H2 headings; no H1 in the body; sentence-case headings.
+ Displays use `$$...$$`; the one tagged equation is referenced once.
+ British spellings used: "neighbourhood", "generalise" (where applicable), "behaviour", "centre", "parametrised".
+ Site-relative links: `../partial-derivatives/` and `../tangent-planes-and-linear-approximations/`. The first is an existing published route. The second points to a sibling article in this batch whose final slug and path are fixed in the manifest but which is not yet published; this dependency is disclosed here and must be rechecked before publication.
+ No images or SVG placeholders were inserted. Figure briefs are separate.

## Limitations

+ No LaTeX renderer or Markdown previewer was available in the environment, so rendering was checked by delimiter inspection only.
+ No second complete external textbook treatment was read; the main results were independently proved.
+ The link to the sibling tangent-plane article is an unpublished dependency at the time of writing.

## Tool checks actually performed

+ Cloned `aniruddhapisolkar/Agentspace` (default branch `main`, remote verified) and `antoniolupetti/algebrica`.
+ Listed and searched the upstream tree for duplicate coverage.
+ Fetched and read the OpenStax §4.2 page.
+ Ran the Python verification script above.
+ Checked math delimiters and front matter by inspection/grep.
