# Illustration notes — Double Integrals

Article: `multivariable-calculus/double-integrals.md`

## double-integrals-1.svg — partition of a rectangle

- **Claim:** a partition of $R=[a,b]\times[c,d]$ into $mn$ subrectangles with one sample point each produces the Riemann sum in (1).
- **Anchor:** after "…the area of a small rectangle is the product of its side lengths in either order."
- **Construction:** plan view, equal scale 58 px per unit, $R=[0.5,3.5]\times[0.5,2.5]$ drawn clear of the axes; dashed grid at one interior division in each direction; cell $R_{ij}$ shaded, sample point at $(1.98,2.02)$; dimension marks for $\Delta x_i$ under the cell and $\Delta y_j$ to its right; $\Delta A_{ij}=\Delta x_i\Delta y_j$ in the caption line.
- **Departure:** the brief's optional oblique inset of the box of height $f$ was dropped; it duplicates the volume reading already carried by figure 1 of the triple-integral entry and crowds a plan-view diagram.
- **Checks:** as common; the cell is 58×58 px so the sample dot and both dimension marks stay clear of the grid.

## double-integrals-2.svg — type I and type II regions

- **Claim:** the same region is swept by vertical segments between $g_1(x)$ and $g_2(x)$ (type I) and by horizontal segments between $h_1(y)$ and $h_2(y)$ (type II).
- **Anchor:** after "The description is a computational convenience, not a classification of integrable sets."
- **Construction:** one ellipse of semi-axes 1.0 and 0.72 used as the lens, equal scale 48 px per unit in both panels; three slices per panel with a heavier representative slice; boundary labels $g_1,g_2$ outside the right of panel (a), $h_1,h_2$ below panel (b) with leaders to the boundary points at $y=1.30$.
- **Departure:** the brief asked for a lens between two arbitrary graphs; an ellipse is used because it is closed, has exact left/right inverses for the horizontal slices, and keeps the two panels visibly the same region. Panel letters are "(a) type I" and "(b) type II" as briefed.
- **Checks:** slice endpoints computed from the ellipse, so every segment is a chord of the shaded region; no slice crosses the boundary.

## double-integrals-3.svg — reversing the order

- **Claim:** $D=\{0\le x\le1,\ x\le y\le1\}=\{0\le y\le1,\ 0\le x\le y\}$, and integrating first in $x$ avoids $\int e^{y^2}dy$.
- **Anchor:** after "…the condition $x\le y$ gives $0\le x\le y$."
- **Construction:** equal scale 186 px per unit square; triangle above $y=x$ shaded; horizontal strip at $y=0.62$ from $x=0$ (open dot, included boundary) to the diagonal with an arrow; "y = x" rotated along the diagonal; "D" label inside.
- **Checks:** the strip ends exactly on the diagonal; the two endpoint labels sit below the strip and clear of the rotated diagonal label.

## Checks

- XML parsed; width/height match the viewBox; every `aria-labelledby` target exists; all IDs unique; no scripts, external references, embedded rasters or non-finite geometry; live `<text>` throughout.
- Rendered in headless Chrome at 2× intrinsic size and again at 240 px width; each render was inspected for clipping, overlap, legibility and agreement with the article's equations.
- Palette: the skill's canonical monochrome (`#312F2F`, `#BEB8B7`, `#636060`, `#E9E3E2`, `#E2DFDD`, `#979797`). The briefs' "one accent colour" line predates that palette; the accent is carried by weight and tone instead of hue.
- 3D figures use one shared cabinet axonometric (`u = x + 0.55y`, `v = z + 0.30y`, x right, y receding up-right, z up). The briefs' "x lower right, y lower left" was not used because it puts the origin at the back-top corner and hides the first octant; the cabinet view keeps the labelled faces visible. This is recorded per figure below where it matters.
