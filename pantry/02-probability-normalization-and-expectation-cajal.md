# CAJAL Figure Report — Module M-02 — Probability, Normalization, and Expectation Values

Recommended: 2 figures, Foundational density.

---

## Figure 1 — Probability Density vs. Probability: The Gaussian PDF with Mean, Variance, and Integral Strip

**Heuristic:** PQ — Proportional/Quantitative
**Rank:** Critical

### BLOCK 1 — ILLUSTRAE PASTE BLOCK

Draw a smooth bell-shaped Gaussian probability density curve f(x) over a horizontal x-axis, with the vertical axis (probability density) starting at zero. The curve is symmetric about a central peak at x = μ. Mark the mean μ on the x-axis with a vertical dashed line descending from the peak to the x-axis. Mark two points at one standard deviation below and above the mean (μ − σ and μ + σ) on the x-axis, each with short tick marks. Shade a narrow vertical strip of finite width between two values a and b (both to the right of the mean), where the shaded area represents the probability P(a ≤ X ≤ b). The strip height follows the curve. Show the full curve tail extending to near-zero on both sides without touching the axis. The curve must not be clipped. Draw a small bracket or double-headed extent marker from μ − σ to μ + σ beneath the axis to indicate the standard deviation span σ.

### BLOCK 2 — FULL SCOPE

**[S — SPECIFICATION]** Single-column 89 mm width, 300 DPI, vector (SVG/EPS), white background.

**[C — CONTENT]** Gaussian PDF f(x) for a continuous random variable X. Elements: (1) the bell curve itself; (2) mean μ as the peak location and the axis of symmetry; (3) standard deviation σ as the distance from the mean to the inflection point, with a bracket spanning μ − σ to μ + σ; (4) a shaded strip between two x-values a and b (a < b, both > μ) whose area equals P(a ≤ X ≤ b) — illustrating that probability is an integral of the density, not a value of f(x); (5) the vertical axis starting at zero, with the peak value above 0.

**[O — ORGANIZATION]** Horizontal x-axis spanning roughly −3σ to +3σ from the mean. Vertical axis from 0 upward; the peak of the curve is the tallest element. Mean μ marked by a dashed vertical line from peak to axis. σ bracket below the x-axis, centered on μ. Shaded strip: narrow, located in the right wing of the distribution (not at the peak), filled with the shaded-area color; strip height follows the curve profile. The curve tails approach but do not touch the x-axis within the frame.

**[P — PRESENTATION]** Flat vector, Okabe-Ito palette. Gaussian curve outline: Blue `#0072B2`, solid, 1.5 pt. Mean dashed line: Blue `#0072B2`, dashed, 1 pt. σ bracket: Orange `#E69F00`, 1 pt. Shaded strip (probability area): Sky Blue `#56B4E9`, 40% opacity fill, bounded by solid 1 pt Sky Blue stroke. Curve fill below the entire Gaussian: none (no fill — strip only). White background; no baked text.

**[E — EXCLUSIONS]** Omit: cumulative distribution function (CDF); discrete probability bars; the Cauchy or Lorentz distribution; the power-of-i cycle; quantum wave function ψ or ψ*ψ overlay; the derivation via polar-coordinate squaring trick; multiple distributions for comparison.

### BLOCK 3 — NEGATIVE PROMPT

CDF curve, discrete histogram bars, Cauchy distribution, quantum wave function overlay, multiple overlaid distributions, text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, dual-headed arrows, hand-drawn styles, human figures, visual clutter, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 2 — Gaussian Wave Packet: Position Probability Density |ψ|² with Mean, Standard Deviation, and Width σ

**Heuristic:** PQ — Proportional/Quantitative
**Rank:** Important

### BLOCK 1 — ILLUSTRAE PASTE BLOCK

Draw a smooth Gaussian probability density curve |ψ(x)|² = N²e^(−x²/2σ²) over a horizontal x-axis, with the vertical axis starting at zero. The curve is centered at x = 0 (mean ⟨x⟩ = 0). Mark the peak at x = 0 with a short vertical tick on the x-axis. Mark the two points x = −σ and x = +σ on the x-axis with short ticks, and draw horizontal dashed lines from x = ±σ up to the curve to indicate the inflection points (where the Gaussian curvature changes sign). Draw a symmetric double-extent marker below the x-axis spanning from −σ to +σ to represent the standard deviation Δx = σ. The curve should taper smoothly to near-zero on both sides within the frame. Show the vertical axis with the peak value at the top and zero at the bottom. Do not shade any area.

### BLOCK 2 — FULL SCOPE

**[S — SPECIFICATION]** Single-column 89 mm width, 300 DPI, vector (SVG/EPS), white background.

**[C — CONTENT]** The position probability density |ψ(x)|² for a normalized Gaussian wave packet with width parameter σ. Elements: (1) the Gaussian bell curve centered at x = 0; (2) the mean ⟨x⟩ = 0 indicated at the peak; (3) x = ±σ inflection point markers on the curve, with dashed horizontal drop-lines to the x-axis; (4) a double-extent bracket below the axis from −σ to +σ representing the standard deviation Δx = σ; (5) vertical axis from zero upward. The figure specifically illustrates the result ⟨x⟩ = 0 and Δx = σ from the worked example.

**[O — ORGANIZATION]** x-axis centered at 0, spanning approximately −3σ to +3σ. Vertical axis starting at 0, peak at the top. Inflection points at x = ±σ: dashed horizontal lines from those curve points horizontally to the vertical axis (or to x-axis tick marks). The extent bracket is below the x-axis, centered on 0, spanning −σ to +σ. No shading. Curve tails near-zero at the frame edges.

**[P — PRESENTATION]** Flat vector, Okabe-Ito palette. |ψ|² curve: Bluish Green `#009E73`, solid, 1.5 pt. Peak marker tick: Blue `#0072B2`, 1 pt. Inflection point dashes (horizontal drop-lines from ±σ): Orange `#E69F00`, dashed, 0.75 pt. σ extent bracket below axis: Orange `#E69F00`, 1 pt. Axis lines: light gray, 0.75 pt. White background; no baked text; no fill under curve.

**[E — EXCLUSIONS]** Omit: the unnormalized version of ψ before normalization; the momentum-space distribution |φ(k)|²; the time-dependent rotating phasor e^(−iEt/ℏ); multiple curves for different σ values; the normalization integral derivation steps; any complex-plane representation; probability strip shading (that is Figure 1's job).

### BLOCK 3 — NEGATIVE PROMPT

momentum space distribution, time-dependent animation frames, multiple sigma curves, normalization step panels, complex plane overlay, shaded probability strip, text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, dual-headed arrows, hand-drawn styles, human figures, visual clutter, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Video Candidate Pass

**Figure 1 — Gaussian PDF with probability strip:** STATIC SUFFICIENT. The core concept (probability as area under the curve, not point value of f) is a static geometric argument. The strip and the curve are a fixed diagram; no causal sequence or transformation is the learning target.

**Figure 2 — Gaussian Wave Packet |ψ|² with Δx = σ:** STATIC SUFFICIENT. The figure establishes that the Gaussian width parameter is literally the standard deviation of the position distribution. This is a one-shot structural identification, not a process unfolding in steps. A static annotated curve communicates it fully.
