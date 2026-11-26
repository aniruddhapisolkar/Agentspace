# Research evidence — Lagrange Multipliers

Batch: `20261126T222013Z-01`
Slug: `lagrange-multipliers`
Article: `multivariable-calculus/lagrange-multipliers.md`
Category: `multivariable-calculus` (provisional)
Research date: 2026-11-26

## Coverage check

Upstream `antoniolupetti/algebrica` was searched by filename and body text for "Lagrange", "multiplier", "constraint" and "constrained".

+ `derivatives/partial-derivatives.md` defines the gradient, the Jacobian and the chain rule, and states the Hessian classification at a free critical point. It does not treat constrained extrema or Lagrange multipliers.
+ `lines-planes-conic-sections/planes.md` gives the equation of a plane and the distance from a point to a plane, which is used only as an independent check in the worked example.
+ No article with "Lagrange multiplier" or "constrained optimisation" in the title or body was found.
+ Conclusion: the topic is not a duplicate. It depends on the gradient and on the implicit function theorem; the latter is a sibling in this batch and is an unpublished dependency at the time of writing.

Open issues and pull requests were not inspected; no claim is made about planned upstream work.

## Scope and reader contract

After reading the article, the reader can:

+ define a constrained local extremum on a set $g=0$;
+ explain the tangency of the level sets of the objective and the constraint, and derive the condition $\nabla f=\lambda\nabla g$;
+ state the precise hypotheses, including the constraint qualification $\nabla g\neq0$;
+ prove the multiplier theorem by testing the derivative along curves in the constraint set and identifying the tangent space with the kernel of $Dg$;
+ extend the condition to several constraints with a rank condition on the Jacobian;
+ solve one- and two-constraint problems, compare candidates and check existence separately;
+ interpret $\lambda$ as the derivative of the optimal value with respect to the constraint level;
+ recognise a failure of the constraint qualification.

Assumed prerequisites: partial derivatives, the gradient, the chain rule, level sets, and the implicit function theorem in the form "a regular level set is locally a graph and its tangent space is the kernel of the derivative". The article recalls the needed consequence. Exclusions: inequality constraints and Karush-Kuhn-Tucker theory, second-order sufficient conditions for constrained extrema, non-smooth constraints, and global existence theory beyond the compact case.

## Sources consulted

1. OpenStax, *Calculus Volume 3*, §4.8 "Lagrange Multipliers".
   URL: https://openstax.org/books/calculus-volume-3/pages/4-8-lagrange-multipliers
   Accessed: 2026-11-26. Full text read.
   Supports: the one-constraint theorem with the hypothesis $\nabla g\neq0$; the proof by parametrising the constraint curve by arc length and differentiating $f(x(s),y(s))$; the system $\nabla f=\lambda\nabla g$, $g=0$; the two-constraint form $\nabla f=\lambda_1\nabla g_1+\lambda_2\nabla g_2$; worked examples in two and three variables; the warning that the method finds candidates and that extrema must exist.
   Use: standard statement, terminology and the curve-parametrisation proof strategy. All prose is rewritten; no passages copied.

2. Paul Dawkins, *Paul's Online Math Notes*, Calculus III, §14.5 "Lagrange Multipliers".
   URL: https://tutorial.math.lamar.edu/Classes/CalcIII/LagrangeMultipliers.aspx
   Accessed: 2026-11-26. Full text read.
   Supports: the same system of equations; the geometric justification by tangency of level curves; the warning that minima and maxima may fail to exist even when the system has solutions; the need to check endpoints of variable ranges when the constraint has a boundary; the two-constraint form; the treatment of an inequality constraint as a region with an interior and a boundary.
   Use: independent confirmation of the method and of the existence and boundary caveats.

3. Algebrica upstream `derivatives/partial-derivatives.md` and `lines-planes-conic-sections/planes.md`.
   URLs: https://algebrica.org/partial-derivatives/ and https://algebrica.org/planes/
   Accessed through the upstream clone, 2026-11-26.
   Supports: house notation for the gradient and the Jacobian, the distance formula for a plane, British-English register and heading style.
   Use: editorial conventions and an independent check of the distance example.

4. Independent proofs (this batch).
   The curve argument for the multiplier condition, the identification of the tangent space under the constraint qualification, the several-constraint form, and the sensitivity formula $M'(c)=\lambda$ were written out and checked. The numerical examples were verified with Python (see below).

Limitation: neither external source proves the several-constraint theorem in full; OpenStax states it and Paul's Notes gives the system. The article proves it from the same tangent-space argument, with the rank condition stated explicitly. The sensitivity formula is not in either source at this level; it is derived in the article under a differentiability assumption on the optimal point.

## Definitions and conventions selected

+ Constraint set: $S=\{x\in U:g(x)=0\}$ for $g\in C^1(U)$.
+ Constrained local maximum at $p\in S$: there is $r>0$ with $f(x)\le f(p)$ for all $x\in S\cap B(p,r)$.
+ Constraint qualification for one constraint: $\nabla g(p)\neq0$.
+ Constraint qualification for $m$ constraints: $\operatorname{rank}Dg(p)=m$, equivalently the gradients $\nabla g_1(p),\ldots,\nabla g_m(p)$ are linearly independent.
+ Multiplier equation: $\nabla f(p)=\lambda\nabla g(p)$, or $\nabla f(p)=\sum_{j=1}^m\lambda_j\nabla g_j(p)$.
+ Lagrangian: $\mathcal{L}=f-\sum_j\lambda_jg_j$; the sign convention changes the signs of the multipliers but not the candidate points.
+ Value function: $M(c)$ is the optimal value of $f$ on $\{g=c\}$.

## Mathematical claims and justification

+ **Tangency.** At a constrained extremum, the derivative of $f$ along every admissible curve through $p$ vanishes. Complete proof via the one-variable Fermat theorem applied to $t\mapsto f(\gamma(t))$.
+ **Tangent space.** Under $\nabla g(p)\neq0$, the constraint set is locally a smooth hypersurface and $T_pS=\ker Dg(p)$. The article states this as the relevant consequence of the implicit function theorem; it does not reprove the theorem.
+ **Multiplier theorem.** $\nabla f(p)$ annihilates $T_pS$, so it lies in the orthogonal complement of $\ker Dg(p)$, which is $\operatorname{span}\{\nabla g(p)\}$. Complete proof conditional on the tangent-space statement.
+ **Several constraints.** The orthogonal complement of $\bigcap_j\ker Dg_j(p)$ is $\operatorname{span}\{\nabla g_j(p)\}$ when the gradients are linearly independent. Complete argument; the rank condition is exactly the hypothesis needed for the span to have dimension $m$.
+ **Sensitivity.** If $p(c)$ is differentiable, $g(p(c))=c$ gives $\nabla g(p(c))\cdot p'(c)=1$, and the multiplier equation gives $M'(c)=\nabla f(p(c))\cdot p'(c)=\lambda(c)$. Complete derivation under the stated differentiability assumption.
+ **Failure of the qualification.** $f=x+y$ on $x^2+y^2=0$ has a constrained extremum at the origin, but $\nabla g(0,0)=0$ and no $\lambda$ satisfies $(1,1)=\lambda(0,0)$. Complete counterexample; all hypotheses except the qualification are satisfied.
+ **Circle example.** The Lagrange system gives $x^2=y^2$ and four candidates; the values are $\pm\frac12$. Since the circle is compact, both extrema are attained. Complete.
+ **Plane example.** The Lagrange system gives $\lambda=-4/9$ and the point $(7/9,14/9,23/9)$; the squared distance is $4/9$ and the distance $2/3$, matching the plane-distance formula. Complete.
+ **Two constraints.** The system gives $\mu=0$, $x=y=z=1/3$ and value $1/3$. Complete; the feasible set is a line and the point is the orthogonal projection of the origin.

## Worked examples and independent checks

Run on 2026-11-26 with Python 3; script `work/checks/verify_batch4.py` in the agent workspace, not committed.

+ Circle: the four candidates $(\pm1/\sqrt2,\pm1/\sqrt2)$ satisfy $x^2+y^2=1$; the products are $+1/2$ for equal signs and $-1/2$ for opposite signs.
+ Plane: the point $(7/9,14/9,23/9)$ satisfies $x+2y+2z=9$ exactly; the squared distance is $36/81=4/9$; the plane-distance formula gives $2/3$.
+ Two constraints: $(1/3,1/3,1/3)$ satisfies $x+y+z=1$ and $x-y=0$; the value is $1/3$.
+ Sensitivity: $M(c)=(c-11)^2/9$ gives $M'(9)=-4/9$, equal to the multiplier.
+ Failure example: $x^2+y^2=0$ has the unique real solution $(0,0)$; the gradient of the constraint vanishes there.

These checks support the arithmetic; the proofs in the article are the basis for the general statements.

## Editorial checks

+ Front matter with proposed canonical URL and CC BY-NC 4.0.
+ Only H2 headings, sentence case; no H1 in the body.
+ Five tagged equations, all referenced in the text.
+ British spellings: "optimisation", "behaviour" (not used), "recognise" (not used), "parametrising" (not used in the final text).
+ Site-relative link: `../implicit-function-theorem/` is a sibling in this batch and is an unpublished dependency at the time of writing. The article does not link to a non-existent route.
+ No SVG or image placeholders.

## Limitations

+ The tangent-space statement is quoted from the implicit function theorem rather than proved again in this article.
+ The sensitivity formula assumes that the optimal point depends differentiably on the constraint level; this is not proved here.
+ Inequality constraints are mentioned only to delimit the scope; no Karush-Kuhn-Tucker theory is developed.
+ No LaTeX renderer was available; rendering was checked by delimiter inspection.

## Tool checks actually performed

+ Searched upstream filenames and bodies for duplicate coverage.
+ Fetched and read OpenStax §4.8 and Paul's Notes §14.5.
+ Ran the Python checks above.
+ Checked headings, delimiters, tags and front matter by script.
