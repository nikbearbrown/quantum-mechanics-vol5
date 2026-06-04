# Research Notes: Module M-04 — Series Expansions and Approximation

**Optional companion module.** Refresher for QM chapters: III·1 (time-independent perturbation theory), III·4 (WKB approximation)
**Condensed from:** _lib_mfp1-13-series-expansions-and-approximations.md
**Generated:** 2026-06-03

---

## A. The Tool — Key Results a QM Student Needs

### Taylor and Maclaurin series

Any sufficiently smooth function f can be approximated near a point a by a polynomial whose coefficients are the function's derivatives at a:

**Taylor series:** f(x) = Σ_{n=0}^{∞} [f^{(n)}(a)/n!] (x − a)^n

When a = 0 this is the **Maclaurin series.** The coefficients are forced: the n-th coefficient must be f^{(n)}(0)/n! to reproduce all derivatives at the expansion point.

### The three series physics (and QM) lives on

All three converge for all real x:

**e^x = 1 + x + x²/2! + x³/3! + x⁴/4! + ···**

**sin x = x − x³/3! + x⁵/5! − x⁷/7! + ···** (odd powers, alternating signs)

**cos x = 1 − x²/2! + x⁴/4! − x⁶/6! + ···** (even powers, alternating signs)

Euler's formula (M-01) is proved by substituting x = iθ into the exponential series: the real and imaginary parts separate into exactly the cosine and sine series. This is the clearest example of how series machinery unlocks a deeper identity.

### Small-parameter expansions: keep the first few terms

Truncate at a finite order and you have an approximation valid near the expansion point. The first dropped term estimates the error.

**Small-angle:** sin θ ≈ θ, cos θ ≈ 1 − θ²/2. Relative error ≈ θ²/6 for sin θ ≈ θ (in radians). At 15°, error ≈ 1%; at 5°, ≈ 0.1%.

**Binomial approximation:** (1 + x)^n ≈ 1 + nx for |x| ≪ 1, any real n.
Useful cases: √(1+x) ≈ 1 + x/2; 1/(1−x) ≈ 1 + x.

### Taylor expansion of a potential: the universal oscillator

**Every smooth potential near a minimum is quadratic:**

Expand V(x) about its minimum x₀:
V(x) = V(x₀) + V'(x₀)(x−x₀) + ½V''(x₀)(x−x₀)² + ···

At a minimum: V'(x₀) = 0. Drop cubic and higher terms. Letting u = x − x₀:

V(x) ≈ V(x₀) + ½ k_eff u²,   where k_eff = V''(x₀)

This is a harmonic potential with spring constant = curvature of V at its minimum. Angular frequency of small oscillations: ω = √(k_eff/m) = √(V''(x₀)/m). The QHO is the leading-order model for any molecular bond, any lattice site, any potential well, because the Taylor expansion of V always starts quadratic at a minimum.

### Convergence — the practical picture

A power series converges within a **radius of convergence** around the expansion point. Outside that radius, partial sums diverge instead of approximating the function. The three series above converge everywhere; the geometric series 1/(1−x) = 1 + x + x² + ··· converges only for |x| < 1. Truncating is reliable near the expansion point; trust degrades away from it. "Small parameter" must genuinely be small compared to 1 (or to the characteristic scale of the problem).

### Worked example: the Taylor approximation of e^{−x} for small x

e^{−x} = 1 − x + x²/2 − x³/6 + ···. For x = 0.1: keeping two terms gives 1 − 0.1 = 0.9; the true value is e^{−0.1} ≈ 0.9048. Error ≈ 0.005, which is (0.1)²/2 = 0.005. The next term predicts the error.

---

## B. Where the Quantum Series Uses It

**QM Vol. III, Ch. 1 (Time-Independent Perturbation Theory):** Perturbation theory is an expansion of energy eigenvalues and eigenstates in powers of the small parameter λ (the coupling strength of the perturbation H'). The first-order correction E^{(1)}_n = ⟨n⁰|H'|n⁰⟩ is the λ¹ term; the second-order correction E^{(2)}_n involves a sum over intermediate states and is the λ² term. The whole method is a power-series expansion of E and ψ in λ, truncated at first or second order. Students who do not recognize this as a Taylor-series truncation cannot judge when perturbation theory is valid (when λ is small) or estimate the error of the approximation (the next term in the series).

Specifically: the condition for first-order perturbation theory to be reliable is |⟨m⁰|H'|n⁰⟩/(E_n⁰ − E_m⁰)| ≪ 1 for all m ≠ n. This is the "small parameter" condition — the ratio of the perturbation matrix element to the unperturbed energy splitting must be small. Checking this is the convergence check of the underlying series.

**QM Vol. III, Ch. 4 (WKB Approximation):** WKB is a semiclassical expansion in powers of ℏ (or equivalently, an expansion that assumes the potential varies slowly over a de Broglie wavelength). The leading-order WKB wave function is e^{(i/ℏ)∫p(x)dx} times a slowly varying amplitude, and corrections are higher powers of ℏ. The expansion breaks down near turning points where p(x) → 0 and the "small" parameter (ℏ/p dp/dx) becomes large. Recognizing this as a series expansion that fails at its radius of convergence is the key to understanding why connection formulas are needed at turning points.

Additionally, the WKB quantization condition ∮ p dx = nℏ (where ∮ is over a full classical orbit) is derived by matching oscillatory and evanescent solutions — which themselves come from recognizing the local ODE as approximately constant-coefficient (the first term in a Taylor expansion of V around each x). The small-parameter structure underpins the whole approximation.

---

## C. Connections

**Earlier math modules this needs:**
- M-01 (Complex Numbers): Euler's formula is the payoff of substituting x = iθ into the exponential series. The series expansion of e^{iθ} is the bridge between real series and complex exponentials.
- M-03 (ODEs): The QHO solution involves recognizing that V(x) ∝ x² near the minimum (a Taylor truncation) and then solving the resulting ODE. WKB uses Taylor expansion of V(x) locally.

**QM chapters this unlocks:**
- Vol. III, Ch. 1 (perturbation theory — the whole framework is a power series in the perturbation strength).
- Vol. III, Ch. 4 (WKB — a semiclassical series expansion; breakdown at turning points = radius-of-convergence failure).
- Any calculation where ψ or E is expanded in a small parameter: variational method (which often involves Taylor-expanding an expectation value), degenerate perturbation theory (small off-diagonal corrections).
- Vol. I, Ch. 6 (QHO): recognizing V(x) = ½mω²x² as the Taylor expansion of any potential near its minimum motivates the QHO as a universal model.

---

## D. Conventions and Pitfalls

**Radians, not degrees.** The series sin x = x − x³/6 + ··· holds only when x is in radians. Using degrees makes sin(θ°) ≈ θ° false — the correct small-angle approximation is sin θ ≈ π θ°/180°, which is not a useful formula. In QM this matters when a phase angle appears in an approximation.

**The expansion point matters.** The Taylor series of f about a = 0 is not the same as the Taylor series about a = x₀. Perturbation theory expands the Hamiltonian about its unperturbed value (H₀ + λH'); WKB expands the potential about the classical turning point. The wrong expansion point invalidates the approximation entirely.

**First-order perturbation theory: when it breaks.** The validity condition |H'_{mn}/(E_n − E_m)| ≪ 1 fails at degeneracy (E_n ≈ E_m), exactly where the denominator vanishes. Degenerate perturbation theory is the fix — but the lesson is that series expansion breaks down when the small-parameter condition is violated, which requires recognizing what the small parameter is.

**Asymptotic vs. convergent series.** Some QM approximations (notably the WKB series in ℏ) are asymptotic series that formally diverge but whose partial sums give excellent approximations when truncated at the right order. This is different from a convergent Taylor series. Advanced QM treatments flag this; the Vol. III WKB chapter should note it. The distinction is beyond this module but worth flagging for completeness.

**"Higher-order corrections" means "the next term in the Taylor series."** Students in perturbation theory often hear "second-order correction" without connecting it to the coefficient of λ² in a Taylor expansion. Making this connection explicit — writing E = E⁰ + λE¹ + λ²E² + ··· as a power series and asking "what does the coefficient of λ² look like?" — demystifies the perturbation expansion.

---

## E. Teaching Considerations

**Perturbation theory is a Taylor series.** The single most helpful framing for Vol. III Ch. 1: "We are expanding the exact energy eigenvalue E(λ) in a Taylor series in the small parameter λ, where H(λ) = H₀ + λH'. The zeroth-order term is the unperturbed energy. The first-order term is the first derivative, which by Hellmann-Feynman is ⟨H'⟩. The second-order term involves the second derivative, which produces the sum-over-states formula." This makes E^{(1)} and E^{(2)} recognizable as Taylor coefficients, not magical formulas.

**WKB validity = large-argument behavior of the series.** WKB works when the de Broglie wavelength λ_dB = h/p is much smaller than the scale over which p(x) changes — equivalently, when |dλ_dB/dx| ≪ 1. This is the "small parameter" for WKB, and the approximation breaks exactly when this ratio approaches 1 — the WKB equivalent of reaching the radius of convergence.

**Every minimum is a spring.** The Taylor-expansion argument (V near a minimum → ½k_eff u²) is one of the most unifying results in physics pedagogy. Showing it explicitly — expanding the Lennard-Jones potential, or the Morse potential, or even a simple double-well — and reading off ω from the curvature V'' gives students a tool they will use for the rest of their physics career. This belongs early in Vol. III Ch. 1 as motivation for why the QHO is the universal perturbation-theory reference system.

**"Small" means: small compared to what?** The question "how small does the parameter need to be?" always has the same answer: small compared to 1 after it has been made dimensionless by the appropriate scale. In perturbation theory, λ|H'_{mn}|/(E_n − E_m) must be ≪ 1. In WKB, |dλ_dB/dx| ≪ 1. Identifying the natural scale is the physicist's job; the series does not do it automatically.

---

## F. Source File Used

`_lib_mfp1-13-series-expansions-and-approximations.md`

Source chapter coverage: deriving Taylor/Maclaurin series by repeated differentiation; the three series (sin, cos, e^x); small-angle approximation with error estimate (≈ θ²/6); binomial approximation (1+x)^n ≈ 1+nx; radius of convergence at the intuitive level; the universal oscillator argument (V near a minimum → ½ k_eff u²); amplitude correction to the pendulum period (keeping the cubic term in sin). Three worked examples: linearized pendulum with error; amplitude correction; universal oscillator.

Source chapter does NOT cover: perturbation theory as a Taylor expansion; WKB as an asymptotic series; the ℏ expansion; asymptotic vs. convergent series. These QM applications need M-16-style material in Sections B and D.

---

## G. Gaps and Flags

- Source chapter is well-developed and self-contained. No thinness flag.
- The connection to perturbation theory (the key QM payoff) requires original M-16 material — the source chapter does not mention perturbation theory, and Section B above is entirely new authoring.
- WKB as a series expansion is also entirely new; the source gives only classical small-angle and binomial examples. Flag: this connection is load-bearing for Vol. III Ch. 4 but absent from the source.
- The source correctly notes that the three series (sin, cos, e^x) were derived first by Mādhava of Sangamagrāma in 14th-century Kerala, ~250 years before Newton and Taylor. The QM module should maintain this attribution rather than using "Taylor series" as the only name.
- The universal-oscillator result (V near minimum → ½ k_eff u²) is one of the strongest passages in the source (Example 3). This should be featured prominently in the module — it is the reason QHO perturbation theory is so universal.
