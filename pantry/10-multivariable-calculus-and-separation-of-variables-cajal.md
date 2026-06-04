# CAJAL Figure Report — Module M-10 — Multivariable Calculus and Separation of Variables

Recommended: 3 figures, Mixed density.

---

## Figure 1 — The Four-Step Separation-of-Variables Cascade (Cartesian)

**Heuristic:** MC — Mechanism/Process
**Rank:** Critical

---

**BLOCK 1 — ILLUSTRAE PASTE BLOCK:**

Draw a vertical four-panel process flowchart showing the separation-of-variables method applied to the 3D infinite square well. Panel 1: a single rectangular region representing the full PDE, with three independent coordinate axes entering from the left and a single wavefunction symbol at center. Panel 2: the product ansatz split — three separate single-variable function boxes (one per coordinate) connected by multiplication symbols, with an arrow indicating substitution into the PDE. Panel 3: the division step — show the single combined equation dividing into three horizontally arranged ratio boxes, each depending on only one coordinate, linked by a plus sign and an equals-constant symbol; use a dividing horizontal rule to represent division by the product. Panel 4: three separate ODE boxes, each with a downward arrow terminating at a boundary-condition block (zero-at-wall constraint), from which a quantized constant emerges. Color the product-ansatz box with Sky Blue, the division step with Orange, the three separated ODEs with Bluish Green, and the boundary-condition blocks with Reddish Purple. Use flat vector, uniform 1pt strokes, white background, Okabe-Ito palette, no baked text.

---

**BLOCK 2 — FULL SCOPE:**

- `[S — SPECIFICATION]` Single-column 89 mm width, 300 DPI, vector (SVG/EPS), white background, four stacked panels with uniform inter-panel spacing and a right-pointing flow arrow linking each panel.

- `[C — CONTENT]` Four panels strictly representing: (1) the 3D PDE as one object with three coordinate inputs; (2) the product ansatz substitution producing a product of three single-variable functions; (3) the division-by-product step that isolates each coordinate ratio, with an equals-constant constraint linking all three; (4) three independent ODEs each terminated at a zero-at-wall boundary condition block, from which a discrete quantized constant issues. The cascade is left-to-right within each panel and top-to-bottom across panels. No energy-level diagram, no wavefunction plots.

- `[O — ORGANIZATION]` Four stacked rectangular panels of equal width; connecting arrow on the right side flows downward from panel to panel. Within panel 3, the three ratio boxes are arranged horizontally at equal spacing. Within panel 4, the three ODE-plus-boundary chains are arranged in three parallel vertical columns. Panels 1–2 are single-column; panels 3–4 are three-column internally.

- `[P — PRESENTATION]` Flat vector. Sky Blue `#56B4E9` for the product-ansatz box (panel 2). Orange `#E69F00` for the division-step connector (panel 3 header). Bluish Green `#009E73` for the three ODE boxes (panel 4). Reddish Purple `#CC79A7` for the boundary-condition blocks at the foot of each ODE column. Neutral light gray for PDE box (panel 1). Uniform 1pt strokes. White background. No baked text. No gradient fills, no drop shadows.

- `[E — EXCLUSIONS]` Omit: energy eigenvalue formula, degeneracy argument, superposition step, spherical coordinate system, specific wavefunction plots, any indication of the 1D analog, actual numbers ($L$, $k$, $n$).

---

**BLOCK 3 — NEGATIVE PROMPT:**

energy eigenvalue equations, spherical coordinates, wavefunction oscillation plots, degeneracy diagram, 1D box cross-section, numeric labels, quantum number ladders, text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, dual-headed arrows, hand-drawn styles, human figures, visual clutter, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 2 — Spherical Separation Cascade: Three Quantum Numbers from Three Equations

**Heuristic:** MC — Mechanism/Process
**Rank:** Critical

---

**BLOCK 1 — ILLUSTRAE PASTE BLOCK:**

Draw a top-to-bottom three-tier mechanism diagram showing how the single central-potential wavefunction equation separates into three independent equations, each producing one quantum number. Top tier: a single oval node representing the full spherical PDE, with three coordinate arrows (radial, polar, azimuthal) branching downward. Middle tier: three rectangular equation boxes arranged horizontally — azimuthal box on the left, polar box in the center, radial box on the right — each connected to the top oval by a branching arrow; show a single-valuedness constraint symbol attached to the azimuthal box, a finiteness-at-poles constraint symbol on the polar box, and a normalizability-termination constraint symbol on the radial box. Bottom tier: three output tokens, one below each middle-tier box, representing the three quantum numbers produced; the azimuthal token is smallest, the polar token mid-size, the radial token largest. Connect each middle-tier box to its output token with a downward arrow. Color azimuthal elements Reddish Purple, polar elements Orange, radial elements Blue; constraint symbols Vermillion. Use flat vector, Okabe-Ito palette, white background, uniform 1pt strokes, no baked text.

---

**BLOCK 2 — FULL SCOPE:**

- `[S — SPECIFICATION]` Single-column 89 mm width, 300 DPI, vector (SVG/EPS), white background, three horizontal tiers with vertical connecting arrows.

- `[C — CONTENT]` Exactly three branching paths from one source node: (1) azimuthal path — equation box → single-valuedness constraint marker → quantum number output token; (2) polar path — equation box → finiteness-at-poles constraint marker → quantum number output token; (3) radial path — equation box → normalizability-termination constraint marker → quantum number output token. The source node receives three coordinate-axis arrows. No wavefunction shapes, no algebraic expressions, no energy levels.

- `[O — ORGANIZATION]` Top tier: one source oval, centered. Middle tier: three boxes in a horizontal row, evenly spaced, each connected by a branching line from the source. Between middle and bottom: each box connects downward via an arrow to a constraint symbol (diamond or circle), then to an output token. Bottom tier: three output tokens aligned horizontally below their respective chains. Left-to-right order: azimuthal, polar, radial.

- `[P — PRESENTATION]` Flat vector. Blue `#0072B2` for radial chain. Orange `#E69F00` for polar chain. Reddish Purple `#CC79A7` for azimuthal chain. Vermillion `#D55E00` for constraint symbols (marking where quantization is imposed). Light gray for source node. Uniform 1pt strokes. White background. No baked text. No gradient fills.

- `[E — EXCLUSIONS]` Omit: spherical harmonic shapes, energy-level diagram, hydrogen atom potential, Laguerre or Legendre polynomials, associated Legendre equation form, specific integers for quantum numbers, spin quantum number, time dependence.

---

**BLOCK 3 — NEGATIVE PROMPT:**

orbital lobe shapes, hydrogen energy-level diagram, polynomial graphs, associated Legendre plots, spin-½ arrow pairs, time-evolution arrows, explicit integer quantum number labels, text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, dual-headed arrows, hand-drawn styles, human figures, visual clutter, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 3 — Sign-of-Separation-Constant Decision Fork

**Heuristic:** VG — Verification Gap
**Rank:** Important

---

**BLOCK 1 — ILLUSTRAE PASTE BLOCK:**

Draw a binary decision-fork diagram with a central diamond decision node at the top, from which two branches descend. The left branch leads to a box representing a negative separation constant, which connects to an oscillatory wave symbol (a smooth sinusoidal arc); below this, a checkmark-shaped marker indicates that the zero-at-walls boundary condition can be satisfied. The right branch leads to a box representing a positive separation constant, which connects to an exponentially growing/decaying curve symbol; below this, an X-shaped block marker indicates that the zero-at-both-walls boundary condition cannot be satisfied. The decision node itself has a single input from above representing the general separated ODE. Use Bluish Green for the left (oscillatory, valid) branch and its checkmark marker, Vermillion for the right (exponential, invalid) branch and its block marker, Sky Blue for the decision diamond, and Orange for the central ODE input. Flat vector, Okabe-Ito palette, white background, uniform 1pt strokes, no baked text.

---

**BLOCK 2 — FULL SCOPE:**

- `[S — SPECIFICATION]` Single-column 89 mm width, 300 DPI, vector (SVG/EPS), white background, vertical fork layout with two descending branches.

- `[C — CONTENT]` One diamond decision node receiving a downward input labeled only with a directional arrow (not text). Left branch: negative-constant box → sinusoidal arc symbol → checkmark boundary-condition-satisfied marker. Right branch: positive-constant box → exponential growth/decay curve symbol → X blocked boundary-condition-failed marker. The sinusoidal arc has at least one zero crossing; the exponential curve has no zero crossings in its depicted range. No algebraic expressions, no specific numbers.

- `[O — ORGANIZATION]` Top-to-bottom flow. Decision node centered. Two branches diverge symmetrically left and right at 45 degrees. Each branch has three nodes stacked vertically (sign box, curve symbol, outcome marker) with downward arrows connecting them. Left branch terminates with a satisfied marker; right branch terminates with a blocked marker.

- `[P — PRESENTATION]` Flat vector. Sky Blue `#56B4E9` for decision diamond. Bluish Green `#009E73` for left branch elements (negative constant box, sinusoidal symbol, checkmark). Vermillion `#D55E00` for right branch elements (positive constant box, exponential symbol, X-block). Orange `#E69F00` for the incoming ODE input arrow. Uniform 1pt strokes. White background. No baked text.

- `[E — EXCLUSIONS]` Omit: specific differential equation forms, numeric values, boundary at only one wall (both walls must be represented by the boundary-condition marker), spherical-coordinate content, 2D or 3D geometry, energy levels, any reference to the azimuthal or radial equations.

---

**BLOCK 3 — NEGATIVE PROMPT:**

differential equation text, numeric axis labels, single-wall boundary indicators, spherical geometry, orbital diagrams, energy-level ladders, text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, dual-headed arrows, hand-drawn styles, human figures, visual clutter, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Video Candidate Pass

**Figure 1 — Four-Step Separation Cascade (Cartesian):**
VIDEO CANDIDATE. Criterion: ≥3 sequential causal stages — the four-step PDE-to-ODE cascade is the learning target, and the transformation from one combined equation into three independent ones requires showing the intermediate division step as a distinct transition. A static diagram risks collapsing the causal sequence into a simultaneously visible layout, obscuring why step 3 (division by product) is what enables step 4. One recommended video for the module: animate Figure 1, revealing each panel in sequence with a brief hold on panel 3 to show the "each term depends on one variable only" argument before the three ODEs separate.

**Figure 2 — Spherical Separation Cascade:**
STATIC SUFFICIENT. The three-branch structure is spatially parallel, not sequentially causal — all three separations happen from the same starting equation, and the branching topology communicates this fully in a single static frame.

**Figure 3 — Sign-of-Separation-Constant Fork:**
STATIC SUFFICIENT. The fork is a binary decision with no time-element; both outcomes are equally present in the reasoning and should be visible simultaneously for comparison.
