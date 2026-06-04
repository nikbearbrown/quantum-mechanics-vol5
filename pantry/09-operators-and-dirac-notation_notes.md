# Research Notes: Module M-09 — Operators and Dirac Notation
**Optional companion module.** Refresher for QM chapters: II·1–II·3
**Condensed from:** `_lib_mfp2-05-operators-inner-products-and-dirac-notation.md`
**Generated:** 2026-06-03

---

## A. The tool (key results condensed)

### Bra–ket notation (Dirac, 1939)

Split the inner product $\langle\phi|\psi\rangle$ into two objects:
- **Ket** $|\psi\rangle$: a vector in the Hilbert space $V$.
- **Bra** $\langle\phi|$: a linear functional in the dual space $V^*$ — a machine that eats a ket and returns the number $\langle\phi|\psi\rangle$.

The inner product sets up the correspondence $|\phi\rangle \leftrightarrow \langle\phi|$, which is **anti-linear**: the bra corresponding to $a|\phi\rangle$ is $a^*\langle\phi|$.

**Grammar rules (type discipline):**
- $\langle\phi|\psi\rangle$: bra × ket = **scalar** (a complex number)
- $|\psi\rangle\langle\phi|$: ket × bra = **operator** (acts on any ket; $|\psi\rangle\langle\phi|$ applied to $|\chi\rangle$ gives $\langle\phi|\chi\rangle|\psi\rangle$)
- $\hat A|\psi\rangle$: operator × ket = **ket**

Knowing what type each expression is prevents the majority of algebraic errors.

### The adjoint

The **adjoint** $\hat A^\dagger$ is defined by:
$$\langle\phi|\hat A\psi\rangle = \langle\hat A^\dagger\phi|\psi\rangle \quad \text{for all }|\phi\rangle,|\psi\rangle$$
For matrices: $(\hat A^\dagger)_{ij} = A_{ji}^*$ (conjugate transpose). Rules:
- $(\hat A\hat B)^\dagger = \hat B^\dagger\hat A^\dagger$ (reverse order)
- $(c\hat A)^\dagger = c^*\hat A^\dagger$ (conjugate the scalar)
- $(|\psi\rangle\langle\phi|)^\dagger = |\phi\rangle\langle\psi|$ (swap and conjugate)

### Hermitian operators ($\hat A^\dagger = \hat A$)

Observable operators. Can be moved freely across the inner product: $\langle\phi|\hat A\psi\rangle = \langle\hat A\phi|\psi\rangle$.

**Real eigenvalues** (two-line proof): sandwich in the eigenstate: $\langle a|\hat A|a\rangle = a\langle a|a\rangle$. The left side equals its own conjugate (Hermiticity), so $a\langle a|a\rangle$ is real, hence $a \in \mathbb{R}$.

**Orthogonal eigenvectors** (two-line proof): for $\hat A|a\rangle = a|a\rangle$ and $\hat A|b\rangle = b|b\rangle$ with $a \neq b$, evaluate $\langle b|\hat A|a\rangle$ two ways. Acting right: $a\langle b|a\rangle$. Acting left (Hermiticity): $b\langle b|a\rangle$. Subtract: $(a-b)\langle b|a\rangle = 0$, so $\langle b|a\rangle = 0$.

**Spectral decomposition:**
$$\hat A = \sum_n a_n|a_n\rangle\langle a_n|$$
The operator is literally the sum of (eigenvalue) × (projector onto eigenstate). This plus the resolution of the identity are the two forms of the same fact.

### Unitary operators ($\hat U^\dagger\hat U = \hat I$, i.e., $\hat U^\dagger = \hat U^{-1}$)

These preserve inner products: $\langle\hat U\phi|\hat U\psi\rangle = \langle\phi|\hat U^\dagger\hat U|\psi\rangle = \langle\phi|\psi\rangle$. Since probabilities are squared norms, unitary operators preserve probabilities. Time evolution $\hat U(t) = e^{-i\hat Ht/\hbar}$ is unitary when $\hat H$ is Hermitian — this is why probability is conserved in Schrödinger evolution.

### The resolution of the identity (central workhorse)

In an orthonormal basis $\{|n\rangle\}$:
$$\hat I = \sum_n|n\rangle\langle n|$$
Inserting $\hat I$ in this form is the main calculational move for changing basis, extracting components, and deriving the Born rule. In the continuous case (position basis): $\hat I = \int|x\rangle\langle x|\,dx$, with $\langle x|x'\rangle = \delta(x-x')$ (requires M-06 for the delta).

### Expectation values and Born rule

For normalized $|\psi\rangle = \sum_n c_n|a_n\rangle$ with $c_n = \langle a_n|\psi\rangle$:
- Probability of outcome $a_n$: $|c_n|^2 = |\langle a_n|\psi\rangle|^2$ (Born rule — a squared inner product)
- Expectation value: $\langle\hat A\rangle = \langle\psi|\hat A|\psi\rangle = \sum_n a_n|c_n|^2$

If $\hat A$ is Hermitian, $\langle\hat A\rangle$ is guaranteed real. **Diagnostic:** if your expectation value is complex, you dropped a dagger when forming the bra.

### Commutators and the uncertainty structure

$$[\hat A, \hat B] = \hat A\hat B - \hat B\hat A$$

Key properties:
- $[\hat A, \hat B] = -[\hat B, \hat A]$ (antisymmetric)
- $[\hat A, \hat B\hat C] = [\hat A,\hat B]\hat C + \hat B[\hat A,\hat C]$ (Leibniz rule)
- If $[\hat A, \hat B] = 0$: share a common eigenbasis, can be measured simultaneously with arbitrary sharpness.
- If $[\hat A, \hat B] \neq 0$: cannot be simultaneously diagonalized; measuring one disturbs the other.

**Canonical commutator:** $[\hat x, \hat p] = i\hbar$ (derived by acting on a test function: $[\hat x,-i\hbar\partial_x]\psi = i\hbar\psi$).

**Robertson uncertainty relation** (from Cauchy–Schwarz):
$$\sigma_A\,\sigma_B \geq \tfrac12\big|\langle[\hat A,\hat B]\rangle\big|$$
Derivation: define $|f\rangle = \delta\hat A|\psi\rangle$, $|g\rangle = \delta\hat B|\psi\rangle$ where $\delta\hat A = \hat A - \langle\hat A\rangle$. Apply Cauchy–Schwarz: $\|f\|^2\|g\|^2 \geq |\langle f|g\rangle|^2$. The imaginary part of $\langle f|g\rangle$ gives $\frac{1}{2i}\langle[\hat A,\hat B]\rangle$, leading to the bound. This is a statement about **state preparation** — how concentrated a state can be in two observables at once — not about measurement disturbance.

For $[\hat x,\hat p] = i\hbar$: $\sigma_x\sigma_p \geq \hbar/2$.

### Worked example: the $-i$ in $\hat p$ is load-bearing

$\hat p = -i\hbar\partial_x$. Check Hermiticity on $L^2$: integrate by parts,
$$\langle\phi|\hat p\psi\rangle = \int\phi^*(-i\hbar)\partial_x\psi\,dx = \underbrace{[-i\hbar\phi^*\psi]_{-\infty}^\infty}_{=\,0} + \int(-i\hbar\partial_x\phi)^*\psi\,dx = \langle\hat p\phi|\psi\rangle$$
The conjugation $(-i)^* = +i$ flips the sign that integration by parts introduced. A bare $\partial_x$ is anti-Hermitian; the $-i$ makes momentum a genuine observable.

---

## B. Where the quantum series uses it

**II·1 (formalism):** M-09 is the formalism. States as kets, observables as Hermitian operators, measurement as the Born rule applied to inner products, time evolution as a unitary operator — all of this is exactly what the chapter develops. The resolution of the identity in the position basis gives the wavefunction $\psi(x) = \langle x|\psi\rangle$. The resolution in the momentum basis gives the momentum-space wavefunction, connecting to M-06 (Fourier transform).

**II·2 (observables):** The spectral decomposition $\hat A = \sum a_n|a_n\rangle\langle a_n|$ is the chapter's working definition of an observable. Expectation values via $\langle\psi|\hat A|\psi\rangle$, variance $\langle\hat A^2\rangle - \langle\hat A\rangle^2$, and the Robertson uncertainty relation all live here.

**II·3 (Schrödinger equation / time evolution):** The time-evolution operator $\hat U(t) = e^{-i\hat Ht/\hbar}$ is unitary (because $\hat H$ is Hermitian). Its action: $|\psi(t)\rangle = \hat U(t)|\psi(0)\rangle$. In the energy eigenbasis (spectral decomposition of $\hat H$), each component picks up a phase $e^{-iE_nt/\hbar}$. This is the Fourier-mode expansion in time, connecting to M-06.

---

## C. Connections

**Earlier math modules needed:**
- M-07 (vector spaces and inner products): M-09 lives entirely on the inner-product structure. The adjoint definition $\langle\phi|\hat A\psi\rangle = \langle\hat A^\dagger\phi|\psi\rangle$ requires the inner product. The Cauchy–Schwarz inequality used in the Robertson derivation is in M-07.
- M-08 (eigenvalues and diagonalization): the spectral decomposition, eigenvalue equation, and orthogonality of eigenstates are established in M-08 and here deployed in operator language.
- M-06 (Fourier transform): the continuous position/momentum bases require the delta function ($\langle x|x'\rangle = \delta(x-x')$) and the Fourier transform ($\langle x|p\rangle = e^{ipx/\hbar}/\sqrt{2\pi\hbar}$). The resolution of the identity in the continuous case is the Fourier inversion formula in disguise.

**QM chapters unlocked by M-09:**
- II·1–II·3: these chapters are the QM version of M-09. The module is a prerequisite in almost every sense.
- III·1 (perturbation theory): matrix elements $\langle n|H'|m\rangle$ in Dirac notation, the resolvent $(E_n^{(0)} - H_0)^{-1}$ as an operator.
- IV·2 (entanglement): partial traces and reduced density matrices use $\langle\phi_B|\hat\rho|\phi_B\rangle$ and require adjoint manipulation.

---

## D. Conventions and pitfalls

1. **Anti-linearity of the bra.** The bra dual to $a|\phi\rangle$ is $a^*\langle\phi|$. Students who treat it as linear will get the sign or phase wrong in every calculation involving complex coefficients. The symptom: a complex expectation value for a Hermitian operator.

2. **Order matters absolutely.** $|\psi\rangle\langle\phi|$ (operator) and $\langle\phi|\psi\rangle$ (scalar) are completely different objects in the same notation. Students confuse them most often when both appear in the same expression.

3. **The adjoint reverses order.** $(\hat A\hat B)^\dagger = \hat B^\dagger\hat A^\dagger$. Students write $(\hat A\hat B)^\dagger = \hat A^\dagger\hat B^\dagger$ by analogy with scalars. The consequence: computing $\langle\psi|\hat A\hat B|\psi\rangle$ incorrectly.

4. **Hermitian vs. self-adjoint in infinite dimensions.** In finite dimensions they coincide. In infinite dimensions an operator can be symmetric ($\langle\phi|\hat A\psi\rangle = \langle\hat A\phi|\psi\rangle$ on a dense domain) without being self-adjoint (requires additionally that domain of $\hat A$ = domain of $\hat A^\dagger$). The momentum operator on a half-line is symmetric but not self-adjoint. The module should flag this caveat; the real-spectrum theorem holds for genuinely self-adjoint operators.

5. **Measurement disturbance vs. Robertson.** Robertson $\sigma_A\sigma_B \geq \frac12|\langle[\hat A,\hat B]\rangle|$ is about state preparation, not clumsy measurement. The measurement-disturbance version is a separate theorem (Ozawa 2003). Students conflate them routinely (documented in Singh & Marshman PER).

6. **The momentum operator's $-i$:** dropping the $-i$ (or getting its sign wrong) makes $\hat p$ anti-Hermitian. This is not a typo; it is the physical content. Worth a dedicated diagnostic.

---

## E. Teaching considerations

**Where students stumble (documented in Singh & Marshman PER):**

- **Translating between notations.** The same calculation in abstract Dirac notation, matrix notation, and position-space integral form often looks like three different problems to students. They learn one representation and cannot switch. The source's Example 1 (spin along $x$ done all three ways in parallel) is the right pedagogical structure.

- **Complex expectation values as a diagnostic.** Students who compute $\langle\hat p\rangle$ and get a complex number often accept it. Training the reflex "complex expectation value of a Hermitian operator = dropped conjugate" pays immediate dividends in II·2.

- **The resolution of the identity as an active tool.** Students see $\hat I = \sum|n\rangle\langle n|$ stated and then never use it. The exercise of inserting it into an expression to derive something — e.g., deriving the position-space wavefunction from $\psi(x) = \langle x|\hat I|\psi\rangle = \int\langle x|x'\rangle\langle x'|\psi\rangle\,dx'$ — turns the identity from decoration to weapon.

- **Commutators as algebra.** $[\hat x, \hat p] = i\hbar$ is often just accepted. The derivation by acting on a test function is two lines and demystifies both the $i\hbar$ and why computing commutators requires acting on something.

- **Robertson vs. Fourier bandwidth.** Both produce $\sigma_x\sigma_p \geq \hbar/2$; students think they are the same theorem stated twice. The module should mark: Robertson is an operator theorem (Cauchy–Schwarz on inner products + commutator algebra); Fourier bandwidth is a theorem about transform pairs. They agree on the position–momentum case because $p = \hbar k$, but diverge on energy–time.

- **Gram–Schmidt and degenerate eigenstates.** When an eigenvalue is degenerate, any basis for the eigenspace is valid — but they must be orthonormalized to use the spectral decomposition or the Born rule correctly. Students often skip this step.

---

## F. Source file used

`_lib_mfp2-05-operators-inner-products-and-dirac-notation.md`

Chapter covers: inner-product axioms (physicist convention); Cauchy–Schwarz (with proof); orthonormal bases and Gram–Schmidt; resolution of the identity; Dirac bra–ket notation (historical note: Dirac 1939, standardized in 3rd ed. of *Principles* 1947); bra as dual-space functional; type grammar (scalar vs. operator); adjoint (definition, rules, matrix form); Hermitian operators (definition + both central theorems derived); unitary operators (inner-product preservation, unitarity of $e^{-i\hat Ht/\hbar}$); infinite-dimensional caveat (Hermitian vs. self-adjoint; Reed–Simon); expectation values (derivation from Born rule via resolution of the identity); commutators (definition, Leibniz, canonical $[\hat x,\hat p]=i\hbar$); Robertson uncertainty relation (full derivation from Cauchy–Schwarz); worked examples: $\sigma_x$ done three ways, $\hat p = -i\hbar\partial_x$ Hermiticity by parts, canonical commutator derivation.

---

## G. Gaps and flags

- **Continuous spectrum / generalized eigenstates.** The source treats finite-dimensional or discrete spectra for the theorems. Position and momentum have continuous spectra; their "eigenstates" $|x\rangle$ and $|p\rangle$ are not normalizable (they are not in $L^2$, but in a larger "rigged Hilbert space"). The module needs a brief note that the spectral theorem extends to continuous spectra with $\langle x|x'\rangle = \delta(x-x')$ replacing $\langle m|n\rangle = \delta_{mn}$, and that the Born rule for continuous observables gives probability densities, not probabilities.

- **Functions of operators.** The source does not cover $f(\hat A)$ defined via the spectral decomposition. Essential for time evolution $e^{-i\hat Ht/\hbar}$ in II·3. Recommend a short add-on: in the eigenbasis, $f(\hat A) = \sum_n f(a_n)|a_n\rangle\langle a_n|$.

- **Tensor products and partial trace.** Not in the source. Needed for IV·2 (entanglement) and IV·6 (open systems). The module should flag these topics as extensions handled in the QM chapters themselves.

- **Superoperators / Lindblad.** Completely outside the source's scope. IV·6 readers will need the concept of a map on density matrices (a superoperator). Not addressable within this module; must be handled in IV·6 directly.

- **Source fact-check flags inherited:** the Hilbert 1904–1910 span of venues is flagged as unverified in the source's own fact-check notes. Not load-bearing for the module content.

- **Robertson vs. Ozawa.** The source correctly cites Ozawa 2003 for the measurement-disturbance version. Worth including in the module as a "see also" to prevent conflation.
