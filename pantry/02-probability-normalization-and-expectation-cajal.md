# CAJAL Figure Intelligence — 02-probability-normalization-and-expectation

**Source:** /Users/bear/Documents/CoWork/bear-textbooks/books/quantum-mechanics-vol5/chapters/02-probability-normalization-and-expectation.md
**Scan:** /scan silent
**Date:** 2026-06-06

---

## Zones Detected

| Concept | Zone | Rationale |
|---|---|---|
| Probability density vs. probability | VG | "Density can exceed 1; probability lives in the integral" asserted without visual grounding showing area-under-curve as probability vs. function value |
| Mean, variance, standard deviation | VG + PQ | Mean as centroid, σ as spread — geometric/structural claim about PDF shape with specific numeric example (σ, μ) |
| Gaussian integral derivation | MC | 3-step mechanism: square the integral → switch to polar → evaluate r-integral; no figure needed (algebraic, not geometric) |
| Gaussian wave packet (worked example) | PQ | Specific values N, σ, ⟨x⟩ = 0, ⟨x²⟩ = σ² — quantitative shape with y-axis meaningful |
| Density vs. probability strip | VG | The distinction f(x) ≥ 0 vs. area = probability shown in prose only — the narrow-strip construction is structural |
| Delta-function normalization | VG | Structural claim (Kronecker → Dirac, discrete → continuous) — no geometric grounding |

**Density recommendation: 3 figures, Foundational density.**

---

## Figure 1 — CRITICAL

**Concept:** A probability density function gives probability only as area under the curve over an interval, not as a function value at a point; the Gaussian PDF with mean and standard deviation marked shows where probability mass concentrates.

**Block 1 — Illustrae Paste Block:**
Draw on a single-column 89mm wide vector canvas with white background. Place a horizontal x-axis in #000000 at 0.5pt extending from −3 to +3 units. Place a vertical axis in #000000 at 0.5pt starting at exactly y = 0 and extending to y = 0.45. Draw a smooth symmetric bell-shaped Gaussian curve peaking at x = 0 in #0072B2 at 1.5pt, starting near zero at the left edge and returning near zero at the right edge, never touching the axis. Draw a vertical dashed line from the peak down to the x-axis in #000000 at 0.5pt. Draw two short vertical tick marks on the x-axis at x = −1 and x = +1. Draw a small horizontal double-extent bracket below the axis spanning from x = −1 to x = +1 in #E69F00 at 1pt. Fill a vertical strip between x = 1.2 and x = 1.7 with area under the Gaussian curve, filled solid #009E73 at 50% opacity, representing P(a ≤ X ≤ b). No text; unannotated.

**Block 2 — Full SCOPE Prompt:**
[S] Single-column 89mm wide vector figure, white background.
[C] Gaussian probability density curve f(x) symmetric about mean μ = 0; vertical axis starting at zero; peak at μ = 0 marked by a dashed vertical line; standard deviation σ = 1 indicated by a bracket spanning −σ to +σ below the x-axis; a shaded strip under the curve between two points to the right of the mean, representing a finite-interval probability as an area; curve tails approaching but not touching the x-axis on both sides.
[O] Mean at center of x-axis; bell symmetric; σ bracket visually spans the middle third of the curve; shaded strip clearly to the right of center; y-axis from exactly zero; peak of curve occupies upper third of canvas.
[P] Flat vector, Okabe-Ito hexes: curve #0072B2 1.5pt; mean dashed #000000 0.5pt; σ bracket #E69F00 1pt; shaded strip #009E73 partial opacity; axes #000000 0.5pt; unannotated.
[E] No multiple curves for different σ; no labels μ, σ, f(x), P on the figure; no discrete bar histogram; no cumulative distribution function; no separate ψ or |ψ|² notation; no axis tick numbers.

**Block 3 — Negative Prompt:**
No Greek letter labels, no axis tick numbers, no "P(a≤X≤b)" annotation, no histogram bars, no CDF curve, no dual-peak distribution; text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, non-standard arrows, dual-headed arrows, hand-drawn styles, visual clutter, watermarks, red-green color combinations, 3D perspective distortion.

---

## Figure 2 — CRITICAL

**Concept:** The mean is the probability-weighted centroid of the distribution, and the standard deviation measures the rms spread; for an asymmetric distribution the mean and the peak (mode) do not coincide.

**Block 1 — Illustrae Paste Block:**
Draw on a full-width 120mm wide vector canvas with white background in two side-by-side panels of equal width. Left panel: draw a horizontal axis from −2 to +3 in #000000 at 0.5pt and a vertical axis from y = 0 upward in #000000 at 0.5pt. Draw a smooth symmetric Gaussian curve peaking at x = 0.5 in #0072B2 at 1.5pt. Draw a vertical dashed line at x = 0.5 in #0072B2 at 0.5pt (peak = mean). Draw a horizontal bracket below the axis at y = −0.05 spanning approximately 1 unit either side of the peak in #E69F00 at 1pt (σ span). Right panel: draw the same axes setup but plot a right-skewed smooth curve (like a log-normal shape) in #D55E00 at 1.5pt that peaks at x = 0.5 but has mean visibly to the right near x = 1.2. Draw a vertical dashed line at x = 0.5 in #D55E00 at 0.5pt for the peak. Draw a vertical dashed line at x = 1.2 in #009E73 at 0.5pt for the mean. No text; unannotated.

**Block 2 — Full SCOPE Prompt:**
[S] Full-width 120mm wide two-panel vector figure, white background.
[C] Left panel: symmetric unimodal distribution where peak and mean coincide at the same x value; σ bracket below axis. Right panel: right-skewed unimodal distribution where peak (mode) is left of mean; two separate vertical dashed lines — one at the peak and one at the mean — visually separated, showing that peak ≠ mean for asymmetric distributions. Both panels have y-axes starting at zero.
[O] Both panels same height and width; left panel distributions symmetric; right panel peak visibly to left of mean line; mean and mode dashed lines clearly separated in right panel.
[P] Flat vector, Okabe-Ito hexes: symmetric curve #0072B2; σ bracket #E69F00; skewed curve #D55E00; mode dashed #D55E00; mean dashed #009E73; axes #000000; unannotated.
[E] No numerical axis labels; no labels "mean", "mode", "σ"; no multiple σ lines; no Gaussian formula; no ψ notation; no filled shaded strip; no bar chart.

**Block 3 — Negative Prompt:**
No text annotations, no numerical axis values, no "mean" or "mode" labels, no formula overlays; text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, non-standard arrows, dual-headed arrows, hand-drawn styles, visual clutter, watermarks, red-green color combinations, 3D perspective distortion.

---

## Figure 3 — IMPORTANT

**Concept:** The Gaussian wave packet |ψ(x)|² is a bell curve centered at zero with width σ; the corresponding momentum-space probability |φ̃(p)|² is also Gaussian with width inversely proportional to σ, illustrating the Fourier-pair trade-off.

**Block 1 — Illustrae Paste Block:**
Draw on a full-width 120mm wide vector canvas with white background in two side-by-side panels. Left panel: draw horizontal x-axis from −3 to +3 in #000000 at 0.5pt and vertical axis from y = 0 upward in #000000 at 0.5pt. Draw a narrow tall Gaussian curve in #0072B2 at 1.5pt centered at x = 0, width σ = 0.7 units — representing a spatially localized wave packet. Right panel: draw horizontal p-axis from −3 to +3 in #000000 at 0.5pt and vertical axis from y = 0 upward in #000000 at 0.5pt. Draw a broad short Gaussian curve in #009E73 at 1.5pt centered at p = 0, width approximately 1/σ ≈ 1.4 units — representing the corresponding momentum distribution. Both curves normalized to same area. No text; unannotated.

**Block 2 — Full SCOPE Prompt:**
[S] Full-width 120mm wide two-panel vector figure, white background.
[C] Left panel: narrow, tall Gaussian |ψ(x)|² in position space (small σ, peaked near zero). Right panel: broad, flat Gaussian |φ̃(p)|² in momentum space (width ∝ 1/σ, same area). Both curves centered at zero. Both panels y-axes starting at zero. The width contrast between panels is the primary visual message.
[O] Both panels same canvas height; narrow curve in left panel visually taller and thinner; broad curve in right panel visually shorter and wider; reciprocal width relationship clear by inspection.
[P] Flat vector, Okabe-Ito hexes: position Gaussian #0072B2; momentum Gaussian #009E73; axes #000000 0.5pt; unannotated.
[E] No labels x, p, σ, ψ, φ; no axis tick numbers; no complex plane spiral; no multiple σ comparison; no shaded strip; no phase factors; no time evolution.

**Block 3 — Negative Prompt:**
No axis labels, no Greek letter labels, no width annotations, no formula overlays, no complex-plane elements; text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, non-standard arrows, dual-headed arrows, hand-drawn styles, visual clutter, watermarks, red-green color combinations, 3D perspective distortion.

---

## Video Candidate Pass

No video candidates. All three figures encode static geometric or distributional relationships. Figure 3's reciprocal-width relationship is a comparison of two fixed shapes, not a causal temporal process. Normalization preservation (the continuity-equation argument) involves no visual mechanism that requires animation over static diagrams.

**Count: 0 video candidates.**
**Recommendation:** All concepts in this chapter are best served by high-quality static figures. If any animation is desired, wave-packet spreading in time (mentioned briefly at the chapter's end in connection with Module M-06) would be the candidate, but that concept belongs to the Fourier Transform chapter.
