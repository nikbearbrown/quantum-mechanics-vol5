# CAJAL Figure Intelligence — 06-the-fourier-transform

**Source:** /Users/bear/Documents/CoWork/bear-textbooks/books/quantum-mechanics-vol5/chapters/06-the-fourier-transform.md
**Scan:** /scan silent
**Date:** 2026-06-06

---

## Zones Detected

| Concept | Zone | Rationale |
|---|---|---|
| Fourier series → Fourier transform as L → ∞ | MC | 3-step mechanism: discrete comb at spacing 2π/L → spacing shrinks as L grows → sum becomes integral |
| Gaussian wave packet: Δx·Δp trade-off | VG + PQ | Geometric/structural claim (narrow x ↔ wide p) with specific product Δx·Δp = ħ/2; no figure |
| Convolution theorem | VG | Structural claim: real-space convolution ↔ frequency-domain multiplication; no visual grounding |
| Born amplitude as Fourier transform of V | VG | Scattering amplitude = ṼV(q) — geometric claim about scattering geometry and transform connection |
| Bandwidth relation and uncertainty principle | VG | Two routes (Fourier vs. Robertson) distinguished in prose only — structural claim needing geometric contrast |
| Wave packet spreading in time | MC | 3-stage causal chain: narrow Δx → wide Δp → different speeds → packet broadens in time |

**Density recommendation: 4 figures, Mixed density.**

---

## Figure 1 — CRITICAL

**Concept:** As the period L grows without bound, the Fourier series discrete frequency comb progressively fills in until in the limit L → ∞ it becomes the continuous Fourier transform spectrum.

**Block 1 — Illustrae Paste Block:**
Draw on a single-column 89mm wide vector canvas with white background in three vertically stacked panels of equal height, all sharing the same horizontal k-axis from −4 to +4 units. Top panel: draw a vertical amplitude axis from y = 0 upward in #000000 at 0.5pt; draw approximately 8 vertical spike lines of equal height in #0072B2 at 1pt, evenly spaced with spacing Δk_large, arranged symmetrically about k = 0, representing the Fourier series coefficients at period L₁. Middle panel: same axes; draw approximately 16 vertical spike lines in #0072B2 at 1pt, spaced at Δk_large/2, representing period 2L₁. Bottom panel: same axes; draw a smooth continuous bell-shaped envelope curve in #E69F00 at 1.5pt, representing the Fourier transform; draw ghost spike lines at the middle-panel spacing in #0072B2 at 0.3pt (very faint). Draw a single downward arrow along the right margin spanning all three panels in #56B4E9 at 1pt. No text; unannotated.

**Block 2 — Full SCOPE Prompt:**
[S] Single-column 89mm wide vector figure, three stacked equal-height panels sharing horizontal k-axis, white background.
[C] Top panel: discrete spike comb with spacing Δk (large, ~8 spikes). Middle panel: denser comb with spacing Δk/2 (~16 spikes). Bottom panel: smooth continuous bell-shaped envelope (the Fourier transform limit), with faint ghost comb marks. All three panels share the same k-axis range. Vertical amplitude axes starting at zero on all panels. Right-margin downward progression arrow.
[O] All three panels same width and horizontal axis range; spike heights roughly equal within each panel; envelope curve in bottom panel approximates the same shape as the spike envelope; ghost combs at very low opacity just visible; spacing visibly halved from top to middle.
[P] Flat vector, Okabe-Ito hexes: spike combs #0072B2 1pt; envelope curve #E69F00 1.5pt; ghost combs #0072B2 0.3pt; progression arrow #56B4E9 1pt; axes #000000 0.5pt; unannotated.
[E] No time-domain function panels; no QM momentum convention factor; no Plancherel normalization labels; no Dirac delta spike; no convolution diagram; no named function labels (Gaussian, sinc); no axis tick number labels.

**Block 3 — Negative Prompt:**
No time-domain panels, no wavefunction labels, no named function annotations, no Dirac delta, no convolution arrows, no axis tick values; text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, non-standard arrows, dual-headed arrows, hand-drawn styles, visual clutter, watermarks, red-green color combinations, 3D perspective distortion.

---

## Figure 2 — CRITICAL

**Concept:** For a Gaussian wave packet, position-space width Δx and momentum-space width Δp are reciprocally related — narrowing one forces widening the other — with the Gaussian being the unique state achieving the minimum product Δx·Δp = ħ/2.

**Block 1 — Illustrae Paste Block:**
Draw on a full-width 120mm wide vector canvas with white background in a 2×2 grid of panels. Top-left: draw horizontal axis (position x) and vertical axis from y = 0 upward in #000000 at 0.5pt; draw a narrow, tall Gaussian bell curve in #56B4E9 at 1.5pt. Top-right: same axes; draw a wide, low Gaussian curve in #E69F00 at 1.5pt. Bottom-left: draw horizontal axis (momentum p) and vertical axis from y = 0 upward in #000000 at 0.5pt; draw a wide, low Gaussian curve in #56B4E9 at 1.5pt, with width matched reciprocally to the top-left. Bottom-right: same axes; draw a narrow, tall Gaussian curve in #E69F00 at 1.5pt, reciprocal to the top-right. Draw small horizontal bracket markers at half-maximum height on all four curves in #000000 at 0.5pt to indicate widths. No text; unannotated.

**Block 2 — Full SCOPE Prompt:**
[S] Full-width 120mm wide 2×2 grid of panels, white background.
[C] Four Gaussian probability density curves: top-left narrow in x (small Δx, state A); bottom-left wide in p (large Δp, same state A); top-right wide in x (large Δx, state B); bottom-right narrow in p (small Δp, same state B). Width brackets at half-maximum on all four. All four y-axes starting at zero. Color pairing: state A = #56B4E9 (top-left and bottom-left); state B = #E69F00 (top-right and bottom-right). The visual message: narrow top pairs with wide bottom within each column.
[O] 2×2 grid; top row = position space; bottom row = momentum space; left column = localized-in-x state; right column = delocalized-in-x state; width contrast between top-left (narrow) and top-right (wide) clearly visible; same contrast inverted in bottom row.
[P] Flat vector, Okabe-Ito hexes: state A #56B4E9 1.5pt; state B #E69F00 1.5pt; width brackets #000000 0.5pt; axes #000000 0.5pt; unannotated.
[E] No time evolution; no complex phase factors; no Robertson commutator diagram; no energy-time uncertainty; no sinusoidal oscillation inside the packet; no axis tick numbers; no Δx·Δp product annotation.

**Block 3 — Negative Prompt:**
No axis tick values, no Greek letter labels, no width annotations "Δx" or "Δp", no time-evolution panels, no complex wavefunction panels, no commutator diagram; text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, non-standard arrows, dual-headed arrows, hand-drawn styles, visual clutter, watermarks, red-green color combinations, 3D perspective distortion.

---

## Figure 3 — IMPORTANT

**Concept:** Wave packet spreading in time is a consequence of the Fourier bandwidth relation: a narrow initial Δx requires broad Δp, different momentum components travel at different speeds, and the packet broadens as t increases.

**Block 1 — Illustrae Paste Block:**
Draw on a full-width 120mm wide vector canvas with white background in three horizontally arranged panels at t₁ < t₂ < t₃. Left panel: draw a horizontal x-axis in #000000 at 0.5pt and vertical axis from y = 0 upward; draw a narrow tall Gaussian curve in #0072B2 at 1.5pt centered at x₀ with a horizontal width bracket. Middle panel: draw same axes; draw a moderately wider and shorter Gaussian in #0072B2 at 1.5pt centered slightly right of x₀; same bracket wider. Right panel: draw same axes; draw a broad flat Gaussian in #0072B2 at 1.5pt centered further right; bracket correspondingly widest. Mark the center position of each Gaussian with a filled 3pt dot in #009E73 at the same horizontal position; connect the three dots with a dashed horizontal guide in #009E73 at 0.5pt to indicate that the center travels at constant speed while the shape broadens. All y-axes start at zero and scaled so all three curves have equal area. No text; unannotated.

**Block 2 — Full SCOPE Prompt:**
[S] Full-width 120mm wide three-panel figure, white background.
[C] Three snapshots of a Gaussian wave packet at three successive times: t₁ (narrow, tall), t₂ (intermediate width), t₃ (broad, flat). The center of each Gaussian moves to the right at a constant group velocity. All three Gaussians have the same area (normalization preserved). Width bracket on each showing broadening. Center-position dots connected by a dashed guide line showing constant-speed center motion.
[O] Left-to-right time progression; each successive Gaussian noticeably wider and shorter than the previous; center position advances to the right at uniform rate; all y-axes starting at zero; curves same color to indicate same state at different times.
[P] Flat vector, Okabe-Ito hexes: Gaussian curves #0072B2 1.5pt; center dots #009E73 3pt; center guide #009E73 dashed 0.5pt; width brackets #000000 0.5pt; axes #000000 0.5pt; unannotated.
[E] No complex phase oscillations inside packets; no separate plots of Δp; no Robertson commutator; no energy-time diagram; no axis tick values; no multiple-component decomposition; no dispersion relation curve.

**Block 3 — Negative Prompt:**
No axis tick labels, no time labels "t₁ t₂ t₃", no Δx annotations, no phase oscillations, no dispersion relation overlay, no decomposition into k-components; text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, non-standard arrows, dual-headed arrows, hand-drawn styles, visual clutter, watermarks, red-green color combinations, 3D perspective distortion.

---

## Figure 4 — SUPPLEMENTARY

**Concept:** In Born scattering, the differential cross-section is the squared Fourier transform of the potential evaluated at the momentum transfer q = 2k·sin(θ/2), so forward scattering (small q) probes the spatial integral of V while large-angle scattering (large q) probes its fine structure.

**Block 1 — Illustrae Paste Block:**
Draw on a single-column 89mm wide vector canvas with white background in two side-by-side panels. Left panel (45% width): draw two arrows from a central filled circle in #000000 3pt: one arrow entering from upper-left in #0072B2 at 1.5pt (incident k_i), one arrow exiting to lower-right in #009E73 at 1.5pt (scattered k_f); draw a curved arc in #E69F00 at 1pt from tip of k_i to tip of k_f indicating momentum transfer q; draw a small angle arc in #000000 at 0.5pt between the two arrows near the center indicating scattering angle θ; fill the central circle with #56B4E9 at 30% opacity representing the potential region. Right panel (55% width): draw a horizontal axis from 0 to π in #000000 at 0.5pt and vertical axis from y = 0 upward; draw a smooth monotonically decreasing curve in #0072B2 at 1.5pt starting high at 0 and falling toward zero at π, with a gentle inflection representing a typical Yukawa-type cross-section. No text; unannotated.

**Block 2 — Full SCOPE Prompt:**
[S] Single-column 89mm wide two-panel vector figure, white background.
[C] Left panel: scattering geometry — incident wave vector, scattered wave vector, potential region as shaded circle, momentum transfer arc q between vector tips, scattering angle arc θ. Right panel: differential cross-section curve dσ/dΩ vs. scattering angle from 0 to π, y-axis from zero, smooth decreasing curve typical of a finite-range screened potential (forward-peaked, falls off at large angles).
[O] Left panel vectors radiate from center; arc connects tips of k_i and k_f; angle arc at central point. Right panel curve starts high at θ = 0 and falls monotonically; y-axis from zero; no divergence at small angles shown.
[P] Flat vector, Okabe-Ito hexes: incident k_i arrow #0072B2; scattered k_f arrow #009E73; momentum transfer arc #E69F00; angle arc #000000; potential circle #56B4E9 30% fill; cross-section curve #0072B2; axes #000000; unannotated.
[E] No 3D spherical polar plot; no Yukawa potential real-space profile; no Rutherford 1/sin⁴ divergence spike; no nuclear diffraction dip labeling; no multiple potential comparison curves; no convolution diagram; no axis tick numbers.

**Block 3 — Negative Prompt:**
No spherical 3D polar plot, no Yukawa real-space curve, no 1/sin⁴ divergence, no nuclear diffraction labels, no multiple cross-section curves stacked, no convolution arrows; text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, non-standard arrows, dual-headed arrows, hand-drawn styles, visual clutter, watermarks, red-green color combinations, 3D perspective distortion.

---

## Video Candidate Pass

**VIDEO CANDIDATE — Figure 1 (Fourier series → Fourier transform limit):** The learning target IS the limiting transition mechanism — the comb densifying continuously as L → ∞. This is a 3-stage causal sequence (L grows → Δk shrinks → sum becomes integral) and the limiting process is below direct observation. An animation showing L growing continuously while the comb fills in and smoothly converges to the envelope curve would make the mathematical limit physically intuitive.

**VIDEO CANDIDATE — Figure 3 (wave packet spreading):** The spreading mechanism has 3+ sequential causal stages: narrow Δx at t = 0 → broad Δp → different speeds for different k → packet broadens as t increases. The time evolution is the concept, and the cyclic contrast between narrow (t = 0) and broad (large t) has a before-after structure that animation makes visceral.

**Count: 2 video candidates.**
**Recommendation:** Prioritize Figure 1 (comb → transform) as it carries the foundational conceptual move of the entire module. Figure 3 (spreading) is secondary but useful as a companion animation to the wave packet discussion in Vol. I Ch. 8.
