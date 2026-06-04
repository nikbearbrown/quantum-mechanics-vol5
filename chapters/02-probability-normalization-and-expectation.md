# Module M-02 — Probability, Normalization, and Expectation Values

**When you need this:** QM Vol. I Ch. 3 introduces Born's rule and $\langle x \rangle$ on page one; Ch. I·9 defines $\Delta x$ and $\Delta p$ as standard deviations; Ch. IV·1 frames all of measurement theory as a probability distribution over outcomes.

---

## The refresher

### Probability density vs. probability

For a continuous random variable $X$, a **probability density function** (PDF) $f(x)$ satisfies:

$$f(x) \geq 0, \qquad \int_{-\infty}^{\infty} f(x)\,dx = 1,$$

and the probability that $X$ falls in the interval $[a,b]$ is

$$P(a \leq X \leq b) = \int_a^b f(x)\,dx.$$

$f(x)$ is **not** a probability. It is a density — it can exceed 1. Only the integral of $f$ over an interval is a probability, and that is bounded between 0 and 1. A single point has probability zero; only intervals have nonzero probability. This distinction is the foundational pitfall with Born's rule.

### Mean, expectation value, and variance

The **mean** (expectation value) of $X$ is the probability-weighted average:

$$\mu \equiv \langle X \rangle = \int_{-\infty}^{\infty} x\, f(x)\, dx.$$

The expectation of any function $g(X)$ follows the same weighting:

$$\langle g(X) \rangle = \int_{-\infty}^{\infty} g(x)\, f(x)\, dx.$$

Expectation is **linear**: $\langle aX + b \rangle = a\langle X\rangle + b$.

The **variance** measures spread as the mean squared deviation from the mean:

$$\sigma^2 = \langle (X - \mu)^2 \rangle = \langle X^2 \rangle - \langle X \rangle^2.$$

"The mean of the square minus the square of the mean" — expand $(X-\mu)^2 = X^2 - 2\mu X + \mu^2$, take the expectation, and the cross term gives $-2\mu\cdot\mu = -2\mu^2$, so $\sigma^2 = \langle X^2\rangle - \mu^2$. The **standard deviation** $\sigma = \sqrt{\sigma^2}$ has the same units as $X$ and is the natural measure of the width of the distribution.

For independent random variables, variances add: $\operatorname{Var}(X + Y) = \operatorname{Var}(X) + \operatorname{Var}(Y)$.

### Normalization as a constraint on $\psi$

The QM normalization condition is

$$\int_{-\infty}^{\infty} |\psi(x,t)|^2\, dx = 1.$$

This is an integral equation fixing the overall amplitude of the wave function. Solving the Schrödinger equation yields $\psi$ up to a free multiplicative constant $N$; normalization determines $|N|$. The time-dependent Schrödinger equation with a Hermitian Hamiltonian preserves normalization: if $\psi$ is normalized at $t=0$, it remains normalized for all $t$.

### The Gaussian integral (used everywhere)

The single most-used integral in normalization and expectation-value calculations:

$$\int_{-\infty}^{\infty} e^{-\alpha x^2}\, dx = \sqrt{\frac{\pi}{\alpha}}, \qquad \alpha > 0.$$

**Derivation.** Let $I = \int_{-\infty}^\infty e^{-\alpha x^2}dx$. Then

$$I^2 = \left(\int_{-\infty}^\infty e^{-\alpha x^2}dx\right)\!\left(\int_{-\infty}^\infty e^{-\alpha y^2}dy\right) = \int_{-\infty}^\infty\!\int_{-\infty}^\infty e^{-\alpha(x^2+y^2)}dx\,dy.$$

Switch to polar coordinates: $x = r\cos\theta$, $y = r\sin\theta$, $dx\,dy = r\,dr\,d\theta$, with $r$ running from $0$ to $\infty$ and $\theta$ from $0$ to $2\pi$:

$$I^2 = \int_0^{2\pi} d\theta \int_0^\infty e^{-\alpha r^2} r\,dr = 2\pi \cdot \frac{1}{2\alpha} = \frac{\pi}{\alpha}.$$

(The $r$-integral uses the substitution $u = \alpha r^2$, $du = 2\alpha r\,dr$: $\int_0^\infty e^{-\alpha r^2}r\,dr = \frac{1}{2\alpha}$.) Therefore $I = \sqrt{\pi/\alpha}$.

Two extensions follow by differentiating with respect to $\alpha$:

$$\int_{-\infty}^{\infty} x^2\, e^{-\alpha x^2}\, dx = \frac{\sqrt{\pi}}{2\alpha^{3/2}}, \qquad \int_{-\infty}^{\infty} x^4\, e^{-\alpha x^2}\, dx = \frac{3\sqrt{\pi}}{4\alpha^{5/2}}.$$

Odd-powered integrands ($x^{2n+1} e^{-\alpha x^2}$) vanish by symmetry.

### Dirac-delta normalization of plane waves

The plane wave $\psi_k(x) = e^{ikx}$ is not square-integrable in the usual sense — $\int |e^{ikx}|^2 dx = \int dx$ diverges. Free-particle states are handled by **Dirac-delta normalization**:

$$\int_{-\infty}^{\infty} e^{ik'x} e^{-ikx}\, dx = 2\pi\,\delta(k' - k),$$

or, with the symmetric convention $\psi_k(x) = e^{ikx}/\sqrt{2\pi}$:

$$\langle \psi_{k'} | \psi_k \rangle = \delta(k' - k).$$

The delta function $\delta(k'-k)$ replaces the Kronecker delta $\delta_{n'n}$ of discrete (bound) states. Physical observables are still well-defined as distributions over a wave packet: a packet $\psi(x) = \int \phi(k) e^{ikx} dk/\sqrt{2\pi}$ normalized in position space ($\int|\psi|^2 dx = 1$) has $\phi(k)$ normalized in momentum space ($\int|\phi|^2 dk = 1$) by Parseval's theorem.

### Worked example: Gaussian wave packet

A Gaussian wave function (not yet normalized) in position space:

$$\psi(x) = N e^{-x^2/(4\sigma^2)}.$$

**Step 1 — Normalize.** Use $|\psi|^2 = N^2 e^{-x^2/(2\sigma^2)}$:

$$\int_{-\infty}^{\infty} N^2 e^{-x^2/(2\sigma^2)}\, dx = N^2 \sqrt{\frac{\pi}{1/(2\sigma^2)}} = N^2 \sigma\sqrt{2\pi} = 1 \implies N = \frac{1}{(2\pi\sigma^2)^{1/4}}.$$

**Step 2 — Compute $\langle x \rangle$.** The integrand $x|\psi|^2 = N^2 x e^{-x^2/(2\sigma^2)}$ is odd; the integral over the symmetric domain vanishes: $\langle x \rangle = 0$.

**Step 3 — Compute $\langle x^2 \rangle$ and $\Delta x$.** Using $\int x^2 e^{-\alpha x^2}dx = \sqrt{\pi}/(2\alpha^{3/2})$ with $\alpha = 1/(2\sigma^2)$:

$$\langle x^2 \rangle = N^2 \cdot \frac{\sqrt{\pi}}{2(1/2\sigma^2)^{3/2}} = \sigma^2.$$

Therefore $\Delta x = \sqrt{\langle x^2\rangle - \langle x\rangle^2} = \sigma$.

The width $\sigma$ of the Gaussian is literally the standard deviation of the position distribution. The Gaussian saturates the uncertainty principle: the Gaussian is the **minimum-uncertainty state**, achieving $\Delta x\,\Delta p = \hbar/2$.

---

## In the quantum series

### Vol. I, Ch. 3 — Born's rule and the meaning of $|\psi|^2$

Born's rule states that $|\psi(x,t)|^2$ is the probability *density* for position. The entire structure of Ch. I·3 is the continuous-distribution formalism of this module applied to $|\psi|^2$:

- The probability of finding the particle in $[a,b]$ is $\int_a^b |\psi|^2 dx$ — a probability density integrated over an interval, not $|\psi(x)|^2$ evaluated at a point.
- The expectation value of position is $\langle x\rangle = \int x|\psi|^2 dx$ — the mean of the position distribution.
- Normalization $\int|\psi|^2 dx = 1$ is enforced as an initial condition; the Schrödinger equation guarantees it is preserved in time.

The complex modulus $|\psi|^2 = \psi^*\psi$ requires the complex-number tools of M-01. Without those, the Born rule cannot be applied.

### Vol. I, Ch. 9 — The uncertainty principle: $\Delta x$ and $\Delta p$ are standard deviations

The quantities $\Delta x$ and $\Delta p$ in the inequality

$$\Delta x \,\Delta p \geq \frac{\hbar}{2}$$

are the **standard deviations** of the position and momentum probability distributions in a given quantum state:

$$(\Delta x)^2 = \langle x^2\rangle - \langle x\rangle^2, \qquad (\Delta p)^2 = \langle p^2\rangle - \langle p\rangle^2.$$

This is $\sigma^2 = \langle X^2\rangle - \langle X\rangle^2$ from this module, applied twice. The uncertainty principle is a theorem about Fourier transform pairs (position and momentum wave functions are related by a Fourier transform — see M-06); the Gaussian saturates it because the Fourier transform of a Gaussian is a Gaussian, as computed in the worked example above.

The $\Delta$ notation in QM carries two distinct meanings: finite differences (e.g., $\Delta E = E_2 - E_1$) and standard deviations (as above). In the uncertainty principle, $\Delta$ always means standard deviation.

### Vol. IV, Ch. 1 — Measurement theory: expectation values of observables

The expectation value of a general observable $\hat{A}$ in state $\psi$ is

$$\langle \hat{A}\rangle = \langle\psi|\hat{A}|\psi\rangle = \int \psi^*(x)\,\hat{A}\,\psi(x)\, dx.$$

This is the mean of the probability distribution over measurement outcomes, with the distribution given by the Born rule generalized to eigenstates of $\hat{A}$. The squared uncertainty is

$$(\Delta A)^2 = \langle \hat{A}^2\rangle - \langle \hat{A}\rangle^2,$$

exactly the variance formula $\sigma^2 = \langle X^2\rangle - \mu^2$ from this module. The completeness of the eigenstates of $\hat{A}$ ensures that the distribution over outcomes is a proper probability distribution (non-negative, summing to 1). The formalism of observable measurement in QM is continuous-distribution probability theory in function-space clothing.

---

## Conventions and pitfalls

**$|\psi(x)|^2$ is a density, not a probability.** The probability that the particle is found at position $x$ is zero — no probability is assigned to a single point for a continuous variable. The probability that the particle is found between $x$ and $x + dx$ is $|\psi(x)|^2\,dx$. Normalizing by setting $|\psi(x_0)|^2 = 1$ at a special point is wrong; normalization requires an integral equal to 1.

**$\langle x\rangle$ is the mean, not the most probable $x$.** For a symmetric distribution the mean and the mode (peak) coincide. For asymmetric wave functions they differ. The expectation value is the probability-weighted average, not the location where $|\psi|^2$ peaks.

**$\Delta$ means standard deviation in the uncertainty principle.** In the same QM text, $\Delta$ also appears as a finite difference ($\Delta E$). Context distinguishes the two uses; the uncertainty principle $\Delta$ always means $\sqrt{\langle X^2\rangle - \langle X\rangle^2}$.

**Plane waves require delta-function normalization.** Free-particle plane waves $e^{ikx}$ are not square-integrable and cannot be normalized with a finite constant. They are handled by Dirac-delta normalization $\langle k'|k\rangle = \delta(k'-k)$, or confined to a box of length $L$ (which gives a discrete set of $k$-values and standard $L^2$ normalization). Physical observables involve wave packets, not individual plane waves.

**Normalization is preserved by the Schrödinger equation.** If $\psi$ is normalized at $t=0$ and the Hamiltonian is Hermitian ($\hat{H}^\dagger = \hat{H}$), then $\int|\psi|^2 dx = 1$ for all $t$. Approximations or truncations can violate this; checking normalization after approximation is a useful diagnostic.

---

## Quick practice

1. Show that $f(x) = \frac{1}{\pi(1+x^2)}$ (the Cauchy–Lorentz distribution) is normalized. Then attempt to compute the mean $\langle x\rangle$; what goes wrong, and what does this tell you about the expectation value?

2. For the wave function $\psi(x) = N e^{-\alpha|x|}$ (with $\alpha > 0$), find the normalization constant $N$, and compute $\langle x\rangle$ and $\langle x^2\rangle$ by explicit integration. What is $\Delta x$?

3. A two-state superposition has $\psi = \frac{1}{\sqrt{2}}(\psi_1 + \psi_2)$, where $\langle\psi_1|\psi_1\rangle = \langle\psi_2|\psi_2\rangle = 1$ and $\langle\psi_1|\psi_2\rangle = 0$. Show that $\psi$ is normalized. Then, if $\hat{H}\psi_n = E_n\psi_n$, compute $\langle\hat{H}\rangle$ and $(\Delta H)^2$. What does the variance tell you about the energy of this state?

---

## Go deeper

The derivation here condenses *Mathematics for Physics*, Vol. 2, Ch. 8, "Probability and Statistics for Physics." That chapter derives the Gaussian as the large-$N$ limit of the binomial (de Moivre–Laplace theorem), covers the Poisson distribution, and derives the law of propagation of uncertainty. The integral techniques underlying normalization and expectation integrals — substitution, integration by parts, and setting up integrals over continuous distributions — are in *Mathematics for Physics*, Vol. 1, Chs. 8 and 9.

For the QM application, see Griffiths, *Introduction to Quantum Mechanics*, 3rd ed., Sec. 1.2–1.5 (the statistical interpretation and expectation values) and Shankar, *Principles of Quantum Mechanics*, Ch. 4 (postulates of QM and measurement). Cohen-Tannoudji, *Quantum Mechanics*, Vol. 1, Ch. III discusses the physical interpretation of $|\psi|^2$ carefully.

---

## References

- A. de Moivre, *Approximatio ad Summam Terminorum Binomii $(a+b)^n$ in Seriem expansi* (1733); *The Doctrine of Chances*, 2nd ed. (1738) — the Gaussian as the large-$N$ limit of the binomial. [verify]
- P.-S. Laplace, *Théorie analytique des probabilités* (1812) — broad statement of the central limit theorem.
- M. Born, "Zur Quantenmechanik der Stoßvorgänge," *Zeitschrift für Physik* **37**, 863 (1926) — the probabilistic interpretation of $|\psi|^2$. [verify]
- D. J. Griffiths, *Introduction to Quantum Mechanics*, 3rd ed. (Cambridge, 2018), Secs. 1.2–1.6.
- R. Shankar, *Principles of Quantum Mechanics*, 2nd ed. (Plenum, 1994), Ch. 4.
- C. Cohen-Tannoudji, B. Diu, F. Laloë, *Quantum Mechanics*, Vol. 1 (Wiley, 1977), Ch. III.
- *Mathematics for Physics*, Vol. 2, Ch. 8 (primary source for this module); Vol. 1, Chs. 8–9 (integral mechanics).
