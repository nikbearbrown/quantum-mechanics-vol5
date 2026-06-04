# CAJAL Figure Report — Module M-14 — Combinatorics and Multiplicity

**Source:** `chapters/14-combinatorics-and-multiplicity.md`
**Mode:** `/scan silent`

Recommended: 3 figures, Mixed density.

---

## Figure 1 — Microstate / macrostate / multiplicity conceptual hierarchy

**Heuristic:** VG | **Rank:** Critical

### BLOCK 1 — ILLUSTRAE PASTE BLOCK

Draw a three-level hierarchy diagram on a white background using flat vector linework and uniform 1pt strokes. At the bottom level, show a row of small individual elements — each representing a single fully-specified microstate arrangement (e.g., specific spin-up and spin-down configurations for a small N system). Use compact grid-like symbols, not text. Group several of these microstate symbols with a bracket or enclosure to indicate they all share the same observable property. At the middle level, a single box or node represents that macrostate — the coarse aggregate summary. At the top, a label or distinct shape represents the multiplicity Ω — the count of how many microstates map to that one macrostate. Use color to distinguish the three levels: microstates in one color, the macrostate node in a second color, the multiplicity count indicator in a third. Show at least two different macrostates side by side (one with high Ω, one with low Ω), so the concept of differing multiplicities is structurally visible. No text baked into the image.

### BLOCK 2 — FULL SCOPE

**[S — SPECIFICATION]** Single-column 89mm width, 300 DPI, vector (SVG/EPS), white background. Hierarchy diagram, two macrostates shown side by side for comparison.

**[C — CONTENT]** Bottom row: individual microstate symbols — small square grids of N = 4 cells, each cell either filled (spin up) or empty (spin down). Show all microstates for N↑ = 1 (four microstates grouped on the left) and all microstates for N↑ = 2 (six microstates grouped on the right). Grouping brackets or enclosures connect each cluster to its macrostate node. Middle row: two macrostate nodes — left labeled N↑ = 1 (with bracket enclosing 4 microstate symbols), right labeled N↑ = 2 (with bracket enclosing 6 microstate symbols). Top: multiplicity indicators — Ω = 4 on the left, Ω = 6 on the right. An upward arrow from microstates through macrostate to Ω on each side.

**[O — ORGANIZATION]** Bottom-to-top flow. Left cluster: low multiplicity. Right cluster: higher multiplicity. Three tiers clearly delineated by horizontal band or spacing. No diagonal crossing arrows.

**[P — PRESENTATION]** Flat vector. Microstate grid cells (spin up): Bluish Green #009E73 fill. Microstate grid cells (spin down): white fill, 0.5pt border. Macrostate node: Sky Blue #56B4E9 rounded rectangle, 1pt border. Multiplicity indicator: Orange #E69F00 circle or diamond. Grouping brackets: Blue #0072B2, 1pt. Tier-separating bands: light gray, no fill. Background: white. No baked text, no gradient, no 3D.

**[E — EXCLUSIONS]** Omit: the stars-and-bars formula for indistinguishable particles (different counting model); Stirling's approximation; entropy S = k ln Ω (a consequence, not the definition); quantum statistics (BE/FD — Figure 3); the Pascal recursion.

### BLOCK 3 — NEGATIVE PROMPT

text labels on the cells, entropy arrows, Boltzmann constant annotations, Pascal triangle, thermodynamic temperature notation, distinguishable vs identical labels baked in, text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, dual-headed arrows, hand-drawn styles, human figures, visual clutter, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 2 — Multiplicity Ω(N, N↑) as binomial distribution, peak sharpening with N

**Heuristic:** PQ | **Rank:** Critical

### BLOCK 1 — ILLUSTRAE PASTE BLOCK

Draw a two-panel or three-panel comparison figure on a white background using flat vector bar charts. Each panel shows the multiplicity Ω(N, N↑) as a function of N↑, plotted as a bar chart with N↑ on the horizontal axis (from 0 to N) and Ω on the vertical axis starting at zero. Show three panels for increasing values of N — for example N = 6, N = 20, and N = 100 (or a symbolic N → large). As N increases, the distribution narrows visibly relative to its width compared to the total span of the horizontal axis, and the peak at N↑ = N/2 dominates. All panels must share a normalized horizontal axis (show N↑/N from 0 to 1) so the sharpening is directly comparable. Use a single color for the bars. No text baked in.

### BLOCK 2 — FULL SCOPE

**[S — SPECIFICATION]** Single-column 89mm width, 300 DPI, vector (SVG/EPS), white background. Three vertically stacked panels (or side-by-side), each a bar chart.

**[C — CONTENT]** Panel 1: N = 6. Bar chart of Ω(6, N↑) = C(6, N↑) for N↑ = 0, 1, 2, 3, 4, 5, 6. Values: 1, 6, 15, 20, 15, 6, 1. Peak at N↑ = 3, peak/total = 20/64 ≈ 31%. Panel 2: N = 20. Bar chart of Ω(20, N↑) for N↑ = 0..20. Bell-shaped, peak at N↑ = 10, visibly narrower relative to span. Panel 3: schematic N = 100 (or symbolic large N). Very narrow bell-shaped distribution peaking sharply at N↑ = N/2, all other bars nearly invisible. Horizontal axis for all panels: N↑/N normalized from 0 to 1. Vertical axis from zero (different scales per panel). A reference bracket on panel 3 indicating the narrow peak width.

**[O — ORGANIZATION]** Three panels stacked vertically, each sharing the normalized horizontal axis 0 to 1. Vertical axes independently scaled. Left-aligned. The visual progression top-to-bottom is "broad → sharp" as N grows.

**[P — PRESENTATION]** Flat vector. All bars: Blue #0072B2. Peak bar (N↑ = N/2): Bluish Green #009E73 (highlighted). Width bracket on panel 3: Vermillion #D55E00, 1pt. Reference baseline at Ω = 0: black 0.5pt. Background: white. No baked text, no gradient, no 3D.

**[E — EXCLUSIONS]** Omit: Stirling approximation curve overlaid (prose); the smooth ln Ω curve from Stirling (a separate derivation object); entropy or temperature axes; the Einstein solid formula (different counting model); quantum statistics (BE/FD).

### BLOCK 3 — NEGATIVE PROMPT

smooth curve overlaid on bars, logarithmic vertical axis, entropy axis, Gaussian curve overlay, Stirling approximation label, numerical bar values baked in, text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, dual-headed arrows, hand-drawn styles, human figures, visual clutter, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 3 — Quantum statistics counting: MB vs BE vs FD for two particles, two states

**Heuristic:** VG | **Rank:** Important

### BLOCK 1 — ILLUSTRAE PASTE BLOCK

Draw a three-column comparison diagram on a white background using flat vector linework. Each column represents one statistical framework: Maxwell–Boltzmann (distinguishable particles), Bose–Einstein (identical bosons), and Fermi–Dirac (identical fermions). Within each column, draw all allowed distinct microstates for the scenario of two particles placed into two single-particle states. For MB, show four distinct configurations (both in state 1, particle A in 1 and B in 2, B in 1 and A in 2, both in state 2), using different fills or labels on the two particle symbols to indicate they are distinguishable. For BE, show three configurations (both in state 1, one in each, both in state 2), using identical symbols. For FD, show only one configuration (one particle in each state), using identical symbols, with the "both in same state" options absent (Pauli exclusion). Mark the count of allowed microstates at the bottom of each column: 4, 3, 1. No text baked into the image.

### BLOCK 2 — FULL SCOPE

**[S — SPECIFICATION]** Single-column 89mm width, 300 DPI, vector (SVG/EPS), white background. Three-column table-style layout with rows for each configuration.

**[C — CONTENT]** Two horizontal "state slots" shown in each configuration (state 1 at top, state 2 at bottom of each cell). Particle symbols: for MB, two circles with distinct fills (one Orange #E69F00, one Sky Blue #56B4E9) to indicate distinguishability; for BE and FD, two identical circles (same fill). MB column: 4 rows — (both in state 1), (A in 1, B in 2), (B in 1, A in 2), (both in state 2). BE column: 3 rows — (both in state 1), (one in each, identical), (both in state 2). FD column: 1 row — (one in each state only); the two doubly-occupied rows are crossed out with a blocking marker (Vermillion #D55E00 X) to show Pauli exclusion. Multiplicity count indicator below each column: 4, 3, 1. A separator between columns.

**[O — ORGANIZATION]** Three columns (MB, BE, FD) with rows for each microstate. Rows are aligned by configuration type where possible. FD column has only one valid row; the two blocked rows are shown crossed out at reduced opacity to make the exclusion mechanism visible. Column separators: light gray 0.5pt vertical lines.

**[P — PRESENTATION]** Flat vector. MB particle A: Orange #E69F00 circle. MB particle B: Sky Blue #56B4E9 circle. BE/FD particles: Reddish Purple #CC79A7 circles (identical). Pauli-exclusion X markers: Vermillion #D55E00. Count indicators: Blue #0072B2 enclosed number. Background: white. No baked text (particle labels and count numbers applied by typography post-production). No gradient, no 3D.

**[E — EXCLUSIONS]** Omit: N > 2 scenarios; the wavefunction antisymmetry derivation (Slater determinant); the full quantum statistics distributions (Fermi–Dirac function, Bose–Einstein distribution); quantum error correction (Module M-14's second QM application); the multiplicity Ω(N, N↑) binomial (Figure 2).

### BLOCK 3 — NEGATIVE PROMPT

energy-level diagrams, Fermi-Dirac distribution curves, Bose-Einstein distribution curves, more than two particles, more than two states, wavefunction symbols, determinant notation, text labels baked in, numbers baked into the image, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, dual-headed arrows, hand-drawn styles, human figures, visual clutter, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Video Candidate Pass

**Figure 1 (microstate/macrostate/multiplicity hierarchy):** STATIC SUFFICIENT. The hierarchy is a structural relationship — the three levels and the grouping brackets communicate the concept fully in a static frame.

**Figure 2 (binomial distribution sharpening with N):** VIDEO CANDIDATE. Criterion: transition mechanism is the learning target. The sharpening of the multiplicity peak as N grows from small (broad, flat) to thermodynamic scale (knife-edge) is a continuous transformation where the static three-panel comparison only approximates the continuous process. Animating N increasing from 6 to 100 with the bars updating shows the thermodynamic limit as a genuine dynamic phenomenon, making the claim "equilibrium is just where microstates concentrate" visceral. However, the three-panel static version communicates the same idea adequately for a reference figure. The bar-chart update is not uniquely temporal as a learning target — the progression is conceptual, not sequential-causal.

**Figure 3 (MB vs BE vs FD counting table):** STATIC SUFFICIENT. The counting table is a structural comparison; no temporal or cyclical element drives the concept.

**Recommendation: no video for this module.** Figure 2 is a mild candidate but the three-panel static format captures the sharpening adequately, and the learning target (peak concentration = equilibrium) does not require observing the transition in motion. STATIC SUFFICIENT across all three figures.
