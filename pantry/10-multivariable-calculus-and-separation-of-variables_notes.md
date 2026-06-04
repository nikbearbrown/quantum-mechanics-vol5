# Research Notes: Module M-10 — Multivariable Calculus and Separation of Variables

**Optional companion module.** Refresher for QM chapters: II·5 (3D Schrödinger equation), II·9 (hydrogen atom)
**Condensed from:** `_lib_mfp2-02-multivariable-calculus-and-partial-derivatives.md` and `_lib_mfp2-07-special-functions-and-separation-of-variables.md`
**Generated:** 2026-06-03

---

## A. The tool (key results condensed; the formulas that matter; a worked example)

### A1. Partial derivatives and the constraint subscript

The partial derivative of f(x,y) with respect to x:

$$\left(\frac{\partial f}{\partial x}\right)_y = \lim_{h\to 0}\frac{f(x+h,y)-f(x,y)}{h}$$

The subscript notation — holding one variable fixed — is critical. In physics it is never optional. ∂f/∂x and ∂f/∂y measure the slope along one cross-section of the surface z = f(x,y); the total differential combines both:

$$df = \left(\frac{\partial f}{\partial x}\right)_y dx + \left(\frac{\partial f}{\partial y}\right)_x dy$$

**Equality of mixed partials (Clairaut/Schwarz):** For a smooth function, the order of differentiation does not matter:

$$\frac{\partial^2 f}{\partial y\,\partial x} = \frac{\partial^2 f}{\partial x\,\partial y}$$

This is the exactness test and also the theorem behind every Maxwell relation in thermodynamics — but here the QM version matters: the Schrödinger equation is a PDE whose Laplacian exploits the symmetry of mixed partials via the spherical coordinate form.

### A2. The gradient and Laplacian

In Cartesian coordinates:

$$\nabla f = \frac{\partial f}{\partial x}\hat x + \frac{\partial f}{\partial y}\hat y + \frac{\partial f}{\partial z}\hat z$$

$$\nabla^2 f = \frac{\partial^2 f}{\partial x^2} + \frac{\partial^2 f}{\partial y^2} + \frac{\partial^2 f}{\partial z^2}$$

In spherical coordinates (r, θ, φ) — the form QM students must read fluently:

$$\nabla^2 = \frac{1}{r^2}\frac{\partial}{\partial r}\!\left(r^2\frac{\partial}{\partial r}\right) + \frac{1}{r^2\sin\theta}\frac{\partial}{\partial\theta}\!\left(\sin\theta\frac{\partial}{\partial\theta}\right) + \frac{1}{r^2\sin^2\theta}\frac{\partial^2}{\partial\phi^2}$$

The three-dimensional time-independent Schrödinger equation is:

$$-\frac{\hbar^2}{2m}\nabla^2\psi + V\psi = E\psi$$

This is a PDE. Solving it by hand requires separating it into ODEs. That requires the Laplacian in the coordinate system where the potential is simple — spherical coordinates for central potentials.

### A3. Separation of variables — the method in four steps

Illustrated on Laplace's equation in Cartesian coordinates (∇²Φ = 0), then immediately extended to Schrödinger.

**Step 1 — Product ansatz.** Assume Φ(x,y,z) = X(x)Y(y)Z(z). Substituting and dividing by XYZ:

$$\frac{X''}{X} + \frac{Y''}{Y} + \frac{Z''}{Z} = 0$$

**Step 2 — Separation argument.** Each term depends on one variable only; since together they sum to zero, each must independently equal a constant:

$$\frac{X''}{X} = -k_x^2, \quad \frac{Y''}{Y} = -k_y^2, \quad \frac{Z''}{Z} = -k_z^2, \quad k_x^2 + k_y^2 + k_z^2 = 0$$

The sign of the separation constant controls whether solutions oscillate (negative → sines/cosines) or grow/decay (positive → exponentials). Getting this wrong is the most common error.

**Step 3 — Boundary conditions quantize.** Imposing Φ = 0 at x = 0 and x = L forces k_x = nπ/L for integer n. The discrete energy levels of a particle in a box arise this way.

**Step 4 — Superposition restores generality.** Any sum of product solutions is also a solution (linearity). The general solution is built by summing over all allowed separation constants.

### A4. Separation in spherical coordinates for a central potential

For ψ(r,θ,φ) = R(r)Θ(θ)Φ(φ) in a central potential V(r):

**φ-equation:**

$$\frac{d^2\Phi}{d\phi^2} = -m^2\Phi \;\Longrightarrow\; \Phi(\phi) = e^{im\phi}$$

Single-valuedness (Φ(φ+2π) = Φ(φ)) quantizes m to integers. This is why orbital angular momentum quantum number m is an integer — not a postulate, a regularity condition.

**θ-equation (with u = cosθ):**

$$\frac{d}{du}\!\left[(1-u^2)\frac{dP}{du}\right] + \left[\ell(\ell+1) - \frac{m^2}{1-u^2}\right]P = 0$$

Finiteness at the poles (u = ±1) requires ℓ to be a non-negative integer with |m| ≤ ℓ — a second quantization from regularity. Solutions are the associated Legendre functions P_ℓ^m(cosθ).

**Full angular factor:** the spherical harmonic

$$Y_{\ell m}(\theta,\phi) = N_{\ell m}\,P_\ell^m(\cos\theta)\,e^{im\phi}$$

**Radial equation:** the potential enters here. For a free particle it gives Bessel functions; for hydrogen, associated Laguerre polynomials.

The separation constant ℓ(ℓ+1) comes from the angular part and reappears in the radial equation as a centrifugal barrier term ℏ²ℓ(ℓ+1)/(2mr²). The angular quantum numbers (ℓ, m) arise from the angle equations alone — independent of the potential.

### A5. Worked example — separation of the 3D infinite square well

A particle in a cubic box [0,L]³ with V=0 inside. Product ansatz ψ = X(x)Y(y)Z(z). Each factor satisfies X'' = -k²X with boundary conditions X(0)=X(L)=0, giving:

$$X_n(x) = \sin(n_x\pi x/L), \quad k_{n_x} = n_x\pi/L, \quad n_x = 1,2,3,\ldots$$

Identical for Y and Z. Total energy:

$$E_{n_x n_y n_z} = \frac{\hbar^2\pi^2}{2mL^2}(n_x^2 + n_y^2 + n_z^2)$$

Degeneracy: states with the same sum (n_x² + n_y² + n_z²) share the same energy. For example, {(1,1,2), (1,2,1), (2,1,1)} are three distinct states with the same E — the first appearance of degeneracy from spatial symmetry.

---

## B. Where the quantum series uses it (specific QM chapters + how)

**QM II·5 — The 3D Schrödinger Equation:**
- The module is the direct prerequisite. Students need: the Laplacian in Cartesian and spherical coordinates, the product ansatz, the separation into radial and angular ODEs, and the role of the separation constant in producing the centrifugal barrier term. The 3D infinite well (worked example A5 above) is the cleanest entry.
- Key obstacle: students from 1D QM see ψ as a function of one variable. The multivariable chain rule and the concept of "hold θ fixed while differentiating in r" are genuinely new.

**QM II·9 — The Hydrogen Atom:**
- Full spherical separation required. The angular part produces Y_ℓm (independent of the Coulomb potential). The radial equation produces associated Laguerre polynomials and the principal quantum number n from a termination condition.
- The separation constant ℓ(ℓ+1) links the angular and radial equations — students need to see it appear in both places and understand it is the same quantity.
- The quantum numbers (n, ℓ, m) map one-to-one to the three separation steps (radial termination, polar regularity, azimuthal single-valuedness). The module should make this correspondence explicit.

---

## C. Connections

- **M-11 (Special Functions):** the separated ODEs from this module are the defining equations of the special functions. M-10 produces the equations; M-11 solves them. These two modules are sequential — M-10 should come first or be read alongside.
- **M-09 (Operators and Dirac Notation):** the Laplacian is an operator; its eigenfunctions are exactly the separated solutions. ∇²ψ = λψ is an eigenvalue problem in function space — but grasping this abstract view requires first seeing the separation machinery concretely.
- **M-07 / M-08 (Vector Spaces, Eigenvalues):** the spherical harmonics form a complete orthonormal basis on the sphere (by Sturm–Liouville theory). This is the function-space analogue of an orthonormal eigenbasis in ℝⁿ.
- **Source overlap:** mfp2-02 focuses on thermodynamics (exact differentials, Maxwell relations, Legendre transform). Its QM-relevant content is: partial derivative notation with constraint subscripts, total differential, multivariable chain rule, and the conceptual framework for PDEs. The separation-of-variables machinery and spherical coordinates come entirely from mfp2-07. The module should draw primarily from mfp2-07 with mfp2-02 supplying the partial-derivative foundation.

---

## D. Conventions and pitfalls

**Sign of the separation constant.** Written as -k² (negative), the ODE X'' = -k²X has oscillatory solutions (sin, cos). Written as +k², it has exponential solutions (e^{kx}, e^{-kx}). The sign must be chosen so the boundary conditions can be satisfied. Getting this wrong produces a solution that cannot meet the boundary conditions at all.

**Spherical coordinate conventions.** Physics convention: θ is the polar angle from the z-axis (colatitude, range [0,π]); φ is the azimuthal angle (range [0,2π]). Mathematics/engineering texts sometimes swap θ and φ. The QM series uses the physics convention. Check before reading any external reference.

**The constraint subscript is not optional.** ∂f/∂x without a subscript is ambiguous whenever the variables are not independent. In spherical coordinates, r, θ, φ are all independent, so the subscript can be dropped — but whenever a constraint links variables (e.g., a gas with equation of state, or a particle constrained to a surface), the subscript is essential. The mfp2-02 source makes this point with thermodynamics; the QM student needs the same habit.

**Single-valuedness quantizes m, not the equation itself.** The azimuthal ODE Φ'' = -m²Φ allows any complex number m. Integer m is forced by requiring Φ(φ+2π) = Φ(φ). Spin escapes this argument because spin wavefunctions are not functions on the sphere — they are components of a spinor that transforms under SU(2), not SO(3). Half-integer spin is allowed precisely because the single-valuedness argument does not apply.

**The angular part does not see the potential.** The Y_ℓm are the same for any central potential. Explicitly: the separation of ∇²ψ yields an angular equation that contains no V(r). This means the angular functions for hydrogen, the 3D harmonic oscillator, and the free particle are all spherical harmonics with the same eigenvalue ℓ(ℓ+1) — what differs is the radial equation and its solutions.

**Termination vs. regularity.** Two types of boundary/regularity conditions arise: (1) termination of a power series (Hermite, Laguerre) — requires the series to be a polynomial so the wavefunction is normalizable; (2) finiteness at a singular point of the ODE (Legendre at u=±1, Bessel at ρ=0). Both produce discrete eigenvalues, but for different structural reasons. Students often conflate them.

---

## E. Teaching considerations

**The mfp2-02 source is not the right primary source for this module.** Its development is framed around thermodynamics: exact differentials, Maxwell relations, Legendre transforms. These are not QM content. What is useful from mfp2-02: (a) partial derivative notation with the constraint subscript, (b) total differential, (c) multivariable chain rule. These should be lifted and re-framed around the Schrödinger PDE, not the first law of thermodynamics. The module will need explicit re-anchoring.

**The Laplacian in spherical coordinates should be given, not derived.** The derivation (via the metric tensor or Jacobian) is a two-page calculation that the QM student does not need. Give the form and show how it separates; explain that the three terms correspond to radial, polar, and azimuthal motion.

**The best entry hook:** write down the 3D Schrödinger equation and ask why it is harder than the 1D version. The answer is "it's a PDE, not an ODE, and a PDE couples all coordinates." Then separation is the tool that decouples them — not magic, but a consequence of linearity and the product structure of the equation.

**Pedagogical sequence within the module:**
1. Partial derivatives and the Laplacian (brief — assume from prior QM modules)
2. Cartesian separation on the infinite 3D box (clean worked example)
3. Spherical coordinates — just the Laplacian form and the separation argument
4. The angular equation and Y_ℓm (name the result; M-11 derives it fully)
5. The central-force split: what the radial equation looks like for H atom
6. Quantum numbers from separation constants — the main payoff

**Common student errors documented in research (from mfp2-07 sources):**
- Wrong sign of separation constant (oscillatory vs. exponential mixup)
- Thinking the angular solution depends on the potential
- Forgetting that "finiteness at the poles" is what forces integer ℓ

---

## F. Source file used

Primary for separation and spherical content:
`/Users/bear/Documents/CoWork/bear-textbooks/books/quantum-mechanics-vol5/pantry/_lib_mfp2-07-special-functions-and-separation-of-variables.md`

Primary for partial derivative foundations:
`/Users/bear/Documents/CoWork/bear-textbooks/books/quantum-mechanics-vol5/pantry/_lib_mfp2-02-multivariable-calculus-and-partial-derivatives.md`

---

## G. Gaps and flags

**FLAG — mfp2-02 is thermodynamics, not QM math.** The source chapter is written entirely around thermodynamics (exact/inexact differentials, Maxwell relations, Legendre transforms, heat capacities). The QM-relevant content — partial derivatives, Laplacian, multivariable chain rule — occupies only the first third of the chapter and is covered at an introductory level. Separation of variables is not covered in mfp2-02 at all. For this module, mfp2-07 is the dominant source; mfp2-02 contributes the partial-derivative notation section only.

**FLAG — spherical coordinate Laplacian derivation absent from sources.** Neither source derives the spherical Laplacian from the Cartesian form. The module will need to either (a) give it without derivation (recommended), (b) cite an external derivation, or (c) derive it via the Jacobian (not recommended for this level). Option (a) is appropriate for a refresher module.

**FLAG — the radial hydrogen equation is only sketched.** mfp2-07 names the associated Laguerre equation and states the energy quantization result (E_n = -13.6 eV/n²) but does not derive the radial solution in detail. The derivation belongs to M-11. M-10 should bring the student to the point where the radial equation is written down and its structure is understood; M-11 finishes it. The module boundary should be clearly marked.

**GAP — cylindrical coordinates not covered.** The sources do not develop the Laplacian in cylindrical coordinates or Bessel functions (the cylindrical analogue of the spherical separation). This is relevant for QM problems with cylindrical symmetry (2D confinement, quantum wires) but is not in the stated QM chapter refs (II·5, II·9). Leave it out of this module; it is covered in M-11 under Bessel functions.
