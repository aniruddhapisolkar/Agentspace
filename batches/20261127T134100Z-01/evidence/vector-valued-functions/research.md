# Research evidence — Vector-Valued Functions

Batch: `20261127T134100Z-01`
Slug: `vector-valued-functions`
Article: `multivariable-calculus/vector-valued-functions.md`
Category: `multivariable-calculus` (provisional)
Research date: 2026-11-27

## Coverage check

The upstream `antoniolupetti/algebrica` tree was searched by filename and body text for "vector-valued", "vector function", "space curve", "helix", "parametric curve" and "curvature".

+ No article defines vector-valued functions of one parameter or develops their calculus.
+ `vectors-and-matrices/vectors.md` introduces vectors, components, dot and cross products, but treats them as static objects, not as functions of a parameter.
+ `integrals/arc-length-of-a-curve.md` treats arc length of a planar curve given by a function or parametric equations. It supplies a prerequisite, not a duplicate: it does not define the derivative of a vector-valued function, the unit tangent, curvature in space, or componentwise integration.
+ No upstream article covers helices or space curves.

Conclusion: not a duplicate. The arc-length entry is linked as the one-dimensional antecedent. Open issues and pull requests were not inspected; no claim is made about planned upstream work.

## Scope and reader contract

After reading the article, the reader can:

+ define a vector-valued function, its component functions, domain and image curve;
+ distinguish a parameterization from the geometric curve and explain orientation;
+ compute componentwise limits, derivatives and integrals;
+ state and use the product rules for dot and cross products;
+ compute speed, arc length, the arc-length function and curvature;
+ derive the tangent line and unit tangent at a regular point;
+ explain why a vanishing derivative can produce a cusp;
+ decompose acceleration into tangential and normal components;
+ avoid confusing a vector-valued function with a vector field.

Assumed prerequisites: [vectors](../vectors/), one-variable differentiation and integration, [partial derivatives](../partial-derivatives/) (only for the comparison with fields), and [arc length of a curve](../arc-length-of-a-curve/). Exclusions: Frenet–Serret frames beyond the normal component, torsion, surfaces parameterized by two variables, and the general theory of curves.

## Sources consulted

1. OpenStax, *Calculus Volume 3*, §3.1 "Vector-Valued Functions and Space Curves" and §3.2 "Calculus of Vector-Valued Functions".
   URLs: https://openstax.org/books/calculus-volume-3/pages/3-1-vector-valued-functions-and-space-curves and https://openstax.org/books/calculus-volume-3/pages/3-2-calculus-of-vector-valued-functions
   Accessed: 2026-11-27. Full text read.
   Supports: component form and unit-vector notation, the helix as the standard space curve, componentwise limits and continuity, the definition of the derivative, differentiation rules including dot and cross products, the tangent line, speed, arc length, and componentwise integration.
   Use: definitions, the helix example, the differentiation rules and the motion interpretation.

2. Paul Dawkins, *Paul's Online Math Notes*, Calculus III, "Vector Functions".
   URL: https://tutorial.math.lamar.edu/Classes/CalcIII/VectorFunctions.aspx
   Accessed: 2026-11-27. Full text read.
   Supports: the definition of a vector function, plane and space curves, helices about each axis, and the line segment formula.
   Use: independent confirmation of the helix parameterization and the curve-versus-parameterization distinction. The linked "Calculus with Vector Functions" page returned a not-found page and was not used.

3. Algebrica upstream `integrals/arc-length-of-a-curve.md` and `vectors-and-matrices/vectors.md`.
   URLs: https://algebrica.org/arc-length-of-a-curve/ and https://algebrica.org/vectors/
   Accessed through the upstream clone, 2026-11-27.
   Supports: the house notation for parametric curves, the arc-length integral, and the vector operations used in the product rules.
   Use: internal links and notational consistency.

## Definitions and conventions selected

+ Parameter interval $I\subseteq\mathbb{R}$; curve in $\mathbb{R}^2$ or $\mathbb{R}^3$.
+ Component form $\mathbf{r}(t)=\langle f(t),g(t),h(t)\rangle$; unit-vector form with $\mathbf{i},\mathbf{j},\mathbf{k}$.
+ Derivative $\mathbf{r}'(t)=\langle f'(t),g'(t),h'(t)\rangle$ when the component derivatives exist.
+ Regular or smooth parameterization: $\mathbf{r}'$ continuous and nonzero.
+ Unit tangent $\mathbf{T}=\mathbf{r}'/\lVert\mathbf{r}'\rVert$; curvature $\kappa=\lVert d\mathbf{T}/ds\rVert$.
+ Arc length $L=\int_a^b\lVert\mathbf{r}'\rVert\,dt$; arc-length function $s(t)=\int_a^t\lVert\mathbf{r}'(u)\rVert\,du$.
+ British spelling: "parameterisation" is avoided in favour of the corpus form "parameterization"; "centre", "orthogonal", "nonnegative" used consistently.

## Mathematical claims and justification

+ **Componentwise limit and continuity.** The vector difference $\mathbf{r}(t)-L$ has squared norm $\sum(f_i(t)-L_i)^2$, so it tends to zero exactly when every component difference does. This proves the equivalence and the limit laws.
+ **Componentwise derivative.** The difference quotient is the vector of component difference quotients; a vector limit exists exactly when its components converge. Hence (4).
+ **Tangent line (5).** For $s\neq0$, $\mathbf{r}(t_0)+s\mathbf{r}'(t_0)$ is the line through the point in the direction of the derivative. If $\mathbf{r}'(t_0)\neq\mathbf{0}$, this is the tangent line; if the derivative vanishes, the line degenerates or the direction is not determined.
+ **Product rules (7)–(8).** Expand the difference quotients for the dot and cross products and use bilinearity and continuity of the products. The cross product is antisymmetric, so the order of the two terms must not be swapped.
+ **Chain rule (9).** Componentwise one-variable chain rule.
+ **Constant distance and constant speed.** $\frac{d}{dt}\lVert\mathbf{r}\rVert^2=2\mathbf{r}\cdot\mathbf{r}'$ and $\frac{d}{dt}\lVert\mathbf{v}\rVert^2=2\mathbf{v}\cdot\mathbf{a}$ by (7). These are separate statements: the first characterises motion on a sphere centred at the origin, the second characterises constant speed. An earlier draft conflated them; the final text separates the two and states the circle example correctly.
+ **Arc length (11).** Chord approximation: $\lVert\mathbf{r}(t+\Delta t)-\mathbf{r}(t)\rVert/\Delta t\to\lVert\mathbf{r}'(t)\rVert$ for a $C^1$ curve, and the Riemann sums converge to the integral. The formula assumes the parameterization is continuously differentiable; a merely continuous curve may fail to be rectifiable.
+ **Arc-length function (12).** Fundamental theorem of calculus applied to the continuous speed. If $\lVert\mathbf{r}'\rVert=1$, then $s(t)-s(a)=t-a$.
+ **Helix length.** $\lVert\mathbf{r}'\rVert=\sqrt{a^2+b^2}$ is constant, so one turn has length $2\pi\sqrt{a^2+b^2}$. Verified numerically for $a=2,$ $b=1$: $14.0496294621$ against $2\pi\sqrt5=14.0496294621$.
+ **Curvature formula (15).** Since $\mathbf{T}=\mathbf{r}'/\lVert\mathbf{r}'\rVert$ and $ds/dt=\lVert\mathbf{r}'\rVert$, the chain rule gives $\kappa=\lVert\mathbf{T}'\rVert/\lVert\mathbf{r}'\rVert$. The identity $\lVert\mathbf{r}'\times\mathbf{r}''\rVert=\lVert\mathbf{r}'\rVert^3\kappa$ follows by differentiating $\mathbf{T}$ and using $\mathbf{T}\cdot\mathbf{T}'=0$.
+ **Helix curvature.** Direct cross product gives $\lVert\mathbf{r}'\times\mathbf{r}''\rVert=a\sqrt{a^2+b^2}$ and $\lVert\mathbf{r}'\rVert^3=(a^2+b^2)^{3/2}$, hence $\kappa=a/(a^2+b^2)$. At $b=0$ this is $1/a$, the curvature of a circle. Numerically at $a=2,$ $b=1,$ $t=0.7$: formula $0.4$, cross-product quotient $0.3999999999999999$.
+ **Cusp.** $\mathbf{r}(t)=\langle t^2,t^3\rangle$ has $\mathbf{r}'(0)=\mathbf{0}$; the one-sided unit tangents are $\pm\langle1,0\rangle$, so no tangent direction exists at the origin. The curve is differentiable everywhere, which shows that differentiability alone does not give a tangent line.
+ **Acceleration decomposition (18).** Project $\mathbf{a}$ onto $\mathbf{T}$ and its orthogonal complement. Then $a_T=\mathbf{a}\cdot\mathbf{T}=(\mathbf{v}\cdot\mathbf{a})/\lVert\mathbf{v}\rVert$ and $a_N=\lVert\mathbf{a}-a_T\mathbf{T}\rVert=\lVert\mathbf{v}\times\mathbf{a}\rVert/\lVert\mathbf{v}\rVert$. The identity $a_N=\kappa v^2$ is the standard normal-acceleration formula.
+ **Circular helix check.** For $\mathbf{r}=\langle\cos t,\sin t,t\rangle$, $\mathbf{v}\cdot\mathbf{a}=0$, $\lVert\mathbf{v}\rVert^2=2$ and $\kappa=1/2$, so $a_N=1=\lVert\mathbf{a}\rVert$.
+ **Componentwise integral (16)–(17).** The Riemann sums of a vector-valued function are vectors of component Riemann sums; the FTC applies to each component.

## Independent checks

Python 3 numeric script (ad hoc, outside the repository; no symbolic package installed):

+ helix $a=2,$ $b=1$: one-turn length $14.049629462081453$ against exact $2\pi\sqrt5=14.049629462081453$;
+ curvature of the same helix at $t=0.7$: cross-product quotient $0.3999999999999999$ against exact $2/5=0.4$;
+ component integral: $\pi^2/8=1.2337005501361697$ and $e^{\pi/2}-1=3.8104773809653514$;
+ circular helix $a=b=1$: tangential acceleration $0.0$ and $\lVert\mathbf{a}\rVert=1.0$.

All checks passed. The tangent-line example was checked by substituting the point and direction; the cusp claim was checked from the one-sided limits of $\mathbf{r}'/\lVert\mathbf{r}'\rVert$.

## Limitations

+ No LaTeX renderer, Pandoc or TeX installation is available (`pandoc` and `pdflatex` not found); the Markdown was checked structurally but not rendered.
+ The proposed route `https://algebrica.org/vector-valued-functions/` is not known to be live.
+ The Frenet–Serret frame and torsion are outside scope; the article uses only the principal normal through the acceleration decomposition.
+ Open issues and pull requests in the upstream repository were not inspected.
+ Links to sibling batch articles are unpublished dependencies until this batch is merged.
