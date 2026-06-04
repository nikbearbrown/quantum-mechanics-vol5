# CAJAL Figure Report — Module M-06 — The Fourier Transform

Recommended: 3 figures, Mixed density.

---

## Figure 1 — The Fourier series becomes the Fourier transform: discrete comb filling into a continuous spectrum

**Heuristic:** MC | **Rank:** Critical

---

**BLOCK 1 — ILLUSTRAE PASTE BLOCK**

Draw three horizontally aligned panels stacked vertically, sharing the same horizontal frequency axis. Top panel: a discrete comb of tall vertical spikes at evenly spaced positions, representing the Fourier series coefficients for a short period L — roughly eight spikes spread across the axis, all the same height for clarity. Middle panel: the same comb with twice as many spikes at half the spacing — the period has doubled, the density has increased. Bottom panel: a smooth continuous curve of the same general envelope shape — the Fourier transform — filling in where the spikes were, with the curve touching or nearly touching the spike tips visible as faint ghost marks. A downward progression arrow runs along the right side of all three panels. No text baked into the image.

**BLOCK 2 — FULL SCOPE**

- `[S — SPECIFICATION]` Single-column, 89 mm width, 300 DPI, vector (SVG/EPS), white background. Three stacked panels of equal height sharing a common horizontal k-axis; a progression indicator on the right margin.
- `[C — CONTENT]` Top panel: ~8 discrete spike marks at spacing Δk = 2π/L₁ (large spacing, small L); middle panel: ~16 spikes at Δk/2 (smaller spacing, larger L); bottom panel: smooth continuous spectral envelope curve, with the ghost comb marks at very low opacity to show the limiting relationship. Right-margin arrow indicating L increasing downward.
- `[O — ORGANIZATION]` All three panels share the same horizontal frequency axis range; vertical axes are all amplitude, starting at zero. Spikes are uniform 1 pt strokes with no fill. Continuous curve in bottom panel is a smooth bell-shaped envelope (not a specific named function). Ghost marks are the same comb as the middle panel, drawn at ~15% opacity.
- `[P — PRESENTATION]` Flat vector, Okabe-Ito: spike combs = Blue `#0072B2`; continuous transform curve = Orange `#E69F00`; ghost comb = Blue `#0072B2` at low opacity; progression arrow = Sky Blue `#56B4E9`. Uniform 1 pt strokes. White background. No baked text.
- `[E — EXCLUSIONS]` Omit the time-domain function panels (only show the spectral side), the QM momentum-space convention, Plancherel normalization factors, the Dirac delta, convolution, any specific named function (Gaussian, sinc).

**BLOCK 3 — NEGATIVE PROMPT**

time-domain function panel, wavefunction curves, Gaussian labeled shape, sinc function label, Dirac delta spike, convolution diagram, text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, dual-headed arrows, hand-drawn styles, human figures, visual clutter, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 2 — Gaussian wave packet: position and momentum widths trade off reciprocally

**Heuristic:** PQ | **Rank:** Critical

---

**BLOCK 1 — ILLUSTRAE PASTE BLOCK**

Draw a two-column comparison diagram, each column containing two vertically stacked panels. Left column, top panel: a narrow tall Gaussian curve in position space (small Δx). Left column, bottom panel: a wide low Gaussian curve in momentum space (large Δp). Right column, top panel: a wide low Gaussian curve in position space (large Δx). Right column, bottom panel: a narrow tall Gaussian curve in momentum space (small Δp). All four panels share the same axis conventions: horizontal axis is the conjugate variable (x top, p bottom), vertical axis is probability density starting at zero. Width markers — horizontal two-tick brackets spanning the half-maximum width — appear on each curve. The four widths satisfy: narrow position pairs with wide momentum and vice versa. No text baked into the image.

**BLOCK 2 — FULL SCOPE**

- `[S — SPECIFICATION]` Single-column, 89 mm width, 300 DPI, vector (SVG/EPS), white background. Two-by-two grid of panels: left column = narrow-x / wide-p case; right column = wide-x / narrow-p case; top row = position space; bottom row = momentum space.
- `[C — CONTENT]` Four Gaussian curves: (top-left) narrow position-space Gaussian; (bottom-left) wide momentum-space Gaussian; (top-right) wide position-space Gaussian; (bottom-right) narrow momentum-space Gaussian. Width brackets on all four curves indicating Δx or Δp (no numerical values, only geometric width indicators). All y-axes start at zero. Curves in each column are paired by color to show they belong to the same state.
- `[O — ORGANIZATION]` Grid layout with shared axis conventions within each row. Top row: x-axis = position; bottom row: x-axis = momentum. Vertical axis = probability density from zero. Pairs within a column share one color; the two columns use two distinct colors. Width brackets sit at half-maximum height of each curve.
- `[P — PRESENTATION]` Flat vector, Okabe-Ito: left-column state (narrow x) = Sky Blue `#56B4E9`; right-column state (wide x) = Orange `#E69F00`; width bracket tick marks = dark gray; axis lines = dark gray. Uniform 1 pt strokes; curve lines 1.5 pt. y-axis from zero. White background. No baked text.
- `[E — EXCLUSIONS]` Omit time-evolved spreading (fixed t=0 only), wave packet oscillations, complex phase factors, the momentum-operator derivation, Robertson commutator route, energy-time uncertainty, three-panel time sequence.

**BLOCK 3 — NEGATIVE PROMPT**

time-evolution spreading sequence, complex wavefunction real/imaginary panels, Robertson commutator diagram, energy-time diagram, operator algebra boxes, three-panel time sequence, text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, dual-headed arrows, hand-drawn styles, human figures, visual clutter, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 3 — Born scattering amplitude as the Fourier transform of the potential at momentum transfer q

**Heuristic:** VG | **Rank:** Important

---

**BLOCK 1 — ILLUSTRAE PASTE BLOCK**

Draw a two-panel figure. Left panel: a scattering geometry diagram — two arrows representing the incident and scattered wave vectors entering and leaving a central region, with a curved arc between their tips indicating the momentum transfer vector q = k_i − k_f, and the scattering angle θ marked between the two arrows. Inside the central region, represent the potential as a shaded circle. Right panel: a polar or Cartesian plot of the differential cross-section as a function of scattering angle — a smooth curve starting high at small angles (forward scattering) and falling off toward larger angles, with a single broad dip (for a smooth finite-range potential). The y-axis starts at zero. No text baked into the image.

**BLOCK 2 — FULL SCOPE**

- `[S — SPECIFICATION]` Single-column, 89 mm width, 300 DPI, vector (SVG/EPS), white background. Two side-by-side panels; left ~45% of width (geometry diagram), right ~55% (cross-section curve).
- `[C — CONTENT]` Left panel: incident wave vector arrow, scattered wave vector arrow, scattering center (shaded circle representing finite-range potential), curved arc connecting vector tips to indicate momentum transfer q, angle mark θ between vectors. Right panel: differential cross-section curve vs. scattering angle (0 to π), y-axis from zero; smooth monotonically decreasing curve with one suppressed dip — consistent with a smooth finite-range potential's Fourier transform. The connection between the two panels is indicated by a light gray arrow from the scattering geometry to the curve (inferred: cross-section is determined by the Fourier transform of the potential evaluated at q — label this as inferred with a dashed arrow).
- `[O — ORGANIZATION]` Left panel: vector arrows radiate from center; arc bridges the tip of k_i to tip of k_f; angle mark at the scattering center. Right panel: horizontal axis = scattering angle (0 to π); vertical axis = cross-section from zero; curve from high forward peak to low back-angle values. Dashed inferred arrow connects the two panels.
- `[P — PRESENTATION]` Flat vector, Okabe-Ito: incident vector = Blue `#0072B2`; scattered vector = Bluish Green `#009E73`; momentum transfer arc = Orange `#E69F00`; potential circle = Sky Blue `#56B4E9` fill at 30% opacity; cross-section curve = Blue `#0072B2`; inferred connection arrow = light gray dashed. Uniform 1 pt strokes; vector arrows 1.5 pt. White background. No baked text.
- `[E — EXCLUSIONS]` Omit the 3D angular spherical plot, Yukawa potential profile in real space, multiple-potential comparison curves, Rutherford singularity (1/sin⁴ divergence at θ=0), convolution theorem derivation diagram, nuclear diffraction dip labeling.

**BLOCK 3 — NEGATIVE PROMPT**

spherical polar plot in 3D, Yukawa potential real-space curve, Rutherford 1/sin4 divergence spike, nuclear diffraction labeled dips, multiple stacked cross-section curves, convolution diagram, text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, dual-headed arrows, hand-drawn styles, human figures, visual clutter, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Video Candidate Pass

**Figure 1 — Discrete comb filling into continuous transform**
VIDEO CANDIDATE. Criterion: transition mechanism is the learning target. The central conceptual move of the module — the Fourier series continuously becoming the Fourier transform as L → ∞ — is a limiting process whose dynamism a three-panel static figure can only gesture at. An animation showing the comb progressively densifying until it smoothly merges into the continuous curve would make the limit concrete and memorable. Recommend this as the one video for the module.

**Figure 2 — Gaussian position-momentum trade-off**
STATIC SUFFICIENT. The reciprocal-width relationship is a simultaneous structural comparison between two fixed states; the two-by-two static grid makes the trade-off legible without requiring animation.

**Figure 3 — Born scattering geometry and cross-section**
STATIC SUFFICIENT. The relationship between scattering geometry (q as a function of θ) and the cross-section curve is a spatial correspondence readable from a side-by-side static figure; no sequential causal staging is needed.
