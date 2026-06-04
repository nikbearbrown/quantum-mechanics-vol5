# Module M-14 — Combinatorics and Multiplicity

**When you need this:** QM Series Vol. II, Chapter 10 (Identical Particles); Vol. IV, Chapter 9 (Quantum Error Correction)

**Condensed from:** *Mathematics for Physics, Vol. 2*, Ch. 9

---

## The refresher

### The load-bearing distinction

Before any formula: internalize three terms, because every counting error in physics begins with confusing them.

- **Microstate**: one fully-specified arrangement — which specific spins are up, which exact qubits are $|0\rangle$, which precise molecules are in which box.
- **Macrostate**: the coarse, measurable summary — the net magnetization, the syndrome measurement result, the total energy.
- **Multiplicity** $\Omega$: the number of microstates that produce a given macrostate.

Many microstates map to one macrostate. The number that map is $\Omega$. Everything below is the arithmetic of $\Omega$.

### Permutations and combinations

A **permutation** counts ordered arrangements. The number of ways to arrange $n$ distinct objects in a row is

$$n! = n \cdot (n-1) \cdot (n-2) \cdots 2 \cdot 1,$$

and the number of ordered arrangements of $k$ chosen from $n$ is $P(n,k) = n!/(n-k)!$.

A **combination** counts unordered selections. When you choose $k$ from $n$ and the order of the chosen set doesn't matter, divide out the $k!$ internal orderings:

$$\boxed{\;\binom{n}{k} = \frac{n!}{k!\,(n-k)!}.\;}$$

**The single decision that determines which formula.** *Does order matter?* For spin counting: you care which spins are up, not which one you labeled "first" — order does not matter — use a combination. The binomial coefficient satisfies the Pascal recursion $\binom{n}{k} = \binom{n-1}{k-1} + \binom{n-1}{k}$ and appears in the binomial theorem $(a+b)^n = \sum_{k=0}^n \binom{n}{k} a^k b^{n-k}$.

> **Historical note.** Pascal's triangle appears in Yang Hui's work in 13th-century China and in the Islamic tradition with al-Karaji, centuries before Pascal's 1665 treatise. "Pascal's triangle" is the Western name for a much older object.

### Multiplicity of a two-state system

A two-state system with $N$ labeled objects, each in one of two states (up/down, $|0\rangle$/$|1\rangle$), has multiplicity

$$\Omega(N, N_\uparrow) = \binom{N}{N_\uparrow} = \frac{N!}{N_\uparrow!\,(N - N_\uparrow)!}$$

for the macrostate with exactly $N_\uparrow$ objects in state "up." This peaks sharply at $N_\uparrow = N/2$ and the peak sharpens as $N$ grows: at thermodynamic scale $N \sim 10^{23}$, the peak is a needle, and the system is overwhelmingly found at the most probable macrostate. Equilibrium is not imposed from outside; it is just where the microstates are concentrated.

**Stars and bars.** When distributing $q$ *indistinguishable* quanta among $N$ *distinguishable* bins (the Einstein solid model), the counting is different:

$$\Omega(N, q) = \binom{q + N - 1}{q}.$$

This formula applies when objects being distributed are identical — do not confuse it with the spin counting above, where the $N$ spins are distinguishable.

### Stirling's approximation

For $N \sim 10^{23}$, the factorial $N!$ has more digits than atoms in a room and cannot be evaluated directly. Worse, we want to *differentiate* $\ln\Omega$ with respect to $N$ — and a factorial is not differentiable. The fix: approximate the sum $\ln N! = \sum_{m=1}^N \ln m$ by an integral:

$$\ln N! = \sum_{m=1}^N \ln m \approx \int_1^N \ln x\,dx = \bigl[x\ln x - x\bigr]_1^N = N\ln N - N + 1.$$

Dropping the negligible $+1$ gives the leading **Stirling approximation**:

$$\boxed{\;\ln N! \approx N\ln N - N.\;}$$

The refined form, from a more careful asymptotic analysis, is

$$N! \approx \sqrt{2\pi N}\left(\frac{N}{e}\right)^N, \qquad \ln N! \approx N\ln N - N + \tfrac{1}{2}\ln(2\pi N).$$

**Why dropping the $\tfrac{1}{2}\ln(2\pi N)$ term is not cheating.** For $N = 10^{23}$: the kept term $N\ln N \approx 5 \times 10^{24}$; the dropped term $\tfrac{1}{2}\ln(2\pi N) \approx 27$. The relative error is one part in $10^{23}$ — no experiment could resolve it.

**Stirling applied to the binomial coefficient.** Using $\ln\Omega = \ln N! - \ln N_\uparrow! - \ln(N-N_\uparrow)!$ and applying the leading Stirling form to each factorial:

$$\ln\Omega = N\ln N - N_\uparrow \ln N_\uparrow - (N - N_\uparrow)\ln(N - N_\uparrow).$$

This is the fundamental formula: a smooth, differentiable function of $N_\uparrow$ that can be maximized analytically and differentiated with respect to energy.

### From multiplicity to entropy: $S = k\ln\Omega$

Why the logarithm? Two interlocking arguments.

**Multiplicities multiply; entropy must add.** If system A has $\Omega_A$ microstates and system B has $\Omega_B$, the combined system has $\Omega_A \Omega_B$ microstates (every microstate of A paired with every microstate of B). Thermodynamic entropy is *extensive* — it adds when you combine systems. The only function that converts multiplication to addition is the logarithm:

$$\ln(\Omega_A \Omega_B) = \ln\Omega_A + \ln\Omega_B.$$

So if entropy is a function of multiplicity and must be additive, it must be proportional to $\ln\Omega$.

**Temperature falls out by differentiating.** With $S = k\ln\Omega$ a differentiable function of energy (Stirling makes this possible), define temperature through

$$\frac{1}{T} \equiv \frac{\partial S}{\partial E}.$$

Maximizing $\Omega$ subject to a fixed total energy is equivalent to requiring that $\partial S_A/\partial E = \partial S_B/\partial E$ — which is the statement that the two systems share a common temperature. The entire equilibrium condition is a calculus exercise on a counting formula.

### Worked example — counting microstates for a small system

**Problem.** A system has $N = 6$ distinguishable spins. How many microstates have exactly $N_\uparrow = 2$ spins up? What fraction of all microstates does this represent?

**Step 1 — count.** Order doesn't matter (which two are up, not which-first):

$$\Omega(6, 2) = \binom{6}{2} = \frac{6!}{2!\,4!} = \frac{6 \times 5}{2} = 15.$$

**Step 2 — total microstates.** Each of the 6 spins is independently up or down: $2^6 = 64$ total microstates.

**Step 3 — fraction.** $15/64 \approx 23.4\%$. Compare with the peak macrostate $N_\uparrow = 3$: $\binom{6}{3} = 20$, giving $20/64 \approx 31.3\%$. The peak is not yet overwhelmingly dominant at $N = 6$; at $N = 10^{23}$ the peak is a knife-edge.

**Step 4 — Stirling check.** For $N = 6$, exact: $\ln 15 \approx 2.71$. Stirling: $6\ln 6 - 6 - (2\ln 2 - 2) - (4\ln 4 - 4) \approx 10.75 - 6 - (-0.61) - (5.55 - 4) = 10.75 - 6 + 0.61 - 1.55 = 3.81$. A 40% error — Stirling is poor for small $N$ and exact only in the thermodynamic limit. Always note which regime you are in.

---

## In the quantum series

### Identical particles: counting changes everything (Vol. II, Ch. 10)

The Chapter 10 distinction between bosons and fermions is, at its mathematical root, a *counting* distinction. Put two quantum particles into two available single-particle states:

| Statistics | Rule | Distinct microstates (2 particles, 2 states) |
|---|---|---|
| Maxwell–Boltzmann (distinguishable) | any occupancy | 4 |
| Bose–Einstein (identical bosons) | any occupancy per state | 3 |
| Fermi–Dirac (identical fermions) | at most 1 per state (Pauli) | **1** |

The Fermi–Dirac count is 1 because the only allowed configuration for two identical fermions in two states is "one in each state." The wavefunction antisymmetry enforces exactly this: a Slater determinant

$$|\psi\rangle = \frac{1}{\sqrt{2}}\bigl(\phi_a(1)\phi_b(2) - \phi_b(1)\phi_a(2)\bigr)$$

vanishes identically when $\phi_a = \phi_b$ — two fermions in the same state give zero amplitude. **Pauli exclusion is the algebraic statement that $\Omega_\text{FD} = 0$ for doubly-occupied single-particle states.** The determinant structure is the counting rule made antisymmetric.

The symmetrization postulate (bosons: symmetric $\psi$; fermions: antisymmetric $\psi$) is the *quantum mechanism* that enforces the counting rules in the table. Chapter 10 derives the physical consequences — Fermi pressure, Bose condensation — from wavefunctions; the combinatorics here is the substrate under that derivation.

### Quantum error correction: syndrome = macrostate (Vol. IV, Ch. 9)

An $[[n, k, d]]$ quantum error-correcting code encodes $k$ logical qubits in $n$ physical qubits and can correct any error on up to $t = \lfloor(d-1)/2\rfloor$ physical qubits. The combinatorics enters immediately.

**Counting errors.** The number of distinct weight-$t$ Pauli errors on $n$ qubits (errors affecting exactly $t$ sites) is

$$\binom{n}{t} \times 3^t,$$

since there are $\binom{n}{t}$ ways to choose which $t$ sites are affected and $3^t$ choices of Pauli operator ($X$, $Y$, or $Z$) at each site.

**The Hamming bound.** For a code to correct all weight-$\leq t$ errors, the cosets of correctable errors must fit inside the full error space without overlapping:

$$\sum_{j=0}^{t}\binom{n}{j} 3^j \leq 2^{n-k}.$$

This is a pure combinatorial inequality: the left side counts how many distinguishable error syndromes the code must accommodate; the right side is the size of the syndrome space.

**Syndrome = macrostate.** A syndrome measurement projects the physical system onto a coset of the stabilizer group. Multiple distinct Pauli error patterns (microstates) produce the same syndrome (macrostate) — exactly the structure of $\Omega$. The decoder's job is to infer which microstate caused the measured macrostate and apply a correction. When two or more distinct errors give the same syndrome, the code is degenerate, and the multiplicity of the syndrome is exactly $\Omega > 1$.

**Fault-tolerance threshold.** The probability that at least $t+1$ errors occur among $n$ gate operations, each with error rate $p$, is bounded by the binomial tail:

$$P(\text{failure}) \leq \binom{n}{t+1} p^{t+1}.$$

Below the threshold error rate $p_\text{th}$, this is exponentially suppressed by concatenation — each level of concatenation replaces $p$ by $\sim p^2 / p_\text{th}$. The binomial coefficient counts the ways failure can occur; the exponential suppression is the same structure as the tunneling suppression in M-13.

---

## Conventions and pitfalls

**Distinguishable vs. identical: the most consequential modeling choice.** Labeled spins (distinguishable by position) → combinations $\binom{N}{N_\uparrow}$. Identical quantum particles → must apply symmetrization → smaller $\Omega$ (FD) or different counting (BE). Applying classical counting to identical quantum particles is the standard error in Chapter 10 problems.

**Stars and bars vs. combinations.** $\binom{n}{k}$ counts choosing $k$ from $n$ distinguishable objects with no repetition. $\binom{q+N-1}{q}$ counts distributing $q$ *identical* quanta among $N$ distinguishable bins with repetition allowed. These are physically different situations; the formulas are not interchangeable.

**When to use the leading vs. refined Stirling.** The leading form $\ln N! \approx N\ln N - N$ is exact in the thermodynamic limit ($N \sim 10^{23}$) to within one part in $10^{23}$. For small $N$ (a 5-qubit code), the error is $O(\ln N)$ and matters; use the refined form or exact factorials.

**Notation.** Some texts write $W$ (Boltzmann's original Wahrscheinlichkeit) rather than $\Omega$. The tombstone equation is $S = k\log W$. Same object, different letter. The form $S = k\ln\Omega$ with the Boltzmann constant $k$ and the natural logarithm is the convention used throughout this series.

**Log base.** Boltzmann entropy uses $\ln$ (natural log) with $k = 1.381 \times 10^{-23}\ \mathrm{J/K}$. Shannon entropy uses $\log_2$ with the result in bits. Von Neumann entropy $S = -\mathrm{Tr}(\rho\log\rho)$ uses $\ln$ in physics contexts. The physics is identical; only the constant of proportionality changes.

**The Gibbs $N!$ factor.** For $N$ identical classical particles, you must divide the naive multiplicity by $N!$ to avoid counting permutations of identical molecules as distinct microstates (the Gibbs paradox). Quantum mechanics handles this automatically via symmetrization. If you are working with a classical gas of identical molecules and your entropy is non-extensive, you forgot the $N!$.

---

## Quick practice

1. **Enumerate, then formula.** A system has $N = 4$ labeled spins. List all microstates with $N_\uparrow = 2$ by hand (there should be 6). Confirm with $\binom{4}{2}$. Now compute $\Omega(4,2)/2^4$ — what fraction of all microstates have exactly two spins up?

2. **Stirling at work.** Use the leading Stirling approximation to compute $\ln\binom{20}{10}$ analytically. Then compute the exact value (either by hand or noting $\binom{20}{10} = 184{,}756$) and report the relative error. At what $N$ does the relative error become negligible for thermodynamic purposes?

3. **Syndrome counting.** A $[[5,1,3]]$ quantum code encodes 1 logical qubit in 5 physical qubits and corrects all weight-1 errors. (a) How many distinct weight-1 Pauli errors are there? (b) How many distinct weight-0 errors (no error)? (c) Does the Hamming bound $\sum_{j=0}^{1}\binom{5}{j}3^j \leq 2^{5-1}$ hold? (d) What does it mean physically if the bound is saturated exactly?

---

## Go deeper

For the full derivation with examples in the two-state paramagnet, Einstein solid, free expansion, and Boltzmann distribution: *Mathematics for Physics, Vol. 2*, Ch. 9 (the source chapter for this module). For the physical consequences of quantum statistics: QM Series Vol. II, Ch. 10. For error correction: Vol. IV, Ch. 9.

---

## References

- L. Boltzmann, "Über die Beziehung zwischen dem zweiten Hauptsatze der mechanischen Wärmetheorie und der Wahrscheinlichkeitsrechnung," *Wiener Berichte* 76 (1877), pp. 373–435 — microstate counting and $S \propto \ln W$. [verify]
- M. Planck, *Vorlesungen über die Theorie der Wärmestrahlung* (1906) — the constant $k$ named for Boltzmann and the form $S = k\log W$.
- J. Stirling, *Methodus Differentialis* (1730) — the asymptotic factorial series identifying $C = \sqrt{2\pi}$ in Stirling's formula.
- A. R. Calderbank and P. W. Shor, "Good quantum error-correcting codes exist," *Physical Review A* 54 (1996), pp. 1098–1105 — quantum error correction; combinatorial counting of syndrome spaces. [verify]
- D. Gottesman, "Stabilizer Codes and Quantum Error Correction," Ph.D. thesis, Caltech (1997) — the stabilizer formalism; syndrome as macrostate. [verify]
- D. V. Schroeder, *An Introduction to Thermal Physics* — standard modern treatment of the two-state paramagnet and Einstein solid (specific chapter and edition: [verify]).
- B. Pascal, *Traité du triangle arithmétique* (1665, posthumous); earlier appearances in Yang Hui (c. 1238–1298) and al-Karaji (c. 953–c. 1029).
