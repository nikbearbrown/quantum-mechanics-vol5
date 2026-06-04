# Research Notes: Module M-18 — Trigonometry, Waves, and the Harmonic Model
**Optional companion module.** Refresher for QM chapters: I·2 (matter waves).
**Condensed from:** `_lib_mfp1-03-trigonometry-and-geometry.md`
**Generated:** 2026-06-03

---

## A. The tool (key results condensed; the formulas that matter; a worked example)

### The three ratios (right triangle)
For an acute angle θ in a right triangle:
$$\sin\theta = \frac{\text{opposite}}{\text{hypotenuse}}, \quad \cos\theta = \frac{\text{adjacent}}{\text{hypotenuse}}, \quad \tan\theta = \frac{\text{opposite}}{\text{adjacent}}$$
These are pure numbers (dimensionless). They depend only on θ, not on the triangle's size (similar triangles).

**Component rule**: for a vector of magnitude A at angle θ from a chosen axis:
$$A_{\text{along}} = A\cos\theta \quad(\text{adjacent}), \qquad A_{\perp} = A\sin\theta \quad(\text{opposite})$$
The component *along the direction you measure the angle from* carries cosine; the *perpendicular* component carries sine.

**Pythagorean identity** (the fundamental constraint):
$$\cos^2\theta + \sin^2\theta = 1$$

### The unit circle and general angles
For any angle θ (measured counterclockwise from positive x-axis), the point on the unit circle is (cos θ, sin θ). Extends the definitions beyond 90°; makes periodicity manifest. Period: 2π (one full turn).

### The radian: the natural unit for angles
- Radian: angle subtending arc length equal to the radius. Full circle: 2π rad = 360°.
- Radian is dimensionless (arc length / radius = length / length).
- **Not merely another unit to convert**: the calculus identities d(sin θ)/dθ = cos θ and d(cos θ)/dθ = −sin θ hold *only in radians*. This is because the limit sin θ/θ → 1 as θ → 0 requires θ in radians. Using degrees in calculus gives a spurious factor of π/180 in every derivative.

### Laws for non-right triangles
Law of sines: a/sin A = b/sin B = c/sin C

Law of cosines: c² = a² + b² − 2ab cos C (Pythagorean theorem with correction; reduces to it when C = 90°)

### Key trig identities for waves
$$\sin(\alpha \pm \beta) = \sin\alpha\cos\beta \pm \cos\alpha\sin\beta$$
$$\cos(\alpha \pm \beta) = \cos\alpha\cos\beta \mp \sin\alpha\sin\beta$$
$$\sin^2\theta + \cos^2\theta = 1$$
Double-angle: sin 2θ = 2 sin θ cos θ; cos 2θ = cos²θ − sin²θ = 1 − 2sin²θ

**Product-to-sum** (crucial for interference):
$$\cos A \cos B = \frac{1}{2}[\cos(A-B) + \cos(A+B)]$$
$$\sin A + \sin B = 2\sin\!\left(\frac{A+B}{2}\right)\cos\!\left(\frac{A-B}{2}\right)$$

### Small-angle approximation
For small θ in radians:
$$\sin\theta \approx \theta, \quad \tan\theta \approx \theta, \quad \cos\theta \approx 1 - \tfrac{1}{2}\theta^2$$
More precisely (Taylor series, first derived by Mādhava c. 1400, later Newton/Leibniz):
$$\sin\theta = \theta - \frac{\theta^3}{6} + \frac{\theta^5}{120} - \cdots, \qquad \cos\theta = 1 - \frac{\theta^2}{2} + \frac{\theta^4}{24} - \cdots$$
The limit sin θ/θ → 1 as θ → 0 (in radians) is the foundation of the small-angle approximation.

### The sinusoidal wave
A traveling sinusoidal wave in 1D:
$$\psi(x,t) = A\cos(kx - \omega t + \varphi)$$
or in complex exponential form (the working form in QM):
$$\psi(x,t) = A e^{i(kx - \omega t)}$$
Key quantities and their dimensions:
- Amplitude A: units of the wave quantity (arbitrary)
- Wavenumber k = 2π/λ ([L⁻¹]): spatial frequency
- Angular frequency ω = 2π/T = 2πf ([T⁻¹]): temporal frequency  
- Phase velocity v_ph = ω/k ([LT⁻¹])
- Phase φ: dimensionless (radians)

The argument of the sinusoid, kx − ωt + φ, must be dimensionless. This is a dimensional-analysis check: k in rad/m, x in m → kx dimensionless; ω in rad/s, t in s → ωt dimensionless.

### Superposition and interference
Two waves of equal amplitude and frequency, differing by phase δ:
$$\psi_1 + \psi_2 = A\cos(kx-\omega t) + A\cos(kx-\omega t + \delta) = 2A\cos(\delta/2)\cos(kx-\omega t+\delta/2)$$
Resultant amplitude: 2A cos(δ/2).
- δ = 0 (in phase): amplitude 2A — **constructive interference**
- δ = π (anti-phase): amplitude 0 — **destructive interference**
- General δ: amplitude 2A |cos(δ/2)|

Two waves of slightly different frequency (ω, k) and (ω + dω, k + dk) — beat pattern / group structure:
$$\psi_1 + \psi_2 \propto \cos\!\left(\frac{dk}{2}x - \frac{d\omega}{2}t\right)\cos(kx - \omega t)$$
Fast carrier oscillates at k, ω; slow envelope moves at group velocity v_g = dω/dk.

### The complex exponential and Euler's formula
$$e^{i\theta} = \cos\theta + i\sin\theta$$
This is the bridge between trigonometric and exponential notation. In QM, wavefunctions are complex; the real sinusoid A cos(kx − ωt) is the real part of Ae^{i(kx−ωt)}.

Key consequence: the product of two complex exponentials is e^{iα} · e^{iβ} = e^{i(α+β)}, which is addition of phases. This is why the complex exponential is the natural language for interference: phase addition is just addition of exponents.

### Worked example: de Broglie wave and double-slit interference
de Broglie: λ = h/p, k = p/ℏ, ω = E/ℏ. The quantum matter wave is:
$$\psi(x,t) = A e^{i(px/\hbar - Et/\hbar)} = A e^{i(kx - \omega t)}$$
For an electron passing through two slits separated by d, the path-length difference for a detector at angle θ is Δ = d sin θ. The phase difference is:
$$\delta = k\Delta = \frac{2\pi}{\lambda}d\sin\theta = \frac{pd\sin\theta}{\hbar}$$
Constructive interference when δ = 2πn, i.e. d sin θ = nλ — the standard double-slit condition. The intensity pattern is |ψ_1 + ψ_2|² = 4A²cos²(δ/2).

---

## B. Where the quantum series uses it (specific QM chapters + how)

**I·2 — Matter waves**
- The entire chapter rests on the sinusoidal wave model. de Broglie's hypothesis λ = h/p assigns every particle a wavelength, and the interference phenomena that confirm it (Davisson–Germer, double-slit electron diffraction) are applications of the superposition and interference formulas above.
- Wavenumber k = p/ℏ and angular frequency ω = E/ℏ: the wave–particle correspondence translates directly into the trigonometric wave language. Students need fluency with ψ(x,t) = Ae^{i(kx−ωt)} to work in I·2.
- Phase vs. group velocity: the de Broglie matter wave has phase velocity v_ph = ω/k = E/p = (p²/2m)/(p) = p/(2m) = v/2 (non-relativistic case) — half the particle speed. The group velocity v_g = dω/dk = p/m = v — the particle's actual speed. Understanding why v_ph ≠ v requires the beat/envelope analysis from this module.
- Small-angle approximation: the double-slit interference pattern formula d sin θ ≈ dθ for small angles is exactly sin θ ≈ θ. Students who do not have the small-angle approximation internalized will miss this step.
- Complex notation: QM wavefunctions are complex from the start (Schrödinger equation is complex). Students need Euler's formula and the connection between A cos(kx−ωt) and Re[Ae^{i(kx−ωt)}] established before I·2 (or at the start of it).

---

## C. Connections

- **Complex exponentials (M linked to mfp1-12)**: the full treatment of e^{iθ} = cos θ + i sin θ belongs to the complex numbers module. M-18 should establish the formula and its use for representing waves; the complex number module develops it algebraically. These two modules are complementary.
- **Fourier analysis (M linked to mfp1-14 / mfp2-06)**: a general wave is a superposition of sinusoids — the Fourier decomposition. The sinusoidal wave of this module is the single Fourier component. The uncertainty principle ΔxΔk ≥ ½ is a mathematical property of the Fourier transform of wave packets, rooted in the same sinusoidal structure.
- **Units and dimensions (M-17)**: the argument of any sinusoid or exponential must be dimensionless. k has units of rad/m, x in m, so kx is dimensionless. ω has units of rad/s, t in s. This is an immediate application of M-17's dimensional homogeneity principle, and worth making explicit.
- **Small-angle → linearization**: the small-angle approximation sin θ ≈ θ is the first instance of "linearize near equilibrium" — a move that recurs throughout QM (perturbation theory, linear response, WKB). Flagging this pattern here seeds the habit.
- **Harmonic oscillator**: the quantum harmonic oscillator (QM II or III) is governed by the same sinusoidal solutions that appear here. The connection cos(ωt + φ) ↔ energy eigenstates of the QHO is worth previewing.

---

## D. Conventions and pitfalls

- **Radians are mandatory in calculus**: d(sin θ)/dθ = cos θ holds only in radians. The factor sin θ/θ → 1 only when θ is in radians. Students must not substitute degrees into wave formulas.
- **Sign convention for traveling waves**: ψ = Ae^{i(kx−ωt)} travels to the right (+x direction). ψ = Ae^{i(kx+ωt)} travels left. Some texts define wave as A cos(ωt − kx), which is the same rightward-traveling wave. Be consistent within the series.
- **Phase velocity vs. group velocity**: for matter waves (non-relativistic), v_ph = v/2 but v_g = v. Students often expect the wave to "travel with the particle" — that is the group velocity, not the phase velocity.
- **Complex conjugate**: |ψ|² = ψ*ψ, not ψ². In particular, |Ae^{ikx}|² = A², not A²e^{2ikx}. Students must not square complex exponentials without taking the modulus.
- **Wavelength vs. wavenumber**: λ = 2π/k (not 1/k). The factor of 2π is the source of many off-by-2π errors.
- **Reduced Planck constant**: de Broglie relation is λ = h/p, but written in k: k = p/ℏ (with ℏ = h/2π). Students confuse h and ℏ in the wave relation.
- **Sin θ ≈ θ validity**: the approximation is good to ~1% for θ < 0.14 rad (~8°); to ~10% for θ < 0.45 rad (~26°). Explicitly state the domain of validity when used in interference problems.

---

## E. Teaching considerations

- **Assign before I·2**: the sinusoidal wave ψ(x,t) = Ae^{i(kx−ωt)} is used in the first pages of I·2. Students need k, ω, phase, and Euler's formula before the chapter begins.
- **The complex exponential is the working form in QM**: the module should teach A cos(kx−ωt) and A e^{i(kx−ωt)} side by side, showing that the latter is more algebraically convenient and that real physical results come from taking Re[·] or from |ψ|². Do not allow students to treat complex exponentials as merely a notation trick.
- **Interference as the central physical application**: the superposition formula (amplitude = 2A cos(δ/2)) is the engine of the double-slit result. Work through it explicitly. Students who understand this derivation understand quantum interference from the inside.
- **Group velocity deserves a dedicated worked example**: the beats derivation (sum of two nearby frequencies → fast carrier and slow envelope) is at the right level and directly explains why the particle's speed equals v_g, not v_ph. Without this, de Broglie waves are mysterious.
- **Small-angle approximation is a skill, not a fact**: do not simply state sin θ ≈ θ; show it on the unit circle (arc ≈ vertical drop for small θ) and as the leading term of the Taylor series. The series connection previews the series-expansion module.
- **Historical note**: Mādhava (c. 1400) found the full sine and cosine series roughly 250 years before Newton/Leibniz. Worth a sentence; reinforces that mathematical tools have deep, non-Western roots.

---

## F. Source file used

`/Users/bear/Documents/CoWork/bear-textbooks/books/quantum-mechanics-vol5/pantry/_lib_mfp1-03-trigonometry-and-geometry.md`

Key sections used: §right triangle ratios, §components from magnitude and angle (central derivation), §unit circle and radian, §laws of sines and cosines, §small-angle approximation, §Worked examples (incline, projectile range, force triangle).

Wave-specific content (sinusoidal wave parameterization, k/ω/phase definitions, superposition/interference, group vs. phase velocity, Euler's formula, de Broglie wave example) was authored in section A and B based on standard sources (see G).

---

## G. Gaps and flags

- **Sinusoidal wave content**: the source chapter covers trigonometry and geometry, not wave physics as such. The sinusoidal wave ψ(x,t) = Ae^{i(kx−ωt)}, interference formulas, and group velocity analysis were authored here from standard references: Griffiths, *Introduction to Quantum Mechanics* (3rd ed.) §1.3–1.4; French, *Vibrations and Waves* Ch. 7; Crawford, *Waves* (Berkeley Physics Course Vol. 3) Ch. 1–2. Verify against the series' own wave treatment.
- **Euler's formula / complex exponentials**: the source chapter does not cover these. M-18 should be cross-referenced with the complex numbers module (mfp1-12). The module should state explicitly whether Euler's formula is being taught here or assumed from the complex numbers module.
- **Group velocity derivation**: not in source chapter; authored here. The derivation is standard (see e.g. French §7.6). Verify that the series does not develop this in a dedicated waves chapter that would make M-18's treatment redundant.
- **Double-slit interference worked example**: authored here. Should be checked against I·2 to ensure the notation (k, λ, δ, Δ) matches what the QM chapter uses.
- **Scope boundary with Fourier module**: this module covers the single sinusoid and its superposition. Fourier analysis (general superposition of sinusoids → wave packets → uncertainty principle) belongs to the Fourier module. M-18 should point to that module for wave packet treatment rather than duplicating it.
