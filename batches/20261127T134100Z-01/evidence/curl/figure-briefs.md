# Figure briefs — Curl

Article: `multivariable-calculus/curl.md`
Batch: `20261127T134100Z-01`

## F1 — Circulation around a small rectangle

+ Target heading: "Circulation density"
+ Insertion anchor: after "The vector (2) combines the three plane densities, and its direction is the axis about which the local circulation is greatest."
+ Mathematical claim: for a counterclockwise rectangle in the $xy$-plane, the circulation is approximately $(Q_x-P_y)\Delta x\Delta y,$ so the scalar curl is the circulation per unit area.
+ Objects: a rectangle with corners $(x,y),$ $(x+\Delta x,y),$ $(x+\Delta x,y+\Delta y),$ $(x,y+\Delta y);$ four oriented edge arrows, counterclockwise; sample field arrows near the rectangle showing the $x$-component increasing with $y$ and the $y$-component increasing with $x.$
+ Labels: $x,$ $y,$ $\Delta x,$ $\Delta y,$ $P,$ $Q,$ and the four edges labelled bottom, right, top, left.
+ Construction: make the top edge field arrow visibly stronger than the bottom edge, and the right edge stronger than the left, so that the net circulation is positive. Use a dashed rectangle for the limiting shrink.
+ Distinction: schematic; the field arrows are sampled, not drawn at every point.
+ Shading: light tint inside the rectangle; one accent colour for the oriented boundary.
+ Alt text: "A small counterclockwise rectangle with field arrows on its four edges, illustrating circulation per unit area."

## F2 — Rigid rotation and shear compared

+ Target heading: "Rigid rotation and shear"
+ Insertion anchor: after "A paddlewheel with its axis along $z$ turns clockwise: the upper arrows push harder than the lower ones."
+ Mathematical claim: the rotational field $\langle-\omega y,\omega x,0\rangle$ has curl $2\omega\mathbf{k},$ while the shear field $\langle y,0,0\rangle$ has curl $-\mathbf{k};$ both turn a paddlewheel, even though only the first has circular arrows.
+ Objects: two panels. Left: circular arrows of $\langle-y,x,0\rangle$ with a small paddlewheel at the centre, axis along $z,$ turning counterclockwise. Right: horizontal parallel arrows of $\langle y,0,0\rangle$ whose length increases upward, with a paddlewheel at the centre turning clockwise.
+ Labels: $\omega,$ $\operatorname{curl}\mathbf{F}=2\omega\mathbf{k},$ $\operatorname{curl}\mathbf{F}=-\mathbf{k},$ and $z$ pointing out of the page.
+ Construction: draw the paddlewheel as a small cross with four vanes. In the left panel the vanes align with the flow; in the right panel the upper vane is pushed more strongly than the lower one. Use the same wheel size in both panels.
+ Distinction: the right panel must not show circular arrows; the point is that parallel flow can still have curl.
+ Shading: none; the wheel is a line drawing, with a curved arrow indicating its rotation.
+ Alt text: "A paddlewheel in a circular flow and in a shear flow with parallel arrows, both turning but in opposite senses."

## F3 — Stokes' theorem: one boundary, two spanning surfaces

+ Target heading: "Stokes' theorem"
+ Insertion anchor: after "It also shows that the surface integral depends only on the boundary: two surfaces with the same oriented boundary give the same flux of curl, provided both satisfy the hypotheses."
+ Mathematical claim: the flux of $\operatorname{curl}\mathbf{F}$ through any oriented surface spanning $C$ equals the circulation of $\mathbf{F}$ around $C,$ with the orientation induced by the right-hand rule.
+ Objects: a closed curve $C$ in a horizontal plane; the flat disk $S_1$ spanning it; a curved cap $S_2$ above it with the same boundary; normal arrows $\mathbf{n}_1$ upward and $\mathbf{n}_2$ upward-ish, both consistent with the counterclockwise orientation of $C.$
+ Labels: $C=\partial S_1=\partial S_2,$ $S_1,$ $S_2,$ $\mathbf{n}_1,$ $\mathbf{n}_2,$ and a right-hand icon or curved arrow indicating the induced orientation.
+ Construction: draw $C$ as an ellipse in perspective, the disk as a flat shaded ellipse, and the cap as a dome above it. Indicate the boundary orientation with arrows on $C$ that agree with both normals. Do not draw the normals in opposite senses.
+ Distinction: schematic; the two surfaces must share exactly the same boundary curve, not merely the same endpoint.
+ Shading: light tint on the disk, a lighter tint on the cap, with the shared boundary in a strong stroke.
+ Alt text: "A closed curve bounding both a flat disk and a curved cap, with consistent normals and boundary orientation for Stokes' theorem."
