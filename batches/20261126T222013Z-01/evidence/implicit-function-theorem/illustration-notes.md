# Illustration notes — Implicit Function Theorem

Batch: `20261126T222013Z-01` · Article: `multivariable-calculus/implicit-function-theorem.md`

Numbering follows the article's reading order. The contraction proof appears before “When the hypothesis fails”, so the contraction figure is F2 and the failure panels are F3, although the Writer brief listed the failures second.

## F1 — `svg/implicit-function-theorem-1.svg`

- **Claim.** The unit circle is locally a graph \(y=\varphi(x)\) near \((0,1)\), where \(F_y=2\), but not near \((1,0)\), where \(F_y=0\) and the tangent is vertical.
- **Anchor.** After the paragraph ending “namely \(x=\sqrt{1-y^2}\)”, before “The general statement”.
- **Construction.** Two square panels, equal aspect, circle radius 58 px. Panel (a) highlights the arc over \(x\in[-0.78,0.78]\), marks the interval on the axis and joins its endpoints to the arc with dashed verticals. Panel (b) marks \((1,0)\), draws the vertical tangent dashed, and shows a line \(x=0.9\) meeting the circle twice at open dots.
- **Checks.** \(F_y=2y\), so \(F_y(0,1)=2\) and \(F_y(1,0)=0\); the highlighted arc is exactly the graph of \(\sqrt{1-x^2}\) on the displayed interval. Rendered at 680 px and 240 px and inspected.

## F2 — `svg/implicit-function-theorem-2.svg`

- **Claim.** For fixed \(x\), \(G_x(y)=y-F(x,y)\) is a contraction of \([b-\delta,b+\delta]\) into itself; its graph crosses the diagonal at the unique fixed point \(\varphi(x)\), and the cobweb converges there.
- **Anchor.** After the contraction mapping principle proof ending “hence \(u=v\)”, before “The function \(\varphi\) is continuous”.
- **Construction.** Schematic square with both axes scaled to \([0,1]\), labelled \(b-\delta\) to \(b+\delta\). The displayed contraction is \(G(y)=0.42+0.38y\) (slope \(0.38<1\)), with fixed point \(y=0.42/0.62\approx0.677\). The cobweb starts at \(y_0=0.08\) and runs four iterations.
- **Checks.** \(G\) maps the interval into itself; the fixed point is the intersection with \(z=y\); the cobweb is visibly monotone and convergent. The figure is labelled “schematic, not to scale”. Rendered at 680 px and 240 px and inspected.

## F3 — `svg/implicit-function-theorem-3.svg`

- **Claim.** When \(F_y(0,0)=0\), the zero set can be an isolated point, a pair of crossing branches, or a cusp, and none is a unique differentiable graph \(y=\varphi(x)\) near the origin.
- **Anchor.** After “the nonlinear equation may still have a solution… not controlled by the linear term”, before “Scope and limitations”.
- **Construction.** Three equal square panels on \(-1.2\le x,y\le1.2\). (a) \(F=x^2+y^2\): the single point \((0,0)\). (b) \(F=x^2-y^2\): the lines \(y=\pm x\). (c) \(F=x^2-y^3\): \(y=|x|^{2/3}\), with a dashed vertical tangent at the origin.
- **Checks.** Each displayed zero set satisfies its equation; \(F_y(0,0)=0\) in all three cases; the cusp is not differentiable at \(0\). Rendered at 680 px and 240 px and inspected.
