# Illustration notes — Inverse Function Theorem

Batch: `20261126T222013Z-01` · Article: `multivariable-calculus/inverse-function-theorem.md`

## F1 — `svg/inverse-function-theorem-1.svg`

- **Claim.** If \(Df(a)\) is invertible, a small neighbourhood \(V\) of \(a\) is mapped bijectively onto an open neighbourhood \(W\) of \(b=f(a)\), and the inverse \(g\) returns each point of \(W\) to its unique preimage in \(V\).
- **Anchor.** After the paragraph ending “for the small \(V\) it produces”, before “The condition is sufficient, not necessary”.
- **Construction.** Two square panels with equal scale. The schematic map is \(f(x,y)=(x+y^2/4,\;y+x^2/4)\) at \(a=(0,0)\), so \(Df(a)=I\). The left panel shows the square \(V\) with a Cartesian grid; the right panel shows its image \(W\) and the image of the grid as a curvilinear mesh. The highlighted point \(x=(0.55,-0.35)\) maps to \(y=f(x)\). Arrows in the gap are labelled \(f\) and \(g=f^{-1}\).
- **Checks.** \(f(0,0)=(0,0)\); \(Df(0,0)=I\); the image grid is the exact image of the source grid, not a decorative distortion. Rendered at 680 px and 240 px and inspected.

## F2 — `svg/inverse-function-theorem-2.svg`

- **Claim.** Polar coordinates are locally invertible for \(r>0\) because \(\det Df=r\), but not globally injective because \(\theta\) and \(\theta+2\pi\) give the same point.
- **Anchor.** After “on that interval the map is injective”, before “The derivative of the inverse can be read from (1)”.
- **Construction.** Left: the rectangle \(0.5\le r\le1.5\), \(-\pi/2<\theta<\pi/2\) with its Cartesian grid and the point \((r_0,\theta_0)=(1,\pi/4)\). Right: the full annulus \(0.5\le r\le1.5\), with the right half shaded as the image of the displayed rectangle, radial and circular grid lines, the image point, and a dashed circular arrow labelled \(\theta+2\pi\): same point.
- **Departure from brief.** The brief asked for a right half-annulus plus a faint duplicate sector. A full annulus with the right half highlighted was used instead, because \(\theta+2\pi\) returns to the same points rather than to a separate sector; the dashed loop states the periodicity directly.
- **Checks.** \(\det Df=r>0\) on the rectangle; the right half-annulus is exactly the image of the displayed \(\theta\)-interval; \((1,\pi/4)\) maps to \((1/\sqrt2,1/\sqrt2)\). Rendered at 680 px and 240 px and inspected.

## F3 — `svg/inverse-function-theorem-3.svg`

- **Claim.** The graph of the inverse is the reflection of the graph of \(f\) in \(y=x\), so the inverse's tangent slope is the reciprocal; where \(f'=0\) the reflected tangent is vertical and the inverse is not differentiable.
- **Anchor.** After “the conclusion of the theorem fails while a continuous inverse still exists”, before “A linear example”.
- **Construction.** Panel (a): \(f(x)=x^2\) and \(g(y)=\sqrt y\) on a common square, with the tangents at \((1,1)\) of slopes \(2\) and \(1/2\). Panel (b): \(f(x)=x^3\) and \(g(y)=y^{1/3}\), equal scale, with the horizontal tangent at the origin and the vertical tangent of the inverse; labels record \(f'(0)=0\) and “g not differentiable”.
- **Checks.** The curves are exact reflections in \(y=x\); the tangent at \((1,1)\) to \(x^2\) has slope \(2\), and to \(\sqrt y\) has slope \(1/2\); \(f'(0)=0\) and the inverse tangent is the \(y\)-axis. Rendered at 680 px and 240 px and inspected.
