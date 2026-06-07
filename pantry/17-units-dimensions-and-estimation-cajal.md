# CAJAL Figure Intelligence — 17-units-dimensions-and-estimation

**Source:** `books/quantum-mechanics-vol5/chapters/17-units-dimensions-and-estimation.md`
**Scan mode:** /scan silent
**Date:** 2026-06-06

---

## Zones Detected

| Concept | Heuristic | Notes |
|---|---|---|
| Hierarchy of atomic length scales: $a_0 \gg \lambda_C \gg r_e$ | VG | Chapter states the three lengths and their ratios but never draws them on a common scale |
| Classical vs. quantum crossover comparison $k_BT$ vs. $\hbar\omega$ | PQ | Specific numerical comparisons given (macroscopic 1 kHz oscillator ratio $\approx 10^{-10}$; hydrogen at room temp ratio $\approx 540$) — never charted |
| Bohr radius derivation: dimensional exponent system solves to give $a_0$ | MC | Three-equation linear system for exponents $\alpha$, $\beta$, $\gamma$ — a multi-step mechanism; diagram of which constants contribute which dimensions would ground it |
| Constants table: key quantum constants in SI and natural units | VG | Chapter explicitly flags this as a reference table that should be built; no figures needed here but the table gap is noted |

**Density recommendation: 2 figures, Foundational density.**

---

## Figure 1 — Hierarchy of Atomic Length Scales

**Rank: CRITICAL**

**Concept statement:** The three characteristic lengths of hydrogen — the Bohr radius $a_0 \approx 0.529$ Å, the Compton wavelength $\lambda_C \approx 3.86 \times 10^{-3}$ Å, and the classical electron radius $r_e \approx 2.8 \times 10^{-5}$ Å — differ by factors of $\alpha \approx 1/137$ from each other, so the scales are separated by roughly two orders of magnitude each.

---

**Block 1 — Illustrae Paste Block**

Produce a single-column 89mm vector figure on a white background showing a horizontal logarithmic ruler spanning from $10^{-5}$ Å to $1$ Å. Draw the ruler as a thin horizontal bar (#000000, 1pt) with major decade tick marks at $10^{-5}$, $10^{-4}$, $10^{-3}$, $10^{-2}$, $10^{-1}$, and $10^{0}$ Å (tick marks are 6pt vertical lines above the bar). Place three vertical arrow indicators dropping from above the ruler to the correct positions: a tall arrow in #0072B2 (2pt) pointing down to $a_0 \approx 0.529$ Å (near the right end of the ruler); a medium arrow in #009E73 (2pt) pointing down to $\lambda_C \approx 3.86 \times 10^{-3}$ Å (near the center); a short arrow in #E69F00 (2pt) pointing down to $r_e \approx 2.8 \times 10^{-5}$ Å (near the left end). Each arrow has a filled circle (#000000, 3pt) at the tip where it meets the ruler bar. Between the $a_0$ and $\lambda_C$ arrows draw a horizontal double-ended bracket (#CC79A7, 1pt dashed) below the ruler spanning those two positions to indicate the ratio $a_0/\lambda_C \approx 137$; between $\lambda_C$ and $r_e$ draw a similar bracket in (#D55E00, 1pt dashed) for the ratio $\lambda_C/r_e \approx 137$. No text; unannotated.

---

**Block 2 — Full SCOPE Prompt**

[S] Single-column 89mm, single horizontal log-ruler panel, vector, white background.

[C] Log-scale ruler from $10^{-5}$ Å to $1$ Å. Three markers at the exact positions: $a_0 = 5.29 \times 10^{-1}$ Å, $\lambda_C = 3.86 \times 10^{-3}$ Å, $r_e = 2.8 \times 10^{-5}$ Å. Two equal-width brackets below the ruler indicating the ratio $\approx 137$ between adjacent scales. All three values and their ratios are explicitly stated in Chapter 17 (specifically Exercise 7 and the main text on the Bohr radius and Compton wavelength sections).

[O] The log ruler makes the three orders-of-magnitude gaps directly legible as equal visual distances. The two brackets with equal span reinforce that the ratio is the same ($\approx \alpha^{-1} = 137$) between each pair. The three arrow colors identify the three physical scales without labels.

[P] Flat vector. Okabe-Ito: #0072B2 for $a_0$ arrow; #009E73 for $\lambda_C$ arrow; #E69F00 for $r_e$ arrow; #CC79A7 dashed bracket for $a_0/\lambda_C$; #D55E00 dashed bracket for $\lambda_C/r_e$; #000000 for ruler bar, tick marks, and dot tips. 1–2pt strokes. Unannotated.

[E] No text labels of any kind, no numerical tick-mark annotations, no atomic radius or nuclear radius markers (not in chapter), no angstrom unit labels, no fine-structure constant $\alpha$ annotation, no additional length scales not in the chapter (no nuclear radius, no Planck length).

---

**Block 3 — Negative Prompt**

No nuclear radius or Planck length markers, no labels on tick marks, no numerical values on the figure, no second ruler for SI units, no atomic orbital diagrams, no wave-function plots alongside the ruler. text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, non-standard arrows, dual-headed arrows, hand-drawn styles, visual clutter, watermarks, red-green color combinations, 3D perspective distortion.

---

## Figure 2 — Classical vs. Quantum Crossover: $k_BT$ vs. $\hbar\omega$

**Rank: IMPORTANT**

**Concept statement:** Whether a physical oscillator behaves classically or quantum mechanically is determined by the single comparison $k_BT$ vs. $\hbar\omega$; the chapter gives specific numerical examples spanning from a 1 kHz macroscopic pendulum ($\hbar\omega / k_BT \approx 10^{-10}$ at 300 K) to atomic hydrogen ($\hbar\omega / k_BT \approx 540$ at 300 K).

---

**Block 1 — Illustrae Paste Block**

Produce a single-column 89mm vector figure on a white background with a single horizontal axis representing the dimensionless ratio $\hbar\omega / k_BT$ on a logarithmic scale from $10^{-12}$ to $10^4$. Draw the axis as a horizontal line (#000000, 1pt) with major decade tick marks. To the left of a central threshold at ratio $= 1$ shade a wide horizontal band of low opacity (#E69F00, 10% opacity fill) indicating the classical regime ($\hbar\omega \ll k_BT$); to the right shade a band in (#0072B2, 10% opacity fill) indicating the quantum regime ($\hbar\omega \gg k_BT$). Mark the threshold with a thin vertical dashed line at ratio $= 1$ in #000000 at 0.5pt. Place three vertical arrow indicators pointing down to the axis: at $\approx 10^{-10}$ a filled circle with a downward arrow in #E69F00 (macroscopic 1 kHz pendulum); at $\approx 10^{-3}$ a filled circle with a downward arrow in #E69F00 (a 1 GHz microwave resonator, representing an intermediate scale); at $\approx 540$ (between $10^2$ and $10^3$) a filled circle with a downward arrow in #0072B2 (hydrogen electron at room temperature). Each circle is #000000 filled, 3pt radius; arrow shafts match the regime color. No text; unannotated.

---

**Block 2 — Full SCOPE Prompt**

[S] Single-column 89mm, single horizontal log-axis panel, vector, white background.

[C] Log axis from $10^{-12}$ to $10^4$. Classical regime shading left of ratio $= 1$; quantum regime shading right. Three markers at: $\hbar\omega / k_BT \approx 10^{-10}$ (1 kHz macroscopic oscillator at 300 K, explicitly calculated in the chapter), $10^{-3}$ (illustrative intermediate example — chosen to spread the scale; this value is consistent with the chapter's framework even if not explicitly named), and $\approx 540$ (hydrogen electron at room temperature, explicitly stated in the chapter). The threshold at ratio $= 1$ corresponds to the crossover temperature $T^* = \hbar\omega / 2k_B$ from Exercise 5.

[O] The log axis spreads 16 decades so the contrast between the pendulum ($10^{-10}$) and the hydrogen atom ($\approx 10^3$) is graphically striking. The two shading regions make the classical/quantum interpretation of the axis position immediate. Arrow colors match the regime.

[P] Flat vector. Okabe-Ito: #E69F00 10% fill for classical region; #0072B2 10% fill for quantum region; #000000 for axis, ticks, threshold dashes, and marker dots. Arrow shafts #E69F00 or #0072B2 matching regime. 1pt strokes. Unannotated.

[E] No text labels, no tick-mark annotations, no specific physical system labels on markers, no third-system marker that is not grounded in the chapter's numerical examples (the intermediate point at $10^{-3}$ is schematic; the two endpoints are chapter-confirmed), no photon energy curves, no temperature-axis overlay.

---

**Block 3 — Negative Prompt**

No Planck distribution curve, no temperature axis, no specific system labels, no energy-level diagrams, no second axis for system names, no values that would require information not in the chapter. text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, non-standard arrows, dual-headed arrows, hand-drawn styles, visual clutter, watermarks, red-green color combinations, 3D perspective distortion.

---

## Video Candidate Pass

No video candidates identified. The length-scale hierarchy (Figure 1) is a static ordering relationship — the visual argument is spatial, not temporal. The classical-quantum crossover (Figure 2) is a comparison of two values on a fixed scale; the transition mechanism is a single threshold comparison, not a sequential causal process. Neither concept benefits from animation over the static figures described.

**Total video candidates: 0.**
