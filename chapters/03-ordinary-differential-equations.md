# Module M-03 — Ordinary Differential Equations and Boundary Conditions

**When you need this:** The time-independent Schrödinger equation is a second-order linear ODE; every 1D bound-state and scattering problem in QM Vol. I Chs. 4–7 is solved by the methods here. The WKB approximation of Ch. III·5 rests on the same oscillatory vs. evanescent solution families.

---

## The refresher

### What an ODE is

A differential equation for a function $u(x)$ is an equation relating $u$ to its own derivatives. Its solution is a *function* — a whole curve, not a number — determined up to free constants that are fixed by boundary or initial conditions. A **second-order** ODE contains $u''$ as the highest derivative; the general solution of a second-order ODE has exactly two free constants.

**Verification by substitution:** any proposed solution can be checked by plugging it in and differentiating. "Guessing the exponential" is not speculation — it is a checkable claim.

### Linear, constant-coefficient, second-order ODEs

The central form in QM:

$$u'' + p\,u' + q\,u = 0, \qquad p,q \in \mathbb{R} \text{ (constants)}.$$

This is **linear** because no term is higher than degree one in $u$ or its derivatives. Linearity purchases **superposition**: if $u_1$ and $u_2$ are both solutions, so is $Au_1 + Bu_2$ for any constants $A, B$.

**The characteristic-equation method** (Euler, 1740s): assume $u = e^{rx}$, so $u' = re^{rx}$, $u'' = r^2 e^{rx}$. Substitute, divide by the never-zero $e^{rx}$, and obtain a polynomial in $r$ — the **characteristic equation**. For the second-order equation above: $r^2 + pr + q = 0$. Solve this quadratic; the roots $r_1, r_2$ determine the solution family.

**Three cases by the discriminant $\Delta = p^2 - 4q$:**

| Case | Roots | General solution |
|---|---|---|
| Two distinct real roots ($\Delta > 0$) | $r_1 \neq r_2 \in \mathbb{R}$ | $u = Ae^{r_1 x} + Be^{r_2 x}$ |
| Complex conjugate roots ($\Delta < 0$) | $r = \alpha \pm i\beta$ | $u = e^{\alpha x}(A\cos\beta x + B\sin\beta x)$ |
| Repeated real root ($\Delta = 0$) | $r_0$ (double) | $u = (A + Bx)e^{r_0 x}$ |

### The two solution families relevant to QM

**Oscillatory (classically allowed region, $E > V$).**

$$u'' = -k^2 u, \qquad k^2 > 0.$$

Characteristic equation: $r^2 + k^2 = 0$, roots $r = \pm ik$. General solution in two equivalent bases:

$$u(x) = A\cos(kx) + B\sin(kx) \quad\text{(trigonometric basis)}$$
$$= Ce^{ikx} + De^{-ikx} \quad\text{(exponential basis; } C, D \text{ complex in general)}$$

Both span the same two-dimensional solution space. The trigonometric basis is natural when boundary conditions are at specific points (e.g., $u(0) = 0$ forces out the cosine). The exponential basis is natural for traveling waves and scattering states.

**Evanescent (classically forbidden region, $E < V$).**

$$u'' = +\kappa^2 u, \qquad \kappa^2 > 0.$$

Characteristic equation: $r^2 - \kappa^2 = 0$, roots $r = \pm\kappa$. General solution:

$$u(x) = Ae^{\kappa x} + Be^{-\kappa x}.$$

Both terms are present inside a finite forbidden region. Only at the boundaries $x \to \pm\infty$ does normalizability kill one term: the growing exponential is discarded in a semi-infinite forbidden region.

Note the pattern: the sign of $E - V$ determines which equation applies. This is the same discriminant logic as the three damping regimes of the classical oscillator (see *Mathematics for Physics*, Vol. 1, Ch. 11), with the classical underdamped (oscillatory) and overdamped (real-exponential) regimes mapping onto the quantum allowed and forbidden regions respectively.

### Boundary conditions and the eigenvalue problem

For the time-independent Schrödinger equation (TISE) on a finite domain, imposing boundary conditions on the general solution does two things: (1) it fixes the free constants, and (2) it restricts the parameter $E$ in the equation to a **discrete set of allowed values**. This is the eigenvalue problem.

The logic is:
1. The ODE is satisfied by a continuous family of solutions parametrized by $E$.
2. Physical boundary conditions (e.g., $\psi = 0$ at an infinite wall, or $\psi \to 0$ as $x \to \pm\infty$) are additional constraints.
3. For generic $E$, no solution satisfies all the boundary conditions simultaneously.
4. Only at specific values $E_n$ (the **eigenvalues**) does a non-trivial solution satisfying all the boundary conditions exist.

**Quantization comes from boundary conditions, not from the ODE itself.** The ODE has solutions for any $E$; the boundaries select the allowed $E_n$.

### Matching conditions at potential interfaces

At a finite step in the potential (finite well walls, barrier edges), $\psi(x)$ and $\psi'(x)$ must both be **continuous**. These two matching conditions at each interface, together with the boundary conditions at the edges, constitute a linear system whose non-trivial solution exists only for specific $E$ values. Forgetting to match $\psi'$ (not just $\psi$) is the most common error in finite-well and barrier problems.

If the potential has an infinite jump (infinite square well), only $\psi$ is matched (to zero at the wall); $\psi'$ may be discontinuous there.

### Worked example: infinite square well

The TISE inside the well ($0 < x < L$, $V = 0$):

$$-\frac{\hbar^2}{2m}\psi'' = E\psi \implies \psi'' = -k^2\psi, \quad k^2 = \frac{2mE}{\hbar^2}.$$

Characteristic equation: $r^2 + k^2 = 0$, roots $r = \pm ik$.

General solution: $\psi(x) = A\sin(kx) + B\cos(kx)$.

Boundary condition at $x = 0$: $\psi(0) = B = 0$. So $\psi(x) = A\sin(kx)$.

Boundary condition at $x = L$: $\psi(L) = A\sin(kL) = 0$. For $A \neq 0$: $kL = n\pi$, $n = 1, 2, 3, \ldots$

Allowed wave numbers: $k_n = n\pi/L$.

Allowed energies:

$$\boxed{E_n = \frac{\hbar^2 k_n^2}{2m} = \frac{n^2\pi^2\hbar^2}{2mL^2}.}$$

The constant $A$ is fixed separately by normalization (see M-02), not by the ODE or the boundary conditions.

**Reading the solution:** $n = 1$ is the ground state, $n = 2$ the first excited state, and so on. The energy grows as $n^2$ — a purely quantum result that follows from $k_n = n\pi/L$ and $E \propto k^2$. There is no classical analog; the ODE + boundary-condition structure is doing all the physics.

---

## In the quantum series

### Vol. I, Ch. 4 — The time-independent Schrödinger equation

The TISE

$$-\frac{\hbar^2}{2m}\frac{d^2\psi}{dx^2} + V(x)\psi = E\psi$$

is a second-order linear ODE in $x$ (for any fixed potential $V(x)$). The general strategy — write the TISE in the form $\psi'' = (\ldots)\psi$, identify the sign and magnitude of the coefficient, write the oscillatory or evanescent general solution, apply boundary conditions, extract $E_n$ — is exactly the characteristic-equation method of this module. Ch. I·4 introduces this framework as the universal machine for 1D QM.

### Vol. I, Ch. 5 — The infinite square well

The infinite square well is the worked example above, carried to completion with normalization. The key physical insight — that energy quantization emerges from the boundary conditions $\psi(0) = \psi(L) = 0$, not from any special property of the ODE itself — is the eigenvalue idea of this module. Without this framing, the discreteness of the energy spectrum can appear mysterious; with it, it is the direct consequence of requiring a standing wave to fit an integer number of half-wavelengths into the box.

### Vol. I, Ch. 6 — The quantum harmonic oscillator

The QHO TISE is

$$\psi'' = \frac{m^2\omega^2}{\hbar^2}\left(x^2 - \frac{2E}{m\omega^2}\right)\psi.$$

This is *not* constant-coefficient — the coefficient of $\psi$ depends on $x$ — so the characteristic-equation method applies only asymptotically ($|x| \to \infty$, where $x^2$ dominates). The large-$|x|$ analysis gives $\psi \sim e^{-m\omega x^2/2\hbar}$, which is the decaying (normalizable) choice. One then substitutes $\psi(x) = H(x)\,e^{-m\omega x^2/2\hbar}$ and finds that $H(x)$ must satisfy Hermite's equation, solved by a power series (Frobenius method, related to M-04). The termination condition for the series — that $H(x)$ must be a polynomial, not an infinite series, to preserve normalizability — is the QHO's eigenvalue condition. The foundation is the same ODE logic; the technique is extended to non-constant coefficients.

### Vol. I, Ch. 7 — The finite square well and scattering states

The finite square well has three regions: interior ($|x| < a$, $V = -V_0$, oscillatory solution) and exterior ($|x| > a$, $V = 0$, evanescent solution for bound states). The general solution is written in each region; $\psi$ and $\psi'$ are matched at $x = \pm a$. The four matching equations (two conditions at two interfaces) plus the normalizability conditions (kill growing exponentials as $|x| \to \infty$) reduce to a transcendental equation for the allowed energies. This is the two-solution-family picture of this module — oscillatory inside, evanescent outside — plus the matching conditions, repeated.

For **scattering states** ($E > 0$), both regions have oscillatory solutions. The matching conditions at the interfaces give transmission and reflection amplitudes (complex numbers); the transmission probability is $T = |t|^2$ where $t$ is the ratio of transmitted to incident complex amplitude. The exponential basis $e^{\pm ikx}$ is natural here (traveling waves, not standing waves).

### Vol. III, Ch. 5 — WKB approximation

The WKB approximation treats the TISE as locally constant-coefficient in each infinitesimal region, with the local wave number

$$k(x) = \frac{\sqrt{2m(E - V(x))}}{\hbar}$$

varying slowly from point to point. In a classically allowed region ($E > V$), the local solution is oscillatory: $\psi \approx A(x)\,e^{i\int k\,dx}$, where the amplitude $A(x) \propto k(x)^{-1/2}$ from current conservation. In a forbidden region ($E < V$), $k(x) \to i\kappa(x)$ and the solution is evanescent: $\psi \approx B(x)\,e^{-\int\kappa\,dx}$. At a **turning point** ($E = V(x_0)$, $k = 0$), neither approximation holds and the two WKB solutions must be connected by **connection formulas** derived from the exact solution near the turning point (typically an Airy function). The whole WKB framework is the constant-coefficient solution family of this module applied patchwork, with connection formulas stitching the regions together.

---

## Conventions and pitfalls

**Sign of the $\psi''$ coefficient determines oscillatory vs. evanescent.** Write the TISE as $\psi'' = f(x)\psi$. If $f < 0$ (i.e., $E > V$): oscillatory, $\sin$ and $\cos$. If $f > 0$ (i.e., $E < V$): evanescent, $e^{\pm\kappa x}$. The sign is determined by the sign of $E - V$, which changes at the classical turning points.

**Both constants are needed inside a finite well.** Inside a finite well the solution is oscillatory, and both $\sin(kx)$ and $\cos(kx)$ are in the general solution. Students sometimes drop one by analogy with the infinite well (where a boundary condition at $x = 0$ forces out $\cos$). In the finite well there is no such boundary condition at the center; both terms survive until the matching conditions at the edges are applied.

**Two separate steps: boundary conditions, then normalization.** The ODE gives a two-parameter family; boundary conditions fix one or both constants (and select the eigenvalue $E_n$); normalization fixes the remaining overall amplitude. These are sequential, not simultaneous. Trying to normalize before applying boundary conditions is a common source of confusion.

**Continuity of $\psi'$ is required at every finite step.** At a discontinuity in $V$ (finite step, barrier edge), both $\psi$ and $\psi'$ must match. At an infinite wall, only $\psi$ matches (to zero); $\psi'$ is allowed to jump. The physical reason: the kinetic energy, proportional to $|\psi'|^2$ integrated, must remain finite everywhere for a finite-step potential, which requires $\psi'$ to be continuous; an infinite potential step can supply an infinite impulse and so allows $\psi'$ to jump.

**Quantization from boundary conditions, not the ODE.** The ODE is satisfied by solutions for every value of $E > 0$ (scattering states) or every $E > V_\text{min}$ (general case). The discrete energy levels emerge only when the boundary conditions are imposed. A student who looks at the ODE alone and expects to read off the energy levels has the causation backwards.

---

## Quick practice

1. Show by direct substitution that $\psi(x) = A\sin(kx) + B\cos(kx)$ satisfies $\psi'' = -k^2\psi$. Then apply the boundary conditions $\psi(0) = 0$ and $\psi(L) = 0$ and find the allowed values of $k$ for $A \neq 0$.

2. For the TISE in a region where $V > E$ (classically forbidden), write the general solution. A particle is in the region $x > 0$ only, with $\psi(x) \to 0$ as $x \to +\infty$. Which term in the general solution survives, and why?

3. Write the general solution in each of three regions for a finite square well: region I ($x < -a$), region II ($-a < x < a$, $V = -V_0$), and region III ($x > a$). List the four matching conditions at $x = \pm a$ without solving them, and count: how many equations, how many unknowns (the free constants), and what does this imply about when a solution exists?

---

## Go deeper

The source for this module is *Mathematics for Physics*, Vol. 1, Ch. 11, "Differential Equations and Oscillatory Motion," which develops the characteristic-equation method for the damped oscillator (the classical three-regime picture) and the general second-order linear constant-coefficient framework. For non-constant-coefficient ODEs (needed for the QHO and hydrogen atom), see *Mathematics for Physics*, Vol. 2, Ch. 7, "Special Functions and Separation of Variables."

For the QM side, Griffiths, *Introduction to Quantum Mechanics*, 3rd ed., Chs. 2–3 works through the infinite well, harmonic oscillator, and free particle using exactly the ODE methods of this module. Shankar, *Principles of Quantum Mechanics*, Ch. 5 treats the harmonic oscillator with the algebraic (ladder operator) method, which bypasses the ODE but does not replace it for wells and barriers. Cohen-Tannoudji, *Quantum Mechanics*, Vol. 1, Ch. II gives a careful treatment of the one-dimensional Schrödinger equation and matching conditions.

---

## References

- Isaac Newton, *Philosophiæ Naturalis Principia Mathematica* (1687) — second-law formulation as a differential equation. [verify]
- Robert Hooke, *Lectures de Potentia Restitutiva* (1678) — linear restoring force $F = -kx$, seed of the harmonic oscillator ODE. [verify]
- Leonhard Euler, "De integratione aequationum differentialium altiorum graduum" (1743, Euler Archive E62) — the exponential substitution $u = e^{rx}$ reducing a linear ODE to its characteristic equation. [verify]
- E. Schrödinger, "Quantisierung als Eigenwertproblem" (Annalen der Physik, 1926) — the Schrödinger equation as an eigenvalue problem; energy quantization from boundary conditions. [verify]
- D. J. Griffiths, *Introduction to Quantum Mechanics*, 3rd ed. (Cambridge, 2018), Chs. 2–3.
- R. Shankar, *Principles of Quantum Mechanics*, 2nd ed. (Plenum, 1994), Ch. 5.
- C. Cohen-Tannoudji, B. Diu, F. Laloë, *Quantum Mechanics*, Vol. 1 (Wiley, 1977), Ch. II.
- *Mathematics for Physics*, Vol. 1, Ch. 11 (source chapter for this module); Vol. 2, Ch. 7 (special functions, for non-constant-coefficient extensions).
