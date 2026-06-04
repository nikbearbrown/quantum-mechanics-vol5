# Module M-18 — Trigonometry, Waves, and the Harmonic Model

**Refresher for QM chapters:** I·2

**Condensed from:** *Mathematics for Physics* Vol 1, Ch 3

---

## When you need this

Read this module before **I·2** (matter waves). The sinusoidal wave $\psi(x,t) = Ae^{i(kx-\omega t)}$ appears in the first pages of that chapter, and every result — de Broglie's hypothesis, the double-slit interference pattern, the distinction between phase and group velocity — is a direct application of the wave model. Without fluency with $k$, $\omega$, phase, and the superposition formula, matter waves are a notational exercise rather than a physical picture.

This module also builds the small-angle approximation ($\sin\theta \approx \theta$ for small $\theta$ in radians) that appears repeatedly in interference geometry throughout the series.

---

## The refresher

### The three ratios and the central rule

In a right triangle, for an acute angle $\theta$:

$$\sin\theta = \frac{\text{opposite}}{\text{hypotenuse}}, \quad \cos\theta = \frac{\text{adjacent}}{\text{hypotenuse}}, \quad \tan\theta = \frac{\text{opposite}}{\text{adjacent}}.$$

These are dimensionless — pure numbers, depending only on the angle, not the triangle's size (similar triangles have proportional sides). The component rule follows immediately: a vector of magnitude $F$ at angle $\theta$ measured from a chosen axis has

$$F_\text{along} = F\cos\theta, \qquad F_\perp = F\sin\theta.$$

The *along* component carries cosine; the *perpendicular* component carries sine. Check with extremes: at $\theta = 0$, $F_\text{along} = F$ and $F_\perp = 0$ (the vector is purely along the axis). Pythagorean identity: $\cos^2\theta + \sin^2\theta = 1$ reconstructs the magnitude.

### The unit circle and the radian

For any angle $\theta$ (measured counterclockwise from the positive $x$-axis), the point on the unit circle is $(\cos\theta, \sin\theta)$. This extends the functions to all angles and makes periodicity manifest: period $2\pi$.

The **radian** measures angle by arc length on the unit circle: one radian subtends an arc equal to the radius. A full circle is $2\pi$ radians. Radians are dimensionless (arc length divided by radius). The calculus identities

$$\frac{d}{d\theta}\sin\theta = \cos\theta, \qquad \frac{d}{d\theta}\cos\theta = -\sin\theta$$

hold *only in radians*. The reason: these identities depend on the limit $\lim_{\theta\to 0}(\sin\theta)/\theta = 1$, which equals 1 only when $\theta$ is in radians (in degrees the limit is $\pi/180$). Never feed degrees into a wave formula or a differential equation.

### Key identities for wave physics

The addition formulas are the engine of interference calculations:

$$\sin(\alpha \pm \beta) = \sin\alpha\cos\beta \pm \cos\alpha\sin\beta$$
$$\cos(\alpha \pm \beta) = \cos\alpha\cos\beta \mp \sin\alpha\sin\beta$$

Double-angle forms ($\beta = \alpha$): $\sin 2\alpha = 2\sin\alpha\cos\alpha$; $\cos 2\alpha = 1 - 2\sin^2\alpha$.

The sum-to-product identity used in the interference derivation:

$$\cos A + \cos B = 2\cos\!\left(\frac{A+B}{2}\right)\cos\!\left(\frac{A-B}{2}\right).$$

### The small-angle approximation

For small $\theta$ in radians:

$$\sin\theta \approx \theta, \qquad \tan\theta \approx \theta, \qquad \cos\theta \approx 1 - \tfrac{1}{2}\theta^2.$$

The geometric picture: for a small angle on the unit circle, the arc length $\theta$ and the vertical drop $\sin\theta$ are nearly the same short segment. The full Taylor series (first found by Mādhava of the Kerala school, c. 1400 CE, some 250 years before Newton and Leibniz) `[verify — standard history of mathematics]`:

$$\sin\theta = \theta - \frac{\theta^3}{6} + \frac{\theta^5}{120} - \cdots, \qquad \cos\theta = 1 - \frac{\theta^2}{2} + \frac{\theta^4}{24} - \cdots.$$

The approximation $\sin\theta \approx \theta$ is good to $\sim 1\%$ for $|\theta| < 0.14$ rad ($\approx 8°$); to $\sim 10\%$ for $|\theta| < 0.45$ rad ($\approx 26°$). Always state the domain of validity when you use it.

### The sinusoidal traveling wave

A sinusoidal wave traveling in the $+x$ direction:

$$\psi(x,t) = A\cos(kx - \omega t + \varphi),$$

or in complex exponential form (the working form in QM):

$$\psi(x,t) = A\,e^{i(kx - \omega t)}.$$

Key parameters and their dimensions:

| Symbol | Name | Dimension | Definition |
|---|---|---|---|
| $A$ | Amplitude | (varies) | peak value |
| $k$ | Wavenumber | $L^{-1}$ (rad/m) | $k = 2\pi/\lambda$ |
| $\lambda$ | Wavelength | $L$ | spatial period |
| $\omega$ | Angular frequency | $T^{-1}$ (rad/s) | $\omega = 2\pi f = 2\pi/T_\text{period}$ |
| $\varphi$ | Phase offset | dimensionless | initial phase |
| $v_\text{ph}$ | Phase velocity | $LT^{-1}$ | $v_\text{ph} = \omega/k$ |

The argument $kx - \omega t + \varphi$ must be dimensionless — a good dimensional check. A leftward-traveling wave replaces $kx - \omega t$ with $kx + \omega t$ (or equivalently, $k$ with $-k$).

**Euler's formula** bridges real and complex forms:

$$e^{i\theta} = \cos\theta + i\sin\theta.$$

The physical wave is the real part of the complex exponential: $\text{Re}[Ae^{i(kx-\omega t)}] = A\cos(kx-\omega t)$. QM wavefunctions are genuinely complex, not just a notational convenience — the imaginary part carries phase information that determines interference. The intensity (probability density) is $|\psi|^2 = \psi^*\psi$, not $\psi^2$.

### Superposition and interference

The superposition principle: the total wave is the sum of its components. For two waves of equal amplitude differing only by a constant phase $\delta$, the sum-to-product identity gives:

$$\psi_1 + \psi_2 = A\cos(kx-\omega t) + A\cos(kx-\omega t+\delta) = 2A\cos(\delta/2)\cos(kx-\omega t+\delta/2).$$

The resultant is a wave at the same frequency with **amplitude $2A|\cos(\delta/2)|$**:

- $\delta = 0$ (in phase): amplitude $2A$ — **constructive interference**.
- $\delta = \pi$ (anti-phase): amplitude $0$ — **destructive interference**.
- General $\delta$: amplitude interpolates between 0 and $2A$.

### Group velocity and beats

Two waves of slightly different frequency and wavenumber: $(\omega, k)$ and $(\omega + d\omega, k + dk)$. Their sum:

$$\psi_1 + \psi_2 = 2A\cos\!\left(\frac{dk}{2}x - \frac{d\omega}{2}t\right)\cos\!\left(kx - \omega t\right).$$

The fast carrier oscillates at $k$, $\omega$; the slow envelope moves at:

$$v_g = \frac{d\omega}{dk}.$$

The **group velocity** $v_g$ is the speed of the envelope — the speed at which energy and information travel. For a non-dispersive medium, $\omega \propto k$ and $v_g = v_\text{ph}$. For a dispersive medium (like matter waves), $v_g \neq v_\text{ph}$, and a wave packet spreads as it travels.

---

## In the quantum series

### I·2 — Matter waves

De Broglie's hypothesis (1924) `[verify — de Broglie 1924 thesis]` assigns every particle of momentum $p$ a wavelength:

$$\lambda = \frac{h}{p}, \qquad k = \frac{p}{\hbar}, \qquad \omega = \frac{E}{\hbar}.$$

The quantum matter wave is then exactly the sinusoidal wave of this module:

$$\psi(x,t) = A\,e^{i(px/\hbar - Et/\hbar)} = A\,e^{i(kx - \omega t)}.$$

Every concept from the refresher — wavenumber, angular frequency, phase, superposition — now has a quantum interpretation. The key new facts are the relations $k = p/\hbar$ and $\omega = E/\hbar$; the wave algebra is unchanged.

**Phase velocity of a de Broglie wave (non-relativistic).** For a free particle with kinetic energy $E = p^2/2m$:

$$\omega = \frac{E}{\hbar} = \frac{p^2}{2m\hbar} = \frac{\hbar k^2}{2m}.$$

$$v_\text{ph} = \frac{\omega}{k} = \frac{\hbar k}{2m} = \frac{p}{2m} = \frac{v}{2}.$$

The phase velocity is *half* the particle's speed. The phase pattern moves at half-speed — it is not the particle.

**Group velocity of a de Broglie wave.** 

$$v_g = \frac{d\omega}{dk} = \frac{\hbar k}{m} = \frac{p}{m} = v.$$

The group velocity equals the particle's classical speed. The *envelope* of the wave packet is what moves with the particle. Without the beats analysis, $v_\text{ph} = v/2$ seems bizarre; with it, there is no paradox.

### Worked example: de Broglie double-slit interference

**Setup.** Electrons of momentum $p$ (hence $\lambda = h/p$, $k = p/\hbar$) pass through two slits separated by $d$. A detector screen is placed far enough away that rays from the two slits to a point at angle $\theta$ are nearly parallel.

**Path-length difference.** For a point at angle $\theta$ on the screen, the path lengths from the two slits differ by $\Delta = d\sin\theta$.

**Phase difference.** Each unit of path length contributes phase $k$ per unit length, so the phase difference between the two waves at the detector is:

$$\delta = k\Delta = \frac{2\pi}{\lambda}d\sin\theta = \frac{pd\sin\theta}{\hbar}.$$

**Interference condition.** From the superposition formula, the intensity (proportional to amplitude squared) is:

$$I(\theta) = 4A^2\cos^2\!\left(\frac{\delta}{2}\right) = 4A^2\cos^2\!\!\left(\frac{pd\sin\theta}{2\hbar}\right).$$

Constructive interference ($I = 4A^2$) when $\delta = 2\pi n$, i.e.:

$$d\sin\theta = n\lambda, \qquad n = 0, \pm 1, \pm 2, \ldots$$

This is the standard double-slit condition — exactly the same as for light, with the de Broglie wavelength $\lambda = h/p$ replacing the optical wavelength.

**Small-angle approximation.** For $\theta \ll 1$ rad, $\sin\theta \approx \theta$, and if the screen is at distance $L$, the transverse position is $y = L\tan\theta \approx L\theta$. The fringe spacing (distance between adjacent bright fringes) is:

$$\Delta y = \frac{\lambda L}{d} = \frac{hL}{pd}.$$

The faster the electrons (larger $p$, smaller $\lambda$), the finer the fringes. This is the formula used to design and interpret electron diffraction experiments.

**Historical note.** The electron double-slit experiment was first performed with a biprism by Jönsson (1961); later with actual double slits by Merli, Missiroli, and Pozzi (1976) and, in the single-electron regime, by Tonomura et al. (1989). `[verify]` The buildup of the interference pattern one electron at a time — a particle landing at one spot, yet the ensemble forming a wave pattern — remains one of the most striking demonstrations in physics.

---

## Conventions and pitfalls

**Radians are not optional in wave formulas.** The argument of $e^{i(kx-\omega t)}$ is in radians. $k$ has units rad/m; $x$ in meters; $kx$ is dimensionless (radians). If you convert $k$ or $\omega$ to "per cycle" units ($f$ in Hz instead of $\omega = 2\pi f$ in rad/s), you must also replace $kx-\omega t$ with $2\pi(x/\lambda - ft)$ or you lose a factor of $2\pi$.

**Sign convention for direction.** $\psi = Ae^{i(kx-\omega t)}$ travels in the $+x$ direction. $\psi = Ae^{i(kx+\omega t)}$ travels in the $-x$ direction. Some texts define $\omega$ as always positive and absorb the direction into the sign of $k$; others use $k < 0$ for leftward waves. Fix the convention at the start of any calculation.

**$|\psi|^2$, not $\psi^2$.** The probability density is $|\psi|^2 = \psi^*\psi$. For a complex wave $Ae^{ikx}$, $|Ae^{ikx}|^2 = A^2$ (a constant). If you write $\psi^2$ instead, you get $A^2e^{2ikx}$, which is wrong and dimensional nonsense in the probability context.

**$\lambda = 2\pi/k$, not $1/k$.** The factor of $2\pi$ is the source of most off-by-$2\pi$ errors. Wavenumber $k$ counts radians per unit length; the wavelength is one full cycle ($2\pi$ radians) per unit length.

**$\hbar$ vs. $h$ in de Broglie relations.** $\lambda = h/p$ uses $h$. The wavenumber form $k = p/\hbar$ uses $\hbar = h/2\pi$. Both are correct; they describe the same physics. The confusion arises when one mixes the formulas: $k = p/h$ (wrong by $2\pi$) or $\lambda = \hbar/p$ (wrong by $2\pi$).

**Phase velocity is not the particle velocity.** For a non-relativistic matter wave, $v_\text{ph} = v/2$. The particle's physical speed equals the *group* velocity of the wave packet. Do not use $v_\text{ph}$ to predict where the particle is.

---

## Quick practice

1. **Phase and group velocity.** A relativistic particle has energy $E = \sqrt{(pc)^2 + (m_0 c^2)^2}$ (Einstein's dispersion relation). Show that $\omega = E/\hbar$ and $k = p/\hbar$ give $v_\text{ph} = c^2/v$ and $v_g = v$, where $v$ is the particle's classical speed. (Hint: use $p = \gamma m_0 v$ and $E = \gamma m_0 c^2$.) What happens to $v_\text{ph}$ for a massless particle?

2. **Double-slit fringe spacing.** Electrons are accelerated through a potential difference of $V = 100$ V. (a) Find the kinetic energy, momentum, and de Broglie wavelength. (b) If the slit separation is $d = 1\ \mu\text{m}$ and the screen is at $L = 1\ \text{m}$, find the fringe spacing $\Delta y = \lambda L/d$ in the small-angle approximation.

3. **Superposition and phase.** Two quantum waves $\psi_1 = e^{ikx}$ and $\psi_2 = e^{i(kx+\pi/3)}$ are superposed. Find $|\psi_1 + \psi_2|^2$ and verify it equals $4\cos^2(\pi/6) = 3$. Then find the phase $\delta$ such that the superposition is (a) maximally constructive and (b) fully destructive.

---

## Go deeper

The source chapter — *Mathematics for Physics* Vol 1, Ch 3 — covers trigonometry and geometry in full, including worked examples on force resolution, projectile range, and the law of cosines. For the wave physics extension (sinusoidal waves, interference, group and phase velocity), see French, *Vibrations and Waves* (MIT Introductory Physics, W. W. Norton, 1971), Chs. 7–8; and Crawford, *Waves* (Berkeley Physics Course Vol. 3, McGraw-Hill, 1968), Ch. 1. For the quantum context, see Griffiths, *Introduction to Quantum Mechanics* (3rd ed., Cambridge, 2018), §1.3–1.4 (normalization and the Fourier transform of a wave packet). `[verify]`

---

## References

1. Louis de Broglie, "Recherches sur la théorie des quanta," *Annales de Physique* 10, series 10, pp. 22–128 (1925). (English translation of his 1924 thesis.) `[verify]`
2. A. P. French, *Vibrations and Waves*. MIT Introductory Physics Series. W. W. Norton, 1971. Chs. 7–8 (interference and beats). `[verify]`
3. Frank S. Crawford Jr., *Waves*. Berkeley Physics Course, Vol. 3. McGraw-Hill, 1968. Ch. 1 (sinusoidal waves). `[verify]`
4. David J. Griffiths, *Introduction to Quantum Mechanics*, 3rd ed. Cambridge University Press, 2018. §1.3–1.4. `[verify]`
5. C. Jönsson, "Elektroneninterferenzen an mehreren künstlich hergestellten Feinspalten," *Zeitschrift für Physik* 161, 454–474 (1961). (First electron double-slit experiment.) `[verify]`
6. A. Tonomura, J. Endo, T. Matsuda, T. Kawasaki, and H. Ezawa, "Demonstration of single-electron buildup of an interference pattern," *American Journal of Physics* 57, 117 (1989). `[verify]`
7. Mādhava of Sangamagrāma and the Kerala school; *Yuktibhāṣā* (c. 1400) — power series for sine and cosine, predating Newton and Leibniz by $\sim$250 years. `[verify — standard history of mathematics]`
