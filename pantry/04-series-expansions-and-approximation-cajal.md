# CAJAL Figure Report — Module M-04 — Series Expansions and Approximation

Recommended: 3 figures, Mixed density.

---

## Figure 1 — Taylor truncation error as a function of expansion order

**Heuristic:** PQ | **Rank:** Critical

---

**BLOCK 1 — ILLUSTRAE PASTE BLOCK**

Draw four overlapping smooth curves on a shared horizontal axis spanning from 0 to approximately 1.5 radians. The first curve is the exact sine function — a smooth arc rising from the origin. The remaining three curves are successive truncations of the Taylor series: the one-term approximation (a straight line through the origin with unit slope), the three-term approximation (a cubic that tracks the sine well before curving away), and the five-term approximation (a quintic that stays close to the exact curve over the full range). Below the main panel, place a second panel showing the absolute error of each truncation — three monotonically rising curves starting at zero. Mark a vertical dashed reference line at approximately 0.26 radians (15 degrees) and a second at 0.087 radians (5 degrees). All y-axes start at zero. No text baked into the image.

**BLOCK 2 — FULL SCOPE**

- `[S — SPECIFICATION]` Single-column, 89 mm width, 300 DPI, vector (SVG/EPS), white background. Two stacked panels sharing a horizontal axis; upper panel height roughly 60%, lower panel 40%.
- `[C — CONTENT]` Exact sine function; first-order Taylor truncation (linear); third-order truncation (cubic); fifth-order truncation (quintic); absolute error of each truncation in the lower panel; reference verticals at 5° and 15° (0.087 and 0.262 rad).
- `[O — ORGANIZATION]` Upper panel: x-axis = angle in radians 0–1.5, y-axis = function value 0–1.2; four curves in distinct colors. Lower panel: x-axis identical, y-axis = absolute error starting at zero; three error curves. Shared vertical dashed reference lines drop through both panels.
- `[P — PRESENTATION]` Flat vector, Okabe-Ito palette: exact sine = Blue `#0072B2` (dominant); order-1 = Vermillion `#D55E00`; order-3 = Orange `#E69F00`; order-5 = Bluish Green `#009E73`. Error curves mirror the same colors at reduced opacity. Reference verticals in light gray. Uniform 1 pt strokes, white background. No baked text.
- `[E — EXCLUSIONS]` Omit cosine truncations, exponential series, binomial approximation, Maclaurin vs. Taylor distinction, complex-plane convergence disks, any discussion of asymptotic series.

**BLOCK 3 — NEGATIVE PROMPT**

cosine curves, exponential curves, complex plane diagram, convergence radius circle, binomial curves, 3D surface, shaded convergence region, text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, dual-headed arrows, hand-drawn styles, human figures, visual clutter, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 2 — Every smooth potential minimum is locally a harmonic oscillator

**Heuristic:** VG | **Rank:** Critical

---

**BLOCK 1 — ILLUSTRAE PASTE BLOCK**

Draw a single smooth potential-energy curve with a broad, asymmetric well — steeper on the left side than the right, with a shallow minimum near the center of the horizontal axis. Mark the minimum point with a filled circle. From that point, overlay a symmetric parabola (the harmonic approximation) that is tangent to the well at the minimum and diverges from it as displacement increases on both sides. Use two clearly different colors for the two curves. Add two short vertical bracket marks flanking the minimum to indicate the region of valid approximation — where the two curves are nearly coincident — and a wider bracket on each side to indicate where they diverge. Place a small horizontal arrow indicating the displacement coordinate measured from the minimum. No text baked into the image.

**BLOCK 2 — FULL SCOPE**

- `[S — SPECIFICATION]` Single-column, 89 mm width, 300 DPI, vector (SVG/EPS), white background. Single panel.
- `[C — CONTENT]` An asymmetric anharmonic potential well (Morse-like shape, steeper left flank, shallower right); the harmonic (parabolic) approximation overlaid, tangent at the minimum; the minimum point marked; a bracket or shaded band indicating the region of agreement; a displacement arrow from the minimum.
- `[O — ORGANIZATION]` Horizontal axis = displacement from equilibrium (centered at minimum); vertical axis = potential energy, starting at zero at the bottom of the panel. The potential well sits in the lower half; both curves enter from the left, descend to the minimum, then diverge as displacement increases. The region of overlap is clearly narrower than the full horizontal range.
- `[P — PRESENTATION]` Flat vector, Okabe-Ito: anharmonic potential = Blue `#0072B2`; harmonic approximation = Orange `#E69F00`; minimum marker = filled circle in Sky Blue `#56B4E9`; overlap band = light gray fill. Uniform 1 pt strokes. White background. No baked text.
- `[E — EXCLUSIONS]` Omit specific molecule labels, Morse-potential formula curves, quantum energy levels drawn inside the well, wavefunction profiles, higher-order Taylor correction overlays, multiple expansion points.

**BLOCK 3 — NEGATIVE PROMPT**

quantum energy level rungs, wavefunction curves inside well, molecular bond labels, Morse formula annotation, multiple expansion points, text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, dual-headed arrows, hand-drawn styles, human figures, visual clutter, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 3 — Perturbation theory as a Taylor expansion: convergence and its breakdown at degeneracy

**Heuristic:** MC | **Rank:** Important

---

**BLOCK 1 — ILLUSTRAE PASTE BLOCK**

Draw a two-column comparison diagram. Left column: a vertical energy-level ladder with two well-separated levels labeled only by position. A small horizontal perturbation arrow enters from the right. The levels shift slightly — indicate the shifted positions with short tick marks offset to the right of the original levels. This represents the convergent case. Right column: the same two-level ladder but now with the levels close together — nearly degenerate. The same perturbation arrow appears. The shifted levels now show one pushed strongly upward and one pushed strongly downward, with diverging curved bracket lines indicating large mixing. A bold jagged or broken line between the two columns signals the contrast. All relationships are structural and geometric; no formulas or labels baked into the image.

**BLOCK 2 — FULL SCOPE**

- `[S — SPECIFICATION]` Single-column, 89 mm width, 300 DPI, vector (SVG/EPS), white background. Two side-by-side panels connected by a central divider element; each panel is a vertical energy diagram.
- `[C — CONTENT]` Left panel: two well-separated horizontal level lines; a perturbation arrow from the side; small displaced copies of each level indicating first-order shifts. Right panel: two nearly coincident level lines; same perturbation arrow; dramatically displaced copies with curved bracket lines indicating large mixing (inferred relation: proximity of levels causes large mixing — label as inferred via dashed bracket rather than solid).
- `[O — ORGANIZATION]` Both panels share a common vertical energy axis orientation (up = higher energy). Levels are drawn as horizontal bars. Perturbation arrows enter from the right side of each panel. Shifted levels sit to the right of their originals. Mixing brackets open outward in the degenerate panel. A vertical dividing line or bold separator between the panels.
- `[P — PRESENTATION]` Flat vector, Okabe-Ito: unperturbed levels = Blue `#0072B2`; perturbation arrows = Orange `#E69F00`; shifted levels = Bluish Green `#009E73`; mixing/divergence brackets = Vermillion `#D55E00`; divider = light gray. Uniform 1 pt strokes; mixing brackets 1.5 pt. White background. No baked text.
- `[E — EXCLUSIONS]` Omit WKB turning points, specific hydrogen-atom levels, three-or-more-level systems, time-dependent perturbation, actual numerical energy values, formulas baked into the figure.

**BLOCK 3 — NEGATIVE PROMPT**

WKB wavefunction curves, turning point marks, hydrogen spectral lines, three-level diagrams, time-evolution arrows, numerical axis labels, formula text, text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, dual-headed arrows, hand-drawn styles, human figures, visual clutter, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Video Candidate Pass

**Figure 1 — Taylor truncation error curves**
STATIC SUFFICIENT. The comparison of truncation orders is a simultaneous overlay, not a sequential process with causal staging; a static panel with color-coded curves conveys the relationship fully.

**Figure 2 — Potential minimum as harmonic oscillator**
STATIC SUFFICIENT. The structural relationship between the anharmonic well and its parabolic approximation is a spatial/geometric claim that a static overlay communicates completely.

**Figure 3 — Perturbation convergence vs. degeneracy**
VIDEO CANDIDATE. Criterion: transition mechanism is the learning target. The key insight is that as the level spacing continuously shrinks toward zero the perturbation shift transitions from small and well-behaved to large and divergent — a continuous transformation that a single static side-by-side cannot fully convey. Recommend this as the one video for the module: animate the right-panel levels sliding together while the mixing brackets grow, making the radius-of-convergence failure visible as a dynamic process.
