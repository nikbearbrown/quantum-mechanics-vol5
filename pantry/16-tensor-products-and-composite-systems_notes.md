# Research Notes: Module M-16 — Tensor Products and Composite Systems
**Optional companion module.** Refresher for QM chapters: IV·2 (entanglement), IV·4 (gates), IV·5 (teleportation).
**Condensed from:** AUTHORED — no single source chapter. Extension of vector-space linear algebra (_lib_mfp2-04-vector-spaces-eigenvalues-and-diagonalization.md). Light web research conducted; sources cited in section F.
**Generated:** 2026-06-03

---

## A. The tool (key results condensed; the formulas that matter; a worked example)

### The problem this module solves
When two quantum systems are combined, the state space is not the direct sum of their individual spaces (which would just give the union of their degrees of freedom). It is the **tensor product** — a new, larger space whose dimension is the *product* (not the sum) of the individual dimensions. This is the mathematical fact that makes quantum entanglement possible and that makes quantum computing exponentially powerful in principle.

### Prerequisite: the vector space (mfp2-04)
The tensor product is a construction on vector spaces. Students need: vector space definition, basis, dimension, linear independence, linear maps as matrices, inner product. All of these are covered in mfp2-04. M-16 is an extension, not a replacement.

### The tensor product of vector spaces: definition
Let V (dimension m) and W (dimension n) be vector spaces over ℂ. Their tensor product V ⊗ W is a vector space of dimension mn, built as follows:
- For every pair (v, w) with v ∈ V, w ∈ W, there is an element v ⊗ w ∈ V ⊗ W (called a "simple tensor" or "product state")
- The construction is bilinear:
  - (αv) ⊗ w = v ⊗ (αw) = α(v ⊗ w)
  - (v₁ + v₂) ⊗ w = v₁ ⊗ w + v₂ ⊗ w
  - v ⊗ (w₁ + w₂) = v ⊗ w₁ + v ⊗ w₂
- V ⊗ W is spanned by all simple tensors, but it contains vectors that are **not** simple tensors — these are the entangled states.

### Basis ordering and the Kronecker product
If V has basis {|0⟩, |1⟩} (dim 2) and W has basis {|0⟩, |1⟩} (dim 2), then V ⊗ W has the ordered basis:
$$\{|0\rangle\otimes|0\rangle,\; |0\rangle\otimes|1\rangle,\; |1\rangle\otimes|0\rangle,\; |1\rangle\otimes|1\rangle\}$$
often written |00⟩, |01⟩, |10⟩, |11⟩. Dimension: 2 × 2 = 4.

**Convention warning**: basis ordering (which tensor factor is "first") must be fixed and stated. Different texts use different orderings. The standard in most quantum information texts is lexicographic: first index varies slowest (|00⟩, |01⟩, |10⟩, |11⟩). Some texts reverse this. Inconsistency causes sign errors in gate matrices.

### The Kronecker product of matrices
If A is an m×m matrix (acting on V) and B is an n×n matrix (acting on W), the operator A ⊗ B acts on V ⊗ W. In the lexicographic basis, its matrix is the **Kronecker product**:
$$A \otimes B = \begin{pmatrix} A_{11}B & A_{12}B & \cdots \\ A_{21}B & A_{22}B & \cdots \\ \vdots & & \ddots \end{pmatrix}$$
where each entry A_{ij}B is an n×n block. The resulting matrix is mn × mn.

**Worked example: two-qubit system**

Single qubit: V = ℂ², basis {|0⟩, |1⟩}. Two qubits: V ⊗ V = ℂ⁴, basis {|00⟩, |01⟩, |10⟩, |11⟩}.

The Pauli X matrix (bit-flip): X = [[0,1],[1,0]].

X ⊗ I (flip qubit 1, do nothing to qubit 2):
$$X \otimes I = \begin{pmatrix}0\cdot I & 1\cdot I \\ 1\cdot I & 0\cdot I\end{pmatrix} = \begin{pmatrix}0&0&1&0\\0&0&0&1\\1&0&0&0\\0&1&0&0\end{pmatrix}$$

This swaps |00⟩ ↔ |10⟩ and |01⟩ ↔ |11⟩ — flips the first qubit regardless of the second.

I ⊗ X (flip qubit 2, do nothing to qubit 1):
$$I \otimes X = \begin{pmatrix}X & 0 \\ 0 & X\end{pmatrix} = \begin{pmatrix}0&1&0&0\\1&0&0&0\\0&0&0&1\\0&0&1&0\end{pmatrix}$$

Note: A ⊗ B ≠ B ⊗ A in general (the matrices are not equal), but (A ⊗ B)(|v⟩ ⊗ |w⟩) = (A|v⟩) ⊗ (B|w⟩) is still just applying A to the first qubit and B to the second.

### Dimension grows multiplicatively
For N qubits: dim = 2^N. This is the source of quantum computing's potential power — the state space grows exponentially with the number of qubits. It is also the source of the difficulty in classical simulation: representing an N-qubit state requires 2^N complex amplitudes.

| N qubits | Dimension | Classical storage (complex doubles) |
|---|---|---|
| 1 | 2 | 2 |
| 2 | 4 | 4 |
| 10 | 1024 | ~16 kB |
| 30 | ~10⁹ | ~16 GB |
| 50 | ~10¹⁵ | ~16 PB |
| 300 | ~10⁹⁰ | more than atoms in universe |

### Separable (product) states vs. entangled states
A state |ψ⟩ ∈ V ⊗ W is **separable** (or a product state) if it can be written as |ψ⟩ = |v⟩ ⊗ |w⟩ for some |v⟩ ∈ V and |w⟩ ∈ W.

A state that cannot be written this way is **entangled**.

**The Bell states** are the canonical examples of entangled states in ℂ² ⊗ ℂ²:
$$|\Phi^+\rangle = \frac{1}{\sqrt{2}}(|00\rangle + |11\rangle)$$
$$|\Phi^-\rangle = \frac{1}{\sqrt{2}}(|00\rangle - |11\rangle)$$
$$|\Psi^+\rangle = \frac{1}{\sqrt{2}}(|01\rangle + |10\rangle)$$
$$|\Psi^-\rangle = \frac{1}{\sqrt{2}}(|01\rangle - |10\rangle)$$

**Why |Φ+⟩ is entangled (explicit argument)**: suppose |Φ+⟩ = (α|0⟩ + β|1⟩) ⊗ (γ|0⟩ + δ|1⟩) = αγ|00⟩ + αδ|01⟩ + βγ|10⟩ + βδ|11⟩. Matching coefficients: αγ = 1/√2, αδ = 0, βγ = 0, βδ = 1/√2. From αδ = 0: either α = 0 or δ = 0. If α = 0, then αγ = 0 ≠ 1/√2. If δ = 0, then βδ = 0 ≠ 1/√2. Contradiction. Therefore |Φ+⟩ is not a product state: it is entangled.

### Partial trace: discarding a subsystem
If the full system AB is in state ρ_AB (a density matrix on V ⊗ W), the **partial trace** gives the reduced state of subsystem A alone:
$$\rho_A = \text{Tr}_B[\rho_{AB}] = \sum_j (\mathbf{I} \otimes \langle j|)\,\rho_{AB}\,(\mathbf{I} \otimes |j\rangle)$$
where {|j⟩} is any orthonormal basis for W.

For the Bell state |Φ+⟩: ρ_AB = |Φ+⟩⟨Φ+|. Tracing over B:
$$\rho_A = \frac{1}{2}|0\rangle\langle 0| + \frac{1}{2}|1\rangle\langle 1| = \frac{I}{2}$$
A maximally mixed state — measuring A alone gives no information about any observable, despite the global state being a pure state. This is the signature of maximal entanglement at the linear-algebra level.

**Interpretation**: the partial trace gives the state you assign to a subsystem when you have no access to the other subsystem. It is the density matrix that correctly predicts all measurement statistics for observables on A alone.

### The CNOT gate as a non-separable operator
The controlled-NOT gate acts on two qubits: it flips the second (target) qubit if and only if the first (control) qubit is |1⟩.
$$\text{CNOT} = |0\rangle\langle 0| \otimes I + |1\rangle\langle 1| \otimes X = \begin{pmatrix}1&0&0&0\\0&1&0&0\\0&0&0&1\\0&0&1&0\end{pmatrix}$$
CNOT is not a product operator (it cannot be written as A ⊗ B for any A, B). This is the mathematical fact that makes it a two-qubit gate — it creates entanglement. Starting from |+⟩|0⟩ = (|0⟩+|1⟩)/√2 ⊗ |0⟩, CNOT produces (|00⟩+|11⟩)/√2 = |Φ+⟩.

---

## B. Where the quantum series uses it (specific QM chapters + how)

**IV·2 — Entanglement**
- Entanglement is defined as the failure of a multi-qubit state to be a product state — which requires the tensor product framework to define "product state" in the first place.
- Bell states are the primary objects of IV·2. Students need to recognize them as vectors in ℂ⁴, expand them in the {|00⟩, |01⟩, |10⟩, |11⟩} basis, and verify non-separability by the explicit argument above.
- The partial trace is the mathematical tool for quantifying entanglement via the reduced state. If ρ_A = I/2 (maximally mixed), the state is maximally entangled. M-16 should establish this connection.
- Schmidt decomposition (advanced): any state |ψ⟩ ∈ V ⊗ W can be written as |ψ⟩ = Σ_i σ_i |u_i⟩|v_i⟩ with σ_i ≥ 0 (Schmidt coefficients). The number of nonzero σ_i is the Schmidt rank; a product state has Schmidt rank 1. This is a consequence of the singular value decomposition of the coefficient matrix — an extension into linear algebra territory that belongs in this module or in a bridging note.

**IV·4 — Quantum gates**
- Single-qubit gates (X, Y, Z, H) are 2×2 unitary matrices acting on ℂ².
- Two-qubit gates are 4×4 unitary matrices acting on ℂ⁴ = ℂ² ⊗ ℂ².
- Local gates (acting on one qubit while leaving the other alone) are Kronecker products: U ⊗ I or I ⊗ U. The explicit matrix form of these — worked out in section A above — is exactly what students need to follow gate diagrams.
- Non-local gates (CNOT, CZ, SWAP) cannot be written as A ⊗ B. CNOT is the standard example. Understanding why CNOT is non-local requires understanding what a product operator is — this module.
- Gate composition: (A₁ ⊗ B₁)(A₂ ⊗ B₂) = (A₁A₂) ⊗ (B₁B₂). This identity (which follows from bilinearity) is used in every circuit calculation. Students need to see it derived, not just stated.

**IV·5 — Quantum teleportation**
- Teleportation uses a shared Bell state, two classical bits, and local operations. The protocol's correctness proof tracks a three-qubit state |ψ⟩ ⊗ |Φ+⟩ ∈ ℂ² ⊗ ℂ² ⊗ ℂ² through a sequence of operations, then traces over two qubits (Alice's pair after measurement). Students cannot follow this without fluency in: basis expansion in ℂ⁸, Kronecker product operator action, and partial trace / measurement collapse.
- The standard proof writes |ψ⟩|Φ+⟩ in the Bell basis for Alice's two qubits; the teleportation theorem is that this rewriting decomposes the three-qubit state so that Bob's qubit is always a known unitary transform of |ψ⟩, conditioned on Alice's two-bit measurement outcome. Every step uses Kronecker product algebra.

---

## C. Connections

- **Vector spaces (mfp2-04)**: M-16 is a direct extension. The tensor product is a new construction on vector spaces; mfp2-04's basis/dimension/linear independence machinery is prerequisite and used throughout.
- **Operators and inner products (mfp2-05)**: the partial trace uses the inner product to sum over a basis. Density matrices (mixed states) are operators on the tensor-product space; their manipulation requires the full operator machinery of mfp2-05.
- **Combinatorics (M-14)**: the 2^N dimension of the N-qubit space is the same combinatorial fact that Ω = 2^N for N two-state systems. The identical-particle symmetrization of mfp2-09 (symmetric/antisymmetric subspaces) lives inside the tensor product space.
- **Identical particles (QM II·10)**: the N-particle Hilbert space is the N-fold tensor product of single-particle spaces, then restricted to the symmetric (bosons) or antisymmetric (fermions) subspace. The tensor product is the starting point; symmetrization is the additional constraint.
- **Schmidt decomposition and SVD**: the Schmidt decomposition of a bipartite state uses the singular value decomposition of the coefficient matrix. This is a bridge from tensor products to numerical linear algebra.

---

## D. Conventions and pitfalls

- **Basis ordering**: fix it and state it. The standard is |00⟩, |01⟩, |10⟩, |11⟩ (first index = first qubit, varies slowest). Some texts reverse this. The Kronecker product formula A ⊗ B assumes a specific ordering; swapping the ordering changes the formula to B ⊗ A. Inconsistency leads to wrong gate matrices.
- **A ⊗ B ≠ B ⊗ A**: tensor product is not commutative in general. The two operators act on the same space (after reordering) but have different matrix representations. V ⊗ W and W ⊗ V are isomorphic but not the same space unless you also permute the basis.
- **Not every element of V ⊗ W is a simple tensor**: this is the central non-obvious fact. The student who thinks "v ⊗ w means every element has this form" misses entanglement entirely. Explicitly show that dim(V ⊗ W) > dim(V) + dim(W) and that most elements cannot be written as single products.
- **Partial trace vs. marginalization**: partial trace is the quantum analog of marginalizing a joint probability distribution. For a product state ρ_A ⊗ ρ_B, Tr_B[ρ_A ⊗ ρ_B] = ρ_A (as expected). For an entangled state the reduced state is mixed even if the global state is pure — this is strange and should be flagged explicitly.
- **Kronecker product is basis-dependent**: A ⊗ B gives the matrix of the operator A ⊗ B in the lexicographic product basis. If you choose a different basis for V ⊗ W (e.g., the Bell basis), the matrix looks different. The operator is the same; only its representation changes.
- **Notation collision**: |v⟩ ⊗ |w⟩ = |v⟩|w⟩ = |vw⟩ (for qubits) are all used. The last one saves space but hides the tensor structure. Use the explicit ⊗ symbol until students are comfortable; then introduce the shorthand.
- **Trace-out order**: Tr_B ≠ Tr_A in general (different bases for the trace). Always specify which system is being traced out.

---

## E. Teaching considerations

- **The key conceptual jump**: students who have seen vector spaces know that "combining two systems" might mean adding their state spaces. The tensor product is a different construction — the space of all *pairs* of states, plus their superpositions. This distinction needs to be stated directly and illustrated with dimensions: dim(V) + dim(W) = 4 (direct sum of two 2D spaces) vs. dim(V ⊗ W) = 4 (tensor product of two 2D spaces coincidentally the same dimension — use 3D + 2D → 5D vs. 6D to illustrate the difference).
- **Entanglement before formalism**: introduce entanglement intuitively (two qubits whose measurement outcomes are correlated beyond any product-state explanation) before giving the formal definition. Then show the product-state decomposition attempt that fails for Bell states — the failure is the definition.
- **Work through the CNOT construction carefully**: showing that CNOT creates |Φ+⟩ from |+⟩|0⟩ is the single most illuminating two-qubit calculation. It ties together: product state input, tensor-product operator action, entangled output.
- **Partial trace with density matrices**: if students have not seen density matrices before IV·2, a minimal introduction is needed here. The partial trace is the key new tool; motivate it as "what does an observer with access only to qubit A see?"
- **Scope**: this module covers the Kronecker/tensor product at the linear-algebra level. It does not cover Schmidt decomposition in full, entanglement measures (von Neumann entropy, concurrence), or LOCC operations — these belong in the QM chapter or an advanced module.
- **Assign before IV·2, IV·4, IV·5**: all three chapters use tensor-product algebra from their first equations. There is no graceful way to introduce entanglement, gates, or teleportation without this language in place.

---

## F. Source file used

AUTHORED — no single source chapter. This module is an extension of the linear algebra covered in `_lib_mfp2-04-vector-spaces-eigenvalues-and-diagonalization.md` (read for context on what students are assumed to know; tensor products are not covered there).

Primary references consulted:
1. Michael A. Nielsen and Isaac L. Chuang, *Quantum Computation and Quantum Information* (10th anniversary ed., Cambridge University Press, 2010). §2.1.7–2.1.8 (tensor products of vector spaces and operators), §2.2.8 (partial trace). The standard reference for tensor products in QC.
2. John Preskill, *Lecture Notes for Physics 229: Quantum Information and Computation* (Caltech, 1998–). Chapter 3 (foundations of quantum information, tensor products). Freely available at http://theory.caltech.edu/~preskill/ph229/. [verify URL current]
3. Asher Peres, *Quantum Theory: Concepts and Methods* (Kluwer, 1993; reprinted Springer, 2002). §5-1 to §5-3 on composite systems. Rigorous treatment of the tensor product in a physics context.
4. Wikipedia, "Tensor product" and "Kronecker product" — used to cross-check the Kronecker product formula and basis ordering convention. [not citable; used for verification only]
5. In-series context: `_lib_mfp2-04-vector-spaces-eigenvalues-and-diagonalization.md` (read in full for what prior linear algebra students have) and `_lib_mfp2-05-operators-inner-products-and-dirac-notation.md` (read header for Dirac notation conventions used in the series).

---

## G. Gaps and flags

- **AUTHORED module**: all content in sections A through E was authored fresh. The mathematical content is standard and well-established; the specific framing and connections to the QM series are author's own. Cross-check with IV·2, IV·4, IV·5 drafts when available.
- **Density matrix prerequisite**: the partial trace calculation requires density matrices. If IV·2 introduces density matrices for the first time, M-16 either needs a one-paragraph density-matrix primer or should defer partial trace to the QM chapter. Flag for series editor to decide.
- **Schmidt decomposition**: mentioned in B but not fully developed in A. The SVD-based derivation would require matrix decompositions beyond what mfp2-04 covers. Either include a self-contained Schmidt decomposition section in M-16, or leave it to IV·2 with a pointer here.
- **Symmetric and antisymmetric subspaces**: the connection to identical particles (bosons/fermions live in the symmetric/antisymmetric subspace of the tensor product) is noted in C but not developed. If II·10 uses tensor product language, a bridge note is needed.
- **Basis ordering convention**: verify which ordering the QM series uses in IV·4 and IV·5. If the series uses a non-standard ordering, the Kronecker product matrices in section A must be adjusted.
- **Entanglement measures**: von Neumann entropy S(ρ_A) = −Tr(ρ_A log ρ_A) quantifies entanglement for pure bipartite states. Not covered here; flag for IV·2.
- **Three-qubit tensor products**: the teleportation protocol uses three qubits (ℂ⁸). Section B sketches this but does not work through the three-qubit basis. If IV·5 requires explicit three-qubit matrix calculations, an additional worked example in M-16 would help.
