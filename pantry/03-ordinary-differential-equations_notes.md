# Research Notes: Module M-03 — Ordinary Differential Equations

**Optional companion module.** Refresher for QM chapters: I·4–I·7 (time-independent Schrödinger equation; infinite and finite square wells; harmonic oscillator), III·5 (WKB and turning points)
**Condensed from:** _lib_mfp1-11-differential-equations-and-oscillatory-motion.md
**Generated:** 2026-06-03

---

## A. The Tool — Key Results a QM Student Needs

### What an ODE is

A differential equation for a function u(x) is an equation involving u and its derivatives. Its solution is a function (or a family of functions), not a number. For a second-order ODE, two constants of integration appear; they are fixed by two boundary or initial conditions.

**The order** of the equation equals the highest derivative present. Newton's second law is second order because acceleration is d²x/dt². The time-independent Schrödinger equation (TISE) is second order in x.

**Verification by substitution:** any proposed solution can be checked by plugging it back in and differentiating. This turns "guessing an exponential" from speculation into a checkable claim.

### Linear second-order constant-coefficient ODEs

The central form: u'' + p u' + q u = 0 (or with a constant right-hand side for driven equations). These are called *linear* because every term is degree-one in u or its derivatives — no u², no (u')³. Linearity buys superposition: if u₁ and u₂ are both solutions, so is Au₁ + Bu₂.

**Characteristic equation method (Euler, 1740s):** Substitute the trial solution u = e^{rx}. Then u' = re^{rx}, u'' = r²e^{rx}. Dividing out the never-zero e^{rx} converts the ODE into a polynomial in r — the characteristic equation. For a second-order equation the polynomial is quadratic; solve for r.

**Three cases (depending on the discriminant):**

1. **Two distinct real roots r₁, r₂:** General solution u = Ae^{r₁x} + Be^{r₂x}. Physical case: exponential growth and/or decay.

2. **Complex conjugate roots r = α ± iβ:** General solution u = e^{αx}(A cos βx + B sin βx). Physical case: oscillation with possible growth/decay envelope. For α = 0 (purely imaginary roots r = ±iβ), u = A cos βx + B sin βx — pure oscillation, the SHO.

3. **Repeated real root r₀:** General solution u = (A + Bx)e^{r₀x}. Appears in the critically damped oscillator; less common in QM.

### The harmonic oscillator equation

u'' = −k²u (with k² > 0) is the universal form. Its characteristic equation r² = −k² has purely imaginary roots r = ±ik, giving:

**General solution: u(x) = A cos(kx) + B sin(kx),  or equivalently  u(x) = Ce^{ikx} + De^{−ikx}**

These are the same two-dimensional solution space expressed in two different bases. In QM both forms appear: the trigonometric basis is natural inside a well; the exponential basis is natural for scattering states and in regions where the solution decays (k → iκ gives real exponentials e^{±κx}).

The exponential form u'' = +κ²u (positive right-hand side, κ² > 0) has real roots r = ±κ, giving:

**General solution: u(x) = Ae^{κx} + Be^{−κx}**

This is the form inside a classically forbidden region (E < V), where the solution is exponentially growing or decaying. Normalizability (requiring ψ → 0 at ±∞) kills one of the two constants in each forbidden region.

### Boundary conditions and eigenvalue problems

For the TISE on a finite domain, the solution must satisfy boundary conditions at the endpoints (or at ±∞). Imposing these conditions on a general solution typically forces the two free constants and — crucially — restricts the parameter appearing in the ODE (which is the energy E in QM) to a discrete set of allowed values. This is an **eigenvalue problem**: only certain values of the parameter (eigenvalues, i.e., allowed energies) permit a non-trivial solution satisfying all the boundary conditions.

The standard example: particle in an infinite square well of width L. The TISE in the interior is ψ'' = −k²ψ with k² = 2mE/ℏ². General solution: ψ = A sin(kx) + B cos(kx). Boundary conditions ψ(0) = 0 and ψ(L) = 0 force B = 0 and sin(kL) = 0, so kL = nπ, giving quantized energies E_n = n²π²ℏ²/(2mL²). The boundary conditions, not the ODE itself, produce quantization.

### Worked example: setting up and solving a square-well interior

TISE for 0 < x < L with V = 0: −(ℏ²/2m) ψ'' = Eψ, i.e., ψ'' = −(2mE/ℏ²)ψ = −k²ψ.
Characteristic equation: r² + k² = 0, roots r = ±ik.
General solution: ψ(x) = A sin(kx) + B cos(kx).
BC at x = 0: ψ(0) = B = 0.
BC at x = L: ψ(L) = A sin(kL) = 0. For A ≠ 0: kL = nπ, n = 1, 2, 3, …
Allowed energies: E_n = ℏ²k_n²/(2m) = n²π²ℏ²/(2mL²). QED.

---

## B. Where the Quantum Series Uses It

**QM Vol. I, Ch. 4 (Time-Independent Schrödinger Equation):** The TISE −(ℏ²/2m)ψ'' + V(x)ψ = Eψ is a second-order linear ODE in x (for 1D problems). Solving it for given V(x) requires recognizing the form (harmonic-oscillator-type vs. exponential-type depending on sign of E − V), writing the general solution, applying boundary conditions, and extracting the allowed energies. This is the characteristic-equation method applied to a physics problem.

**QM Vol. I, Ch. 5 (The Infinite Square Well):** Exactly the worked example above. The quantization of energy emerges entirely from the ODE + boundary conditions machinery.

**QM Vol. I, Ch. 6 (The Quantum Harmonic Oscillator):** The TISE for the QHO is ψ'' = (mω/ℏ)²(x² − 2E/ℏω)ψ. This is not a constant-coefficient ODE (the coefficient of ψ depends on x), so the characteristic-equation method does not apply directly. Instead, one uses asymptotic analysis (ψ → e^{−mωx²/2ℏ} for large x, which IS a constant-coefficient-type argument in the asymptotic limit), then a power-series substitution (Hermite polynomial recursion). The ODE toolkit from this module provides the foundation; the full QHO treatment extends it.

**QM Vol. I, Ch. 7 (The Free Particle / Finite Square Well):** The finite well has three regions: interior (oscillatory, k² > 0) and exterior (decaying, κ² > 0). Students must write the appropriate general solution in each region and then match ψ and ψ' at the interfaces — a boundary-matching calculation that requires fluency with both the sin/cos and the e^{±κx} solution forms.

**QM Vol. III, Ch. 5 (WKB Approximation):** WKB treats the TISE locally as a constant-coefficient ODE in each small region, with the local wave number k(x) = √(2m(E−V(x)))/ℏ varying slowly. The oscillatory and exponential solution families are the zeroth-order WKB approximations in classically allowed and forbidden regions respectively. Connection formulas at turning points (where k → 0) require knowing how the two solution families interpolate. The entire WKB argument rests on the constant-coefficient-ODE picture applied patchwork.

---

## C. Connections

**Earlier math modules this needs:**
- M-01 (Complex Numbers): The complex roots of the characteristic equation, and the passage between e^{±ikx} and sin/cos, require comfort with complex exponentials and Euler's formula.
- M-04 (Series Expansions): The QHO solution and some irregular potentials require power-series (Frobenius) solution methods — these extend the constant-coefficient technique and use the series machinery of M-04.

**QM chapters this unlocks:**
- Vol. I, Ch. 4–7 (the core 1D QM chapters — wells, barriers, the oscillator).
- Vol. III, Ch. 5 (WKB).
- Any eigenvalue problem in the series where the Hamiltonian leads to a 1D ODE (e.g., the radial equation for hydrogen, which is a 1D ODE in r after separation of variables in 3D).

---

## D. Conventions and Pitfalls

**Sign of the second derivative term:** In different QM texts the TISE is written as ψ'' = −k²ψ (oscillatory) or ψ'' = +κ²ψ (exponential). Students get tangled because the sign of E − V determines which form applies. A reliable rule: if E > V (classically allowed), the solution oscillates; if E < V (classically forbidden), the solution is real exponential. The switch in sign is the switch between these two regimes.

**Arbitrary constants and normalization:** The ODE solution has two free constants. One is often fixed by a boundary condition (e.g., ψ = 0 at a wall); the other is fixed by normalization. Students sometimes confuse these two separate steps and try to normalize before applying the boundary condition, or miss that normalization is a separate constraint on top of the ODE.

**Continuity conditions at interfaces:** At a step in V (finite well walls, etc.), ψ and ψ' must both be continuous (assuming the potential step is finite). Students often remember to match ψ but forget ψ'. Both conditions are needed; they together produce the transcendental equation for the allowed energies.

**The Wronskian and linear independence:** The two solutions of a second-order ODE are linearly independent if their Wronskian W = u₁u₂' − u₂u₁' ≠ 0. For sin(kx) and cos(kx), W = k ≠ 0. For e^{κx} and e^{−κx}, W = −2κ ≠ 0. This is why both are in the general solution. Students sometimes throw away the growing exponential for normalizability reasons before reaching the boundary (which is correct in unbounded regions) but then try to apply it inside a finite well where the boundary is at a finite distance (incorrect — both solutions are needed inside the well).

**Quantization comes from boundary conditions, not the ODE:** The ODE itself is satisfied by a continuous range of k values. Only after imposing the physical boundary conditions (ψ = 0 at infinite walls, or ψ → 0 at x → ±∞, or matching conditions at interfaces) does the discrete spectrum emerge. This is the conceptual core of quantization in the ODE picture.

---

## E. Teaching Considerations

**The characteristic equation trick is the payoff:** Most students have "solved" differential equations by memorization ("the spring solution is A cos ωt + B sin ωt"). Showing that this falls out of the characteristic-equation method — substitute e^{rx}, divide out the exponential, solve the resulting polynomial — converts a memorized formula into a derived result. After that, the e^{±κx} solution for classically forbidden regions requires no new trick; it is just the same method with a different sign of k².

**Two forms for oscillatory solutions — both useful:** The sin/cos form is natural when the boundary conditions are at specific points (ψ(0) = 0 forces out the cosine term). The e^{±ikx} form is natural for scattering (traveling waves, reflection/transmission coefficients). Students should be able to switch between them using Euler's formula and should recognize both as the same general solution.

**Eigenvalue problems need a narrative:** "Quantization falls out of boundary conditions" is the key insight, but students often encounter it as a mechanical calculation (impose BC, get transcendental equation, solve numerically) without understanding why the energy is restricted. The framing that helps: "The ODE has solutions for any E, but only certain E values produce a solution that satisfies all the physical requirements (boundary conditions + normalizability). Those E values are the eigenvalues — the allowed energies."

**Matching conditions at interfaces deserve a dedicated drill:** This is the step students most consistently get wrong in finite-well and barrier problems. Running through a two-region matching (inside vs. outside a finite well) step by step — write general solution in each region, list the conditions, count the equations and unknowns, solve — before the first barrier problem saves significant debugging later.

---

## F. Source File Used

`_lib_mfp1-11-differential-equations-and-oscillatory-motion.md`

Source chapter coverage: first-order separable ODEs (exponential decay); second-order linear constant-coefficient ODEs; verification by substitution; characteristic-equation method for the damped oscillator (three regimes); initial vs. boundary conditions; the SHO form u'' = −ω²u and its solution A cos ωt + B sin ωt; structural universality of the SHO form (pendulum, LC circuit, etc.); superposition as the consequence of linearity.

Source chapter does NOT cover: eigenvalue problems explicitly; matching conditions at potential interfaces; non-constant-coefficient ODEs (QHO); the separation between the ODE's general solution and the physical boundary-condition selection of allowed eigenvalues. These are key QM applications that need M-16-style framing in the module.

---

## G. Gaps and Flags

- Source chapter is solid on the constant-coefficient case, which is the right foundation. No thinness flag for the core material.
- The eigenvalue-problem framing (why boundary conditions produce quantization) is not spelled out in the source; it is implicit in the characteristic-equation discussion. Needs M-16 original material in the module — this is the central QM application.
- Non-constant-coefficient ODEs (needed for the QHO and hydrogen atom radial equation) are not covered. Flag: the source gives only the constant-coefficient engine; power-series (Frobenius) solutions are absent. A pointer to the MFP2 special-functions chapter (_lib_mfp2-07-special-functions-and-separation-of-variables.md) is warranted for students who go further.
- The three-regime framework (underdamped/critically damped/overdamped) from the source maps onto the QM framework (oscillatory/evanescent/normalizable turning-point) with a sign flip. Explicitly drawing this analogy in the module would help QM students see that the ODE machinery they are using is the same one they saw in the classical oscillator.
