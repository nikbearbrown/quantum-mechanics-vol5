# CAJAL Figure Report — Module M-08 — Eigenvalues and Diagonalization

Recommended: 3 figures, Mixed density.

---

## Figure 1 — Eigenvectors as Invariant Directions: Stretched vs. Rotated

**Heuristic:** VG — Verification Gap
**Rank:** Critical

---

**BLOCK 1 — ILLUSTRAE PASTE BLOCK**

Draw a two-panel side-by-side comparison showing the action of a linear operator on vectors in a 2D vector space. In the left panel, show a fan of four input arrows from a common origin at evenly spaced angles, and their corresponding output arrows after the operator acts — most are rotated and stretched, changing both length and direction, shown as displaced arrows with a curved transformation arc indicating rotation. In the right panel, isolate two arrows from the same operator: one along the eigenvector direction, shown before and after as two collinear arrows with the output simply longer than the input (a scale mark or ratio tick between them), and a second eigenvector direction in the opposite sense, similarly collinear but with the output arrow pointing in the same direction and again scaled. A small right-angle or alignment tick on the eigenvector arrows signals no rotation. Use flat vector rendering, uniform 1pt strokes, white background, and no baked text.

**BLOCK 2 — FULL SCOPE**

- `[S — SPECIFICATION]` Single-column 89mm width, 300 DPI, vector (SVG/EPS), white background. Two-panel horizontal comparison with shared baseline.
- `[C — CONTENT]` Left panel: 4 general input vectors and their corresponding output vectors after transformation, showing rotation (direction change) and scaling (length change). Curved arc on each output arrow indicates rotation. Right panel: 2 eigenvectors before and after — both remain collinear (no rotation), output is a scaled version of input. Tick mark or scale bracket between input and output lengths signals the eigenvalue scaling. Small alignment indicator (collinearity mark) distinguishes the eigenvector case.
- `[O — ORGANIZATION]` Two equal-width panels side by side. Left panel uses 4 input-output arrow pairs (≤8 elements). Right panel uses 2 input-output eigenvector pairs plus their scaling indicators (≤6 elements). A thin vertical separator line between panels. No axis grid lines.
- `[P — PRESENTATION]` Flat vector, Okabe-Ito. General input vectors: light gray. General output vectors (rotated): Orange `#E69F00`, with curved rotation arc in Vermillion `#D55E00`. Eigenvector input: Sky Blue `#56B4E9`. Eigenvector output (scaled): Blue `#0072B2`. Collinearity tick: Bluish Green `#009E73`. Scale bracket: light gray. Uniform 1pt strokes.
- `[E — EXCLUSIONS]` Omit: characteristic equation, determinant, eigenvalue numerical values, matrix entries, the cross product, 3D vectors, complex eigenvectors, any reference to Hermitian or spectral decomposition.

**BLOCK 3 — NEGATIVE PROMPT**

matrix notation, determinant formula, characteristic polynomial, numerical eigenvalue labels, complex number notation, Hermitian symbol, spectral decomposition, 3D arrows, text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, dual-headed arrows, hand-drawn styles, human figures, visual clutter, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion.

---

## Figure 2 — Diagonalization: Coordinate Change Reveals the Eigenbasis

**Heuristic:** MC — Mechanism/Process
**Rank:** Critical

---

**BLOCK 1 — ILLUSTRAE PASTE BLOCK**

Draw a three-panel horizontal sequence showing the diagonalization process. In the first panel, render a 2D coordinate system with oblique (non-orthogonal) grid lines and a matrix acting on a vector — show the original basis vectors as two non-perpendicular arrows and the operator's matrix as a filled grid of non-zero cells (a small 2×2 array of filled squares, none of which are empty). In the second panel, show the change-of-basis arrow: two new basis arrows that are the eigenvectors, rendered as perpendicular (or at least independent) directions, with P (the eigenvector matrix) indicated by a transformation arc connecting old basis to new basis arrows. In the third panel, show the diagonal matrix: a 2×2 grid of squares where only the two diagonal cells are filled and the off-diagonal cells are empty, alongside a 2D coordinate system in the eigenbasis where the operator stretches along the two axes independently. A left-to-right step sequence connects the three panels. Use flat vector rendering, uniform 1pt strokes, white background, and no baked text.

**BLOCK 2 — FULL SCOPE**

- `[S — SPECIFICATION]` Single-column 89mm width, 300 DPI, vector (SVG/EPS), white background. Three-panel horizontal layout with step arrows.
- `[C — CONTENT]` Step 1: original basis (two non-orthogonal arrows) and a 2×2 matrix grid with all four cells filled (indicating dense coupling). Step 2: transformation arc from old basis to eigenvector basis (two new arrows), with P labeled by a bracket (not baked text). Step 3: diagonal matrix (2×2 grid, only diagonal filled) and eigenbasis coordinate system (two perpendicular arrows, scaling ticks along each). Off-diagonal empty cells visually contrast with filled diagonal cells.
- `[O — ORGANIZATION]` Left-to-right three-panel sequence. Each panel has ≤6 visual elements. Small rightward step arrows between panels. Matrix grids rendered as small squares (filled=non-zero, open=zero) without numerical values. Eigenvector arrows are the dominant element of panels 2 and 3.
- `[P — PRESENTATION]` Flat vector, Okabe-Ito. Original basis arrows: light gray. Eigenvector arrows: Blue `#0072B2`. Filled matrix cells (non-zero): Orange `#E69F00`. Empty off-diagonal cells: white with light gray border. Diagonal cells: Bluish Green `#009E73`. Transformation arc P: Sky Blue `#56B4E9`. Step arrows: light gray. Uniform 1pt strokes.
- `[E — EXCLUSIONS]` Omit: numerical matrix entries, eigenvalue numbers, complex entries, characteristic equation derivation, defective matrices, unitary vs. non-unitary distinction, spectral decomposition formula.

**BLOCK 3 — NEGATIVE PROMPT**

numerical matrix entries, characteristic polynomial, defective matrix Jordan form, unitary symbol, spectral decomposition formula, complex number entries, text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, dual-headed arrows, hand-drawn styles, human figures, visual clutter, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion.

---

## Figure 3 — Spectral Decomposition: Operator as Sum of Eigenvalue-Weighted Projectors

**Heuristic:** VG — Verification Gap
**Rank:** Important

---

**BLOCK 1 — ILLUSTRAE PASTE BLOCK**

Draw a single panel showing the spectral decomposition of a 2D Hermitian operator as a sum of two projector contributions. On the left, show a filled 2×2 matrix grid (both diagonal and off-diagonal cells filled) representing the full operator A. An equals sign leads to a right-hand side showing two additive terms. The first term is a small eigenvalue-scale marker (a stretched tick) multiplied by a 2×2 grid with only the upper-left cell filled (the first projector, rank-1). A plus sign connects to a second term: a second eigenvalue-scale marker (a shorter or longer tick, contrasting with the first) multiplied by a 2×2 grid with only the lower-right cell filled (the second projector, rank-1). To the right of the equation, show the geometric interpretation: two perpendicular eigenvector arrows, each with an oval "lobe" around it (the projector's range), with the first lobe scaled by one tick size and the second by another. Use flat vector rendering, uniform 1pt strokes, white background, and no baked text.

**BLOCK 2 — FULL SCOPE**

- `[S — SPECIFICATION]` Single-column 89mm width, 300 DPI, vector (SVG/EPS), white background. Single panel with algebraic-structure layout on the left and geometric interpretation on the right.
- `[C — CONTENT]` Left: full 2×2 matrix (filled grid) = eigenvalue-scale marker × rank-1 projector grid (one filled cell) + eigenvalue-scale marker × rank-1 projector grid (other filled cell). Right: geometric view — two perpendicular eigenvector arrows from origin, each surrounded by an oval lobe; the lobe for eigenvalue 1 is scaled differently from lobe for eigenvalue 2. Scale markers (length ticks) visually encode the eigenvalues. Total elements: ≤8.
- `[O — ORGANIZATION]` Left side: algebraic decomposition using matrix-cell grid icons. Right side: geometric vector diagram with projector lobes. A vertical separator between algebraic and geometric views. Eigenvalue scaling is conveyed by relative lobe size or tick length, not by numbers.
- `[P — PRESENTATION]` Flat vector, Okabe-Ito. Full operator matrix cells: Blue `#0072B2`. First projector cell: Bluish Green `#009E73`. Second projector cell: Orange `#E69F00`. First lobe: Bluish Green `#009E73`, low-opacity fill. Second lobe: Orange `#E69F00`, low-opacity fill. Eigenvector arrows: Blue `#0072B2`. Scale ticks: Sky Blue `#56B4E9`. Uniform 1pt strokes.
- `[E — EXCLUSIONS]` Omit: numerical eigenvalue values, Dirac notation angle brackets baked in, formula for functions of operators, density matrix, continuous spectrum or delta-function notation.

**BLOCK 3 — NEGATIVE PROMPT**

numerical eigenvalue labels, Dirac notation baked into image, functions-of-operators formula, density matrix symbol, Dirac delta notation, complex spectrum diagram, text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, dual-headed arrows, hand-drawn styles, human figures, visual clutter, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion.

---

## Video Candidate Pass

**Figure 1 — Eigenvectors as Invariant Directions:** STATIC SUFFICIENT. The comparison between rotated general vectors and collinear eigenvectors is a spatial contrast, fully legible side by side. No cyclical process or hidden transition.

**Figure 2 — Diagonalization: Coordinate Change:** VIDEO CANDIDATE. Criterion: ≥3 sequential causal stages, and the transformation mechanism (change of coordinates, matrix goes from dense to diagonal) is the central learning target. Animating the oblique basis morphing into the eigenbasis — while the off-diagonal matrix cells drain and only the diagonal fills — makes the change-of-coordinates interpretation viscerally clear in a way three frozen panels cannot. **Recommended as the single video for this module.**

**Figure 3 — Spectral Decomposition:** STATIC SUFFICIENT. The additive structure of the decomposition is algebraic, not temporal. The projector-lobe geometry is a spatial layout that the reader inspects rather than watches unfold.
