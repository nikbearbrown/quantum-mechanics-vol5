# Module M-04 — Series Expansions and Approximation

**Refresher for QM chapters:** III·1 (time-independent perturbation theory), III·4 (WKB approximation)

**Condensed from:** Mathematics for Physics Vol 1, Ch 13

---

## When you need this

Open perturbation theory (III·1) and you will find energies written as $E = E^{(0)} + \lambda E^{(1)} + \lambda^2 E^{(2)} + \cdots$. That is a Taylor series. Open the WKB chapter (III·4) and you will find an expansion in powers of $\hbar$. That is an asymptotic series. Both methods live or die by the same question: is my small parameter actually small, and what do I lose by stopping at second order? This module gives you the machinery to answer that question.

---

## The refresher

### The Taylor series in one formula

Any sufficiently smooth function $f$ can be reconstructed near a point $a$ from its derivatives there:

$$f(x) = \sum_{n=0}^{\infty} \frac{f^{(n)}(a)}{n!}\,(x - a)^n.$$

When $a = 0$ this is the **Maclaurin series**. The coefficients $f^{(n)}(0)/n!$ are forced — they are the unique polynomial that matches every derivative of $f$ at the expansion point. The factorial $n!$ appears because differentiating $x^n$ exactly $n$ times brings down $n \cdot (n-1) \cdots 1$.

### The three series everything rests on

All three converge for every real $x$:

$$e^x = 1 + x + \frac{x^2}{2!} + \frac{x^3}{3!} + \cdots$$

$$\sin x = x - \frac{x^3}{3!} + \frac{x^5}{5!} - \frac{x^7}{7!} + \cdots \quad \text{(odd powers, alternating signs)}$$

$$\cos x = 1 - \frac{x^2}{2!} + \frac{x^4}{4!} - \frac{x^6}{6!} + \cdots \quad \text{(even powers, alternating signs)}$$

These are not independent: Euler's formula $e^{i\theta} = \cos\theta + i\sin\theta$ (M-01) is proved by substituting $x = i\theta$ into the exponential series and sorting by real and imaginary parts.

### Small-parameter expansions: truncate and bound the error

Keep the first few terms and call it an approximation. The first term you discard estimates your error.

**Small-angle:** From the sine series, $\sin\theta \approx \theta$. The next term is $-\theta^3/6$, so the relative error is approximately $\theta^2/6$ (in radians). At $15^\circ = 0.262$ rad this is about 1%; at $5^\circ$ it is 0.1%. The approximation is not a trick — it is the series truncated after one term, with a computable error.

From the cosine series: $\cos\theta \approx 1 - \theta^2/2$.

**Binomial approximation:** For $|x| \ll 1$ and any real $n$:

$$(1 + x)^n \approx 1 + nx.$$

Special cases: $\sqrt{1+x} \approx 1 + x/2$; $(1-x)^{-1} \approx 1 + x$. This collapses relativistic corrections, perturbative denominators, and most "keep the leading term" calculations in QM.

### Every smooth potential near a minimum is a harmonic oscillator

This is the deepest use of Taylor expansion in all of physics. Expand any potential $V(x)$ about its minimum at $x_0$:

$$V(x) = V(x_0) + \underbrace{V'(x_0)}_{=\,0}\,(x-x_0) + \tfrac{1}{2}V''(x_0)\,(x-x_0)^2 + \cdots$$

The linear term vanishes at a minimum. Dropping cubic and higher terms (valid for small displacements) gives a harmonic potential with effective spring constant $k_\text{eff} = V''(x_0)$ and oscillation frequency $\omega = \sqrt{V''(x_0)/m}$. Every molecular bond, every lattice site, every potential well looks like a quantum harmonic oscillator to leading order — which is exactly why QHO perturbation theory is the universal reference system.

### Convergence: the practical picture

Every power series has a radius of convergence. Inside it, adding terms homes in on the function; outside, the partial sums diverge. The series for $e^x$, $\sin x$, and $\cos x$ converge everywhere. The geometric series $1/(1-x) = 1 + x + x^2 + \cdots$ converges only for $|x| < 1$. A truncated series is reliable near the expansion point and progressively untrustworthy farther away — which is precisely why "small angle" must be small.

### Worked example: second-order period correction for the pendulum

The pendulum equation $\ddot\theta = -(g/L)\sin\theta$ is nonlinear and has no solution in elementary functions. Replace $\sin\theta$ by its one-term Taylor series to get $\ddot\theta \approx -(g/L)\theta$, a harmonic oscillator with period $T_0 = 2\pi\sqrt{L/g}$. Carrying the cubic correction $-\theta^3/6$ through a careful perturbative expansion of the motion yields the leading amplitude-dependent correction [verify]:

$$T \approx T_0\!\left(1 + \frac{\theta_0^2}{16}\right).$$

The structure is exactly what the chapter predicts: the correction is order $\theta_0^2$, the same as the squared-angle error we estimated from the dropped term. For $\theta_0 = 0.5$ rad the correction is 1.6% — small but measurable, and a direct experimental confirmation that "small angle" was a truncation all along.

---

## In the quantum series

### Perturbation theory is a Taylor expansion in the coupling

Time-independent perturbation theory (III·1) begins with a Hamiltonian $\hat H(\lambda) = \hat H_0 + \lambda \hat H'$ where $\lambda$ is a small dimensionless coupling. The exact energy eigenvalue $E_n(\lambda)$ is a smooth function of $\lambda$, so it has a Taylor expansion:

$$E_n(\lambda) = E_n^{(0)} + \lambda E_n^{(1)} + \lambda^2 E_n^{(2)} + \cdots$$

The zeroth-order term $E_n^{(0)}$ is the unperturbed energy. The first-order correction is

$$E_n^{(1)} = \langle n^{(0)} | \hat H' | n^{(0)} \rangle,$$

which is the "first derivative" of $E_n$ with respect to $\lambda$ evaluated at $\lambda = 0$ (this follows from the Hellmann–Feynman theorem — the first derivative of the energy is the expectation value of $\partial\hat H/\partial\lambda$). The second-order correction $E_n^{(2)} = \sum_{m \neq n} |\langle m^{(0)}|\hat H'|n^{(0)}\rangle|^2 / (E_n^{(0)} - E_m^{(0)})$ is the coefficient of $\lambda^2$.

Recognizing this as a Taylor series immediately tells you when the method is valid: the expansion converges when $\lambda$ is small, which means concretely that the ratio of the perturbation matrix element to the unperturbed level spacing must be much less than 1,

$$\left|\frac{\langle m^{(0)}|\hat H'|n^{(0)}\rangle}{E_n^{(0)} - E_m^{(0)}}\right| \ll 1 \quad \text{for all } m \neq n.$$

This is the convergence check of the underlying series. Degenerate perturbation theory is required precisely when a denominator vanishes — the series hits the boundary of its radius of convergence, and you must reorganize the expansion before truncating.

The eigenstates themselves are also expanded in powers of $\lambda$:

$$|n\rangle = |n^{(0)}\rangle + \lambda |n^{(1)}\rangle + \lambda^2 |n^{(2)}\rangle + \cdots$$

with $|n^{(1)}\rangle = \sum_{m \neq n} \frac{\langle m^{(0)}|\hat H'|n^{(0)}\rangle}{E_n^{(0)} - E_m^{(0)}} |m^{(0)}\rangle$. Every formula in III·1 is a Taylor coefficient. Knowing this converts the perturbation expansion from a list of results to memorize into a structure to understand.

### WKB is an asymptotic series in $\hbar$

The WKB approximation (III·4) is the leading term of a systematic expansion of the wavefunction in powers of $\hbar$. Write $\psi(x) = e^{iS(x)/\hbar}$ and substitute into the Schrödinger equation. Expanding $S(x) = S_0(x) + \hbar S_1(x) + \hbar^2 S_2(x) + \cdots$ gives equations for each order. The leading-order result (keeping only $S_0$) yields the WKB wavefunction

$$\psi(x) \approx \frac{A}{\sqrt{p(x)}}\,e^{\pm (i/\hbar)\int p(x)\,dx}, \qquad p(x) = \sqrt{2m[E - V(x)]},$$

in classically allowed regions where $p(x) > 0$, and an exponentially decaying form in forbidden regions. The prefactor $1/\sqrt{p}$ comes from the $\hbar S_1$ correction.

The expansion breaks down near **turning points** where $p(x) \to 0$ — exactly where the "small parameter" $\hbar|p'/p^2|$ ceases to be small (the local de Broglie wavelength grows to match the scale over which $p$ varies). This is a radius-of-convergence failure: the series is asymptotic in $\hbar$, meaning it formally diverges for any fixed $\hbar > 0$ if you include enough terms, yet the first few terms give excellent approximations for small $\hbar$. Connection formulas across turning points are required precisely because the WKB series breaks there.

The WKB quantization condition $\oint p\,dx = \left(n + \tfrac{1}{2}\right)h$ (where the integral is over a complete classical orbit) is recovered by matching the oscillatory and evanescent solutions — a direct application of Taylor-expansion logic: recognize the local ODE as approximately constant-coefficient in a neighborhood of each point, then patch the regions together.

---

## Conventions and pitfalls

**Radians only.** The series $\sin x = x - x^3/6 + \cdots$ holds only when $x$ is in radians. The small-angle approximation $\sin\theta \approx \theta$ is false in degrees. In QM, phase angles in wavefunctions and perturbation parameters are always dimensionless; this is not usually a trap, but it bites when converting numerical results.

**The expansion point matters.** Perturbation theory expands about $\lambda = 0$ (no perturbation). WKB expands the potential about each point locally. Choosing the wrong center invalidates the approximation entirely, even when the truncation order is correct.

**Asymptotic vs. convergent.** The WKB series in $\hbar$ is asymptotic — it diverges if you keep all terms, yet truncated at the right order it is highly accurate. This is different from the Taylor series of $\sin x$, which converges everywhere. Vol. III flags this for WKB; the distinction matters when you wonder whether "adding more terms" always helps.

**Degeneracy is a convergence failure.** When two unperturbed levels are nearly degenerate, the denominator $E_n^{(0)} - E_m^{(0)}$ is small, and the ratio $|\langle m|\hat H'|n\rangle|/(E_n^{(0)} - E_m^{(0)})$ can be large even for small $\hat H'$. The series has left its radius of convergence. Degenerate perturbation theory reorganizes the expansion so that it starts from the right zeroth-order basis — analogous to expanding about the correct point $a$ rather than a distant one.

**"Higher-order corrections" = next Taylor coefficient.** Students in III·1 often hear "second-order correction" without connecting it to $\lambda^2$ in a power series. Writing $E(\lambda)$ explicitly as a polynomial and asking what the $\lambda^2$ coefficient looks like demystifies the sum-over-intermediate-states formula: it is the second derivative of $E$ with respect to $\lambda$.

---

## Quick practice

1. **Binomial in QM.** The relativistic energy is $E = mc^2/\sqrt{1 - v^2/c^2}$. Use the binomial approximation $(1+x)^n \approx 1 + nx$ with $x = -v^2/c^2$ and $n = -1/2$ to recover the Newtonian kinetic energy $\frac{1}{2}mv^2$ as the leading correction. What is the next term, and when does it matter?

2. **Perturbation validity check.** A hydrogen atom is placed in a weak electric field $\mathcal{E}$ (the Stark effect). The perturbation is $\hat H' = e\mathcal{E}z$. State the condition on $\mathcal{E}$ for first-order perturbation theory to be valid, in terms of the matrix element $\langle n\ell m|z|n'\ell' m'\rangle$ and the energy spacing. What goes wrong at exact degeneracy?

3. **Taylor as a tool.** The potential for a diatomic molecule near its equilibrium separation $r_0$ is the Morse potential $V(r) = D_e\left(1 - e^{-\alpha(r-r_0)}\right)^2$. Expand $V$ to second order in $u = r - r_0$ and identify the effective spring constant $k_\text{eff} = D_e\alpha^2 \cdot 2$, hence the harmonic oscillation frequency $\omega = \alpha\sqrt{2D_e/m}$. Sketch the Morse well and indicate where the harmonic approximation fails.

---

## Go deeper

The full derivation — including the systematic coefficient construction by repeated differentiation, the small-angle approximation with its precise error bound, the binomial theorem for real exponents, the radius of convergence, and three worked examples (linearized pendulum, period correction, every minimum is a spring) — is in **Mathematics for Physics Vol 1, Ch 13**. The present module condenses the formulas and pivots directly to the QM applications.

---

## References

- Mādhava of Sangamagrāma (c. 1340–1425) and the Kerala school — power-series expansions of sine, cosine, and arctangent with error terms; transmitted through Nilakantha's *Tantrasangraha* and the *Yuktibhāṣā*, roughly 250 years before European formulations. [verify]
- Brook Taylor, *Methodus Incrementorum Directa et Inversa* (1715) — the general Taylor expansion. [verify]
- Colin Maclaurin, *A Treatise of Fluxions* (1742) — the $a = 0$ special case. [verify]
- Isaac Newton, generalized binomial theorem (c. 1665; *Epistola prior*, 1676) — $(1+x)^n$ for real $n$. [verify]
- Joseph-Louis Lagrange, *Théorie des fonctions analytiques* (1797) — the remainder term that makes truncation rigorous. [verify]
- E. Schrödinger, "Quantisierung als Eigenwertproblem" (Parts I–IV), *Annalen der Physik* **79**, 361–376; 489–527; **80**, 437–490; **81**, 109–139 (1926) — original Schrödinger equation; perturbation expansion appears in Part III. [verify]
- G. Wentzel, "Eine Verallgemeinerung der Quantenbedingungen für die Zwecke der Wellenmechanik," *Zeitschrift für Physik* **38**, 518–529 (1926); H. A. Kramers, *ibid.* **39**, 828–840 (1926); L. Brillouin, *Comptes Rendus* **183**, 24–26 (1926) — the three independent WKB papers published in the same year. [verify]
