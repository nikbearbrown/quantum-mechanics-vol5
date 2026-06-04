# Module M-12 — Matrices, Determinants, and Linear Systems

**When you need this:** QM chapters II·7 (Spin-½), IV·1 (Density Matrices), IV·4 (Quantum Gates)

**Condensed from:** *Mathematics for Physics* Vol 1, Ch 10 (real matrix foundations); QM-critical extensions — complex matrices, Hermitian conjugate, Pauli matrices, trace, Kronecker product — authored fresh.

---

## When you need this

Spin-½ is the simplest non-trivial quantum system, and the entire chapter II·7 is 2×2 matrix algebra. The Pauli matrices are the spin operators (up to $\hbar/2$); states are two-component column vectors; measurements are eigenvalue computations; time evolution is matrix exponentiation. Chapter IV·1 (density matrices) adds the trace and the concept of a mixed state. Chapter IV·4 (quantum gates) adds unitary matrices and the tensor product for multi-qubit systems.

The Vol 1 linear-algebra foundation covers real matrices with classical mechanics examples (tensions, static equilibrium). This module lifts those foundations into the complex matrix language QM requires: Hermitian conjugate, Hermitian and unitary matrices, and the Pauli matrices as a concrete worked system. The source's mechanical examples are mentioned briefly to ground the abstract machinery; the QM examples are where the module lives.

---

## The refresher

### What a matrix is and what it does

A **matrix** is a rectangular array of numbers (real or complex). An $m \times n$ matrix $A$ has $m$ rows and $n$ columns; the entry in row $i$ and column $j$ is $A_{ij}$. A column vector with $n$ entries is an $n \times 1$ matrix.

Matrix multiplication: $(AB)_{ij} = \sum_k A_{ik}\,B_{kj}$. The product $AB$ requires the number of columns of $A$ to equal the number of rows of $B$. Matrix multiplication is **not commutative** in general: $AB \neq BA$.

The **commutator** of two matrices is

$$[A, B] = AB - BA.$$

If $[A, B] = 0$, the matrices commute — they share a common set of eigenvectors. In QM, the commutator $[\hat{A}, \hat{B}] = i\hbar\hat{C}$ encodes the uncertainty principle; for the Pauli matrices, $[\sigma_i, \sigma_j] = 2i\varepsilon_{ijk}\sigma_k$ is the algebra of angular momentum.

A **linear system** $A\mathbf{x} = \mathbf{b}$ asks: find the vector $\mathbf{x}$ such that $A$ applied to it gives $\mathbf{b}$. In QM the "system" is often: given an operator (matrix) and an eigenvalue condition, find the eigenstates.

### The determinant

For a $2 \times 2$ matrix:

$$\det A = \begin{vmatrix} a_{11} & a_{12} \\ a_{21} & a_{22}\end{vmatrix} = a_{11}a_{22} - a_{12}a_{21}.$$

**Geometric meaning:** the signed area of the parallelogram spanned by the two row vectors. Zero determinant means the rows are linearly dependent — the matrix is **singular** and $A\mathbf{x} = \mathbf{b}$ has either no solution or infinitely many.

For a $3 \times 3$ matrix, **cofactor expansion** along the top row:

$$\det A = a_{11}\begin{vmatrix} a_{22} & a_{23} \\ a_{32} & a_{33}\end{vmatrix} - a_{12}\begin{vmatrix} a_{21} & a_{23} \\ a_{31} & a_{33}\end{vmatrix} + a_{13}\begin{vmatrix} a_{21} & a_{22} \\ a_{31} & a_{32}\end{vmatrix}.$$

**Key properties:**
- $\det(AB) = \det(A)\det(B)$
- $\det(A^\dagger) = (\det A)^*$
- $\det A = 0 \Leftrightarrow A$ is singular $\Leftrightarrow$ columns/rows are linearly dependent
- $\det(\alpha A) = \alpha^n \det(A)$ for an $n\times n$ matrix (not $\alpha\det A$ — a frequent error)

**Solvability.** The system $A\mathbf{x} = \mathbf{b}$ has a unique solution when $\det A \neq 0$. Cramer's rule gives

$$x_j = \frac{\det A_j}{\det A},$$

where $A_j$ is $A$ with column $j$ replaced by $\mathbf{b}$. Useful for $2 \times 2$ systems and conceptually; for $n > 3$, use Gaussian elimination.

### Complex matrices: the Hermitian conjugate

QM requires matrices with complex entries. Two operations matter:

**Complex conjugate** $A^*$: replace each entry $A_{ij}$ with $A_{ij}^*$.

**Transpose** $A^T$: reflect entries across the diagonal, $(A^T)_{ij} = A_{ji}$.

**Hermitian conjugate (adjoint)** $A^\dagger$: conjugate and transpose simultaneously,

$$A^\dagger = (A^*)^T, \qquad (A^\dagger)_{ij} = A_{ji}^*.$$

A matrix is **Hermitian** if $A^\dagger = A$ (each entry equals the complex conjugate of its mirror). Hermitian matrices have real eigenvalues and orthogonal eigenvectors — they represent observables in QM.

A matrix is **unitary** if $U^\dagger U = U U^\dagger = I$. Unitary matrices preserve inner products and norms; they represent time evolution, rotations, and quantum gates.

Key distinctions to keep:
- $A^*$: conjugate entries, same shape
- $A^T$: transpose, no conjugation
- $A^\dagger$: conjugate transpose — the one QM uses

For **real** matrices, $A^\dagger = A^T$. For a real symmetric matrix, $A^\dagger = A$, so it is automatically Hermitian.

### The trace

The **trace** of an $n \times n$ matrix is the sum of the diagonal entries:

$$\operatorname{tr}(A) = \sum_{i=1}^n A_{ii}.$$

**Key properties:**

1. $\operatorname{tr}(AB) = \operatorname{tr}(BA)$ — cyclic invariance. More generally, $\operatorname{tr}(ABC) = \operatorname{tr}(BCA) = \operatorname{tr}(CAB)$.
2. $\operatorname{tr}(A + B) = \operatorname{tr}(A) + \operatorname{tr}(B)$
3. $\operatorname{tr}(A^\dagger) = (\operatorname{tr} A)^*$
4. The trace is **basis-independent**: $\operatorname{tr}(S^{-1}AS) = \operatorname{tr}(A)$ for any invertible $S$.
5. For a $2 \times 2$ matrix: $\operatorname{tr}(A) = \lambda_1 + \lambda_2$ and $\det(A) = \lambda_1\lambda_2$, where $\lambda_i$ are eigenvalues.

The trace is **not** the same as the determinant. $\det(A + B) \neq \det(A) + \det(B)$ and $\operatorname{tr}(AB) \neq \operatorname{tr}(A)\operatorname{tr}(B)$. These are among the most common algebraic errors.

**QM uses of the trace:**

- Expectation value of observable $\hat{A}$ in state $\rho$: $\langle \hat{A}\rangle = \operatorname{tr}(\rho \hat{A})$
- Normalization of the density matrix: $\operatorname{tr}(\rho) = 1$
- Purity: $\operatorname{tr}(\rho^2) \leq 1$, with equality iff the state is pure
- Probability of outcome $a_i$: $P(a_i) = \operatorname{tr}(\Pi_i\,\rho)$ where $\Pi_i = |a_i\rangle\langle a_i|$ is the projector

### Eigenvalues and the characteristic polynomial

The **eigenvalue equation** for matrix $A$ is $A\mathbf{v} = \lambda\mathbf{v}$: the vector $\mathbf{v}$ (the eigenvector) changes only by the scalar $\lambda$ (the eigenvalue). Rearranging:

$$(A - \lambda I)\mathbf{v} = \mathbf{0}.$$

For a non-trivial solution $\mathbf{v} \neq \mathbf{0}$ to exist, the matrix $(A - \lambda I)$ must be singular:

$$\det(A - \lambda I) = 0.$$

This is the **characteristic polynomial** of $A$, a degree-$n$ polynomial in $\lambda$ whose roots are the eigenvalues. For a $2\times 2$ matrix:

$$\det\begin{pmatrix}a_{11}-\lambda & a_{12} \\ a_{21} & a_{22}-\lambda\end{pmatrix} = \lambda^2 - \operatorname{tr}(A)\,\lambda + \det(A) = 0.$$

The coefficients encode the trace and determinant directly.

**For Hermitian $A$:** all eigenvalues are real. If $\lambda_1 \neq \lambda_2$, the corresponding eigenvectors are orthogonal: $\mathbf{v}_1^\dagger\mathbf{v}_2 = 0$. This is the finite-dimensional version of the Sturm–Liouville theorem (Module M-11) — the spectral theorem for Hermitian matrices, developed fully in Module M-08.

**Spectral decomposition.** A Hermitian matrix decomposes as

$$A = \sum_i \lambda_i\,|v_i\rangle\langle v_i|,$$

where $\{|v_i\rangle\}$ is the orthonormal eigenbasis. In QM, measurement of observable $A$ yields eigenvalue $\lambda_i$ with probability $|\langle v_i|\psi\rangle|^2$, and collapses the state to $|v_i\rangle$.

---

### The Pauli matrices and spin-½

The **Pauli matrices** are the three traceless Hermitian $2 \times 2$ matrices:

$$\sigma_x = \begin{pmatrix}0 & 1 \\ 1 & 0\end{pmatrix}, \qquad \sigma_y = \begin{pmatrix}0 & -i \\ i & 0\end{pmatrix}, \qquad \sigma_z = \begin{pmatrix}1 & 0 \\ 0 & -1\end{pmatrix}.$$

These are $\sigma_1, \sigma_2, \sigma_3$ in index notation. Together with the identity $I$, they form a basis for all $2\times 2$ Hermitian matrices: any Hermitian $2\times 2$ matrix $A$ decomposes as $A = a_0 I + \mathbf{a}\cdot\boldsymbol{\sigma}$ with real $a_0$ and $\mathbf{a}$.

**Properties to know and use:**

Each Pauli matrix is Hermitian ($\sigma_i^\dagger = \sigma_i$) and squares to the identity ($\sigma_i^2 = I$). Each has eigenvalues $\pm 1$ and is traceless ($\operatorname{tr}(\sigma_i) = 0$) with $\det(\sigma_i) = -1$.

**Commutation relations** (the algebra of SU(2), hence of angular momentum):

$$[\sigma_i, \sigma_j] = 2i\,\varepsilon_{ijk}\,\sigma_k,$$

where $\varepsilon_{ijk}$ is the Levi-Civita symbol ($+1$ for even permutations of $xyz$, $-1$ for odd). Explicitly:

$$[\sigma_x, \sigma_y] = 2i\sigma_z, \qquad [\sigma_y, \sigma_z] = 2i\sigma_x, \qquad [\sigma_z, \sigma_x] = 2i\sigma_y.$$

**Anticommutation relations:**

$$\{\sigma_i, \sigma_j\} = \sigma_i\sigma_j + \sigma_j\sigma_i = 2\delta_{ij}I.$$

Combined: $\sigma_i\sigma_j = \delta_{ij}I + i\varepsilon_{ijk}\sigma_k$.

**Spin operators.** The spin-½ angular momentum operators are $\hat{S}_i = (\hbar/2)\sigma_i$. The spin-½ Hilbert space is $\mathbb{C}^2$; states are two-component column vectors (spinors).

**Eigenstates of $\sigma_z$:**

$$|{\uparrow}\rangle = \begin{pmatrix}1\\0\end{pmatrix} \;\text{(spin up, eigenvalue }+1), \qquad |{\downarrow}\rangle = \begin{pmatrix}0\\1\end{pmatrix} \;\text{(spin down, eigenvalue }-1).$$

**Eigenstates of $\sigma_x$:**

$$|{+x}\rangle = \frac{1}{\sqrt{2}}\begin{pmatrix}1\\1\end{pmatrix} \;\text{(eigenvalue }+1), \qquad |{-x}\rangle = \frac{1}{\sqrt{2}}\begin{pmatrix}1\\-1\end{pmatrix} \;\text{(eigenvalue }-1).$$

**Eigenstates of $\sigma_y$:**

$$|{+y}\rangle = \frac{1}{\sqrt{2}}\begin{pmatrix}1\\i\end{pmatrix} \;\text{(eigenvalue }+1), \qquad |{-y}\rangle = \frac{1}{\sqrt{2}}\begin{pmatrix}1\\-i\end{pmatrix} \;\text{(eigenvalue }-1).$$

**Spin-$\hat{n}$ component.** For any unit vector $\hat{n} = (\sin\theta\cos\phi, \sin\theta\sin\phi, \cos\theta)$, the operator $\hat{n}\cdot\boldsymbol{\sigma}$ has eigenvalues $\pm 1$ and eigenstates:

$$|{+\hat{n}}\rangle = \begin{pmatrix}\cos(\theta/2) \\ e^{i\phi}\sin(\theta/2)\end{pmatrix}, \qquad |{-\hat{n}}\rangle = \begin{pmatrix}-e^{-i\phi}\sin(\theta/2) \\ \cos(\theta/2)\end{pmatrix}.$$

**Rotation of spinors.** A rotation by angle $\alpha$ about axis $\hat{n}$ acts on the spinor as:

$$U = e^{-i\alpha\hat{n}\cdot\boldsymbol{\sigma}/2} = \cos(\alpha/2)\,I - i\sin(\alpha/2)\,(\hat{n}\cdot\boldsymbol{\sigma}).$$

This uses $(\hat{n}\cdot\boldsymbol{\sigma})^2 = I$. The factor $1/2$ means a $2\pi$ rotation gives $U = -I$, not $+I$: a spinor picks up a phase of $-1$ under a full rotation. This is the mathematical signature of spin-½ and has no classical analogue.

### The density matrix

A **pure state** $|\psi\rangle$ defines a **density matrix** $\rho = |\psi\rangle\langle\psi|$ — a rank-1 Hermitian positive semi-definite matrix with $\operatorname{tr}(\rho) = 1$ and $\rho^2 = \rho$.

A **mixed state** is a statistical mixture: $\rho = \sum_i p_i |\psi_i\rangle\langle\psi_i|$ with $p_i \geq 0$ and $\sum_i p_i = 1$. For a single qubit, the general density matrix is

$$\rho = \frac{1}{2}(I + \mathbf{r}\cdot\boldsymbol{\sigma}), \qquad |\mathbf{r}| \leq 1.$$

The vector $\mathbf{r}$ is the **Bloch vector**. Its coordinates are the spin expectation values: $r_i = \langle\sigma_i\rangle = \operatorname{tr}(\rho\sigma_i)$. Pure states live on the **Bloch sphere** ($|\mathbf{r}| = 1$); mixed states live inside it.

Properties encoded in the density matrix:
- $\operatorname{tr}(\rho) = 1$: normalization — the probabilities sum to 1
- $\rho^\dagger = \rho$: Hermiticity — $\mathbf{r}$ must be real
- $\rho \geq 0$: positive semi-definite — eigenvalues non-negative, equivalent to $|\mathbf{r}| \leq 1$
- $\operatorname{tr}(\rho^2) = (1 + |\mathbf{r}|^2)/2$: equals 1 iff $|\mathbf{r}| = 1$ (pure state), less than 1 for mixed states

**Expectation value** of any observable $\hat{A}$:

$$\langle\hat{A}\rangle = \operatorname{tr}(\rho\,\hat{A}).$$

This is the fundamental formula for computing predictions from a density matrix — including when the state is mixed and no single wavefunction describes it.

### Quantum gates: unitary matrices

A **quantum gate** on a single qubit is a $2\times 2$ unitary matrix $U$ ($UU^\dagger = I$). Gates are applied by matrix-vector multiplication: $|\psi'\rangle = U|\psi\rangle$. Sequential gates compose by matrix multiplication: applying $V$ then $U$ gives $UV|\psi\rangle$.

**Standard single-qubit gates:**

Pauli gates — each is its own inverse (Hermitian and unitary):
$$X = \sigma_x = \begin{pmatrix}0&1\\1&0\end{pmatrix}, \qquad Y = \sigma_y = \begin{pmatrix}0&-i\\i&0\end{pmatrix}, \qquad Z = \sigma_z = \begin{pmatrix}1&0\\0&-1\end{pmatrix}.$$

Hadamard gate:
$$H = \frac{1}{\sqrt{2}}\begin{pmatrix}1 & 1 \\ 1 & -1\end{pmatrix}.$$

$H^2 = I$ (self-inverse). $H|0\rangle = (|0\rangle + |1\rangle)/\sqrt{2}$ — the Hadamard creates equal superposition.

Phase gate $S = \operatorname{diag}(1, i)$, $T$-gate $T = \operatorname{diag}(1, e^{i\pi/4})$: these add phases without changing the populations.

**Computing with gates.** The practical toolkit:

1. Matrix-vector product: apply a gate to a state $|\psi\rangle = \alpha|0\rangle + \beta|1\rangle = \begin{pmatrix}\alpha\\\beta\end{pmatrix}$.
2. Matrix product: compose sequential gates ($U_2 U_1$ applies $U_1$ first).
3. Hermitian conjugate: invert a unitary gate ($U^{-1} = U^\dagger$).
4. Trace: compute expectation values and probabilities.

### The Kronecker product for composite systems

A two-qubit system lives in $\mathbb{C}^2 \otimes \mathbb{C}^2 \cong \mathbb{C}^4$. The **Kronecker product** (matrix tensor product) $A \otimes B$ encodes operators on composite systems:

$$(A \otimes B)_{(ik),(j\ell)} = A_{ij}\,B_{k\ell}.$$

Explicitly, for $2\times 2$ matrices:

$$A \otimes B = \begin{pmatrix}a_{11}B & a_{12}B \\ a_{21}B & a_{22}B\end{pmatrix}.$$

**Example.** $\sigma_z \otimes I$ (the $z$-spin of qubit 1 in a two-qubit system):

$$\sigma_z \otimes I = \begin{pmatrix}1&0&0&0\\0&1&0&0\\0&0&-1&0\\0&0&0&-1\end{pmatrix}.$$

**The CNOT gate** (controlled-NOT, the key two-qubit gate):

$$\text{CNOT} = \begin{pmatrix}1&0&0&0\\0&1&0&0\\0&0&0&1\\0&0&1&0\end{pmatrix}$$

in the basis $|00\rangle, |01\rangle, |10\rangle, |11\rangle$. It flips qubit 2 if and only if qubit 1 is $|1\rangle$. CNOT is not a tensor product of single-qubit gates — it is an entangling gate.

A single-qubit gate $U$ acting on qubit 1 alone is $U \otimes I$ as a $4\times 4$ matrix; acting on qubit 2 alone it is $I \otimes U$. Confusing these dimensions (writing a $2\times 2$ gate where a $4\times 4$ is needed) is a common error. The rule: $n$ qubits require $2^n \times 2^n$ matrices.

For full treatment of the tensor product and composite Hilbert spaces, see Module M-17.

---

## Worked example: eigenvalues and eigenvectors of $\sigma_x$

**Problem.** Find the eigenvalues and eigenvectors of $\sigma_x = \begin{pmatrix}0&1\\1&0\end{pmatrix}$ and interpret the result as a spin measurement.

**Step 1 — characteristic polynomial:**

$$\det(\sigma_x - \lambda I) = \det\begin{pmatrix}-\lambda & 1 \\ 1 & -\lambda\end{pmatrix} = \lambda^2 - 1 = 0.$$

Eigenvalues: $\lambda_{\pm} = \pm 1$. Check: $\operatorname{tr}(\sigma_x) = 0 = \lambda_+ + \lambda_-$ ✓; $\det(\sigma_x) = -1 = \lambda_+\lambda_-$ ✓.

**Step 2 — eigenvectors:**

For $\lambda = +1$: $(\sigma_x - I)\mathbf{v} = \mathbf{0}$ gives $\begin{pmatrix}-1&1\\1&-1\end{pmatrix}\mathbf{v} = \mathbf{0}$, so $v_1 = v_2$. Normalized: $|{+x}\rangle = \frac{1}{\sqrt{2}}\begin{pmatrix}1\\1\end{pmatrix}$.

For $\lambda = -1$: $(\sigma_x + I)\mathbf{v} = \mathbf{0}$ gives $\begin{pmatrix}1&1\\1&1\end{pmatrix}\mathbf{v} = \mathbf{0}$, so $v_1 = -v_2$. Normalized: $|{-x}\rangle = \frac{1}{\sqrt{2}}\begin{pmatrix}1\\-1\end{pmatrix}$.

**Step 3 — orthogonality check:**

$$\langle{+x}|{-x}\rangle = \frac{1}{\sqrt{2}}\begin{pmatrix}1&1\end{pmatrix}\cdot\frac{1}{\sqrt{2}}\begin{pmatrix}1\\-1\end{pmatrix} = \frac{1}{2}(1-1) = 0 \;\checkmark.$$

**Step 4 — QM interpretation.** $\sigma_x$ is a Hermitian observable (measurable). Its eigenvalues $\pm 1$ (equivalently, $S_x = \pm\hbar/2$) are the only possible outcomes of an $x$-spin measurement. After measuring $S_x = +\hbar/2$, the state collapses to $|{+x}\rangle$, a superposition of $|{\uparrow}\rangle$ and $|{\downarrow}\rangle$ in equal proportions.

**Step 5 — verify Hadamard diagonalizes $\sigma_x$.** Since $H|{+x}\rangle = |{\uparrow}\rangle$ and $H|{-x}\rangle = |{\downarrow}\rangle$, the Hadamard gate rotates between the $z$-eigenbasis and the $x$-eigenbasis. Verify: $H\,\sigma_x\,H^\dagger = \sigma_z$ (matrix multiplication: compute it explicitly as a check — it works because $H$ implements the change-of-basis between $\sigma_x$ and $\sigma_z$ eigenstates).

---

## In the quantum series

### QM II·7 — Spin-½

The entire chapter is $2\times 2$ matrix algebra. Key computations: (a) finding eigenvalues of $\hat{S}_n = \hat{\mathbf{S}}\cdot\hat{n}$ for any direction $\hat{n}$ by the characteristic polynomial; (b) computing rotation of spinors using $U = e^{-i\alpha\hat{n}\cdot\boldsymbol{\sigma}/2}$; (c) evaluating $\langle S_x\rangle$, $\langle S_y\rangle$, $\langle S_z\rangle$ for a given spinor using $\langle S_i\rangle = \langle\psi|\hat{S}_i|\psi\rangle = (\hbar/2)\langle\psi|\sigma_i|\psi\rangle$.

The non-commutativity of Pauli matrices $[\sigma_x, \sigma_y] = 2i\sigma_z$ directly encodes the non-commutativity of spin measurements: measuring $S_x$ then $S_y$ gives a different result from measuring $S_y$ then $S_x$.

### QM IV·1 — Density Matrix

The density matrix is Hermitian, positive semi-definite, and has unit trace. For a single qubit the Bloch-sphere parametrization $\rho = (I + \mathbf{r}\cdot\boldsymbol{\sigma})/2$ encodes all physical information. The trace formula $\langle A\rangle = \operatorname{tr}(\rho A)$ is the central computational tool; students need to be fluent with matrix products and the cyclic property of trace.

Purity $\operatorname{tr}(\rho^2)$: compute $\rho^2$ by matrix multiplication, then trace the result. For the Bloch parametrization: $\rho^2 = (I + \mathbf{r}\cdot\boldsymbol{\sigma})^2/4 = (1 + |\mathbf{r}|^2)I/4 + (\mathbf{r}\cdot\boldsymbol{\sigma})/2$, so $\operatorname{tr}(\rho^2) = (1 + |\mathbf{r}|^2)/2$.

### QM IV·4 — Quantum Gates

Every single-qubit gate is a $2\times 2$ unitary matrix. Gate composition is matrix multiplication; the inverse of a unitary gate is its Hermitian conjugate. Two-qubit gates are $4\times 4$ unitary matrices, constructed as Kronecker products for separable operations or directly (as the CNOT) for entangling operations.

A simple circuit to verify by hand: $H\,X\,H = Z$. Compute step by step:

$$X\,H = \begin{pmatrix}0&1\\1&0\end{pmatrix}\frac{1}{\sqrt{2}}\begin{pmatrix}1&1\\1&-1\end{pmatrix} = \frac{1}{\sqrt{2}}\begin{pmatrix}1&-1\\1&1\end{pmatrix},$$

$$H\,(XH) = \frac{1}{\sqrt{2}}\begin{pmatrix}1&1\\1&-1\end{pmatrix}\frac{1}{\sqrt{2}}\begin{pmatrix}1&-1\\1&1\end{pmatrix} = \frac{1}{2}\begin{pmatrix}2&0\\0&-2\end{pmatrix} = \begin{pmatrix}1&0\\0&-1\end{pmatrix} = Z. \;\checkmark$$

---

## Conventions and pitfalls

**$A^\dagger$ vs. $A^T$ vs. $A^*$.** These are three different operations. For matrices with complex entries: $A^\dagger = (A^*)^T$ — conjugate each entry AND transpose. Never write $A^*$ when you mean $A^\dagger$: for $\sigma_y$, the element $(1,2)$ is $-i$; its conjugate is $+i$; the $(1,2)$ element of $A^\dagger$ (which is the $(2,1)$ entry of $A^*$) is $+i$, and indeed $\sigma_y^\dagger = \sigma_y$ (Hermitian). Getting the order of operations wrong gives the wrong matrix.

**Row vs. column vectors.** In QM, $|\psi\rangle$ is a column vector; $\langle\psi|$ is its Hermitian conjugate, a row vector. The inner product $\langle\phi|\psi\rangle$ is (row) times (column) = scalar. The outer product $|\psi\rangle\langle\phi|$ is (column) times (row) = matrix (a rank-1 operator). Reversing these produces scalars where matrices are needed and vice versa.

**Determinant is not additive.** $\det(A + B) \neq \det(A) + \det(B)$. This error kills Cramer's rule computations. Also: $\det(\alpha A) = \alpha^n\det(A)$, not $\alpha\det(A)$, for an $n\times n$ matrix.

**Trace cyclicity requires valid multiplication.** $\operatorname{tr}(ABC) = \operatorname{tr}(BCA) = \operatorname{tr}(CAB)$ — cyclic, not arbitrary permutation. $\operatorname{tr}(ABC) \neq \operatorname{tr}(ACB)$ in general. The cyclic permutation also requires the product to be defined and square.

**Pauli matrix convention.** The standard physics convention is as given above: $[\sigma_x, \sigma_y] = 2i\sigma_z$. Some sources use $\sigma_i/2$ for the generators (so that the commutator is $[\sigma_i/2, \sigma_j/2] = i\varepsilon_{ijk}(\sigma_k/2)$). Mixing conventions gives wrong commutators. Verify any convention by checking $[\sigma_x, \sigma_y]$ gives $2i\sigma_z$ (physics) or $i\sigma_z$ (half-convention).

**Two-qubit dimensions.** A single qubit is $\mathbb{C}^2$; a two-qubit system is $\mathbb{C}^4$. Pauli matrices are $2\times 2$ and act on one qubit. To apply $\sigma_x$ to qubit 1 of a two-qubit system, the operator is $\sigma_x \otimes I_{2\times 2}$ — a $4\times 4$ matrix. Writing just $\sigma_x$ in a two-qubit calculation is a dimension error.

**The identity matrix $I$ vs. the scalar $1$.** In matrix equations, $I$ is the identity matrix (trace $n$ for an $n\times n$ system); $1$ is a scalar. Writing "$U^\dagger U = 1$" when you mean "$U^\dagger U = I$" is ambiguous and sometimes wrong.

---

## Quick practice

1. **Eigenvalues of $\sigma_z$.** Compute $\det(\sigma_z - \lambda I) = 0$ explicitly, find the eigenvalues, and verify that $\operatorname{tr}(\sigma_z) = \lambda_1 + \lambda_2$ and $\det(\sigma_z) = \lambda_1\lambda_2$. Write the eigenvectors and confirm they are orthogonal.

2. **Density matrix.** Compute the density matrix $\rho = |{+x}\rangle\langle{+x}|$ for the state $|{+x}\rangle = (1,1)^T/\sqrt{2}$. Verify: (a) $\operatorname{tr}(\rho) = 1$, (b) $\rho^2 = \rho$ (pure state), (c) $\langle\sigma_x\rangle = \operatorname{tr}(\rho\sigma_x) = 1$.

3. **Gate composition.** Verify by matrix multiplication that $H\,Z\,H = X$. Then compute the action of the circuit on the state $|{\uparrow}\rangle = (1, 0)^T$: first apply $H$, then $Z$, then $H$, and confirm the result equals $X|{\uparrow}\rangle = |{\downarrow}\rangle = (0,1)^T$.

---

## Go deeper

The real-matrix foundations — linear systems, determinants, Cramer's rule, Gaussian elimination — are in *Mathematics for Physics* Vol 1, Ch 10 ("Linear Systems and Matrices"), which covers the theory through $3\times 3$ systems with worked examples from classical mechanics. The QM-critical extensions in this module (complex matrices, Hermitian conjugate, Pauli matrices, trace, Kronecker product) go beyond that source and are authored fresh here.

For deeper treatment of the spectral theorem and diagonalization (the foundation for measurement theory), see Module M-08 and *Mathematics for Physics* Vol 2, Ch 4. For the tensor product and composite Hilbert spaces, see Module M-17.

---

## References

- Sylvester, J. J. "A word on nonions." Coinage of "matrix" for the rectangular array (1850). [verify exact publication]
- Cayley, A. "A Memoir on the Theory of Matrices." *Philosophical Transactions of the Royal Society* **148** (1858), pp. 17–46. [Matrix algebra as such; matrix multiplication defined here.]
- Pauli, W. "Zur Quantenmechanik des magnetischen Elektrons." *Zeitschrift für Physik* **43** (1927), pp. 601–623. [Introduction of the Pauli matrices as spin operators.] [verify]
- Dirac, P. A. M. *The Principles of Quantum Mechanics*, 4th ed. Oxford University Press, 1958. Ch. XI (spin). [The spinor formalism in Dirac's own notation.] [verify]
- Nielsen, M. A., and I. L. Chuang. *Quantum Computation and Quantum Information*. Cambridge University Press, 2000. Ch. 2 (quantum circuits, density matrices, Kronecker products). [The standard reference for quantum gates and the Bloch sphere.] [verify]
- Griffiths, D. J. *Introduction to Quantum Mechanics*, 3rd ed. Cambridge University Press, 2018. Ch. 4.4 (spin-½, Pauli matrices). [verify edition]
- Jiuzhang Suanshu (*The Nine Chapters on the Mathematical Art*), Ch. 8 (*Fangcheng*), c. 150 BCE. [Array-based Gaussian elimination, two millennia before Gauss.] [verify]
