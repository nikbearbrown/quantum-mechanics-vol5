# CAJAL Figure Intelligence — 01-complex-numbers-and-the-complex-exponential

**Source:** /Users/bear/Documents/CoWork/bear-textbooks/books/quantum-mechanics-vol5/chapters/01-complex-numbers-and-the-complex-exponential.md
**Scan:** /scan silent
**Date:** 2026-06-06

---

## Zones Detected

| Concept | Zone | Rationale |
|---|---|---|
| Polar form, modulus, argument | VG | Complex-plane geometry (unit circle, radial vector, angle θ, conjugate reflection) asserted in prose only |
| Euler's formula derivation | MC | 3-step mechanism: series substitution → power-of-i cycle → real/imaginary separation |
| Complex exponential with decay | VG | Spiral inward trajectory in the complex plane claimed but never shown; envelope/oscillation coupling is structural |
| Phasor addition (worked example) | VG + PQ | Geometric claim (vector addition = amplitude/phase) with specific values 3, 4, 5, 53.1° |
| Stationary-state phasor rotation | MC | 3-stage causal chain: phasor rotates at E/ħ → modulus fixed at 1 → probability density time-independent |
| Global vs. relative phase | VG | Structural distinction — overall phase unobservable, relative phase produces interference — geometric claim, no figure |

**Density recommendation: 4 figures, Mixed density.**

---

## Figure 1 — CRITICAL

**Concept:** The complex plane gives z = a + bi both a Cartesian representation (components a, b) and a polar representation (modulus r, argument θ), with the complex conjugate z* as a reflection across the real axis.

**Block 1 — Illustrae Paste Block:**
Draw on a single-column 89mm wide vector canvas with white background. Place horizontal (Re) and vertical (Im) axes in #000000 at 0.5pt, extending −1.5 to +1.5 on both axes. Draw a full circle of radius 1.0 centered at origin in #0072B2 at 1pt stroke. Place a filled 3pt dot at coordinates (0.6, 0.8) in #009E73. Draw a solid line from origin to (0.6, 0.8) in #009E73 at 1pt. Draw a small arc from the positive real axis to that line, radius 0.25 units, in #E69F00 at 1pt. Draw a dashed vertical line from (0.6, 0.8) to (0.6, 0) in #000000 at 0.5pt. Draw a dashed horizontal line from (0.6, 0) to origin in #000000 at 0.5pt. Place a filled 3pt dot at (0.6, −0.8) in #D55E00. Draw a dashed vertical line from (0.6, 0.8) to (0.6, −0.8) in #CC79A7 at 0.5pt. No text; unannotated.

**Block 2 — Full SCOPE Prompt:**
[S] Single-column 89mm wide vector figure, white background, Okabe-Ito palette only, 1pt strokes main elements, 0.5pt dashed projections, 3pt filled dots.
[C] Complex plane: real axis horizontal, imaginary axis vertical; point z at approximately (0.6, 0.8) in first quadrant; radial line r from origin to z; angle arc θ from positive real axis to radial line; unit circle; horizontal and vertical dashed projections forming a right triangle with components a and b; complex conjugate z* at (0.6, −0.8) in fourth quadrant; vertical dashed line connecting z to z* showing mirror reflection across real axis.
[O] Origin centered; z in first quadrant; z* in fourth quadrant directly below; angle arc small and near origin; projection right-triangle visible; unit circle radius visually distinct from radial line to z.
[P] Flat vector, Okabe-Ito hexes: unit circle #0072B2; z dot and radial line #009E73; θ arc #E69F00; projections #000000 dashed; z* dot #D55E00; conjugate connection #CC79A7 dashed; axes #000000; unannotated.
[E] No labels, tick marks, or numbers on axes; no arrows on radial line; no labels r, θ, a, b, z, z*; no multiplication illustration; no Euler's formula derivation; no spiral or decay; no phase factors from QM; no second example point beyond z and z*.

**Block 3 — Negative Prompt:**
No axis tick labels, no coordinate numbers, no vector labels, no arrows on modulus line, no complex multiplication diagram; text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, non-standard arrows, dual-headed arrows, hand-drawn styles, visual clutter, watermarks, red-green color combinations, 3D perspective distortion.

---

## Figure 2 — CRITICAL

**Concept:** Phasor addition reduces the superposition of two oscillations of the same frequency to a single vector addition in the complex plane, yielding the resultant amplitude and phase from one right-triangle geometry.

**Block 1 — Illustrae Paste Block:**
Draw on a single-column 89mm wide vector canvas with white background. Place horizontal and vertical axes in #000000 at 0.5pt, ranging −0.5 to +5 on horizontal and −0.5 to +5 on vertical. Draw a horizontal arrow from origin to (3, 0) in #56B4E9 at 1.5pt with filled arrowhead. Draw a vertical arrow from (3, 0) to (3, 4) in #E69F00 at 1.5pt with filled arrowhead. Draw a diagonal arrow from origin to (3, 4) in #0072B2 at 2pt with filled arrowhead. Draw dashed rectangle construction lines from (3, 0) horizontally and from (0, 4) vertically, meeting at (3, 4), in #000000 at 0.5pt dashed. Draw a small right-angle marker at (3, 0) in #000000 at 0.5pt. Draw a small arc at origin from the positive horizontal axis to the diagonal arrow in #009E73 at 1pt. No text; unannotated.

**Block 2 — Full SCOPE Prompt:**
[S] Single-column 89mm wide vector figure, white background.
[C] Complex plane vector addition from the worked example: first phasor of magnitude 3 along positive real axis; second phasor of magnitude 4 along positive imaginary axis placed tip-to-tail at head of first; resultant from origin to final head at (3, 4) of magnitude 5; right-angle marker at junction (3, 0); small arc at origin indicating resultant angle; dashed construction lines forming the rectangle.
[O] Origin at lower-left region; all three arrows in first quadrant; resultant diagonal clearly longer than either component; arc visually distinct from arrowheads.
[P] Flat vector, Okabe-Ito hexes: A₁ arrow #56B4E9; A₂ arrow #E69F00; resultant #0072B2 at 2pt (visually dominant); construction dashes #000000 0.5pt; angle arc #009E73; unannotated.
[E] No magnitude or angle number labels; no unit circle; no decay envelope; no sinusoidal curves; no time axis; no complex conjugate point; no second worked example; no quantum wave function annotation.

**Block 3 — Negative Prompt:**
No length labels "3", "4", "5", no angle label, no axis tick numbers, no phasor name labels; text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, non-standard arrows, dual-headed arrows, hand-drawn styles, visual clutter, watermarks, red-green color combinations, 3D perspective distortion.

---

## Figure 3 — IMPORTANT

**Concept:** A complex exponent with negative real part produces an inward spiral in the complex plane, encoding simultaneous exponential decay (shrinking radius) and oscillation (angle advancing with each revolution).

**Block 1 — Illustrae Paste Block:**
Draw on a full-width 120mm wide vector canvas with white background. Place horizontal (Re) and vertical (Im) axes in #000000 at 0.5pt, range −1.3 to +1.3 on both axes. Draw a dashed circle of radius 1.0 centered at origin in #E69F00 at 0.5pt. Draw an inward spiral starting at (1.0, 0) and winding counterclockwise for approximately 2.5 turns, each successive loop smaller than the previous, terminating near (0.15, 0.05), in #0072B2 at 1.5pt — representing the trajectory of e^(rt) with r = −γ + iω as t increases from 0. Place a filled 3pt dot at the starting point (1.0, 0) in #009E73. Place a filled 3pt dot at the terminal point near origin in #D55E00. No text; unannotated.

**Block 2 — Full SCOPE Prompt:**
[S] Full-width 120mm wide vector figure, white background.
[C] Complex plane trajectory of e^(rt) for r = −γ + iω (γ > 0): a spiral starting on positive real axis at radius 1.0, winding counterclockwise, shrinking in radius each revolution, converging toward origin. Dashed reference circle at initial radius 1.0. Start point (t = 0) and end point (large t) marked as distinct filled dots.
[O] Spiral centered at origin; clearly inward and converging; approximately 2–3 full visible turns; start on positive real axis; end dot near origin.
[P] Flat vector, Okabe-Ito hexes: spiral #0072B2 1.5pt; reference circle #E69F00 dashed 0.5pt; start dot #009E73; end dot #D55E00; axes #000000 0.5pt; unannotated.
[E] No time axis; no separate real-part or imaginary-part plots; no growing spiral; no labels for γ or ω values; no arrows along spiral path; no rectangular bounding box; no stationary-state phase rotation material.

**Block 3 — Negative Prompt:**
No arrows on spiral, no parameter labels, no turn-count annotations, no time labels; text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, non-standard arrows, dual-headed arrows, hand-drawn styles, visual clutter, watermarks, red-green color combinations, 3D perspective distortion.

---

## Figure 4 — IMPORTANT

**Concept:** A stationary-state phasor rotates at constant rate E/ħ on the unit circle while its modulus stays exactly 1, showing geometrically why the probability density |ψ|² is time-independent even though ψ itself evolves.

**Block 1 — Illustrae Paste Block:**
Draw on a single-column 89mm wide vector canvas with white background, divided into two equal panels side by side. Left panel: draw a unit circle in #0072B2 at 1pt with Re and Im axes in #000000 at 0.5pt. Draw three arrows from origin to the unit circle at angles approximately 15°, 75°, and 135°, all of identical length 1.0, in #009E73, #E69F00, and #D55E00 respectively, each at 1.5pt with small filled arrowheads. Draw a curved arc arrow along the circle from the first to the second arrow tip in #CC79A7 at 1pt indicating counterclockwise rotation direction. Right panel: draw a horizontal axis at y = 0 and a vertical axis from y = 0 to y = 1.5, both in #000000 at 0.5pt. Draw three horizontal bars of identical height 1.0 side by side, each filled solid in #009E73, #E69F00, and #D55E00 respectively, representing |ψ|² = constant for each phasor angle. No text; unannotated.

**Block 2 — Full SCOPE Prompt:**
[S] Single-column 89mm wide two-panel vector figure, white background.
[C] Left panel: unit circle in complex plane; three phasor snapshot arrows at three different angles, all reaching the unit circle (radius 1); arc indicating counterclockwise rotation direction. Right panel: three equal-height bars each of height 1.0 corresponding to the three phasor positions, showing |ψ|² invariant across all rotation angles. Right panel vertical axis starts at zero.
[O] Left and right panels same height; arrows in left panel equally spaced in angle; all three bars in right panel identical height; right-panel y-axis visibly starting at zero.
[P] Flat vector, Okabe-Ito hexes; each phasor matched by color to its bar: #009E73, #E69F00, #D55E00; unit circle #0072B2; rotation arc #CC79A7; axes #000000; unannotated.
[E] No time axis; no sinusoidal wave; no decay; no second eigenstate; no interference term; no labels E or ħ; no tick marks or numbers on axes; no rotating animation arrow (static only).

**Block 3 — Negative Prompt:**
No energy labels, no ħ symbols, no time values, no sinusoidal overlay, no axis tick numbers; text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, non-standard arrows, dual-headed arrows, hand-drawn styles, visual clutter, watermarks, red-green color combinations, 3D perspective distortion.

---

## Video Candidate Pass

**VIDEO CANDIDATE — Figure 4 (stationary-state phasor rotation):** The learning target IS the rotation mechanism itself — a phasor spinning continuously on the unit circle while the modulus-squared projection stays constant. This is a transformation below direct observation (quantum phase is not measurable), and the invariance of |ψ|² under rotation only becomes viscerally convincing in motion. A 3–5 second loop showing the phasor sweeping the unit circle with a live bar readout of |ψ|² would resolve the most common student misconception that stationary states do not evolve.

**VIDEO CANDIDATE — Figure 3 (decaying spiral):** The inward spiral is a 3-stage causal sequence as t increases: (1) angle advances (oscillation), (2) radius shrinks (decay), (3) the two combine in a single complex exponential. An animation tracing the spiral as t advances from 0 would show the geometric inseparability of damping and oscillation.

**Count: 2 video candidates.**
**Recommendation:** Prioritize Figure 4 — it carries the central QM payoff of this chapter (why stationary states have time-independent probability despite complex phase rotation). The Figure 3 animation is secondary and serves the classical motivation for complex exponents.
