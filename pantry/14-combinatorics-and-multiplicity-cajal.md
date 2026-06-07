# CAJAL Figure Intelligence — 14-combinatorics-and-multiplicity

**Source:** `books/quantum-mechanics-vol5/chapters/14-combinatorics-and-multiplicity.md`
**Scan mode:** /scan silent
**Date:** 2026-06-06

---

## Zones Detected

| Concept | Heuristic | Notes |
|---|---|---|
| Binomial multiplicity $\Omega(N, N_\uparrow)$ peaking at $N_\uparrow = N/2$ and sharpening with $N$ | VG | Prose asserts peak sharpens; no visual grounding of shape change across scales |
| Stirling approximation accuracy: 40% error at $N=6$, negligible at thermodynamic scale | PQ | Specific relative error values given; comparison never charted against exact |
| Three statistics counting (MB / BE / FD for 2 particles in 2 states) | VG | Table counts microstates but never shows the actual configurations visually |
| Entropy additivity: multiplicities multiply, logs add, entropy is extensive | MC | Three-step chain (multiply → log → add) is load-bearing argument, purely prose |

**Density recommendation: 3 figures, Mixed density.**

---

## Figure 1 — Multiplicity Peak and Gaussian Sharpening

**Rank: CRITICAL**

**Concept statement:** The multiplicity $\Omega(N, N_\uparrow) = \binom{N}{N_\uparrow}$ peaks at $N_\uparrow/N = 0.5$ and that peak narrows dramatically with increasing $N$, making the most-probable macrostate overwhelmingly dominant at thermodynamic scale.

---

**Block 1 — Illustrae Paste Block**

Produce a full-width 120mm vector figure on a white background with two stacked panels of equal height sharing a common horizontal axis spanning 0 to 1 (representing $N_\uparrow / N$). Top panel: draw three groups of vertical bars representing the normalized discrete multiplicity $\Omega(N, N_\uparrow)/\Omega_\text{max}$ for $N = 6$ (bars colored #E69F00, wide), $N = 20$ (bars colored #0072B2, medium), and $N = 100$ (bars colored #009E73, narrow); bars are centered at each valid $N_\uparrow/N$ value and normalized so the peak equals 1; all three distributions share the same panel. Bottom panel: plot the corresponding Gaussian envelopes $\exp(-2s^2/N)$ (where $s = N_\uparrow - N/2$), normalized to 1, as smooth continuous curves with 1pt strokes in the same three colors (#E69F00, #0072B2, #009E73) and no fill, so the narrowing is clearly legible — the $N=6$ envelope is wide, $N=20$ is noticeably narrower, $N=100$ is a sharp spike near $x = 0.5$. Draw a thin vertical dashed line at $x = 0.5$ in both panels using #000000 at 0.5pt weight. The vertical axis in both panels starts at zero. No text; unannotated.

---

**Block 2 — Full SCOPE Prompt**

[S] Full-width 120mm, two equal stacked panels with shared $x$-axis from 0 to 1 ($N_\uparrow/N$), vector, white background.

[C] Top panel: exact normalized binomial multiplicity bars for $N=6$, $N=20$, $N=100$, each normalized to peak = 1. Bottom panel: Gaussian envelope $\exp(-2s^2/N)$ normalized to 1 for the same three $N$ values, derived from the Stirling approximation in the chapter's Challenge problem 9. Vertical dashed line at $N_\uparrow/N = 0.5$ in both panels. All values computable from the chapter's formula.

[O] Discrete bars first (actual counting), Gaussian curves second (analytic approximation) — the two-panel structure makes the Stirling approximation's accuracy visible. Three colors consistently map $N=6$ → #E69F00, $N=20$ → #0072B2, $N=100$ → #009E73 across both panels.

[P] Flat vector. Okabe-Ito palette only. Bars at 60% opacity. Gaussian curves solid 1pt strokes, no fill. Dashed reference line #000000 0.5pt. $y$-axis from zero. Unannotated.

[E] No text labels, no tick-mark annotations, no $\sigma$ markers, no shaded regions, no log-scale axes, no Poisson distributions, no non-binomial distributions, no fabricated data, no grid lines beyond the zero baseline.

---

**Block 3 — Negative Prompt**

No Poisson or normal distributions not derived from the Stirling expansion of $\binom{N}{N_\uparrow}$, no colored shading under curves, no error bars, no log-scale axes, no annotations of peak width or standard deviation. text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, non-standard arrows, dual-headed arrows, hand-drawn styles, visual clutter, watermarks, red-green color combinations, 3D perspective distortion.

---

## Figure 2 — Three Statistics: Explicit Microstate Enumeration

**Rank: CRITICAL**

**Concept statement:** For two particles occupying two single-particle states, Maxwell-Boltzmann counting yields 4 distinct microstates, Bose-Einstein yields 3, and Fermi-Dirac yields 1, a difference that is visceral when the configurations are shown explicitly rather than tabulated as counts.

---

**Block 1 — Illustrae Paste Block**

Produce a single-column 89mm vector figure on a white background arranged as three vertical columns, one per statistics type. Each column contains a vertical stack of rectangular microstate tiles; each tile shows two side-by-side boxes (representing state 1 on the left and state 2 on the right) with filled circles inside the boxes indicating particle occupancy. In the left column (Maxwell-Boltzmann): draw four tiles using two distinctly colored circles (#E69F00 for particle A and #0072B2 for particle B, radius 4pt each); tile 1 has both circles in box 1, tile 2 has both in box 2, tile 3 has A in box 1 and B in box 2, tile 4 has A in box 2 and B in box 1. In the center column (Bose-Einstein): draw three tiles using two identical circles (#009E73, radius 4pt); tile 1 has both in box 1, tile 2 has both in box 2, tile 3 has one in each box. In the right column (Fermi-Dirac): draw one tile using one circle (#009E73, radius 4pt) in each box. Boxes are 14pt wide by 11pt tall with #000000 1pt outlines. Tiles are separated by 4pt vertical gaps within each column; columns are separated by 10pt horizontal gaps. No text; unannotated.

---

**Block 2 — Full SCOPE Prompt**

[S] Single-column 89mm, three-column tile layout, vector, white background.

[C] Exactly the microstate configurations from the chapter table: MB has 4 microstates (both in state 1; both in state 2; A in 1 B in 2; A in 2 B in 1), BE has 3 (both in state 1; both in state 2; one in each), FD has 1 (one in each). Two distinct circle colors for MB particles (distinguishable); one circle color for BE and FD (identical particles). Configuration content is directly from chapter table.

[O] Columns left-to-right: MB (4 tiles), BE (3 tiles), FD (1 tile). Tile count decreasing left-to-right makes the counting difference immediately apparent without any labels. Consistent circle-in-box encoding across all three columns.

[P] Flat vector. Okabe-Ito: #E69F00 and #0072B2 for the two distinguishable MB particles; #009E73 for identical BE/FD particles; #000000 for box outlines. 1pt strokes. No fill on boxes. Unannotated.

[E] No wavefunctions, no Slater determinant notation, no energy-level diagrams, no spin arrows, no mathematical symbols of any kind, no hatching, no labels, no probability annotations, no grid lines.

---

**Block 3 — Negative Prompt**

No energy-level ladder diagrams, no spin-up/spin-down arrows, no Feynman diagrams, no Slater determinant notation, no quantum circuit symbols, no probability values. text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, non-standard arrows, dual-headed arrows, hand-drawn styles, visual clutter, watermarks, red-green color combinations, 3D perspective distortion.

---

## Figure 3 — Stirling Accuracy: Relative Error vs. N

**Rank: IMPORTANT**

**Concept statement:** The leading Stirling approximation $\ln N! \approx N\ln N - N$ carries a 40% relative error at $N=6$ that drops to negligible at $N \gtrsim 30$, quantifying exactly when the approximation can be trusted.

---

**Block 1 — Illustrae Paste Block**

Produce a single-column 89mm vector figure on a white background with a single-panel line chart. The horizontal axis runs from $N = 2$ to $N = 30$ at integer steps. The vertical axis starts at zero and shows relative error $|(\ln N!_\text{approx} - \ln N!_\text{exact})|/|\ln N!_\text{exact}|$ as a dimensionless fraction. Plot the relative error of the leading Stirling approximation ($N\ln N - N$) as a solid curve in #D55E00 at 1.5pt weight. Plot the relative error of the refined Stirling approximation ($N\ln N - N + \tfrac{1}{2}\ln(2\pi N)$) as a dashed curve in #0072B2 at 1.5pt weight. Both curves begin elevated at small $N$ and descend toward zero as $N$ increases. Draw a horizontal reference line at $y = 0$ in #000000 at 0.5pt weight. Place a filled circle marker of radius 4pt in #D55E00 at the coordinate $(N=6, \text{error} \approx 0.40)$ on the leading-Stirling curve, corresponding to the specific value quoted in the chapter. No text; unannotated.

---

**Block 2 — Full SCOPE Prompt**

[S] Single-column 89mm, single panel, vector, white background.

[C] Relative error of $\ln N!$ for the leading Stirling approximation ($N\ln N-N$) and the refined form ($N\ln N - N + \frac{1}{2}\ln(2\pi N)$) versus $N$ from 2 to 30. The 40% relative error at $N=6$ for the leading approximation is explicitly stated in the chapter. Zero reference line. Point marker at $N=6$ on the leading curve. All values are analytically computable from the formulas in the chapter.

[O] Single panel. Leading-error curve (#D55E00 solid) is the primary object. Refined-error curve (#0072B2 dashed) sits below it, visually demonstrating the refinement's benefit. Both curves asymptote toward zero, showing when each approximation becomes reliable.

[P] Flat vector. Okabe-Ito: #D55E00 solid 1.5pt (leading), #0072B2 dashed 1.5pt (refined), #000000 0.5pt (reference line). $y$-axis from zero. Unannotated.

[E] No tick labels, no absolute values of $\ln N!$, no log-scale $y$-axis, no shaded uncertainty bands, no comparison to approximations not in the chapter (no asymptotic expansions beyond the two forms named).

---

**Block 3 — Negative Prompt**

No logarithmic $y$-axis, no absolute factorial curves, no additional Stirling terms beyond the two in the chapter, no shading under curves, no comparison to Gamma function or other extensions. text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, non-standard arrows, dual-headed arrows, hand-drawn styles, visual clutter, watermarks, red-green color combinations, 3D perspective distortion.

---

## Video Candidate Pass

**VIDEO CANDIDATE — Gaussian Sharpening of the Multiplicity Peak**

The continuous narrowing of $\Omega(N, N_\uparrow)/\Omega_\text{max}$ as $N$ grows from 6 toward $10^{23}$ is both the central physical claim of the chapter and a transition mechanism that unfolds across scales impossible to compress into a static panel. Showing the distribution animate from a broad histogram at $N=6$ through the intermediate regime to a needle-thin spike satisfies the sequential causal stages criterion: (1) flat-to-broad distribution at $N \sim 6$; (2) progressive concentration through $N \sim 100$; (3) effective delta-function at thermodynamic scale — and the transformation between stages is the learning target, not the endpoints alone. Figure 1 covers this partially as a static snapshot; the video would extend it as a continuous sweep over $N$ with a running indicator of $\sigma/N = 1/\sqrt{2N}$.

**Total video candidates: 1.**
**Recommendation:** Animate the normalized multiplicity $\Omega(N, N_\uparrow)/\Omega_\text{max}$ as $N$ sweeps from 6 to 200, with the Gaussian envelope overlaid and a shrinking $\sigma/N$ readout demonstrating the vanishing relative width. Pause at $N=6$, $N=20$, $N=100$ to correspond to Figure 1 checkpoints.
