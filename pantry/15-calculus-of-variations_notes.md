# Research Notes: Module M-15 — Calculus of Variations
**Optional companion module.** Refresher for QM chapters: III·3 (variational principle).
**Condensed from:** `_lib_mfp2-11-calculus-of-variations-and-lagrangian-hamiltonian.md`
**Generated:** 2026-06-03

---

## A. The tool (key results condensed; the formulas that matter; a worked example)

### The core upgrade: functional → variation
- Ordinary calculus: extremize f(x) by setting df/dx = 0 (a point is the unknown)
- Calculus of variations: extremize S[y] = ∫ L(y, y', x) dx by setting δS = 0 (a whole function y(x) is the unknown)
- S[y] is a **functional** — it eats a function and returns a number
- Terminology: "stationary action," not "least action" — the action may be a saddle point, not a minimum

### Setup (the variation)
Neighboring trial path: ȳ(x) = y(x) + ε η(x), where η is arbitrary but vanishes at endpoints:
$$\eta(x_1) = \eta(x_2) = 0$$
The **variation** δS = ε · (d/dε) S[y + εη]|_{ε=0}. Stationarity: δS = 0 for every allowed η.

### Derivation of the Euler–Lagrange equation
Differentiate under the integral, integrate the η' term by parts:
$$\int_{x_1}^{x_2} \frac{\partial L}{\partial y'}\,\eta'\,dx = \underbrace{\left[\frac{\partial L}{\partial y'}\,\eta\right]_{x_1}^{x_2}}_{= 0 \text{ (endpoint condition)}} - \int_{x_1}^{x_2} \frac{d}{dx}\!\left(\frac{\partial L}{\partial y'}\right)\eta\,dx$$
Apply the fundamental lemma (if ∫ f(x)η(x) dx = 0 for all η, then f = 0):
$$\boxed{\frac{d}{dx}\!\left(\frac{\partial L}{\partial y'}\right) - \frac{\partial L}{\partial y} = 0}$$
**Critical point for students**: the boundary term vanishes *because* η(x₁) = η(x₂) = 0. Forgetting this is the single most common error in deriving the EL equation.

### Mechanics: recovering Newton from a Lagrangian
Replace x → t, y → q (generalized coordinate), y' → q̇, and let L = T − V. Hamilton's principle: actual motion makes S stationary. EL equation gives:
$$\frac{d}{dt}\!\left(\frac{\partial L}{\partial \dot{q}}\right) - \frac{\partial L}{\partial q} = 0$$
For 1D particle: L = ½mẋ² − V(x). Then ∂L/∂ẋ = mẋ, d/dt(mẋ) = mẍ, ∂L/∂x = −dV/dx. Result: mẍ = F. Newton's second law emerges.

### Why L = T − V? 
Not derivable within classical mechanics without circularity. Justified by what it produces (Newton's laws). The deep "why" is Feynman's path integral: the classical path emerges as stationary-phase limit of the sum over all paths.

### Generalized coordinates (the real power)
EL equation holds in *any* coordinate system. Constraints handled by choosing coordinates that respect them — no need to compute constraint forces. Example: pendulum in angle θ gives equation of motion directly without computing tension.

### The Hamiltonian (bridge to QM)
Canonical momentum: p ≡ ∂L/∂q̇. Hamiltonian via Legendre transform:
$$H(q,p) = p\dot{q} - L$$
Hamilton's equations:
$$\boxed{\dot{q} = \frac{\partial H}{\partial p}, \qquad \dot{p} = -\frac{\partial H}{\partial q}}$$
For conservative time-independent systems, H = T + V (total energy). Promoting H to operator Ĥ gives Schrödinger equation: Ĥψ = iℏ ∂ψ/∂t. The classical Hamiltonian is the direct parent of the quantum Hamiltonian operator.

### Noether's theorem (symmetry → conservation)
If L does not depend on coordinate q (q is "cyclic"), then ∂L/∂q = 0, and:
$$\frac{d}{dt}\!\left(\frac{\partial L}{\partial \dot{q}}\right) = 0 \implies p = \text{const}$$
- Spatial translation symmetry → linear momentum conserved
- Rotational symmetry → angular momentum conserved
- Time translation symmetry → energy conserved
Conservation laws are shadows of symmetries; Noether's theorem is the lamp.

### Beltrami identity (special case when L has no explicit x dependence)
$$L - y'\frac{\partial L}{\partial y'} = \text{const}$$
Useful shortcut when L = L(y, y') only.

### Worked example: brachistochrone → cycloid
Descent-time functional: T[y] = ∫ √[(1 + y'²)/(2gy)] dx. L has no explicit x → use Beltrami identity → y(1 + y'²) = const. Solution in parametric form:
$$x = R(\phi - \sin\phi), \quad y = R(1 - \cos\phi) \quad \text{(cycloid)}$$

---

## B. Where the quantum series uses it (specific QM chapters + how)

**III·3 — Variational principle**
- The variational method: find ground-state energy by minimizing ⟨ψ|Ĥ|ψ⟩ over a family of trial wavefunctions ψ(r; α) parameterized by α. This is precisely δ⟨H⟩ = 0 — a functional extremization where the functional eats a wavefunction and returns a number (an expectation value).
- The Euler–Lagrange equation is the background machinery: stationarity of ⟨H⟩ with respect to variations in ψ (constrained by ⟨ψ|ψ⟩ = 1) yields the Schrödinger equation itself via functional differentiation.
- Rayleigh–Ritz method: parameterize trial ψ as linear combination of basis functions; the variational condition becomes a matrix eigenvalue problem.
- Hartree–Fock: variational minimization over Slater-determinant trial states — a direct application of the calculus of variations to multi-electron wavefunctions.
- The language "the variational principle states that ⟨H⟩ ≥ E₀" is a consequence of the stationarity argument: the ground state energy is the minimum of the expectation value functional.

---

## C. Connections

- **Schrödinger equation itself**: the time-dependent Schrödinger equation can be derived as the Euler–Lagrange equation of the action S = ∫∫ ψ*(iℏ∂_t − Ĥ)ψ d³r dt, treating ψ* as the dynamical variable. The variational principle is not just a method — it is the generating principle of QM.
- **Path integrals**: Feynman's formulation of QM sums exp(iS/ℏ) over all paths; the classical path is where contributions are stationary (constructive interference). This is the deepest answer to "why does nature extremize the action" and also why L = T − V rather than T + V.
- **Lagrange multipliers / constrained variation**: the normalization constraint ⟨ψ|ψ⟩ = 1 in the variational method is handled by a Lagrange multiplier, which turns out to be the energy eigenvalue. Students need to recognize this connection.
- **Operators and inner products (M linked to mfp2-05)**: the Hilbert space structure and inner product ⟨ψ|Ĥ|ψ⟩ are the setting in which the variational functional lives. The calculus of variations machinery ports directly to infinite-dimensional function spaces once the inner product is in place.

---

## D. Conventions and pitfalls

- **"Least" vs. "stationary" action**: always say "stationary." The principle of stationary action is correct; "least action" is the traditional name but is sometimes literally false (saddle points exist). The QM variational method does give a genuine minimum (⟨H⟩ ≥ E₀), but the underlying principle is stationarity.
- **The boundary term**: η(x₁) = η(x₂) = 0 is mandatory. Without it, surface terms appear and the Euler–Lagrange equation picks up boundary contributions. In QM, natural boundary conditions (ψ → 0 at infinity) play the same role.
- **Why L = T − V**: do not claim it is derived. It is a postulate justified by its output (Newton's laws). The Feynman path-integral explanation is the honest deep answer.
- **Functional derivative notation**: some QM texts write δ⟨H⟩/δψ* = 0 using the functional derivative. This is the variational machinery in Dirac notation. The EL equation is the special case where L has the form it has here.
- **Canonical momentum vs. kinetic momentum**: p = ∂L/∂q̇ is the canonical momentum; in the presence of electromagnetic fields it differs from mv. In QM, p̂ = −iℏ∇ is the canonical momentum. This distinction matters in III·3 when discussing the variational method in the presence of a vector potential.
- **Degrees of freedom**: EL gives one equation per generalized coordinate. For an N-particle system in 3D, there are 3N coordinates and 3N EL equations.

---

## E. Teaching considerations

- **Do the brachistochrone**: not for its physical importance, but because it is the purest functional-extremization problem — the unknown is obviously a whole curve, making the conceptual upgrade from ordinary calculus vivid.
- **Derive the EL equation, don't announce it**: the integration-by-parts argument is at exactly the right level and makes the boundary-term condition feel necessary, not arbitrary.
- **Connect immediately to QM**: after recovering Newton from L = T − V, immediately tell students that the same formalism (promote q → q̂, p → p̂, H → Ĥ) generates quantum mechanics. This is the reason to learn the Hamiltonian.
- **The variational method (III·3) needs the EL equation**: the statement "minimize ⟨H⟩ over trial states" is a functional extremization. Students who do not recognize this cannot follow derivations in the QM chapter. Assign M-15 before III·3.
- **Noether's theorem is optional for III·3 but illuminating**: if III·3 discusses symmetries and conservation laws (it should), Noether's theorem connects the variational apparatus to something students already know (conservation of momentum, energy). Worth a paragraph even if not derived in full.
- **Scope warning**: do not go further into canonical transformations or Hamilton–Jacobi theory. That belongs to the classical mechanics book. This module's job is to hand students the EL equation, the Hamiltonian, and enough Noether to connect symmetry to conservation.

---

## F. Source file used

`/Users/bear/Documents/CoWork/bear-textbooks/books/quantum-mechanics-vol5/pantry/_lib_mfp2-11-calculus-of-variations-and-lagrangian-hamiltonian.md`

Key sections used: §3.1 (functionals and variation), §3.2 (EL equation derivation), §3.3 (Lagrangian and Newton), §3.4 (generalized coordinates), §3.5 (Hamiltonian), §3.6 (Noether), §6 (path integral and field theory connections).

---

## G. Gaps and flags

- **Constrained variation / Lagrange multipliers**: the source chapter does not work through the constrained variation needed for the QM normalization condition. A bridging note is needed for III·3 showing that minimizing ⟨H⟩ subject to ⟨ψ|ψ⟩ = 1 introduces a Lagrange multiplier equal to the energy eigenvalue.
- **Functional derivative formalism**: the source uses δS notation but does not introduce the functional derivative δF/δy(x) explicitly. QM texts sometimes use this notation; a one-paragraph bridge would help.
- **Infinite-dimensional function spaces**: the source works in finite-dimensional generalized coordinates. The extension to wavefunctions (an infinite-dimensional function space) is stated but not shown. Flag for III·3: the EL equation works in Hilbert space because the inner product is well-defined; this is not trivially obvious.
- **Path integral connection**: mentioned in §6 of the source but not developed. If III·3 or later QM chapters use path integrals, a more substantial bridge note is needed.
- **Fermat's principle / Snell's law example**: pedagogically valuable (shows the variational idea outside mechanics) but not directly relevant to III·3. Include in the module for breadth; flag as optional reading.
