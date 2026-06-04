# Module M-05 — Fourier Series and the Wave Equation

**Refresher for QM chapters:** I·5 (infinite square well, eigenstate superposition), III·10 (periodic potentials, Bloch's theorem)

**Condensed from:** Mathematics for Physics Vol 1, Ch 14

---

## When you need this

The infinite square well (I·5) asks you to write an arbitrary initial wavefunction as a sum over energy eigenstates and then time-evolve it. That is a Fourier sine series, dressed in QM notation. Bloch's theorem (III·10) rests on the fact that a periodic potential can be expanded in a discrete set of spatial harmonics, and that each Fourier mode mixes a definite pair of momentum states. If you have seen Fourier series before, those chapters will be derivations; if not, they will be magic words. This module makes them derivations.

---

## The refresher

### Partial derivatives: two variables, two rates of change

A function $y(x, t)$ of two variables has two distinct rates of change. The **partial derivative** $\partial y/\partial x$ holds $t$ fixed and differentiates in $x$; $\partial y/\partial t$ holds $x$ fixed and differentiates in $t$. For a sinusoidal wave $y = A\sin(kx - \omega t)$:

$$\frac{\partial y}{\partial x} = Ak\cos(kx - \omega t) \quad \text{(slope of the spatial snapshot)},$$

$$\frac{\partial y}{\partial t} = -A\omega\cos(kx - \omega t) \quad \text{(transverse velocity of one point)}.$$

These are physically different quantities — a slope (dimensionless) and a velocity (m/s) — measured from the same function at the same instant. The curly $\partial$ is the notation that keeps them from being confused.

### The wave equation and why linearity is everything

Newton's second law applied to a small element of string under tension $F_T$ with mass per unit length $\mu$ gives the **one-dimensional wave equation**:

$$\frac{\partial^2 y}{\partial t^2} = v^2\,\frac{\partial^2 y}{\partial x^2}, \qquad v = \sqrt{\frac{F_T}{\mu}}.$$

Read it physically: curvature in space drives acceleration in time. Where the string is most bent, the tension mismatch is largest, and the string accelerates back hardest. The wave speed $v$ is a property of the medium alone.

The crucial property: the equation is **linear**. Every term is first-degree in $y$ and its derivatives, so if $y_1$ and $y_2$ both satisfy it, so does $c_1 y_1 + c_2 y_2$. **Superposition is the direct consequence of linearity.** This is the same property that makes the Schrödinger equation tractable: $\hat H$ is a linear operator, so any linear combination of solutions is a solution.

### Separation of variables: reducing a PDE to two ODEs

Look for solutions of the form $y(x, t) = X(x)\,T(t)$. Substituting into the wave equation and dividing:

$$\frac{T''(t)}{v^2\,T(t)} = \frac{X''(x)}{X(x)} = -k^2,$$

where $-k^2$ must be a constant (each side depends only on one variable, so both must equal the same constant). This gives two ordinary differential equations, both of the harmonic-oscillator form (M-03):

$$X'' = -k^2 X \quad \Rightarrow \quad X(x) = A\sin(kx) + B\cos(kx),$$

$$T'' = -(vk)^2 T = -\omega^2 T \quad \Rightarrow \quad T(t) = C\sin(\omega t) + D\cos(\omega t),$$

with $\omega = vk$. Imposing **boundary conditions** (e.g., a string fixed at $x = 0$ and $x = L$) forces $B = 0$ and $\sin(kL) = 0$, giving the **quantization** of allowed wavenumbers:

$$k_n = \frac{n\pi}{L}, \quad n = 1, 2, 3, \ldots$$

The allowed angular frequencies are $\omega_n = vk_n = n\pi v/L$. The general standing-wave mode is

$$y_n(x, t) = \sin\!\left(\frac{n\pi x}{L}\right)\!\left[C_n\sin(\omega_n t) + D_n\cos(\omega_n t)\right].$$

**This is the pattern that repeats in QM.** The energy eigenstates of the infinite square well are found by exactly the same procedure: separate the Schrödinger equation, impose boundary conditions, recover a discrete set of allowed wavenumbers, and identify the eigenstates as $\psi_n(x) = \sqrt{2/L}\sin(n\pi x/L)$.

### Fourier series: the general solution is a sum of modes

By superposition (linearity), the **general solution** is a sum over all allowed modes:

$$y(x, t) = \sum_{n=1}^{\infty} \sin\!\left(\frac{n\pi x}{L}\right)\!\left[C_n\sin(\omega_n t) + D_n\cos(\omega_n t)\right].$$

At $t = 0$ this becomes $y(x, 0) = \sum_{n=1}^{\infty} D_n \sin(n\pi x/L)$ — any initial shape expressed as a sum of sines. This is the **Fourier sine series**. The coefficients $D_n$ are found by projecting onto each mode using the **orthogonality** of the sine functions:

$$\int_0^L \sin\!\left(\frac{n\pi x}{L}\right)\sin\!\left(\frac{m\pi x}{L}\right)dx = \frac{L}{2}\,\delta_{nm},$$

which gives the coefficient formula:

$$D_n = \frac{2}{L}\int_0^L y(x, 0)\,\sin\!\left(\frac{n\pi x}{L}\right)dx.$$

This formula is not magic — it follows in one line from multiplying both sides of $y = \sum D_m \sin(m\pi x/L)$ by $\sin(n\pi x/L)$ and integrating. The orthogonality does all the work. The structure is: **expand in an orthogonal basis, project onto each basis function to find the coefficient.**

### General Fourier series for a periodic function

For a function of period $T$ with fundamental angular frequency $\omega_0 = 2\pi/T$, the general **Fourier series** (real form) is:

$$f(t) = \frac{a_0}{2} + \sum_{n=1}^{\infty}\!\left[a_n\cos(n\omega_0 t) + b_n\sin(n\omega_0 t)\right],$$

with $a_n = \frac{2}{T}\int_0^T f(t)\cos(n\omega_0 t)\,dt$ and $b_n = \frac{2}{T}\int_0^T f(t)\sin(n\omega_0 t)\,dt$.

Fourier's theorem (1822): any periodic function — including one with corners or jumps — can be represented this way [verify]. The only subtlety at jump discontinuities is the **Gibbs phenomenon**: the partial sums overshoot by about 9% of the jump height, and the overshoot persists as more terms are added (though it narrows). This matters for periodic-potential problems where $V(x)$ has sharp steps.

### The complex Fourier series (the form QM needs)

The real sin/cos form is not the natural language of quantum mechanics. Using Euler's formula $e^{i n\omega_0 t} = \cos(n\omega_0 t) + i\sin(n\omega_0 t)$ (M-01), the Fourier series takes the **complex form**:

$$f(t) = \sum_{n=-\infty}^{\infty} c_n\, e^{in\omega_0 t},$$

with coefficients

$$c_n = \frac{1}{T}\int_0^T f(t)\, e^{-in\omega_0 t}\,dt.$$

The sum runs over all integers $n$ (positive, zero, and negative), corresponding to positive and negative frequencies. For a real-valued $f$, the coefficients satisfy $c_{-n} = c_n^*$, so no information is lost by going complex — you just combine the sine and cosine coefficients into a single complex number. This complex form is the one that generalizes to the Fourier transform (M-06): as the period $T \to \infty$, the discrete sum over $n$ becomes an integral over a continuous frequency, and the $c_n$ become the transform $\tilde f(\omega)$.

The complex form is what QM actually uses. The spatial Bloch factor $e^{ikx}$ is a complex Fourier mode. The time-evolution factor $e^{-iE_n t/\hbar}$ is a complex Fourier coefficient in time. Writing QM expansions in the real sin/cos form is possible but awkward; the complex form is the right language.

### Worked example: expanding a parabolic wavefunction in the square-well basis

A particle in an infinite square well $(0 \leq x \leq L)$ is prepared in the state $\psi(x, 0) = Nx(L - x)$, a parabolic bump that vanishes at the walls. The energy eigenstates are $\psi_n(x) = \sqrt{2/L}\,\sin(n\pi x/L)$ with energies $E_n = n^2\pi^2\hbar^2/2mL^2$.

The expansion coefficients are the Fourier sine coefficients:

$$c_n = \int_0^L \psi_n^*(x)\,\psi(x, 0)\,dx = N\sqrt{\frac{2}{L}}\int_0^L x(L-x)\sin\!\left(\frac{n\pi x}{L}\right)dx.$$

The integrand is an even function about $x = L/2$ for odd $n$ and odd for even $n$, so $c_n = 0$ for all even $n$. Only odd modes are present in the initial state. After normalization the state is

$$\psi(x, 0) = \sum_{n\,\text{odd}} c_n\,\psi_n(x),$$

and time evolution proceeds by multiplying each coefficient by its time-evolution factor:

$$\psi(x, t) = \sum_{n\,\text{odd}} c_n\, e^{-iE_n t/\hbar}\,\psi_n(x).$$

The probability of measuring energy $E_n$ is $|c_n|^2$; the state oscillates because different modes advance their phases at different rates $\omega_n = E_n/\hbar$. The beating between modes produces the oscillating probability density — **quantum revival** — and it is purely a Fourier phenomenon: interference between terms at incommensurable frequencies.

---

## In the quantum series

### The infinite square well is a vibrating string in QM clothing

The energy eigenstates of the infinite square well are found by exactly the separation-of-variables procedure above: separate $\psi(x,t) = \psi(x)e^{-iEt/\hbar}$ (which itself requires recognizing the time part as $T'' = -\omega^2 T$ with $\omega = E/\hbar$), solve the spatial ODE $\psi'' = -k^2\psi$ with $k = \sqrt{2mE}/\hbar$, impose $\psi(0) = \psi(L) = 0$, and recover the discrete spectrum $k_n = n\pi/L$. The eigenstates are standing sine waves. The Fourier series expansion of an arbitrary initial state in this basis is literally the calculation done above, with $\hbar$ appearing only in $E_n$ and the phase factors. This is not an analogy — it is the same mathematics. (I·5)

The Fourier-coefficient formula $c_n = \langle\psi_n|\psi\rangle = \int\psi_n^*(x)\psi(x)\,dx$ tells you:
- $|c_n|^2$ is the probability of finding energy $E_n$ on measurement (Born rule as Fourier coefficient squared).
- $\sum_n |c_n|^2 = 1$ is the normalization condition (Parseval's theorem, stated here as completeness of the eigenstate basis).
- Time evolution is $c_n(t) = c_n(0)\,e^{-iE_n t/\hbar}$ — each mode picks up an independent phase.

### Periodic potentials and Bloch's theorem

A crystal has a periodic potential $V(x + a) = V(x)$ where $a$ is the lattice spacing. Because $V$ is periodic, it has a Fourier series:

$$V(x) = \sum_{n=-\infty}^{\infty} V_n\, e^{i(2\pi n/a)x},$$

with Fourier coefficients $V_n = \frac{1}{a}\int_0^a V(x)\,e^{-i(2\pi n/a)x}\,dx$. The reciprocal-lattice vectors are $G_n = 2\pi n/a$. **Each Fourier component $V_n$ couples momentum states that differ by $\hbar G_n$**, because $e^{iG_n x}$ is a plane wave that transfers momentum $\hbar G_n$ via the matrix element $\langle k'|V|k\rangle = V_n\,\delta_{k', k+G_n}$.

Bloch's theorem — that the eigenstates of a periodic Hamiltonian take the form $\psi_k(x) = e^{ikx}u_k(x)$ where $u_k$ has the lattice periodicity — follows directly from this Fourier structure. Because $u_k$ is periodic, it can itself be expanded as $u_k(x) = \sum_n A_n e^{i G_n x}$, making the Bloch state $\psi_k = \sum_n A_n e^{i(k + G_n)x}$ — a superposition of plane waves with momenta $\hbar(k + G_n)$. The band gaps at the Brillouin zone boundary ($k = \pm\pi/a$) arise where two such plane waves ($k$ and $k - G_1 = k - 2\pi/a$) are degenerate in the free-particle case and get mixed by the Fourier component $V_1$ of the potential. The gap width is $2|V_1|$ — the magnitude of the relevant Fourier coefficient of $V$. (III·10)

---

## Conventions and pitfalls

**Normalization of basis functions.** The standing-wave functions $\sin(n\pi x/L)$ are orthogonal but not orthonormal: $\int_0^L \sin^2(n\pi x/L)\,dx = L/2$. The energy eigenstates $\psi_n = \sqrt{2/L}\sin(n\pi x/L)$ are orthonormal. Use the normalized $\psi_n$ when computing $c_n = \langle\psi_n|\psi\rangle$; using the unnormalized sine gives $c_n$ off by a factor of $\sqrt{L/2}$.

**Complex conjugate in the coefficient formula.** The expansion coefficient is $c_n = \int\psi_n^*(x)\psi(x)\,dx$ — the complex conjugate on $\psi_n$ is essential when the basis functions are complex. Students who learned real Fourier series often omit it when moving to complex bases.

**Complex vs. real form.** The real sin/cos series is a special case of the complex series when $f$ is real-valued. In QM, wavefunctions are generally complex, and the complex Fourier series is the natural form. Bloch's theorem and time-evolution phases both require complex exponentials.

**Completeness vs. orthogonality.** The orthogonality relation $\langle\psi_n|\psi_m\rangle = \delta_{nm}$ does not by itself guarantee that any function can be expanded in the $\{\psi_n\}$ basis — that is the separate statement of **completeness** $\sum_n |\psi_n\rangle\langle\psi_n| = \hat I$. For the infinite square well and for most standard Hamiltonians encountered in Vol. I–III, completeness can be quoted; but it should be recognized as a separate fact from orthogonality.

**Gibbs phenomenon.** When $V(x)$ has a jump discontinuity (square barrier, Kronig–Penney model), the Fourier series converges slowly (coefficients $\sim 1/n$) and overshoots at the jump by about 9%. The energy gaps in a nearly-free-electron model still come out right — the Fourier coefficient of $V$ at the relevant reciprocal lattice vector is the physical quantity — but the spatial picture of the potential from a finite-mode Fourier sum looks fringed near the steps.

**Separation of variables: conditions for it to work.** Separation requires a linear PDE with homogeneous boundary conditions and coefficients that factor. It works for the time-independent Schrödinger equation (the Hamiltonian is time-independent, the boundary conditions are on the spatial wavefunction). It does not work for time-dependent Hamiltonians, which is why perturbation theory (M-04) is needed for those.

---

## Quick practice

1. **Coefficient integral.** A square-well particle is prepared in the ground state of an offset harmonic oscillator, approximated as $\psi(x, 0) \propto \cos(\pi x/L)$ (re-zero appropriately). Compute $c_1$ and $c_2$, the projections onto the first two square-well eigenstates, using the orthogonality integral. Comment on why $c_2 = 0$.

2. **Complex Fourier series.** Convert the real Fourier series $f(t) = \cos(\omega_0 t) + \frac{1}{2}\sin(2\omega_0 t)$ into the complex form $f(t) = \sum_n c_n e^{in\omega_0 t}$. Identify all nonzero $c_n$ and verify $c_{-n} = c_n^*$.

3. **Bloch gap.** A weak periodic potential has Fourier coefficients $V_0 = -1.0$ eV (the average), $V_1 = V_{-1} = -0.1$ eV, and all higher coefficients negligible. At the first Brillouin zone boundary $k = \pi/a$, two free-electron states are degenerate. Use the result that the gap width is $2|V_1|$ to find the energy gap. What physical quantity sets which states are coupled?

---

## Go deeper

The full derivation — partial derivatives, the string-tension argument for the wave equation, d'Alembert's traveling-wave solution, superposition and standing waves, the Fourier series with worked coefficient integrals, the Gibbs phenomenon, and the decibel coda — is in **Mathematics for Physics Vol 1, Ch 14**. The present module condenses to what QM needs: separation of variables, orthogonal expansions, and the complex Fourier form that M-06 generalizes to the continuous transform.

---

## References

- Jean le Rond d'Alembert, "Recherches sur la courbe que forme une corde tendue mise en vibration," *Mémoires de l'Académie royale des sciences de Berlin* (1747; published 1749) — the wave equation and its general solution $f(x-vt)+g(x+vt)$. [verify]
- Daniel Bernoulli, "Réflexions et éclaircissements sur les nouvelles vibrations des cordes," *Mémoires de l'Académie royale des sciences de Berlin* (1753) — every string motion as a superposition of harmonic modes. [verify]
- Joseph Fourier, *Théorie analytique de la chaleur* (Paris, 1822; earlier memoir blocked by Lagrange in 1807) — any periodic function as a sum of sines and cosines. [verify]
- Felix Bloch, "Über die Quantenmechanik der Elektronen in Kristallgittern," *Zeitschrift für Physik* **52**, 555–600 (1929) — the form $\psi_k(x) = e^{ikx}u_k(x)$ for eigenstates in a periodic potential. [verify]
- Ralph Kronig and William Penney, "Quantum mechanics of electrons in crystal lattices," *Proceedings of the Royal Society of London A* **130**, 499–513 (1931) — the exactly solvable periodic-potential model illustrating Bloch bands and gaps. [verify]
