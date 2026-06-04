# Research Notes: Module M-06 — The Fourier Transform
**Optional companion module.** Refresher for QM chapters: I·8 (wave packets), III·5 (transitions), III·8 (Born scattering)
**Condensed from:** `_lib_mfp2-06-fourier-transforms-and-their-physics.md`
**Generated:** 2026-06-03

---

## A. The tool (key results condensed)

### The transform pair

Forward transform (position → wavenumber):
$$\tilde f(k) = \int_{-\infty}^{\infty} f(x)\, e^{-ikx}\,dx$$

Inverse transform (wavenumber → position):
$$f(x) = \frac{1}{2\pi}\int_{-\infty}^{\infty} \tilde f(k)\, e^{ikx}\,dk$$

Derivation: the $L\to\infty$ limit of the Fourier series. As period $L\to\infty$, spacing $\Delta k = 2\pi/L \to 0$, discrete sum becomes integral. This is not a separate definition — it is the series you already know in the continuous limit.

**Quantum convention:** symmetric split $1/\sqrt{2\pi\hbar}$ on each side, with $p = \hbar k$:
$$\tilde\psi(p) = \frac{1}{\sqrt{2\pi\hbar}}\int \psi(x)\, e^{-ipx/\hbar}\,dx$$

**Convention warning:** the $2\pi$ factor can live entirely on the inverse, be split symmetrically as $1/\sqrt{2\pi}$, or vanish (with ordinary frequency $\nu$). The sign of the exponent can also flip. None is more correct; inconsistency between conventions is the source of half the errors students bring to office hours.

### Plancherel (norm preservation)
$$\int|f(x)|^2\,dx = \frac{1}{2\pi}\int|\tilde f(k)|^2\,dk$$
The transform is (up to a constant) unitary: a normalized wavefunction stays normalized in either space.

### The convolution theorem
Convolution in real space: $(f*g)(x) = \int f(x')g(x-x')\,dx'$

Key result:
$$\widetilde{f*g}(k) = \tilde f(k)\cdot\tilde g(k)$$

Proof: change variable $u=x-x'$, separate the integrals. Convolution in position space = pointwise multiplication in $k$-space (and vice versa).

### The bandwidth relation
For rms widths $\Delta x$ (of $|f|^2$) and $\Delta k$ (of $|\tilde f|^2$):
$$\Delta x\,\Delta k \geq \tfrac12$$

This is a theorem about any Fourier pair — not a quantum postulate. Follows from the scaling property: $f(ax) \Rightarrow \tilde f(k/a)/a$, so width product is scale-invariant. **Keep distinct** from Robertson: $\sigma_A\sigma_B \geq \frac12|\langle[\hat A,\hat B]\rangle|$ is a statement about operators and commutators. Both reproduce $\sigma_x\sigma_p \geq \hbar/2$, but by different routes. The energy–time relation $\Delta E\,\Delta t \sim \hbar$ is purely the bandwidth relation (time is not a QM operator; Robertson does not apply).

### The Gaussian: its own transform
$$f(x) = e^{-x^2/2a^2} \;\Longrightarrow\; \tilde f(k) \propto e^{-a^2 k^2/2}$$

The Gaussian is the unique shape that saturates the bandwidth bound: $\Delta x\,\Delta k = \frac12$. This is why the Gaussian wave packet is the minimum-uncertainty state — the most "classical-looking" quantum state.

### The Dirac delta
Defined entirely by its action under integration:
$$\int \delta(x-x_0)\,f(x)\,dx = f(x_0)$$
Not an ordinary function — it is a distribution. Arises as the Fourier transform of a constant:
$$\delta(x-x') = \frac{1}{2\pi}\int_{-\infty}^{\infty} e^{ik(x-x')}\,dk$$
This is the continuous analogue of the Kronecker delta, and it is what makes the continuous resolution of the identity $\int|x\rangle\langle x|\,dx = \hat I$ work with $\langle x|x'\rangle = \delta(x-x')$.

### Worked example: Gaussian wave packet in position → momentum

Take $\psi(x) = (\pi a^2)^{-1/4} e^{-x^2/2a^2}$. Complete the square in the exponent:
$$\tilde\psi(p) \propto \exp\!\left(-\frac{a^2 p^2}{2\hbar^2}\right)$$
Position width: $\Delta x = a/\sqrt{2}$. Momentum width: $\Delta p = \hbar/(a\sqrt{2})$. Product: $\Delta x\,\Delta p = \hbar/2$. Saturation of the bound. Small $a$ (localized) → large $\Delta p$ in exact reciprocal proportion.

---

## B. Where the quantum series uses it

**I·8 (wave packets):** The Fourier transform is the direct mathematical engine. A wave packet $\psi(x,0)$ is built by superposing plane waves with a momentum-space envelope $\tilde\psi(p)$; the transform pair converts between the two representations. Group velocity $v_g = d\omega/dk$ comes from the phase of $\tilde\psi$ after time evolution; phase velocity from the carrier. The Gaussian wave packet (Example 3 in the source) is the specific worked case students need to follow I·8.

**III·5 (transitions):** Fermi's Golden Rule involves transition matrix elements of the form $\langle f|V|i\rangle$, and when the perturbation $V$ is a function of position, its Fourier transform encodes which spatial frequencies drive the transition. Time-domain treatments of time-dependent perturbation theory also invoke the frequency-domain picture (frequency of driving vs. natural frequency) — the time–frequency bandwidth relation appears in the energy–time version of the uncertainty principle for transition rates.

**III·8 (Born scattering):** The Born approximation for the scattering amplitude is
$$f(\theta) \propto \int V(\mathbf{r})\, e^{i(\mathbf{k}_i - \mathbf{k}_f)\cdot\mathbf{r}}\,d^3r$$
This is explicitly the 3D Fourier transform of the potential $V(\mathbf{r})$ evaluated at the momentum transfer $\mathbf{q} = \hbar(\mathbf{k}_i - \mathbf{k}_f)$. The Born amplitude is $\tilde V(\mathbf{q})$. Students cannot follow the Born derivation without recognizing this as a Fourier transform.

---

## C. Connections

**Earlier math modules needed:**
- M-02 (complex exponentials): $e^{ikx}$ is the building block of the transform; Euler's formula converts it to trig.
- M-05 (Fourier series, if present): the source chapter explicitly derives the transform as the $L\to\infty$ limit of the series; students who saw the series first will find the transform less mysterious.
- M-03 (integration techniques, completing the square): the Gaussian transform requires completing the square in the exponent — a calculation that stalls students who are shaky on it.

**QM chapters unlocked by M-06:**
- I·8: wave packets become computable, not just pictorial.
- III·5: the spectral picture of transitions becomes accessible.
- III·8: Born scattering reduces to a single integral recognition.
- Also anticipates: free-particle time evolution (momentum space is diagonal for the free particle — each $\tilde\psi(p)$ merely acquires phase $e^{-ip^2t/2m\hbar}$).

---

## D. Conventions and pitfalls

1. **The $2\pi$ placement.** The asymmetric convention (source uses it) puts $1/2\pi$ entirely on the inverse. The symmetric convention (quantum use) splits as $1/\sqrt{2\pi\hbar}$. Students who mix conventions from different textbooks get factors of $2\pi$ or $\hbar$ wrong in momentum-space norms.

2. **Sign of exponent.** Physics: $e^{-ikx}$ in the forward transform (positive frequencies carry positive wavevectors). Engineering: often uses $e^{+ikx}$. The convention changes the sign of $k$ in the transform of $f'(x)$.

3. **The delta as a spike.** Students picture $\delta(x)$ as "a very tall, thin spike." This fails when they try to manipulate it outside an integral or multiply two deltas. The source is explicit: it is only defined by its action under integration.

4. **Bandwidth relation vs. Robertson.** The distinction matters in III·5. The energy–time relation is bandwidth, not Robertson; time is not a QM operator. Students who treat $\Delta E\,\Delta t$ as "Robertson applied to $\hat H$ and $\hat t$" import a category error.

5. **Plancherel normalization.** The norm conservation includes a $1/2\pi$ factor (asymmetric convention). Students forget this when checking that $\tilde\psi(p)$ is normalized after computing it from $\psi(x)$.

---

## E. Teaching considerations

**Where students stumble:**

- **Convention collision.** Most QM textbooks (Griffiths, Sakurai) use slightly different conventions from most math courses. Students who look up a formula online or in a different text often get the factor wrong. Worth making the quantum convention explicit with a labeled box at module start.

- **The Gaussian integral.** Completing the square $-x^2/2a^2 - ipx/\hbar = -(x + ipa^2/\hbar)^2/2a^2 - p^2a^2/2\hbar^2$ requires comfort with complex shifts in the exponent. This step is where I·8 calculations stall. A worked substitution helps.

- **Recognizing the Born integral.** Students often fail to see that $\int V(\mathbf{r})e^{i\mathbf{q}\cdot\mathbf{r}}d^3r$ is a Fourier transform — especially in 3D, or when $V$ is spherically symmetric and the angular integration has already been done, leaving only the radial piece. Flagging this connection before III·8 pays off.

- **The delta function in continuous bases.** The identity $\langle x|x'\rangle = \delta(x-x')$ looks alarming at first. Students need to see that it is just the continuous-limit version of $\langle e_m|e_n\rangle = \delta_{mn}$ — same orthonormality, continuous index.

- **Conflating bandwidth with measurement disturbance.** A common misconception (documented in the Singh & Marshman PER) is treating the uncertainty principle as being about clumsy instruments. The bandwidth version makes clear it is a property of the wavefunction itself, before any measurement.

---

## F. Source file used

`_lib_mfp2-06-fourier-transforms-and-their-physics.md`

Chapter covers: transform as limit of Fourier series; Plancherel; convolution theorem (with full proof by substitution); bandwidth relation; the Gaussian as minimum-uncertainty state; Dirac delta (operational definition, not rigorous distribution theory); worked examples: top-hat/sinc (single slit), double slit by convolution, Gaussian wave packet. Notes on generalizations: spectroscopy/deconvolution, crystallography, free-particle dynamics, Bessel/circular aperture hand-off, FFT.

---

## G. Gaps and flags

- **3D Fourier transform:** the source covers only 1D explicitly. The Born approximation (III·8) is a 3D transform. Module will need a short note on the 3D case, $\tilde f(\mathbf{k}) = \int f(\mathbf{r})e^{-i\mathbf{k}\cdot\mathbf{r}}d^3r$, including the spherical-symmetry reduction to a 1D integral involving $\sin(qr)/qr$.

- **Parseval vs. Plancherel:** the source uses "Plancherel" (the $L^2$-norm version). Some QM texts say "Parseval." Worth noting the terminology is sometimes conflated.

- **Distribution theory:** the source flags Schwartz's rigorous treatment but stays operational. If students ask "what does $\delta^2(x)$ mean?" the module should redirect to the flag in the source rather than attempting an answer.

- **Source fact-check flags inherited:** the Cauchy 1827 attribution and the Gabor pagination are flagged unverified in the source's own fact-check notes. Not load-bearing for the module.
