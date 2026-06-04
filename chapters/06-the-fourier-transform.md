# Module M-06 — The Fourier Transform

**Refresher for QM chapters:** I·8 (wave packets), III·5 (transitions), III·8 (Born approximation)

**Condensed from:** Mathematics for Physics Vol 2, Ch 6

---

## When you need this

In I·8 you build a wave packet by superposing plane waves with a momentum-space envelope — that superposition is the inverse Fourier transform. In III·8 the Born approximation for scattering writes the amplitude as $\int V(\mathbf{r})\,e^{i\mathbf{q}\cdot\mathbf{r}}\,d^3r$ — that integral is the Fourier transform of the potential evaluated at the momentum transfer. If you recognize these as the same operation, both chapters become one calculation. If you do not, each one looks like a new formula to memorize. This module makes them the same operation.

---

## The refresher

### The transform as the $L \to \infty$ limit of the Fourier series

Module M-05 expanded a periodic function of period $L$ in complex Fourier modes:

$$f(x) = \sum_{n=-\infty}^{\infty} c_n\, e^{ik_n x}, \qquad c_n = \frac{1}{L}\int_{-L/2}^{L/2} f(x)\, e^{-ik_n x}\,dx, \qquad k_n = \frac{2\pi n}{L}.$$

The spectrum is a discrete comb of wavenumbers spaced $\Delta k = 2\pi/L$ apart. Now let the period grow without bound: $L \to \infty$. The spacing $\Delta k \to 0$, the comb fills in, and the sum over $n$ becomes an integral over a continuous variable $k$. Substituting $1/L = \Delta k/2\pi$ and passing to the limit defines the **Fourier transform pair**:

$$\boxed{\tilde f(k) = \int_{-\infty}^{\infty} f(x)\, e^{-ikx}\,dx} \qquad \text{(forward transform: position → wavenumber)}$$

$$\boxed{f(x) = \frac{1}{2\pi}\int_{-\infty}^{\infty} \tilde f(k)\, e^{ikx}\,dk} \qquad \text{(inverse transform: wavenumber → position)}$$

This is a derivation, not a definition: the Fourier transform is the Fourier series you already know, taken to continuous frequency. The function $\tilde f(k)$ is the **continuous spectrum** of $f$ — it says how much of each pure wave $e^{ikx}$ the function contains.

### The quantum convention: position and momentum

In QM the natural variable is momentum $p = \hbar k$, and the conventional choice is the **symmetric split** with $1/\sqrt{2\pi\hbar}$ on each side:

$$\tilde\psi(p) = \frac{1}{\sqrt{2\pi\hbar}}\int_{-\infty}^{\infty} \psi(x)\, e^{-ipx/\hbar}\,dx, \qquad \psi(x) = \frac{1}{\sqrt{2\pi\hbar}}\int_{-\infty}^{\infty} \tilde\psi(p)\, e^{ipx/\hbar}\,dp.$$

**This is the change of basis between position and momentum eigenstates.** Inserting the continuous resolution of the identity $\int |x\rangle\langle x|\,dx = \hat I$ into $\langle p|\psi\rangle$ gives exactly the Fourier integral:

$$\tilde\psi(p) = \langle p|\psi\rangle = \int \langle p|x\rangle\langle x|\psi\rangle\,dx = \frac{1}{\sqrt{2\pi\hbar}}\int e^{-ipx/\hbar}\,\psi(x)\,dx,$$

where $\langle x|p\rangle = e^{ipx/\hbar}/\sqrt{2\pi\hbar}$ is the **momentum eigenstate in position representation** — a pure wave with wavenumber $k = p/\hbar$. The Fourier transform is not a computational trick layered on top of the quantum formalism: it is the inner product between position and momentum eigenstates, with the plane wave as the overlap kernel.

**Convention warning.** The factor of $2\pi$ can be placed entirely on the inverse transform (as in the mathematical convention above), split symmetrically as $1/\sqrt{2\pi}$ (or $1/\sqrt{2\pi\hbar}$ in QM), or removed by using ordinary frequency $\nu$ with $e^{-2\pi i\nu x}$. The sign of the exponent can also flip between fields ($e^{-ikx}$ vs. $e^{+ikx}$ as the forward transform). No convention is more correct; inconsistency between a QM text, a math reference, and a physics paper is the source of most mysterious factors of $2\pi$ or $\hbar$. Write the convention explicitly every time.

### Plancherel: the transform preserves probability

The transform is (up to a constant) unitary. **Plancherel's theorem** [verify] states:

$$\int_{-\infty}^{\infty}|f(x)|^2\,dx = \frac{1}{2\pi}\int_{-\infty}^{\infty}|\tilde f(k)|^2\,dk.$$

In the symmetric QM convention, a normalized position-space wavefunction $\int|\psi(x)|^2\,dx = 1$ gives a normalized momentum-space wavefunction $\int|\tilde\psi(p)|^2\,dp = 1$. Total probability is the same in either basis. This is the analysis-level version of the fact that a unitary change of basis preserves norms.

### The convolution theorem

The **convolution** of two functions smears one with the other:

$$(f * g)(x) = \int_{-\infty}^{\infty} f(x')\,g(x - x')\,dx'.$$

The **convolution theorem** says this complicated operation becomes simple multiplication in Fourier space:

$$\boxed{\widetilde{f * g}(k) = \tilde f(k)\cdot\tilde g(k).}$$

*Proof in one step:* substitute $g(x - x')$, change variable $u = x - x'$, and the two integrals separate into $\tilde f(k) \cdot \tilde g(k)$. Equivalently (by swapping roles): multiplication in real space is convolution in Fourier space.

QM applications: when the perturbation is a product of two factors (e.g., a spatial envelope times an oscillation), the transition matrix element is the convolution of their transforms. In scattering, the double-slit amplitude is the single-slit transform times the two-delta transform — the two-slit structure is a convolution, so the diffraction pattern is a product.

### The bandwidth relation and the uncertainty principle

Define the rms spatial width $\Delta x$ of $|f|^2$ and the rms spectral width $\Delta k$ of $|\tilde f|^2$. Then for any function:

$$\boxed{\Delta x\,\Delta k \geq \tfrac{1}{2}.}$$

This is a theorem about **any** Fourier pair, with no quantum mechanics involved. Intuition: the scaling property $f(x) \mapsto f(ax)$ compresses the function by factor $a$ while stretching its transform by the same factor — the product of widths is invariant, so squeeze in $x$ and the spectrum spreads in $k$.

Rescaling to momentum via $p = \hbar k$ converts this to $\Delta x\,\Delta p \geq \hbar/2$ — the **Heisenberg uncertainty principle**. But there are two routes to this inequality, and keeping them distinct matters:

1. **Fourier route:** $\Delta x\,\Delta k \geq \frac12$ (pure mathematics of transform pairs) $\xrightarrow{p = \hbar k}$ $\Delta x\,\Delta p \geq \frac\hbar2$.

2. **Robertson route:** For any two observables $\hat A$, $\hat B$ with commutator $[\hat A, \hat B]$: $\sigma_A\sigma_B \geq \frac12|\langle[\hat A,\hat B]\rangle|$. For $[\hat x, \hat p] = i\hbar$: $\sigma_x\sigma_p \geq \frac\hbar2$.

Both reproduce $\sigma_x\sigma_p \geq \hbar/2$, but they are not the same statement. The energy–time relation $\Delta E\,\Delta t \sim \hbar$ is the Fourier route applied to time and frequency — it is **not** the Robertson route, because time is not an operator in standard quantum mechanics. Treating $\Delta E\,\Delta t$ as a Robertson commutator is a category error that III·5 sometimes tempts students into.

### The Gaussian: minimum uncertainty and its own transform

The Gaussian $f(x) = e^{-x^2/2a^2}$ transforms to another Gaussian:

$$\tilde f(k) = a\sqrt{2\pi}\,e^{-a^2 k^2/2}.$$

Proof: complete the square in the exponent of $\int e^{-x^2/2a^2}e^{-ikx}dx$, then use the standard Gaussian integral $\int e^{-u^2/2a^2}du = a\sqrt{2\pi}$.

The Gaussian is the **unique shape that saturates the bandwidth bound**: $\Delta x\,\Delta k = \frac12$ exactly. For the normalized QM Gaussian $\psi(x) = (\pi a^2)^{-1/4}e^{-x^2/2a^2}$, the position width is $\Delta x = a/\sqrt{2}$ and the momentum width is $\Delta p = \hbar/(a\sqrt{2})$, giving $\Delta x\,\Delta p = \hbar/2$. This is why the Gaussian wave packet is the **minimum-uncertainty state** — the most classical-like quantum state, with the position and momentum uncertainties balanced as tightly as the laws of nature permit. Small $a$ (well-localized in $x$) forces large $\Delta p$, and vice versa, in exact reciprocal proportion.

### The Dirac delta: the continuous Kronecker

To handle continuous bases we need an object that selects a single point. The **Dirac delta** is defined entirely by its action under integration:

$$\int_{-\infty}^{\infty} \delta(x - x_0)\,f(x)\,dx = f(x_0).$$

It is not an ordinary function — it is a distribution (in Schwartz's sense [verify]) — and manipulating it outside an integral leads to nonsense. It arises as the Fourier transform of a constant:

$$\delta(x - x') = \frac{1}{2\pi}\int_{-\infty}^{\infty} e^{ik(x - x')}\,dk.$$

This is the continuous analogue of the Kronecker delta $\delta_{mn}$ and is what makes the continuous resolution of the identity work: $\langle x|x'\rangle = \delta(x - x')$ is the continuous-basis version of $\langle e_m|e_n\rangle = \delta_{mn}$.

### Worked example: Gaussian wave packet from position to momentum space

Take the normalized Gaussian $\psi(x) = (\pi a^2)^{-1/4}e^{-x^2/2a^2}$ (centered at $x = 0$, zero mean momentum). The momentum wavefunction, using the symmetric QM convention:

$$\tilde\psi(p) = \frac{1}{\sqrt{2\pi\hbar}}\int_{-\infty}^{\infty} (\pi a^2)^{-1/4} e^{-x^2/2a^2}\, e^{-ipx/\hbar}\,dx.$$

Complete the square: $-x^2/2a^2 - ipx/\hbar = -\frac{1}{2a^2}\!\left(x + ipa^2/\hbar\right)^2 - \frac{p^2 a^2}{2\hbar^2}$. The completed-square integral is the standard Gaussian shifted to a complex center (the shift does not affect the value for functions analytic in the strip — justified by contour deformation):

$$\tilde\psi(p) = \left(\frac{a^2}{\pi\hbar^2}\right)^{1/4}\exp\!\left(-\frac{a^2 p^2}{2\hbar^2}\right).$$

This is a Gaussian in $p$ with width $\Delta p = \hbar/(a\sqrt{2})$. Position width: $\Delta x = a/\sqrt{2}$. Product: $\Delta x\,\Delta p = \hbar/2$ — saturation of the uncertainty bound.

**Reading the result physically:** large $a$ means the particle is spread out in space (large $\Delta x$) and has a narrow, well-defined momentum (small $\Delta p$). Small $a$ means it is localized (small $\Delta x$) but has a wide momentum distribution (large $\Delta p$). The Fourier transform enforces this trade-off automatically.

### The 3D transform and Born scattering

The Fourier transform generalizes to three dimensions in the obvious way:

$$\tilde f(\mathbf{k}) = \int f(\mathbf{r})\, e^{-i\mathbf{k}\cdot\mathbf{r}}\,d^3r, \qquad f(\mathbf{r}) = \frac{1}{(2\pi)^3}\int \tilde f(\mathbf{k})\, e^{i\mathbf{k}\cdot\mathbf{r}}\,d^3k.$$

For a **spherically symmetric** potential $V(r)$, choosing $\hat z \parallel \mathbf{q}$ (momentum transfer $\mathbf{q} = \mathbf{k}_i - \mathbf{k}_f$) and integrating over angles:

$$\tilde V(q) = \int_0^\infty V(r)\,\frac{2\sin(qr)}{qr}\cdot 2\pi r^2\,dr = \frac{4\pi}{q}\int_0^\infty V(r)\,r\sin(qr)\,dr,$$

reducing a 3D transform to a 1D integral.

The **first Born approximation** for the scattering amplitude is [verify]:

$$f(\theta) = -\frac{m}{2\pi\hbar^2}\int V(\mathbf{r})\, e^{i\mathbf{q}\cdot\mathbf{r}}\,d^3r = -\frac{m}{2\pi\hbar^2}\,\tilde V(\mathbf{q}),$$

where $q = 2k\sin(\theta/2)$ and $k = |\mathbf{k}_i| = |\mathbf{k}_f|$ (elastic scattering). **The Born scattering amplitude is the Fourier transform of the potential, evaluated at the momentum transfer.** Recognizing this converts the Born formula from an intimidating integral into a transform computation: for a Yukawa potential $V(r) = V_0 e^{-r/a}/r$, its 3D transform is $\tilde V(q) = 4\pi V_0/(q^2 + a^{-2})$ — a Lorentzian in $q$ — giving the screened-Coulomb (Yukawa) differential cross-section directly.

---

## In the quantum series

### Position and momentum as conjugate Fourier variables (I·8)

A free-particle wave packet is built by superposing momentum eigenstates $e^{ipx/\hbar}/\sqrt{2\pi\hbar}$ with weight $\tilde\psi(p)$:

$$\psi(x, 0) = \frac{1}{\sqrt{2\pi\hbar}}\int \tilde\psi(p)\, e^{ipx/\hbar}\,dp.$$

This is the inverse Fourier transform from $p$-space to $x$-space. Time evolution of the free particle is simplest in momentum space: each component $\tilde\psi(p)$ acquires the phase $e^{-ip^2 t/2m\hbar}$ (because $E = p^2/2m$), giving

$$\psi(x, t) = \frac{1}{\sqrt{2\pi\hbar}}\int \tilde\psi(p)\, e^{-ip^2 t/2m\hbar}\, e^{ipx/\hbar}\,dp.$$

For a Gaussian $\tilde\psi(p)$, completing the square in the exponent yields the time-evolved $\psi(x,t)$ — a Gaussian that spreads: $\Delta x(t) = \Delta x(0)\sqrt{1 + (t\hbar/m\Delta x(0)^2)^2}$. **Wave packet spreading is a direct consequence of the Fourier bandwidth relation:** a narrow $\Delta x$ at $t = 0$ requires a wide $\Delta p$, and different momentum components travel at different speeds $v = p/m$, so the packet broadens in time. The spreading is not mysterious — it is kinematics plus Fourier.

The **group velocity** of the packet, $v_g = d\omega/dk|_{k_0}$, gives the speed of the packet center. The **phase velocity** $v_\phi = \omega/k$ gives the speed of individual phase fronts. For a quantum particle $\omega = \hbar k^2/2m$, so $v_g = \hbar k_0/m = p_0/m$ (the classical particle velocity) while $v_\phi = \hbar k_0/2m = p_0/2m$ — half the classical speed. The packet center moves classically; the individual wave crests do not.

### Transitions and the time–frequency bandwidth (III·5)

Time-dependent perturbation theory computes transition amplitudes as

$$c_{f \leftarrow i}(t) \propto \int_0^t \langle f|\hat V(t')| i\rangle\, e^{i\omega_{fi} t'}\,dt',$$

where $\omega_{fi} = (E_f - E_i)/\hbar$. For a perturbation that turns on at $t = 0$ and runs for time $T$, the integral is the Fourier transform of $\langle f|\hat V|i\rangle$ as a function of time, evaluated at the transition frequency $\omega_{fi}$. The transition probability is large when the Fourier spectrum of the perturbation has significant weight at $\omega_{fi}$ — which is the energy-conservation condition in Fourier language.

For a perturbation of duration $T$, its Fourier spectrum has width $\Delta\omega \sim 1/T$ (the bandwidth relation in time–frequency). This gives $\Delta E \sim \hbar/T$, which is the **energy–time uncertainty relation** — a Fourier theorem, not a Robertson commutator. The longer the interaction lasts, the more sharply defined the energy transfer.

### The Born amplitude is a Fourier transform (III·8)

As derived above, the first Born scattering amplitude is $f(\theta) \propto \tilde V(\mathbf{q})$ — the 3D Fourier transform of the potential at the momentum transfer $\mathbf{q}$. Every feature of the Born cross-section is a feature of the potential's Fourier transform:

- **Forward scattering** ($\theta = 0$, $q = 0$): $\tilde V(0) = \int V(\mathbf{r})\,d^3r$ is the spatial integral of the potential — a long-range potential with large $\tilde V(0)$ gives strong forward enhancement.
- **Large-angle scattering** ($q$ large): the cross-section is determined by the high-$q$ components of $\tilde V$, which are small for smooth potentials (the transform of a smooth function falls off rapidly) and large for sharp potentials (e.g., a hard-sphere potential has significant power at all $q$ up to $\sim 1/R$).
- **Diffraction dips** in nuclear scattering ($^{12}$C, $^{16}$O): the Fourier transform of a uniform sphere is $\propto j_1(qR)/qR$ (a spherical Bessel function), which has zeros at definite angles — the same mathematics as single-slit diffraction.

Reading Born scattering through Fourier eyes converts an opaque integral into a physical picture: you are measuring the spatial frequency content of the potential at the spatial frequency set by the momentum transfer.

---

## Conventions and pitfalls

**The $2\pi$ placement.** Three common conventions are in active use. (1) Asymmetric: $1/2\pi$ on inverse only (standard math convention, used in the source chapter). (2) Symmetric: $1/\sqrt{2\pi}$ on each side (common in quantum optics and signal processing). (3) Quantum: $1/\sqrt{2\pi\hbar}$ on each side with $p = \hbar k$ (Griffiths-style QM). **State the convention you are using and do not switch mid-calculation.** Mixing conventions imports mysterious factors of $2\pi$ or $\hbar$ that are hard to track down.

**Sign of the exponent.** Physics convention: $e^{-ikx}$ in the forward transform (so positive-$k$ modes have positive-phase speed to the right). Engineering convention: $e^{+ikx}$. The sign flips the transform of $f'(x)$: under physics convention $\widetilde{f'} = ik\tilde f$; under engineering convention $\widetilde{f'} = -ik\tilde f$. This matters when computing momentum-space representations of derivatives.

**The delta is defined by integration, not by a picture.** $\delta(x)$ is not a "very tall, very thin spike." It is an object defined by $\int\delta(x-x_0)f(x)\,dx = f(x_0)$. Multiplying two deltas together, or asking for its value at a point, are undefined operations. The correct response to $\delta^2(x)$ is to note it has no meaning without a further integral structure.

**Bandwidth $\neq$ Robertson for energy and time.** The energy–time uncertainty $\Delta E\,\Delta t \sim \hbar$ is the Fourier bandwidth relation applied to time and energy, with $E = \hbar\omega$. It is **not** Robertson's theorem applied to $\hat H$ and $\hat t$, because $\hat t$ is not a self-adjoint operator in standard quantum mechanics. Students who try to apply Robertson to $[\hat H, \hat t] = i\hbar$ are importing a category error. The correct physical content is: a system that interacts for time $\Delta t$ cannot exchange energy more sharply than $\Delta E \sim \hbar/\Delta t$.

**Plancherel normalization factor.** In the asymmetric convention, $\int|f|^2\,dx = \frac{1}{2\pi}\int|\tilde f|^2\,dk$ — there is a $1/2\pi$ on the right. In the symmetric convention both integrals are equal. Students who check normalization of $\tilde\psi(p)$ using the wrong convention will find it off by a factor of $2\pi\hbar$.

**Completing the square with complex shifts.** The key step in the Gaussian transform — replacing $x$ with $x + ipa^2/\hbar$ — involves a complex shift of the integration variable. This is valid because $e^{-z^2/2a^2}$ is entire (analytic everywhere), so Cauchy's theorem guarantees the contour can be shifted. Students who are uncertain about this step should treat it as a formal manipulation and verify the result by checking that $|\tilde\psi(p)|^2$ integrates to 1.

---

## Quick practice

1. **Transform a top hat.** Compute the Fourier transform $\tilde f(k)$ of $f(x) = 1$ for $|x| < a/2$, zero otherwise. Identify the result as a sinc function, locate its first zero, and explain why narrowing $a$ (smaller slit) widens the diffraction pattern.

2. **Gaussian saturation.** For $\psi(x) = (\pi a^2)^{-1/4}e^{-x^2/2a^2}$, compute $\Delta x = \sqrt{\langle x^2\rangle - \langle x\rangle^2}$ directly from $|\psi(x)|^2$, and compute $\Delta p$ from $|\tilde\psi(p)|^2$. Verify $\Delta x\,\Delta p = \hbar/2$. Then state: if $a$ is halved, by what factor does $\Delta p$ change?

3. **Born scattering for a Yukawa potential.** The Yukawa potential is $V(r) = V_0 e^{-\mu r}/r$. Its 3D Fourier transform (spherical symmetry) is $\tilde V(q) = 4\pi V_0/(q^2 + \mu^2)$. (a) Write the Born differential cross-section $d\sigma/d\Omega \propto |f(\theta)|^2$ as a function of scattering angle $\theta$ using $q = 2k\sin(\theta/2)$. (b) Take $\mu \to 0$ to recover the Rutherford cross-section for Coulomb scattering. (c) Explain physically why large $q$ (wide-angle) scattering is suppressed for a screened potential.

---

## Go deeper

The full derivation — the $L\to\infty$ limit of the Fourier series, Plancherel's theorem, the convolution theorem (with the substitution proof), the bandwidth relation, the single-slit sinc, the double-slit by convolution, the Gaussian packet, and the Dirac delta — is in **Mathematics for Physics Vol 2, Ch 6**. The present module condenses those results and extends them to the three QM applications (wave packets, transitions, Born scattering) that the source chapter does not cover.

---

## References

- Joseph Fourier, *Théorie analytique de la chaleur* (Paris, 1822) — the founding work: heat-equation solutions as trigonometric series and, on the infinite line, the integral transform. The transform arose from a physics PDE. [verify]
- Michel Plancherel, "Contribution à l'étude de la représentation d'une fonction arbitraire par des intégrales définies," *Rendiconti del Circolo Matematico di Palermo* **30**, 289–335 (1910) — the Fourier transform is unitary on $L^2$: $\int|f|^2 = \int|\tilde f|^2$. [verify]
- Paul Dirac, *The Principles of Quantum Mechanics* (Oxford University Press, 1930) — introduced the delta function as the continuum analogue of the Kronecker delta, and the bra–ket formalism that makes $\langle x|p\rangle = e^{ipx/\hbar}/\sqrt{2\pi\hbar}$ the natural statement. [verify]
- Laurent Schwartz, *Théorie des distributions* (Hermann, Paris, 1950–51) — placed the Dirac delta and its derivatives on rigorous mathematical ground as distributions; the backstop for the module's operational treatment. [verify]
- Dennis Gabor, "Theory of communication," *Journal of the Institution of Electrical Engineers* **93** (Part III), 429–441 (1946) — the time–frequency bandwidth relation and the Gaussian as the minimum-uncertainty signal. [verify pagination]
- Max Born, "Zur Quantenmechanik der Stossvorgänge," *Zeitschrift für Physik* **37**, 863–867 (1926) — the Born approximation for scattering and its probabilistic interpretation. [verify]
- Werner Heisenberg, "Über den anschaulichen Inhalt der quantentheoretischen Kinematik und Mechanik," *Zeitschrift für Physik* **43**, 172–198 (1927) — the original uncertainty-relation paper; Heisenberg's argument was based on the Fourier width relation, not Robertson's commutator bound (which came later). [verify]
