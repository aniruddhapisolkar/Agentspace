# Research evidence — Fubini's Theorem

Batch: `20261127T121407Z-01`
Slug: `fubinis-theorem`
Article: `multivariable-calculus/fubinis-theorem.md`
Category: `multivariable-calculus` (provisional)
Research date: 2026-11-27

## Coverage check

Upstream `antoniolupetti/algebrica` was searched by filename and body text for "Fubini", "iterated integral", "product measure", "Tonelli" and "double integral".

+ No article with "Fubini" or "Tonelli" in its title or body was found.
+ `lines-planes-conic-sections/polar-coordinates.md` uses a double integral and states the polar transformation, but does not state or prove an iterated-integral theorem.
+ `functions/gaussian-function.md` evaluates a double integral by symmetry; it relies on the iterated formula without naming it.
+ `integrals/definite-integrals.md` establishes the one-dimensional theory that the section-wise argument uses.

Conclusion: not a duplicate. The entry supplies the theorem that the existing polar and Gaussian material uses implicitly. Open issues and pull requests were not inspected; no claim is made about planned upstream work.

## Scope and reader contract

After reading the article, the reader can:

+ state the rectangle form of Fubini's theorem with the integrability and section hypotheses;
+ explain why the integrability of the slice function $g$ is a separate conclusion;
+ follow the step-function proof that compares $g$ with the Darboux sums;
+ apply the theorem to type I and type II regions and to $z$-simple solids;
+ change the order of integration by redrawing the region;
+ compute an integral that is impossible in one order and elementary in the other;
+ explain why $f=(x^2-y^2)/(x^2+y^2)^2$ has unequal iterated integrals and is not integrable;
+ state Tonelli's theorem and the Fubini condition $\int|f|<\infty$ in the Lebesgue setting.

Assumed prerequisites: the Riemann integral in one and several variables, Darboux sums, continuity and uniform continuity, and the definition of a plane region of type I or II. Exclusions: a full construction of product measures, the proof of Tonelli's theorem, and the general Fubini theorem for abstract $\sigma$-finite spaces (stated, not proved).

## Sources consulted

1. University of Toronto, MAT237, *Multivariable Calculus*, §4.3 "Iterated Integrals", "The Iterated Integral Theorem".
   URL: https://www.math.toronto.edu/courses/mat237y1/20199/notes/Chapter4/S4.3.html
   Accessed: 2026-11-27. Full text read.
   Supports: the exact rectangle statement — $f$ integrable, every section $f_y$ integrable, $g(y)=\int_a^b f(x,y)\,dx$ integrable, and $\iint_R f=\int_c^d g$; the remark that the roles of $x$ and $y$ may be switched; the reduction to non-rectangular regions; and the $n$-dimensional generalisation.
   Use: the theorem statement (2)–(3), the section hypothesis, and the structure of the proof. The step-function proof in the article is written out independently from the Darboux estimates; MAT237 states the theorem and leaves the proof to its exercises.

2. OpenStax, *Calculus Volume 3*, §5.1 "Double Integrals over Rectangular Regions", Theorem 5.2 (Fubini's Theorem).
   URL: https://openstax.org/books/calculus-volume-3/pages/5-1-double-integrals-over-rectangular-regions
   Accessed: 2026-11-27. Full text read.
   Supports: the continuous case on a rectangle, the equality of the two iterated integrals and the double integral, and the extension to bounded functions discontinuous on finitely many continuous curves.
   Use: independent confirmation of the continuous corollary and the application conditions.

3. Gerald B. Folland, *Real Analysis: Modern Techniques and Their Applications*, 2nd edition, §2.5 "Product Measures".
   Publisher: Wiley, 1999. No stable open-access URL; consulted from the standard text.
   Supports: the Tonelli theorem for nonnegative measurable functions on $\sigma$-finite spaces, the Fubini theorem under $\int|f|\,d(\mu\times\nu)<\infty$, and the role of $\sigma$-finiteness.
   Use: the measure-theoretic statements (9) and the absolute-integrability condition. The statements are paraphrased; no proof is reproduced.

4. Algebrica upstream `integrals/definite-integrals.md`, `lines-planes-conic-sections/polar-coordinates.md` and `functions/gaussian-function.md`.
   URLs: https://algebrica.org/definite-integrals/, https://algebrica.org/polar-coordinates/, https://algebrica.org/gaussian-function/
   Accessed through the upstream clone, 2026-11-27.
   Supports: house notation, British-English register, and the existing uses of iterated integrals.

## Definitions and conventions selected

+ Rectangle $R=[a,b]\times[c,d]$; integrability in the Riemann sense.
+ Vertical section $f_x(y)=f(x,y)$; slice function $g(x)=\int_c^d f(x,y)\,dy$.
+ Theorem hypothesis: $f$ integrable on $R$ and every section integrable.
+ Type I region: $a\le x\le b$, $\varphi_1(x)\le y\le\varphi_2(x)$.
+ $z$-simple solid: $(x,y)\in\Omega$, $\psi_1(x,y)\le z\le\psi_2(x,y)$.
+ Measure statement: $\sigma$-finite $(X,\mathcal{A},\mu)$ and $(Y,\mathcal{B},\nu)$; product measure $\mu\times\nu$.
+ British spelling: "recognise", "generalisation", "behaviour" where used.

## Mathematical claims and justification

+ **Theorem (2)–(3).** Stated with the section hypothesis, following MAT237. The symmetric form is stated separately rather than derived by a change of notation.
+ **Continuity gives the hypotheses.** A continuous function on a compact rectangle is bounded and uniformly continuous; each section is continuous, hence integrable; the slice function is continuous by uniform continuity, hence integrable. Explained.
+ **Step-function proof.** For a partition $P$, the functions $L_P(x)=\sum_j m_{ij}|J_j|$ and $U_P(x)=\sum_j M_{ij}|J_j|$ are constant on each $x$-interval. Pointwise $L_P\le g\le U_P$. Their integrals are $L(f,P)$ and $U(f,P)$. Integrability of $f$ gives partitions with $U-L<\varepsilon$, so $g$ is integrable and its integral equals $\iint_R f$. This is a complete proof of (2), modulo the standard equivalence of the Darboux criterion with integrability.
+ **Section hypothesis is not redundant.** The pointwise comparison (4) needs $g(x)$ to be defined at every $x$; without it the outer integral is not defined. Explained, with the counterexample as evidence that the conclusion can fail.
+ **Type I reduction (7).** Apply the rectangle theorem to $F=f\chi_D$; the section vanishes outside $[\varphi_1(x),\varphi_2(x)]$. The boundary contributes nothing because it has zero area.
+ **Triple reduction (8).** Apply Fubini first in $z$ over the interval $[\psi_1,\psi_2]$, then in the plane. Direct iteration.
+ **Order reversal example.** $D=\{0\le x\le1,\ x^2\le y\le1\}$; $\int_0^1\int_0^{\sqrt y}xe^{y^2}\,dx\,dy=\int_0^1(y/2)e^{y^2}\,dy=(e-1)/4$. The region description is correct: $y\ge x^2$ with $0\le x\le1$ is equivalent to $0\le y\le1$, $0\le x\le\sqrt y$.
+ **Rectangle example.** $\int_0^1\int_0^1x\cos(xy)\,dy\,dx=\int_0^1\sin x\,dx=1-\cos1$. The inner integral is $\sin x$ because $\int_0^1x\cos(xy)\,dy=[\sin(xy)]_{y=0}^{1}=\sin x$.
+ **Counterexample.** For $f=(x^2-y^2)/(x^2+y^2)^2$ on $[0,1]^2$, $\int_0^1f\,dx=-1/(1+y^2)$ and $\int_0^1f\,dy=1/(1+x^2)$; the iterated integrals are $-\pi/4$ and $\pi/4$. The antiderivatives are $-x/(x^2+y^2)$ and $y/(x^2+y^2)$ respectively, verified by differentiation. The function is unbounded near the origin and $|f|\sim r^{-2}$ along generic directions, so $\int|f|=\infty$ and neither the Riemann nor the Lebesgue integrability hypothesis holds.
+ **Tonelli (9).** Stated for nonnegative measurable $f$ on $\sigma$-finite spaces, with extended values allowed. No proof; attribution to Folland §2.5.
+ **Fubini (measure form).** Stated under $\int|f|<\infty$, with sections integrable almost everywhere. No proof; attribution to Folland §2.5.

## Independent checks

Python 3 script `work/checks/verify_batch6.py` (outside the repository), composite Simpson quadrature:

+ $x e^{y^2}$ over $0\le x\le\sqrt y\le1$: computed $0.429570457115$, exact $(e-1)/4=0.429570457115$;
+ $x\cos(xy)$ over $[0,1]^2$: computed $0.459697694132$, exact $1-\cos1=0.459697694132$;
+ counterexample, first order: computed $-0.785398163397$, exact $-\pi/4$;
+ counterexample, second order: computed $0.785398163397$, exact $\pi/4$.

All four checks passed. The two counterexample values were also derived exactly from the displayed antiderivatives, which is the stronger verification.

## Limitations

+ No LaTeX renderer, Pandoc or TeX installation is available (`pandoc` and `pdflatex` not found); the Markdown was checked structurally but not rendered.
+ The live route `https://algebrica.org/fubinis-theorem/` is proposed, not known to exist.
+ The measure-theoretic Tonelli and Fubini theorems are stated without proof; Folland is cited for them. The Riemann proof is given in full.
+ The exact theorem numbering in Folland was not checked against a copy during this run; only the section (§2.5) is cited.
+ Open issues and pull requests in the upstream repository were not inspected.
+ Links to sibling batch articles are unpublished dependencies until this batch is merged.

## Figure briefs

See `figure-briefs.md` in this directory.
