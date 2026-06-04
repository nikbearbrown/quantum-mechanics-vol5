# CAJAL Figure Report — Module M-17 — Units, Dimensions, and Estimation

Recommended: 2 figures, Foundational density.

---

## Figure 1 — Dimensional analysis procedure: pendulum and Bohr radius side by side

**Heuristic:** MC — Mechanism/Process
**Rank:** Critical

**BLOCK 1 — ILLUSTRAE PASTE BLOCK:**
Draw a two-panel flowchart illustrating the Rayleigh dimensional-analysis procedure, applied once to the pendulum period and once to the Bohr radius, so the student sees the same method applied at classical and quantum scales. Left panel (pendulum): a three-row input column listing the candidate variables (length ℓ, gravitational acceleration g, bob mass m), each with its dimension written symbolically. An arrow feeds into a matrix-solve step represented as a horizontal dimension-equation block with three rows (M, L, T) showing which exponents must sum to match the target dimension T¹L⁰M⁰. The output at the bottom is the derived power law T_p ∝ √(ℓ/g), with mass struck through to show it drops out. Right panel (Bohr radius): the same three-row structure with ℏ, m_e, and the electromagnetic coupling e²/4πε₀, their dimensions listed symbolically. The same M-L-T matrix block, and the output a_0 ∝ ℏ²/(m_e · e²/4πε₀). Use consistent color coding across both panels: input-variable nodes in one color, the dimension-matching block in a second, and the output result in a third. Connect panels with a shared method arrow to emphasize the single procedure applied at two scales.

**BLOCK 2 — FULL SCOPE:**

`[S — SPECIFICATION]` Single-column 89 mm width, 300 DPI, SVG/EPS, white background. Two-panel layout, panels side by side of equal width, separated by a thin vertical rule, with a shared method label between them.

`[C — CONTENT]` Left panel: three input nodes (ℓ, g, m) with dimension annotations → dimension-exponent matrix block (3 rows: M, L, T) → output node (T_p ∝ √(ℓ/g), mass crossed out). Right panel: three input nodes (ℏ, m_e, e²/4πε₀) with dimension annotations → same matrix block structure → output node (a_0 ∝ ℏ²/(m_e·coupling)). No numerical values in the image. No variable labels or text baked into vectors.

`[O — ORGANIZATION]` Top-to-bottom flow within each panel: input column → arrow → matrix block → arrow → output. The matrix block is a rectangle divided into three horizontal rows, each row representing one base dimension (M, L, T). A shared horizontal double-headed arrow connecting the two matrix blocks indicates they use the same method. The crossed-out mass node in the left panel uses a diagonal strike mark.

`[P — PRESENTATION]` Flat vector, Okabe-Ito palette, 1 pt strokes, white background, no baked text. Input-variable nodes: Sky Blue `#56B4E9`. Dimension-matrix block: Blue `#0072B2`. Output nodes: Bluish Green `#009E73`. Struck-out mass node: light gray with Vermillion `#D55E00` diagonal strike. Method-link arrow: Orange `#E69F00`. Background: white.

`[E — EXCLUSIONS]` Omit: numerical values of any constants, SI unit symbols, Buckingham Π-theorem formal statement, significant figures, natural units. Do not depict the pendulum as a physical object or the hydrogen atom as an orbital diagram. Do not include any text baked into the image.

**BLOCK 3 — NEGATIVE PROMPT:**
Physical pendulum illustration, orbital atom diagram, Bohr orbit circles, numerical constant values, SI unit abbreviations baked in, text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, dual-headed arrows, hand-drawn styles, human figures, visual clutter, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion.

---

## Figure 2 — Quantum scales on a log axis: ℏ as action, a₀, λ_C, and classical-quantum crossover

**Heuristic:** PQ — Proportional/Quantitative
**Rank:** Important

**BLOCK 1 — ILLUSTRAE PASTE BLOCK:**
Draw a single horizontal logarithmic axis spanning length scales from roughly 10⁻¹⁵ m (femtometer / Compton wavelength regime) to 10⁻⁹ m (nanometer / de Broglie wavelength regime). Place three labeled tick-mark positions on the axis: the Compton wavelength λ_C ≈ 3.9×10⁻¹³ m, the Bohr radius a₀ ≈ 5.3×10⁻¹¹ m, and the de Broglie wavelength of a 1 eV electron ≈ 1.2×10⁻⁹ m. Use distinct marker shapes or colored triangular markers above the axis for each. Below the axis, indicate two regime zones with colored bands: a left zone (λ < λ_C) labeled by color as the relativistic-QM / pair-production regime; a right zone (λ > a₀) labeled by color as the non-relativistic regime. Between λ_C and a₀ mark the non-relativistic QM window. Above the axis, show a secondary bar indicating the "classical fails" zone (scales ≤ a₀) compared to "classical adequate" (scales >> a₀ in macroscopic regime, off the right edge). The axis must start at its left boundary with no truncation visual artifact — the axis extends with a left arrow to indicate smaller scales continue.

**BLOCK 2 — FULL SCOPE:**

`[S — SPECIFICATION]` Single-column 89 mm width, 300 DPI, SVG/EPS, white background. Single horizontal log-scale axis, full width of the column, with colored regime bands below and marker triangles above.

`[C — CONTENT]` Log axis: 10⁻¹⁵ m to 10⁻⁹ m, base-10 tick marks at each decade. Three markers: λ_C (Compton wavelength, ≈ 3.9×10⁻¹³ m), a₀ (Bohr radius, ≈ 5.3×10⁻¹¹ m), λ_dB (1 eV electron, ≈ 1.2×10⁻⁹ m). Regime bands below the axis: Vermillion `#D55E00` band (relativistic/QFT zone, left of λ_C), Blue `#0072B2` band (non-relativistic QM window, λ_C to a₀), Bluish Green `#009E73` band (atomic/molecular scale, a₀ to λ_dB). No numerical values baked into the image; positions only.

`[O — ORGANIZATION]` The axis runs left to right with a left-extending arrow indicating continuation below the shown range. Decade tick marks are uniform height. Three colored triangular markers sit above the axis at their respective positions. Regime color bands are rectangles of equal height below the axis, separated by vertical dividers at λ_C and a₀. A secondary thin bar above the axis spans the atomic regime (λ_C to λ_dB) and is distinguished from the full axis bar by color.

`[P — PRESENTATION]` Flat vector, Okabe-Ito palette, 1 pt strokes, white background, no baked text. Axis line: black. Compton marker triangle: Vermillion `#D55E00`. Bohr-radius marker triangle: Blue `#0072B2`. de Broglie marker triangle: Bluish Green `#009E73`. Regime band left: Vermillion `#D55E00` at 25% opacity. Regime band middle: Blue `#0072B2` at 25% opacity. Regime band right: Bluish Green `#009E73` at 25% opacity. Secondary bar: Orange `#E69F00`.

`[E — EXCLUSIONS]` Omit: energy-level diagram, atomic orbital pictures, momentum axis, natural-units conversion labels, SI unit abbreviations baked in, any numbers baked into the image. Do not show a y-axis. Do not depict any wave oscillations or sinusoidal curves on this figure — it is a scale diagram only.

**BLOCK 3 — NEGATIVE PROMPT:**
Energy-level diagram, orbital diagrams, momentum axis, wave oscillation curves, y-axis with probability density, text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, dual-headed arrows, hand-drawn styles, human figures, visual clutter, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion.

---

## Video Candidate Pass

**Figure 1 — Dimensional analysis procedure: pendulum and Bohr radius side by side**
VIDEO CANDIDATE. Criterion: ≥3 sequential causal stages. The dimensional-analysis procedure has three distinct sequential steps — write the candidate variables with their dimensions, set up and solve the exponent-matching system, read off the derived scaling law — and the student benefits from seeing each step appear in order rather than all at once. Animating the procedure through both worked examples (classical then quantum) with each step building on the last makes the universality of the method apparent. **Recommend as the single video for this module.**

**Figure 2 — Quantum scales on a log axis**
STATIC SUFFICIENT. A static axis snapshot is the correct format for a scale-comparison diagram. There is no temporal or procedural sequence; the spatial arrangement of scales on a log axis is the complete message.
