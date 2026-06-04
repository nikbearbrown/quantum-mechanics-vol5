# Module M-10 — Multivariable Calculus and Separation of Variables

**When you need this:** QM chapters II·5 (The 3D Schrödinger Equation), II·9 (The Hydrogen Atom)

**Condensed from:** *Mathematics for Physics* Vol 2, Ch 7 (primary); Vol 2, Ch 2 (partial-derivative foundations)

---

## When you need this

The moment you move from one-dimensional QM to the real world, the Schrödinger equation becomes a partial differential equation in three variables. Chapter II·5 writes it down; you immediately need to know how to handle it. The central skill is **separation of variables** — the technique that breaks a PDE in three coordinates into three independent ODEs. Chapter II·9 (hydrogen) is where it pays off most visibly: three coordinate separations produce three quantum numbers $(n, \ell, m)$, each arising from a boundary or regularity condition on the separated equation for that coordinate. If the logic of "why $m$ must be an integer" or "where the centrifugal barrier comes from" is opaque, this module is the fix.

---

## The refresher

### Partial derivatives: the essential notation

A function of several variables $f(x, y, z)$ has a separate rate of change in each direction. The **partial derivative** with respect to $x$ holds all other variables fixed:

$$\left(\frac{\partial f}{\partial x}\right)_{y,z} = \lim_{h\to 0}\frac{f(x+h, y, z) - f(x, y, z)}{h}.$$

The subscript on the parenthesis is not decoration — it names what is held fixed. When variables are genuinely independent (as $x, y, z$ are in Cartesian coordinates), the subscript is often dropped; when variables are linked by a constraint, dropping it is an error. In spherical coordinates $r, \theta, \phi$ are independent, so $\partial/\partial r$ at fixed $\theta, \phi$ is unambiguous.

The **total differential** accounts for all directions simultaneously:

$$df = \frac{\partial f}{\partial x}\,dx + \frac{\partial f}{\partial y}\,dy + \frac{\partial f}{\partial z}\,dz.$$

**Equality of mixed partials (Clairaut–Schwarz theorem).** For any smooth function,

$$\frac{\partial^2 f}{\partial y\,\partial x} = \frac{\partial^2 f}{\partial x\,\partial y}.$$

The order of differentiation does not matter. This theorem is used everywhere in what follows: the Laplacian's terms can be grouped freely, and the self-adjointness of the separated operators ultimately traces back to it.

### The gradient and the Laplacian

The **gradient** of $f$ is the vector of partial derivatives, pointing in the direction of steepest increase:

$$\nabla f = \frac{\partial f}{\partial x}\,\hat{x} + \frac{\partial f}{\partial y}\,\hat{y} + \frac{\partial f}{\partial z}\,\hat{z}.$$

The **Laplacian** $\nabla^2 f = \nabla \cdot \nabla f$ is the divergence of the gradient:

$$\nabla^2 f = \frac{\partial^2 f}{\partial x^2} + \frac{\partial^2 f}{\partial y^2} + \frac{\partial^2 f}{\partial z^2} \qquad (\text{Cartesian}).$$

The 3D time-independent Schrödinger equation is:

$$\boxed{-\frac{\hbar^2}{2m}\nabla^2\psi + V(\mathbf{r})\,\psi = E\psi.}$$

This is a PDE. Solving it requires expressing $\nabla^2$ in a coordinate system matched to the geometry of $V$, then separating variables. For a central potential $V = V(r)$, spherical coordinates are the right choice.

### The spherical Laplacian

In spherical coordinates $(r, \theta, \phi)$ — where $\theta \in [0, \pi]$ is the polar angle from the $z$-axis and $\phi \in [0, 2\pi)$ is the azimuthal angle — the Laplacian takes the form

$$\nabla^2 = \frac{1}{r^2}\frac{\partial}{\partial r}\!\left(r^2\frac{\partial}{\partial r}\right) + \frac{1}{r^2\sin\theta}\frac{\partial}{\partial\theta}\!\left(\sin\theta\,\frac{\partial}{\partial\theta}\right) + \frac{1}{r^2\sin^2\theta}\frac{\partial^2}{\partial\phi^2}.$$

This result is given without derivation (the derivation requires the metric tensor or Jacobian and is not needed for QM). The three terms correspond to radial variation, polar variation, and azimuthal variation. Their different $r$-prefactors are what make the radial and angular parts separate cleanly.

### Separation of variables: the method in four steps

The strategy is to assume the solution is a **product of single-variable functions**, substitute, and show the equation splits. Done once carefully, the pattern is clear forever.

**Illustration: the 3D infinite square well** (Cartesian coordinates, $V = 0$ inside the box $[0,L]^3$, $\psi = 0$ on the walls).

**Step 1 — product ansatz.** Guess $\psi(x,y,z) = X(x)\,Y(y)\,Z(z)$. Substitute into $-(\hbar^2/2m)\nabla^2\psi = E\psi$:

$$-\frac{\hbar^2}{2m}\bigl(X''YZ + XY''Z + XYZ''\bigr) = EXYZ.$$

**Step 2 — divide by the product.** Divide through by $XYZ$:

$$-\frac{\hbar^2}{2m}\left(\frac{X''}{X} + \frac{Y''}{Y} + \frac{Z''}{Z}\right) = E.$$

**Step 3 — the separation argument.** Each term $X''/X$ depends only on $x$; the remaining two depend only on $y$ and $z$. A function of $x$ alone that equals a function of $y$ and $z$ alone must be a constant. Therefore each ratio is separately constant:

$$\frac{X''}{X} = -k_x^2, \qquad \frac{Y''}{Y} = -k_y^2, \qquad \frac{Z''}{Z} = -k_z^2,$$

with the **constraint** $\dfrac{\hbar^2}{2m}(k_x^2 + k_y^2 + k_z^2) = E$.

The sign $-k^2$ (negative) is chosen deliberately: it gives oscillatory solutions $\sin(k_x x)$ and $\cos(k_x x)$, which can satisfy the zero-at-walls boundary condition. A positive constant would give growing/decaying exponentials, which cannot be zero at both walls simultaneously. Choosing the wrong sign is the single most common error in separation of variables.

**Step 4 — boundary conditions quantize.** The condition $X(0) = X(L) = 0$ forces $X_n(x) = \sin(n_x\pi x/L)$ with $k_x = n_x\pi/L$, $n_x = 1, 2, 3, \ldots$ The separation constant is not arbitrary — it is quantized by the boundary condition. The PDE has produced discrete eigenvalues. The total energy is

$$E_{n_x n_y n_z} = \frac{\hbar^2\pi^2}{2mL^2}\bigl(n_x^2 + n_y^2 + n_z^2\bigr), \qquad n_x, n_y, n_z = 1, 2, 3, \ldots$$

**Superposition restores generality.** A sum of product solutions is also a solution (because the Schrödinger equation is linear). The general solution is a superposition over all allowed $(n_x, n_y, n_z)$.

### Separation in spherical coordinates: the central-force split

For a **central potential** $V = V(r)$, substitute $\psi(r,\theta,\phi) = R(r)\,\Theta(\theta)\,\Phi(\phi)$ into the Schrödinger equation with the spherical Laplacian. Multiply through by $r^2/(R\Theta\Phi)$. The $\phi$ dependence appears only in the last term of the Laplacian; setting it equal to a constant $-m^2$ gives the **azimuthal equation**:

$$\frac{d^2\Phi}{d\phi^2} = -m^2\Phi \;\Longrightarrow\; \Phi(\phi) = e^{im\phi}.$$

**Regularity quantizes $m$:** the wavefunction must be single-valued — $\Phi(\phi + 2\pi) = \Phi(\phi)$ — which forces $e^{2\pi im} = 1$, hence $m \in \mathbb{Z}$. This is not a postulate. The integer character of the orbital angular momentum quantum number $m$ is a consequence of the single-valuedness requirement on a function defined on the sphere. (Spin escapes this argument because spinors are not functions on the sphere; they transform under SU(2), which admits half-integer representations.)

The remaining radial-plus-polar equation separates again. The polar part, with $u = \cos\theta$, becomes the **associated Legendre equation** with a second separation constant named $\ell(\ell+1)$:

$$\frac{d}{du}\!\left[(1-u^2)\frac{dP}{du}\right] + \left[\ell(\ell+1) - \frac{m^2}{1-u^2}\right]P = 0.$$

**Regularity quantizes $\ell$:** demanding finiteness at the poles $u = \pm 1$ (i.e., at $\theta = 0$ and $\theta = \pi$) forces $\ell$ to be a non-negative integer with $|m| \leq \ell$. The solutions are the associated Legendre functions $P_\ell^m(\cos\theta)$. The full angular factor is the **spherical harmonic**:

$$Y_{\ell m}(\theta,\phi) = N_{\ell m}\,P_\ell^m(\cos\theta)\,e^{im\phi}.$$

The **radial equation** is the last step. With the angular part separated and contributing the constant $\ell(\ell+1)$, the equation for $R(r)$ becomes

$$-\frac{\hbar^2}{2m}\frac{1}{r^2}\frac{d}{dr}\!\left(r^2\frac{dR}{dr}\right) + \left[\frac{\hbar^2\ell(\ell+1)}{2mr^2} + V(r)\right]R = ER.$$

The term $\hbar^2\ell(\ell+1)/(2mr^2)$ is the **centrifugal barrier** — it comes not from any classical assumption but directly from the separation constant $\ell(\ell+1)$ that the angular equation contributed. The angular separation has left its mark on the radial equation.

Crucially: the angular equation never involved $V(r)$. The spherical harmonics $Y_{\ell m}$ are the angular eigenfunctions for **every** central potential — hydrogen, the 3D harmonic oscillator, and the free particle alike. What differs between problems is the radial equation and its solutions.

---

## Worked example: the 3D infinite square well and its degeneracy

A particle in a cubic box $[0, L]^3$, $V = 0$ inside. From the separation above:

$$E_{n_x n_y n_z} = \frac{\hbar^2\pi^2}{2mL^2}(n_x^2 + n_y^2 + n_z^2), \qquad n_x, n_y, n_z \geq 1.$$

The ground state $(1,1,1)$ has energy $E_{111} = 3\hbar^2\pi^2/(2mL^2)$ — non-degenerate.

The first excited energy level has $(n_x^2 + n_y^2 + n_z^2) = 6$, achieved by the three states $(2,1,1)$, $(1,2,1)$, $(1,1,2)$. All three have the same energy but different wavefunctions — a **3-fold degeneracy**, arising purely from the cubic symmetry of the box. The wavefunction for $(2,1,1)$ is $\psi \propto \sin(2\pi x/L)\sin(\pi y/L)\sin(\pi z/L)$ — a product of three factors, each determined by a separate, independent ODE.

This is the first appearance of degeneracy from spatial symmetry in the series: the box has the same length in all three directions, so permuting $(n_x, n_y, n_z)$ gives states with the same energy but genuinely different spatial structure.

---

## In the quantum series

### QM II·5 — The 3D Schrödinger Equation

The chapter opens by writing the 3D Schrödinger equation with the full spherical Laplacian. The product ansatz $\psi = R(r)\Theta(\theta)\Phi(\phi)$ is the first move. The module above gives you the mechanics: how to substitute, how the division-by-product creates terms that each depend on only one variable, and why those terms must therefore be individually constant. The quantum numbers $\ell$ and $m$ appear as separation constants — not from angular momentum algebra (that comes later in the series) but from the geometry of the Laplacian in spherical coordinates.

The 3D infinite square well (Cartesian separation) is the cleanest entry point: same four steps, simpler algebra, concrete energy levels and degeneracy. Work through it completely before tackling the spherical case.

### QM II·9 — The Hydrogen Atom

The hydrogen atom is the central-force problem with $V(r) = -e^2/(4\pi\varepsilon_0 r)$. The angular separation is identical to the general case above — it produces $Y_{\ell m}$ regardless of the potential. The new content is the radial equation for the Coulomb potential, whose solutions are the associated Laguerre polynomials (see Module M-11). The principal quantum number $n$ arises from a termination condition on the radial power series, exactly as the energy eigenvalues of the 1D harmonic oscillator arise from terminating the Hermite series.

The key architectural point: the three quantum numbers $(n, \ell, m)$ arise from three different places in the separation:
- $m$ from the azimuthal equation, via single-valuedness
- $\ell$ from the polar equation, via finiteness at the poles
- $n$ from the radial equation, via normalizability (series termination)

No number is postulated. Every one is a boundary or regularity condition in disguise.

---

## Conventions and pitfalls

**Sign of the separation constant.** This is the most-documented error in teaching separation of variables. A negative separation constant $-k^2$ gives oscillatory solutions; a positive one gives exponentials. The choice is dictated by which boundary condition must be met: zero-at-walls requires oscillation, so the constant must be negative. Choose the sign before you write the ODE.

**Spherical coordinate conventions.** The QM series uses the physics convention: $\theta \in [0, \pi]$ is the polar angle (colatitude, measured from the $z$-axis), and $\phi \in [0, 2\pi)$ is the azimuthal angle. Mathematics texts and some engineering references reverse $\theta$ and $\phi$. When consulting any external source, verify the convention first. Mixing them makes $Y_{10} \propto \sin\theta$ instead of $\cos\theta$.

**The angular equation does not see the potential.** The $Y_{\ell m}$ functions are universal for central potentials because $V(r)$ factors out of the angular part when dividing by $\psi = R\Theta\Phi$. Students who memorize the hydrogen wavefunctions as "hydrogen's angular functions" are wrong — they are the angular functions of every spherically symmetric problem.

**Why not cylindrical?** Cylindrical coordinates separate the Schrödinger equation for problems with cylindrical symmetry (quantum wires, 2D confinement). The radial part in that geometry gives Bessel functions instead of associated Laguerre polynomials. The QM chapters II·5 and II·9 focus on spherical geometry, so we focus here on spherical separation. The cylindrical case is covered under Bessel functions in Module M-11.

**Termination vs. regularity quantization.** Two distinct mechanisms produce discrete eigenvalues in separation: (1) a power-series solution that must *terminate* to remain normalizable (Hermite polynomials, Laguerre polynomials), and (2) finiteness at a *singular endpoint* of the ODE (Legendre polynomials at $u = \pm 1$). Do not conflate them. Both are regularity conditions, but they arise at different stages and from different structural properties of the ODE.

---

## Quick practice

1. **Sign choice.** Separate $\partial^2\psi/\partial x^2 + \partial^2\psi/\partial y^2 = 0$ on the strip $0 \leq x \leq L$, $y \geq 0$, with $\psi = 0$ at $x = 0, L$ and $\psi \to 0$ as $y \to \infty$. Explain why the separation constant must be negative for $X(x)$ and positive for $Y(y)$, and write down the allowed modes.

2. **Degeneracy count.** For the 3D infinite square well of side $L$, list all $(n_x, n_y, n_z)$ triples that give the second excited energy level (the third distinct energy value). What is the degeneracy, and what symmetry of the box causes it?

3. **Where $m$ comes from.** Starting from the azimuthal equation $\Phi'' = -m^2\Phi$ with solution $\Phi = e^{im\phi}$, state the regularity condition that forces $m \in \mathbb{Z}$, and explain in one sentence why this argument fails for spin-$\tfrac{1}{2}$.

---

## Go deeper

The separation mechanics and the spherical-coordinate Laplacian are developed fully in *Mathematics for Physics* Vol 2, Ch 7 ("Special Functions and Separation of Variables"), Sections 3–6. The thermodynamics-focused Ch 2 of the same volume is not the right reference for QM; its partial-derivative foundations (total differential, multivariable chain rule) provide helpful background if the notation is unfamiliar, but the separation machinery lives in Ch 7.

---

## References

- Griffiths, D. J. *Introduction to Quantum Mechanics*, 3rd ed. Cambridge University Press, 2018. §4.1–4.2 (3D Schrödinger equation, separation in spherical coordinates). [verify edition]
- Shankar, R. *Principles of Quantum Mechanics*, 2nd ed. Springer, 1994. Ch. 13 (the hydrogen atom; separation in spherical coordinates derived in full). [verify]
- Boas, M. L. *Mathematical Methods in the Physical Sciences*, 3rd ed. Wiley, 2006. Ch. 13 (partial differential equations and separation of variables). [verify]
- Wawro, M., et al. "Upper-division student difficulties with separation of variables." *Physical Review Special Topics — Physics Education Research* **11**, 020131 (2015). [verify; documents the sign-of-separation-constant and single-valuedness errors this module addresses]
- Legendre, A.-M. "Recherches sur l'attraction des sphéroïdes homogènes." *Mémoires de Mathématiques et de Physique, présentés à l'Académie Royale des Sciences par divers savans* **10** (read 1782, published 1785). [The associated Legendre functions arrived from the gravitational multipole expansion, not from quantum mechanics.]
