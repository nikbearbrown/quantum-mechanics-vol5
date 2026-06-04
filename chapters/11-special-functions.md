# Module M-11 — Special Functions: Hermite, Legendre, Laguerre, Spherical Harmonics, Bessel

**When you need this:** QM chapters I·7 (Quantum Harmonic Oscillator), II·6 (Angular Momentum), II·9 (Hydrogen Atom), III·7 (Scattering)

**Condensed from:** *Mathematics for Physics* Vol 2, Ch 7

---

## When you need this

Four different QM systems — the harmonic oscillator, the angular momentum eigenstates, the hydrogen atom, and the scattering problem — each produce a different family of functions when you solve their differential equations. A student working through the series will encounter Hermite polynomials in I·7, Legendre polynomials and spherical harmonics in II·6, associated Laguerre polynomials in II·9, and spherical Bessel functions in III·7. These look like four unrelated collections of exotic formulas to memorize.

They are not. Every family is the set of orthogonal eigenfunctions of a **self-adjoint** second-order differential operator — a Sturm–Liouville operator. One theorem, the Sturm–Liouville theorem, explains why they are orthogonal, why arbitrary functions expand in them, and why their eigenvalues are real. This module gives you the unified structure and enough detail on each family to use them confidently in QM.

The explicit polynomial coefficients: look them up. The structure — how each family arises, why it is orthogonal, and what its orthogonality weight is — is the part to understand.

---

## The refresher

### The unifying structure: Sturm–Liouville theory

Every special function family satisfies an equation of the form

$$\frac{d}{dx}\!\left[p(x)\frac{dy}{dx}\right] + q(x)\,y + \lambda\,w(x)\,y = 0,$$

called the **Sturm–Liouville form**, where $p(x)$ and $w(x) > 0$ are real functions on an interval $[a, b]$, and $\lambda$ is the eigenvalue. Define the operator $\hat{L}y = \frac{1}{w}\big[-(py')' - qy\big]$; it is **self-adjoint** with respect to the weighted inner product

$$\langle f, g\rangle = \int_a^b f^*(x)\,g(x)\,w(x)\,dx.$$

Self-adjointness means $\langle f, \hat{L}g\rangle = \langle \hat{L}f, g\rangle$ — provided the boundary term $\big[p(f^* g' - (f^*)' g)\big]_a^b$ vanishes. It vanishes whenever the boundary or regularity conditions imposed on the problem kill it.

**The orthogonality theorem.** For two eigenfunctions $y_m$, $y_n$ with distinct eigenvalues $\lambda_m \neq \lambda_n$:

$$(\lambda_m - \lambda_n)\int_a^b y_m(x)\,y_n(x)\,w(x)\,dx = \big[p(y_m' y_n - y_m y_n')\big]_a^b = 0,$$

so $\int_a^b y_m\,y_n\,w\,dx = 0$.

This is the same proof every time — two lines of algebra, with the boundary term vanishing by the same regularity conditions that quantize the eigenvalue. It explains all the orthogonality relations in the catalogue below as instances of one theorem.

**Generalized Fourier series.** Because each Sturm–Liouville family is also **complete** — every sufficiently smooth function can be represented — any target function $f$ expands as

$$f(x) = \sum_n c_n\,y_n(x), \qquad c_n = \frac{\langle y_n, f\rangle}{\langle y_n, y_n\rangle} = \frac{\int f\,y_n\,w\,dx}{\int y_n^2\,w\,dx}.$$

The coefficients are computed by orthogonality exactly as ordinary Fourier coefficients: project $f$ onto each basis function in turn. The Fourier series of periodic functions is the special case with a trigonometric basis; every special-function expansion generalizes the same idea to a basis adapted to the geometry of the problem.

### The catalogue

| Family | Defining ODE | Interval, weight $w$ | QM role |
|--------|-------------|----------------------|---------|
| Hermite $H_n(\xi)$ | $H'' - 2\xi H' + 2nH = 0$ | $(-\infty,\infty)$, $w=e^{-\xi^2}$ | harmonic oscillator eigenstates |
| Legendre $P_\ell(u)$ | $\frac{d}{du}[(1-u^2)P'] + \ell(\ell+1)P = 0$ | $[-1,1]$, $w=1$ | axisymmetric central-potential angular part |
| Associated Legendre $P_\ell^m(u)$ | same with $-m^2/(1-u^2)$ term | $[-1,1]$, $w=1$ | non-axisymmetric angular solutions |
| Spherical harmonics $Y_{\ell m}(\theta,\phi)$ | $\hat{L}^2 Y = \hbar^2\ell(\ell+1)Y$ | sphere, $w=\sin\theta$ | angular eigenstates of every central potential |
| Associated Laguerre $L_n^k(\rho)$ | $\rho L'' + (k+1-\rho)L' + nL = 0$ | $[0,\infty)$, $w=\rho^k e^{-\rho}$ | hydrogen radial wavefunctions |
| Spherical Bessel $j_\ell(x)$ | $x^2 j'' + 2x j' + [x^2 - \ell(\ell+1)]j = 0$ | $[0,\infty)$, $w=r^2$ | free-particle radial; scattering partial waves |
| Cylindrical Bessel $J_m(x)$ | $x^2 R'' + xR' + (x^2 - m^2)R = 0$ | $[0,a]$, $w=\rho$ | cylindrical geometry, waveguides, Airy disk |

---

### Hermite polynomials — harmonic oscillator (QM I·7)

**Where they come from.** The 1D harmonic oscillator equation, written in the dimensionless variable $\xi = \sqrt{m\omega/\hbar}\,x$, is

$$-\frac{d^2\psi}{d\xi^2} + \xi^2\psi = \frac{2E}{\hbar\omega}\psi.$$

The asymptotic behavior as $|\xi| \to \infty$ is Gaussian, so factor it out: write $\psi(\xi) = H(\xi)\,e^{-\xi^2/2}$. Substituting gives **Hermite's equation** for $H$:

$$H'' - 2\xi H' + 2n H = 0, \qquad n = \frac{E}{\hbar\omega} - \frac{1}{2}.$$

**Quantization.** The power-series solution to Hermite's equation has infinitely many terms in general. For $\psi$ to be normalizable, $H$ must be a polynomial — the series must terminate. This forces $n$ to be a non-negative integer, giving the energy spectrum:

$$\boxed{E_n = \hbar\omega\!\left(n + \tfrac{1}{2}\right), \qquad n = 0, 1, 2, \ldots}$$

The evenly spaced ladder, including zero-point energy $E_0 = \tfrac{1}{2}\hbar\omega$, follows from the termination condition alone.

**The first few polynomials** (physicist's convention, leading coefficient $2^n$):
$$H_0(\xi) = 1, \quad H_1(\xi) = 2\xi, \quad H_2(\xi) = 4\xi^2 - 2, \quad H_3(\xi) = 8\xi^3 - 12\xi.$$

**Full eigenstates:**
$$\psi_n(x) = N_n\,H_n(\xi)\,e^{-\xi^2/2}, \qquad N_n = \left(\frac{m\omega}{\pi\hbar}\right)^{1/4}\frac{1}{\sqrt{2^n\,n!}}.$$

**Orthogonality** (weight $e^{-\xi^2}$, from the Gaussian factor):
$$\int_{-\infty}^{\infty} H_m(\xi)\,H_n(\xi)\,e^{-\xi^2}\,d\xi = \sqrt{\pi}\,2^n\,n!\,\delta_{mn}.$$

**Recurrence relation** (practical for matrix elements):
$$H_{n+1}(\xi) = 2\xi\,H_n(\xi) - 2n\,H_{n-1}(\xi).$$

This recurrence, combined with $\xi\,H_n = \tfrac{1}{2}H_{n+1} + n\,H_{n-1}$, lets you compute $\langle n|\hat{x}|n'\rangle$ and $\langle n|\hat{p}|n'\rangle$ algebraically without evaluating a Gaussian integral.

*Note:* the ladder-operator derivation (using $\hat{a}^\dagger$ and $\hat{a}$) produces the same energy spectrum and the same eigenstates. The power-series route reveals the polynomial structure explicitly; the ladder route is more efficient for most QM calculations. Both are valid; Module M-09 covers the operator side.

---

### Legendre polynomials and spherical harmonics — angular momentum (QM II·6)

**Where they come from.** Separation of the spherical Laplacian (see Module M-10) produces the polar equation. With $u = \cos\theta$:

$$\frac{d}{du}\!\left[(1-u^2)\frac{dP}{du}\right] + \ell(\ell+1)\,P = 0.$$

This is the **Legendre equation**. Demanding finiteness at $u = \pm 1$ (the poles $\theta = 0, \pi$) forces $\ell \in \{0, 1, 2, \ldots\}$ and gives the **Legendre polynomials** $P_\ell(u)$.

**The first few:**
$$P_0(u) = 1, \quad P_1(u) = u, \quad P_2(u) = \tfrac{1}{2}(3u^2 - 1), \quad P_3(u) = \tfrac{1}{2}(5u^3 - 3u).$$

**Orthogonality** (weight $w = 1$):
$$\int_{-1}^{1} P_m(u)\,P_n(u)\,du = \frac{2}{2n+1}\,\delta_{mn}.$$

**Associated Legendre functions** arise when $m \neq 0$ (non-axisymmetric solutions). They are defined by

$$P_\ell^m(u) = (-1)^m(1-u^2)^{m/2}\frac{d^m}{du^m}P_\ell(u), \qquad |m| \leq \ell.$$

The constraint $|m| \leq \ell$ comes from combining the regularity condition at the poles with the azimuthal single-valuedness condition.

**Spherical harmonics** combine the polar and azimuthal parts:

$$Y_{\ell m}(\theta,\phi) = \sqrt{\frac{(2\ell+1)}{4\pi}\frac{(\ell-|m|)!}{(\ell+|m|)!}}\,P_\ell^{|m|}(\cos\theta)\,e^{im\phi}.$$

**Orthonormality on the sphere** (weight $w = \sin\theta$ — the area element):
$$\int_0^{2\pi}\!\int_0^{\pi} Y_{\ell'm'}^*(\theta,\phi)\,Y_{\ell m}(\theta,\phi)\,\sin\theta\,d\theta\,d\phi = \delta_{\ell\ell'}\,\delta_{mm'}.$$

**Key low-$\ell$ harmonics:**
$$Y_{00} = \frac{1}{\sqrt{4\pi}}, \quad Y_{10} = \sqrt{\frac{3}{4\pi}}\cos\theta, \quad Y_{1,\pm 1} = \mp\sqrt{\frac{3}{8\pi}}\sin\theta\,e^{\pm i\phi}.$$

$Y_{00}$ is spherically symmetric (the $s$-orbital shape). $Y_{10}$ is the $p_z$ lobe. Linear combinations of $Y_{1,\pm 1}$ give $p_x$ and $p_y$.

**Angular momentum eigenvalue equations:**
$$\hat{L}^2\,Y_{\ell m} = \hbar^2\ell(\ell+1)\,Y_{\ell m}, \qquad \hat{L}_z\,Y_{\ell m} = \hbar m\,Y_{\ell m}.$$

The separation constant $\ell(\ell+1)$ from the PDE is exactly the eigenvalue of the angular momentum squared operator. The quantum number $m$ from the azimuthal separation is the eigenvalue of $\hat{L}_z$. The PDE separation and the operator eigenvalue problem are the same thing, seen from two angles.

**Phase convention:** the factor $(-1)^m$ in the associated Legendre functions for $m > 0$ is the **Condon–Shortley convention**, standard in physics. Some mathematical references omit it or place it differently. Always verify $[Y_{\ell'm'}^*, Y_{\ell m}]$ orthogonality holds with the convention you are using. [verify: Condon–Shortley, *The Theory of Atomic Spectra*, 1935]

---

### Associated Laguerre polynomials — hydrogen radial wavefunctions (QM II·9)

**Where they come from.** With the angular part separated and $Y_{\ell m}$ already determined, the hydrogen radial equation for $R(r)$ is

$$-\frac{\hbar^2}{2\mu}\frac{1}{r^2}\frac{d}{dr}\!\left(r^2\frac{dR}{dr}\right) + \left[\frac{\hbar^2\ell(\ell+1)}{2\mu r^2} - \frac{e^2}{4\pi\varepsilon_0 r}\right]R = ER.$$

(Here $\mu$ is the reduced mass.) For $E < 0$ (bound states), introduce the dimensionless variable $\rho = 2r/(na_0)$ where $a_0 = \hbar^2/({\mu e^2/4\pi\varepsilon_0})$ is the Bohr radius and $n$ is determined by the termination condition. After factoring out the asymptotic forms $\rho^\ell$ (regular at origin) and $e^{-\rho/2}$ (normalizable at infinity), the equation for the remaining factor $L(\rho)$ is the **associated Laguerre equation**:

$$\rho\frac{d^2L}{d\rho^2} + (2\ell + 2 - \rho)\frac{dL}{d\rho} + (n - \ell - 1)L = 0.$$

**Quantization.** For the series to terminate (so that $R$ is normalizable), the quantity $n - \ell - 1$ must be a non-negative integer, the **radial quantum number** $n_r = n - \ell - 1 \geq 0$. This forces $n = 1, 2, 3, \ldots$ and $\ell = 0, 1, \ldots, n - 1$. The **hydrogen energy spectrum** is

$$\boxed{E_n = -\frac{13.6\;\text{eV}}{n^2}, \qquad n = 1, 2, 3, \ldots}$$

**Radial wavefunctions:**
$$R_{n\ell}(r) = -\sqrt{\left(\frac{2}{na_0}\right)^3\frac{(n-\ell-1)!}{2n[(n+\ell)!]^3}}\,e^{-r/na_0}\!\left(\frac{2r}{na_0}\right)^\ell L_{n-\ell-1}^{2\ell+1}\!\!\left(\frac{2r}{na_0}\right).$$

The full wavefunction is $\psi_{n\ell m}(r,\theta,\phi) = R_{n\ell}(r)\,Y_{\ell m}(\theta,\phi)$.

**Orthogonality** (weight $w = r^2$, the radial part of the spherical volume element):
$$\int_0^\infty R_{n\ell}(r)\,R_{n'\ell}(r)\,r^2\,dr = \delta_{nn'}.$$

**Degeneracy.** For fixed $n$, $\ell$ runs from $0$ to $n-1$, and for each $\ell$, $m$ runs from $-\ell$ to $+\ell$ ($2\ell + 1$ values). The total number of spatial states with energy $E_n$ is $\sum_{\ell=0}^{n-1}(2\ell+1) = n^2$, doubled by spin: $\mathbf{2n^2}$ states per level. Every one of these quantum numbers — and the degeneracy count — falls out of the three separation conditions. Nothing is postulated.

**First few explicit radial functions** (for reference):
$$R_{10} = 2\left(\frac{1}{a_0}\right)^{3/2}e^{-r/a_0}, \quad R_{20} = \frac{1}{\sqrt{2}}\!\left(\frac{1}{2a_0}\right)^{3/2}\!\!\left(1 - \frac{r}{2a_0}\right)e^{-r/2a_0}.$$

$R_{10}$ has no nodes; $R_{20}$ has one node at $r = 2a_0$. In general $R_{n\ell}$ has $n - \ell - 1$ radial nodes.

---

### Spherical Bessel functions — scattering (QM III·7)

**Where they come from.** For a **free particle** or a particle outside a finite-range potential (where $V = 0$), the radial Schrödinger equation in spherical coordinates is

$$\frac{d^2u}{dr^2} + \left[k^2 - \frac{\ell(\ell+1)}{r^2}\right]u = 0, \qquad u = rR.$$

This is the **spherical Bessel equation** in standard form. Its two linearly independent solutions are the **spherical Bessel function** $j_\ell(x)$ (regular at $r = 0$) and the **spherical Neumann function** $n_\ell(x)$ (singular at $r = 0$):

$$j_\ell(x) = \sqrt{\frac{\pi}{2x}}\,J_{\ell+1/2}(x), \qquad n_\ell(x) = (-1)^{\ell+1}\sqrt{\frac{\pi}{2x}}\,J_{-\ell-1/2}(x).$$

Here $J_\nu$ is the standard (cylindrical) Bessel function of order $\nu$. The relation to cylindrical Bessel functions is exact; spherical Bessel functions are Bessel functions of half-integer order.

**The first few** (for direct use in scattering):
$$j_0(x) = \frac{\sin x}{x}, \qquad j_1(x) = \frac{\sin x}{x^2} - \frac{\cos x}{x}, \qquad n_0(x) = -\frac{\cos x}{x}.$$

**Asymptotic forms** ($kr \to \infty$, the physically important limit):
$$j_\ell(kr) \xrightarrow{kr \to \infty} \frac{\sin(kr - \ell\pi/2)}{kr}, \qquad n_\ell(kr) \xrightarrow{kr \to \infty} -\frac{\cos(kr - \ell\pi/2)}{kr}.$$

**In scattering.** Outside the interaction region, where $V = 0$, the general radial solution is a linear combination $j_\ell\cos\delta_\ell - n_\ell\sin\delta_\ell$. The **phase shift** $\delta_\ell$ is defined by comparing this to the free-particle solution $j_\ell$: it encodes how much the potential has shifted the asymptotic wave. The scattering amplitude and total cross section are computed from the phase shifts via the partial-wave expansion. The $j_\ell$ functions are the reference; the $n_\ell$ functions appear because the origin is excluded from the scattering region (so both regular and irregular solutions are allowed).

**Cylindrical Bessel functions $J_m(x)$.** These arise in problems with cylindrical symmetry (waveguides, optical fibers, quantum wires). Their zeros determine the allowed modes: for a hard-wall cylinder of radius $a$, the condition $J_m(ka) = 0$ quantizes $k$. The famous factor $1.22$ in the Rayleigh resolution limit $\theta_{\min} = 1.22\lambda/D$ is $j_{1,1}/\pi$ where $j_{1,1} \approx 3.832$ is the first zero of $J_1$. [verify: Rayleigh, *Phil. Mag.*, 1879]

---

## Worked example: which special function and why

The following table is the diagnostic. Given a QM system, the logic of identification is always the same five steps: (1) choose the coordinate system that makes the boundary conditions or the potential separable; (2) apply the product ansatz; (3) recognize the resulting ODE by its form; (4) apply the regularity or termination condition that quantizes the eigenvalue; (5) the special function is the name of the regular solution.

| QM system | Coordinate system | Separated ODE | Quantization mechanism | Special function |
|-----------|------------------|---------------|------------------------|-----------------|
| 1D harmonic oscillator | Cartesian (1D) | Hermite: $H'' - 2\xi H' + 2nH = 0$ | series termination (normalizability) | $H_n(\xi)$ |
| Any central potential (angular) | Spherical ($\theta$, $\phi$) | Associated Legendre | finiteness at poles ($\theta = 0, \pi$) | $Y_{\ell m}(\theta,\phi)$ |
| Hydrogen atom (radial) | Spherical ($r$) | Associated Laguerre | series termination (normalizability) | $L_{n-\ell-1}^{2\ell+1}(\rho)$ |
| Free particle or scattering (radial) | Spherical ($r$) | Spherical Bessel | regularity at $r = 0$ (or asymptotic form) | $j_\ell(kr)$, $n_\ell(kr)$ |
| Cylindrical geometry (waveguide, wire) | Cylindrical ($\rho$) | Bessel: $\rho^2 R'' + \rho R' + (k^2\rho^2 - m^2)R = 0$ | zeros at wall: $J_m(ka) = 0$ | $J_m(k\rho)$ |

**Example application.** The ground state of the harmonic oscillator: $n = 0$, so $H_0(\xi) = 1$ (a constant). The eigenfunction is $\psi_0 \propto e^{-\xi^2/2}$ — a pure Gaussian with no nodes. Energy: $E_0 = \tfrac{1}{2}\hbar\omega$. The zero-point energy is non-zero because the termination condition's minimum allowed value is $n = 0$, not $n = -1$.

**Normalization check for $\psi_0$.** Setting $\int_{-\infty}^\infty |\psi_0|^2\,dx = 1$ with $\psi_0 = N_0\,e^{-\xi^2/2}$ and $d\xi = \sqrt{m\omega/\hbar}\,dx$:

$$N_0^2\sqrt{\frac{\hbar}{m\omega}}\int_{-\infty}^\infty e^{-\xi^2}\,d\xi = N_0^2\sqrt{\frac{\hbar}{m\omega}}\,\sqrt{\pi} = 1 \;\Longrightarrow\; N_0 = \left(\frac{m\omega}{\pi\hbar}\right)^{1/4}.$$

This is a computation type that frequently appears in QM homework — the integral $\int e^{-\xi^2}d\xi = \sqrt\pi$ is the Gaussian integral and is used whenever $n=0$ Hermite (or any Gaussian ground state) is normalized.

---

## In the quantum series

### QM I·7 — Quantum Harmonic Oscillator

The series-solution derivation of the harmonic oscillator produces Hermite's equation and the termination condition. The explicit forms $H_0 = 1$, $H_1 = 2\xi$, $H_2 = 4\xi^2 - 2$ give the first three eigenstates directly. For computing matrix elements $\langle n|\hat{x}|n'\rangle$ in the series, the recurrence $H_{n+1} = 2\xi H_n - 2nH_{n-1}$ is the practical tool.

### QM II·6 — Angular Momentum

The spherical harmonics $Y_{\ell m}$ are the joint eigenstates of $\hat{L}^2$ and $\hat{L}_z$. The eigenvalue equations $\hat{L}^2 Y_{\ell m} = \hbar^2\ell(\ell+1)Y_{\ell m}$ and $\hat{L}_z Y_{\ell m} = \hbar m\,Y_{\ell m}$ connect the separation constants from Module M-10 directly to the angular momentum operators. Orthonormality is required for computing expectation values and selection rules: a matrix element $\langle \ell'm'|\hat{O}|\ell m\rangle$ is an integral $\int Y_{\ell'm'}^* \hat{O}[Y_{\ell m}]\,d\Omega$ evaluated by orthogonality.

### QM II·9 — Hydrogen Atom

The complete hydrogen wavefunction $\psi_{n\ell m} = R_{n\ell}(r)Y_{\ell m}(\theta,\phi)$ is a product of a radial function (associated Laguerre) and an angular function (spherical harmonic). The orbital shapes ($s$, $p$, $d$, ...) are determined by $|Y_{\ell m}|^2$; the radial distribution function $r^2|R_{n\ell}|^2$ gives the most probable radius. The degeneracy $2n^2$ per energy level is counted by the constraint structure: $n$ fixes $E_n$; $\ell = 0, \ldots, n-1$; $m = -\ell, \ldots, +\ell$; the factor of 2 is spin.

### QM III·7 — Scattering

The partial-wave expansion writes the wavefunction as a sum of incoming and outgoing spherical waves, each characterized by a phase shift $\delta_\ell$. The radial solution outside the interaction region is $j_\ell(kr)\cos\delta_\ell - n_\ell(kr)\sin\delta_\ell$, matching asymptotically to $\sin(kr - \ell\pi/2 + \delta_\ell)/(kr)$. For a hard-sphere potential of radius $a$: $\tan\delta_\ell = j_\ell(ka)/n_\ell(ka)$, with the $\ell = 0$ phase shift dominant at low energy ($ka \ll 1$). The total cross section is $\sigma = (4\pi/k^2)\sum_\ell(2\ell+1)\sin^2\delta_\ell$.

---

## Conventions and pitfalls

**Physicist's Hermite vs. probabilist's Hermite.** Two conventions exist. The physicist's $H_n$ has leading coefficient $2^n$ and orthogonality weight $e^{-\xi^2}$. The probabilist's $\mathrm{He}_n$ has leading coefficient $1$ and weight $e^{-\xi^2/2}$. QM uniformly uses the physicist's convention. Verify by checking $H_1$: physicist's gives $H_1 = 2\xi$; probabilist's gives $\mathrm{He}_1 = \xi$. Using the wrong convention changes normalization constants by powers of 2.

**Associated Laguerre: normalization conventions vary.** Different authors define $L_n^k$ with or without a factor of $(-1)^k$ (or with the argument scaled differently). The hydrogen radial function is sensitive to the exact convention. When consulting any reference for explicit $R_{n\ell}$, verify the normalization by checking $\int_0^\infty |R_{n\ell}|^2 r^2\,dr = 1$.

**Condon–Shortley phase.** The standard physics convention includes the phase $(-1)^m$ for $m > 0$ in the associated Legendre functions:

$$P_\ell^m(u) = (-1)^m(1-u^2)^{m/2}\frac{d^m}{du^m}P_\ell(u), \quad m \geq 0.$$

Some mathematical tables omit it. The effect: $Y_{1,1}$ gets a factor of $-1$ compared to the convention without it. Mixing conventions produces wrong phases in angular momentum matrix elements and selection rules.

**Regular vs. irregular Bessel.** $j_\ell$ is regular (finite) at $r = 0$; $n_\ell$ diverges there. For any problem whose domain includes the origin (hydrogen, a particle in a sphere), only $j_\ell$ appears in the radial solution. In scattering, both appear because the origin is inside the scattering target and excluded from the region where the asymptotic expansion is applied.

**Nodes.** The number of radial nodes of $R_{n\ell}$ is $n - \ell - 1$. The number of nodes of $\psi_n$ for the harmonic oscillator is $n$. These are quick consistency checks: a student who writes a wavefunction that contradicts the node count has made an error somewhere.

**Do not memorize polynomial coefficients.** Memorize: (1) which physical system produces which family; (2) the quantization condition (termination vs. regularity); (3) the orthogonality weight; (4) the asymptotic behavior. Look up the explicit polynomials as needed.

---

## Quick practice

1. **Identification.** A particle is confined to the surface of a unit sphere (rigid rotor). The Hamiltonian is $\hat{H} = \hat{L}^2/(2I)$. Write down the energy eigenvalues and eigenfunctions without solving an ODE — by recognizing which special functions apply and why.

2. **Orthogonality check.** Use the orthogonality of Legendre polynomials to compute $\int_{-1}^1 P_2(u)\cdot u\,du$. First express $u = P_1(u)$, then apply the orthogonality relation $\int_{-1}^1 P_m P_n\,du = \frac{2}{2n+1}\delta_{mn}$.

3. **Hydrogen degeneracy.** List all quantum states $(n, \ell, m)$ with $n = 3$. Count them (excluding spin) and verify the count equals $n^2 = 9$. Identify which subshell ($3s$, $3p$, $3d$) each set belongs to, and state how many radial nodes each radial function $R_{3\ell}$ has.

---

## Go deeper

All seven families in the catalogue above, and the Sturm–Liouville theorem unifying them, are developed in *Mathematics for Physics* Vol 2, Ch 7 ("Special Functions and Separation of Variables"). The source covers Hermite, Legendre/spherical harmonics, and Bessel in full; the associated Laguerre section (Section 4, table row) names the equation and states the quantization result without full derivation. For the complete hydrogen radial solution, consult the QM series chapter II·9 directly, or Griffiths §4.2. For spherical Bessel functions in scattering, see *Mathematics for Physics* Vol 2, Ch 7, Section 3 (cylindrical Bessel), and QM III·7 for the partial-wave formalism.

---

## References

- Legendre, A.-M. "Recherches sur l'attraction des sphéroïdes homogènes." *Mémoires de Mathématiques et de Physique* **10** (read 1782, published 1785). [First appearance of $P_\ell(\cos\theta)$ in the multipole expansion of the Newtonian potential.]
- Hermite, C. Work on the polynomials bearing his name (1864). [The polynomial factors of the harmonic oscillator eigenstates; also appears in his 1873 proof of the transcendence of $e$.] [verify exact 1864 publication]
- Bessel, F. W. Systematization of the Bessel functions (1824), arising from planetary-perturbation calculations. [verify exact publication title and venue]
- Sturm, J. C. F., and J. Liouville. Papers founding Sturm–Liouville theory, *Journal de Mathématiques Pures et Appliquées* vols. 1–2 (1836–1837). [The unifying theorem that all special-function families are orthogonal eigenfunctions of self-adjoint operators. Dates and venue confirmed in Lützen, *Archive for History of Exact Sciences*.] [verify Lützen citation details]
- Condon, E. U., and G. H. Shortley. *The Theory of Atomic Spectra*. Cambridge University Press, 1935. [The phase convention for associated Legendre functions standard in physics.] [verify]
- Griffiths, D. J. *Introduction to Quantum Mechanics*, 3rd ed. Cambridge University Press, 2018. §4.2 (hydrogen atom; explicit $R_{n\ell}$ derivation and table). [verify edition]
- Abramowitz, M., and I. A. Stegun. *Handbook of Mathematical Functions*. National Bureau of Standards, 1964 (Dover reprint). Chapters 22 (orthogonal polynomials), 9 (Bessel functions), 10 (spherical Bessel functions). [The authoritative reference for explicit formulas, zeros, and numerical values.] [verify chapter numbers]
