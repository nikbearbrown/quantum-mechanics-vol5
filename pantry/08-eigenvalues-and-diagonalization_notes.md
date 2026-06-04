# Research Notes: Module M-08 — Eigenvalues and Diagonalization
**Optional companion module.** Refresher for QM chapters: II·2 (observables), III·2 (fine structure), IV·6 (open systems)
**Condensed from:** `_lib_mfp2-04-vector-spaces-eigenvalues-and-diagonalization.md`
**Generated:** 2026-06-03

---

## A. The tool (key results condensed)

### The eigenvalue problem

For a linear map $A$ (matrix or operator), find the nonzero vectors it merely stretches:
$$A\mathbf v = \lambda\mathbf v, \quad \mathbf v \neq \mathbf 0$$
$\mathbf v$ is the **eigenvector**, $\lambda$ is the **eigenvalue**. Most vectors get rotated when $A$ acts; eigenvectors are the invariant directions — $A$ acts on them like scalar multiplication.

### Where the characteristic equation comes from (the full derivation)

Rewrite as $(A - \lambda I)\mathbf v = \mathbf 0$. This homogeneous system has a nonzero solution if and only if the matrix $A - \lambda I$ is singular:
$$\det(A - \lambda I) = 0$$
This is not a recipe to memorize — it is the literal condition for a nonzero vector in the nullspace of $A - \lambda I$ to exist. The determinant vanishes exactly when there is linear dependence, which is exactly when a nonzero solution exists. The **characteristic polynomial** $p(\lambda) = \det(A-\lambda I)$ has degree $n$ for an $n\times n$ matrix; its roots are the eigenvalues. Over $\mathbb{C}$, there are always $n$ roots (counted with multiplicity).

For each eigenvalue $\lambda_j$: solve $(A - \lambda_j I)\mathbf v = \mathbf 0$ to find the eigenvector(s).

### Diagonalization

If $A$ ($n\times n$) has $n$ linearly independent eigenvectors $\mathbf v_1, \dots, \mathbf v_n$ with eigenvalues $\lambda_1, \dots, \lambda_n$: stack eigenvectors as columns of $P$, so $AP = PD$ where $D = \operatorname{diag}(\lambda_1,\dots,\lambda_n)$. Since eigenvectors are independent, $P$ is invertible:
$$A = PDP^{-1}, \qquad D = P^{-1}AP$$
In the eigenbasis, $A$ is diagonal — all couplings are gone. Not every matrix diagonalizes (defective matrices exist), but all matrices arising as Hermitian operators in QM do.

### The spectral theorem for Hermitian matrices

A complex matrix is **Hermitian** if $A^\dagger = A$ (conjugate transpose). Two central theorems, derived in the source:

**Real eigenvalues.** Let $A\mathbf v = \lambda\mathbf v$. Multiply left by $\mathbf v^\dagger$: $\mathbf v^\dagger A\mathbf v = \lambda\|\mathbf v\|^2$. The left side equals its own conjugate (because $A^\dagger = A$), so $\lambda\|\mathbf v\|^2$ is real. Since $\|\mathbf v\|^2 > 0$, $\lambda$ is real. (For real symmetric matrices: identical argument with $A^T = A$.)

**Orthogonal eigenvectors.** Take distinct eigenvalues $\lambda_1 \neq \lambda_2$, both real. Compute $\mathbf v_2^\dagger A\mathbf v_1$ two ways: acting right gives $\lambda_1\mathbf v_2^\dagger\mathbf v_1$; acting left (using $A^\dagger = A$) gives $\lambda_2\mathbf v_2^\dagger\mathbf v_1$. Subtract:
$$(\lambda_1 - \lambda_2)\mathbf v_2^\dagger\mathbf v_1 = 0$$
Since $\lambda_1 \neq \lambda_2$, the inner product $\mathbf v_2^\dagger\mathbf v_1 = 0$: eigenvectors are orthogonal. Normalize each to unit length → $P$ is unitary ($P^\dagger = P^{-1}$), and $A = PDP^\dagger$ with $D$ real diagonal.

The finite-dimensional spectral theorem: **every Hermitian matrix is diagonalizable by a unitary change of basis, with real eigenvalues.** This is the mathematical guarantee behind every observable in QM.

### Worked example: 2×2 Hermitian (Pauli matrix $\sigma_y$)

$$\sigma_y = \begin{pmatrix}0 & -i \\ i & 0\end{pmatrix}, \quad \sigma_y^\dagger = \sigma_y$$
Characteristic equation: $\lambda^2 - 1 = 0 \Rightarrow \lambda = \pm 1$. Real, despite imaginary entries — spectral theorem at work. Eigenvectors: $\mathbf v_+ = (1, i)^T/\sqrt{2}$ and $\mathbf v_- = (1,-i)^T/\sqrt{2}$. Inner product: $\mathbf v_-^\dagger\mathbf v_+ = (1,-i)\cdot(1,i)^T/2 = (1 + 1)/2 \cdot 0$... check: $(1)^*(1) + (-i)^*(i) = 1 + i^2(-1) = 1 - 1 = 0$. Orthogonal, as required.

These are the spin-$\frac12$ eigenstates along $\pm y$.

### Degenerate eigenvalues

When an eigenvalue has multiplicity $>1$, its eigenspace may have dimension $>1$. Gram–Schmidt renders any basis for that eigenspace orthonormal. The spectral theorem still holds: degenerate Hermitian matrices are still fully diagonalizable.

### Simultaneous diagonalization

Two Hermitian operators $\hat A$ and $\hat B$ share a common orthonormal eigenbasis if and only if $[\hat A, \hat B] = 0$ (commutator vanishes). This is the mathematical foundation of quantum numbers: $\hat H$, $\hat L^2$, $\hat L_z$ commute in hydrogen, so states can be simultaneously labeled by all three eigenvalues $(n, \ell, m)$.

---

## B. Where the quantum series uses it

**II·2 (observables):** Every observable is a Hermitian operator. Its possible measurement outcomes are its eigenvalues — real (spectral theorem), reproducible (measuring an eigenstate gives the same answer with certainty). Its eigenstates form an orthonormal basis (spectral decomposition). The spectral decomposition $\hat A = \sum_n a_n |a_n\rangle\langle a_n|$ is the operator written as a sum of eigenvalue-times-projector — which is immediately the resolution of the identity from M-07. Students who arrive at II·2 without having seen the spectral theorem are forced to accept real eigenvalues as an axiom rather than a theorem.

**III·2 (fine structure):** Degenerate perturbation theory. Fine structure (spin-orbit coupling, relativistic correction) lifts degeneracy in the hydrogen spectrum. The calculation requires diagonalizing the perturbation $H'$ within the degenerate subspace — literally finding the eigenvectors of a Hermitian matrix restricted to a degenerate eigenspace. This is the spectral theorem applied to a subspace. Students must know how to set up $\det(H' - E^{(1)}I) = 0$ within the degenerate block.

**IV·6 (open systems):** The density matrix $\rho$ is a Hermitian, positive-semidefinite operator with trace 1. Its eigenvalues are the classical probabilities of the ensemble's pure states (all real, all $\geq 0$, summing to 1). Diagonalizing $\rho$ gives the **preferred basis** of the open system. The Lindblad equation governs the time evolution of $\rho$; its steady states are eigenvalues of the Lindblad superoperator. Both require fluency with eigenvalues and diagonalization for operators beyond simple $2\times2$ matrices.

---

## C. Connections

**Earlier math modules needed:**
- M-07 (vector spaces and inner products): the spectral theorem proof uses inner products explicitly ($\mathbf v^\dagger A\mathbf v$, orthogonality condition $\mathbf v_2^\dagger\mathbf v_1 = 0$). Gram–Schmidt for degenerate subspaces requires inner products.
- M-01 (determinants, linear systems): the characteristic equation $\det(A-\lambda I) = 0$ and solving the resulting homogeneous system requires determinant fluency.
- M-02 (complex numbers): Hermitian matrices have complex entries; eigenvalues and eigenvectors may be complex even when eigenvalues are real.

**QM chapters unlocked by M-08:**
- II·2 (observables): fully accessible once the spectral theorem is in hand.
- III·2 (fine structure / degenerate perturbation theory): directly requires diagonalizing $H'$ within a degenerate block.
- IV·6 (open systems): density matrix eigendecomposition.
- II·1 and M-09 (Dirac notation): the spectral decomposition $\hat A = \sum a_n|a_n\rangle\langle a_n|$ is M-08 written in M-09 language.

---

## D. Conventions and pitfalls

1. **Symmetric vs. Hermitian.** Over $\mathbb{R}$, symmetric ($A^T = A$) guarantees real eigenvalues and orthogonal eigenvectors. Over $\mathbb{C}$, the correct condition is Hermitian ($A^\dagger = A$). A complex symmetric matrix ($A^T = A$, $A \neq A^\dagger$) need not have real eigenvalues. Students who carry over the real condition to complex matrices will accept a wrong answer.

2. **Why set the determinant to zero?** The source explicitly calls out that students who treat $\det(A-\lambda I)=0$ as a rule-to-memorize cannot answer "why?" The derivation — nonzero nullspace requires singularity — is the payload.

3. **Defective matrices.** Not every matrix diagonalizes. The Jordan form exists for defective matrices but is not needed for QM (Hermitian operators are never defective). The module should flag this without developing it.

4. **Eigenvalues vs. eigenvectors for repeated roots.** When the characteristic polynomial has a repeated root, the eigenspace may or may not have full dimension (algebraic vs. geometric multiplicity). For Hermitian matrices they always agree — state this explicitly.

5. **The generalized eigenvalue problem.** The normal-mode example in the source introduces $K\mathbf a = \omega^2 M\mathbf a$. In QM this appears as $H\mathbf c = E S\mathbf c$ in non-orthogonal bases. Reduce to the standard form by $M^{-1/2}KM^{-1/2}\mathbf u = \omega^2\mathbf u$ (mass-weighted). Worth a brief mention since students encounter it in molecular QM.

---

## E. Teaching considerations

**Where students stumble:**

- **Why set det = 0?** Documented in Serbin & Wawro (2024): students treat $A\mathbf v = \lambda\mathbf v$ and $\hat H|\psi\rangle = E|\psi\rangle$ as unrelated equations. Explicitly drawing the connection — both are the same characteristic-equation problem — is the module's main pedagogical job.

- **Hermitian vs. symmetric confusion.** Students from a real linear algebra course may never have seen Hermitian matrices. The Pauli matrix example (imaginary entries, real eigenvalues) is the canonical counter-expectation exercise: "it has $i$'s in it, so shouldn't the eigenvalues be complex?"

- **Orthogonality of complex eigenvectors.** Students check $\mathbf v_1\cdot\mathbf v_2$ (dot product without conjugate) rather than $\mathbf v_1^\dagger\mathbf v_2$. For real eigenvectors these agree; for complex eigenvectors they diverge. The $\sigma_y$ example exposes this immediately.

- **Degenerate perturbation theory setup.** The step from "the perturbation $H'$ acts on a degenerate subspace" to "find eigenvalues of the matrix $\langle i|H'|j\rangle$ within that subspace" is where III·2 loses students. They need to have done a $2\times2$ Hermitian diagonalization by hand at least once.

- **The spectral decomposition as a tool.** Students see $\hat A = \sum a_n|a_n\rangle\langle a_n|$ written down but do not use it. A worked example: apply the spectral decomposition to compute $f(\hat A)$ (e.g., $e^{\hat A}$) as $\sum f(a_n)|a_n\rangle\langle a_n|$ — essential for time evolution $e^{-i\hat H t/\hbar}$.

---

## F. Source file used

`_lib_mfp2-04-vector-spaces-eigenvalues-and-diagonalization.md`

Chapter covers: vector space axioms, linear independence, basis, dimension; linear transformations as matrices; determinants and singularity; the characteristic equation (full derivation); diagonalization ($A = PDP^{-1}$); defective matrices (flagged, not developed); spectral theorem proof for real symmetric and Hermitian matrices; worked examples: 2×2 symmetric, $\sigma_y$ Pauli matrix, Jones-calculus wave plate; normal modes as eigenvalue problem (including the generalized eigenvalue problem for unequal masses).

---

## G. Gaps and flags

- **Continuous spectrum.** The source treats only discrete spectra (finite-dimensional matrices). QM operators like $\hat x$ and $\hat p$ have continuous spectra with generalized eigenfunctions (not normalizable). The module should flag this: the spectral theorem for infinite-dimensional operators with continuous spectrum requires functional analysis (Reed & Simon). Practical note: the Dirac delta replaces the Kronecker delta as the "orthonormality" relation.

- **Functions of operators / matrix functions.** Computing $e^{\hat H}$ or $e^{-i\hat H t/\hbar}$ via diagonalization is not covered in the source but is needed immediately in II·2 and throughout. Add a one-paragraph note: in the eigenbasis, $f(A) = Pf(D)P^{-1}$ where $f(D)$ applies $f$ to each diagonal entry.

- **Complete sets of commuting observables (CSCO).** Simultaneous diagonalization is mentioned only in passing in the source (as the normal-modes example). The module needs to make the $[\hat A, \hat B] = 0 \Leftrightarrow$ simultaneous eigenbasis connection explicit — it is the backbone of quantum number labeling.

- **Density matrix diagonalization for IV·6.** The source does not treat positive-semidefinite matrices or trace conditions specifically. A brief note that $\rho$ is Hermitian + positive-semidefinite + $\mathrm{tr}\,\rho = 1$ means its eigenvalues are probabilities would help bridge to IV·6.

- **Unverified source citation:** Serbin & Wawro (2024) volume/pages flagged as unverified in the source's own fact-check notes. Not load-bearing for the module content.
