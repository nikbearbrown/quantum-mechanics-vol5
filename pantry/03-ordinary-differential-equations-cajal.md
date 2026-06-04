# CAJAL Figure Report — Module M-03 — Ordinary Differential Equations and Boundary Conditions

Recommended: 3 figures, Mixed density.

---

## Figure 1 — Three Solution Families of the Second-Order Linear ODE: Discriminant Decision Tree

**Heuristic:** MC — Mechanism/Process
**Rank:** Critical

### BLOCK 1 — ILLUSTRAE PASTE BLOCK

Draw a top-down process flowchart. At the top, place a single rectangular node representing the second-order linear ODE. Below it, a diamond decision node asks about the sign of the discriminant Δ = p² − 4q. Three branches descend from the diamond: left branch (Δ > 0, two distinct real roots), center branch (Δ = 0, repeated real root), right branch (Δ < 0, complex conjugate roots). Each branch leads to a rectangular terminal node showing the form of the general solution. Below the left terminal node, add a small schematic curve showing two real exponentials diverging from each other (one growing, one decaying). Below the center terminal node, show a single exponential modulated by a linear factor. Below the right terminal node, show a damped oscillatory curve. Connect the oscillatory solution box to a second-level annotation box indicating the quantum allowed-region case (u'' = −k²u), and connect the real-exponential box to a second-level annotation box indicating the quantum forbidden-region case (u'' = +κ²u). Use seven components total.

### BLOCK 2 — FULL SCOPE

**[S — SPECIFICATION]** Single-column 89 mm width, 300 DPI, vector (SVG/EPS), white background.

**[C — CONTENT]** The characteristic-equation method applied to u'' + pu' + qu = 0 with three outcome branches determined by the discriminant Δ = p² − 4q: (1) Δ > 0 → two real roots r₁ ≠ r₂ → Ae^(r₁x) + Be^(r₂x) with schematic diverging exponentials; (2) Δ = 0 → repeated root r₀ → (A + Bx)e^(r₀x) with schematic; (3) Δ < 0 → complex roots α ± iβ → e^(αx)(A cosβx + B sinβx) with damped oscillation schematic. The oscillatory branch is annotated as the quantum classically-allowed case; the real-exponential branch as the classically-forbidden case. These are the only inferred relations and are labeled as such.

**[O — ORGANIZATION]** Top-to-bottom flowchart. Root node at top center. Diamond node below it with three exits: left (Δ > 0), center (Δ = 0), right (Δ < 0). Terminal solution boxes at the second level. Small schematic curve thumbnails attached below each terminal box. Two annotation boxes at the bottom left (forbidden) and bottom right (allowed) connected by dashed lines to the relevant terminal boxes (these dashed connections are labeled as the QM correspondence, an inferred relation). Flowchart arrows are single-headed, top-to-bottom. Total labeled components: ODE node, diamond, three terminal nodes, two QM annotation nodes = 7.

**[P — PRESENTATION]** Flat vector, Okabe-Ito palette. ODE root node: Blue `#0072B2`, 1 pt border, white fill. Diamond decision node: neutral light gray fill, 1 pt border. Δ > 0 terminal (real exponentials): Vermillion `#D55E00`, 1 pt border. Δ = 0 terminal (repeated root): neutral light gray, 1 pt border. Δ < 0 terminal (oscillatory): Bluish Green `#009E73`, 1 pt border. Schematic curves: same color as their parent terminal box, 0.75 pt. QM annotation boxes: Sky Blue `#56B4E9`, 0.75 pt dashed border (inferred). Flowchart arrows: dark gray, 1 pt, single-headed. White background; no baked text.

**[E — EXCLUSIONS]** Omit: Wronskian or linear independence test; variation of parameters; non-constant-coefficient ODEs (Hermite, Bessel); higher-order ODEs (> 2nd order); the QHO Hermite polynomial chain; numerical ODE methods; complex-plane root locus diagram.

### BLOCK 3 — NEGATIVE PROMPT

Wronskian determinant diagram, variation of parameters panels, Hermite polynomial diagram, Bessel function, higher-order ODE, numerical method flowchart, complex root locus, text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, dual-headed arrows, hand-drawn styles, human figures, visual clutter, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 2 — Infinite Square Well: Eigenfunction Solutions and Energy Quantization

**Heuristic:** PQ — Proportional/Quantitative
**Rank:** Critical

### BLOCK 1 — ILLUSTRAE PASTE BLOCK

Draw a vertical energy-level diagram with the horizontal axis representing position x from 0 to L and the vertical axis representing energy E starting at zero. Draw two vertical infinite-wall lines at x = 0 and x = L extending upward to indicate the infinite potential barriers. At each of the first three energy levels (n = 1, 2, 3), draw a horizontal line at the appropriate height (proportional to n²: n=1 at height 1 unit, n=2 at height 4 units, n=3 at height 9 units relative to a baseline) spanning from x = 0 to x = L. Superimposed on each energy-level line, draw the corresponding standing wave eigenfunction ψₙ(x) = A sin(nπx/L) as a smooth sinusoidal curve, with the curve oscillating above and below the energy-level line. The n=1 waveform shows half a sine wave (one arch), n=2 shows a full sine wave (two arches, one up one down), n=3 shows one-and-a-half sine waves (three arches). Each waveform is contained between x = 0 and x = L and touches zero at both walls.

### BLOCK 2 — FULL SCOPE

**[S — SPECIFICATION]** Single-column 89 mm width, 300 DPI, vector (SVG/EPS), white background.

**[C — CONTENT]** Energy spectrum and eigenfunctions of the infinite square well from the module's worked example. Elements: (1) vertical potential walls at x = 0 and x = L (infinite barriers); (2) three horizontal energy levels at heights proportional to n² (n = 1, 2, 3) — the quantized energies Eₙ = n²π²ℏ²/2mL²; (3) eigenfunction waveforms ψₙ(x) = A sin(nπx/L) superimposed on each level as oscillating curves anchored to zero at both walls; (4) the n² spacing is visible from the unequal gaps between energy levels. The energy axis starts at zero. The n = 1 state is the ground state; each higher n has one additional node between the walls.

**[O — ORGANIZATION]** Vertical layout: energy axis on the left, position axis at the bottom (x from 0 to L). Infinite walls drawn as thick vertical lines at x = 0 and x = L with upward hatching to indicate infinite height. Energy levels as horizontal dashes at heights 1E₁, 4E₁, 9E₁ (the n² progression is the visual message). Waveforms ride on their respective energy-level lines, using that line as the zero-crossing baseline. Waveform amplitude is consistent across all three levels (uniform normalization visually). Energy level spacings clearly increase from level to level (gap from n=1 to n=2 is smaller than from n=2 to n=3).

**[P — PRESENTATION]** Flat vector, Okabe-Ito palette. Infinite walls: dark gray (near black), 2 pt, with upward hatch marks in the same dark gray. Energy level lines: Blue `#0072B2`, 0.75 pt, dashed. n=1 waveform: Bluish Green `#009E73`, solid, 1.5 pt. n=2 waveform: Orange `#E69F00`, solid, 1.5 pt. n=3 waveform: Reddish Purple `#CC79A7`, solid, 1.5 pt. Energy axis and position axis: light gray, 0.75 pt. White background; no baked text; no fill under waveforms.

**[E — EXCLUSIONS]** Omit: probability density |ψ|² curves (a downstream quantity — these are ψ, not |ψ|²); the finite square well (separate concept); the harmonic oscillator potential; time-dependent factor e^(−iEt/ℏ); energy levels beyond n = 3; the normalization constant derivation.

### BLOCK 3 — NEGATIVE PROMPT

probability density curves, finite square well, harmonic oscillator parabola, time-dependent arrows, energy levels beyond n=3, normalization integral steps, text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, dual-headed arrows, hand-drawn styles, human figures, visual clutter, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 3 — Finite Square Well: Oscillatory Interior, Evanescent Exterior, and Matching at the Interface

**Heuristic:** VG — Verification Gap
**Rank:** Important

### BLOCK 1 — ILLUSTRAE PASTE BLOCK

Draw a schematic of a one-dimensional finite square well. Use a horizontal position axis. Show the potential profile as a rectangular step: V = 0 outside (|x| > a), V = −V₀ inside (|x| < a), drawn as a thick step-function line. Draw a horizontal dashed energy line at a negative energy E (between −V₀ and 0) indicating a bound state energy. In the interior region (|x| < a) draw a smooth sinusoidal oscillating curve (the classically allowed oscillatory solution) riding above and below the energy line, anchored to zero curvature at the center. In the left exterior region (x < −a) draw a smooth decaying exponential rising from zero far left and approaching a finite value at x = −a. In the right exterior region (x > a) draw the mirror-image decaying exponential descending to zero far right. At each interface (x = −a and x = +a) draw a small filled dot where the interior and exterior curves meet, and draw short matching arrows indicating that both the curve value and the slope are continuous across the interface.

### BLOCK 2 — FULL SCOPE

**[S — SPECIFICATION]** Single-column 89 mm width, 300 DPI, vector (SVG/EPS), white background.

**[C — CONTENT]** Finite square well bound state: (1) the potential V(x) as a step function (V = −V₀ inside |x| < a, V = 0 outside); (2) a bound-state energy level E (negative, above −V₀) as a dashed horizontal line; (3) the oscillatory wavefunction inside (classically allowed, E > V); (4) the evanescent decaying exponential outside (classically forbidden, E < V); (5) matching conditions at x = ±a: the wavefunction and its first derivative are continuous (matching junction dots and slope-continuity indicators). This illustrates the two-solution-family picture plus the boundary matching from the module.

**[O — ORGANIZATION]** Horizontal position axis with three labeled regions: left exterior (x < −a), interior (|x| < a), right exterior (x > a). The interface positions x = −a and x = +a are marked by vertical dashed boundary lines spanning from the potential step upward through the wavefunction. Potential step: drawn as a thick line along the bottom, dropping to −V₀ inside. Energy level: horizontal dashed line above the −V₀ floor and below V = 0. Wavefunction: a single continuous curve that transitions smoothly from evanescent to oscillatory to evanescent, touching the matching dots at each interface. Matching indicators at both interfaces. Symmetry: the figure has left-right symmetry (even-parity bound state shown).

**[P — PRESENTATION]** Flat vector, Okabe-Ito palette. Potential step profile: dark gray (near black), 2 pt solid. Bound state energy dashed line: Blue `#0072B2`, dashed, 1 pt. Interior oscillatory wavefunction: Bluish Green `#009E73`, solid, 1.5 pt. Exterior evanescent wavefunction: Orange `#E69F00`, solid, 1.5 pt. Interface boundary vertical dashes: light gray, 0.75 pt, dashed. Matching junction dots: Vermillion `#D55E00`, filled circles, 3 pt diameter. Matching slope-continuity arrows (small angled tick pairs at each dot): Vermillion `#D55E00`, 0.75 pt. White background; no baked text.

**[E — EXCLUSIONS]** Omit: scattering states (E > 0 transmission/reflection); the WKB approximation turning-point connection formulas; the infinite square well (separate figure); multiple energy levels stacked; the harmonic oscillator potential; the quantization condition transcendental equation; complex exponential traveling-wave representation.

### BLOCK 3 — NEGATIVE PROMPT

scattering state transmission arrows, WKB connection formula diagram, multiple bound state levels stacked, harmonic oscillator parabola, transcendental equation graph, traveling wave complex exponential, text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, dual-headed arrows, hand-drawn styles, human figures, visual clutter, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Video Candidate Pass

**Figure 1 — Discriminant Decision Tree:** STATIC SUFFICIENT. The flowchart is a decision structure, not a causal process unfolding in time. The three branches exist simultaneously; a tree diagram communicates them without motion.

**Figure 2 — Infinite Square Well Eigenfunctions and Energy Levels:** VIDEO CANDIDATE. Criterion: ≥3 sequential causal stages with a transformation below direct observation. The logic chain — increase n → add one node → wavelength decreases → k increases → energy grows as n² — is a four-step causal progression. An animation that builds the levels one by one while showing each standing wave fitting into the box (half-wavelength at a time) and marking the new energy height would make the quantization-from-boundary-conditions argument kinetically visible. **Recommend this as the one video for Module M-03.**

**Figure 3 — Finite Well Matching:** STATIC SUFFICIENT. The matching condition at the interface is a single-point structural claim (value and slope must be equal). A static diagram with matching arrows at the junction communicates this fully; no cyclic or multi-stage process is the learning target.
