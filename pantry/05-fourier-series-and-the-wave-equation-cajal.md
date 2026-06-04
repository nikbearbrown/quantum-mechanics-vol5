# CAJAL Figure Report — Module M-05 — Fourier Series and the Wave Equation

Recommended: 3 figures, Mechanistic density.

---

## Figure 1 — Separation of variables: one PDE splits into two ODEs, boundary conditions quantize the modes

**Heuristic:** MC | **Rank:** Critical

---

**BLOCK 1 — ILLUSTRAE PASTE BLOCK**

Draw a vertical flowchart with five labeled stages connected by downward arrows. First box: a single wide rectangle representing the two-variable wave equation — the PDE. A horizontal dashed split line divides it into two narrower rectangles side by side, each representing one ODE (spatial and temporal). The splitting step is marked with a downward arrow labeled with the separation-constant symbol only — no words. From the spatial ODE box, a further downward arrow leads to a row of discrete horizontal bars representing the quantized mode spectrum — evenly spaced at first but labeled by integer index marks only. From the temporal ODE box, a downward arrow leads to a box showing a sinusoidal oscillation symbol (a simple wave arc). A final convergence arrow from both branches leads to a bottom box representing the general superposition (a multi-component bar shape suggesting a sum). No text baked into the image.

**BLOCK 2 — FULL SCOPE**

- `[S — SPECIFICATION]` Single-column, 89 mm width, 300 DPI, vector (SVG/EPS), white background. Single-column flowchart, approximately 6 nodes tall.
- `[C — CONTENT]` Node 1: the PDE (represented as a single undivided rectangle). Node 2: the spatial ODE (left branch). Node 3: the temporal ODE (right branch). Node 4a: discrete quantized wavenumbers (spatial branch output — a comb of horizontal marks). Node 4b: sinusoidal oscillation (temporal branch output — a single arc). Node 5: general superposition (convergence of both branches — represented as a stacked multi-bar shape). Separation constant shown only as a symbol at the split arrow.
- `[O — ORGANIZATION]` Top-to-bottom flow. At the split, two parallel branches diverge and descend before converging at the bottom. Arrows: solid single-headed downward. Branch split arrows angled outward. Convergence arrows angled inward to the final node.
- `[P — PRESENTATION]` Flat vector, Okabe-Ito: PDE box border = Blue `#0072B2`; spatial branch = Sky Blue `#56B4E9`; temporal branch = Orange `#E69F00`; quantized comb marks = Bluish Green `#009E73`; superposition node = Reddish Purple `#CC79A7`; arrows = dark gray. Uniform 1 pt strokes, node borders 1.5 pt. White background. No baked text.
- `[E — EXCLUSIONS]` Omit the physical string diagram, tension-force derivation, d'Alembert traveling-wave solution, the Schrödinger equation analogue, Fourier coefficient integrals, Gibbs phenomenon.

**BLOCK 3 — NEGATIVE PROMPT**

string diagram, tension force arrows, traveling wave illustration, Schrödinger equation box, Gibbs overshoot diagram, coefficient integral diagram, text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, dual-headed arrows, hand-drawn styles, human figures, visual clutter, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 2 — Orthogonality does the projection: extracting a Fourier coefficient

**Heuristic:** VG | **Rank:** Critical

---

**BLOCK 1 — ILLUSTRAE PASTE BLOCK**

Draw a two-panel figure. Left panel: show an arbitrary smooth curve (the initial shape — an asymmetric hump) on a horizontal axis from 0 to L. Below it, draw five or six sine-wave arcs of increasing frequency (modes n = 1 through 5 or 6), each on its own narrow horizontal strip, stacked vertically and sharing the same horizontal axis. Each mode is drawn in a distinct color cycling through the Okabe-Ito palette. Right panel: a vertical bar chart with five or six bars, one per mode, showing the projection coefficient magnitude for each — bars of varying height, starting at zero on the y-axis. The bar for the mode whose shape most closely matches the initial curve is the tallest. No text baked into the image.

**BLOCK 2 — FULL SCOPE**

- `[S — SPECIFICATION]` Single-column, 89 mm width, 300 DPI, vector (SVG/EPS), white background. Two side-by-side panels; left panel approximately 55% of width, right panel 45%.
- `[C — CONTENT]` Left panel: one arbitrary initial-state curve (smooth, asymmetric, vanishing at endpoints) at top; five individual sine-mode arcs stacked below it, each on its own strip, sharing the same x-axis span 0 to L. Right panel: vertical bar chart, one bar per mode, y-axis starting at zero, bar heights proportional to projection coefficient magnitudes drawn from the shape shown.
- `[O — ORGANIZATION]` Left panel stacks the initial curve above the mode strips in descending order n = 1, 2, 3, 4, 5. Right panel bars are ordered left-to-right n = 1 to 5, y-axis from zero upward. A visual correspondence (color matching) links each mode strip to its bar.
- `[P — PRESENTATION]` Flat vector, Okabe-Ito: initial curve = Blue `#0072B2`; mode n=1 = Sky Blue `#56B4E9`; n=2 = Orange `#E69F00`; n=3 = Bluish Green `#009E73`; n=4 = Reddish Purple `#CC79A7`; n=5 = light gray. Bars in right panel use the matching mode color. Uniform 1 pt strokes; y-axis from zero; no 3D. White background. No baked text.
- `[E — EXCLUSIONS]` Omit complex exponential modes, cosine modes, the coefficient integral formula, time evolution, the parabolic worked-example wavefunction by name, Gibbs phenomenon.

**BLOCK 3 — NEGATIVE PROMPT**

complex exponential wave diagram, cosine mode strips, Gibbs overshoot curve, time-evolution panel, parabolic wavefunction label, integral formula diagram, text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, dual-headed arrows, hand-drawn styles, human figures, visual clutter, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 3 — Bloch theorem: periodic potential couples momentum states separated by reciprocal lattice vectors

**Heuristic:** VG | **Rank:** Important

---

**BLOCK 1 — ILLUSTRAE PASTE BLOCK**

Draw a horizontal momentum-axis diagram. Place equally spaced vertical tick marks representing the reciprocal lattice — a comb of momenta separated by a fixed interval G. Above the axis, draw a series of downward-pointing filled circles at positions k, k+G, k+2G, k−G, k−2G to represent the plane-wave components of a Bloch state. Connect nearest-neighbor components with horizontal double-headed brackets (not dual-headed arrows — curved brackets instead) indicating that each Fourier component of the periodic potential couples these specific pairs. Mark the first Brillouin zone boundary with two vertical dashed lines flanking the central region (the interval from −π/a to +π/a). At the zone boundary positions, indicate two degenerate level circles connected by a curved bracket labeled with a gap indicator (a small vertical bar with outward tick marks, no text). No text baked into the image.

**BLOCK 2 — FULL SCOPE**

- `[S — SPECIFICATION]` Single-column, 89 mm width, 300 DPI, vector (SVG/EPS), white background. Single horizontal-axis panel.
- `[C — CONTENT]` Horizontal k-axis; reciprocal lattice comb at integer multiples of G = 2π/a; filled circles at k, k±G, k±2G representing Bloch-state plane-wave components; coupling brackets between neighboring components; Brillouin zone boundary dashed verticals at ±π/a; gap indicator at zone boundary (inferred relation: band gap arises from coupling of degenerate states — mark as inferred with dashed bracket).
- `[O — ORGANIZATION]` Momentum axis runs left to right, centered at k = 0. Reciprocal lattice marks evenly spaced. Bloch components as filled circles above axis. Coupling brackets below or above the circles, alternating to avoid overlap. Zone boundary verticals span the full panel height. Gap indicator sits between the zone-boundary pair of circles.
- `[P — PRESENTATION]` Flat vector, Okabe-Ito: k-axis = dark gray; Bloch component circles = Sky Blue `#56B4E9`; reciprocal lattice comb = Blue `#0072B2`; coupling brackets = Orange `#E69F00`; zone boundary lines = light gray dashed; gap indicator = Vermillion `#D55E00`. Uniform 1 pt strokes; zone boundary dashed 1 pt. White background. No baked text.
- `[E — EXCLUSIONS]` Omit the band dispersion (parabolic free-electron curve), the Kronig-Penney potential profile, real-space lattice diagram, three-dimensional Brillouin zone, time evolution, Gibbs phenomenon in the potential.

**BLOCK 3 — NEGATIVE PROMPT**

parabolic free-electron dispersion curve, Kronig-Penney potential step diagram, real-space crystal lattice, 3D Brillouin zone polyhedron, time-evolution arrows, Gibbs fringe pattern, text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, dual-headed arrows, hand-drawn styles, human figures, visual clutter, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Video Candidate Pass

**Figure 1 — Separation of variables flowchart**
STATIC SUFFICIENT. The flowchart depicts a logical decomposition structure, not a temporal sequence with causal staging; a static diagram communicates the branching and convergence completely.

**Figure 2 — Orthogonality projection into Fourier coefficients**
VIDEO CANDIDATE. Criterion: ≥3 sequential causal stages. The conceptual chain — arbitrary state is multiplied by each mode in turn, the integral selects only the matching component, the coefficient appears — has three causally ordered stages that a static two-panel figure compresses into simultaneity. A short animation showing one mode "lighting up" the coefficient bar as the projection integral sweeps across the initial curve, then cycling through each mode in sequence, would make the orthogonality mechanism visceral. Recommend this as the one video for the module.

**Figure 3 — Bloch coupling diagram**
STATIC SUFFICIENT. The coupling between specific momentum states is a structural relationship on a fixed axis; the zone boundary and gap are spatial properties readable from a static figure.
