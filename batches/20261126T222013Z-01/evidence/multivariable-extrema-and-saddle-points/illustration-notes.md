# Illustration notes — Multivariable Extrema and Saddle Points

Batch: `20261126T222013Z-01` · Article: `multivariable-calculus/multivariable-extrema-and-saddle-points.md`

## F1 — `svg/multivariable-extrema-and-saddle-points-1.svg`

- **Claim.** The graph of \(z=x^2-y^2\) has a critical point at the origin that is neither a maximum nor a minimum: the section \(y=0\) is the upward parabola \(z=x^2\), the section \(x=0\) is the downward parabola \(z=-y^2\).
- **Anchor.** After the paragraph ending “along the \(y\)-axis it falls”, before the Fermat paragraph in “Critical points”.
- **Construction.** Axonometric projection \(x\mapsto(52x,15x)\), \(y\mapsto(-38y,-14y)\), \(z\mapsto(0,-30z)\), origin at \((170,130)\), domain \(-1.4\le x,y\le1.4\). Surface sampled on a \(12\times12\) grid, filled uniformly and overlaid with six constant-coordinate curves in each direction. Both traces are computed from the equations at 81 samples.
- **Scale.** True relative \(x,y\) scale; vertical scale chosen to fit the \(340\times240\) frame. No numeric \(x,y\) ticks were kept because they collided with the sheet; the \(z\) scale is marked at \(-1\) and \(1\).
- **Checks.** XML valid; no external references; traces pass through \((0,0)\); the upward trace has \(z=1.96\) at \(x=\pm1.4\) and the downward trace has \(z=-1.96\) at \(y=\pm1.4\). Rendered in headless Chrome at 680 px and 240 px and inspected.

## F2 — `svg/multivariable-extrema-and-saddle-points-2.svg`

- **Claim.** The level curves of \(f(x,y)=x^3+y^3-3xy\) show a saddle at \((0,0)\), where the level curve \(f=0\) crosses itself, and a local minimum at \((1,1)\), surrounded by closed level curves.
- **Anchor.** After “The gradient vanishes at both, but the Hessian assigns them different characters”, before “When the determinant vanishes”.
- **Construction.** Marching squares on a \(360\times360\) grid over \(-1.8\le x,y\le2.4\), with contour polylines joined through shared grid-edge keys and Douglas–Peucker simplification at \(0.004\) data units (about 0.25 px). Equal aspect, 60 px per unit. Levels \(-0.5,0,0.5,1,2,3\); \(f=0\) is drawn heavier. The critical values are \(0\) and \(-1\), so the brief's suggested \(c=-2,-3\) were omitted: the global minimum is \(-1\), and those levels are empty.
- **Checks.** \(f(0,0)=0\), \(f(1,1)=-1\); the \(f=0\) curve passes through the origin and \((1.5,1.5)\); the \(c=-0.5\) curve is closed around \((1,1)\); \(f_x=3x^2-3y\), \(f_y=3y^2-3x\) vanish only at \((0,0)\) and \((1,1)\). Rendered at 680 px and 240 px and inspected; no clipping.

## F3 — `svg/multivariable-extrema-and-saddle-points-3.svg`

- **Claim.** Four functions with a critical point at the origin and a degenerate Hessian there have four different characters: \(x^4+y^4\) a minimum, \(-x^4-y^4\) a maximum, \(x^4-y^4\) a saddle, \(x^2+y^3\) a saddle.
- **Anchor.** After the table, before “For \(x^4+y^4\), the function is non-negative…”.
- **Construction.** Four panels with the same axonometric projection and the same vertical scale \(18\) px per unit, domain \(-1\le x,y\le1\). Each surface is a uniform translucent sheet with a \(4\times4\) constant-coordinate mesh; the origin is marked. The \(x,y\) axes lie under the sheet so they remain subordinate.
- **Checks.** All four Hessians at the origin have determinant zero: zero matrix for (a)–(c), \(\operatorname{diag}(2,0)\) for (d). The fourth surface visibly rises in \(x\) and falls in \(-y\). Rendered at 680 px and 240 px and inspected; captions do not touch the divider lines.
