# Module M-16 — Tensor Products and Composite-System Linear Algebra

**Refresher for QM chapters:** IV·2, IV·4, IV·5

**Condensed from:** AUTHORED — extension of vector-space linear algebra (no single source chapter). Primary references: Nielsen & Chuang §2.1, Preskill Ph229 Ch. 3, Peres Ch. 5.

---

## When you need this

Read this module before **IV·2** (entanglement), **IV·4** (quantum gates), or **IV·5** (teleportation). All three chapters open with multi-qubit states — vectors in a composite Hilbert space — and the tensor product is the only way to build that space. Without it, you will be able to follow individual equations but not understand why the structure is the way it is.

Prerequisite: the vector space module (M-07 / mfp2-04) — basis, dimension, linear independence, inner product, and linear operators as matrices. The tensor product is a new construction *on* vector spaces; it does not replace the earlier machinery, it extends it.

---

## The refresher

### The central fact: dimension multiplies

When two classical systems are combined — two coins, two dice — you describe the joint state by listing the state of each one. The number of possible joint states is the *product* of the individual counts: two coins with two states each give $2 \times 2 = 4$ joint states. The state space of a quantum composite system works the same way, but at the level of complex vector spaces: the joint Hilbert space is the **tensor product** $V \otimes W$, and its dimension is $\dim(V) \times \dim(W)$.

This is not the direct sum $V \oplus W$ (dimension $m + n$, the "union" of degrees of freedom). It is a new, larger space whose dimension is $mn$. That multiplicative growth is the mathematical engine behind both quantum entanglement and the exponential state-space of quantum computing.

### The tensor product of vector spaces

Let $V$ (dimension $m$) and $W$ (dimension $n$) be complex vector spaces. Their tensor product $V \otimes W$ is defined by the following rules. For every pair $(|v\rangle, |w\rangle)$ with $|v\rangle \in V$ and $|w\rangle \in W$, there is an element $|v\rangle \otimes |w\rangle \in V \otimes W$, called a **simple tensor** or **product state**. The construction is bilinear:

$$\alpha(|v\rangle \otimes |w\rangle) = (\alpha|v\rangle) \otimes |w\rangle = |v\rangle \otimes (\alpha|w\rangle)$$

$$(|v_1\rangle + |v_2\rangle) \otimes |w\rangle = |v_1\rangle \otimes |w\rangle + |v_2\rangle \otimes |w\rangle$$

$$|v\rangle \otimes (|w_1\rangle + |w_2\rangle) = |v\rangle \otimes |w_1\rangle + |v\rangle \otimes |w_2\rangle$$

The space $V \otimes W$ is *spanned* by all simple tensors but also contains linear combinations of simple tensors that cannot themselves be written as a single product. Those non-product elements are the **entangled states**.

### Basis ordering and the standard product basis

If $V$ has basis $\{|0\rangle, |1\rangle\}$ (dimension 2) and $W$ also has basis $\{|0\rangle, |1\rangle\}$ (dimension 2), then $V \otimes W$ has dimension $2 \times 2 = 4$ and the standard ordered basis is:

$$\{|0\rangle \otimes |0\rangle,\; |0\rangle \otimes |1\rangle,\; |1\rangle \otimes |0\rangle,\; |1\rangle \otimes |1\rangle\}$$

written compactly as $\{|00\rangle, |01\rangle, |10\rangle, |11\rangle\}$. The ordering convention used here — and throughout Nielsen & Chuang — is **lexicographic**: the first (left) index varies slowest. This convention is what gives the Kronecker product its standard block form; deviating from it changes every gate matrix.

For $N$ qubits: $\dim = 2^N$. Thirty qubits require $\sim 10^9$ complex amplitudes ($\sim$16 GB) to represent classically. Fifty qubits require $\sim$16 petabytes. This exponential growth is simultaneously the source of quantum computing's potential power and of the difficulty in simulating it classically.

### The Kronecker product of operators

If $A$ is an $m \times m$ matrix acting on $V$ and $B$ is an $n \times n$ matrix acting on $W$, the operator $A \otimes B$ acts on $V \otimes W$ by $(A \otimes B)(|v\rangle \otimes |w\rangle) = (A|v\rangle) \otimes (B|w\rangle)$. In the lexicographic basis its matrix is the **Kronecker product**:

$$A \otimes B = \begin{pmatrix} A_{11}B & A_{12}B & \cdots \\ A_{21}B & A_{22}B & \cdots \\ \vdots & & \ddots \end{pmatrix}$$

where each entry $A_{ij}B$ is an $n \times n$ block. The resulting matrix is $mn \times mn$.

A key identity — used in every gate-circuit calculation — is:

$$(A_1 \otimes B_1)(A_2 \otimes B_2) = (A_1 A_2) \otimes (B_1 B_2).$$

This follows directly from bilinearity and says that applying a product operator twice just composes each factor independently: local operations on different subsystems compose locally.

### Worked example: two qubits and a Bell state

**Setup.** A single qubit lives in $V = \mathbb{C}^2$ with basis $\{|0\rangle, |1\rangle\}$. Two qubits live in $V \otimes V = \mathbb{C}^4$ with basis $\{|00\rangle, |01\rangle, |10\rangle, |11\rangle\}$.

**Step 1: a product state.** The state $|{+}\rangle \otimes |0\rangle$, where $|{+}\rangle = (|0\rangle + |1\rangle)/\sqrt{2}$:

$$|{+}\rangle \otimes |0\rangle = \frac{1}{\sqrt{2}}(|0\rangle + |1\rangle) \otimes |0\rangle = \frac{1}{\sqrt{2}}(|00\rangle + |10\rangle).$$

This is a product state: measuring the first qubit and measuring the second are independent operations.

**Step 2: apply CNOT.** The controlled-NOT gate flips the second (target) qubit if and only if the first (control) qubit is $|1\rangle$:

$$\text{CNOT} = |0\rangle\langle 0| \otimes I + |1\rangle\langle 1| \otimes X = \begin{pmatrix}1&0&0&0\\0&1&0&0\\0&0&0&1\\0&0&1&0\end{pmatrix}.$$

Apply it to $|{+}\rangle|0\rangle$:

$$\text{CNOT}\,\frac{1}{\sqrt{2}}(|00\rangle + |10\rangle) = \frac{1}{\sqrt{2}}(|00\rangle + |11\rangle) = |\Phi^+\rangle.$$

$|00\rangle$ is unchanged (control is $|0\rangle$); $|10\rangle$ becomes $|11\rangle$ (control is $|1\rangle$, target flips).

**Step 3: verify that $|\Phi^+\rangle$ is entangled.** Suppose for contradiction that

$$|\Phi^+\rangle = \frac{1}{\sqrt{2}}(|00\rangle + |11\rangle) = (\alpha|0\rangle + \beta|1\rangle) \otimes (\gamma|0\rangle + \delta|1\rangle).$$

Expanding the right side: $\alpha\gamma|00\rangle + \alpha\delta|01\rangle + \beta\gamma|10\rangle + \beta\delta|11\rangle$. Matching coefficients:

$$\alpha\gamma = \tfrac{1}{\sqrt{2}}, \quad \alpha\delta = 0, \quad \beta\gamma = 0, \quad \beta\delta = \tfrac{1}{\sqrt{2}}.$$

From $\alpha\delta = 0$: either $\alpha = 0$ or $\delta = 0$. If $\alpha = 0$, then $\alpha\gamma = 0 \neq 1/\sqrt{2}$. If $\delta = 0$, then $\beta\delta = 0 \neq 1/\sqrt{2}$. Contradiction in every case. Therefore $|\Phi^+\rangle$ cannot be written as a product state: it is entangled.

**Why CNOT is not a product operator.** Suppose $\text{CNOT} = A \otimes B$ for some $2 \times 2$ matrices $A, B$. Then $(A \otimes B)|{+}\rangle|0\rangle = (A|{+}\rangle) \otimes (B|0\rangle)$ — a product state. But CNOT maps $|{+}\rangle|0\rangle$ to $|\Phi^+\rangle$, which is entangled. Contradiction: a product operator cannot create entanglement. CNOT is genuinely a two-qubit gate.

### Separable versus entangled states

A state $|\psi\rangle \in V \otimes W$ is **separable** (a product state) if it factors as $|\psi\rangle = |v\rangle \otimes |w\rangle$ for some $|v\rangle \in V$, $|w\rangle \in W$. A state that cannot be written this way is **entangled**.

The four **Bell states** are the maximally entangled two-qubit states:

$$|\Phi^\pm\rangle = \frac{1}{\sqrt{2}}(|00\rangle \pm |11\rangle), \qquad |\Psi^\pm\rangle = \frac{1}{\sqrt{2}}(|01\rangle \pm |10\rangle).$$

They form an orthonormal basis for $\mathbb{C}^4$ — the Bell basis — and are used throughout quantum information (superdense coding, teleportation, entanglement witnesses). By the argument above, none of them is a product state.

**Separability test (two qubits).** Write the coefficient matrix $M$ of $|\psi\rangle = \sum_{ij} c_{ij}|ij\rangle$ as a $2 \times 2$ matrix with entries $c_{ij}$. The state is separable if and only if $\text{rank}(M) = 1$, i.e., the matrix has only one nonzero singular value (Schmidt rank 1). For $|\Phi^+\rangle$, $M = \frac{1}{\sqrt{2}}\begin{pmatrix}1 & 0 \\ 0 & 1\end{pmatrix}$ has rank 2: maximally entangled.

### The partial trace: discarding a subsystem

The **partial trace** over subsystem $B$ gives the reduced state of subsystem $A$ alone:

$$\rho_A = \text{Tr}_B[\rho_{AB}] = \sum_j (\mathbf{I} \otimes \langle j|)\,\rho_{AB}\,(\mathbf{I} \otimes |j\rangle),$$

where $\{|j\rangle\}$ is any orthonormal basis for $W$. This is the quantum analog of marginalizing a joint probability distribution: it gives the state an observer with access only to $A$ should assign.

**Key example.** For $|\Phi^+\rangle$, the joint density matrix is $\rho_{AB} = |\Phi^+\rangle\langle\Phi^+|$. Tracing over $B$:

$$\rho_A = \frac{1}{2}|0\rangle\langle 0| + \frac{1}{2}|1\rangle\langle 1| = \frac{I}{2}.$$

The reduced state of $A$ is the maximally mixed state — an observer with access to qubit $A$ alone sees nothing but a perfectly random coin, despite the global state $|\Phi^+\rangle$ being a pure state. The information is encoded in the *correlations*, not in the individual qubits. This is the linear-algebra signature of maximal entanglement: the reduced state is maximally mixed.

**Contrast with a product state.** For $\rho_{AB} = \rho_A \otimes \rho_B$, the partial trace gives $\text{Tr}_B[\rho_A \otimes \rho_B] = \rho_A \cdot \text{Tr}[\rho_B] = \rho_A$ (since $\text{Tr}[\rho_B] = 1$). No information is lost: the subsystem state is exactly what you put in.

---

## In the quantum series

### IV·2 — Entanglement

IV·2 defines entanglement precisely as the failure of a multi-qubit state to be a product state — which requires the tensor product framework just to define "product state." The Bell states are the primary objects of that chapter. Students need to expand them in the $\{|00\rangle, |01\rangle, |10\rangle, |11\rangle\}$ basis, verify non-separability by the coefficient-matching argument above, and compute the partial trace to confirm maximal entanglement.

The partial trace is the mathematical tool for quantifying entanglement: the von Neumann entropy $S(\rho_A) = -\text{Tr}(\rho_A \log \rho_A)$ of the reduced state measures how entangled the global pure state is. For $|\Phi^+\rangle$, $\rho_A = I/2$ gives $S = \log 2 = 1$ ebit — the maximum for a two-qubit system. IV·2 develops this; M-16 supplies the algebraic machinery to get there.

### IV·4 — Quantum gates

Single-qubit gates ($X$, $Y$, $Z$, $H$) are $2 \times 2$ unitary matrices acting on $\mathbb{C}^2$. Two-qubit gates are $4 \times 4$ unitary matrices acting on $\mathbb{C}^4 = \mathbb{C}^2 \otimes \mathbb{C}^2$.

Local gates (acting on one qubit while leaving the other alone) are Kronecker products. The Hadamard $H = \frac{1}{\sqrt{2}}\begin{pmatrix}1&1\\1&-1\end{pmatrix}$ applied to the first qubit only:

$$H \otimes I = \frac{1}{\sqrt{2}}\begin{pmatrix}I & I \\ I & -I\end{pmatrix} = \frac{1}{\sqrt{2}}\begin{pmatrix}1&0&1&0\\0&1&0&1\\1&0&-1&0\\0&1&0&-1\end{pmatrix}.$$

Non-local gates (CNOT, CZ, SWAP) cannot be written as $A \otimes B$. The worked example above shows why CNOT is non-local. Understanding this distinction is what separates "can write down a gate matrix" from "understands why a gate is or is not two-qubit."

### IV·5 — Quantum teleportation

The teleportation protocol tracks a three-qubit state $|\psi\rangle \otimes |\Phi^+\rangle \in \mathbb{C}^2 \otimes \mathbb{C}^2 \otimes \mathbb{C}^2$ (dimension 8) through a sequence of operations, then traces over Alice's two qubits after her measurement. Every step is Kronecker product algebra: expanding in the eight-dimensional basis, rewriting in the Bell basis for Alice's pair, reading off Bob's conditional state. The protocol's correctness — that Bob always ends up with a known unitary transform of the original $|\psi\rangle$ — is a theorem about the structure of $\mathbb{C}^2 \otimes \mathbb{C}^2 \otimes \mathbb{C}^2$ that cannot even be stated without the tensor product language.

---

## Conventions and pitfalls

**Basis ordering must be fixed and stated.** The Kronecker product formula $A \otimes B$ (with the block structure above) assumes lexicographic ordering: $|00\rangle, |01\rangle, |10\rangle, |11\rangle$. Some texts reverse this. If you swap the ordering, the formula becomes $B \otimes A$, and every gate matrix changes. Before any numerical calculation, state your ordering convention explicitly.

**$A \otimes B \neq B \otimes A$ in general.** Tensor product is not commutative. $V \otimes W$ and $W \otimes V$ are isomorphic but not identical; swapping subsystems requires the swap operator $\text{SWAP}|ij\rangle = |ji\rangle$.

**Not every element of $V \otimes W$ is a simple tensor.** The space is spanned by simple tensors $|v\rangle \otimes |w\rangle$ but it contains vectors — the entangled states — that are not simple tensors. A student who thinks "everything in $V \otimes W$ looks like $|v\rangle \otimes |w\rangle$" will miss entanglement entirely. The dimension count confirms this: $\dim(V \otimes W) = mn$, but the set of simple tensors is parameterized by $m + n$ complex numbers (up to normalization), not $mn$. The "extra" elements are the entangled ones.

**The partial trace is basis-independent but trace order is not.** $\text{Tr}_B \neq \text{Tr}_A$ in general: they trace over different subsystems and give different reduced states. Always specify which subsystem you are tracing out.

**Notation collisions.** $|v\rangle \otimes |w\rangle = |v\rangle|w\rangle = |vw\rangle$ (for short labels) are all used. The last form is compact but hides the tensor structure. Use explicit $\otimes$ until you are comfortable, then adopt shorthand.

**Density matrices are required for partial trace.** The partial trace formula is stated for density matrices $\rho_{AB}$. For a pure state $|\psi\rangle$, form $\rho = |\psi\rangle\langle\psi|$ first, then trace. Do not attempt to "partially trace a ket."

---

## Quick practice

1. **Kronecker product.** Let $X = \begin{pmatrix}0&1\\1&0\end{pmatrix}$ (Pauli-$X$) and $Z = \begin{pmatrix}1&0\\0&-1\end{pmatrix}$ (Pauli-$Z$). Write out the $4 \times 4$ matrix for $X \otimes Z$ in the standard $\{|00\rangle, |01\rangle, |10\rangle, |11\rangle\}$ ordering. Then verify by direct matrix multiplication that $(X \otimes Z)|01\rangle = -|10\rangle$.

2. **Separability check.** Consider the two-qubit state $|\psi\rangle = \frac{1}{\sqrt{3}}(|00\rangle + |01\rangle + |10\rangle)$. Write the coefficient matrix $M$ with entries $c_{ij}$ (rows indexed by the first qubit, columns by the second). Compute $\text{rank}(M)$. Is $|\psi\rangle$ separable? If not, find its Schmidt decomposition (hint: use the singular value decomposition of $M$).

3. **Partial trace.** Let $|\Psi^-\rangle = (|01\rangle - |10\rangle)/\sqrt{2}$. Form $\rho_{AB} = |\Psi^-\rangle\langle\Psi^-|$ and compute $\rho_A = \text{Tr}_B[\rho_{AB}]$. What is $\rho_A$? What does this tell you about the entanglement of $|\Psi^-\rangle$?

---

## Go deeper

The standard reference for tensor products in quantum information is Nielsen & Chuang, *Quantum Computation and Quantum Information* (Cambridge, 10th anniversary ed., 2010), §§2.1.7–2.1.8 (tensor products of vector spaces and operators) and §2.2.8 (partial trace) `[verify — section numbers stable in 10th anniversary ed.]`. Preskill's lecture notes for Ph229 — freely available at http://theory.caltech.edu/~preskill/ph229/ `[verify — URL current as of 2025]` — cover tensor products in Chapter 3 with excellent physical motivation. For a more mathematically demanding treatment that stays close to physics intuition, see Peres, *Quantum Theory: Concepts and Methods* (Springer, 2002), §§5-1 to 5-3.

---

## References

1. Michael A. Nielsen and Isaac L. Chuang, *Quantum Computation and Quantum Information*, 10th anniversary ed. Cambridge University Press, 2010. §2.1.7–2.1.8, §2.2.8. `[verify]`
2. John Preskill, *Lecture Notes for Physics 229: Quantum Information and Computation*, Caltech, 1998–. Ch. 3. Available at http://theory.caltech.edu/~preskill/ph229/. `[verify — URL current]`
3. Asher Peres, *Quantum Theory: Concepts and Methods*. Kluwer, 1993; reprinted Springer, 2002. §§5-1 to 5-3. `[verify]`
