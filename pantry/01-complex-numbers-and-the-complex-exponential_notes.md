# Research Notes: Module M-01 — Complex Numbers and the Complex Exponential

**Optional companion module.** Refresher for QM chapters: I·3 (wave function), I·8 (wave packets), II·7 (spin)
**Condensed from:** _lib_mfp1-12-complex-numbers-and-exponentials.md
**Generated:** 2026-06-03

---

## A. The Tool — Key Results a QM Student Needs

### Complex arithmetic

A complex number z = a + bi, with i² = −1. Real part Re(z) = a, imaginary part Im(z) = b. Complex conjugate z̄ = a − bi. Modulus |z| = √(a² + b²); it is always real and non-negative.

Division: multiply numerator and denominator by the conjugate of the denominator. This is the only genuinely new move; everything else is ordinary algebra with i² = −1 inserted wherever it appears.

### Polar form and Euler's formula

Every complex number can be written z = re^{iθ}, where r = |z| is the modulus and θ = arg(z) is the argument (angle in the complex plane). The central identity:

**e^{iθ} = cos θ + i sin θ**   (Euler's formula)

Derived — not asserted — by substituting x = iθ into the Maclaurin series for e^x and sorting even/odd powers into the cosine and sine series respectively (see M-04 for the series machinery).

Key corollaries:
- cos θ = Re(e^{iθ}),  sin θ = Im(e^{iθ})
- Multiplication multiplies moduli and adds arguments: z₁z₂ = r₁r₂ e^{i(θ₁+θ₂)}
- The unit circle: |e^{iθ}| = 1 for all real θ
- e^{iπ} + 1 = 0 (Euler's identity — a special case, not the point)

### The complex exponential as oscillation + decay

A complex exponent r = −γ + iω gives:

e^{rt} = e^{(−γ + iω)t} = e^{−γt}(cos ωt + i sin ωt)

Real part of the exponent → decay envelope; imaginary part → angular frequency of oscillation. This is why the characteristic equation of a damped ODE (see M-03) produces an oscillating solution when its roots are complex: the imaginary part of the root *is* the frequency.

A general oscillation A cos(ωt + φ) is the real part of a single complex exponential:

A cos(ωt + φ) = Re(Ã e^{iωt}),   where Ã = Ae^{iφ}

The complex amplitude Ã encodes both magnitude and phase in one number. Adding two oscillations at the same frequency reduces to adding two complex numbers — one right-triangle calculation instead of a page of trig identities.

### Worked example: phasor addition

x₁ = 3 cos(ωt), x₂ = 4 cos(ωt + 90°). Complex amplitudes: Ã₁ = 3, Ã₂ = 4e^{iπ/2} = 4i.
Sum: Ã = 3 + 4i. Modulus = 5, argument = arctan(4/3) ≈ 53.1°.
Result: x₁ + x₂ = 5 cos(ωt + 53.1°). A Pythagorean calculation, not a trig-identity marathon.

---

## B. Where the Quantum Series Uses It

**QM Vol. I, Ch. 3 (The Wave Function):** ψ(x,t) is intrinsically complex — there is no real-valued wave function that works. The time-dependent factor e^{−iEt/ℏ} is a rotating phasor; its modulus is 1, so |ψ|² = |ψ_spatial|². The Born rule extracts probability from |ψ|², which requires knowing how to take the modulus of a complex number. Students must understand that ψ itself is not a probability, that Im(ψ) is not a fiction, and that the phase of ψ (though locally unobservable for a single state) is physically real in interference.

**QM Vol. I, Ch. 8 (Wave Packets):** A wave packet is a superposition Σ φ(k) e^{i(kx−ωt)} dk. Each term is a complex exponential with wave number k and angular frequency ω(k). The envelope (group velocity) emerges from the interference of nearby k-values — a Fourier argument that lives entirely in complex-exponential language. Phase velocity vs. group velocity is a direct consequence of the behavior of e^{iφ} as φ changes.

**QM Vol. II, Ch. 7 (Spin):** Spinors are two-component complex vectors. The phase factor e^{iφ/2} appears in rotation operators for spin-½, and e^{iφ/2} ≠ e^{i(φ+2π)/2}: a 2π rotation of a spin-½ particle introduces a factor of −1. The modulus-argument decomposition of complex numbers is the language in which this is stated and understood.

---

## C. Connections

**Earlier math modules this needs:**
- M-04 (Series Expansions): Euler's formula is proved by substituting into power series. A student who has seen M-04 can reconstruct the proof; without it, Euler's formula must be accepted on trust.

**QM chapters this unlocks:**
- All of QM Vol. I from Ch. 3 onward (ψ is complex throughout).
- Vol. I Ch. 8 (wave packets, Fourier superposition of complex exponentials).
- Vol. II Ch. 7 (spin, spinor phases, SU(2) rotation operators).
- Vol. II Ch. 4 (time evolution operator e^{−iĤt/ℏ} as an exponential of an operator — a direct generalization of e^{iθ}).

---

## D. Conventions and Pitfalls

**Physics vs. engineering sign convention:** Physicists write e^{−iωt} for a positive-frequency wave (time factor e^{−iEt/ℏ}); engineers often write e^{+jωt}. The QM series uses e^{−iωt} throughout. A formula copied from an engineering source may have a conjugated phase — check the sign before importing.

**ψ is not the real part of anything:** In classical physics, one complexifies to compute and then takes Re( ) at the end. In QM, ψ is genuinely complex. There is no final "take the real part" step; both real and imaginary parts of ψ are physical. This is the single most important conceptual shift from the classical use of complex numbers.

**Modulus vs. modulus squared:** The probability density is |ψ|² = ψ*ψ, not |ψ|. Forgetting the square is a persistent arithmetic error. Normalization is ∫|ψ|² dx = 1, not ∫|ψ| dx = 1.

**Argument is defined modulo 2π:** The argument of a complex number is not unique; arg(z) and arg(z) + 2π describe the same number. In spin physics, the 2π ambiguity in the argument of e^{iφ} is physically meaningful (spin-½ picks up a sign under 2π rotation), so one must be careful about which branch of the argument is being used.

**Phase of ψ is locally unobservable but globally consequential:** The overall phase of a state e^{iφ}|ψ⟩ is unobservable. Relative phases between components of a superposition are observable (they produce interference). Students often conflate these and conclude "phase doesn't matter" — exactly wrong for interference and for the Aharonov-Bohm effect.

---

## E. Teaching Considerations

**The classical bait-and-switch:** Students arrive knowing the classical trick — complexify, compute, take Re( ) — and apply it to ψ. This produces the wrong physics immediately (they try to write ψ_real = Re(ψ_complex) and lose normalization and interference terms). The framing that helps: "In classical oscillations, complex exponentials are a computational convenience; in QM, ψ is *required* to be complex because the Schrödinger equation has an i in it. The complex exponential is not a shortcut here — it is the physics."

**The phase as a clock:** Framing e^{−iEt/ℏ} as a clock hand rotating in the complex plane at rate E/ℏ helps students see why stationary states have time-independent probabilities (|e^{−iEt/ℏ}|² = 1) while superpositions do not (different clock rates → beating). This makes Ch. I·3 and Ch. I·8 much more intuitive.

**Modulus: the "length" of a complex number:** Students who see |ψ|² for the first time often mistake it for an absolute value sign. Emphasizing that |z| = √(z*z) is the length of the arrow in the complex plane — and that length² = z*z — makes |ψ|² feel geometrically natural rather than mysterious.

**Polar form before Euler:** Experience shows students who are comfortable with re^{iθ} as "a vector of length r at angle θ" absorb Euler's formula much faster than those who encounter it cold as an algebraic identity.

---

## F. Source File Used

`_lib_mfp1-12-complex-numbers-and-exponentials.md`

Source chapter coverage: complex arithmetic from i² = −1; the complex plane and polar form; Euler's formula derived from Maclaurin series; oscillation as Re( ) of a complex exponential; complex amplitudes (phasors); the underdamped oscillator as one complex exponent. Three worked examples: Bombelli's cubic (historical motivation), phasor addition, underdamped oscillator.

Source chapter does NOT cover: operator exponentials (e^{iĤt/ℏ}); spinors; the distinction between classical "take the real part" and QM's intrinsically complex ψ. These are M-16-style additions needed for the QM context.

---

## G. Gaps and Flags

- Source chapter is strong and self-contained for classical/oscillation use. The QM-specific content (ψ intrinsically complex, phase conventions, spinors) requires M-16-style additions in Section B and D of the module — the source does not provide this material.
- Euler's formula derivation assumes familiarity with Maclaurin series (M-04). The source notes this dependency explicitly ("borrowed from Chapter 13"). If M-04 is not used, the derivation needs to be accepted as given.
- The source uses the physicist's sign convention e^{iθ} = cos θ + i sin θ throughout; no cross-reference to engineering convention. The QM module should flag the e^{−iωt} vs. e^{+jωt} issue explicitly (Section D above is original M-16 material).
- No flag on thinness: source chapter is well-developed. The classical-to-QM conceptual shift in Sections D–E requires original authoring not present in the source.
