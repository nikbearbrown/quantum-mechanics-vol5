# CAJAL Figure Report — Module M-18 — Trigonometry, Waves, and the Harmonic Model

Recommended: 3 figures, Mixed density.

---

## Figure 1 — The sinusoidal traveling wave: anatomy of one full cycle

**Heuristic:** VG — Verification Gap
**Rank:** Critical

**BLOCK 1 — ILLUSTRAE PASTE BLOCK:**
Draw a single sinusoidal wave plotted on a horizontal spatial axis (x-axis) showing exactly one full wavelength plus a half-wavelength on either side. Annotate the wave's anatomy with bracket-and-arrow callouts: a horizontal double-bracket spanning one full period to indicate wavelength λ; a vertical double-bracket from the axis to the crest to indicate amplitude A; a filled circle at a particular phase point to indicate the phase offset φ position; and a small horizontal arrow pointing in the direction of wave travel (+x direction). Above the wave plot, add a second thin horizontal axis with a dotted vertical projection line connecting a point on the wave cycle to a corresponding point on the unit circle, showing how the cosine function maps the unit-circle angle to the wave height. Separately, in a compact inset to the right, show the complex exponential form as a rotating phasor — a circle with a rotating arrow at angle (kx − ωt), with the real part projecting horizontally (cosine component) and imaginary part projecting vertically (sine component), making the Euler formula geometry visible. Do not annotate with any text in the image.

**BLOCK 2 — FULL SCOPE:**

`[S — SPECIFICATION]` Single-column 89 mm width, 300 DPI, SVG/EPS, white background. Two sub-panels stacked vertically: main wave plot (approx. 2/3 height) and a right-side phasor inset (approx. 1/3 width of the main panel, same height as main panel).

`[C — CONTENT]` Main panel: sinusoidal wave with amplitude A (crest-to-axis), wavelength λ (full cycle bracket), direction arrow (+x), and phase point marker. Unit-circle projection strip above the x-axis showing one unit circle linked to the wave by a dotted vertical. Phasor inset: a circle of unit radius, a rotating arm at a representative angle, horizontal projection (real/cosine), vertical projection (imaginary/sine), both projections marked with short tick marks.

`[O — ORGANIZATION]` Main panel axis: horizontal (x) with the wave displayed over approximately 2.5 wavelengths. Amplitude bracket on the left side, wavelength bracket below the axis. Direction arrow on the crest. Unit circle positioned above the wave at one specific x point, with a dotted projection line. Phasor inset: compact circle diagram in the upper right corner of the figure, separated by a thin border.

`[P — PRESENTATION]` Flat vector, Okabe-Ito palette, 1 pt strokes, white background, no baked text. Wave curve: Blue `#0072B2`, 2 pt stroke. Amplitude bracket: Bluish Green `#009E73`. Wavelength bracket: Orange `#E69F00`. Phase marker dot: Reddish Purple `#CC79A7`. Direction arrow: Sky Blue `#56B4E9`. Unit circle and projection lines: neutral gray. Phasor arm: Blue `#0072B2`. Real projection: Bluish Green `#009E73`. Imaginary projection: Vermillion `#D55E00`. Axes: black, 1 pt.

`[E — EXCLUSIONS]` Omit: time-axis plot, probability density, group velocity envelope, two-wave superposition. Do not depict standing waves. Do not show wave packets or dispersion. Do not include any text labels, unit symbols, or numerical values baked into the image.

**BLOCK 3 — NEGATIVE PROMPT:**
Standing wave, wave packet envelope, two-wave superposition, time-axis, probability density curve, dispersion curve, text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, dual-headed arrows, hand-drawn styles, human figures, visual clutter, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion.

---

## Figure 2 — Superposition and interference: constructive, destructive, and partial

**Heuristic:** PQ — Proportional/Quantitative
**Rank:** Critical

**BLOCK 1 — ILLUSTRAE PASTE BLOCK:**
Draw three stacked horizontal panels, each showing the sum of two equal-amplitude sinusoidal waves and their resultant. Panel 1 (top): the two waves are in phase (δ = 0); both are shown as thin curves, their sum as a thick curve with amplitude 2A — constructive interference. Panel 2 (middle): the two waves are anti-phase (δ = π); their sum is the flat zero line — destructive interference. Panel 3 (bottom): the two waves have an intermediate phase offset (δ = π/2); the sum has an intermediate amplitude between 0 and 2A and a shifted peak. All three panels share the same x-axis scale and the same amplitude scale, with the y-axis running from −2A to +2A. Mark the resultant amplitude visually with a vertical double-bracket on the right edge of each panel. The phases of the two component waves should differ visibly from panel to panel — shift the second wave rightward progressively. Use consistent color coding: first component wave, second component wave, and resultant in distinct colors across all three panels.

**BLOCK 2 — FULL SCOPE:**

`[S — SPECIFICATION]` Single-column 89 mm width, 300 DPI, SVG/EPS, white background. Three stacked panels of equal height, sharing a common y-axis amplitude range (−2A to +2A), separated by thin horizontal rules.

`[C — CONTENT]` Three panels (δ = 0, π, π/2). Each panel: two thin sinusoidal component curves and one thick resultant curve. Right-edge amplitude bracket indicating |resultant amplitude| for each panel. The component waves ψ₁ and ψ₂ are identical in frequency and amplitude, differing only in phase offset δ. Y-axis starts at −2A (not truncated). No numerical axis labels baked in.

`[O — ORGANIZATION]` Y-axis: shared vertical axis on the left side, running from −2A to +2A across all three panels. Horizontal dividing rules between panels. The second component wave (ψ₂) is progressively right-shifted across the three panels (no shift, half-wavelength shift, quarter-wavelength shift). Amplitude bracket on the right edge of each panel; brackets increase in height from Panel 2 (zero height, flat line) through Panel 3 (intermediate) to Panel 1 (full 2A).

`[P — PRESENTATION]` Flat vector, Okabe-Ito palette, 1 pt strokes for components, 2 pt stroke for resultant, white background, no baked text. Component wave ψ₁: Sky Blue `#56B4E9`, 1 pt. Component wave ψ₂: Orange `#E69F00`, 1 pt. Resultant: Blue `#0072B2`, 2 pt. Amplitude bracket: Bluish Green `#009E73`. Zero-result flat line (Panel 2): Vermillion `#D55E00`, 2 pt. Y-axis: black, 1 pt. Panel dividers: light gray rule.

`[E — EXCLUSIONS]` Omit: beats / group velocity envelope (different frequencies), probability density interpretation, de Broglie wave labeling, double-slit geometry. Do not include any text labels, δ values, or amplitude values baked into the image. Do not depict more than two component waves per panel.

**BLOCK 3 — NEGATIVE PROMPT:**
Beat envelope with different-frequency waves, double-slit geometry diagram, probability density curve, de Broglie wavelength annotation, more than two component waves per panel, text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, dual-headed arrows, hand-drawn styles, human figures, visual clutter, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion.

---

## Figure 3 — Group velocity vs. phase velocity: carrier wave and envelope

**Heuristic:** VG — Verification Gap
**Rank:** Important

**BLOCK 1 — ILLUSTRAE PASTE BLOCK:**
Draw a horizontal two-snapshot diagram showing a wave packet at two successive time moments, t₁ and t₂, to illustrate the distinction between phase velocity and group velocity. In the top row (t₁): a modulated wave — a fast oscillating carrier multiplied by a slow amplitude envelope — shown as a thick envelope curve enclosing thin carrier oscillations. Mark two reference features: a crest of the carrier wave (phase marker, small filled circle on the carrier peak) and the center of the envelope (group marker, vertical dashed line at the envelope maximum). In the bottom row (t₂): the same wave packet at a later time. The envelope center has moved a short distance to the right (group velocity, v_g); the carrier crest has moved a longer distance to the right (phase velocity, v_ph > v_g for a dispersive medium). Use horizontal arrows below each snapshot connecting the marker positions between t₁ and t₂, one arrow for the envelope displacement and one for the carrier-crest displacement, with the envelope arrow visibly shorter than the carrier-crest arrow to show v_g < v_ph. This relationship corresponds to the de Broglie matter-wave case (non-relativistic). Do not annotate with any text.

**BLOCK 2 — FULL SCOPE:**

`[S — SPECIFICATION]` Single-column 89 mm width, 300 DPI, SVG/EPS, white background. Two-row stacked layout (t₁ top, t₂ bottom) with displacement arrows between them below the x-axis.

`[C — CONTENT]` Each row: carrier wave (fast oscillation, thin curve), amplitude envelope (slow modulation, thick dashed curve), phase marker (filled circle on a carrier crest), group marker (vertical dashed line at envelope center). Between-row arrows: envelope displacement arrow (shorter, indicating v_g) and phase-marker displacement arrow (longer, indicating v_ph). The phase-marker displacement is approximately twice the envelope displacement to reflect v_ph = v/2 and v_g = v for the non-relativistic de Broglie case (ratio 2:1 approximately, inferred from the chapter's explicit result).

`[O — ORGANIZATION]` Top row (t₁) and bottom row (t₂) share the same horizontal x-axis scale. Phase marker (carrier crest): Blue filled circle. Envelope center marker: vertical Orange dashed line. Below the two rows: two horizontal arrows stacked, annotated only by their relative lengths (no text). The envelope arrow is drawn in Bluish Green; the phase arrow is drawn in Vermillion. No third row.

`[P — PRESENTATION]` Flat vector, Okabe-Ito palette, 1 pt strokes, white background, no baked text. Carrier wave curve: Blue `#0072B2`, 1 pt. Envelope curve: Orange `#E69F00`, 2 pt dashed. Phase marker circle: Blue `#0072B2` filled. Group/envelope marker line: Orange `#E69F00` dashed. Group displacement arrow: Bluish Green `#009E73`. Phase displacement arrow: Vermillion `#D55E00`. Row divider: light gray. Axes: black, 1 pt.

`[E — EXCLUSIONS]` Omit: dispersion relation curve (ω vs. k plot), Fourier components, probability density, double-slit. Do not show the wave packet spreading (dispersion broadening) — keep both snapshots at equal envelope width to isolate the velocity distinction. Do not depict more than one wave packet per row.

**BLOCK 3 — NEGATIVE PROMPT:**
Dispersion relation ω-k plot, Fourier decomposition spectrum, probability density axes, double-slit geometry, envelope spreading / broadening, multiple simultaneous wave packets, text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, dual-headed arrows, hand-drawn styles, human figures, visual clutter, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion.

---

## Video Candidate Pass

**Figure 1 — Sinusoidal wave anatomy**
STATIC SUFFICIENT. The anatomy of a wave is a spatial snapshot — amplitude, wavelength, phase, and the Euler-circle projection are all structural features that a single frozen frame conveys completely. No step unfolds in time.

**Figure 2 — Superposition and interference: three-panel comparison**
STATIC SUFFICIENT. The three panels are a comparison set, not a temporal sequence. The learning target is the amplitude contrast across phase offsets, which is fully visible in a side-by-side static layout.

**Figure 3 — Group velocity vs. phase velocity: carrier and envelope**
VIDEO CANDIDATE. Criterion: transition mechanism is the learning target. The core misconception (phase velocity ≠ particle speed) is resolved by watching the carrier crest and the envelope center move at different speeds simultaneously. A static two-snapshot approximation conveys the direction of travel but not the lived sense of the two motions diverging from the same initial packet. Animation — showing the carrier oscillations rippling fast while the envelope drifts slowly — is the most direct demonstration of why v_ph = v/2 while v_g = v for a matter wave. **Recommend as the single video for this module.**
