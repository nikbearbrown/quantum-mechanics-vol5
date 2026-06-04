# CAJAL Figure Report — Module M-15 — Calculus of Variations and Stationarity

**Source:** `chapters/15-calculus-of-variations.md`
**Mode:** `/scan silent`

Recommended: 3 figures, Mechanistic density.

---

## Figure 1 — The variation: stationary path, wiggle η(x), and integration-by-parts boundary term

**Heuristic:** MC | **Rank:** Critical

### BLOCK 1 — ILLUSTRAE PASTE BLOCK

Draw a single-panel spatial diagram on a white background using flat vector linework. The horizontal axis represents the independent variable x, running from a fixed left endpoint x₁ to a fixed right endpoint x₂. Two fixed endpoint dots are marked at each end. Draw a smooth curve between the endpoints representing the stationary path y(x). Above and below this curve, draw two or three neighboring trial paths — smooth curves that also connect the same fixed endpoints, deviating from y(x) in the interior but returning to the exact same endpoint values. The deviation between a trial path and the stationary path at an interior point should be visually indicated with a small double-headed bracket or vertical offset marker labeled as the wiggle. Shade or highlight the region between the stationary path and one trial path to convey the concept of a variation. At each endpoint, show a clear visual stop — the wiggle curves must visibly terminate at the same points as the stationary path, with no overshoot. The diagram has six or fewer distinct visual components. No text baked into the image.

### BLOCK 2 — FULL SCOPE

**[S — SPECIFICATION]** Single-column 89mm width, 300 DPI, vector (SVG/EPS), white background. Single panel, schematic spatial layout.

**[C — CONTENT]** Horizontal axis: independent variable x from x₁ to x₂. Two fixed endpoint markers (filled dots) at (x₁, y(x₁)) and (x₂, y(x₂)). The stationary path y(x): a smooth curve (e.g., a gentle arc) connecting the endpoints. Two trial paths ȳ(x) = y(x) + εη(x): one above the stationary path and one below, both returning precisely to the endpoints. A vertical offset marker at an interior point x = x_mid showing the deviation εη(x_mid) between the stationary path and one trial path. A shaded thin strip between the stationary path and the upper trial path (the "variation" region). The η(x₁) = η(x₂) = 0 constraint is structurally represented by the trial paths meeting the endpoints exactly — no annotation needed, just the visual convergence. Six components: stationary path, two trial paths, two endpoint markers, interior offset marker.

**[O — ORGANIZATION]** Horizontal reading left to right. Stationary path runs through the center. Trial paths fan above and below in the interior but converge at both endpoints. The offset marker is placed at the widest deviation point. Shaded strip is thin and clearly between exactly two curves.

**[P — PRESENTATION]** Flat vector. Stationary path y(x): Blue #0072B2, 1.5pt. Upper trial path: Orange #E69F00, 1pt. Lower trial path: Sky Blue #56B4E9, 1pt. Shaded variation strip between stationary and upper trial: Orange #E69F00 at 10% opacity fill. Endpoint markers: Blue #0072B2 filled circles, radius 2pt. Offset marker (vertical bracket): Vermillion #D55E00, 0.5pt. Background: white. No baked text, no gradient, no 3D.

**[E — EXCLUSIONS]** Omit: the Euler–Lagrange equation itself (derived consequence, not the diagram's content); specific functional forms for L; the Lagrangian L = T − V substitution; the pendulum example; any coordinate system label beyond the two endpoints; the path-integral sum-over-paths interpretation (too advanced for the variation-setup diagram).

### BLOCK 3 — NEGATIVE PROMPT

arrows showing path direction, axis tick-mark numbers, coordinate grid, Lagrangian formula overlaid, potential energy curve, force arrows, specific functional shapes (sine, parabola labeled), text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, dual-headed arrows, hand-drawn styles, human figures, visual clutter, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 2 — The Lagrangian bridge: from S[y] through Euler–Lagrange to Newton to Hamiltonian to Schrödinger

**Heuristic:** VG | **Rank:** Critical

### BLOCK 1 — ILLUSTRAE PASTE BLOCK

Draw a vertical progression diagram on a white background using flat vector linework and uniform 1pt strokes. The diagram shows a chain of conceptual steps descending from the action functional at the top, through the Euler–Lagrange equation, to Newton's second law, to the Hamiltonian canonical equations, and finally to the Schrödinger equation at the bottom. Each step is represented as a node or block, connected by downward arrows. A secondary annotation-style element on each arrow indicates what operation or substitution connects consecutive steps — for example, a small shape indicating "set δS = 0" on the first arrow, "substitute L = T − V" on the second, "Legendre transform" on the third, "promote p → −iℏ∇" on the fourth. Use a color progression or consistent color scheme across the five nodes, with the quantum mechanics endpoint differentiated from the classical steps above it. Maximum six labeled components. No text baked into the image.

### BLOCK 2 — FULL SCOPE

**[S — SPECIFICATION]** Single-column 89mm width, 300 DPI, vector (SVG/EPS), white background. Vertical flowchart, five nodes, four arrows.

**[C — CONTENT]** Node 1 (top): action functional S[y] = ∫L dx — the variational starting point. Arrow 1 (down): stationarity condition δS = 0 applied. Node 2: Euler–Lagrange equation d/dx(∂L/∂y′) − ∂L/∂y = 0. Arrow 2 (down): substitution L = T − V, coordinate q, time t. Node 3: Newton's second law F = mq̈. Arrow 3 (down): canonical momentum p = ∂L/∂q̇, Legendre transform H = pq̇ − L. Node 4: Hamiltonian canonical equations ṗ = −∂H/∂q, q̇ = ∂H/∂p. Arrow 4 (down): promote q → q̂, p → −iℏ∇. Node 5 (bottom): Schrödinger equation Ĥψ = iℏ ∂ψ/∂t. The five nodes are the content; the arrows carry the connecting operation as small shape indicators (not text). Color distinguishes classical (nodes 1–4) from quantum (node 5).

**[O — ORGANIZATION]** Vertical top-to-bottom flow. Nodes are rounded rectangles of equal width. Arrows are single-headed downward. Small operation-indicator shapes (not text labels) on each arrow — e.g., a delta symbol shape for stationarity, an equals sign shape for substitution, a stylized L shape for Legendre transform, a hat symbol for quantization. The quantum node (5) has a visually distinct border or fill.

**[P — PRESENTATION]** Flat vector. Classical nodes (1–4): Blue #0072B2 border, white fill, 1pt. Quantum node (5): Bluish Green #009E73 border, Bluish Green #009E73 at 10% opacity fill, 1pt. Arrows: neutral gray, 1pt, single-headed. Operation-indicator shapes: Orange #E69F00. Background: white. No baked text (all equation text and operation labels applied by typography), no gradient, no 3D.

**[E — EXCLUSIONS]** Omit: the Noether's theorem symmetry–conservation connection (a separate conceptual branch, not the main chain); the path-integral formulation (separate application); the quantum variational method Rayleigh–Ritz detail (Figure 3); the pendulum worked example; Lagrange multiplier detail.

### BLOCK 3 — NEGATIVE PROMPT

branching arrows, Noether's theorem branch, path integral branch, bidirectional arrows, specific matrix eigenvalue content, detailed wavefunction ψ(x) curves, energy level diagrams, text labels baked in, equation text in the image, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, dual-headed arrows, hand-drawn styles, human figures, visual clutter, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 3 — Variational upper bound: trial wavefunction energies vs exact ground state E₀

**Heuristic:** PQ | **Rank:** Important

### BLOCK 1 — ILLUSTRAE PASTE BLOCK

Draw a single-panel quantitative figure on a white background using flat vector linework. The horizontal axis represents a trial-function parameter — for example, a width or shape parameter α that controls the family of trial wavefunctions. The vertical axis represents the expectation value ⟨H⟩ = ⟨ψ_trial|Ĥ|ψ_trial⟩/⟨ψ_trial|ψ_trial⟩, starting at zero and running upward. Draw a single horizontal dashed reference line at the exact ground-state energy E₀, which is below all trial-function energy values. Plot two or three smooth curves, one for each trial function family, showing ⟨H⟩ as a function of the parameter α. Each curve has a minimum above the E₀ reference line. On one curve, mark the minimum with a small dot — this is the variational estimate. Indicate with a vertical bracket or offset marker the gap between the trial minimum and E₀, which must be positive (the variational bound). The y-axis starts at zero. No text baked in.

### BLOCK 2 — FULL SCOPE

**[S — SPECIFICATION]** Single-column 89mm width, 300 DPI, vector (SVG/EPS), white background. Single panel, quantitative line plot.

**[C — CONTENT]** Vertical axis: ⟨H⟩ expectation value, starting at zero (y-axis from zero as required for quantitative figures), with energy increasing upward. Horizontal axis: trial-function parameter α (e.g., width parameter, dimensionless). Horizontal dashed reference line at E₀ (exact ground-state energy, below all curves). Three trial-function curves: (1) Blue #0072B2 — a Gaussian trial function family, minimum close to E₀ (tight bound); (2) Orange #E69F00 — a parabolic/polynomial trial function family, minimum somewhat above E₀; (3) Sky Blue #56B4E9 — a wider-class family, minimum farther above E₀. Each curve's minimum is marked with a filled dot. A vertical bracket on the Blue curve from its minimum down to the E₀ line, indicating the variational gap. The E₀ reference line extends across the full horizontal span. The key structural content: all curves remain above E₀; the best trial function's minimum approaches E₀ most closely.

**[O — ORGANIZATION]** Standard line-plot layout. E₀ dashed line at the bottom of the active range (above zero on the axis). Three curves arch above it with distinct minima. Minimum-mark dots on each curve. Vertical gap bracket on the lowest-minimum curve. Axis from zero.

**[P — PRESENTATION]** Flat vector. Trial curve 1 (tight bound): Blue #0072B2, 1pt. Trial curve 2 (moderate bound): Orange #E69F00, 1pt. Trial curve 3 (loose bound): Sky Blue #56B4E9, 1pt. Minimum dots: matching color, radius 2pt. E₀ reference line: Vermillion #D55E00, 1pt dashed (lower bound is the critical reference). Variational gap bracket: Reddish Purple #CC79A7, 0.5pt. Axis lines and zero line: black 0.5pt. Background: white. No baked text, no gradient, no 3D.

**[E — EXCLUSIONS]** Omit: the Rayleigh–Ritz matrix eigenvalue equation (algebra, not the geometric bound); specific basis function formulas; the normalization constraint derivation; the Lagrange multiplier eigenvalue result; the infinite square well specific numbers (prose worked example).

### BLOCK 3 — NEGATIVE PROMPT

curves that dip below the E₀ reference line, y-axis that does not start at zero, excited-state energy levels, energy-eigenvalue ladder diagrams, wavefunction shape panels, basis function plots, Hamiltonian matrix elements baked in, text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, dual-headed arrows, hand-drawn styles, human figures, visual clutter, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Video Candidate Pass

**Figure 1 (stationary path and wiggle):** VIDEO CANDIDATE. Criterion: transition mechanism is the learning target. The variation is inherently a process — starting from the stationary path, smoothly deforming it into trial paths with an arbitrary wiggle η(x), and demonstrating that the boundary conditions force the wiggle to vanish at the endpoints while allowing free interior deformation. This continuous deformation cannot be fully captured in a snapshot of two or three trial paths; watching the wiggle sweep continuously (sweeping η from +ε to −ε while the endpoints stay pinned) would make the "hold endpoints fixed, vary only the interior" constraint visceral. However, the static figure with two trial paths and a gap bracket communicates the structure adequately.

**Figure 2 (Lagrangian bridge flowchart):** STATIC SUFFICIENT. The flowchart is a structural inheritance diagram; no cyclical or sequential-causal temporal element drives the concept.

**Figure 3 (variational upper bound):** STATIC SUFFICIENT. The bound is a static geometric relationship — all trial-function energies lie above E₀. No temporal element.

**Recommendation: one video — Figure 1 (the variation animated).** Criterion: transition mechanism is the learning target. Animate the family of trial paths as the wiggle amplitude ε sweeps from −ε_max to +ε_max, with the two endpoints pinned and the interior deviation smoothly varying. The visual of the path "breathing" around the stationary path while the endpoints stay frozen communicates the mathematical structure of δS more powerfully than any static snapshot. This is the module's most abstract concept and the one students most often misunderstand as "minimization" rather than "stationarity under all perturbations."
