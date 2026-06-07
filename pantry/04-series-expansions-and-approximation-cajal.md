# CAJAL Figure Intelligence — 04-series-expansions-and-approximation

**Source:** /Users/bear/Documents/CoWork/bear-textbooks/books/quantum-mechanics-vol5/chapters/04-series-expansions-and-approximation.md
**Scan:** /scan silent
**Date:** 2026-06-06

---

## Zones Detected

| Concept | Zone | Rationale |
|---|---|---|
| Taylor truncation error vs. expansion order | PQ | Quantitative claim: error is ≈ θ²/6 for sin, error grows with distance from expansion point; specific values 5°, 15° cited |
| Every smooth potential minimum is a QHO | VG | Geometric claim: anharmonic well and parabola are tangent at minimum, diverge away — structural, no figure |
| Perturbation theory as Taylor expansion | MC | 3-step mechanism: perturbation small → expansion converges → near-degenerate denominator → convergence fails |
| Small-angle approximation accuracy | PQ | Specific quantitative thresholds (1% at 15°, 0.1% at 5°) — chart with y-axis at zero required |
| Convergent vs. asymptotic series | VG | Structural distinction: series converges everywhere vs. diverges but first terms accurate — geometric claim |
| Pendulum correction as Taylor result | VG + PQ | Specific value θ₀² correction with 1.6% at 0.5 rad — quantitative confirmation |

**Density recommendation: 3 figures, Mixed density.**

---

## Figure 1 — CRITICAL

**Concept:** Taylor truncation of sin(x) shows accuracy increasing with expansion order near x = 0 and decreasing with distance from the expansion point, with quantifiable error from the first omitted term.

**Block 1 — Illustrae Paste Block:**
Draw on a single-column 89mm wide vector canvas with white background in two vertically stacked panels sharing a horizontal axis from x = 0 to x = 1.5. Upper panel (60% height): draw a vertical y-axis from 0 to 1.2 in #000000 at 0.5pt. Draw four smooth curves: exact sin(x) in #0072B2 at 2pt; the linear approximation x in #D55E00 at 1pt; the cubic approximation x − x³/6 in #E69F00 at 1pt; the quintic approximation x − x³/6 + x⁵/120 in #009E73 at 1pt. All four curves start at origin. Draw two vertical dashed reference lines at x = 0.087 and x = 0.262 in #000000 at 0.5pt dropping through both panels. Lower panel (40% height): draw a vertical y-axis from 0 upward in #000000 at 0.5pt starting at zero. Draw three smooth error curves (absolute deviation of each approximation from exact sin) in #D55E00, #E69F00, #009E73 at 1pt each, all starting at zero and rising monotonically. No text; unannotated.

**Block 2 — Full SCOPE Prompt:**
[S] Single-column 89mm wide vector figure, two stacked panels sharing horizontal axis, white background.
[C] Upper panel: exact sin(x) in blue; first-order linear approximation; third-order cubic approximation; fifth-order quintic approximation — all starting at origin and spanning 0 to 1.5 rad. Lower panel: absolute error of each truncation starting at zero — three curves corresponding to the three approximations. Vertical reference lines at 0.087 rad (5°) and 0.262 rad (15°) through both panels. All y-axes starting at zero.
[O] Upper panel: exact curve most curved, linear most divergent above x ≈ 0.5; curves separate progressively right of origin; quintic closest to exact longest. Lower panel: all three error curves start at zero, rise monotonically, quintic error lowest. Reference verticals drop into both panels.
[P] Flat vector, Okabe-Ito hexes: exact sin #0072B2 2pt; order-1 #D55E00 1pt; order-3 #E69F00 1pt; order-5 #009E73 1pt; reference verticals #000000 dashed 0.5pt; axes #000000 0.5pt; unannotated.
[E] No cosine truncations; no exponential series; no binomial approximation; no complex-plane convergence disk; no asymptotic series; no axis tick number labels; no radian/degree mixed labeling.

**Block 3 — Negative Prompt:**
No axis tick labels, no curve name labels, no degree or radian values marked, no cosine curves, no exponential series, no convergence disk; text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, non-standard arrows, dual-headed arrows, hand-drawn styles, visual clutter, watermarks, red-green color combinations, 3D perspective distortion.

---

## Figure 2 — CRITICAL

**Concept:** Every smooth potential minimum looks like a harmonic oscillator (parabola) locally — the Taylor expansion zeroes out the linear term and the quadratic coefficient gives the effective spring constant; anharmonic corrections appear only away from the minimum.

**Block 1 — Illustrae Paste Block:**
Draw on a single-column 89mm wide vector canvas with white background. Draw a horizontal x-axis in #000000 at 0.5pt and a vertical y-axis from y = 0 upward in #000000 at 0.5pt. Draw a smooth asymmetric potential well in #0072B2 at 1.5pt — steeper on the left flank, shallower and more gradually rising on the right — with a minimum near x = 0, resembling a Morse-like shape. Place a filled 3pt dot at the minimum in #000000. From the minimum, draw a symmetric parabola in #E69F00 at 1.5pt that is tangent to the well curve at the minimum and diverges visibly from it for large displacements on both sides. Draw a gray shaded band of light fill (#000000 at 5% opacity) between the two curves in the region where they nearly coincide, spanning roughly one-third of the horizontal extent. No text; unannotated.

**Block 2 — Full SCOPE Prompt:**
[S] Single-column 89mm wide vector figure, white background.
[C] Asymmetric anharmonic potential well (steeper left flank, shallower right) with a well-defined minimum; harmonic parabolic approximation overlaid, tangent to the well at the minimum and matching its curvature at that point; minimum point marked; shaded region of agreement flanking the minimum where both curves are close; curves diverge beyond the agreement region. Vertical axis starts at zero.
[O] Minimum at horizontal center; both curves descend to minimum from both sides; parabola symmetric about minimum; potential well asymmetric; divergence between curves clearly visible at large displacements; shaded agreement band visually narrow relative to full x-range.
[P] Flat vector, Okabe-Ito hexes: anharmonic potential #0072B2 1.5pt; harmonic parabola #E69F00 1.5pt; minimum dot #000000 3pt; agreement band light gray fill; axes #000000 0.5pt; unannotated.
[E] No quantum energy level rungs inside the well; no wavefunction curves; no molecular labels; no Morse formula annotation; no multiple expansion points; no higher-order correction overlay curves; no axis tick numbers.

**Block 3 — Negative Prompt:**
No quantum energy level rungs, no wavefunction profiles, no molecular bond labels, no Morse potential formula, no multiple expansion points, no axis tick values; text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, non-standard arrows, dual-headed arrows, hand-drawn styles, visual clutter, watermarks, red-green color combinations, 3D perspective distortion.

---

## Figure 3 — IMPORTANT

**Concept:** Perturbation theory converges when level spacing is large relative to the coupling matrix element; near degeneracy the denominator shrinks and the same perturbation drives large level mixing — a radius-of-convergence failure.

**Block 1 — Illustrae Paste Block:**
Draw on a full-width 120mm wide vector canvas with white background in two side-by-side panels. Left panel: draw a vertical energy axis in #000000 at 0.5pt. Draw two horizontal level bars well separated vertically in #0072B2 at 2pt. Draw a short horizontal arrow entering from the right at each level in #E69F00 at 1pt. Draw the two levels slightly shifted (small displacement) to the right of the originals in #009E73 at 1.5pt dashed, indicating small first-order shifts. Right panel: same layout but draw the two original level bars in #0072B2 very close together vertically (nearly degenerate). Draw the same horizontal perturbation arrows in #E69F00. Draw the two shifted levels in #009E73 dashed now far apart — one pushed strongly upward, one strongly downward — with curved bracket lines in #D55E00 at 1pt connecting each original to its shifted position, indicating large mixing. A thin vertical separator between panels in #000000. No text; unannotated.

**Block 2 — Full SCOPE Prompt:**
[S] Full-width 120mm wide two-panel vector figure, white background.
[C] Left panel: two well-separated energy levels; perturbation arrows; small shifted copies showing first-order corrections that are small relative to level spacing. Right panel: two nearly degenerate levels (close together); same perturbation arrows; shifted copies pushed far apart; curved mixing brackets showing dramatically large level repulsion. Visual contrast between small shifts (left) and large shifts (right) is the primary message.
[O] Both panels same height; left panel levels clearly separated by large gap; right panel levels nearly touching; shifted levels in right panel span most of vertical height; mixing brackets only in right panel; thin separator between panels.
[P] Flat vector, Okabe-Ito hexes: original levels #0072B2 2pt; perturbation arrows #E69F00; shifted levels #009E73 dashed 1.5pt; mixing brackets #D55E00 1pt; separator #000000 0.5pt; unannotated.
[E] No WKB wavefunction curves; no specific hydrogen atom levels; no three-or-more-level systems; no time-dependent perturbation arrows; no numerical energy values; no axis tick labels; no QHO levels.

**Block 3 — Negative Prompt:**
No energy value annotations, no level number labels, no WKB curves, no hydrogen atom spectral lines, no three-level diagrams, no time-evolution arrows; text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, non-standard arrows, dual-headed arrows, hand-drawn styles, visual clutter, watermarks, red-green color combinations, 3D perspective distortion.

---

## Video Candidate Pass

**VIDEO CANDIDATE — Figure 3 (perturbation convergence breakdown):** The learning target is the continuous transition mechanism: as the level spacing shrinks toward zero, the perturbation expansion transitions from small, well-behaved corrections to large, divergent mixing. This is a 3-stage causal process (spacing decreases → denominator shrinks → shifts explode) with a transition below direct observation (the algebraic pole in the perturbation series). An animation showing the two levels sliding together while the shift magnitudes grow would make the radius-of-convergence concept viscerally clear.

**Count: 1 video candidate.**
**Recommendation:** Animate Figure 3 — have the right-panel levels start well-separated and slide continuously together while the corrected level positions update in real time, showing the mixing brackets growing and then diverging. This directly embeds the "perturbation theory breaks down at degeneracy" message in a causal visual.
