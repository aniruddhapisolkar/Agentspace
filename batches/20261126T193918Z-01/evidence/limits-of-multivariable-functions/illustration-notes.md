# Illustration notes — Limits of Multivariable Functions

Batch `20261126T193918Z-01`. Illustrator evidence. Article:
`multivariable-calculus/limits-of-multivariable-functions.md`.

All figures are standalone SVG 1.1, UTF-8, live text, palette `#312F2F` / `#BEB8B7` /
`#636060` / `#E9E3E2` / `#979797`, no external references. Rendered with headless
Chrome at intrinsic size (2×) and inside a 240 px-wide page; inspected visually.

## Figure 1 — `svg/limits-of-multivariable-functions-1.svg`

- Claim: for f(x,y)=xy/(x²+y²), the path y=0 gives 0 and the path y=x gives 1/2, so
  the limit at the origin does not exist.
- Anchor: after “The two approaches give different values, $0$ and $1/2$, so no
  single number can be the limit.”
- Construction: two schematic panels with a shared tone code. Left: punctured
  δ-disc (r=0.55 in domain units, equal x/y scale 52 px per unit) with the x-axis
  path in `#636060` and the y=x path in `#312F2F`; arrowheads computed from the ray
  directions and placed at both sides of the excluded origin, which is an open
  circle. Right: t–f graph with the levels 0 and 1/2 at the same 156 px per unit;
  the segments stop 8 px short of t=0, and t=0 is a dashed line.
- Departures: brief asked for “distinct coloured curves”; the house palette is
  monochrome, so the paths are distinguished by tone (dark vs mid grey) and by
  direct labels carried into the right panel. No hue was added.
- Checks: values 0 and 1/2 are placed on the correct axes; the open origin is not
  drawn as a value; labels do not overlap at 240 px.

## Figure 2 — `svg/limits-of-multivariable-functions-2.svg`

- Claim: 0<‖x−x₀‖<δ ⇒ |f(x)−L|<ε; in R² the punctured δ-ball is a disc without
  its centre.
- Anchor: after “so the punctured ball is a disc with its centre removed.”
- Construction: left, a δ-disc (r=42 px) around x₀ with a marked interior point x
  and a dashed δ-radius; right, a one-variable restriction f(t) with an ε-band
  (half-width 25 px) around L, a removable point at t=x₀ drawn open, and a marked
  interior value f(x) inside the band. The band and disc use the same region fill
  to signal the mapping; the two panels are linked by matching symbols x₀, L and
  the words “domain” / “values of f”.
- Departures: the brief allowed a 2D restriction plus an inset; done as two panels
  instead of a 3D graph, because the disc is the point of the multivariable
  definition and is drawn at readable size.
- Checks: the curve stays inside the band for |t−x₀| small, and the value at t=x₀
  is open while f(x) is marked as an attained value.

## Figure 3 — `svg/limits-of-multivariable-functions-3.svg`

- Claim: z=xy²/(x²+y⁴) tends to 0 along every line through the origin but to 1/2
  along x=y².
- Anchor: after “Hence the limit does not exist, even though all linear approaches
  agree.”
- Construction: exact contour map. Solving xy²/(x²+y⁴)=k gives x=ky², so the level
  sets are parabolas; four of them (k=0.2,0.4,0.6,0.8) are drawn in `#CFC7C6`, the
  ridge k=1 (x=y², value 1/2) in `#312F2F` at 2.2 px, and the two straight lines
  y=±0.65x as steep dashed lines. A small profile inset plots k(x)=x·0.36/(x²+0.36²)
  for y=0.6, showing the ridge height 1/2 at x=y²=0.36. Axes: y horizontal, x
  vertical (82 px per x-unit, 72 px per y-unit; unequal scale, both axes labelled).
- Departures: a filled 3D surface was developed and rejected — the knife-edge
  ridge above x=y² produces hidden-surface artifacts (holes and folds) at this
  size, and the exact contour map states the same claim without them. The profile
  inset replaces the 3D ridge height. This is a documented refinement, not a
  change of the mathematical claim.
- Checks: every level curve is the exact parabola x=ky²; the ridge is labelled
  1/2; the dashed lines are straight and pass through the origin; the inset peak is
  at x=0.36 with value 0.5.
