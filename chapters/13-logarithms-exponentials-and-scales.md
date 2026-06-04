# Module M-13 — Logarithms, Exponentials, and Scales

**When you need this:** QM Series Vol. I, Chapter 6 (Barrier Penetration); Vol. III, Chapter 4 (WKB Approximation)

**Condensed from:** *Mathematics for Physics, Vol. 2*, Ch. 1

---

## The refresher

### The fundamental property and the laws

The logarithm answers: *to what power must I raise the base to get this number?* If $y = b^x$, then $x = \log_b y$. The entire usefulness of the logarithm flows from one consequence of the exponent laws:

$$\boxed{\;\log_b(ac) = \log_b a + \log_b c.\;}$$

**The logarithm turns multiplication into addition.** The companion laws follow immediately:

$$\log_b\!\left(\frac{a}{c}\right) = \log_b a - \log_b c, \qquad \log_b(a^n) = n\,\log_b a.$$

**Change of base:** $\log_b a = \dfrac{\log_c a}{\log_c b}$, so in particular $\log_{10} a = \dfrac{\ln a}{\ln 10} \approx \dfrac{\ln a}{2.303}$.

> **Warning — the single most common error.** There is *no* law for $\log(a + b)$. The identity $\log(ac) = \log a + \log c$ applies to *products only*. Writing $\log(E_1 + E_2) = \log E_1 + \log E_2$ is always false. If you see a sum inside a logarithm, it cannot be split.

### Why $e$ is not optional

The base that physics keeps producing on its own is $e \approx 2.71828$, singled out by the property $\dfrac{d}{dx}e^x = e^x$ — the exponential that is its own derivative. Physics generates $e$ because processes constantly obey the rule *the rate of change of a quantity is proportional to the quantity itself*:

$$\frac{dN}{dt} = kN.$$

Separating variables ($dN/N = k\,dt$, integrate, exponentiate) gives

$$N(t) = N_0\,e^{kt}.$$

If $k > 0$, exponential growth; if $k = -\lambda < 0$, exponential decay. The half-life of a decaying quantity is the time for $N$ to halve: setting $N(t_{1/2}) = N_0/2$ and solving with the logarithm gives

$$\boxed{\;t_{1/2} = \frac{\ln 2}{\lambda} \approx \frac{0.693}{\lambda}.\;}$$

The mean lifetime is $\tau = 1/\lambda$, so $t_{1/2} = \tau \ln 2$.

### Linearizing data — the two key diagnostics

Two functional forms, two types of axes, two straight-line diagnostics:

| Law | Take $\log_{10}$ of both sides | Straight line on |
|-----|-------------------------------|-----------------|
| $y = A\,x^k$ (power law) | $\log y = k\log x + \log A$ | **log–log axes** (slope $= k$) |
| $y = A\,e^{kx}$ (exponential) | $\log y = \frac{k}{\ln 10}\,x + \log A$ | **semi-log axes** (slope $= k/\ln 10$) |

*Power law → line on log–log; exponential → line on semi-log.* Which one straightens your data tells you which kind of law you have.

### Worked example — half-life from a semi-log plot

**Problem.** A radioactive sample gives the following count rates (proportional to $N$):

| Time $t$ (h) | Rate (counts/min) |
|---|---|
| 0 | 1200 |
| 2 | 670 |
| 4 | 375 |
| 6 | 210 |

Is this exponential? If so, find $\lambda$ and $t_{1/2}$.

**Step 1 — check linearity.** Take $\ln$ of each rate:

$$\ln 1200 \approx 7.09, \quad \ln 670 \approx 6.51, \quad \ln 375 \approx 5.93, \quad \ln 210 \approx 5.35.$$

Differences per hour: $(7.09 - 5.35)/6 = 0.29$ per hour, consistent across intervals — a straight line on semi-log axes confirms the exponential law.

**Step 2 — read the slope.** Fitting a line: slope $= -\lambda = -0.29\ \mathrm{h}^{-1}$, so $\lambda = 0.29\ \mathrm{h}^{-1}$.

**Step 3 — compute the half-life.**

$$t_{1/2} = \frac{\ln 2}{\lambda} = \frac{0.693}{0.29} \approx 2.4\ \mathrm{h}.$$

Check: at $t = 2.4\ \mathrm{h}$, the rate should be $1200/2 = 600$ counts/min; interpolating the table gives roughly 600. Consistent.

---

## In the quantum series

### The exponential in the classically forbidden region

In barrier-penetration problems (Vol. I, Ch. 6), the time-independent Schrödinger equation in a region where $E < V$ is

$$-\frac{\hbar^2}{2m}\frac{d^2\psi}{dx^2} + V\psi = E\psi \;\Longrightarrow\; \frac{d^2\psi}{dx^2} = \kappa^2\psi, \qquad \kappa \equiv \frac{\sqrt{2m(V-E)}}{\hbar}.$$

The general solution is $\psi(x) = A e^{+\kappa x} + B e^{-\kappa x}$ — real exponentials, not complex waves. Because $\kappa > 0$, the growing solution $e^{+\kappa x}$ diverges and is rejected on normalizability grounds; the physical solution in the forbidden region is the **decaying exponential** $\psi(x) \propto e^{-\kappa x}$.

The transmission probability through a rectangular barrier of width $L$ is

$$\boxed{\;T \approx e^{-2\kappa L}, \qquad \kappa = \frac{\sqrt{2m(V_0 - E)}}{\hbar}.\;}$$

This is the same $e^{-\lambda t}$ structure as radioactive decay, but in the *spatial* variable $x$ rather than time. The "decay constant" is $\kappa$ (units: m$^{-1}$), and the "lifetime" is $1/\kappa$ — the spatial scale over which the wavefunction falls to $1/e$ of its value.

**The habit that saves you:** evaluate the exponent before computing $T$. If $2\kappa L = 10$, then $T \approx e^{-10} \approx 4.5 \times 10^{-5}$ — a five-order-of-magnitude suppression — without touching a calculator. If $2\kappa L = 0.1$, then $T \approx 1 - 0.1 \approx 0.9$ — essentially no suppression. Knowing which regime you are in before doing algebra is what physicists actually do.

**Useful numbers to internalize** (electron, $V_0 - E = 1\ \mathrm{eV}$):

$$\kappa \approx 5.1 \times 10^9\ \mathrm{m}^{-1} \approx 5.1\ \mathrm{nm}^{-1}.$$

This means barriers narrower than $\sim 0.2\ \mathrm{nm}$ give significant tunneling ($\kappa L \lesssim 1$); barriers wider than $\sim 2\ \mathrm{nm}$ are effectively opaque ($\kappa L \gtrsim 10$, $T \lesssim 10^{-9}$).

| $2\kappa L$ | $T = e^{-2\kappa L}$ | qualitative |
|---|---|---|
| 0.5 | $\approx 0.61$ | substantial |
| 2 | $\approx 0.14$ | partial |
| 10 | $\approx 4.5 \times 10^{-5}$ | very small |
| 20 | $\approx 2 \times 10^{-9}$ | negligible |
| 50 | $\approx 2 \times 10^{-22}$ | essentially zero |

Rule of thumb: each 2.3 units of $2\kappa L$ reduces $T$ by one order of magnitude ($e^{-2.303} = 10^{-1}$).

### The WKB generalization — the exponent becomes an integral

For a non-rectangular barrier where $V(x)$ varies with position (Vol. III, Ch. 4), the WKB approximation gives

$$T \approx \exp\!\left(-\frac{2}{\hbar}\int_{x_1}^{x_2}\!\sqrt{2m\bigl(V(x) - E\bigr)}\,dx\right),$$

where $x_1, x_2$ are the classical turning points (where $V = E$). This is still an exponential in a negative exponent — the form is identical to the rectangular case — but the exponent is now an integral of $\sqrt{V - E}$ rather than the constant $\kappa L$. Taking the logarithm of the WKB transmission probability directly extracts this integral:

$$\ln T = -\frac{2}{\hbar}\int_{x_1}^{x_2}\!\sqrt{2m(V(x)-E)}\,dx.$$

**The Gamow factor for alpha decay** is exactly this integral, applied to the Coulomb barrier around a nucleus. The decay rate $\lambda \propto e^{-G}$ where $G = \frac{2}{\hbar}\int_R^{R_c}\!\sqrt{2m(V_\text{Coulomb}(r)-E)}\,dr$. Small changes in the nuclear charge $Z$ or the decay energy $E$ produce enormous changes in $\lambda$ — because the changes enter the *exponent*. This exponential sensitivity is why nuclear half-lives span from nanoseconds to $10^{10}$ years: a range of $10^{26}$, compressed to manageable numbers on a log scale.

### Order-of-magnitude estimation — the core skill

The semi-log reasoning built up for radioactive decay transfers directly to tunneling. A plot of $\ln T$ versus barrier width $L$ is a straight line of slope $-2\kappa$. From the slope you extract $\kappa$, and from $\kappa = \sqrt{2m(V_0-E)}/\hbar$ you extract the barrier height above the particle energy.

**Example.** An experiment on a scanning tunneling microscope measures that the tunneling current drops by a factor of $e^{1}$ for each $0.1\ \mathrm{nm}$ ($1\ \text{\AA}$) increase in tip–sample distance. What is the effective $\kappa$?

The current is proportional to $T = e^{-2\kappa L}$. A change $\Delta L = 0.1\ \mathrm{nm}$ changes $\ln(\text{current})$ by $-2\kappa\,\Delta L = -1$, so

$$\kappa = \frac{1}{2 \times 0.1\ \mathrm{nm}} = 5\ \mathrm{nm}^{-1} = 5 \times 10^9\ \mathrm{m}^{-1}.$$

This corresponds to a 1 eV effective barrier for an electron. The exponential sensitivity to tip height — current changes by a factor of $e$ per Ångstrom of distance — is why the STM achieves atomic resolution. The logarithm turns a one-order-of-magnitude sensitivity into a linear, readable signal.

---

## Conventions and pitfalls

**Exponents must be dimensionless.** $e^{-2\kappa L}$ requires $\kappa L$ to be a pure number. $\kappa$ has units m$^{-1}$; $L$ has units m; the product is dimensionless. A common error is to work with $\kappa$ in nm$^{-1}$ and $L$ in m — unit mismatch by a factor of $10^9$. Check units before computing the exponent.

**Sign of the exponent.** In the classically forbidden region ($E < V$), the wavefunction is a real decaying exponential with *negative* exponent. If your calculation gives $e^{+|\kappa|x}$ as the physical solution inside the barrier, stop: the growing exponential is not normalizable and must be rejected. The physical solution always has the *decaying* sign.

**$T \leq 1$ is a hard constraint.** If your calculation gives $T > 1$, the exponent has the wrong sign. Quick check: is $2\kappa L > 0$? If yes, $e^{-2\kappa L} < 1$. This sanity check catches sign errors before they propagate.

**$\ln$ versus $\log_{10}$.** The WKB formula uses the natural exponential $e$ throughout. "Take the log to linearize" means take $\ln$, which gives the rate constant directly as the slope. Using $\log_{10}$ gives slope $= -2\kappa / \ln 10 \approx -2\kappa / 2.303$ — correct but requires a conversion step. State which base you are using.

**$e^{a+b} = e^a \cdot e^b$, not $e^a + e^b$.** For a barrier in two segments with different $\kappa$ values, the total transmission is $T = e^{-2\kappa_1 L_1} \cdot e^{-2\kappa_2 L_2} = e^{-2(\kappa_1 L_1 + \kappa_2 L_2)}$ — the exponents add, not the transmissions. This is the log law $\log(ac) = \log a + \log c$ running in reverse: products become sums in the exponent.

**No log-of-a-sum identity.** When dealing with $(V(x) - E)$ inside the WKB integral, remember that $\ln(V - E)$ cannot be split. The log acts on the final numerical value, not term by term.

---

## Quick practice

1. **Tunneling estimate.** An electron ($m = 9.11 \times 10^{-31}\ \mathrm{kg}$) encounters a rectangular barrier with $V_0 - E = 2\ \mathrm{eV}$ and width $L = 0.5\ \mathrm{nm}$. (a) Compute $\kappa$. (b) Compute $2\kappa L$. (c) Estimate $T$ without a calculator, to within a factor of 3, using the table above or the rule $e^{-2.3} \approx 10^{-1}$.

2. **Semi-log reasoning.** A measurement of tunneling current $I$ versus barrier width $L$ gives: $I = 4.2\ \mu\mathrm{A}$ at $L = 0.3\ \mathrm{nm}$, and $I = 0.07\ \mu\mathrm{A}$ at $L = 0.9\ \mathrm{nm}$. (a) Plot $\ln I$ against $L$ mentally and find the slope. (b) Extract $\kappa$ from the slope. (c) Estimate the effective barrier height $V_0 - E$ in eV.

3. **WKB exponent.** The WKB transmission through a triangular barrier (linear $V(x)$ from $V_0$ at $x=0$ to $V=E$ at $x=L$) gives an exponent $\frac{2}{\hbar}\int_0^L \sqrt{2m(V_0 - V_0 x/L - E + V_0 x/L + E \cdot x/L)}\,dx$. Without evaluating the integral, write down its units and confirm the exponent is dimensionless.

---

## Go deeper

For the full derivation of the log and exponential laws, the decay ODE, power-law vs. exponential linearization, and worked examples in decibels and radiocarbon dating: *Mathematics for Physics, Vol. 2*, Ch. 1 (the source chapter for this module). For the WKB derivation and connection formulas: QM Series Vol. III, Ch. 4.

---

## References

- E. Rutherford and F. Soddy, "The Cause and Nature of Radioactivity," *Philosophical Magazine* 4 (1902), pp. 370–396 and 569–585. [verify]
- G. Gamow, "Zur Quantentheorie des Atomkernes," *Zeitschrift für Physik* 51 (1928), pp. 204–212 — the tunneling model of alpha decay and the Gamow factor. [verify]
- R. H. Fowler and L. Nordheim, "Electron Emission in Intense Electric Fields," *Proceedings of the Royal Society A* 119 (1928), pp. 173–181 — field emission as quantum tunneling; the exponential suppression. [verify]
- G. Binnig, H. Rohrer, Ch. Gerber, and E. Weibel, "Surface Studies by Scanning Tunneling Microscopy," *Physical Review Letters* 49 (1982), pp. 57–61 — the STM; exponential sensitivity of tunneling current to tip–sample distance. [verify]
- J. Napier, *Mirifici Logarithmorum Canonis Descriptio* (Edinburgh, 1614) — the invention of logarithms.
