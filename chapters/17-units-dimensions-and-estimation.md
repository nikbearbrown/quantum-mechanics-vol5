# Module M-17 — Units, Dimensions, and Estimation

**Refresher for QM chapters:** I·1

**Condensed from:** *Mathematics for Physics* Vol 1, Ch 1

---

## When you need this

Read this module before **I·1** (why classical physics failed). That chapter argues from the breakdown of classical predictions — the ultraviolet catastrophe, the photoelectric threshold, the stability of atoms — and every argument is at root a statement about *scales*. To see why classical physics fails at the atomic scale, you need to know what sets that scale. The tool is dimensional analysis: the same algebra used to derive the pendulum period, applied to Planck's constant and the electron mass, hands you the size of the hydrogen atom before you write a single differential equation.

---

## The refresher

### Dimensions as algebra

Every physical quantity carries a dimension — a label for what *kind* of thing is being measured. In mechanics the three base dimensions are length $L$, mass $M$, and time $T$. We write $[q]$ for the dimension of $q$:

$$[\text{speed}] = LT^{-1}, \quad [\text{acceleration}] = LT^{-2}, \quad [\text{force}] = MLT^{-2}, \quad [\text{energy}] = ML^2T^{-2}.$$

Dimensions multiply and divide like algebraic symbols. The **principle of dimensional homogeneity**: only quantities of the same dimension can be added, subtracted, or equated. You cannot add a length to a time. A dimensionally inconsistent equation is *certainly wrong*. A dimensionally consistent equation is *merely allowed* — consistency is necessary, not sufficient, for truth.

A pure number (like $\tfrac{1}{2}$, $\pi$, or $e$) carries no dimension and can never introduce a dimensional error. This matters: it means dimensional analysis can determine the *form* of an answer (which variables appear and with what powers) but it can never supply a numerical coefficient.

### Buckingham $\Pi$-theorem and Rayleigh's method

Any physically meaningful relation among $n$ dimensioned variables built from $k$ independent base dimensions can be rewritten as a relation among exactly $n - k$ dimensionless groups (the $\Pi$s). The proof is linear algebra: the dimensionless groups are the null space of the exponent matrix.

**Worked derivation — the pendulum period.** The period $T_p$ plausibly depends on the length $\ell$, gravitational acceleration $g$, and bob mass $m$. Assume $T_p = C\,\ell^a g^b m^c$. Match dimensions (both sides must equal $T^1 L^0 M^0$):

- Mass: $c = 0$ — *mass is irrelevant.*
- Time: $-2b = 1 \Rightarrow b = -\tfrac{1}{2}$.
- Length: $a + b = 0 \Rightarrow a = \tfrac{1}{2}$.

$$T_p = C\sqrt{\frac{\ell}{g}}.$$

Dimensional analysis derives the dependence without solving the equation of motion. It cannot supply $C = 2\pi$; that requires the full theory.

### Significant figures and relative uncertainty

Significant figures encode relative uncertainty. A quantity reported to three significant figures is known to roughly $\pm 0.5\%$. For a product or quotient, the result retains the *fewest* significant figures of any input because relative uncertainties combine — the sloppiest input dominates.

The precise rule: for $q = A^m B^n$, take $\ln q = m\ln A + n\ln B$, differentiate:

$$\frac{\delta q}{q} = \sqrt{\left(m\,\frac{\delta A}{A}\right)^2 + \left(n\,\frac{\delta B}{B}\right)^2}$$

(combining in quadrature for independent errors). The exponent $m$ or $n$ amplifies the relative uncertainty of its factor. A cube amplifies threefold.

### Order-of-magnitude estimation

Decompose the unknown into factors each estimable to within a factor of ten. Combine. Only the *exponent* of the result is to be trusted; the leading digit is not. When you have a plausible low bound $x_\text{lo}$ and high bound $x_\text{hi}$, the natural midpoint on a log scale is the geometric mean $\sqrt{x_\text{lo} \cdot x_\text{hi}}$.

**Example — de Broglie wavelength of a 1 eV electron.** Using $\lambda = h/p = h/\sqrt{2m_e E}$:

$$\lambda = \frac{6.626 \times 10^{-34}\ \text{J·s}}{\sqrt{2 \times 9.11 \times 10^{-31}\ \text{kg} \times 1.602 \times 10^{-19}\ \text{J}}} \approx 1.23\ \text{nm}.$$

This is atomic scale — electrons at 1 eV wavelengths comparable to atomic spacings, which is why electron diffraction in crystals (Davisson–Germer, 1927) was decisive evidence for matter waves. The estimate requires no QM: only dimensional combination of known constants.

---

## In the quantum series

### $\hbar$ as the quantum of action

Planck's constant $h = 6.626 \times 10^{-34}$ J·s; $\hbar = h/2\pi = 1.055 \times 10^{-34}$ J·s. Its dimension:

$$[\hbar] = \text{J·s} = \text{kg·m}^2\text{s}^{-1} = ML^2T^{-1} = \text{action} = \text{energy} \times \text{time} = \text{momentum} \times \text{length}.$$

$\hbar$ is an *action*, not an energy. It quantizes angular momentum (the orbital angular momentum quantum number is $l$ in units of $\hbar$, so $[L] = \hbar$) and is the natural unit for the product $p \cdot x$ that appears in the uncertainty principle $\Delta x\,\Delta p \geq \hbar/2$.

Seeing $\hbar$ as an action — not just "a small number" — is the conceptual step that makes quantization feel inevitable rather than arbitrary. Whenever classical physics would produce an action much larger than $\hbar$, quantum effects are small; when the relevant action is comparable to $\hbar$, quantum effects dominate.

### Deriving the Bohr radius by dimensional analysis

The hydrogen ground state has a characteristic length set by the constants that appear in the problem: $\hbar$ (quantum of action), $m_e$ (electron mass), and $e^2/4\pi\epsilon_0$ (the electromagnetic coupling strength, with dimension $ML^3T^{-2}$). We want a length from these three. Assume $a_0 = \hbar^\alpha m_e^\beta (e^2/4\pi\epsilon_0)^\gamma$ and match dimensions:

| Dimension | Equation |
|---|---|
| $M$: | $\beta + \gamma = 0$ |
| $L$: | $2\alpha + 3\gamma = 1$ |
| $T$: | $-\alpha - 2\gamma = 0$ |

Solving: $\gamma = -1$, $\beta = 1$, $\alpha = 2$. So:

$$a_0 = \frac{4\pi\epsilon_0\hbar^2}{m_e e^2} \approx 5.29 \times 10^{-11}\ \text{m} = 0.529\ \text{Å}.$$

No Schrödinger equation was solved. Dimensional analysis predicts the atomic size to within the pure number (which turns out to be 1, confirmed by solving the full problem). Classical electrodynamics predicts no characteristic length: a classically radiating electron spirals inward on a timescale of $\sim 10^{-11}$ s, with no preferred stopping radius. The existence of $a_0$ is a quantum prediction — the first quantum result you can derive by dimension alone.

### The Compton wavelength

The length scale where quantum and relativistic effects are both significant is set by $\hbar$, $m_e$, and $c$. The unique combination with dimension of length:

$$\lambda_C = \frac{\hbar}{m_e c} \approx 3.86 \times 10^{-13}\ \text{m}.$$

Above $\lambda_C$, non-relativistic QM is adequate; below it, pair production and quantum field effects dominate. The Compton effect — the shift in X-ray wavelength upon scattering from electrons — is explained by treating photons as particles and using $\lambda_C$ as the relevant scale.

### Natural units ($\hbar = c = 1$)

In particle physics and advanced QM, it is conventional to set $\hbar = c = 1$ (and sometimes $k_B = 1$ as well). In these units, mass, energy, momentum, and inverse length all share the same dimension ("inverse length" and "mass" are the same quantity). Energies are quoted in eV or MeV; lengths are in $\text{eV}^{-1}$ via the conversion:

$$\hbar c \approx 197.3\ \text{MeV·fm} = 197.3 \times 10^{-15}\ \text{MeV·m}.$$

To restore SI factors from a natural-units result: count the powers of $\hbar$ and $c$ needed to give the right dimension. For example, a cross-section $\sigma$ has dimension $L^2 = (\hbar c)^2 / \text{energy}^2$; a lifetime $\tau$ has dimension $T = \hbar / \text{energy}$.

Natural units are a precision tool, not a shortcut. A student who sets $\hbar = c = 1$ without being able to restore the factors is flying blind. Practice the restoration: if you compute a length in natural units and get a number in MeV$^{-1}$, multiply by $\hbar c \approx 197$ MeV·fm to recover meters.

### Worked example: estimating when classical physics fails

At room temperature, $k_B T \approx 1/40\ \text{eV} \approx 4 \times 10^{-21}\ \text{J}$. For a macroscopic oscillator of frequency $\nu = 1\ \text{kHz}$, the quantum of energy is $h\nu = 6.6 \times 10^{-31}\ \text{J}$. Ratio: $h\nu / k_B T \approx 10^{-10}$. Classical physics is completely adequate — quantum effects are negligible at a factor of $10^{10}$ below thermal energy.

For an atomic electron in hydrogen, the relevant energy is the Rydberg: $E_1 = m_e e^4 / (8\epsilon_0^2 h^2) \approx 13.6\ \text{eV}$. At room temperature $k_B T \approx 0.025\ \text{eV}$, so $E_1 / k_B T \approx 540$. Quantum effects dominate; classical thermal arguments are irrelevant to atomic structure. The crossover between classical and quantum behavior is exactly the dimensional comparison $k_B T$ vs. $\hbar\omega$ (or $E_\text{quantized}$). Chapter I·1 returns to this repeatedly.

---

## Conventions and pitfalls

**SI vs. Gaussian (CGS) units.** QM texts split almost evenly. In SI, the Coulomb force is $F = e^2/(4\pi\epsilon_0 r^2)$; the Bohr radius is $a_0 = 4\pi\epsilon_0\hbar^2/(m_e e^2)$. In Gaussian units, $F = e^2/r^2$ (no $4\pi\epsilon_0$), and the Bohr radius is $a_0 = \hbar^2/(m_e e^2)$. These are the same quantity; only the bookkeeping of electromagnetic constants differs. Check which system the text you are reading uses before applying any formula involving $e$.

**$\hbar$ vs. $h$.** $\hbar = h/2\pi$. The de Broglie relation is $\lambda = h/p$; written with wavenumber $k = 2\pi/\lambda$, this is $k = p/\hbar$. Confusing $h$ and $\hbar$ introduces a factor of $2\pi$ — a silent error with no dimensional signal.

**eV vs. Joule.** In QM, energies are almost always quoted in eV. Key benchmarks: electron rest mass $m_e c^2 = 511\ \text{keV}$; hydrogen ground state $-13.6\ \text{eV}$; room-temperature thermal energy $k_BT \approx 25\ \text{meV}$. Know these by heart.

**Arguments of exponentials and sinusoids must be dimensionless.** The argument of $e^{ix}$ or $\sin(\omega t)$ is dimensionless. $\omega$ has units of rad/s; $t$ in seconds; $\omega t$ is dimensionless. If you find a dimensioned argument, something is wrong upstream.

**Natural units pitfall.** When $\hbar = c = 1$, mass, energy, and inverse length are numerically the same. This is a *convention*, not a physical identity. The dimensions are still there; you have simply chosen units that make the conversion factors equal to 1. You must be able to restore those factors to compare with experiment.

---

## Quick practice

1. **Dimensional derivation.** A mass $m$ on a spring of stiffness $k$ (units N/m = kg/s²) oscillates with period $T$. Using only dimensional analysis, derive how $T$ depends on $m$ and $k$. (You should find $T \propto \sqrt{m/k}$.) Why can the amplitude of oscillation not appear in the result?

2. **Bohr radius check.** Verify that $\hbar^2/(m_e e^2/4\pi\epsilon_0)$ has units of length. Use SI values: $[\hbar] = \text{J·s}$, $[m_e] = \text{kg}$, $[e^2/4\pi\epsilon_0] = \text{N·m}^2 = \text{kg·m}^3\text{s}^{-2}$. Show every cancellation explicitly.

3. **Natural units restoration.** In natural units ($\hbar = c = 1$), the lifetime of an excited hydrogen state is written as $\tau = A / (m_e \alpha^5)$, where $\alpha \approx 1/137$ is the (dimensionless) fine-structure constant. What dimensions must $A$ carry in natural units? Restore $\hbar$ and $m_e c^2$ to express $\tau$ in seconds, given $m_e c^2 = 511\ \text{keV}$ and $\hbar \approx 6.6 \times 10^{-16}\ \text{eV·s}$.

---

## Go deeper

The source chapter — *Mathematics for Physics* Vol 1, Ch 1 — covers dimensional analysis, significant figures, and estimation in full. For the quantum-physics extensions (Bohr radius, Compton wavelength, natural units), see Griffiths, *Introduction to Quantum Mechanics* (3rd ed., Cambridge, 2018), §1.2; and Cohen-Tannoudji, Diu, and Laloë, *Quantum Mechanics* (Wiley, 2019), Complement A-I. For natural units specifically, see Peskin and Schroeder, *An Introduction to Quantum Field Theory* (Westview, 1995), §1.1–1.2. `[verify]`

---

## References

1. Edgar Buckingham, "On Physically Similar Systems; Illustrations of the Use of Dimensional Equations," *Physical Review* 4, 345–376 (1914). `[verify]`
2. David J. Griffiths, *Introduction to Quantum Mechanics*, 3rd ed. Cambridge University Press, 2018. §1.2 (the wave function; scales). `[verify]`
3. Claude Cohen-Tannoudji, Bernard Diu, and Franck Laloë, *Quantum Mechanics*, 2 vols. Wiley-VCH, 2019. Complement A-I (orders of magnitude in atomic physics). `[verify]`
4. BIPM, *The International System of Units (SI)*, 9th ed. (2019); NIST Special Publication 330 (2019). `[verify]`
5. NIST CODATA 2018 recommended values: $\hbar = 1.054571817 \times 10^{-34}\ \text{J·s}$; $m_e = 9.1093837015 \times 10^{-31}\ \text{kg}$; $a_0 = 5.29177210903 \times 10^{-11}\ \text{m}$; $\lambda_C = 3.8615926796 \times 10^{-13}\ \text{m}$. `[verify — values current]`
6. NASA, *Mars Climate Orbiter Mishap Investigation Board Phase I Report* (1999). (Motivating example for unit discipline.) `[verify]`
