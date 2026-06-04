# CAJAL Figure Report — Module M-11 — Special Functions: Hermite, Legendre, Laguerre, Spherical Harmonics, Bessel

Recommended: 2 figures, Foundational density.

---

## Figure 1 — Sturm–Liouville Taxonomy: Seven Special-Function Families from One Structure

**Heuristic:** VG — Verification Gap
**Rank:** Critical

---

**BLOCK 1 — ILLUSTRAE PASTE BLOCK:**

Draw a two-level hierarchy diagram. At the top, a single wide anchor box represents the Sturm–Liouville self-adjoint operator — the unifying structure. From this box, seven branches descend to seven leaf boxes arranged in a horizontal row, each representing one special-function family. The branches connect via angled lines from the anchor to each leaf. Each leaf box contains only a geometric shape or icon distinguishing it: a smooth oscillatory arc (Hermite), a dome-shaped curve (Legendre), a dome with a kink/inflection (associated Legendre), a sphere surface outline (spherical harmonics), a decaying oscillation to the right (associated Laguerre), a damped oscillation starting from zero (spherical Bessel), and a horizontal oscillation (cylindrical Bessel). To the right of each leaf box, a small property badge carries only a color band — not text — indicating the quantization mechanism: series-termination families use Bluish Green badges, regularity-at-endpoint families use Orange badges, asymptotic-form families use Sky Blue badges. Color the anchor box Blue, the branch lines neutral gray, the leaf boxes light gray with a 1pt Blue stroke. Flat vector, Okabe-Ito palette, white background, uniform 1pt strokes, no baked text.

---

**BLOCK 2 — FULL SCOPE:**

- `[S — SPECIFICATION]` Single-column 89 mm width, 300 DPI, vector (SVG/EPS), white background, two-level hierarchy with the anchor box spanning full column width and seven leaf boxes in a horizontal row below.

- `[C — CONTENT]` Exactly seven leaf nodes, left to right in order matching the module catalogue: Hermite, Legendre, Associated Legendre, Spherical Harmonics, Associated Laguerre, Spherical Bessel, Cylindrical Bessel. The anchor node represents the Sturm–Liouville self-adjoint operator as the shared parent. Each leaf has a distinguishing shape icon (described above) and a color-coded quantization-mechanism badge. Three badge colors: Bluish Green = series termination (Hermite, Associated Laguerre); Orange = regularity at endpoint (Legendre, Associated Legendre, Spherical Harmonics); Sky Blue = asymptotic/boundary-zeros (Spherical Bessel, Cylindrical Bessel). No interval or weight information is shown.

- `[O — ORGANIZATION]` Two tiers. Anchor box: full-width rectangle at top. Branch lines: seven angled lines descending from the bottom edge of the anchor box to the top edges of the seven leaf boxes. Leaf boxes: uniform size, evenly spaced, aligned along a common horizontal baseline. Badge: small rectangle or circle at the right edge of each leaf box, flush with the leaf boundary. No labels, no text.

- `[P — PRESENTATION]` Flat vector. Blue `#0072B2` for anchor box fill and stroke. Bluish Green `#009E73` for series-termination badges. Orange `#E69F00` for regularity badges. Sky Blue `#56B4E9` for asymptotic badges. Light gray `#CCCCCC` for leaf box fills, 1pt Blue stroke on each. Neutral gray for branch lines. Uniform 1pt strokes throughout. White background. No baked text. No gradient fills.

- `[E — EXCLUSIONS]` Omit: orthogonality weight functions, interval notation, QM system names, polynomial coefficients, recurrence relations, the Wronskian, Sturm–Liouville boundary terms, any representation of the ODE, spin functions, non-polynomial families beyond those in the module catalogue.

---

**BLOCK 3 — NEGATIVE PROMPT:**

orthogonality integral symbols, interval bracket notation, ODE formula panels, Wronskian diagram, polynomial coefficient table, recurrence arrow loops, spin-state representations, non-QM function families, text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, dual-headed arrows, hand-drawn styles, human figures, visual clutter, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 2 — Harmonic Oscillator Eigenstates: Hermite Polynomial Node Count (n = 0 to 3)

**Heuristic:** PQ — Proportional/Quantitative
**Rank:** Important

---

**BLOCK 1 — ILLUSTRAE PASTE BLOCK:**

Draw a four-panel comparison chart with a shared vertical axis and four horizontally aligned panels, one per quantum number n = 0, 1, 2, 3. In each panel, draw the smooth probability-amplitude wavefunction profile — a Gaussian-envelope modulated curve — that has exactly n zero crossings (nodes). The n = 0 panel shows a single smooth Gaussian peak with no nodes. The n = 1 panel shows one zero crossing with a positive lobe on the left and a negative lobe on the right, both enveloped by the decaying Gaussian. The n = 2 panel shows two zero crossings with three alternating lobes. The n = 3 panel shows three zero crossings with four alternating lobes. All four panels share a common horizontal baseline (y = 0) drawn as a thin gray rule. Positive lobes are filled with Bluish Green at 40% opacity; negative lobes with Vermillion at 40% opacity. The Gaussian envelope is shown as a thin dashed curve in Orange over each panel. The y-axis starts at zero for the envelope; the wavefunction amplitude can go negative. Flat vector, Okabe-Ito palette, white background, uniform 1pt strokes, no baked text.

---

**BLOCK 2 — FULL SCOPE:**

- `[S — SPECIFICATION]` Single-column 89 mm width, 300 DPI, vector (SVG/EPS), white background, four equal-width panels sharing a continuous baseline axis. A shared vertical amplitude axis appears at the left edge only.

- `[C — CONTENT]` Four wavefunction profiles for n = 0, 1, 2, 3 of the quantum harmonic oscillator, each modulated by the Gaussian envelope $e^{-\xi^2/2}$. The node count in each panel is exactly equal to n. Positive lobes are visually distinct from negative lobes by fill color. The Gaussian envelope is shown as a dashed reference curve. No energy eigenvalue marks, no probability density (no squaring), no classical turning points, no potential well shape.

- `[O — ORGANIZATION]` Four panels arranged horizontally, equal width, separated by thin vertical dividers. Shared horizontal baseline at y = 0 runs continuously across all four panels. Vertical amplitude axis on the left, originating at the shared baseline. Panels ordered n = 0, 1, 2, 3 from left to right. Each wavefunction curve is centered vertically within its panel. The Gaussian envelope dashed curve is superimposed on each panel.

- `[P — PRESENTATION]` Flat vector. Bluish Green `#009E73` at 40% fill opacity for positive lobes. Vermillion `#D55E00` at 40% fill opacity for negative lobes. Orange `#E69F00` dashed curve for Gaussian envelope. Baseline gray `#AAAAAA` for the y = 0 rule and panel dividers. Wavefunction curves in Blue `#0072B2` at full opacity, 1.5pt stroke. Uniform 1pt strokes for axes and dividers. White background. No baked text.

- `[E — EXCLUSIONS]` Omit: probability density plots (no $|\psi|^2$ panels), potential well $V(x)$, classical turning-point markers, energy eigenvalue labels, ladder-operator arrows, recurrence arrows linking panels, any 2D or 3D spatial probability density.

---

**BLOCK 3 — NEGATIVE PROMPT:**

probability density plots, potential well curve, classical turning point markers, energy eigenvalue tick marks, ladder operator arrows, recurrence arrows, 2D orbital density maps, text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, dual-headed arrows, hand-drawn styles, human figures, visual clutter, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Video Candidate Pass

**Figure 1 — Sturm–Liouville Taxonomy:**
STATIC SUFFICIENT. The hierarchy is a classification structure — all branches are co-equal descendants of the same parent, with no causal sequence among them. The spatial layout communicates the taxonomy fully in a single static frame.

**Figure 2 — Hermite Polynomial Node Count:**
STATIC SUFFICIENT. The four panels are a parallel comparison on a shared axis, not a temporal or causal sequence. The progression n = 0 → 3 is a discrete parameter scan, fully legible in static side-by-side panels. No transition mechanism is the learning target.
