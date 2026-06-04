# Module M-01 — Complex Numbers and the Complex Exponential

**When you need this:** QM Vol. I Chs. 3 and 8 use complex arithmetic on every page; Ch. II·7 (spin) requires complex two-component vectors and phase factors under rotation.

---

## The refresher

### Complex arithmetic

A complex number is a pair of real numbers packaged as $z = a + bi$, where $i^2 = -1$. The real part is $\operatorname{Re}(z) = a$; the imaginary part is $\operatorname{Im}(z) = b$. The **complex conjugate** reverses the sign of the imaginary part: $z^* = a - bi$ (physicists write $z^*$; mathematicians often write $\bar{z}$). The **modulus** (or magnitude) is

$$|z| = \sqrt{z z^*} = \sqrt{a^2 + b^2} \geq 0.$$

Addition is componentwise. Multiplication uses ordinary algebra with the substitution $i^2 = -1$ wherever it appears:

$$(a + bi)(c + di) = (ac - bd) + (ad + bc)i.$$

Division: multiply numerator and denominator by the conjugate of the denominator,

$$\frac{1}{c + di} = \frac{c - di}{c^2 + d^2},$$

turning a complex denominator into a real one. That is the only genuinely new arithmetic move; everything else is ordinary algebra.

### Polar form

Plot $z$ as a point $(a, b)$ in the complex plane. The number is equally described by its distance from the origin and its angle from the positive real axis:

$$r = |z|, \qquad \theta = \operatorname{atan2}(b,\, a),$$

so that $z = r(\cos\theta + i\sin\theta)$. Multiplication in polar form is clean: lengths multiply and angles add,

$$z_1 z_2 = r_1 r_2 \, e^{i(\theta_1 + \theta_2)},$$

which is proved directly once Euler's formula is in hand.

### Euler's formula

Substitute $x = i\theta$ into the Maclaurin series for $e^x$ (see Module M-04 for the series machinery) and sort even and odd powers using $i^2 = -1,\ i^3 = -i,\ i^4 = 1, \ldots$:

$$e^{i\theta} = 1 + i\theta - \frac{\theta^2}{2!} - i\frac{\theta^3}{3!} + \frac{\theta^4}{4!} + \cdots
= \underbrace{\left(1 - \frac{\theta^2}{2!} + \frac{\theta^4}{4!} - \cdots\right)}_{\cos\theta}
+ i\underbrace{\left(\theta - \frac{\theta^3}{3!} + \frac{\theta^5}{5!} - \cdots\right)}_{\sin\theta}.$$

Therefore

$$\boxed{e^{i\theta} = \cos\theta + i\sin\theta.}$$

This is Euler's formula — derived, not announced. Compact polar form follows immediately: any complex number is $z = re^{i\theta}$. The unit circle is the set of all $e^{i\theta}$ (modulus 1 for every real $\theta$).

Key corollaries:
- $\cos\theta = \operatorname{Re}(e^{i\theta})$, $\sin\theta = \operatorname{Im}(e^{i\theta})$
- $e^{i\pi} + 1 = 0$ (a special case, not the main point)
- $|e^{i\theta}| = 1$ for all real $\theta$

### Complex exponentials encode oscillation and decay together

A complex exponent $r = -\gamma + i\omega$ gives

$$e^{rt} = e^{-\gamma t}(\cos\omega t + i\sin\omega t).$$

The real part of the exponent governs the decay envelope; the imaginary part is the angular frequency of oscillation. The two phenomena — damping and oscillation — are a single complex exponential, not two separate functions. A **complex amplitude** $\tilde{A} = Ae^{i\phi}$ packages magnitude $A$ and phase $\phi$ into one number, so that a general oscillation is

$$A\cos(\omega t + \phi) = \operatorname{Re}(\tilde{A}\,e^{i\omega t}).$$

Adding two oscillations of the same frequency reduces to adding two complex numbers — one vector sum in the plane — instead of a trig-identity page.

### Worked example: phasor addition

Add $x_1 = 3\cos(\omega t)$ and $x_2 = 4\cos(\omega t + 90^\circ)$.

Complex amplitudes: $\tilde{A}_1 = 3$, $\tilde{A}_2 = 4e^{i\pi/2} = 4i$.

Sum: $\tilde{A} = 3 + 4i$.

$$|\tilde{A}| = \sqrt{3^2 + 4^2} = 5, \qquad \phi = \arctan(4/3) \approx 53.1^\circ.$$

Result: $x_1 + x_2 = 5\cos(\omega t + 53.1^\circ)$. The amplitude and phase come from one right-triangle calculation, not from expanding trigonometric angle-sum formulas.

---

## In the quantum series

### Vol. I, Ch. 3 — The wave function: $\psi$ is intrinsically complex

The Schrödinger equation contains an explicit $i$ on the left-hand side:

$$i\hbar \frac{\partial \psi}{\partial t} = \hat{H}\psi.$$

This means $\psi$ cannot be real — a real function cannot satisfy an equation that requires its time derivative to equal an imaginary multiple of itself. There is no "take the real part at the end" step. Both $\operatorname{Re}(\psi)$ and $\operatorname{Im}(\psi)$ are physically active.

The time-dependent factor for a stationary state of energy $E$ is $e^{-iEt/\hbar}$ — a phasor rotating at angular rate $E/\hbar$ in the complex plane. Because $|e^{-iEt/\hbar}| = 1$, the probability density $|\psi(x,t)|^2 = |\psi(x)|^2$ is time-independent for a stationary state, even though $\psi$ itself is rotating. This is why stationary states have definite energy but still oscillate in the complex plane.

Born's rule extracts the probability density as $|\psi|^2 = \psi^*\psi$. Computing $|\psi|^2$ for a sum $\psi = \psi_1 + \psi_2$ of two components gives

$$|\psi_1 + \psi_2|^2 = |\psi_1|^2 + |\psi_2|^2 + 2\operatorname{Re}(\psi_1^*\psi_2).$$

The cross-term $2\operatorname{Re}(\psi_1^*\psi_2)$ is the **interference term** — it is real and nonzero precisely because $\psi$ is complex. Interference in a double-slit experiment is this cross-term made visible; it vanishes only when the relative phase is $\pm 90^\circ$.

### Vol. I, Ch. 8 — Wave packets: superposing complex exponentials

A free-particle wave packet is a superposition of plane waves, each with a definite wave number $k$:

$$\psi(x,t) = \int_{-\infty}^{\infty} \phi(k)\, e^{i(kx - \omega(k)t)}\, dk.$$

Every term $e^{i(kx-\omega t)}$ is a complex exponential in both $x$ and $t$. The **envelope** of the packet travels at the group velocity $v_g = d\omega/dk$, which emerges from the constructive interference of neighboring $k$-values — a Fourier argument that is stated entirely in complex-exponential language. Phase velocity $v_\phi = \omega/k$ and group velocity $v_g$ are distinct because different $k$-components rotate at different rates; the distinction is invisible without complex exponentials.

To see the group velocity emerge, expand $\omega(k)$ around the central wave number $k_0$: $\omega(k) \approx \omega_0 + (d\omega/dk)_{k_0}(k - k_0)$. Substituting into the packet integral and factoring out $e^{i(k_0 x - \omega_0 t)}$, the remaining integral is $\phi(k)$ evaluated at $k - k_0$ multiplied by $e^{i(k-k_0)(x - v_g t)}$ — a shape function that translates rigidly at speed $v_g = (d\omega/dk)_{k_0}$. The whole argument is a manipulation of complex exponential integrals; there is no real-valued version of this calculation.

### Vol. II, Ch. 7 — Spin: phase factors and spinors

A spin-$\frac{1}{2}$ state is a two-component complex vector (a **spinor**). A rotation by angle $\phi$ about the $z$-axis acts on a spinor with the operator

$$R_z(\phi) = \begin{pmatrix} e^{-i\phi/2} & 0 \\ 0 & e^{i\phi/2} \end{pmatrix}.$$

Because the phases are $e^{\pm i\phi/2}$, a full $2\pi$ rotation gives $e^{\pm i\pi} = -1$ — the spinor changes sign. A physical rotation by $360^\circ$ does not return a spin-$\frac{1}{2}$ spinor to its original value; it takes $720^\circ$. The argument that modulus is 1 ($|e^{i\phi/2}|=1$) while the argument changes by $\pi$ under $\phi \to \phi + 2\pi$ is purely a statement about complex exponentials and the ambiguity of the argument modulo $2\pi$.

---

## Conventions and pitfalls

**Physics vs. engineering time convention.** Physicists write $e^{-i\omega t}$ for a positive-frequency mode (energy eigenstate has $e^{-iEt/\hbar}$). Engineers often write $e^{+j\omega t}$. The QM series uses $e^{-i\omega t}$ throughout. A formula copied from an engineering source may have its phase conjugated — verify the sign before importing it.

**$\psi$ is not the real part of anything.** In classical oscillation problems the standard procedure is: complexify, compute, then take $\operatorname{Re}(\cdot)$ at the end. In QM that final step does not exist. $\psi$ is genuinely complex; discarding $\operatorname{Im}(\psi)$ loses physical information (interference, Berry phases, the Aharonov–Bohm effect).

**Modulus squared, not modulus.** The probability density is $|\psi|^2$, not $|\psi|$. Normalization is $\int |\psi|^2 dx = 1$. Setting $|\psi| = 1$ at some special point is a common first error.

**Overall phase vs. relative phase.** The global phase of a state, $e^{i\alpha}|\psi\rangle$, is unobservable: $|e^{i\alpha}\psi|^2 = |\psi|^2$. But the relative phase between two components of a superposition is observable and produces interference. Concluding "phase doesn't matter" from the former is exactly wrong for the latter.

**Argument is defined modulo $2\pi$.** The argument of $e^{i\phi}$ is not unique. For spinors, the $2\pi$ ambiguity is physically meaningful: $e^{i(\phi + 2\pi)/2} = -e^{i\phi/2}$. The branch of the argument matters in spin-$\frac{1}{2}$ physics.

---

## Quick practice

1. Compute $(2 + 3i)(1 - i)$ and $\dfrac{1+i}{2-i}$, expressing each in the form $a+bi$. Find the modulus and argument of $1+i$.

2. Using the cycle of powers of $i$ ($i^0=1, i^1=i, i^2=-1, i^3=-i, i^4=1, \ldots$), derive $e^{i\pi/2}$ and $e^{i\pi}$ from the series definition $e^{i\theta} = \sum_{n=0}^\infty (i\theta)^n/n!$, and verify each result geometrically on the unit circle.

3. A superposition of two energy eigenstates has $\psi(x,t) = \psi_1(x)e^{-iE_1 t/\hbar} + \psi_2(x)e^{-iE_2 t/\hbar}$. Show that $|\psi|^2$ oscillates in time at frequency $(E_2 - E_1)/h$. Why does $|\psi|^2$ for a *single* eigenstate not oscillate?

---

## Go deeper

The derivation here condenses *Mathematics for Physics*, Vol. 1, Ch. 12, "Complex Numbers and Exponentials." That chapter works through three detailed examples (Bombelli's cubic, phasor addition, the underdamped oscillator) and connects complex roots of the characteristic equation to the decaying-oscillation solution of Ch. 11.

For the QM application of complex exponentials to operators, see Shankar, *Principles of Quantum Mechanics*, Ch. 1 (mathematical introduction) and Ch. 4 (time evolution operator $e^{-i\hat{H}t/\hbar}$). Cohen-Tannoudji, *Quantum Mechanics*, Vol. 1, Complement $B_{\text{I}}$ discusses the wave function and its complex character explicitly.

---

## References

- Leonhard Euler, *Introductio in analysin infinitorum* (1748), Book I, Chs. 7–8 (Euler Archive E101) — $e^{i\theta} = \cos\theta + i\sin\theta$ derived from the power series. [verify]
- Rafael Bombelli, *L'Algebra* (1572) — complex numbers as intermediates in real algebra (cubic $x^3 = 15x+4$). [verify]
- Caspar Wessel (1799) and Jean-Robert Argand (1806) — geometric (complex-plane) interpretation; term "complex number" legitimized by Gauss (1831). [verify]
- R. Shankar, *Principles of Quantum Mechanics*, 2nd ed. (Plenum, 1994), Ch. 1 and Ch. 4.
- C. Cohen-Tannoudji, B. Diu, F. Laloë, *Quantum Mechanics*, Vol. 1 (Wiley, 1977), Ch. I and Complement $B_{\text{I}}$.
- *Mathematics for Physics*, Vol. 1, Ch. 12 (source chapter for this module).
