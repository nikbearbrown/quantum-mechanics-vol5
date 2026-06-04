# CAJAL Figure Report — Module M-09 — Operators and Dirac Notation

Recommended: 3 figures, Mixed density.

---

## Figure 1 — Bra–Ket Type Grammar: Scalar vs. Operator from the Same Symbols

**Heuristic:** VG — Verification Gap
**Rank:** Critical

---

**BLOCK 1 — ILLUSTRAE PASTE BLOCK**

Draw a single panel divided into two clearly separated horizontal rows, each illustrating one of the two ways to combine a bra and a ket. In the top row, show a bra (a leftward-pointing half-bracket shape) followed by a ket (a rightward-pointing half-bracket shape) with the open ends facing each other — the "inner" arrangement — and draw an outgoing single line or dot indicating the result is one number, a scalar. In the bottom row, show a ket shape followed by a bra shape with their open ends facing outward — the "outer" arrangement — and draw from this a small rectangular grid of cells (a 2×2 operator matrix icon, all cells filled) plus an arrow indicating it maps one ket to another ket. A thin horizontal separator between the two rows. Additionally, draw a small vertical "anti-linearity" indicator in the corner: a bra shape with a conjugate star next to a coefficient, contrasted with the ket shape with no star. Use flat vector rendering, uniform 1pt strokes, white background, and no baked text.

**BLOCK 2 — FULL SCOPE**

- `[S — SPECIFICATION]` Single-column 89mm width, 300 DPI, vector (SVG/EPS), white background. Single panel with two rows plus a small sidebar indicator.
- `[C — CONTENT]` Row 1 (bra × ket = scalar): bra half-bracket facing right, ket half-bracket facing left, bracket pair closed, resulting in a single dot or scalar glyph (a circle). Row 2 (ket × bra = operator): ket half-bracket facing right, bra half-bracket facing left, bracket pair open outward, resulting in a 2×2 filled grid icon and a mapping arrow (ket → ket). Sidebar: a coefficient label next to a bra shape shows a star/conjugate indicator, contrasted with a coefficient next to a ket shape with no star — signaling anti-linearity. Total elements ≤8.
- `[O — ORGANIZATION]` Two horizontal rows separated by a thin line. Bracket shapes are the dominant visual element — use geometric half-brackets (angular or rounded, consistent). Scalar result shown as a filled circle. Operator result shown as a small grid icon plus a mapping arrow. Anti-linearity sidebar in lower-right corner uses a star symbol (geometric, not typographic) next to the bra bracket only.
- `[P — PRESENTATION]` Flat vector, Okabe-Ito. Bra brackets: Sky Blue `#56B4E9`. Ket brackets: Blue `#0072B2`. Scalar result dot: Bluish Green `#009E73`. Operator grid icon: Orange `#E69F00`. Mapping arrow: light gray. Anti-linearity star indicator: Vermillion `#D55E00`. Separator line: light gray. Uniform 1pt strokes.
- `[E — EXCLUSIONS]` Omit: adjoint definition, Hermitian operators, unitary operators, expectation value formula, commutator, resolution of the identity, inner product axioms. This figure is purely type-grammar for bra-ket combinations.

**BLOCK 3 — NEGATIVE PROMPT**

adjoint dagger symbol baked in, Hermitian condition formula, unitary condition, expectation value formula, commutator notation, resolution of identity formula, inner product axiom list, text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, dual-headed arrows, hand-drawn styles, human figures, visual clutter, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion.

---

## Figure 2 — The Adjoint: How Operators Flip Across the Inner Product

**Heuristic:** VG — Verification Gap
**Rank:** Critical

---

**BLOCK 1 — ILLUSTRAE PASTE BLOCK**

Draw a single panel illustrating the defining relation of the adjoint with a visual "flip" structure. Show a bra on the left and a ket on the right, with an operator icon (a small filled rectangle) sitting between them on the ket side — this represents bra applied to (operator times ket). Draw a two-headed equivalence arrow or an equals bridge, leading to the mirror image: the same bra, the same ket, but now the operator icon has crossed over to the bra side and acquired a small dagger or double-star modifier icon above it — this represents (adjoint-operator times bra) applied to ket. Below the main diagram, show a row of three small rule panels illustrating order-reversal: two operator rectangles A and B in sequence on the left, then a dagger symbol flipping their order to B-dagger then A-dagger on the right. Show the scalar conjugation rule: a coefficient and an operator on the left, transforming to a conjugated coefficient and adjoint operator on the right, using a star symbol on the coefficient. Use flat vector rendering, uniform 1pt strokes, white background, and no baked text.

**BLOCK 2 — FULL SCOPE**

- `[S — SPECIFICATION]` Single-column 89mm width, 300 DPI, vector (SVG/EPS), white background. Main diagram in upper two-thirds; three rule panels in lower third.
- `[C — CONTENT]` Main: bra half-bracket — operator rectangle — ket half-bracket on the left of an equals bridge; on the right: (adjoint-operator with dagger marker) half-bracket — ket half-bracket. The dagger is a distinct geometric marker (a cross or double-dot), not a text glyph. Lower rule panels (three): (1) A-rect then B-rect → B-dagger-rect then A-dagger-rect (order reversal); (2) coefficient-circle then operator-rect → star-coefficient-circle then adjoint-rect (scalar conjugation); (3) ket-bracket then bra-bracket with dagger → bra-bracket then ket-bracket (ket-bra adjoint swaps). Total elements across all: ≤8 per sub-panel.
- `[O — ORGANIZATION]` Main diagram centered horizontally. Lower rule strip: three equal-width mini-panels in a row. An "=" bridge or double-arrow separates left and right sides of each rule. Dagger marker is a consistent geometric symbol (not typography) placed above or beside the operator rectangle.
- `[P — PRESENTATION]` Flat vector, Okabe-Ito. Bra brackets: Sky Blue `#56B4E9`. Ket brackets: Blue `#0072B2`. Operator rectangle A: Orange `#E69F00`. Operator rectangle B: Reddish Purple `#CC79A7`. Adjoint marker (dagger): Vermillion `#D55E00`. Star/conjugate marker on coefficient: Vermillion `#D55E00`. Equals bridge: light gray. Uniform 1pt strokes.
- `[E — EXCLUSIONS]` Omit: Hermitian condition (A = A-dagger), unitary condition, specific matrix entries, commutator, momentum operator, integration by parts. This figure is purely the adjoint definition and its three manipulation rules.

**BLOCK 3 — NEGATIVE PROMPT**

Hermitian self-adjoint equation, unitary condition, matrix numerical entries, commutator notation, momentum operator formula, integration by parts, text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, dual-headed arrows, hand-drawn styles, human figures, visual clutter, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion.

---

## Figure 3 — Robertson Uncertainty: From Cauchy–Schwarz to the Commutator Bound

**Heuristic:** MC — Mechanism/Process
**Rank:** Important

---

**BLOCK 1 — ILLUSTRAE PASTE BLOCK**

Draw a four-stage vertical flowchart illustrating the logical chain from Cauchy–Schwarz to the Robertson uncertainty bound. In the first stage, show two abstract vector arrows f and g from a common origin, with a right-angle drop from each to the horizontal indicating their norms, and an angle between them indicating their overlap — the Cauchy–Schwarz geometry. An downward step arrow leads to the second stage: a square inequality icon with the two norms squared on the left and the squared overlap magnitude on the right, the relationship shown as a ≥ bridge. A downward step arrow leads to the third stage: the overlap expression is decomposed into real and imaginary parts, shown as a horizontal split into two sub-boxes — one labeled with a plus icon (real part) and one with a circled i icon (imaginary part), where the imaginary part contains a small bracket-shaped commutator icon. A downward step arrow leads to the fourth stage: the final bound — two variance symbols (sigma-shaped icons or bell-curve silhouettes) on the left side of a ≥ bridge, and a half-value icon (a split circle or bisected disk) times the commutator icon on the right. Use flat vector rendering, uniform 1pt strokes, white background, and no baked text.

**BLOCK 2 — FULL SCOPE**

- `[S — SPECIFICATION]` Single-column 89mm width, 300 DPI, vector (SVG/EPS), white background. Single-column four-stage flowchart, top to bottom.
- `[C — CONTENT]` Stage 1: Cauchy–Schwarz geometry — two vectors f, g, angle between them, norm projections. Stage 2: squared-norm inequality (||f||^2 * ||g||^2 ≥ |<f|g>|^2), rendered as geometric icons — two length bars, a ≥ symbol, and one overlap magnitude icon. Stage 3: decomposition of <f|g> into real and imaginary parts — two sub-boxes, one with a real-part icon (horizontal bar), one with an imaginary-part icon (circled i or i-dot), the imaginary sub-box containing a commutator bracket-pair icon. Stage 4: final bound — two bell-curve silhouettes (sigma_A and sigma_B) ≥ half-disk times commutator icon. Four downward step arrows connecting stages. Total elements: ≤8 per stage.
- `[O — ORGANIZATION]` Vertical flowchart, four equally spaced stages connected by downward step arrows. Each stage is a self-contained box. Step arrows are one-directional (downward only). The commutator icon (two nested half-brackets) appears in stages 3 and 4 for visual continuity.
- `[P — PRESENTATION]` Flat vector, Okabe-Ito. Stage 1 vectors f, g: Blue `#0072B2` and Bluish Green `#009E73`. Cauchy–Schwarz inequality ≥ bridge: light gray. Stage 2 norm bars: Sky Blue `#56B4E9`. Overlap magnitude: Orange `#E69F00`. Stage 3 real sub-box: light gray. Imaginary sub-box with commutator: Reddish Purple `#CC79A7`. Stage 4 variance bell curves: Blue `#0072B2`. Commutator icon: Reddish Purple `#CC79A7`. Half-disk: Sky Blue `#56B4E9`. Step arrows: light gray. Uniform 1pt strokes.
- `[E — EXCLUSIONS]` Omit: measurement disturbance interpretation (Heisenberg microscope), Ozawa's theorem, specific numeric values, position and momentum labels, Hamiltonian, energy-time uncertainty. This figure is purely the algebraic chain: Cauchy–Schwarz → imaginary part → commutator bound.

**BLOCK 3 — NEGATIVE PROMPT**

Heisenberg microscope diagram, measurement apparatus, position-momentum labels, Hamiltonian symbol, energy-time uncertainty, Ozawa disturbance diagram, numerical values, text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, dual-headed arrows, hand-drawn styles, human figures, visual clutter, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion.

---

## Video Candidate Pass

**Figure 1 — Bra–Ket Type Grammar:** STATIC SUFFICIENT. The two-row comparison is a spatial taxonomy. No temporal process; the reader scans the two cases at will.

**Figure 2 — The Adjoint:** STATIC SUFFICIENT. The flip structure and the three manipulation rules are displayed as parallel comparisons. The mechanism (operator crosses the inner product with conjugation) is spatial, not temporal.

**Figure 3 — Robertson Uncertainty: Cauchy–Schwarz Chain:** VIDEO CANDIDATE. Criterion: ≥3 sequential causal stages and the derivation chain (Cauchy–Schwarz → imaginary part extraction → commutator bound) is the learning target. Animating the inequality propagating downward — each stage arriving from the one above, with the commutator icon materializing from the imaginary decomposition — would show the logical dependency that a static flowchart can only imply. **Recommended as the single video for this module.**
