# CAJAL Figure Report — Module M-13 — Logarithms, Exponentials, and Scales

**Source:** `chapters/13-logarithms-exponentials-and-scales.md`
**Mode:** `/scan silent`

Recommended: 3 figures, Mixed density.

---

## Figure 1 — Log–log vs semi-log linearization diagnostic

**Heuristic:** PQ | **Rank:** Critical

### BLOCK 1 — ILLUSTRAE PASTE BLOCK

Draw a two-panel comparison figure on a white background using flat vector linework and uniform 1pt strokes. Both panels share a vertical axis scale in their own units; both x-axes run from small positive values to large. The left panel shows a curve that bends upward as a power-law relationship on linear axes, then below it (or as an inset) shows the same data as a straight line when plotted on log–log axes — both axes logarithmically spaced. Mark the slope triangle on the straight-line version to indicate the exponent k. The right panel shows an exponential curve bending sharply upward on linear axes, then as a straight line on semi-log axes — the vertical axis logarithmically spaced, the horizontal axis linear. Mark the slope triangle on the semi-log straight line to indicate decay or growth rate. Use two distinct colors for the two functional families: one for the power-law pair, one for the exponential pair. Keep all elements strictly two-dimensional with no gradient fills, no drop shadows, and no text labels baked into the image.

### BLOCK 2 — FULL SCOPE

**[S — SPECIFICATION]** Single-column 89mm width, 300 DPI, vector (SVG/EPS), white background. Two-panel layout side by side (or 2×2 sub-panels: top row = curved, bottom row = linearized).

**[C — CONTENT]** Left panel pair: a power law y = Ax^k (k > 1) shown first on linear–linear axes (upward-bending curve) and then on log–log axes (straight line with slope triangle labeled k). Right panel pair: an exponential y = Ae^{kx} shown first on linear–linear axes (sharply rising curve) and then on semi-log axes (straight line, vertical axis logarithmic, horizontal axis linear, slope triangle labeled k/ln10 or equivalently the rate). The two families are color-coded: power-law curves in Sky Blue #56B4E9; exponential curves in Orange #E69F00. Slope triangles and reference ticks in neutral light gray. The relationship — which axis transform linearizes which law — is the sole content.

**[O — ORGANIZATION]** 2×2 grid: row 1 = raw curves on linear axes; row 2 = linearized versions on log–log (left) and semi-log (right). A thin neutral dividing line between rows and columns. The visual progression top-to-bottom is "raw → linearized." Axes tick marks only, no numerical labels (those are applied in typography). Arrow or bracket indicating the slope triangle on each lower panel.

**[P — PRESENTATION]** Flat vector. Okabe-Ito palette. Power-law curves: Sky Blue #56B4E9, 1pt stroke. Exponential curves: Orange #E69F00, 1pt stroke. Slope triangles: light gray fill, 0.5pt border. Axis lines: black 0.5pt. Background: white. No baked text, no gradient, no 3D.

**[E — EXCLUSIONS]** Omit: specific numerical data points or scatter; decibel or pH scales; radioactive decay curve (handled in Figure 2); the log-of-a-sum warning (prose); base-10 vs natural log distinction (prose); worked example values.

### BLOCK 3 — NEGATIVE PROMPT

curved linear-axis plots that are not the raw form, scatter-plot data points, numerical axis labels, tick-mark numbers, logarithm base annotations, color-coded legend boxes, text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, dual-headed arrows, hand-drawn styles, human figures, visual clutter, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 2 — Tunneling transmission T = e^{−2κL} vs barrier width

**Heuristic:** PQ | **Rank:** Critical

### BLOCK 1 — ILLUSTRAE PASTE BLOCK

Draw a single-panel quantitative line plot on a white background with flat vector linework. The horizontal axis represents barrier width L (linear scale). The vertical axis represents the transmission probability T = e^{−2κL} on a logarithmic scale, running from 1 at the top to very small values near zero at the bottom (y-axis from the natural floor of the logarithmic scale, not forced to zero on the log axis). Plot two or three curves corresponding to different values of κ — one for a small κ (high transmission, slow decay), one for a large κ (low transmission, fast decay) — each as a straight line on this semi-log plot. Mark on one curve the qualitative regimes: near the top where T is close to 1 labeled "substantial tunneling," and near the bottom where T approaches zero labeled "exponential suppression." Show the equal-step rule with a bracket indicating that each equal increment in L produces a constant multiplicative drop in T. Use distinct Okabe-Ito colors for the different κ curves. Keep the layout strictly two-dimensional with no text baked in, no gradient fills, and no drop shadows.

### BLOCK 2 — FULL SCOPE

**[S — SPECIFICATION]** Single-column 89mm width, 300 DPI, vector (SVG/EPS), white background. Single panel, semi-log axes: horizontal axis linear (barrier width L), vertical axis logarithmic (transmission T).

**[C — CONTENT]** Two or three straight lines corresponding to different decay constants κ (small, medium, large), each a straight line on the semi-log plot with negative slope −2κ. The lines are derived from T = e^{−2κL}. On the largest-κ line, mark three regime zones: a top bracket at small L indicating "T ≈ 1, substantial," a mid bracket indicating "T ≈ e^{−2}, partial," and a bottom zone indicating "T ≪ 1, suppressed." A reference bracket on one line showing equal-L increments producing equal multiplicative drops (the semi-log straight-line property). The y-axis is logarithmic, spanning from T = 1 at top to T = 10^{−5} or smaller at bottom. The x-axis is linear.

**[O — ORGANIZATION]** Single panel. Y-axis logarithmic starting at T = 1 (the physically meaningful upper bound). X-axis from L = 0. Lines run top-left to bottom-right. Regime brackets and reference bracket placed without overlapping the lines. Axis ticks at decade intervals on y.

**[P — PRESENTATION]** Flat vector. First κ curve: Blue #0072B2, 1pt. Second κ curve: Bluish Green #009E73, 1pt. Third κ curve (if used): Orange #E69F00, 1pt. Regime bracket fills: light gray at 20% opacity. Reference slope bracket: Reddish Purple #CC79A7, 0.5pt. Axis lines: black 0.5pt. Background: white. No baked text, no gradient, no 3D.

**[E — EXCLUSIONS]** Omit: specific numerical values of κ or L; the WKB integral formula (Figure 3); the Gamow factor derivation; STM application specifics; the table of 2κL values (prose); the rectangular-barrier wavefunction drawing.

### BLOCK 3 — NEGATIVE PROMPT

linear-scale y-axis, scatter data points, numerical axis label text, specific κ or L value annotations baked in, gradient fills, the wavefunction ψ(x) curve, barrier potential diagram, text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, dual-headed arrows, hand-drawn styles, human figures, visual clutter, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 3 — WKB tunneling geometry: classically allowed and forbidden regions

**Heuristic:** MC | **Rank:** Important

### BLOCK 1 — ILLUSTRAE PASTE BLOCK

Draw a single-panel spatial diagram on a white background using flat vector linework. The horizontal axis represents position x. On this axis, draw a smooth barrier potential V(x) as a hill-shaped curve that rises above a horizontal reference line representing the particle energy E. The region where V(x) > E — the classically forbidden zone — is shaded in a distinct color between the two intersection points x₁ and x₂, which are the classical turning points. Left of x₁ and right of x₂, where V(x) < E, are the classically allowed regions. Show a schematic decaying wavefunction underneath the barrier (a smooth exponentially decaying shape) and oscillatory wave shapes in the classically allowed regions on both sides. Mark the two turning points x₁ and x₂ with vertical reference lines. Use no more than six labeled components total. Keep the figure strictly two-dimensional with flat color fills, no gradients, and no text baked into the image.

### BLOCK 2 — FULL SCOPE

**[S — SPECIFICATION]** Single-column 89mm width, 300 DPI, vector (SVG/EPS), white background. Single panel, schematic spatial layout.

**[C — CONTENT]** Horizontal axis: position x. A smooth hill-shaped curve for V(x) (the barrier potential, peaking at the center). A horizontal dashed line at energy E. The classically forbidden region (where V > E) shaded in a fill color between x₁ and x₂. Two vertical reference lines at the turning points x₁ and x₂ (where V = E). Left of x₁: a schematic oscillatory wavefunction ψ (incoming/transmitted wave, several periods shown). Inside the barrier x₁ to x₂: a smooth decaying exponential envelope for ψ (dropping from x₁ to x₂). Right of x₂: a lower-amplitude oscillatory wavefunction ψ (transmitted wave). An arc or bracket over the forbidden region indicating the WKB exponent integral from x₁ to x₂. Components: V(x) curve, E reference line, two turning-point markers, oscillatory ψ left, decaying ψ inside, oscillatory ψ right — six components.

**[O — ORGANIZATION]** Single horizontal panel. V(x) in upper region. E line horizontal. Forbidden region shaded. Wavefunctions in lower spatial region. Left-to-right reading: incident oscillation → exponential decay → transmitted oscillation.

**[P — PRESENTATION]** Flat vector. V(x) curve: Blue #0072B2, 1.5pt. E reference line: Orange #E69F00, 1pt dashed. Forbidden-region shading: Vermillion #D55E00 at 15% opacity fill. Turning-point reference lines: light gray 0.5pt. Oscillatory ψ (classically allowed): Bluish Green #009E73, 1pt. Decaying ψ (forbidden): Reddish Purple #CC79A7, 1pt. Background: white. No baked text, no gradient, no 3D.

**[E — EXCLUSIONS]** Omit: the rectangular barrier special case (this is the general WKB geometry); numerical κ values; the Gamow factor for alpha decay specifically; the STM application; specific energy-level numbers; the connection formula derivation.

### BLOCK 3 — NEGATIVE PROMPT

rectangular step-function potential, specific numerical values baked in, arrow showing particle direction, human-scale analogies, gradient fills on the barrier, realistic molecular or nuclear structures, text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, dual-headed arrows, hand-drawn styles, human figures, visual clutter, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Video Candidate Pass

**Figure 1 (log–log vs semi-log diagnostic):** STATIC SUFFICIENT. The two-panel comparison is structural — a slider animating the axis change would add interactivity but the conceptual point (which transform linearizes which law) is captured in a single static frame.

**Figure 2 (T vs L semi-log):** STATIC SUFFICIENT. The semi-log straight lines are already the punchline; no temporal or cyclical element is the learning target.

**Figure 3 (WKB tunneling geometry):** VIDEO CANDIDATE. Criterion: transition mechanism is the learning target. The spatial attenuation of ψ as it passes through the forbidden region — and the connection between the depth/width of the forbidden zone and the degree of suppression — is a continuous spatial process. Animating the barrier height or width changing and watching the transmitted amplitude shrink (or the decaying exponential steepen) makes the exponential sensitivity visceral in a way a static snapshot cannot. **Recommended video: one, Figure 3 — animate barrier width L growing from near-zero to large, showing transmitted-wave amplitude shrinking exponentially. The semi-log version (Figure 2) can caption with the corresponding T value updating.**
