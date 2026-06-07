# CAJAL Figure Intelligence — 03-ordinary-differential-equations

**Source:** /Users/bear/Documents/CoWork/bear-textbooks/books/quantum-mechanics-vol5/chapters/03-ordinary-differential-equations.md
**Scan:** /scan silent
**Date:** 2026-06-06

---

## Zones Detected

| Concept | Zone | Rationale |
|---|---|---|
| Characteristic-equation method | MC | 4-step mechanism: assume e^(rx) → substitute → get polynomial → solve for roots; three outcome cases |
| Oscillatory vs. evanescent solution families | VG | Two distinct curve shapes (sinusoidal vs. real-exponential) asserted by equation only; no visual contrast |
| Boundary conditions produce quantization | MC | 3-step causal chain: general solution exists at all E → BC imposes constraint → only discrete E_n survive |
| Infinite square well worked example | VG + PQ | Energy-level ladder E_n ∝ n² asserted with specific formula; quantized standing waves not visually grounded |
| Matching conditions at potential interface | VG | Continuity of ψ and ψ′ at a boundary — structural geometric claim about smooth joining |
| Three discriminant cases (Δ > 0, < 0, = 0) | MC | Three-branch decision: distinct real / complex conjugate / repeated root; algebraic, not geometric — no figure needed |

**Density recommendation: 3 figures, Mixed density.**

---

## Figure 1 — CRITICAL

**Concept:** The two solution families of the TISE — oscillatory sinusoidal (classically allowed, E > V) and evanescent real-exponential (classically forbidden, E < V) — have visually distinct shapes determined entirely by the sign of E − V.

**Block 1 — Illustrae Paste Block:**
Draw on a full-width 120mm wide vector canvas with white background in two side-by-side panels. Left panel: draw a horizontal x-axis in #000000 at 0.5pt from 0 to +4 units and a vertical y-axis from −1.2 to +1.2 in #000000 at 0.5pt with a faint line at y = 0 in #000000 at 0.3pt. Draw a smooth sinusoidal curve completing approximately 1.5 full cycles, starting at y = 0, in #0072B2 at 1.5pt, representing A·cos(kx) + B·sin(kx). Right panel: draw the same axis setup with vertical range 0 to +1.2. Draw a smooth decaying curve starting at y = 1.0 at x = 0 falling toward zero in #D55E00 at 1.5pt, representing the normalizable B·e^(−κx). Draw separately a smooth growing curve starting near zero at x = 0 rising to y = 1.2 in #E69F00 at 1pt dashed, representing the non-normalizable A·e^(+κx). No text; unannotated.

**Block 2 — Full SCOPE Prompt:**
[S] Full-width 120mm wide two-panel vector figure, white background.
[C] Left panel: oscillatory solution — a sinusoidal curve with approximately 1.5 cycles, crossing zero multiple times, constant amplitude, representing A·cos(kx) + B·sin(kx) in a classically allowed region. Right panel: two evanescent solutions — decaying exponential (normalizable, solid) and growing exponential (non-normalizable, dashed). Both panels y-axes passing through or starting at zero.
[O] Left panel: sinusoid symmetric about zero, 1–2 full cycles. Right panel: decaying solid starts high at x = 0, falls to near zero; growing dashed starts low at x = 0, rises; they clearly diverge.
[P] Flat vector, Okabe-Ito hexes: oscillatory curve #0072B2 1.5pt; decaying exponential #D55E00 1.5pt; growing exponential #E69F00 1pt dashed; axes #000000 0.5pt; zero-line #000000 0.3pt; unannotated.
[E] No quantitative scale values on axes; no potential function V(x); no boundary condition markers; no energy labels; no three-region structure; no QHO or hydrogen atom solutions; no annotation distinguishing which exponential is accepted or rejected.

**Block 3 — Negative Prompt:**
No axis label values, no k or κ parameter labels, no "allowed/forbidden" text, no potential curve overlay, no boundary markers; text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, non-standard arrows, dual-headed arrows, hand-drawn styles, visual clutter, watermarks, red-green color combinations, 3D perspective distortion.

---

## Figure 2 — CRITICAL

**Concept:** Quantization in the infinite square well arises from the boundary conditions: sinusoidal solutions at any energy E exist, but only discrete k_n = nπ/L fit an integer number of half-wavelengths into the box, making ψ = 0 at both walls.

**Block 1 — Illustrae Paste Block:**
Draw on a full-width 120mm wide vector canvas with white background. Draw a horizontal x-axis from 0 to L in #000000 at 0.5pt. Draw thick vertical lines at x = 0 and x = L in #000000 at 2pt representing infinite walls. Inside the well, draw three standing-wave curves vertically offset at their respective energy baselines: n = 1 at height 1.0 unit, a single half-sine arch in #0072B2 at 1.5pt, touching zero at both walls; n = 2 at height 4.0 units, two half-sines (one arch up, one down) in #009E73 at 1.5pt, touching zero at both walls and midpoint; n = 3 at height 9.0 units, three half-sines in #E69F00 at 1.5pt, touching zero at both walls and two interior nodes. Draw faint horizontal dashed baselines in #000000 at 0.3pt for n = 1, 4, 9 units to show the n² energy spacing. Draw one dashed curve in #D55E00 at 0.5pt that starts at zero at x = 0 but does not reach zero at x = L, showing a non-quantized rejected solution. No text; unannotated.

**Block 2 — Full SCOPE Prompt:**
[S] Full-width 120mm wide vector figure, white background.
[C] Infinite square well: two vertical walls at x = 0 and x = L; three accepted standing-wave eigenfunctions n = 1, 2, 3 each touching zero at both walls, placed on baselines at heights proportional to n² (1, 4, 9 relative units); increasing node count with n visible; one dashed rejected curve that fails the right-wall boundary condition; y-axis starting at zero; energy gap between n = 2 and n = 3 visibly larger than gap between n = 1 and n = 2.
[O] Walls at left and right; all waveforms span the full width; node count increases with n; rejected curve clearly does not touch zero at right wall; n² spacing gives unequal vertical gaps.
[P] Flat vector, Okabe-Ito hexes: n = 1 #0072B2; n = 2 #009E73; n = 3 #E69F00; rejected #D55E00 dashed; baselines #000000 dashed 0.3pt; walls #000000 2pt; x-axis #000000 0.5pt; unannotated.
[E] No energy-level axis tick numbers; no |ψ|² probability density curves; no finite well; no harmonic oscillator potential; no time-dependent phase factors; no energy levels beyond n = 3; no normalization constant.

**Block 3 — Negative Prompt:**
No energy value labels E_n, no quantum number labels n, no axis tick numbers, no |ψ|² curves, no potential well depth label, no harmonic oscillator parabola; text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, non-standard arrows, dual-headed arrows, hand-drawn styles, visual clutter, watermarks, red-green color combinations, 3D perspective distortion.

---

## Figure 3 — IMPORTANT

**Concept:** At a finite potential step, both ψ and ψ′ must be continuous at the interface, producing a smooth join from oscillatory (interior) to decaying exponential (exterior) with matching value and slope.

**Block 1 — Illustrae Paste Block:**
Draw on a single-column 89mm wide vector canvas with white background. Draw a horizontal x-axis in #000000 at 0.5pt. Draw the step potential as a low horizontal line at y = −0.6 for x < 0 (V = 0 reference) and a higher horizontal line at y = 0 for x > 0 (V = V₀) in #000000 at 1pt, with a vertical riser at x = 0. Draw a dashed horizontal energy line at y = −0.3 in #0072B2 at 0.5pt, representing the bound-state energy E between the two potential levels. Draw a smooth sinusoidal oscillatory curve for x < 0 in #0072B2 at 1.5pt, arriving at x = 0 at some non-zero value and slope. Draw a smooth decaying exponential for x > 0 in #D55E00 at 1.5pt, starting at the same height and slope as the oscillatory curve at x = 0, then falling toward zero. Place a filled 3pt dot at (0, junction_height) in #009E73 marking the join. No text; unannotated.

**Block 2 — Full SCOPE Prompt:**
[S] Single-column 89mm wide vector figure, white background.
[C] Step potential V(x): low level for x < 0, higher level for x > 0, with vertical riser at x = 0. Dashed energy line between the two potential levels. Oscillatory ψ for x < 0. Decaying exponential ψ for x > 0. At x = 0, both the value and slope of the two curves match — smooth join with no kink, marked by a junction dot.
[O] Step at horizontal center; oscillatory curve arriving from left; decaying curve departing right; junction dot at the join; curves visually continuous in both height and slope at junction.
[P] Flat vector, Okabe-Ito hexes: potential step #000000 1pt; energy line #0072B2 dashed; oscillatory #0072B2 1.5pt; decaying #D55E00 1.5pt; junction dot #009E73; x-axis #000000 0.5pt; unannotated.
[E] No infinite wall; no three-region finite well; no multiple energy levels; no transmission/reflection amplitude arrows; no WKB curves; no quantization condition shown; no labels V₀ or E.

**Block 3 — Negative Prompt:**
No V₀ labels, no x = 0 annotation, no kink in the curves, no reflection/transmission arrows, no energy level labels, no three-region structure; text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, non-standard arrows, dual-headed arrows, hand-drawn styles, visual clutter, watermarks, red-green color combinations, 3D perspective distortion.

---

## Video Candidate Pass

**VIDEO CANDIDATE — Figure 2 (boundary condition quantization):** The learning target is the causal mechanism: as E is continuously swept upward from zero, the wave function at x = L oscillates away from zero until E reaches each E_n, where it snaps to exactly zero. This is a 3+ sequential causal stage process (E increases → kL changes → ψ(L) moves → occasional zero coincidence at E_n). An animation sweeping E and displaying ψ(L) as a real-time readout would make quantization visually self-evident and directly address the most persistent error (that the ODE, not the boundary conditions, restricts the energy).

**Count: 1 video candidate.**
**Recommendation:** Animate Figure 2 — sweep E continuously from 0 upward, showing ψ(L) oscillating as E changes, with the wave function inside the box updating in real time and snapping to a zero at each E_n. The static Figure 2 (three accepted solutions plus one rejected) remains required alongside as a reference diagram.
