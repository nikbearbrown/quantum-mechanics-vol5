# Module M-07 — Vectors, Vector Spaces, and Inner Products

**When you need this:** QM chapters II·1 (Hilbert-space formalism), IV·2 (entanglement and the Schmidt decomposition)

**Condensed from:** *Mathematics for Physics* Vol 1, Ch 4 (concrete 3D vectors) and Vol 2, Ch 4 (abstract vector spaces); inner-product axioms drawn from Vol 2, Ch 5

---

## The refresher

### From arrows to abstract spaces

The Vol. 1 picture is concrete: a **vector** is a quantity with magnitude and direction, written in components relative to orthonormal unit vectors $\hat\imath, \hat\jmath, \hat k$:

$$\vec A = A_x\hat\imath + A_y\hat\jmath + A_z\hat k, \qquad |\vec A| = \sqrt{A_x^2 + A_y^2 + A_z^2}.$$

Vectors add component-by-component and scale component-by-component. The dot product gives a number measuring alignment:

$$\vec A\cdot\vec B = A_xB_x + A_yB_y + A_zB_z = |\vec A||\vec B|\cos\varphi.$$

The Vol. 2 picture abstracts this. A **vector space** $V$ over a field $\mathbb{F}$ ($\mathbb{R}$ or $\mathbb{C}$) is any set of objects that can be added and scaled, with the arithmetic obeying the obvious rules: commutativity and associativity of addition, a zero vector, additive inverses, and distributivity of scalar multiplication. The elements need not be arrows. Column vectors in $\mathbb{C}^n$ qualify. Polynomials qualify. Square-integrable functions on $\mathbb{R}$, with the identification $(f + g)(x) = f(x) + g(x)$ and $(cf)(x) = c\,f(x)$, qualify — and this last example is the one quantum mechanics lives in.

### Linear independence, basis, dimension

A set of vectors $\{\mathbf v_1, \dots, \mathbf v_k\}$ is **linearly independent** if the only solution to

$$c_1\mathbf v_1 + c_2\mathbf v_2 + \cdots + c_k\mathbf v_k = \mathbf 0$$

is $c_1 = c_2 = \cdots = c_k = 0$. Intuitively: no vector in the set can be built from the others. A **basis** is a linearly independent set that also spans the space — every vector $\mathbf v \in V$ has a unique expansion $\mathbf v = \sum_i c_i\mathbf e_i$. The number of basis vectors is the **dimension** of $V$; it does not depend on which basis is chosen.

**Choosing a basis is choosing coordinates.** The same abstract vector looks different in different bases; this is why the matrix representing a linear operator changes when you change basis, even though the operator itself does not.

### Inner products: the complex (Hermitian) case

An **inner product** on a complex vector space assigns to each ordered pair $(\phi, \psi)$ a complex number $\langle\phi|\psi\rangle$ satisfying three axioms. We adopt the **physicist's convention** throughout — conjugate-linear in the *first* argument:

1. **Conjugate symmetry:** $\langle\phi|\psi\rangle = \langle\psi|\phi\rangle^*$
2. **Linearity in the second argument:** $\langle\phi\,|\,a\psi_1 + b\psi_2\rangle = a\langle\phi|\psi_1\rangle + b\langle\phi|\psi_2\rangle$
3. **Positive-definiteness:** $\langle\psi|\psi\rangle \geq 0$, with equality only if $|\psi\rangle = 0$

The **norm** is $\|\psi\| = \sqrt{\langle\psi|\psi\rangle}$. Two vectors are **orthogonal** when $\langle\phi|\psi\rangle = 0$.

The two canonical examples:

- **Finite-dimensional ($\mathbb{C}^n$):** $\displaystyle\langle\phi|\psi\rangle = \sum_{i=1}^n \phi_i^*\,\psi_i$ — note the conjugate on the first entry. Without it, $\langle\psi|\psi\rangle = \sum\psi_i^2$ need not be real.
- **Function space ($L^2$):** $\displaystyle\langle\phi|\psi\rangle = \int_{-\infty}^{\infty} \phi^*(x)\,\psi(x)\,dx$ — the continuum analogue.

The real 3D dot product is the special case $\mathbb{R}^3$ with no conjugate needed (real vectors are their own conjugates).

### The Cauchy–Schwarz inequality

For any two vectors in an inner-product space:

$$|\langle\phi|\psi\rangle|^2 \leq \langle\phi|\phi\rangle\,\langle\psi|\psi\rangle.$$

*Proof sketch.* If $|\psi\rangle = 0$ both sides vanish. Otherwise, let $|\chi\rangle = |\phi\rangle - \frac{\langle\psi|\phi\rangle}{\langle\psi|\psi\rangle}|\psi\rangle$ — the part of $\phi$ remaining after subtracting its projection onto $\psi$. Positive-definiteness requires $\langle\chi|\chi\rangle \geq 0$; expanding and clearing denominators yields the inequality. $\blacksquare$

This inequality carries significant weight: it is the engine of the Robertson uncertainty relation in Module M-09.

### Orthonormal bases and the resolution of the identity

A basis $\{|n\rangle\}_{n=1}^N$ (finite) or $\{|n\rangle\}_{n=0}^\infty$ (countably infinite) is **orthonormal** if

$$\langle m|n\rangle = \delta_{mn} = \begin{cases}1 & m = n \\ 0 & m \neq n.\end{cases}$$

From any independent set, the **Gram–Schmidt** procedure builds an orthonormal one: take vectors in turn, subtract each one's projections onto the already-orthonormalized vectors, then normalize. In an orthonormal basis, expansion coefficients are just inner products. If $|\psi\rangle = \sum_n c_n|n\rangle$, then $c_n = \langle n|\psi\rangle$ because $\langle m|\psi\rangle = \sum_n c_n\langle m|n\rangle = c_m$.

Substituting $c_n = \langle n|\psi\rangle$ back into the expansion:

$$|\psi\rangle = \sum_n |n\rangle\langle n|\psi\rangle = \left(\sum_n |n\rangle\langle n|\right)|\psi\rangle.$$

Since this holds for every $|\psi\rangle$, the operator in parentheses must be the identity:

$$\boxed{\sum_n |n\rangle\langle n| = \hat I.}$$

This is the **resolution of the identity** — the most-used identity in quantum mechanics. Each term $|n\rangle\langle n|$ is the **projector** onto the $n$-th basis direction. The whole sum reconstructs the identity because the projectors tile the space without overlap. Inserting this form of $\hat I$ into any expression is the standard technique for changing basis, computing matrix elements, or deriving the Born rule.

---

### Worked example: Gram–Schmidt in $\mathbb{C}^2$

Start with the independent (but non-orthonormal) set $\{|\mathbf u_1\rangle, |\mathbf u_2\rangle\}$ where

$$|\mathbf u_1\rangle = \begin{pmatrix}1\\i\end{pmatrix}, \qquad |\mathbf u_2\rangle = \begin{pmatrix}1\\0\end{pmatrix}.$$

**Step 1.** Normalize $|\mathbf u_1\rangle$:

$$\langle\mathbf u_1|\mathbf u_1\rangle = 1^*\cdot 1 + i^*\cdot i = 1 + (-i)(i) = 1 + 1 = 2,$$

so $|e_1\rangle = \frac{1}{\sqrt 2}\begin{pmatrix}1\\i\end{pmatrix}$.

**Step 2.** Subtract the projection of $|\mathbf u_2\rangle$ onto $|e_1\rangle$:

$$\langle e_1|\mathbf u_2\rangle = \frac{1}{\sqrt 2}(1^*\cdot 1 + i^*\cdot 0) = \frac{1}{\sqrt 2}.$$

The residual is:

$$|\mathbf u_2\rangle - \langle e_1|\mathbf u_2\rangle\,|e_1\rangle = \begin{pmatrix}1\\0\end{pmatrix} - \frac{1}{\sqrt 2}\cdot\frac{1}{\sqrt 2}\begin{pmatrix}1\\i\end{pmatrix} = \begin{pmatrix}1\\0\end{pmatrix} - \begin{pmatrix}1/2\\i/2\end{pmatrix} = \begin{pmatrix}1/2\\-i/2\end{pmatrix}.$$

Normalizing: magnitude $= \frac{1}{\sqrt 2}$, so $|e_2\rangle = \frac{1}{\sqrt 2}\begin{pmatrix}1\\-i\end{pmatrix}$.

**Check:** $\langle e_1|e_2\rangle = \frac{1}{2}(1 + i^*\cdot(-i)) = \frac{1}{2}(1 + (-i)(-i)) = \frac{1}{2}(1 - 1) = 0$. Orthogonal, as required. Note that the cross-term required the conjugate on the bra — without it the check gives $\frac{1}{2}(1 + i(-i)) = \frac{1}{2}(1+1) \neq 0$, a spurious failure.

---

## In the quantum series

### Hilbert space is an infinite-dimensional inner-product space

The state space of quantum mechanics is not $\mathbb{C}^n$ for any finite $n$ (except for spin-only problems) but rather $L^2(\mathbb{R})$ or a tensor product of copies of it — an **infinite-dimensional** complete inner-product space called a **Hilbert space**. "Complete" means that every Cauchy sequence of vectors converges to a vector *in the space*; this is the technical condition that keeps limits well-behaved and is assumed without proof here. States are unit vectors: $\langle\psi|\psi\rangle = 1$. The inner product is $\langle\phi|\psi\rangle = \int\phi^*(x)\psi(x)\,dx$.

Everything from this module carries over to the infinite-dimensional case with one substitution: sums $\sum_n$ over discrete basis indices become integrals $\int dk$ when the basis is continuous (position eigenstates, momentum eigenstates). The resolution of the identity in the position basis reads

$$\int_{-\infty}^{\infty} |x\rangle\langle x|\,dx = \hat I, \qquad \langle x|x'\rangle = \delta(x - x'),$$

where the Kronecker delta has been replaced by the Dirac delta (Module M-06). This gives the wavefunction its meaning: $\psi(x) = \langle x|\psi\rangle$ is just the component of the state $|\psi\rangle$ in the continuous position basis.

### The Born rule as a projection

The expansion $|\psi\rangle = \sum_n c_n|a_n\rangle$ in an energy (or any observable) eigenbasis, with $c_n = \langle a_n|\psi\rangle$, is the resolution of the identity applied to a state. The Born rule says the probability of measuring eigenvalue $a_n$ is

$$P(a_n) = |c_n|^2 = |\langle a_n|\psi\rangle|^2.$$

This is the squared projection of the state onto the eigenstate — a geometric fact about inner-product spaces with no additional content beyond what this module develops. Normalization of $|\psi\rangle$ ensures $\sum_n|c_n|^2 = 1$ (probabilities sum to one), which is just the Pythagorean theorem in Hilbert space: $\langle\psi|\psi\rangle = \sum_n|c_n|^2$.

### Entanglement and the tensor-product inner product (QM IV·2)

For a two-particle system, the state space is the **tensor product** $\mathcal H_A \otimes \mathcal H_B$. If $\{|a_m\rangle\}$ is an orthonormal basis for $\mathcal H_A$ and $\{|b_n\rangle\}$ for $\mathcal H_B$, then $\{|a_m\rangle\otimes|b_n\rangle\}$ is an orthonormal basis for $\mathcal H_A\otimes\mathcal H_B$, with inner product that factors:

$$\langle a_m\otimes b_n\,|\,a_{m'}\otimes b_{n'}\rangle = \langle a_m|a_{m'}\rangle\,\langle b_n|b_{n'}\rangle = \delta_{mm'}\delta_{nn'}.$$

A general state in $\mathcal H_A\otimes\mathcal H_B$ is $|\Psi\rangle = \sum_{m,n} c_{mn}|a_m\rangle\otimes|b_n\rangle$. It is **entangled** if it cannot be written as a single product $|\alpha\rangle\otimes|\beta\rangle$; the **Schmidt decomposition** — essentially a singular-value decomposition applied to the coefficient matrix $c_{mn}$ — identifies this: a state is entangled if and only if its Schmidt rank (number of nonzero singular values) exceeds one. Without comfort with bases, orthonormality, and expansion coefficients, the concept of entanglement has no mathematical content.

---

## Conventions and pitfalls

**1. Physicist vs. mathematician convention.** Physicists put the conjugate on the *first* slot: $\langle\phi|\psi\rangle = \sum\phi_i^*\psi_i$. Mathematicians often put it on the second. The quantum series uses the physicist's convention exclusively. State it once; never switch.

**2. Forgetting the conjugate.** Writing $\langle a\phi|\psi\rangle = a\langle\phi|\psi\rangle$ instead of $a^*\langle\phi|\psi\rangle$ is the single most common error. The mnemonic: scalars pulled out of the *bra* (first slot) get conjugated. Pulled out of the ket: unchanged.

**3. Real vs. complex orthogonality.** For real vectors, $\langle\phi|\psi\rangle = 0$ looks like geometric perpendicularity. For complex vectors, $\langle\phi|\psi\rangle = 0$ is an algebraic condition with no visual meaning. Do not try to picture it as perpendicular arrows.

**4. Infinite dimension.** The finite-dimensional basis intuition (a basis is a finite list of vectors) generalizes, but completeness requires limits. $L^2(\mathbb{R})$ is complete; not every inner-product space is. The distinction matters if you want to guarantee that a Cauchy sequence of states converges to a state.

**5. The cross product is not needed.** The Vol. 1 source covers the cross product at length; it is irrelevant here. QM uses only the inner product. Omit it.

---

## Quick practice

**1.** Let $|\phi\rangle = \frac{1}{\sqrt 2}(1, i)^T$ and $|\psi\rangle = \frac{1}{\sqrt 2}(1, -i)^T$ in $\mathbb{C}^2$. Compute $\langle\phi|\psi\rangle$ and $\langle\psi|\phi\rangle$. Verify $\langle\phi|\psi\rangle = \langle\psi|\phi\rangle^*$ and check that both are orthonormal.

**2.** A normalized state $|\psi\rangle = \frac{3}{5}|0\rangle + \frac{4i}{5}|1\rangle$ (in an orthonormal basis $\{|0\rangle,|1\rangle\}$). Use the resolution of the identity to find $\langle 0|\psi\rangle$ and $\langle 1|\psi\rangle$, then verify $|\langle 0|\psi\rangle|^2 + |\langle 1|\psi\rangle|^2 = 1$.

**3.** Show by direct calculation that the set $\{|\alpha\rangle, |\beta\rangle\}$ where $|\alpha\rangle = (1, 0, i)^T/\sqrt{2}$ and $|\beta\rangle = (0, 1, 0)^T$ is orthonormal in $\mathbb{C}^3$. Find a third vector $|\gamma\rangle$ orthonormal to both. (*Hint: use Gram–Schmidt starting from $(i, 0, 1)^T$, then normalize.*)

---

## Go deeper

For the full development of concrete 3D vectors (components, dot product derivation via law of cosines, cross product as oriented area): **Vol. 1, Ch. 4** of *Mathematics for Physics*.

For abstract vector spaces, linear independence, basis, dimension, linear maps as matrices, and the spectral theorem proof: **Vol. 2, Ch. 4**.

For inner-product axioms, Gram–Schmidt, resolution of the identity, and Dirac notation: **Vol. 2, Ch. 5** — which is the direct source for Module M-09.

**Hard cases:** For the rigorous treatment of infinite-dimensional Hilbert spaces and the subtleties of completeness and convergence, see J. von Neumann, *Mathematical Foundations of Quantum Mechanics* (Princeton, 1955), or Reed and Simon, *Methods of Modern Mathematical Physics, Vol. I* (Academic Press, 1972).

---

## References

- Wilson, E. B. *Vector Analysis.* Yale University Press, 1901. (Founded on lectures of J. Willard Gibbs; established the dot product and component formalism in modern form.) `[verify]`
- Grassmann, H. *Die lineale Ausdehnungslehre.* Wiegand, 1844. (The exterior/wedge product as oriented area; precursor to abstract vector spaces.) `[verify]`
- Nguyen, T., and D. E. Meltzer. "Initial understanding of vector concepts among students in introductory physics courses." *American Journal of Physics* **71**, 630–638 (2003). DOI 10.1119/1.1571831. `[verify]`
- Hilbert, D. "Grundzüge einer allgemeinen Theorie der linearen Integralgleichungen." *Nachrichten von der Gesellschaft der Wissenschaften zu Göttingen*, 1904. (Introduced inner-product-space methods and the spectral idea two decades before quantum mechanics.) `[verify: full publication details]`
- Dirac, P. A. M. *The Principles of Quantum Mechanics.* 4th ed. Oxford University Press, 1958. (The state-space and inner-product formalism as physicists use it.) `[verify edition]`
- von Neumann, J. *Mathematische Grundlagen der Quantenmechanik.* Springer, 1932. English translation: *Mathematical Foundations of Quantum Mechanics.* Princeton University Press, 1955. (Rigorous Hilbert-space formulation; proves completeness theorems omitted here.) `[verify]`
