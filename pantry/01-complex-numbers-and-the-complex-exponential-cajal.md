# CAJAL Figure Report — Module M-01 — Complex Numbers and the Complex Exponential

Recommended: 3 figures, Mixed density.

---

## Figure 1 — The Complex Plane: Cartesian and Polar Representations of z

**Heuristic:** VG — Verification Gap
**Rank:** Critical

### BLOCK 1 — ILLUSTRAE PASTE BLOCK

Draw a single Cartesian coordinate plane with the horizontal axis labeled as the real axis and the vertical axis as the imaginary axis. Place a single point z in the first quadrant, connected to the origin by a line of length r (the modulus). Draw a horizontal dashed projection from the origin to directly below z, and a vertical dashed projection from that foot up to z, forming a right triangle with legs a (real part) and b (imaginary part) and hypotenuse r. Mark the angle θ between the positive real axis and the line from origin to z. On the unit circle (a circle of radius 1 centered at the origin), place a second point showing e^(iθ) — where the same angle θ intercepts the unit circle — and draw short tick marks to indicate unit radius. Connect both points to the origin with solid lines. Indicate the conjugate z* as a reflected point below the real axis with a short dashed vertical line of length b below the axis.

### BLOCK 2 — FULL SCOPE

**[S — SPECIFICATION]** Single-column 89 mm width, 300 DPI, vector (SVG/EPS), white background.

**[C — CONTENT]** Complex plane with: origin O; point z = a + bi at coordinates (a, b); modulus r = |z| as the length of the line from O to z; real component a as horizontal projection; imaginary component b as vertical projection; angle θ (argument) from positive real axis to the line Oz; unit circle (radius 1) with the point e^(iθ) on it at angle θ; conjugate z* = a − bi as the reflection of z across the real axis. The right triangle formed by a, b, r is explicit.

**[O — ORGANIZATION]** Standard orientation: real axis horizontal, imaginary axis vertical, both labeled. z in the first quadrant (a > 0, b > 0). z* in the fourth quadrant, directly below z. The unit circle occupies the central region; its intersection with the line at angle θ marks e^(iθ). Dashed projections form the right triangle. The angle arc θ sits near the origin between the real axis and the Oz line.

**[P — PRESENTATION]** Flat vector, Okabe-Ito palette with hex. Point z: Sky Blue `#56B4E9` filled circle. Modulus line r: Blue `#0072B2`, solid, 1 pt. Projection dashes for a and b: neutral light gray, 0.75 pt. Unit circle: Orange `#E69F00`, 1 pt, no fill. e^(iθ) point on unit circle: Bluish Green `#009E73` filled circle. z* point: Reddish Purple `#CC79A7` filled circle. Angle arc θ: Blue `#0072B2`, thin arc near origin. White background; no baked text.

**[E — EXCLUSIONS]** Omit: multiplication of two complex numbers (separate concept); Euler's formula derivation; the i^n power cycle; any reference to QM wave functions; de Moivre's theorem; multiple example points.

### BLOCK 3 — NEGATIVE PROMPT

multiple example points, multiplication arrows, power cycle diagram, wave function overlay, text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, dual-headed arrows, hand-drawn styles, human figures, visual clutter, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 2 — Phasor Addition as Vector Sum in the Complex Plane

**Heuristic:** VG — Verification Gap
**Rank:** Important

### BLOCK 1 — ILLUSTRAE PASTE BLOCK

Draw a Cartesian complex plane. Place two phasor arrows originating from the origin: the first along the positive real axis with length 3 (representing the complex amplitude Ã₁ = 3), and the second at 90° to the real axis (pointing straight up) with length 4 (representing Ã₂ = 4i). Show their vector sum Ã = 3 + 4i as a third arrow from the origin to the point (3, 4), with length 5. Use a dashed construction path: a horizontal segment of length 3 from the origin, then a vertical segment of length 4 upward, meeting at the tip of the resultant arrow — the standard parallelogram (here a rectangle) construction. Mark the angle φ ≈ 53° between the resultant arrow and the positive real axis with a small arc near the origin. Display the right triangle formed by the three lengths 3, 4, 5 explicitly inside the construction.

### BLOCK 2 — FULL SCOPE

**[S — SPECIFICATION]** Single-column 89 mm width, 300 DPI, vector (SVG/EPS), white background.

**[C — CONTENT]** Complex plane showing the worked phasor addition from the module: Ã₁ = 3 (real axis), Ã₂ = 4i (imaginary axis), resultant Ã = 3 + 4i with modulus 5. The 3–4–5 right triangle formed by the Cartesian components. Angle φ between resultant and real axis, illustrating φ = arctan(4/3). Construction dashes showing the tip-to-tail or parallelogram method.

**[O — ORGANIZATION]** Origin at lower-left of the plotting region (with small negative-axis stubs for context). Ã₁ arrow along the real axis (horizontal, pointing right). Ã₂ arrow along the imaginary axis (vertical, pointing up). Resultant Ã as a diagonal arrow to the upper-right. Dashed rectangle construction lines from tips of Ã₁ and Ã₂ meeting at the resultant tip. Angle arc φ near the origin between real axis and resultant. All three arrows originate at the origin.

**[P — PRESENTATION]** Flat vector, Okabe-Ito palette. Ã₁ arrow: Sky Blue `#56B4E9`, solid, 1 pt, filled arrowhead. Ã₂ arrow: Orange `#E69F00`, solid, 1 pt, filled arrowhead. Resultant Ã arrow: Blue `#0072B2`, solid, 1.5 pt, filled arrowhead (visually dominant). Construction dashes: light gray, 0.75 pt, dashed. Angle arc φ: Bluish Green `#009E73`, thin. White background; no baked text.

**[E — EXCLUSIONS]** Omit: sinusoidal waveforms showing the time-domain oscillations; the unit circle; the conjugate; any second example beyond the 3–4–5 case; reference to quantum wave functions or spin.

### BLOCK 3 — NEGATIVE PROMPT

sinusoidal waveforms, unit circle overlay, multiple example cases, quantum wave function annotation, text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, dual-headed arrows, hand-drawn styles, human figures, visual clutter, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 3 — Decaying Oscillation from a Complex Exponent: The e^(rt) Envelope

**Heuristic:** PQ — Proportional/Quantitative
**Rank:** Important

### BLOCK 1 — ILLUSTRAE PASTE BLOCK

Draw a single horizontal time axis with a vertical amplitude axis starting at zero. Plot a smooth oscillating curve that starts with a positive peak near t = 0 and decreases in amplitude over time — a damped sinusoid representing Re(e^(rt)) = e^(−γt) cos(ωt). Superimpose two smooth envelope curves: one decaying exponential bounding the peaks from above (e^(−γt)), and its mirror image below the axis (−e^(−γt)). The envelope curves touch the oscillating curve at its successive peaks and troughs. Use three visually distinct curves: the central oscillating curve and the two bounding envelopes. The vertical axis runs from a negative minimum to a positive maximum, with zero marked. The oscillating curve begins at amplitude 1 at t = 0 and decays toward zero as t increases. The envelope curves converge symmetrically to zero.

### BLOCK 2 — FULL SCOPE

**[S — SPECIFICATION]** Single-column 89 mm width, 300 DPI, vector (SVG/EPS), white background.

**[C — CONTENT]** Three curves illustrating e^(rt) with r = −γ + iω: (1) the real part Re(e^(rt)) = e^(−γt)cos(ωt) — the oscillating curve; (2) the upper decay envelope e^(−γt); (3) the lower decay envelope −e^(−γt). The vertical axis starts at a negative value (minimum envelope) and passes through zero; the horizontal axis is time t ≥ 0. The curves show that the decay envelope is set by the real part of r (γ), and the oscillation frequency is set by the imaginary part (ω).

**[O — ORGANIZATION]** Horizontal time axis from 0 rightward (approximately 1.5–2 full oscillation cycles visible before the amplitude becomes negligibly small). Vertical amplitude axis: symmetric about zero, running from roughly −1 to +1 (normalized so the initial amplitude is 1). Oscillating curve: begins at (0, 1), crosses zero multiple times, each successive peak visibly lower. Envelope curves: upper starts at (0, 1) and decays smoothly; lower starts at (0, −1) and rises smoothly to meet at zero. The envelope curves meet the oscillating curve exactly at its extrema (tangent at peaks and troughs). Y-axis starts at the negative minimum, passes through zero which is marked.

**[P — PRESENTATION]** Flat vector, Okabe-Ito palette. Oscillating curve: Blue `#0072B2`, solid, 1.5 pt. Upper decay envelope: Vermillion `#D55E00`, dashed, 1 pt. Lower decay envelope: Vermillion `#D55E00`, dashed, 1 pt. Zero axis line: light gray, 0.5 pt, solid. White background; no baked text. No filled regions or shading.

**[E — EXCLUSIONS]** Omit: complex-plane trajectory of e^(rt) as a spiral; comparison with purely imaginary exponent (no decay); the imaginary part Im(e^(rt)); any reference to quantum stationary states, spin, or wave packets; multiple curves for different γ values.

### BLOCK 3 — NEGATIVE PROMPT

complex plane spiral trajectory, multiple decay-rate curves, imaginary part curve, quantum state annotations, filled shaded regions, text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, dual-headed arrows, hand-drawn styles, human figures, visual clutter, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Video Candidate Pass

**Figure 1 — Complex Plane (Cartesian and Polar):** STATIC SUFFICIENT. The diagram is a static geometric relationship between two representations of the same point; no transformation or causal sequence is the learning target.

**Figure 2 — Phasor Addition:** STATIC SUFFICIENT. The construction is a single-step geometric argument (vector addition); the result is a fixed triangle. The static diagram captures the full content without a temporal sequence.

**Figure 3 — Decaying Oscillation Envelope:** VIDEO CANDIDATE. Criterion: transition mechanism is the learning target. The key concept is that a single complex exponent simultaneously encodes two phenomena — the oscillation frequency and the decay rate — that the student has previously encountered only as separate functions. An animation showing e^(rt) sweeping in the complex plane (a decaying spiral) while the Re and Im projections play out on horizontal time axes would make the two-in-one structure viscerally clear in a way a static curve cannot. **Recommend this as the one video for Module M-01.**
