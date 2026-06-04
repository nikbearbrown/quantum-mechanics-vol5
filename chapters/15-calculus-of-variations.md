# Module M-15 — Calculus of Variations and Stationarity

**When you need this:** QM Series Vol. III, Chapter 3 (The Variational Method)

**Condensed from:** *Mathematics for Physics, Vol. 2*, Ch. 11

---

## The refresher

### The conceptual upgrade: from functions to functionals

Ordinary calculus extremizes a *function*: you have $f(x)$ depending on a number $x$, and you find the best $x$ by setting $f'(x) = 0$. The calculus of variations is the exact conceptual upgrade: you extremize a **functional** — a machine that takes an entire *function* $y(x)$ and returns a single number.

The canonical example is a functional of the form

$$S[y] = \int_{x_1}^{x_2} L\bigl(y,\, y',\, x\bigr)\,dx,$$

where $L$ is a given function of the path's value $y$, its slope $y' = dy/dx$, and $x$. The functional $S[y]$ depends on the *whole shape* of $y(x)$, not on a single number.

**Terminology.** The quantity $S$ is called the **action** in mechanics. The correct statement of the principle is *stationarity* of the action ($\delta S = 0$), not minimization — the true path may be a saddle point, not a minimum. "Least action" is the traditional name and is often literally true, but "stationary action" is the honest word.

### The variation

To extremize $S[y]$, mimic ordinary calculus: nudge the whole path and demand the first-order change vanish. Let $y(x)$ be the candidate stationary path and consider a neighboring trial path

$$\bar{y}(x) = y(x) + \varepsilon\,\eta(x),$$

where $\varepsilon$ is a small number and $\eta(x)$ is an arbitrary smooth "wiggle." Because both paths must hit the same *fixed endpoints*, the wiggle must vanish there:

$$\eta(x_1) = \eta(x_2) = 0.$$

This fixed-endpoint condition is load-bearing — an entire term in the derivation lives or dies by it. The **variation** $\delta S$ is the first-order change in $S$ as $\varepsilon \to 0$:

$$\delta S = \varepsilon\,\frac{d}{d\varepsilon}S[y + \varepsilon\eta]\bigg|_{\varepsilon=0}.$$

Stationarity means $\delta S = 0$ for *every* allowed wiggle $\eta$.

### Derivation of the Euler–Lagrange equation

Differentiate under the integral (the chain rule gives $\partial\bar{y}/\partial\varepsilon = \eta$ and $\partial\bar{y}'/\partial\varepsilon = \eta'$):

$$\frac{d}{d\varepsilon}S\bigg|_0 = \int_{x_1}^{x_2}\!\left(\frac{\partial L}{\partial y}\,\eta + \frac{\partial L}{\partial y'}\,\eta'\right)dx = 0.$$

The first term already has the bare $\eta$ we want. The second has $\eta'$ — integrate it by parts:

$$\int_{x_1}^{x_2}\frac{\partial L}{\partial y'}\,\eta'\,dx = \underbrace{\left[\frac{\partial L}{\partial y'}\,\eta\right]_{x_1}^{x_2}}_{\displaystyle = 0\;\text{(endpoint condition)}} - \int_{x_1}^{x_2}\frac{d}{dx}\!\left(\frac{\partial L}{\partial y'}\right)\eta\,dx.$$

The boundary term vanishes because $\eta(x_1) = \eta(x_2) = 0$. Forgetting this is the single most common student error in the derivation. What remains is

$$\int_{x_1}^{x_2}\!\left[\frac{\partial L}{\partial y} - \frac{d}{dx}\!\left(\frac{\partial L}{\partial y'}\right)\right]\eta(x)\,dx = 0.$$

This must hold for *every* wiggle $\eta(x)$. By the **fundamental lemma of the calculus of variations** (if $\int f(x)\eta(x)\,dx = 0$ for all smooth $\eta$ vanishing at the endpoints, then $f(x) \equiv 0$), the bracket must vanish pointwise:

$$\boxed{\;\frac{d}{dx}\!\left(\frac{\partial L}{\partial y'}\right) - \frac{\partial L}{\partial y} = 0.\;}$$

This is the **Euler–Lagrange equation**. Any path that makes $S$ stationary must satisfy it.

### Recovering Newton's second law

Replace $x \to t$, $y \to q$ (a generalized coordinate), $y' \to \dot{q}$, and define the **Lagrangian** $L = T - V$ (kinetic minus potential energy). The Euler–Lagrange equation becomes

$$\frac{d}{dt}\!\left(\frac{\partial L}{\partial \dot{q}}\right) - \frac{\partial L}{\partial q} = 0.$$

For a particle in one dimension: $L = \tfrac{1}{2}m\dot{x}^2 - V(x)$. Then

$$\frac{\partial L}{\partial \dot{x}} = m\dot{x} \;\Rightarrow\; \frac{d}{dt}(m\dot{x}) = m\ddot{x}, \qquad \frac{\partial L}{\partial x} = -\frac{dV}{dx}.$$

The equation reads $m\ddot{x} = -dV/dx = F$ — **Newton's second law**, recovered from a variational principle.

**Why $L = T - V$?** It cannot be derived from within classical mechanics without circularity. It is justified by what it produces: it reproduces Newton's laws, as just demonstrated. The deep "why" is Feynman's path integral (see "In the quantum series" below), where the classical path emerges as the stationary-phase limit of a sum over all paths with weight $e^{iS/\hbar}$. Assert the form, verify it gives Newton, and point onward.

### The Hamiltonian — the bridge to quantum mechanics

The **canonical momentum** conjugate to $q$ is

$$p \equiv \frac{\partial L}{\partial \dot{q}}.$$

The **Hamiltonian** is the Legendre transform of $L$:

$$H(q, p) = p\dot{q} - L.$$

Computing $dH$ from the definitions and using the Euler–Lagrange equation yields **Hamilton's canonical equations**:

$$\boxed{\;\dot{q} = \frac{\partial H}{\partial p}, \qquad \dot{p} = -\frac{\partial H}{\partial q}.\;}$$

For a conservative system with time-independent $L$, the Hamiltonian equals the total energy: $H = T + V$. This classical $H$ is the direct parent of the quantum Hamiltonian operator $\hat{H}$: promote $q \to \hat{q}$, $p \to \hat{p} = -i\hbar\nabla$, and the Schrödinger equation $\hat{H}\psi = i\hbar\,\partial\psi/\partial t$ follows. The bridge from classical to quantum runs straight through the Hamiltonian.

### Noether's theorem — one paragraph

Emmy Noether proved in 1918 that **every continuous symmetry of the action corresponds to a conserved quantity**. The simplest case: if $L$ does not depend on coordinate $q$ (it is "cyclic" or "ignorable"), then $\partial L/\partial q = 0$, and the Euler–Lagrange equation collapses to

$$\frac{d}{dt}\!\left(\frac{\partial L}{\partial \dot{q}}\right) = 0 \;\Longrightarrow\; p = \text{constant}.$$

Spatial translation symmetry gives conserved linear momentum; rotational symmetry gives conserved angular momentum; time translation symmetry (no explicit $t$ dependence) gives conserved energy. Conservation laws are not separate postulates — they are shadows of symmetries, and Noether's theorem is the lamp.

### Worked example — the pendulum without constraint forces

A simple pendulum of mass $m$ and length $\ell$, angle $\theta$ from vertical. In Cartesian coordinates the tension must be computed explicitly. In Lagrangian mechanics, choose $\theta$ as the single generalized coordinate respecting the rigid-rod constraint. The kinetic and potential energies are

$$T = \tfrac{1}{2}m\ell^2\dot\theta^2, \qquad V = -mg\ell\cos\theta,$$

so $L = \tfrac{1}{2}m\ell^2\dot\theta^2 + mg\ell\cos\theta$. Compute:

$$\frac{\partial L}{\partial \dot\theta} = m\ell^2\dot\theta, \qquad \frac{d}{dt}\!\left(\frac{\partial L}{\partial \dot\theta}\right) = m\ell^2\ddot\theta, \qquad \frac{\partial L}{\partial\theta} = -mg\ell\sin\theta.$$

The Euler–Lagrange equation gives immediately

$$m\ell^2\ddot\theta + mg\ell\sin\theta = 0 \;\Longrightarrow\; \ddot\theta = -\frac{g}{\ell}\sin\theta.$$

No tension, no resolving forces along the arc — just energy bookkeeping and one derivative. The tension was never needed because choosing $\theta$ as the coordinate automatically respects the constraint.

---

## In the quantum series

### The variational method as $\delta\langle H\rangle = 0$ (Vol. III, Ch. 3)

The quantum variational method asks: over all normalized trial wavefunctions $\psi$, which one minimizes the expectation value $\langle H\rangle = \langle\psi|\hat{H}|\psi\rangle$? That minimum is an upper bound on the ground-state energy $E_0$:

$$E_0 \leq \frac{\langle\psi|\hat{H}|\psi\rangle}{\langle\psi|\psi\rangle}$$

for any $\psi$. The inequality is exact (equality) when $\psi$ is the true ground state. This is precisely the statement that $\langle H\rangle$ is a functional $F[\psi] = \langle\psi|\hat{H}|\psi\rangle/\langle\psi|\psi\rangle$ whose minimum over all $\psi$ is $E_0$. The calculus of variations machinery — extremize a functional by demanding its variation vanish — is the background mechanism.

**The normalization constraint and the energy eigenvalue as a Lagrange multiplier.** In practice, the trial wavefunctions are required to be normalized: $\langle\psi|\psi\rangle = 1$. This is a constraint on the optimization. Handle it with a Lagrange multiplier $\lambda$: extremize the unconstrained functional

$$G[\psi] = \langle\psi|\hat{H}|\psi\rangle - \lambda\,\langle\psi|\psi\rangle.$$

Setting the variation $\delta G = 0$ with respect to variations $\delta\psi^*$ of the wavefunction gives (schematically)

$$\hat{H}|\psi\rangle = \lambda|\psi\rangle.$$

**The Lagrange multiplier is the energy eigenvalue.** The stationarity condition for $\langle H\rangle$ subject to normalization is the Schrödinger eigenvalue equation, with $\lambda = E$. The variational principle does not just bound the ground-state energy — it *derives* the energy eigenvalue equation as its stationarity condition.

This is the deepest connection between the calculus of variations and quantum mechanics: the Schrödinger equation is the Euler–Lagrange equation of the action functional $S[\psi^*, \psi] = \int\!\!\int \psi^*\bigl(i\hbar\partial_t - \hat{H}\bigr)\psi\,d^3r\,dt$, treating $\psi^*$ as the dynamical variable.

**The Rayleigh–Ritz method.** In practice, Chapter III·3 parameterizes $\psi$ as a linear combination of $n$ basis functions: $\psi = \sum_i c_i \phi_i$. The variational condition $\delta\langle H\rangle = 0$ over the coefficients $c_i$ becomes a matrix eigenvalue problem:

$$\sum_j H_{ij} c_j = E \sum_j S_{ij} c_j, \qquad H_{ij} = \langle\phi_i|\hat{H}|\phi_j\rangle, \quad S_{ij} = \langle\phi_i|\phi_j\rangle.$$

This reduces an infinite-dimensional variational problem (over all wavefunctions) to a finite-dimensional eigenvalue problem (over the $c_i$ coefficients). The accuracy improves as the basis grows.

**Why the variational bound is always an upper bound.** The exact eigenstates $\{|n\rangle\}$ form a complete basis. Any trial $|\psi\rangle = \sum_n a_n |n\rangle$ gives

$$\langle\psi|\hat{H}|\psi\rangle = \sum_n |a_n|^2 E_n \geq E_0 \sum_n |a_n|^2 = E_0,$$

using $E_n \geq E_0$ for all $n$. The lower bound $E_0$ is achieved only when $a_n = 0$ for all $n \neq 0$, i.e., when $\psi$ is exactly the ground state. Any approximation gives a value strictly above $E_0$ — the variational bound is guaranteed conservative.

### The path integral — why $L = T - V$ and the classical limit

The deep "why" of the Lagrangian formulation is Feynman's path integral: in quantum mechanics, the amplitude to go from $(q_1, t_1)$ to $(q_2, t_2)$ is the sum over *all* paths $q(t)$ connecting those endpoints, each weighted by $e^{iS[q]/\hbar}$ where $S[q] = \int_{t_1}^{t_2} L\,dt$:

$$K(q_2, t_2; q_1, t_1) = \int \mathcal{D}q(t)\; e^{iS[q]/\hbar}.$$

For paths far from the stationary point, the phase $S/\hbar$ varies rapidly and the contributions cancel by destructive interference. Near the stationary path ($\delta S = 0$), the phase is nearly constant and the contributions add constructively. In the classical limit $\hbar \to 0$, only the stationary path survives — the classical trajectory is the path of stationary action because it dominates the quantum sum. This is the honest answer to "why does nature extremize the action": it doesn't exactly; quantum mechanics sums over all paths, and the classical path is just the one that wins.

---

## Conventions and pitfalls

**"Stationary," not "least."** The principle of stationary action is the correct statement. The true path may be a saddle point rather than a minimum, particularly for paths traversing caustics or in systems with conjugate points. The quantum variational method *does* give a genuine minimum ($\langle H\rangle \geq E_0$), but the underlying Euler–Lagrange machinery is about stationarity.

**The boundary term vanishes because $\eta = 0$ at the endpoints.** This is the most commonly dropped step in student derivations. In quantum mechanics, the analogous condition is that trial wavefunctions vanish at the boundary (or decay to zero at infinity for bound states). Without boundary conditions, the integration-by-parts argument fails and the Euler–Lagrange equation picks up extra surface terms.

**$L = T - V$ is not derived within classical mechanics; it is postulated.** Do not claim otherwise. It is justified by producing Newton's laws. The Feynman path integral is the honest explanation for why $T - V$ (not $T + V$).

**Canonical momentum vs. kinetic momentum.** $p = \partial L/\partial\dot{q}$ is the *canonical* momentum. In the presence of a magnetic vector potential $\mathbf{A}$, the Lagrangian is $L = \tfrac{1}{2}m\dot{q}^2 + q_\text{charge}(\dot{\mathbf{r}}\cdot\mathbf{A} - \phi)$, and the canonical momentum $p = m\dot{q} + q_\text{charge}A$ differs from the kinetic momentum $m\dot{q}$. In QM, $\hat{p} = -i\hbar\nabla$ is the canonical momentum. This distinction matters in III·3 when the trial wavefunction is in a magnetic field.

**Functional derivative notation.** Some QM texts write the stationarity condition as $\delta\langle H\rangle/\delta\psi^* = 0$, using the functional derivative. This is the variational machinery in Dirac notation; the Euler–Lagrange equation is the special case. The notation changes; the idea does not.

**Do not confuse Lagrange multipliers in the algebraic sense with the variational context.** In the variational method, the Lagrange multiplier $\lambda$ (enforcing $\langle\psi|\psi\rangle = 1$) turns out to equal the energy eigenvalue $E$ — a non-obvious result that requires working through the stationarity condition explicitly.

---

## Quick practice

1. **The key derivation.** Derive the Euler–Lagrange equation from $\delta S = 0$ for $S[y] = \int_{x_1}^{x_2} L(y, y', x)\,dx$. Write out every step of the integration by parts. Identify precisely where $\eta(x_1) = \eta(x_2) = 0$ is used. State the fundamental lemma you invoke at the end.

2. **Variational bound.** For the infinite square well ($V = 0$ for $0 \leq x \leq a$, $V = \infty$ otherwise), the exact ground state is $\psi_0 = \sqrt{2/a}\sin(\pi x/a)$ with $E_0 = \pi^2\hbar^2/(2ma^2)$. Try the normalized trial function $\psi_\text{trial} = \sqrt{30/a^5}\,x(a-x)$ (a parabola vanishing at both walls). (a) Compute $\langle\psi_\text{trial}|\hat{T}|\psi_\text{trial}\rangle$ where $\hat{T} = -\hbar^2/(2m)\,d^2/dx^2$. (b) Compare to $E_0$. (c) Verify the variational bound holds ($\langle T\rangle \geq E_0$) and compute the percentage overestimate.

3. **Lagrange multiplier as eigenvalue.** Write $G[\psi] = \langle\psi|\hat{H}|\psi\rangle - \lambda\langle\psi|\psi\rangle$ with $\psi = \sum_n c_n|n\rangle$ where $|n\rangle$ are exact energy eigenstates. Compute $\partial G/\partial c_n^* = 0$ for each $n$ and show that the resulting equations require either $c_n = 0$ or $E_n = \lambda$. Interpret: if you want a stationary point, $\lambda$ must equal one of the energy eigenvalues.

---

## Go deeper

For the full brachistochrone derivation (cycloid answer), the Snell's law example from Fermat's principle, the Beltrami identity, and the Hamiltonian–Lagrangian formalism in generalized coordinates: *Mathematics for Physics, Vol. 2*, Ch. 11 (the source chapter for this module). For the quantum variational method and Rayleigh–Ritz in practice: QM Series Vol. III, Ch. 3.

---

## References

- J.-L. Lagrange, letter to Euler (1755) — the analytic $\delta$-method; and *Mécanique analytique* (1788) — mechanics rebuilt on a single variational principle. [verify]
- L. Euler, *Methodus inveniendi lineas curvas maximi minimive proprietate gaudentes* (1744) — the first systematic treatment of the calculus of variations; the Euler–Lagrange equation. [verify]
- W. R. Hamilton, "On a General Method in Dynamics," *Philosophical Transactions of the Royal Society* (1834, 1835) — stationary action, the Hamiltonian, and canonical equations. [verify]
- E. Noether, "Invariante Variationsprobleme," *Nachrichten von der Gesellschaft der Wissenschaften zu Göttingen* (1918) — continuous symmetry implies conserved quantity. [verify]
- R. P. Feynman and A. R. Hibbs, *Quantum Mechanics and Path Integrals* (McGraw-Hill, 1965) — the path-integral formulation; $e^{iS/\hbar}$ as the weight; the classical limit as stationary phase. [verify edition]
- Lord Rayleigh (J. W. Strutt), *The Theory of Sound*, Vol. 1 (1877) — the Rayleigh–Ritz variational method for eigenvalue bounds; minimum-energy trial functions. [verify]
- H. Goldstein, C. Poole, and J. Safko, *Classical Mechanics*, 3rd ed. (Addison-Wesley, 2002) — standard reference for Lagrangian/Hamiltonian mechanics, Noether's theorem, and canonical transformations. [verify]
