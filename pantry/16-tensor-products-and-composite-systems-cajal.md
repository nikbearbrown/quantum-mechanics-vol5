# CAJAL Figure Report — Module M-16 — Tensor Products and Composite Systems

Recommended: 3 figures, Mixed density.

---

## Figure 1 — Dimension multiplication: direct sum vs. tensor product

**Heuristic:** VG — Verification Gap
**Rank:** Critical

**BLOCK 1 — ILLUSTRAE PASTE BLOCK:**
Draw a side-by-side schematic comparing two ways of combining two 2-dimensional complex vector spaces V and W. On the left panel, show the direct sum V ⊕ W: two separate 2D column vectors stacked into a single 4-component column, with a clear boundary at the midpoint indicating the stack join — the space has dimension 2 + 2 = 4. On the right panel, show the tensor product V ⊗ W: a 2×2 grid of basis-pair slots, each cell labeling one of the four ordered basis pairs (|00⟩, |01⟩, |10⟩, |11⟩ in lexicographic order), the whole grid representing a single flat 4-dimensional space with dimension 2 × 2 = 4. Shade the cells of the tensor-product grid in two tiers: the four product-state cells form the frame of the grid; indicate a set of interior points (not a separate grid cell) floating inside the tensor-product panel to represent the entangled elements — linear combinations that fill the rest of the space but cannot be written as single grid cells. Use arrows from each parent space to each panel showing which construction is being used. Include a numeric dimension label on each panel (sum = 4; product = 4), but distinguish that the structure is fundamentally different.

**BLOCK 2 — FULL SCOPE:**

`[S — SPECIFICATION]` Single-column 89 mm width, 300 DPI, SVG/EPS, white background. Two side-by-side panels of equal width separated by a vertical divider line.

`[C — CONTENT]` Two source spaces V (dim 2) and W (dim 2). Left panel: direct sum V ⊕ W, dimension label 2+2=4, stacked-column representation. Right panel: tensor product V ⊗ W, dimension label 2×2=4, 2×2 grid of product-basis cells labeled |00⟩, |01⟩, |10⟩, |11⟩ in lexicographic order, plus a shaded interior zone indicating entangled (non-product) elements. Arrows from V and W into each panel.

`[O — ORGANIZATION]` Horizontal two-panel layout. Left panel: two rectangles stacked vertically (V on top, W below), joined by a bracket labeled "dim 2+2=4." Right panel: 2×2 grid, rows indexed by V basis, columns by W basis; interior region (lighter shade) inside the grid frame indicates the full span including entangled states. Arrows from shared V and W boxes at the top feed into both panels.

`[P — PRESENTATION]` Flat vector, Okabe-Ito palette, uniform 1 pt strokes, white background, no baked text. Direct-sum stacked column: Sky Blue `#56B4E9` (V block) and Orange `#E69F00` (W block). Tensor-product grid outer frame: Blue `#0072B2`; product-basis cell fill: light gray; entangled-interior fill: Reddish Purple `#CC79A7` at 30% opacity. Connecting arrows: neutral gray.

`[E — EXCLUSIONS]` Omit: density matrices, partial trace, operator Kronecker products, Schmidt decomposition, Bell states. Do not show any algebraic expressions inside the image. Do not represent the spaces as geometric Euclidean planes or Bloch spheres.

**BLOCK 3 — NEGATIVE PROMPT:**
Bloch sphere representation, Euclidean geometry arrows, 3D perspective, density matrix symbols, partial trace notation, Bell-state labels baked into cells, text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, dual-headed arrows, hand-drawn styles, human figures, visual clutter, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion.

---

## Figure 2 — Kronecker product block structure and local-gate composition rule

**Heuristic:** VG — Verification Gap
**Rank:** Critical

**BLOCK 1 — ILLUSTRAE PASTE BLOCK:**
Draw an annotated schematic of the Kronecker product matrix structure. Show a 2×2 matrix A divided into four scalar entries arranged in a 2×2 grid of blocks. In each block position, show a scaled copy of an n×n matrix B, where the scaling factor corresponds to the entry A_ij. Use shading intensity to indicate the magnitude of A_ij — darker blocks for larger entries, lighter blocks for smaller entries — so the block-nested structure is visually apparent. Beneath the main diagram, show a two-step composition: a product of two Kronecker-product operators (A₁⊗B₁)(A₂⊗B₂) represented as two block matrices chained horizontally with a multiplication arrow, then an equals sign and a single block matrix representing (A₁A₂)⊗(B₁B₂), illustrating that local composition on each subsystem is independent. Use distinct colors for the A-type matrices and the B-type matrices to make the nesting hierarchy visually immediate.

**BLOCK 2 — FULL SCOPE:**

`[S — SPECIFICATION]` Single-column 89 mm width, 300 DPI, SVG/EPS, white background. Two stacked panels: top panel for the block structure, bottom panel for the composition identity.

`[C — CONTENT]` Top panel: A is a 2×2 matrix; B is an n×n matrix; the Kronecker product A⊗B is a 2n×2n matrix with four n×n blocks arranged in a 2×2 grid, each block being A_ij·B. Shade each block proportionally to |A_ij|. Bottom panel: the composition identity (A₁⊗B₁)(A₂⊗B₂) = (A₁A₂)⊗(B₁B₂). Use abstract rectangles with color coding rather than actual matrix entries — no numerical values. Use two-color nesting: A-type matrices in Sky Blue `#56B4E9`, B-type matrices (inner blocks) in Orange `#E69F00`.

`[O — ORGANIZATION]` Top panel: outer 2×2 grid in Sky Blue showing A-matrix structure; inner blocks in Orange shaded by |A_ij| intensity (lighter = smaller). Bottom panel: three Kronecker-product matrices separated by a multiplication symbol and an equals sign; color coding consistent with top panel.

`[P — PRESENTATION]` Flat vector, Okabe-Ito palette, 1 pt strokes, white background, no baked text. A-level outer: Sky Blue `#56B4E9`. B-level inner blocks: Orange `#E69F00` graduated from light gray (near zero) to full Orange (large). Composition-panel backgrounds: white with light gray horizontal rule separating the two panels.

`[E — EXCLUSIONS]` Omit: specific gate matrices (do not depict CNOT, H, X, Z by name or structure), entangled states, Bell states, partial trace, density matrices. Do not use any actual matrix entries or numerals baked into the image. Do not represent qubit states as Bloch spheres.

**BLOCK 3 — NEGATIVE PROMPT:**
Bloch sphere, named gate matrices (CNOT, Hadamard, Pauli), actual numerical matrix entries, entanglement diagrams, Bell state labels, text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, dual-headed arrows, hand-drawn styles, human figures, visual clutter, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion.

---

## Figure 3 — Bell-state creation: product state → entangled state, and partial-trace result

**Heuristic:** MC — Mechanism/Process
**Rank:** Important

**BLOCK 1 — ILLUSTRAE PASTE BLOCK:**
Draw a three-stage horizontal process diagram illustrating the creation of a Bell state and the consequence of the partial trace. Stage 1: two separate qubit nodes, each shown as a filled circle, connected by no bond — representing the product state |+⟩⊗|0⟩. Stage 2: a two-qubit gate block (rectangle) bridging both qubit nodes, representing the CNOT operation applied to the pair. Stage 3: the output, now shown as two filled circles connected by a double-bonded arc or entanglement link, representing the Bell state |Φ⁺⟩ where the two qubits can no longer be described independently. To the right of Stage 3, branch to a sub-panel: trace over (discard) the lower qubit by graying it out with a dashed circle, and show the remaining qubit in a maximally mixed state, represented visually as a filled half-and-half disk (equal probability of both basis states) rather than a pure state. Use arrows between stages. Indicate the separable/entangled boundary between Stage 1 and Stage 3 with a vertical dashed line. Use color to distinguish entangled vs. product character.

**BLOCK 2 — FULL SCOPE:**

`[S — SPECIFICATION]` Single-column 89 mm width, 300 DPI, SVG/EPS, white background. One horizontal row of three stages plus one branch sub-panel, all connected by arrows.

`[C — CONTENT]` Stage 1: product state — two independent qubit nodes, no correlation bond, each node Bluish Green `#009E73`. Stage 2: CNOT gate — a rectangular gate block spanning both qubits, Blue `#0072B2`. Stage 3: Bell state |Φ⁺⟩ — two qubit nodes joined by an entanglement arc, both Reddish Purple `#CC79A7`. Partial-trace branch: lower qubit grayed out (neutral gray dashed), upper qubit shown as half-filled disk indicating maximally mixed state I/2.

`[O — ORGANIZATION]` Left to right: Stage 1 → arrow → Stage 2 → arrow → Stage 3 → downward branch arrow → partial-trace sub-panel. Vertical dashed separator between Stage 1 and Stage 3 spans the full height of the figure to indicate the separability boundary. Gate block in Stage 2 touches both qubit lines (top = control, bottom = target — no text; position conveys role).

`[P — PRESENTATION]` Flat vector, Okabe-Ito palette, 1 pt strokes, white background, no baked text. Product-state qubits: Bluish Green `#009E73`. Gate rectangle: Blue `#0072B2`. Bell-state entangled qubits: Reddish Purple `#CC79A7`. Entanglement arc: Reddish Purple `#CC79A7`. Traced-out qubit: light gray dashed circle. Maximally mixed qubit: half Sky Blue `#56B4E9`, half light gray disk. Separability boundary dashed line: Vermillion `#D55E00`.

`[E — EXCLUSIONS]` Omit: Bloch sphere, circuit-diagram notation with classical wires, measurement symbols, density matrix notation, Schmidt decomposition. Do not show teleportation, superdense coding, or any other downstream protocol. Do not depict more than two qubits in this diagram.

**BLOCK 3 — NEGATIVE PROMPT:**
Bloch sphere, classical wire double-line notation, measurement meter symbols, more than two qubits, teleportation protocol stages, text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, dual-headed arrows, hand-drawn styles, human figures, visual clutter, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion.

---

## Video Candidate Pass

**Figure 1 — Dimension multiplication: direct sum vs. tensor product**
STATIC SUFFICIENT. The comparison is a spatial side-by-side snapshot; the distinction is structural, not procedural. No transition mechanism is the learning target here.

**Figure 2 — Kronecker product block structure and local-gate composition rule**
STATIC SUFFICIENT. The block nesting hierarchy and the composition identity are both static structural claims. The relationship is algebraic, not sequential.

**Figure 3 — Bell-state creation: product state → entangled state, and partial-trace result**
VIDEO CANDIDATE. Criterion: ≥3 sequential causal stages with a transformation below direct observation. The conversion of a product state to an entangled Bell state through the CNOT gate, followed by the partial trace that reveals the maximally mixed reduced state, is a three-stage causal process (product input → gate action → entanglement + trace outcome). Animating the bond forming between qubits at Stage 2→3 and the lower qubit fading to gray at the partial-trace step makes the causal chain concrete in a way that a static panel cannot. **Recommend as the single video for this module.**
