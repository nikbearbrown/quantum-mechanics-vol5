# CAJAL Figure Report — Module M-12 — Matrices, Determinants, and Linear Systems

Recommended: 3 figures, Mixed density.

---

## Figure 1 — Three Conjugate Operations on a Complex Matrix: $A^*$, $A^T$, $A^\dagger$

**Heuristic:** VG — Verification Gap
**Rank:** Critical

---

**BLOCK 1 — ILLUSTRAE PASTE BLOCK:**

Draw a three-panel comparison diagram showing a single source 2×2 complex matrix in the center and three derived matrices arranged around it, each produced by one of the three conjugation operations. The source matrix panel sits at left center, represented as a 2×2 grid with four cells filled with distinct abstract geometric markers (circles, squares, triangles, stars) to indicate complex entries without using numbers. The top branch leads to the complex-conjugate result panel: same grid layout, same positions, but the geometric markers are shown in a mirrored/inverted form representing conjugation with no transposition. The middle-right branch leads to the transpose result panel: the grid is the same but the markers have swapped positions across the main diagonal (upper-right and lower-left exchange). The bottom branch leads to the Hermitian-conjugate result panel: both conjugation and transposition are applied — the markers occupy the transposed positions and appear in the conjugated form. Connect each derived panel to the source with a directional arrow. Mark the Hermitian-conjugate arrow as the thickest (2pt) to indicate it is the QM-primary operation. Use Sky Blue for the source panel border, Orange for the $A^*$ branch, Blue for the $A^T$ branch, and Bluish Green for the $A^\dagger$ branch and its border. Flat vector, Okabe-Ito palette, white background, uniform 1pt strokes (2pt for $A^\dagger$ arrow), no baked text.

---

**BLOCK 2 — FULL SCOPE:**

- `[S — SPECIFICATION]` Single-column 89 mm width, 300 DPI, vector (SVG/EPS), white background, hub-and-spoke layout with source matrix at left and three derived matrices branching right.

- `[C — CONTENT]` Source matrix: 2×2 grid, four cells each carrying a distinct abstract shape (not a number or letter) representing a complex entry. Three derived panels: (1) $A^*$ — same grid, shapes modified to indicate conjugation (e.g., shape interior filled vs. hollow), no positional change; (2) $A^T$ — shapes in transposed positions (off-diagonal pair swapped), no modification of shape form; (3) $A^\dagger$ — shapes in transposed positions AND in conjugated form. Directional arrows from source to each derived panel. Relative stroke weight distinguishes $A^\dagger$ as primary. No algebraic notation, no index labels, no specific matrix entries.

- `[O — ORGANIZATION]` Source panel: left-center. $A^*$ panel: upper right, connected by upper diagonal arrow. $A^T$ panel: middle right, connected by horizontal arrow. $A^\dagger$ panel: lower right, connected by lower diagonal arrow. All derived panels are the same size as the source. Arrow angles are symmetric above and below the horizontal. The three derived panels align vertically on the right side of the figure.

- `[P — PRESENTATION]` Flat vector. Sky Blue `#56B4E9` border on source matrix panel. Orange `#E69F00` arrow and border for $A^*$. Blue `#0072B2` arrow and border for $A^T$. Bluish Green `#009E73` arrow (2pt) and border for $A^\dagger$. Light gray fill for all grid cells. Uniform 1pt strokes for all elements except the $A^\dagger$ arrow (2pt). White background. No baked text.

- `[E — EXCLUSIONS]` Omit: Hermitian property ($A^\dagger = A$), unitary property, eigenvalue content, specific matrix entries (numerical or symbolic), $n \times n$ for $n > 2$, the real-symmetric special case arrow, trace or determinant indicators.

---

**BLOCK 3 — NEGATIVE PROMPT:**

numerical matrix entries, algebraic index notation, eigenvalue arrows, unitary property diagram, Hermitian-equals-self indicator, real-symmetric equivalence note, n×n grid for n>2, trace or determinant formula panels, text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, dual-headed arrows, hand-drawn styles, human figures, visual clutter, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 2 — The Bloch Sphere: Pure States on the Surface, Mixed States in the Interior

**Heuristic:** VG — Verification Gap
**Rank:** Critical

---

**BLOCK 1 — ILLUSTRAE PASTE BLOCK:**

Draw a schematic cross-sectional diagram of the Bloch sphere as a flat circle (not a 3D sphere). The circle's boundary represents the surface where pure states live; the interior represents the mixed-state region. Draw three labeled anchor points on the boundary: one at the north pole, one at the south pole, and one at a general point on the equator. Draw one point strictly inside the circle representing a mixed state, connected to the center by a vector arrow. Draw the center point itself, representing the maximally mixed state. A thin vertical dashed axis runs from south pole through center to north pole. Indicate the radial distance from center to surface as a single-headed arrow pointing outward from center to the equator boundary. Color the boundary circle stroke Bluish Green; the interior region with a very light Bluish Green fill (10% opacity); the pure-state boundary points as solid Blue filled circles; the interior mixed-state point as an open Orange circle with Orange fill (50% opacity); the center point as a solid Reddish Purple filled circle; the axis dashed line neutral gray; the radial vector arrow Blue. Flat vector, Okabe-Ito palette, white background, uniform 1pt strokes, no baked text.

---

**BLOCK 2 — FULL SCOPE:**

- `[S — SPECIFICATION]` Single-column 89 mm width, 300 DPI, vector (SVG/EPS), white background, single circular cross-section with three marked boundary points, one interior point, one center point, one axis, and one radial arrow.

- `[C — CONTENT]` Bloch sphere cross-section (flat circle). Boundary: represents $|\mathbf{r}| = 1$ (pure states). Three boundary points: north pole ($|{\uparrow}\rangle$-direction), south pole ($|{\downarrow}\rangle$-direction), equatorial point (arbitrary mixed-angle pure state). One interior point: represents a mixed state with $|\mathbf{r}| < 1$. Center: represents maximally mixed state $\rho = I/2$, $\mathbf{r} = \mathbf{0}$. Radial vector from center to the interior mixed-state point represents the Bloch vector $\mathbf{r}$. Vertical dashed axis from south to north pole represents the $z$-axis of spin measurement. No Pauli matrix labels, no coordinate axes other than the vertical spin axis, no great circles, no longitude/latitude lines.

- `[O — ORGANIZATION]` Single large circle centered in the figure. Dashed vertical axis through center, extending slightly beyond the circle boundary at top and bottom. North-pole point at top of circle; south-pole point at bottom; equatorial point at right edge. Interior mixed-state point placed at roughly 50% radius in the upper-right quadrant. Radial arrow from center to interior point. Center point marked distinctly from interior point.

- `[P — PRESENTATION]` Flat vector. Bluish Green `#009E73` for circle boundary stroke (1.5pt). Very light Bluish Green `#009E73` at 10% fill opacity for interior region. Blue `#0072B2` solid circles for pure-state boundary points (5pt diameter). Orange `#E69F00` open circle with 50% fill for mixed-state interior point. Reddish Purple `#CC79A7` solid circle for center/maximally-mixed point. Blue `#0072B2` single-headed arrow for Bloch vector. Neutral gray dashed line for vertical axis. Uniform 1pt strokes. White background. No baked text.

- `[E — EXCLUSIONS]` Omit: coordinate axis labels ($x$, $y$, $z$), qubit state labels, Pauli matrix symbols, purity formula, longitude/latitude grid lines, great circles, equatorial plane hatching, rotation axes, time-evolution trajectory, gate action arrows, specific Bloch vector coordinates.

---

**BLOCK 3 — NEGATIVE PROMPT:**

coordinate axis labels, qubit ket notation, Pauli matrix symbols, purity formula annotation, longitude latitude grid, great circle arcs, equatorial plane hatch, rotation trajectory curves, gate-action arrows, specific Bloch vector components, text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, dual-headed arrows, hand-drawn styles, human figures, visual clutter, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 3 — Pauli Matrix Commutation Cycle

**Heuristic:** VG — Verification Gap
**Rank:** Important

---

**BLOCK 1 — ILLUSTRAE PASTE BLOCK:**

Draw a cycle diagram with three equally spaced nodes arranged in a triangle, each node representing one of the three Pauli operators. Connect the nodes with three curved directional arrows forming a clockwise cycle. Each arrow runs from one node to the next in the cyclic order (x → y → z → x), indicating the commutation result at the arrowhead. No text or letter labels appear anywhere. The arrowheads and the nodes should be the only elements. The three nodes are differentiated by distinct Okabe-Ito fill colors: the x-node is Orange, the y-node is Bluish Green, the z-node is Blue. The three cycle arrows are drawn in Reddish Purple to indicate the commutation relationship. Each arrow is a smooth arc running outside the straight edge between the two nodes. Flat vector, Okabe-Ito palette, white background, uniform 1pt strokes for node borders and 1.5pt for cycle arrows, no baked text.

---

**BLOCK 2 — FULL SCOPE:**

- `[S — SPECIFICATION]` Single-column 89 mm width, 300 DPI, vector (SVG/EPS), white background, equilateral triangle arrangement of three circular nodes with three external curved arrows forming a directed cycle.

- `[C — CONTENT]` Three nodes representing the three Pauli operators, differentiated by color only (no labels). Three curved directed arrows forming a single clockwise cycle: x-node → y-node → z-node → x-node. The directed arrows represent the commutation cycle $[\sigma_x, \sigma_y] \propto \sigma_z$, $[\sigma_y, \sigma_z] \propto \sigma_x$, $[\sigma_z, \sigma_x] \propto \sigma_y$ — a cyclic triadic relationship. No anticommutation, no identity matrix node, no eigenvalue content.

- `[O — ORGANIZATION]` Equilateral triangle layout. Top node: z (Blue). Lower-left node: x (Orange). Lower-right node: y (Bluish Green). Cycle arrows follow the clockwise direction: top → lower-right → lower-left → top. Arrows are external arcs (do not pass through the interior of the triangle). Node circles are uniform diameter (approximately 12mm at final print size). Arrow arcs have a consistent curvature radius.

- `[P — PRESENTATION]` Flat vector. Orange `#E69F00` fill for x-node. Bluish Green `#009E73` fill for y-node. Blue `#0072B2` fill for z-node. Reddish Purple `#CC79A7` for the three cyclic directional arrows (1.5pt stroke). Neutral gray `#AAAAAA` for node border strokes (1pt). White background. No baked text. No gradient fills.

- `[E — EXCLUSIONS]` Omit: identity matrix node, anticommutation arrows (do not add second arrow set for $\{\sigma_i, \sigma_j\}$), eigenvalue ±1 markers, Bloch sphere, spin-state column vectors, numeric factor $2i$, Levi-Civita symbol representation, counter-clockwise cycle arrows.

---

**BLOCK 3 — NEGATIVE PROMPT:**

identity matrix node, anticommutation arrow set, eigenvalue markers, Bloch sphere outline, spin-state vectors, counter-clockwise cycle arrows, Levi-Civita diagram, numeric coefficient labels, text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, dual-headed arrows, hand-drawn styles, human figures, visual clutter, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Video Candidate Pass

**Figure 1 — Three Conjugate Operations:**
STATIC SUFFICIENT. The three operations are parallel transformations on the same source object — they do not build on each other causally. The comparison is most useful with all four panels visible simultaneously for direct inspection of what changes and what stays fixed.

**Figure 2 — Bloch Sphere:**
STATIC SUFFICIENT. The Bloch sphere is a spatial representation of state space, not a temporal process. The key insight (pure states on the surface, mixed states inside, center = maximally mixed) is a structural claim fully communicated by the annotated cross-section.

**Figure 3 — Pauli Commutation Cycle:**
VIDEO CANDIDATE. Criterion: cyclical where return-to-start matters — the commutation cycle $[\sigma_x, \sigma_y] \propto \sigma_z \to [\sigma_y, \sigma_z] \propto \sigma_x \to [\sigma_z, \sigma_x] \propto \sigma_y \to$ back to start is exactly the kind of closed algebraic loop where a static diagram can be misread as three independent facts rather than one cyclic identity. Recommended video for the module: animate Figure 3, lighting each arc of the cycle in sequence to make the closed-loop character of the SU(2) algebra explicit. One recommended video total for the module.
