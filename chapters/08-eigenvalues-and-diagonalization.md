# Module M-08 — Eigenvalues and Diagonalization

**When you need this:** QM chapters II·2 (observables and the spectral decomposition), III·2 (degenerate perturbation theory / fine structure), IV·6 (density matrices and open systems)

**Condensed from:** *Mathematics for Physics* Vol 2, Ch 4

---

## The refresher

### The eigenvalue problem: invariant directions of a linear map

For a linear operator $A$ (a matrix or an operator on a function space), an **eigenvector** is a nonzero vector that $A$ merely stretches — it does not change direction:

$$A\mathbf{v} = \lambda\mathbf{v}, \qquad \mathbf{v} \neq \mathbf{0}.$$

The scalar $\lambda$ is the corresponding **eigenvalue**. Most vectors get rotated when $A$ acts; eigenvectors are the invariant directions. The name is from the German *eigen* ("own" or "characteristic"), popularized by David Hilbert around 1904 in his integral-equation work. `[verify: Hilbert 1904 Göttingen Nachrichten]`

### Where the characteristic equation comes from

Rearrange the eigenvalue equation:

$$A\mathbf{v} = \lambda\mathbf{v} \;\Longrightarrow\; (A - \lambda I)\mathbf{v} = \mathbf{0}.$$

This is a homogeneous linear system. It always has the trivial solution $\mathbf{v} = \mathbf{0}$, which we forbid. A nonzero solution exists if and only if $A - \lambda I$ is singular — that is, if and only if it has a nontrivial nullspace. And a matrix is singular precisely when its determinant vanishes:

$$\boxed{\det(A - \lambda I) = 0.}$$

This is the **characteristic equation**. Setting the determinant to zero is not a recipe to memorize but the literal condition for a nonzero eigenvector to exist: a nonzero vector in the nullspace of $A - \lambda I$ requires that matrix to be non-invertible, which requires its determinant to be zero. Students who treat this as a rule-to-memorize cannot answer "why?" and cannot recognize the same structure when it appears in a different physical context.

Expanding the determinant gives the **characteristic polynomial** $p(\lambda) = \det(A - \lambda I)$, of degree $n$ for an $n \times n$ matrix. Its roots are the eigenvalues. Over $\mathbb{C}$ there are always $n$ roots counted with multiplicity (Fundamental Theorem of Algebra). For each eigenvalue $\lambda_j$, solving $(A - \lambda_j I)\mathbf{v} = \mathbf{0}$ gives the eigenvector(s).

### Diagonalization

Suppose $A$ (an $n \times n$ matrix) has $n$ linearly independent eigenvectors $\mathbf{v}_1, \dots, \mathbf{v}_n$ with eigenvalues $\lambda_1, \dots, \lambda_n$. Stack the eigenvectors as columns of a matrix $P = [\mathbf{v}_1 \;\cdots\; \mathbf{v}_n]$. Then $AP = PD$ where $D = \operatorname{diag}(\lambda_1, \dots, \lambda_n)$. Since the eigenvectors are independent, $P$ is invertible, and:

$$\boxed{A = PDP^{-1}, \qquad D = P^{-1}AP.}$$

The matrix $D$ is $A$ *expressed in the eigenbasis* — it is diagonal, with all couplings gone. Diagonalization is a change of coordinates that makes the action of $A$ maximally transparent: in the eigenbasis, $A$ multiplies each coordinate independently by its eigenvalue.

Not every matrix is diagonalizable. A **defective** matrix has fewer than $n$ independent eigenvectors; the simplest example is $\bigl[\begin{smallmatrix}1&1\\0&1\end{smallmatrix}\bigr]$, which has only one eigenvector for its repeated eigenvalue $\lambda = 1$. Such matrices reduce only to Jordan form. In quantum mechanics, however, the operators that arise as observables are never defective — the spectral theorem below guarantees it.

### The spectral theorem for Hermitian matrices

A complex matrix is **Hermitian** if $A^\dagger = A$ (conjugate transpose equals itself). This is the complex generalization of "symmetric": for real matrices, $A^T = A$ is the right condition; over $\mathbb{C}$, it must be $A^\dagger = A$.

**Theorem (spectral theorem, finite-dimensional form).** Every Hermitian matrix $A$ has:
- All eigenvalues real.
- Eigenvectors belonging to distinct eigenvalues are orthogonal (with respect to the standard complex inner product $\langle\mathbf{u}|\mathbf{v}\rangle = \mathbf{u}^\dagger\mathbf{v}$).
- A complete orthonormal set of eigenvectors exists; i.e., $A$ is diagonalizable by a unitary matrix $U$ ($U^\dagger = U^{-1}$): $A = UDU^\dagger$ with $D$ real diagonal.

*Proof of real eigenvalues.* Let $A\mathbf{v} = \lambda\mathbf{v}$, $\mathbf{v} \neq \mathbf{0}$. Multiply both sides on the left by $\mathbf{v}^\dagger$:

$$\mathbf{v}^\dagger A\mathbf{v} = \lambda\,\mathbf{v}^\dagger\mathbf{v} = \lambda\|\mathbf{v}\|^2.$$

Now take the complex conjugate of the scalar $\mathbf{v}^\dagger A\mathbf{v}$. Since it is a $1\times1$ matrix (a number), conjugating equals taking the dagger: $(\mathbf{v}^\dagger A\mathbf{v})^* = \mathbf{v}^\dagger A^\dagger \mathbf{v}$. But $A^\dagger = A$, so the conjugate equals the original. The number $\mathbf{v}^\dagger A\mathbf{v}$ is its own conjugate, hence real. Since $\|\mathbf{v}\|^2 > 0$ is real and positive, $\lambda = (\mathbf{v}^\dagger A\mathbf{v})/\|\mathbf{v}\|^2$ is real. $\square$

*Proof of orthogonal eigenvectors.* Take distinct eigenvalues $\lambda_1 \neq \lambda_2$ (both now known real), with $A\mathbf{v}_1 = \lambda_1\mathbf{v}_1$ and $A\mathbf{v}_2 = \lambda_2\mathbf{v}_2$. Compute $\mathbf{v}_2^\dagger A\mathbf{v}_1$ two ways:

- Acting right: $\mathbf{v}_2^\dagger A\mathbf{v}_1 = \lambda_1\,\mathbf{v}_2^\dagger\mathbf{v}_1$.
- Acting left (using $A^\dagger = A$ to move $A$ onto the bra): $(A\mathbf{v}_2)^\dagger\mathbf{v}_1 = \lambda_2\,\mathbf{v}_2^\dagger\mathbf{v}_1$.

Subtracting: $(\lambda_1 - \lambda_2)\,\mathbf{v}_2^\dagger\mathbf{v}_1 = 0$. Since $\lambda_1 \neq \lambda_2$, we must have $\mathbf{v}_2^\dagger\mathbf{v}_1 = 0$. $\square$

When an eigenvalue is repeated (degenerate), Gram–Schmidt orthonormalizes its eigenspace internally. The final result is an orthonormal eigenbasis and real eigenvalues in all cases.

### The spectral decomposition

Once $A$ is diagonalized in an orthonormal eigenbasis $\{|\lambda_n\rangle\}$ with eigenvalues $\{\lambda_n\}$, the resolution of the identity (Module M-07) gives the operator a transparent form:

$$A = UDU^\dagger = \sum_n \lambda_n\,|\lambda_n\rangle\langle\lambda_n|.$$

This is the **spectral decomposition**: the operator is literally the sum of each eigenvalue times the projector onto the corresponding eigenstate. It carries every fact about $A$ without coordinates.

### Functions of operators via spectral decomposition

If you can diagonalize $A = UDU^\dagger$, you can define any function of $A$ by applying that function to each eigenvalue:

$$f(A) = Uf(D)U^\dagger = \sum_n f(\lambda_n)\,|\lambda_n\rangle\langle\lambda_n|,$$

where $f(D) = \operatorname{diag}(f(\lambda_1), f(\lambda_2), \dots)$. The source chapter does not treat this, but it is essential for time evolution. The time-evolution operator is:

$$\hat U(t) = e^{-i\hat H t/\hbar} = \sum_n e^{-iE_n t/\hbar}\,|E_n\rangle\langle E_n|.$$

Computing $e^{\hat H}$ for a general matrix by brute-force power series is arduous; in the eigenbasis it is trivial — exponentiate each eigenvalue separately. The same works for $\sin(\hat A)$, $\ln(\hat A)$, or any analytic function: spectral decomposition reduces $f(A)$ to applying $f$ to a list of numbers.

### Simultaneous diagonalization

Two Hermitian operators $\hat A$ and $\hat B$ share a common orthonormal eigenbasis if and only if they commute:

$$[\hat A, \hat B] \equiv \hat A\hat B - \hat B\hat A = 0 \;\;\Longleftrightarrow\;\; \hat A \text{ and } \hat B \text{ are simultaneously diagonalizable.}$$

When they commute, each eigenvector of $\hat A$ is also an eigenvector of $\hat B$, and states can be labeled simultaneously by both eigenvalues. This is the mathematical backbone of **quantum numbers**.

---

### Worked example: $2 \times 2$ Hermitian diagonalization ($\sigma_y$)

Let $\sigma_y = \bigl[\begin{smallmatrix}0 & -i \\ i & 0\end{smallmatrix}\bigr]$. Check: $\sigma_y^\dagger = (\sigma_y^T)^* = \bigl[\begin{smallmatrix}0 & -i\\i&0\end{smallmatrix}\bigr]^* = \bigl[\begin{smallmatrix}0&i\\-i&0\end{smallmatrix}\bigr]^T$... directly: $(\sigma_y^\dagger)_{ij} = \sigma_y^*{}_{ji}$, so $(\sigma_y^\dagger)_{11} = 0$, $(\sigma_y^\dagger)_{12} = (i)^* = -i$... more directly: $(0,\,-i;\,i,\,0)$ — conjugate transpose swaps row/column and conjugates, giving $(0,\,i;\,-i,\,0)$... this equals $\sigma_y$? Check: $\sigma_y = (0,-i;i,0)$ and $\sigma_y^\dagger = (0^*, i^*; (-i)^*, 0^*) = (0,-i;i,0) = \sigma_y$. Yes, Hermitian.

**Characteristic equation:**

$$\det(\sigma_y - \lambda I) = \det\begin{pmatrix}-\lambda & -i \\ i & -\lambda\end{pmatrix} = \lambda^2 - (-i)(i) = \lambda^2 - 1 = 0 \;\Longrightarrow\; \lambda = \pm 1.$$

Real eigenvalues despite imaginary entries — the spectral theorem at work.

**Eigenvectors.** For $\lambda = +1$: solve $(\sigma_y - I)\mathbf{v} = 0$, i.e. $(-1,-i;i,-1)\mathbf{v} = 0$. From the first row: $-v_1 - iv_2 = 0$, so $v_1 = -iv_2$. Taking $v_2 = 1$: $\mathbf{v}_+ = (-i, 1)^T$. Normalize: $|{-i}|^2 + 1^2 = 2$, so $|\lambda{=}+1\rangle = \frac{1}{\sqrt{2}}\binom{-i}{1}$.

For $\lambda = -1$: $v_1 = iv_2$, so $|\lambda{=}-1\rangle = \frac{1}{\sqrt{2}}\binom{i}{1}$.

**Orthogonality check:** $\langle\lambda{=}{-1}|\lambda{=}{+1}\rangle = \frac{1}{2}[(i)^*(-i) + 1^*(1)] = \frac{1}{2}[-i(-i) + 1] = \frac{1}{2}[-1 + 1] = 0$. These are the spin-$\tfrac{1}{2}$ eigenstates along $\pm y$.

**Spectral decomposition:** $\sigma_y = (+1)|\lambda{=}+1\rangle\langle\lambda{=}+1| + (-1)|\lambda{=}-1\rangle\langle\lambda{=}-1|$. One can verify this reconstructs $(0,-i;i,0)$ directly.

---

## In the quantum series

### Observables are Hermitian — and the spectral theorem is why (QM II·2)

Every observable $\hat A$ in quantum mechanics is a Hermitian operator on the Hilbert space. The spectral theorem guarantees:

- **Eigenvalues are real:** every possible measurement outcome is a real number. This is not an empirical assumption; it follows from Hermiticity.
- **Eigenstates are orthogonal:** distinct measurement outcomes correspond to mutually distinguishable (orthogonal) states.
- **Eigenstates are complete:** any state can be expanded in the eigenbasis, which is the prerequisite for the Born rule to assign probabilities to all possible outcomes.

Students who arrive at II·2 without the spectral theorem are forced to accept "measurement outcomes are real" as an axiom. With the theorem, it is a two-line derivation.

### Degenerate perturbation theory (QM III·2)

Fine structure in hydrogen lifts the degeneracy of states sharing the same principal quantum number $n$ but differing in $\ell$ or $j$. The method: treat the perturbation $H' = H_\text{SO} + H_\text{rel}$ as an operator restricted to the degenerate subspace; diagonalize the matrix $M_{ij} = \langle n,i\,|H'|\,n,j\rangle$ within that subspace. The first-order energy corrections are the eigenvalues of $M$; the "good" states — the ones that diagonalize $H'$ — are the eigenvectors.

This is literally the $2 \times 2$ or $4 \times 4$ Hermitian diagonalization of this module, applied to a subspace. Students who have not done this by hand at least once will not be able to set up the secular determinant $\det(M - E^{(1)}I) = 0$ in context. The module worked example ($\sigma_y$) is the right warm-up.

### Continuous spectrum: generalized eigenfunctions (beyond the source)

The finite-dimensional spectral theorem assumes $n$ eigenvalues and $n$ eigenvectors. Quantum mechanics routinely involves operators whose spectrum is not discrete. The **position operator** $\hat x|\xi\rangle = \xi|\xi\rangle$ and the **momentum operator** $\hat p|p\rangle = p|p\rangle$ have purely continuous spectra: every real number $\xi$ or $p$ is an "eigenvalue," and the corresponding "eigenstates" $|x\rangle = \delta(x - \xi)$ and $|p\rangle = e^{ipx/\hbar}/\sqrt{2\pi\hbar}$ are not square-integrable — they lie outside $L^2(\mathbb{R})$.

The correct framework is the **rigged Hilbert space** (or Gelfand triple): $\Phi \subset \mathcal{H} \subset \Phi^*$, where $\Phi$ is a space of "nice" (rapidly decaying, smooth) functions, $\mathcal{H} = L^2$, and $\Phi^*$ is the space of continuous linear functionals on $\Phi$ (which includes the Dirac delta). Generalized eigenvectors live in $\Phi^*$, not in $\mathcal{H}$. The spectral theorem extends to this setting (the **nuclear spectral theorem**, due to Gel'fand and collaborators in the 1950s), with the resolution of the identity becoming:

$$\hat I = \int_{-\infty}^{\infty} |x\rangle\langle x|\,dx, \qquad \langle x|x'\rangle = \delta(x - x').$$

In practice: whenever you see the continuous resolution $\int|x\rangle\langle x|\,dx = \hat I$ or orthonormality $\langle p|p'\rangle = \delta(p - p')$, you are using the generalized spectral theorem. The Dirac delta replaces the Kronecker delta; "probability" becomes "probability density"; and none of the eigenstates are normalizable. For everyday calculations this is handled by working with normalizable wave packets and taking limits; for full rigor, see Reed and Simon.

### Functions of operators and time evolution (QM II·2, II·3)

The time-evolution operator $\hat U(t) = e^{-i\hat H t/\hbar}$ is defined by the spectral decomposition:

$$\hat U(t) = \sum_n e^{-iE_n t/\hbar}|E_n\rangle\langle E_n|.$$

Each energy eigenstate picks up a phase $e^{-iE_nt/\hbar}$; the time evolution of a general state is just the superposition of these phases. Computing $\hat U(t)$ by this route requires knowing the eigenbasis of $\hat H$ — which is why energy eigenvalue problems are so central. For a spin-$\tfrac12$ particle in a magnetic field, $\hat H \propto \sigma_z$, the diagonalization is trivial; for hydrogen, it is Chapters 6–7 of the QM series.

### Density matrices and open systems (QM IV·6)

The **density matrix** $\hat\rho$ of a quantum state is Hermitian, positive-semidefinite (all eigenvalues $\geq 0$), and $\operatorname{tr}\hat\rho = 1$. Diagonalizing it:

$$\hat\rho = \sum_n p_n|\psi_n\rangle\langle\psi_n|, \qquad p_n \geq 0, \quad \sum_n p_n = 1.$$

The eigenvalues $p_n$ are the classical probabilities of the pure states $|\psi_n\rangle$ in the ensemble. This diagonalization identifies the **preferred basis** — the states the environment effectively selects. For an open system (M-09 and QM IV·6), the dynamics of $\hat\rho$ under the Lindblad equation can be analyzed by finding the eigenoperators of the Lindblad superoperator (a map on density matrices, not on state vectors) — which is an eigenvalue problem in the larger space of operators.

---

## Conventions and pitfalls

**1. Symmetric vs. Hermitian over $\mathbb{C}$.** For real matrices, symmetry ($A^T = A$) guarantees real eigenvalues and orthogonal eigenvectors. For complex matrices, the correct condition is Hermitian ($A^\dagger = A$). A complex symmetric matrix ($A^T = A$ but $A \neq A^\dagger$) need not have real eigenvalues. The Pauli matrix $\sigma_y$ is Hermitian but not symmetric; its eigenvalues $\pm 1$ are real. Build and solve a $2\times2$ example of a complex symmetric matrix with complex eigenvalues to kill this confusion.

**2. Why set det $= 0$? (And not something else.)** Students who cannot answer this question have memorized a recipe, not understood the problem. The answer is one sentence: a nonzero eigenvector is a nonzero element of the nullspace of $A - \lambda I$, and a matrix has a nontrivial nullspace if and only if its determinant vanishes.

**3. Algebraic vs. geometric multiplicity.** The **algebraic multiplicity** of an eigenvalue is its multiplicity as a root of the characteristic polynomial; the **geometric multiplicity** is the dimension of the corresponding eigenspace (the nullspace of $A - \lambda I$). For Hermitian matrices, algebraic and geometric multiplicities always agree — the eigenspace is "full" — which is why Hermitian matrices are never defective.

**4. Orthogonality requires the conjugate inner product.** To verify that two complex eigenvectors are orthogonal, compute $\mathbf{v}_2^\dagger\mathbf{v}_1$ (with the conjugate on the first factor), not $\mathbf{v}_2^T\mathbf{v}_1$. For real eigenvectors these coincide; for complex eigenvectors they do not. The $\sigma_y$ example above exposes this immediately.

**5. Defective matrices exist, but not in QM.** Knowing defective matrices exist prevents a false belief that every matrix diagonalizes. But every Hermitian matrix does, so in practice this caveat is "flag it and move on."

---

## Quick practice

**1.** Find the eigenvalues and orthonormal eigenvectors of $A = \bigl[\begin{smallmatrix}1 & 2 \\ 2 & 1\end{smallmatrix}\bigr]$. Write the spectral decomposition $A = \sum_n\lambda_n|\lambda_n\rangle\langle\lambda_n|$ and verify by multiplying out.

**2.** Given the spectral decomposition from Exercise 1, compute $e^A$ and $e^{iA}$ using the formula $f(A) = \sum f(\lambda_n)|\lambda_n\rangle\langle\lambda_n|$. Check that $e^{iA}$ is unitary.

**3.** Two Hermitian operators on $\mathbb{C}^2$ are $\hat A = \sigma_z = \bigl[\begin{smallmatrix}1&0\\0&-1\end{smallmatrix}\bigr]$ and $\hat B = \sigma_x = \bigl[\begin{smallmatrix}0&1\\1&0\end{smallmatrix}\bigr]$. Compute $[\hat A, \hat B]$. Do they share an eigenbasis? If not, find the eigenbases of each and exhibit a state that is an eigenstate of $\hat A$ but not of $\hat B$.

---

## Go deeper

Full derivations (characteristic equation, diagonalization theorem, spectral theorem proof for real symmetric and Hermitian matrices, normal-modes worked example): **Vol. 2, Ch. 4** of *Mathematics for Physics*.

**Hard cases:** For the continuous-spectrum generalization (rigged Hilbert spaces, nuclear spectral theorem): Reed, M., and B. Simon. *Methods of Modern Mathematical Physics, Vol. I: Functional Analysis.* Academic Press, 1972. For an accessible treatment of the physicist's rigged Hilbert space: Ballentine, L. E. *Quantum Mechanics: A Modern Development.* World Scientific, 1998, Ch. 1.

For the Lindblad equation and superoperators: Breuer, H.-P., and F. Petruccione. *The Theory of Open Quantum Systems.* Oxford University Press, 2002. `[verify]`

---

## References

- Cayley, A. "A Memoir on the Theory of Matrices." *Philosophical Transactions of the Royal Society of London* **148**, 17–37 (1858). (The founding paper of matrix algebra; eigenvalues implicit in the secular equation.) `[verify]`
- Cauchy, A.-L. *Exercices de mathématiques*, Vol. 4, pp. 174–195. 1829. (Real eigenvalues and orthogonal principal axes of symmetric quadratic forms — the spectral theorem's ancestor, via the secular equation of celestial mechanics. Pagination confirmed in Hawkins, T. "Cauchy and the spectral theory of matrices." *Historia Mathematica* **2**, 1–29, 1975.) `[verify Hawkins citation]`
- Hilbert, D. "Grundzüge einer allgemeinen Theorie der linearen Integralgleichungen." *Nachrichten von der Gesellschaft der Wissenschaften zu Göttingen*, 1904. (Where *Eigenwert* and *Eigenfunktion* terminology was introduced and popularized.) `[verify]`
- Jones, R. C. "A New Calculus for the Treatment of Optical Systems." *Journal of the Optical Society of America* **31**, 488–493 (1941). (Jones-calculus polarization eigenstates as the optical avatar of the eigenvalue problem.) `[verify]`
- Shankar, R. *Principles of Quantum Mechanics.* 2nd ed. Plenum, 1994. Ch. 1 (Mathematical Introduction) for spectral theorem in a QM context. `[verify edition]`
- Cohen-Tannoudji, C., B. Diu, and F. Laloë. *Quantum Mechanics.* 2 vols. Wiley, 1977. Vol. 1, Complement $\text{B}_\text{III}$, for Hermitian operators and spectral decomposition. `[verify complement label]`
- Reed, M., and B. Simon. *Methods of Modern Mathematical Physics, Vol. II: Fourier Analysis, Self-Adjointness.* Academic Press, 1975. (Continuous spectrum, self-adjoint extensions, and the nuclear spectral theorem.) `[verify]`
- Serbin, K., and M. Wawro. "Student interpretations of eigenequations in linear algebra and quantum mechanics." *International Journal of Research in Undergraduate Mathematics Education* (2024). (Documents cross-context blindness: students treat $A\mathbf{v}=\lambda\mathbf{v}$ and $\hat H|\psi\rangle = E|\psi\rangle$ as unrelated equations.) `[verify: volume/pages unconfirmed]`
