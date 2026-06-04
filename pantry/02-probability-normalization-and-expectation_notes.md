# Research Notes: Module M-02 — Probability, Normalization, and Expectation

**Optional companion module.** Refresher for QM chapters: I·3 (wave function and Born rule), I·9 (uncertainty principle), IV·1 (measurement and observables)
**Condensed from:** _lib_mfp2-08-probability-and-statistics-for-physics.md (primary); _lib_mfp1-08-the-integral.md and _lib_mfp1-09-integration-techniques-and-applications.md (for the integral mechanics underlying normalization and expectation integrals)
**Generated:** 2026-06-03

---

## A. The Tool — Key Results a QM Student Needs

### Probability density vs. probability

For a continuous random variable X, the probability density function (PDF) f(x) satisfies:
- f(x) ≥ 0 everywhere
- ∫_{−∞}^{∞} f(x) dx = 1   (normalization)
- P(a ≤ X ≤ b) = ∫_a^b f(x) dx   (probability over an interval)

f(x) is NOT a probability. It is a density: f(x) can exceed 1. Only an integral of f over an interval is a probability (bounded by 1). This distinction is the foundational pitfall in Born's rule.

### Mean (expectation value) and variance

For a continuous distribution with density f(x):

**Mean:** μ = E[X] = ∫_{−∞}^{∞} x f(x) dx

**Expectation of any function:** E[g(X)] = ∫_{−∞}^{∞} g(x) f(x) dx

**Variance:** σ² = Var(X) = E[(X − μ)²] = E[X²] − (E[X])²

"The mean of the square minus the square of the mean." This is the workhorse computational identity — always expand the square, use linearity, and the cross-term cancels cleanly.

**Standard deviation:** σ = √(Var(X)), same units as X.

Expectation is linear: E[aX + b] = aE[X] + b. This follows directly from linearity of the integral.

For independent random variables: Var(X + Y) = Var(X) + Var(Y). Variances add; standard deviations do not.

### Normalization as a constraint

The normalization condition ∫f dx = 1 is not optional — it expresses the certainty that the particle exists somewhere. In QM:

∫_{−∞}^{∞} |ψ(x,t)|² dx = 1

This is an integral equation constraining the overall amplitude of ψ. Determining the normalization constant (fixing the free multiplicative constant in a solution to the Schrödinger equation) is a routine integral computation. The integral techniques of M-09 — power rule, Gaussian integrals, improper integrals with limits at ±∞ — are what make normalization calculations executable.

Key Gaussian integral (needed repeatedly): ∫_{−∞}^{∞} e^{−αx²} dx = √(π/α), for α > 0.

### Worked example: expectation and uncertainty for a Gaussian wave packet

For ψ(x) ∝ e^{−x²/4σ²} (a Gaussian, properly normalized):
- ⟨x⟩ = 0 (by symmetry — the integrand x|ψ|² is odd)
- ⟨x²⟩ = σ² (from the Gaussian integral with an extra x² factor)
- Δx = √(⟨x²⟩ − ⟨x⟩²) = σ

The width σ of the Gaussian in position space is literally the standard deviation of the position distribution. The uncertainty principle Δx Δp ≥ ℏ/2 is saturated by the Gaussian — the Gaussian is the minimum-uncertainty state.

---

## B. Where the Quantum Series Uses It

**QM Vol. I, Ch. 3 (The Wave Function):** Born's rule states that |ψ(x,t)|² is the probability density for finding the particle at position x. This immediately demands: (1) knowing what a probability density is (density, not probability); (2) normalization ∫|ψ|² dx = 1; (3) computing ⟨x⟩ = ∫ x |ψ|² dx and ⟨x²⟩ for Δx. The entire formalism of Ch. I·3 is probability-of-a-continuous-distribution applied to |ψ|².

**QM Vol. I, Ch. 9 (The Uncertainty Principle):** Δx and Δp in the uncertainty relation Δx Δp ≥ ℏ/2 are standard deviations of the position and momentum probability distributions. The inequality is a mathematical theorem about Fourier transform pairs; its statement and its saturation (by Gaussians) are both probability-theory statements. Students who do not know that Δ means standard deviation cannot understand what the uncertainty principle asserts.

**QM Vol. IV, Ch. 1 (Measurement and Observables):** The expectation value of an observable Â is ⟨Â⟩ = ⟨ψ|Â|ψ⟩ = ∫ ψ*(x) Â ψ(x) dx. This is a probability-weighted mean, with the density |ψ|² replaced by ψ*ψ (they are equal for position eigenstates). The variance (ΔA)² = ⟨Â²⟩ − ⟨Â⟩² is the squared uncertainty in a measurement of A. The whole structure of observable measurement in QM is the continuous-distribution formalism of this module.

---

## C. Connections

**Earlier math modules this needs:**
- M-01 (Complex Numbers): |ψ|² = ψ*ψ requires taking the modulus squared of a complex function. Without M-01, the Born rule is opaque.
- The integral techniques from _lib_mfp1-08-the-integral.md and _lib_mfp1-09-integration-techniques-and-applications.md: normalization integrals and expectation integrals are definite integrals over infinite domains, often involving Gaussians and power-rule antiderivatives. Students who cannot evaluate ∫_{−∞}^{∞} x² e^{−αx²} dx are blocked at the first normalization calculation.

**QM chapters this unlocks:**
- All expectation value calculations in QM Vols. I–IV.
- Vol. I Ch. 9 (uncertainty principle as a standard-deviation inequality).
- Vol. IV Ch. 1 (measurement formalism, completeness, probability distributions over measurement outcomes).
- The entire language of ⟨Â⟩ and ΔA throughout the series.

---

## D. Conventions and Pitfalls

**Born rule: density, not probability.** The single most common error QM students make in Ch. I·3 is reading |ψ(x)|² as "the probability of the particle being at x." It is a probability density. The probability that the particle is found between x and x + dx is |ψ(x)|² dx — the density times the infinitesimal width. This error propagates: students "normalize" by setting |ψ(x₀)|² = 1 at some point rather than integrating, or conclude that a peaked wave function means "the particle is at the peak" rather than "the particle is most likely near the peak."

**⟨x⟩ is not the most probable x.** The expectation value is the mean of the distribution, not its mode (peak). For a symmetric distribution they coincide, but for asymmetric wave functions they differ. This confuses students who conflate "expected" with "most likely."

**Δ means standard deviation, not "small change."** In the context of QM uncertainty, Δx and Δp are standard deviations of their respective probability distributions. The notation Δ also appears in QM for finite increments (as in ΔE = E_2 − E_1). Students must distinguish these uses by context; the uncertainty-principle Δ always means √(⟨x²⟩ − ⟨x⟩²).

**Normalization can fail after time evolution.** A normalized wave function remains normalized under unitary (Hamiltonian) time evolution — the Schrödinger equation preserves normalization. But if a student truncates a series expansion or applies an approximation, normalization can be violated. Checking normalization after approximation is a good diagnostic.

**Improper integrals and boundary behavior.** Normalization of physical wave functions requires that ψ(x) → 0 as x → ±∞ (otherwise ∫|ψ|² dx diverges). Plane waves e^{ikx} are not normalizable in this sense; they are handled by Dirac-delta normalization or by restricting to a box. Students need to know which situations call for each treatment.

---

## E. Teaching Considerations

**"Probability density" needs a concrete picture.** The best entry point is a uniform distribution on [0, 1]: f(x) = 1 for 0 ≤ x ≤ 1. Here the density equals 1 everywhere but the probability of landing in any single point is 0. Then show a density that exceeds 1: f(x) = 2 for 0 ≤ x ≤ 0.5. Density > 1 is fine; no probability exceeds 1. This strips away the mystery before Born's rule arrives.

**Expectation value as a weighted average, not a likely value.** The formula ⟨x⟩ = ∫ x |ψ|² dx is the probability-weighted average of x — exactly the same as the average of a dataset, but with a continuous weight. Students who see this as "the mean of the position distribution" stop trying to find a special point x₀ where ψ peaks and call that the expectation.

**Uncertainty as spread, not ignorance.** Δx is the standard deviation of the position distribution if you were to prepare many copies of the same state and measure each one. It is a property of the state, not of the measurement apparatus or the experimenter's knowledge. Framing Δx as the "width of the probability distribution" rather than "how precisely we know x" avoids the misreading that measurement disturbs the system and creates the uncertainty.

**Gaussian integrals are worth memorizing in their general form.** The family ∫_{−∞}^{∞} x^{2n} e^{−αx²} dx (n = 0, 1, 2) appears constantly. Giving students the pattern — each xⁿ factor brings down a derivative with respect to α — saves algebraic time later and emphasizes that these are all closely related.

---

## F. Source Files Used

**Primary:** `_lib_mfp2-08-probability-and-statistics-for-physics.md`
Coverage: random variables; PDF vs. PMF; mean and variance (continuous and discrete); the identity E[X²] − E[X]²; independence and additivity of variance; Gaussian (de Moivre–Laplace theorem), Poisson, and Boltzmann distributions; propagation of uncertainty. Example 2 is directly the QM expectation value ⟨x⟩ and (Δx)², making this the strongest QM-relevant passage in the source.

**Supporting (for integral mechanics):**
- `_lib_mfp1-08-the-integral.md`: the definite integral as accumulated area; Fundamental Theorem; the fact that probability = area under the PDF curve.
- `_lib_mfp1-09-integration-techniques-and-applications.md`: substitution, integration by parts; setting up integrals over continuous distributions ("slice, write contribution, integrate" — the same move as normalization and expectation over a wavefunction).

---

## G. Gaps and Flags

- Source (mfp2-08) is well-developed and explicitly connects to QM (Example 2 is the Born rule expectation value, verbatim). No thinness flag.
- The Gaussian integral ∫_{−∞}^{∞} e^{−αx²} dx = √(π/α) is not derived in the source; it is assumed or relegated to a table. The module notes should either quote it explicitly or point to an integration-techniques note. This is a gap in the source material for the normalization calculation — flag for M-16 authoring.
- The Dirac-delta normalization of plane waves (vs. L² normalization) is not covered in the source. This is needed for Vol. I free-particle states and scattering. Flag: needs M-16 original material or a forward pointer to the QM chapter that introduces it.
- Propagation of uncertainty (source §3.6) is not directly needed for QM Vols. I–IV but is useful in experimental labs. Low priority for inclusion.
- Boltzmann distribution (source §3.5) — included in the source for completeness but not needed for the QM modules listed. Omit from module to keep focus.
