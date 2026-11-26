# Illustration notes — Lagrange Multipliers

Batch: `20261126T222013Z-01` · Article: `multivariable-calculus/lagrange-multipliers.md`

## F1 — `svg/lagrange-multipliers-1.svg`

- **Claim.** At a constrained extremum the level curve of \(f\) is tangent to the constraint, so \(\nabla f\) and \(\nabla g\) are parallel. For \(f=xy\) on \(x^2+y^2=1\), they point the same way at the maximum \(p_{\max}\) and opposite ways at the minimum \(p_{\min}\).
- **Anchor.** After “The tangency picture is a guide, not a proof…”, before “The multiplier theorem”.
- **Construction.** Equal-aspect plane, 88 px per unit, unit circle of radius 88 px. Level curves \(xy=\pm0.25,\pm0.5\) are sampled from \(y=c/x\). At \(p_{\max}=(1/\sqrt2,1/\sqrt2)\), \(\nabla f=(y,x)\) and \(\nabla g=(2x,2y)\) are drawn on the same ray with lengths proportional to their norms (22 px per unit); at \(p_{\min}=(1/\sqrt2,-1/\sqrt2)\) they are drawn on opposite rays. The \(g\)-arrows are dashed, the \(f\)-arrows solid.
- **Departures from brief.** The brief asked for \(p_{\max}\) and \(p_{\min}\) to be labelled; only those two of the four symmetric candidates are marked and labelled, to keep the tangency arrows readable.
- **Checks.** \(\nabla f(p_{\max})=(1/\sqrt2)(1,1)\), \(\nabla g(p_{\max})=\sqrt2(1,1)\); \(\nabla f(p_{\min})=(1/\sqrt2)(-1,1)\), \(\nabla g(p_{\min})=\sqrt2(1,-1)\). Rendered at 680 px and 240 px and inspected.

## F2 — `svg/lagrange-multipliers-2.svg`

- **Claim.** The constrained extrema of \(f=xy\) on the unit circle are the highest and lowest points of the circle lifted onto the surface \(z=xy\).
- **Anchor.** After the sentence giving the maximum \(1/2\) and minimum \(-1/2\), before “Distance to a plane”.
- **Construction.** The surface \(z=xy\) on \(-1\le x,y\le1\) is a translucent sheet with a \(4\times4\) mesh. The lifted curve is \((\cos t,\sin t,\cos t\sin t)\), sampled at 200 points. The unit circle at \(z=0\) is dashed for reference; short vertical guides join the labelled extrema to it. The projection \(x\mapsto(33.94x,33.94x)\), \(y\mapsto(-33.94y,33.94y)\), \(z\mapsto(0,-45z)\) was chosen so that the lifted circle projects to a simple closed loop rather than a self-crossing figure. The brief's “y into the page and to the left” is realised with \(y\) receding left and downward; both \(x\) and \(y\) recede from the viewer, which gave the clean loop.
- **Checks.** At \(t=\pi/4\), \(z=1/2\); at \(t=3\pi/4\), \(z=-1/2\); the four marked points are the two maxima and two minima. Rendered at 680 px and 240 px and inspected.

## F3 — `svg/lagrange-multipliers-3.svg`

- **Claim.** With independent constraints \(g_1=x+y+z-1=0\) and \(g_2=x-y=0\), the feasible set is their intersection line, and at the minimiser \(\nabla f\) lies in the span of \(\nabla g_1,\nabla g_2\).
- **Anchor.** After “The point found is the orthogonal projection… global minimum”, before “The multiplier as a sensitivity”.
- **Construction.** The two planes are clipped to the box \([-0.5,1.5]^3\) by half-space clipping and drawn translucent. The feasible line is \(x=y\), \(z=1-2x\) with \(x\in[-1/4,3/4]\). At \(p=(1/3,1/3,1/3)\), \(\nabla g_1=(1,1,1)\), \(\nabla g_2=(1,-1,0)\) and \(\nabla f=(2/3,2/3,2/3)\); arrows have lengths proportional to the vector norms. The relation \(\nabla f=\frac23\nabla g_1+0\cdot\nabla g_2\) is printed in the figure.
- **Checks.** \(g_1(p)=g_2(p)=0\); \(\operatorname{rank}Dg(p)=2\); \(f(p)=1/3\). Rendered at 680 px and 240 px and inspected.
