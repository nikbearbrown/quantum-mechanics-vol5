# Research Notes: Module M-12 — Matrices, Determinants, and Linear Systems

**Optional companion module.** Refresher for QM chapters: II·7 (spin), IV·1 (density matrix), IV·4 (quantum gates)
**Condensed from:** `_lib_mfp1-10-linear-systems-and-matrices.md`
**Generated:** 2026-06-03

---

## A. The tool (key results condensed; the formulas that matter; a worked example)

### A1. What a matrix is and what it does

A matrix is a rectangular array of numbers that encodes a linear system of equations. For a 2×2 system:

$$\begin{pmatrix} a_{11} & a_{12} \\ a_{21} & a_{22}\end{pmatrix}\begin{pmatrix}x\\y\end{pmatrix} = \begin{pmatrix}b_1\\b_2\end{pmatrix}$$

In QM, the "system" is often: what are the components of a state in a given basis? Or: what does an operator do to a state? The matrix encodes the operator; the column vector encodes the state.

The subscript convention: a_{ij} = element in row i, column j. The product AB has (AB)_{ij} = Σ_k A_{ik} B_{kj}. Matrix multiplication is not commutative: AB ≠ BA in general. The commutator [A,B] = AB - BA measures the failure of commutativity — in QM this quantity is central (it is ℏ times the structure constants of the symmetry algebra for the Pauli matrices).

### A2. The determinant — what it is and why it matters

For a 2×2 matrix:

$$\det A = \begin{vmatrix} a_{11} & a_{12} \\ a_{21} & a_{22}\end{vmatrix} = a_{11}a_{22} - a_{12}a_{21}$$

Geometric meaning: the signed area of the parallelogram spanned by the two row vectors. A zero determinant means the rows are parallel (linearly dependent) — the matrix is singular and the linear system has no unique solution.

For a 3×3 matrix, cofactor expansion along the first row:

$$\det A = a_{11}\begin{vmatrix} a_{22} & a_{23} \\ a_{32} & a_{33}\end{vmatrix} - a_{12}\begin{vmatrix} a_{21} & a_{23} \\ a_{31} & a_{33}\end{vmatrix} + a_{13}\begin{vmatrix} a_{21} & a_{22} \\ a_{31} & a_{32}\end{vmatrix}$$

The alternating ± signs are part of the definition.

**Key properties of the determinant:**
- det(AB) = det(A) det(B)
- det(A†) = (det A)* (where † is conjugate transpose)
- det(A) = 0 ↔ A is singular ↔ columns/rows are linearly dependent
- For a unitary matrix U: |det U| = 1 (because UU† = I implies det(U)det(U†) = 1)
- det(I) = 1, det(-I) = (-1)^n where n is the dimension

In QM: the determinant of a unitary operator is a phase factor e^{iφ}. Hermitian operators have real eigenvalues (their determinant, as a product of eigenvalues, is real). The characteristic polynomial det(A - λI) = 0 yields the eigenvalues.

### A3. The trace

The trace of an n×n matrix is the sum of diagonal elements:

$$\text{tr}(A) = \sum_i a_{ii} = \sum_i \lambda_i$$

where λ_i are the eigenvalues. Key properties:
- tr(AB) = tr(BA) — cyclic: tr(ABC) = tr(BCA) = tr(CAB)
- tr is basis-independent: tr(S^{-1}AS) = tr(A) for any invertible S
- tr(A†) = (tr A)*
- For a 2×2 matrix: det A = λ_1 λ_2, tr A = λ_1 + λ_2

**QM use of trace:**
- The expectation value of an observable A in state ρ: ⟨A⟩ = tr(ρA)
- tr(ρ) = 1 (normalization of density matrix)
- tr(ρ²) ≤ 1 with equality iff ρ is a pure state (ρ² = ρ)
- tr is used to compute probabilities: P(outcome a_i) = tr(P_i ρ) where P_i is the projector

### A4. Cramer's rule and solving linear systems

**Cramer's rule** gives the unique solution to Ax = b (when det A ≠ 0) as:

$$x_j = \frac{\det A_j}{\det A}$$

where A_j is A with column j replaced by the right-hand side b. Each unknown is a ratio of determinants. Conceptual value: shows exactly why det A controls solvability. Computational value: useful for 2×2 systems; slow for n > 3.

**Gaussian elimination** is the practical method: systematically eliminate unknowns by row operations until the system is upper triangular, then back-substitute. The elimination steps never change det A (up to sign if rows are swapped) — they are the machinery of LU decomposition.

**Solvability conditions:**
- det A ≠ 0: unique solution
- det A = 0 and b compatible: infinitely many solutions (the system is under-determined)
- det A = 0 and b incompatible: no solution

### A5. The 2×2 machinery — Pauli matrices and spin-½

**The Pauli matrices:**

$$\sigma_x = \begin{pmatrix}0&1\\1&0\end{pmatrix}, \quad \sigma_y = \begin{pmatrix}0&-i\\i&0\end{pmatrix}, \quad \sigma_z = \begin{pmatrix}1&0\\0&-1\end{pmatrix}$$

**Properties that matter for QM:**
- Each σ_i is Hermitian: σ_i† = σ_i (eigenvalues real: ±1)
- Each σ_i squares to the identity: σ_i² = I
- Each σ_i is traceless: tr(σ_i) = 0
- det(σ_i) = -1
- Commutation relations (the algebra of angular momentum):
  $$[\sigma_i, \sigma_j] = 2i\epsilon_{ijk}\sigma_k$$
  For example, [σ_x, σ_y] = 2iσ_z
- Anticommutation: {σ_i, σ_j} = 2δ_{ij}I

**Spin operators:** S_i = ℏ/2 σ_i. The spin-½ system has Hilbert space ℂ², states are 2-component spinors.

**Eigenstates of σ_z:**
- |↑⟩ = (1,0)^T with eigenvalue +1
- |↓⟩ = (0,1)^T with eigenvalue -1

**Eigenstates of σ_x:**
- |+x⟩ = (1,1)^T/√2 with eigenvalue +1
- |-x⟩ = (1,-1)^T/√2 with eigenvalue -1

**Rotation operator for spin:** a rotation by angle θ about axis n̂ acts on the spinor as:

$$U = e^{-i\theta\hat n\cdot\boldsymbol\sigma/2} = \cos(\theta/2)I - i\sin(\theta/2)(\hat n\cdot\boldsymbol\sigma)$$

This uses the fact that (n̂·σ)² = I. The factor of 1/2 means a 2π rotation gives U = -I (not +I) — a spinor picks up a phase of -1 under 360° rotation.

**Spectral decomposition of a Hermitian 2×2 matrix:**
Any Hermitian 2×2 matrix decomposes as A = a₀I + a·σ, where a₀ = (tr A)/2 and a = (tr(Aσ_x)/2, tr(Aσ_y)/2, tr(Aσ_z)/2). Eigenvalues are a₀ ± |a|.

### A6. The density matrix (2×2 case)

The density matrix for a spin-½ system:

$$\rho = \frac{1}{2}(I + \mathbf{r}\cdot\boldsymbol\sigma), \quad |\mathbf{r}| \leq 1$$

Properties encoded in the matrix:
- tr(ρ) = 1 (normalization) — verified: tr((1/2)I) = 1, tr((r·σ)) = 0 since Pauli matrices are traceless
- ρ† = ρ (Hermiticity) — r must be real
- ρ ≥ 0 (positive semi-definite) — equivalent to |r| ≤ 1 (the Bloch ball)
- Pure state: ρ = |ψ⟩⟨ψ|, equivalently ρ² = ρ, which forces |r| = 1 (Bloch sphere surface)
- tr(ρ²) = (1 + |r|²)/2 — equals 1 iff |r| = 1 (pure state)

Expectation value of observable σ_i:

$$\langle\sigma_i\rangle = \text{tr}(\rho\sigma_i) = r_i$$

The Bloch vector r is the expectation value vector of the spin. Reading off the expectation values from the density matrix is a trace computation.

### A7. Quantum gates — unitary 2×2 matrices

A quantum gate on a single qubit is a unitary 2×2 matrix U (UU† = I). Key single-qubit gates:

**Pauli gates** (each is its own inverse):
- X = σ_x (NOT gate): flips |0⟩↔|1⟩
- Y = σ_y
- Z = σ_z: introduces phase |1⟩ → -|1⟩

**Hadamard gate:**

$$H = \frac{1}{\sqrt{2}}\begin{pmatrix}1&1\\1&-1\end{pmatrix}$$

H² = I. Takes |0⟩ → (|0⟩+|1⟩)/√2 (superposition). The Hadamard is a rotation by π around the x+z axis.

**Phase gate:** S = diag(1, i), T = diag(1, e^{iπ/4})

**Two-qubit gate — CNOT:** acts on ℂ² ⊗ ℂ² = ℂ⁴. Matrix (in the basis |00⟩, |01⟩, |10⟩, |11⟩):

$$\text{CNOT} = \begin{pmatrix}1&0&0&0\\0&1&0&0\\0&0&0&1\\0&0&1&0\end{pmatrix}$$

The Kronecker product (tensor product) of matrices encodes operations on composite systems. If U acts on qubit 1 and V acts on qubit 2 independently: U ⊗ V.

**Computing with 2×2 matrices:** the practical toolkit for gates is: (a) matrix-vector product to apply a gate to a state, (b) matrix product to compose sequential gates, (c) Hermitian conjugate to invert a unitary gate, (d) trace to compute expectation values and probabilities.

### A8. The Kronecker delta

$$\delta_{ij} = \begin{cases}1 & i=j \\ 0 & i\neq j\end{cases}$$

This is the identity matrix's components: I_{ij} = δ_{ij}. It appears constantly in QM to express orthonormality (⟨i|j⟩ = δ_{ij}), completeness (Σ_i |i⟩⟨i| = I, which reads Σ_i (|i⟩⟨i|)_{jk} = δ_{jk}), and the contraction of indices in tensor notation.

**Do not confuse with the Dirac delta function** δ(x - x'). The Kronecker delta is for discrete indices; the Dirac delta is for continuous variables. Their roles are analogous (they both enforce "same index/argument = 1, different = 0") but they are different mathematical objects.

### A9. Worked example — eigenvalues and eigenvectors of a 2×2 Hermitian matrix

Find the eigenvalues and eigenvectors of:

$$A = \begin{pmatrix}1 & 2\\2 & -2\end{pmatrix}$$

**Step 1 — characteristic equation:**

$$\det(A - \lambda I) = \det\begin{pmatrix}1-\lambda & 2\\2 & -2-\lambda\end{pmatrix} = (1-\lambda)(-2-\lambda) - 4 = \lambda^2 + \lambda - 6 = 0$$

$$(\lambda-2)(\lambda+3) = 0 \;\Longrightarrow\; \lambda_1 = 2, \quad \lambda_2 = -3$$

Check: λ_1 + λ_2 = -1 = tr(A) ✓; λ_1 λ_2 = -6 = det(A) = -2 - 4 = -6 ✓

**Step 2 — eigenvectors:**

For λ_1 = 2: (A - 2I)v = 0 gives -v_1 + 2v_2 = 0, so v_1 = (2,1)/√5.

For λ_2 = -3: (A + 3I)v = 0 gives 4v_1 + 2v_2 = 0, so v_2 = (1,-2)/√5.

Check orthogonality: v_1 · v_2 = (2)(1) + (1)(-2) = 0 ✓ (guaranteed by Hermitian/real symmetric A).

**QM reading:** A is a Hermitian observable. Its eigenvalues ±{2,-3} are the possible measurement outcomes. After measuring and getting outcome 2, the state collapses to (2,1)^T/√5.

---

## B. Where the quantum series uses it (specific QM chapters + how)

**QM II·7 — Spin:**
- The entire chapter is 2×2 matrix algebra. The Pauli matrices are the spin operators (up to ℏ/2). States are 2-component spinors.
- Key computations: (a) eigenvalues of S_n = S·n̂ for any direction n̂, yielding ±ℏ/2; (b) rotation of spinors using U = exp(-iθn̂·σ/2); (c) computing ⟨S_x⟩, ⟨S_y⟩, ⟨S_z⟩ from a given spinor.
- The non-commutativity of Pauli matrices directly encodes the non-commutativity of angular momentum measurements: [S_x, S_y] = iℏS_z.

**QM IV·1 — Density Matrix:**
- The density matrix is a 2×2 Hermitian matrix for a single qubit, or 4×4 for a two-qubit system. The trace formula ⟨A⟩ = tr(ρA) is the central computational tool.
- Students need: Hermitian conjugate, trace, matrix products to compute ρ² (purity), and the Bloch sphere parametrization ρ = (I + r·σ)/2.
- The partial trace (for tracing out one qubit of a two-qubit system) is a matrix computation — not in M-12 but built on it.

**QM IV·4 — Quantum Gates:**
- Every single-qubit gate is a 2×2 unitary matrix. Two-qubit gates are 4×4 unitary matrices. Gate composition is matrix multiplication.
- Students need: matrix-vector products, matrix products, determinant (to verify unitarity), and the tensor product (Kronecker product) for multi-qubit systems.
- The Hadamard, phase, and CNOT gates are the standard examples; their matrix forms and compositions must be computable by hand for small circuits.

---

## C. Connections

- **M-08 (Eigenvalues and Diagonalization):** the spectral theorem for Hermitian matrices is the foundation for measurement in QM. M-12 provides the concrete 2×2 machinery (determinant of A - λI, solving for eigenvectors); M-08 gives the abstract theorem (real eigenvalues, orthogonal eigenvectors, spectral decomposition).
- **M-09 (Operators and Dirac Notation):** the abstract operators of QM (Ĥ, L̂², Ŝ_z...) are represented as matrices in a chosen basis. M-12 is the concrete version of M-09 — same objects, finite-dimensional matrix representation.
- **M-07 (Vectors and Vector Spaces):** spinors are vectors in ℂ². The inner product ⟨ψ|φ⟩ = Σ_i ψ_i* φ_i is the standard complex inner product; the norm squared is ⟨ψ|ψ⟩ = Σ_i |ψ_i|².
- **M-17 (Tensor Products):** the Kronecker product A ⊗ B for composite systems is the direct extension of the single-system matrices here. A two-qubit system lives in ℂ² ⊗ ℂ² ≅ ℂ⁴ and its operators are 4×4 matrices constructed as tensor products.

---

## D. Conventions and pitfalls

**Adjoint (†) vs. transpose (T) vs. complex conjugate (*).** For matrices with complex entries: the adjoint (Hermitian conjugate) A† = (A*)^T — conjugate each entry AND transpose. A Hermitian matrix satisfies A† = A. A unitary matrix satisfies UU† = U†U = I. A real symmetric matrix has A† = A^T = A, making it simultaneously Hermitian and real. The notation A† and A* means different things: never write A* when you mean A†.

**Row vector vs. column vector.** In physics, |ψ⟩ is a column vector; ⟨ψ| is a row vector (its Hermitian conjugate). The inner product ⟨φ|ψ⟩ is (row)·(column) = scalar. The outer product |ψ⟩⟨φ| is (column)·(row) = matrix. Getting this backwards produces scalars that should be matrices and vice versa.

**2×2 vs. 4×4 for two-qubit systems.** A single qubit lives in ℂ²; a two-qubit system lives in ℂ⁴. The Pauli matrices are 2×2 and act on one qubit. To have σ_x act on qubit 1 of a two-qubit system, the correct operator is σ_x ⊗ I (4×4). Writing just σ_x in a two-qubit problem is an error of dimension.

**Trace cyclicity requires the matrix product to exist.** tr(ABC) = tr(BCA) = tr(CAB) requires the matrices to be square and of the same size, or at minimum for the products to be defined. The cyclic property is not tr(ABC) = tr(ACB) — the cyclic permutation is specific.

**The determinant is multiplicative, not additive.** det(A+B) ≠ det(A) + det(B). This is the single most common algebraic error. det(αA) = α^n det(A) for an n×n matrix.

**Pauli matrix conventions.** The standard physics convention is given above. Some sources define σ_y with the opposite sign convention for the imaginary entries, or use a different ordering. Always verify [σ_x, σ_y] = 2iσ_z (physics) or [σ_x, σ_y] = iσ_z (if σ_i = σ_i/2 convention). Mixing conventions gives wrong commutators.

**The identity matrix I vs. the number 1.** In matrix equations, I is the identity matrix; 1 is a scalar. Writing "A = 1" when you mean "A = I" is dimensionally inconsistent (the identity matrix has trace n, not trace 1 for n > 1).

---

## E. Teaching considerations

**The source chapter (mfp1-10) is aimed at classical physics contexts** — static equilibrium, cable tensions, ladder problems. The matrix algebra is exactly the same machinery but applied to force balance rather than spin states. The chapter establishes: what a linear system is, why the determinant controls solvability, how Cramer's rule works, and the 3×3 extension. This is a solid foundation, but M-12 needs to explicitly bridge the physical context from classical systems to QM ones.

**The key gap in the source: complex matrices are not discussed.** The source deals entirely with real matrices (physical forces are real numbers). The Pauli matrices have complex entries (σ_y has imaginary entries); the density matrix is complex Hermitian; unitary matrices are complex. M-12 must extend the source's real-matrix machinery to complex matrices: Hermitian conjugate, complex eigenvalues of non-Hermitian operators, unitary matrices. This extension should be presented explicitly rather than assumed.

**The 2×2 case is the right starting point for QM.** The spin-½ system is the simplest non-trivial QM system. Everything in M-12 that matters for II·7 (Pauli matrices, eigenstates, rotations of spinors) can be understood with 2×2 matrices computed by hand. The chapter draft should stay in 2×2 as long as possible before moving to 4×4 (two-qubit) and n×n (general).

**Worked example structure for the module:**
1. Eigenvalues of σ_z (trivial — diagonal matrix)
2. Eigenvalues of σ_x (the first non-trivial one; introduces the characteristic polynomial)
3. Pauli matrices: verify all six commutators [σ_i, σ_j] = 2iε_{ijk}σ_k
4. Density matrix for the |+x⟩ state: compute ρ = |+x⟩⟨+x|, verify tr(ρ²) = 1
5. Gate composition: H·X·H = Z (verify by matrix multiplication)

**The determinant's geometric meaning (signed area)** is valuable intuition even in QM — it explains why det = 0 means the matrix is singular (two state vectors that are linearly dependent span zero area). Present this briefly before the formula.

**Do not derive Cramer's rule for 3×3 by cofactor expansion in a QM context.** For QM applications, the 2×2 case is the workhorse. Gaussian elimination and the characteristic polynomial are more important than Cramer's rule for computing eigensystems.

---

## F. Source file used

`/Users/bear/Documents/CoWork/bear-textbooks/books/quantum-mechanics-vol5/pantry/_lib_mfp1-10-linear-systems-and-matrices.md`

---

## G. Gaps and flags

**FLAG — source covers only real matrices.** The source chapter has no complex entries in any matrix. The Pauli matrices (which require complex entries in σ_y), density matrices, and unitary gates are all outside the scope of the source. M-12 must supply the extension to complex matrices independently. Possible approach: add a section "Complex matrices: Hermitian conjugate, unitary and Hermitian matrices" not drawn from the source.

**FLAG — tensor product (Kronecker product) not in source.** The Kronecker product A ⊗ B — needed for two-qubit gates and composite systems (IV·4) — is not in the source chapter. It is covered in M-17 (Tensor Products and Composite Systems). M-12 should either (a) not cover two-qubit gates beyond naming them, or (b) include a brief Kronecker product section cross-referenced to M-17.

**FLAG — eigenvalue computation in the source uses static physics, not QM observables.** The worked examples (pan, ladder) use the linear system machinery to find tensions, not eigenvalues of operators. The module needs explicit eigenvalue examples in a QM framing. The A9 worked example above (finding eigenvalues and eigenvectors of a 2×2 Hermitian matrix and interpreting them as measurement outcomes) is not present in the source and must be written fresh for M-12.

**GAP — the trace is not discussed in the source.** The trace of a matrix does not appear anywhere in the source chapter. Since tr is central for density matrices (IV·1), M-12 must introduce it independently.

**GAP — no complex inner product or ⟨ψ|φ⟩ notation.** The source works with real dot products for force components. The complex inner product ⟨ψ|φ⟩ = Σ_i ψ_i* φ_i and the norm ⟨ψ|ψ⟩ must be added. This is closely tied to the Hermitian conjugate gap above.
