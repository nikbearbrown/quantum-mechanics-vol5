# Research Notes: Module M-05 — Fourier Series and the Wave Equation

**Optional companion module.** Refresher for QM chapters: I·5 (the infinite square well and superposition of energy eigenstates), III·10 (periodic potentials and Bloch's theorem)
**Condensed from:** _lib_mfp1-14-partial-derivatives-wave-equation-and-fourier.md
**Generated:** 2026-06-03

---

## A. The Tool — Key Results a QM Student Needs

### Functions of two variables and partial derivatives

A function y(x,t) of two variables has two distinct rates of change. The **partial derivative** ∂y/∂x holds t fixed and differentiates in x; ∂y/∂t holds x fixed and differentiates in t. The symbol ∂ (curly d) marks the held variable. The two partial derivatives measure physically different things — spatial slope vs. temporal rate of change — and must not be conflated.

For a sinusoidal wave y = A sin(kx − ωt):
- ∂y/∂x = Ak cos(kx − ωt)  — slope of the snapshot
- ∂y/∂t = −Aω cos(kx − ωt) — transverse velocity of one point
- ∂²y/∂x² = −Ak² sin(kx − ωt)
- ∂²y/∂t² = −Aω² sin(kx − ωt)

### The wave equation

The one-dimensional wave equation:

**∂²y/∂t² = v² ∂²y/∂x²**

where v is the wave speed. It couples the curvature of the spatial profile (∂²y/∂x²) to the temporal acceleration (∂²y/∂t²): where the string is most curved, it accelerates most strongly back toward equilibrium.

The equation is **linear**: if y₁ and y₂ both satisfy it, so does c₁y₁ + c₂y₂. This linearity is what permits superposition — adding solutions gives a solution.

### Separation of variables: standing waves

Look for solutions of the wave equation of the form y(x,t) = X(x)T(t) (separated). Substituting:

X(x) T''(t) = v² X''(x) T(t)   →   T''(t)/T(t) = v² X''(x)/X(x) = −ω² (a constant)

This forces two ODEs:
- X'' = −(ω/v)² X = −k² X,  with k = ω/v
- T'' = −ω² T

Both are the harmonic-oscillator ODE from M-03. Solutions:
- X(x) = A sin(kx) + B cos(kx)
- T(t) = C sin(ωt) + D cos(ωt)

Imposing boundary conditions (e.g., fixed endpoints: y = 0 at x = 0 and x = L):
- y(0,t) = 0 → B = 0
- y(L,t) = 0 → sin(kL) = 0 → k_n = nπ/L, n = 1, 2, 3, …

Allowed modes: y_n(x,t) = sin(n πx/L) · (C_n sin(ω_n t) + D_n cos(ω_n t)), where ω_n = v k_n = nπv/L.

These are standing waves: spatial pattern sin(nπx/L) oscillates in time, but the pattern does not travel. Nodes (points where sin = 0) are fixed in space.

### Fourier series: expanding in the eigenfunctions

By **superposition** (linearity), the general solution is a sum over all allowed modes:

y(x,t) = Σ_{n=1}^{∞} sin(nπx/L) · [C_n sin(ω_n t) + D_n cos(ω_n t)]

At t = 0: y(x,0) = Σ_{n=1}^{∞} D_n sin(nπx/L). This expresses the initial shape as a sum of sine functions — a **Fourier sine series**. The coefficients D_n are found by exploiting orthogonality of the sine functions:

∫_0^L sin(nπx/L) sin(mπx/L) dx = (L/2) δ_{nm}

Therefore: **D_n = (2/L) ∫_0^L y(x,0) sin(nπx/L) dx**

The formula for the Fourier coefficients is an inner product of the initial function with the n-th mode, using the orthogonality of the basis functions. This is the fundamental pattern: expand in a set of orthogonal functions, project onto each one to find the coefficient.

General Fourier series for a function of period T (fundamental angular frequency ω₀ = 2π/T):

y(t) = a₀/2 + Σ_{n=1}^{∞} [a_n cos(nω₀t) + b_n sin(nω₀t)]

where a_n = (2/T) ∫_0^T y(t) cos(nω₀t) dt and b_n = (2/T) ∫_0^T y(t) sin(nω₀t) dt.

Any periodic function — even one with corners or jumps — can be represented this way (Fourier's theorem, 1822). The Gibbs phenomenon (persistent small overshoot near a jump discontinuity, ≈ 9% of the jump, not decreasing as more terms are added) is the only exception to the "smooth convergence" intuition.

### Worked example: square-well state expansion

A particle in an infinite square well (0 to L) is prepared in the state ψ(x,0) = N·x(L−x) (a parabolic bump, zero at the walls). Expand in energy eigenstates ψ_n(x) = √(2/L) sin(nπx/L):

c_n = ∫_0^L ψ_n*(x) ψ(x,0) dx = N √(2/L) ∫_0^L sin(nπx/L) · x(L−x) dx

The integral is nonzero only for odd n (the integrand is an even function about L/2 for odd n, odd for even n). This is a direct Fourier coefficient calculation. After normalization, the state is a superposition c_1 ψ_1 + c_3 ψ_3 + c_5 ψ_5 + ···, with time evolution c_n(t) = c_n e^{−iE_n t/ℏ}. The Fourier decomposition determines both the measurement probabilities (|c_n|² = probability of measuring E_n) and the subsequent time evolution.

---

## B. Where the Quantum Series Uses It

**QM Vol. I, Ch. 5 (The Infinite Square Well):** Energy eigenstates are ψ_n(x) = √(2/L) sin(nπx/L) — exactly the standing-wave modes of a string fixed at both ends. An arbitrary initial state ψ(x,0) is expanded as a sum over these eigenstates; the coefficients c_n are found by the Fourier-coefficient formula (an inner product integral). Time evolution proceeds by multiplying each c_n by e^{−iE_n t/ℏ}. The resulting probability distribution |ψ(x,t)|² oscillates: this is quantum beating, and it is a purely Fourier phenomenon (interference between modes at different frequencies ω_n = E_n/ℏ). Students who have not done a Fourier expansion will find the general-solution step opaque.

**QM Vol. III, Ch. 10 (Periodic Potentials and Bloch's Theorem):** A periodic potential V(x + a) = V(x) has the same periodicity as the lattice. The solutions to the TISE in this potential (Bloch states) are of the form ψ_{k}(x) = e^{ikx} u_k(x), where u_k is periodic with the lattice period. This is a consequence of the translation symmetry of a periodic potential — the same mathematical structure as standing waves on a periodic domain. The allowed energies form bands separated by gaps, and the gap structure follows from the Fourier expansion of V(x): the n-th Fourier component of V mixes states with momenta differing by 2nπ/a (Umklapp). Students need to understand that a periodic function is expanded in a discrete Fourier series, and that the Fourier coefficients of V determine which state-pairs are mixed.

---

## C. Connections

**Earlier math modules this needs:**
- M-01 (Complex Numbers): Fourier series can be written compactly as Σ c_n e^{inω₀t} using complex exponentials. The complex form is the one used in QM (Bloch's theorem uses e^{ikx}; time evolution factors use e^{−iEt/ℏ}). Converting between sin/cos form and complex exponential form requires M-01.
- M-03 (ODEs): Separation of variables reduces the wave equation (PDE) to two ODEs; solving the resulting ODEs uses the harmonic-oscillator solution machinery of M-03. The standing-wave calculation is M-03 applied twice.
- M-02 (Probability): The Fourier coefficients |c_n|² give the probability of measuring energy eigenvalue E_n. The completeness relation Σ|c_n|² = 1 is the normalization condition (M-02) expressed in the energy-eigenstate basis.

**QM chapters this unlocks:**
- Vol. I, Ch. 5 (infinite square well with general initial states — the Fourier expansion of ψ in energy eigenstates).
- Vol. III, Ch. 10 (periodic potentials — Bloch's theorem, band structure, Fourier decomposition of a periodic potential).
- The general formalism of eigenstate expansions in QM (any Hilbert space expansion of ψ in an orthonormal basis is a generalized Fourier decomposition — the overlap integral c_n = ⟨ψ_n|ψ⟩ is a Fourier coefficient).
- Vol. I, Ch. 8 (wave packets) and the Fourier transform — a continuous version of the Fourier series (this connects M-05 to the MFP2 Fourier-transform chapter, _lib_mfp2-06).

---

## D. Conventions and Pitfalls

**Normalization of basis functions:** The sine functions sin(nπx/L) are orthogonal but not orthonormal — their norm is √(L/2). The energy eigenstates ψ_n = √(2/L) sin(nπx/L) are orthonormal. When computing Fourier coefficients c_n = ∫ψ_n* ψ dx, students must use the normalized ψ_n. Using the unnormalized sin gives a coefficient that is off by a factor of √(L/2).

**Complex vs. real Fourier series:** In QM, Fourier expansions typically use complex exponentials (c_n = ∫ ψ_n* ψ dx, with ψ_n complex). The real-valued sin/cos form of the Fourier series is a special case that applies when the basis functions are real (e.g., standing-wave modes of an infinite square well). For scattering problems, traveling waves e^{±ikx} are the natural basis — a complex Fourier expansion.

**The Fourier coefficient formula uses the conjugate:** c_n = ∫ ψ_n*(x) ψ(x) dx — note the complex conjugate on ψ_n. Students learning Fourier series from a real-analysis context often see c_n = ∫ f(x) sin(nπx/L) dx without a conjugate (since sin is real). When they move to complex basis functions, the conjugate is essential.

**Completeness vs. orthogonality:** The sine functions are orthogonal: ∫ sin(nπx/L) sin(mπx/L) dx = (L/2) δ_{nm}. Completeness — the claim that any (reasonable) function on [0,L] vanishing at the endpoints can be expanded in this basis — is a deeper theorem. Students sometimes assume completeness is obvious; it is not, and the completeness of the energy eigenstates of a given Hamiltonian must be established (or quoted) separately for each problem.

**Gibbs phenomenon:** When a function has a jump discontinuity, the Fourier partial sums overshoot the jump by about 9% no matter how many terms are included. The oscillations narrow but the peak overshoot persists. This matters in periodic-potential problems where the potential V(x) has sharp steps — the Fourier expansion of V converges everywhere except at the step, and the convergence is slow (coefficients fall as 1/n for a step function). Students should not expect the Fourier series of a square wave to converge uniformly.

**Separation of variables: when it works.** Separation of variables (looking for solutions of the form X(x)T(t)) works for the wave equation because the equation is linear and the boundary conditions are homogeneous (zero at the walls). It does NOT work when the boundary conditions are inhomogeneous, or when the PDE has variable coefficients that do not factor. In QM, separation of variables works for the Schrödinger equation for stationary states (time-independent Hamiltonian) and for 3D potentials with the right symmetry (central potentials separate in spherical coordinates). Students should recognize the conditions, not apply separation blindly.

---

## E. Teaching Considerations

**The Fourier expansion of ψ is the QM version of Fourier series:** The hardest conceptual move in Vol. I Ch. 5 is not solving the ODE for ψ_n — it is understanding that an arbitrary initial state ψ(x,0) is expanded in the basis {ψ_n}, and that the coefficients c_n carry all the information about measurement outcomes and time evolution. Making this explicit — "this is exactly the Fourier series you have seen before, with sin(nπx/L)/√(L/2) replacing sin(nπx/L)" — anchors the QM machinery to something familiar.

**Orthogonality is the key to finding the coefficients:** The Fourier coefficient formula c_n = ∫ψ_n* ψ dx is not a definition to memorize — it follows from multiplying ψ = Σ c_m ψ_m by ψ_n* and integrating, using ∫ψ_n* ψ_m dx = δ_{nm}. Deriving the formula this way (one line of algebra) shows that it is a consequence of orthogonality, not a separate piece of machinery.

**Standing waves as the energy eigenstates of the square well:** The physical picture (standing waves) and the mathematical picture (energy eigenstates) should be reconciled explicitly. A standing wave is a separable solution X(x)T(t); the spatial factor X(x) is the energy eigenstate; the temporal factor T(t) = e^{−iE_n t/ℏ} gives the time dependence. The "beat" between two modes with different E_n values produces an oscillating probability density — this is quantum interference in real time, and it is a Fourier phenomenon.

**Bloch's theorem as a Fourier fact:** For a student who understands that a periodic function is expanded in discrete Fourier modes, Bloch's theorem (ψ_{k}(x) = e^{ikx} u_k(x) with u_k periodic) is a restatement of the fact that the eigenstates of a periodic Hamiltonian are labeled by a continuous index k (the crystal momentum) and that u_k can be expanded in the Fourier modes of the lattice. Presenting it this way connects Vol. III Ch. 10 to the Fourier series framework rather than making it appear as a new theorem requiring separate motivation.

**Separation of variables as "reduce a PDE to ODEs."** This framing — rather than "find a product solution" — emphasizes the purpose: we cannot solve a PDE directly, so we look for solutions that factor, which converts the PDE into ODEs we can handle with M-03 methods. The boundary conditions then restrict the allowed solutions to a discrete set (quantization in the square well; allowed k values in a periodic potential). Framing it as a reduction strategy demystifies the method.

---

## F. Source File Used

`_lib_mfp1-14-partial-derivatives-wave-equation-and-fourier.md`

Source chapter coverage: functions of two variables; partial derivatives (physical meaning: slope vs. transverse velocity); derivation of the wave equation from Newton's second law on a string element; d'Alembert's traveling-wave solution f(x−vt) + g(x+vt); superposition and standing waves (adding right- and left-movers, node/antinode structure, allowed frequencies f_n = nv/2L); Fourier series statement (any periodic function as a sum of sinusoids); square-wave Fourier series (odd harmonics, Gibbs phenomenon); decibel as a logarithm (coda, not needed for QM modules). Three worked examples: reading a wave function with partial derivatives; harmonics of a guitar string; building a tone from harmonics.

Source chapter does NOT cover: quantum wave functions, energy eigenstates, Bloch's theorem, the complex Fourier expansion, the Fourier coefficient formula derived from orthogonality, or the orthonormality of quantum mechanical basis functions. These require M-16-style original authoring.

---

## G. Gaps and Flags

- Source chapter covers the wave-equation/Fourier-series material solidly at the introductory level. The QM-specific applications (energy eigenstate expansion, Bloch's theorem) require substantial M-16 original material in Sections B and D.
- The complex Fourier series (c_n = (1/T) ∫ f(t) e^{−inω₀t} dt) is not discussed in the source — only the real sin/cos form. The complex form is needed for QM. Flag: a short M-16 addition showing the equivalence via Euler's formula (M-01) is needed.
- The Fourier transform (the continuous limit of the Fourier series, needed for wave packets in Vol. I Ch. 8) is not covered in this source chapter. The source says explicitly that the Fourier transform belongs to Volume 2 (_lib_mfp2-06). For completeness, the module should note that M-05 covers the series (discrete, periodic functions) and that the transform (continuous, aperiodic functions) is a separate module.
- Separation of variables is presented in the source through the standing-wave derivation, but not named or summarized as a general technique. The module should make the "reduction of PDE to ODE" step explicit, since it is the method students will encounter again in the hydrogen atom (spherical coordinates) and the 3D harmonic oscillator.
- The decibel coda in the source is irrelevant to QM. Omit.
- No thinness flag: source material is adequate for the wave-equation and Fourier-series topics. The QM connections require original material.
