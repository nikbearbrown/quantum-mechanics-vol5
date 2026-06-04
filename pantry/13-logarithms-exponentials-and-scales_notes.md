# Research Notes: Module M-13 — Logarithms, Exponentials, and Scales

**Optional companion module.** Refresher for QM chapters: I·6 (barrier penetration / tunneling), III·4 (WKB approximation)
**Condensed from:** `_lib_mfp2-01-logarithms-exponentials-and-scales.md`
**Generated:** 2026-06-03

---

## A. The tool (key results condensed; the formulas that matter; a worked example)

### A1. Core log/exponential laws

**The fundamental property:**

$$\log_b(ac) = \log_b a + \log_b c$$

Logarithm turns multiplication into addition. Companion laws:

$$\log_b\!\left(\frac{a}{c}\right) = \log_b a - \log_b c, \qquad \log_b(a^n) = n\log_b a$$

**Change of base:**

$$\log_b a = \frac{\log_c a}{\log_c b} \qquad\Longrightarrow\qquad \log_{10} a = \frac{\ln a}{\ln 10} \approx \frac{\ln a}{2.3026}$$

**There is no law for log(a+b).** The single most common error. The identity log(ac) = log a + log c applies to products only. Write this warning explicitly in the module.

**Why e is natural:** the differential equation dN/dt = kN has solution N(t) = N_0 e^{kt}. The base e is singled out by being its own derivative: d/dx(e^x) = e^x. Physics keeps producing this ODE (any process where the rate of change is proportional to the current value), so e keeps appearing.

### A2. Exponential growth/decay — the central ODE

The fundamental equation of exponential behavior:

$$\frac{dN}{dt} = kN \;\Longrightarrow\; N(t) = N_0\,e^{kt}$$

Derivation by separation of variables: dN/N = k dt → ln N = kt + C → N = N_0 e^{kt}.

For decay (k = -λ, λ > 0):

$$N(t) = N_0\,e^{-\lambda t}$$

**Half-life** — time for N to halve:

$$\frac{N_0}{2} = N_0 e^{-\lambda t_{1/2}} \;\Longrightarrow\; \boxed{t_{1/2} = \frac{\ln 2}{\lambda} \approx \frac{0.693}{\lambda}}$$

**Mean lifetime** (QM decay width notation: Γ = ℏ/τ):

$$\tau = \frac{1}{\lambda}, \qquad t_{1/2} = \tau\ln 2$$

**QM tunneling connection:** the wavefunction amplitude in a classically forbidden region decays as ψ(x) ∝ e^{-κx} with κ = √(2m(V-E))/ℏ. The transmission probability goes as T ∝ e^{-2κL} for a barrier of width L. This is the exponential decay structure — the same mathematics as radioactive decay, but now in the spatial coordinate.

### A3. Linearizing data — the two key diagnostics

**Power law:** y = A x^k

Take log_10 of both sides:

$$\log_{10} y = k\,\log_{10} x + \log_{10} A$$

On **log-log axes** (both axes logarithmic), this is a straight line. **Slope = the exponent k.** The intercept gives log₁₀(A).

**Exponential:** y = A e^{kx}

Take log_10:

$$\log_{10} y = \frac{k}{\ln 10}\,x + \log_{10} A$$

On **semi-log axes** (log y, linear x), this is a straight line. **Slope = k/ln10**; recover k by multiplying slope by ln 10 ≈ 2.303.

**Diagnostic pair to memorize:**
- Data straight on log-log → power law; slope = exponent
- Data straight on semi-log → exponential; slope × ln 10 = rate constant

### A4. The tunneling exponent — explicit QM formula

For a rectangular barrier, height V₀, width L, particle energy E < V₀, the WKB transmission amplitude (QM I·6, III·4):

$$T \approx e^{-2\kappa L}, \quad \kappa = \frac{\sqrt{2m(V_0 - E)}}{\hbar}$$

**Reading this exponentially:** T is small when κL is large. The exponent -2κL is linear in L. On a semi-log plot, ln T vs. L gives a straight line of slope -2κ. Measuring the slope extracts κ, and hence (V₀ - E) if the mass is known.

**Order-of-magnitude estimate:** for an electron (m_e = 9.11 × 10⁻³¹ kg), barrier excess V₀ - E = 1 eV = 1.6 × 10⁻¹⁹ J, barrier width L = 1 nm = 10⁻⁹ m:

$$\kappa = \frac{\sqrt{2 \times 9.11\times10^{-31} \times 1.6\times10^{-19}}}{1.055\times10^{-34}} \approx 5.1\times10^9 \;\text{m}^{-1}$$

$$2\kappa L \approx 2 \times 5.1\times10^9 \times 10^{-9} \approx 10.2$$

$$T \approx e^{-10.2} \approx 3.7\times10^{-5}$$

This is the kind of back-of-envelope calculation that QM I·6 requires. Knowing that κ ≈ 5×10⁹ m⁻¹ for a 1 eV barrier means that barriers narrower than ~1/κ ≈ 0.2 nm give significant tunneling; barriers wider than 2 nm are essentially opaque.

**WKB general case:** for a non-rectangular barrier, the exponent generalizes to an integral:

$$T \approx \exp\!\left(-\frac{2}{\hbar}\int_{x_1}^{x_2}\!\sqrt{2m(V(x)-E)}\,dx\right)$$

This is still an exponential, but the exponent is an integral rather than 2κL. The log of T gives the integral directly — so taking the log of a WKB transmission probability extracts a line integral of √(V - E), the "action" through the barrier.

### A5. Orders of magnitude and semi-log reasoning

**Fundamental skill:** given e^{-κL}, estimate its magnitude without a calculator.

- e^{-1} ≈ 0.37 (about 1/3)
- e^{-2} ≈ 0.14 (about 1/7)
- e^{-10} ≈ 4.5 × 10⁻⁵
- e^{-20} ≈ 2 × 10⁻⁹
- e^{-70} ≈ 10⁻³⁰ (completely negligible)

Rule of thumb: e^{-2.303} ≈ 10⁻¹, so each 2.3 units of the exponent reduces T by one order of magnitude. For κL = 10, T ≈ 10⁻⁴·⁴ — a five-order-of-magnitude suppression.

**Quantum tunneling sensitivity:** T goes as e^{-2κL}, so T is exponentially sensitive to L. A 10% increase in barrier width gives a 10% increase in 2κL, which multiplies T by e^{-0.1 × 2κL}. For κL = 10, a 10% wider barrier gives T → T × e^{-2} ≈ 0.14 T — tunneling is seven times less likely. This extreme sensitivity is why scanning tunneling microscopes (STM) have atomic resolution — a 0.1 nm change in tip height changes the tunneling current by roughly a factor of e^{-1} ≈ 3.

**WKB exponential for α decay:** the Gamow factor for alpha decay from a nucleus is:

$$G = \exp\!\left(-\frac{2}{\hbar}\int_{R}^{R_c}\!\sqrt{2m(V_{\text{Coulomb}}(r)-E)}\,dr\right)$$

The decay rate (inverse half-life) goes as e^{-G}. The exponential sensitivity to Z and E explains why nuclear half-lives vary from nanoseconds to 10¹⁰ years — an enormous dynamic range compressed to manageable numbers on a log scale.

### A6. Worked example — reading a tunneling exponent

**Problem:** The tunneling transmission through a Josephson junction can be written T = T₀ e^{-αΔ} where Δ is the superconducting gap and α is a parameter depending on the junction geometry. Measurements give T₀ = 0.85 and α = 12 eV⁻¹. For a gap Δ = 1.5 meV:

**Step 1 — compute the exponent:**

$$\alpha\Delta = 12\;\text{eV}^{-1} \times 1.5\times10^{-3}\;\text{eV} = 0.018$$

**Step 2 — compute T:**

$$T = 0.85 \times e^{-0.018} \approx 0.85 \times 0.982 \approx 0.83$$

A small exponent: the gap barely suppresses transmission. Now if the gap doubles to 3 meV: αΔ = 0.036, T ≈ 0.85 × 0.965 ≈ 0.82. Still barely suppressed.

**Now a semiconductor barrier:** T = e^{-2κL} with κ = 5×10⁹ m⁻¹, L = 2 nm:

$$2\kappa L = 2 \times 5\times10^9 \times 2\times10^{-9} = 20, \quad T = e^{-20} \approx 2\times10^{-9}$$

The same functional form, vastly different regime. The skill is to evaluate the exponent first and immediately estimate the magnitude.

**Reading a semi-log plot:** given a plot of ln(tunneling current) vs. barrier width, with slope -1.5 nm⁻¹:

$$-2\kappa = -1.5\;\text{nm}^{-1} \;\Longrightarrow\; \kappa = 0.75\;\text{nm}^{-1} = 7.5\times10^8\;\text{m}^{-1}$$

$$V_0 - E = \frac{\hbar^2\kappa^2}{2m} = \frac{(1.055\times10^{-34})^2\times(7.5\times10^8)^2}{2\times9.11\times10^{-31}} \approx 0.023\;\text{eV}$$

A very shallow effective barrier. The log of the transmission probability, treated as a linear function of L, extracts the barrier height directly from the slope.

---

## B. Where the quantum series uses it (specific QM chapters + how)

**QM I·6 — Barrier Penetration:**
- The wavefunction in the classically forbidden region is ψ ∝ e^{-κx} (exponentially decaying). The transmission coefficient T ∝ e^{-2κL}. Students must evaluate κ from barrier parameters, compute 2κL, and interpret the resulting T as a probability.
- Semi-log reasoning: a plot of ln T vs. L is linear with slope -2κ. Students often plot T on linear axes and see a rapidly decreasing curve they cannot easily interpret. The semi-log plot makes the exponential structure transparent.
- The concept of "the wavefunction doesn't stop at the barrier, it just decays exponentially" is mathematical before it is physical — students need to know that e^{-κx} is a real, positive, decreasing function, not a complex wave.

**QM III·4 — WKB Approximation:**
- The WKB connection formulas involve e^{±∫κ dx} — exponential growth and decay in the classically forbidden region. The tunneling amplitude is determined by the exponent -(1/ℏ)∫√(2m(V-E)) dx evaluated numerically or analytically.
- The semiclassical approximation selects the decaying exponential (not the growing one) in the forbidden region — this is a regularity/boundary condition argument that has the same structure as the termination conditions in M-11, but now applied to the exponential function.
- The Gamow factor for alpha decay is a direct application: compute the integral, take the exponential, get the decay rate. The half-life follows via t_{1/2} = ln2/λ (A2 above).
- Order-of-magnitude reasoning: students need to estimate whether a barrier gives significant or negligible tunneling without full numerical solution. The estimate from A4 (e^{-10} ≈ 10⁻⁵ for a 1 eV, 1 nm barrier) is the template.

---

## C. Connections

- **M-04 (Series Expansions):** the exponential e^x = Σ x^n/n! is a power series. For small exponents (|κL| ≪ 1), T ≈ 1 - 2κL — first-order approximation to the tunneling probability. When the exponent is large, the full exponential is needed; when small, the series approximation is accurate. Knowing which regime applies is an order-of-magnitude judgment.
- **M-02 (Probability):** T is a probability (0 ≤ T ≤ 1). In the tunneling context, T = |transmission amplitude|². The exponential e^{-2κL} is automatically in [0,1] for κ, L > 0. Students should verify this explicitly — it is a sanity check on the sign of the exponent.
- **M-03 (ODEs):** the WKB approximation solves the Schrödinger equation approximately. The exact solution in a constant-potential forbidden region is a linear combination of e^{+κx} and e^{-κx}. The ODE context (second-order linear ODE with real solutions) is where the exponentials arise — M-13 is the tool for evaluating those solutions.
- **M-18 (Units and Estimation):** κ has units of m⁻¹; κL is dimensionless (as it must be, since it appears in an exponent). Unit checking on κ before computing 2κL is essential and easy to skip. The formula κ = √(2m(V-E))/ℏ should be checked: [kg × J]^{1/2} / [J·s] = [kg·m²/s²·kg]^{1/2} / [J·s] ... working this out carefully is a good dimensional-analysis exercise.

---

## D. Conventions and pitfalls

**The exponent must be dimensionless.** e^{-2κL} requires 2κL to be a pure number. If κ has units m⁻¹ and L has units m, the product κL is dimensionless. A common error is to mix κ in units of nm⁻¹ with L in units of m — check units before computing.

**Sign of the exponent.** In the forbidden region (E < V), the wavefunction is a real exponential (not complex). The decaying solution is e^{-κx} with κ > 0. The growing solution e^{+κx} is rejected on normalizability grounds. Students sometimes confuse the sign convention and write e^{+κx} as the physical solution — it diverges and is not normalizable.

**T ≤ 1.** The transmission probability must be between 0 and 1. If a calculation gives T > 1, something is wrong (usually the sign of the exponent or a missing factor). A quick sanity check: if 2κL > 0, then e^{-2κL} < 1. If you get T > 1, the exponent has the wrong sign.

**ln vs. log₁₀.** In the WKB formula and in the natural exponential e^{kt}, the natural logarithm ln is always the right choice. Using log₁₀ gives an answer off by a factor of ln 10 ≈ 2.303. When the source says "take the log of both sides" to linearize an exponential, confirm which log is being taken: ln gives the rate constant directly (slope = k); log₁₀ gives slope = k/ln10.

**e^{a+b} = e^a · e^b, not e^a + e^b.** When a tunneling exponent involves a sum of terms (e.g., a barrier in two segments with different κ values), the transmission is the product of the individual e^{-2κ₁L₁} · e^{-2κ₂L₂} = e^{-2κ₁L₁ - 2κ₂L₂}, not their sum. Logarithms add; exponentials multiply.

**Reading the exponent before computing T.** Standard practice: before evaluating e^{-x}, estimate x. If x = 50, the answer is essentially zero (e^{-50} ≈ 2×10⁻²²). If x = 0.01, the answer is essentially 1 (e^{-0.01} ≈ 0.99). Computing e^{50} on a calculator before recognizing the result is negligible wastes time and can produce floating-point underflow. Estimate the exponent first.

---

## E. Teaching considerations

**The source (mfp2-01) is well-matched to this module** — it is explicitly framed around building fluency with log scales and exponential behavior, rather than proving theorems. It gives three worked examples (decibel, radioactive decay, Arrhenius plot) that illustrate the same technique in different contexts. The QM module should add the tunneling exponent as a fourth worked example (A4/A6 above) with the same structure.

**The "estimate the exponent first" habit is the core skill for QM.** Students who can write down T = e^{-2κL} often cannot say whether the answer is 10⁻² or 10⁻²⁰ without a calculator. The module should build the ability to estimate 2κL for typical QM parameters (electrons, ~1 eV barriers, ~1 nm widths) so that the student has an immediate physical sense of when tunneling matters.

**Useful numerics to memorize (worth including as a box):**
- κ for a 1 eV barrier on an electron ≈ 5 × 10⁹ m⁻¹ ≈ 5 nm⁻¹
- κL = 1 → T ≈ e^{-2} ≈ 14% (barrier width ≈ 0.2 nm at 1 eV)
- κL = 5 → T ≈ e^{-10} ≈ 4.5 × 10⁻⁵
- κL = 10 → T ≈ e^{-20} ≈ 2 × 10⁻⁹

**The WKB integral** (A4, general case) is conceptually a generalization of 2κL to a variable barrier. The key point for the module: the log of T is the integral, not T itself. Students who want to extract the effective barrier parameters from measured T values should plot ln T, not T.

**Connection to the STM** (scanning tunneling microscope) is pedagogically powerful. A 0.1 nm (1 Å) change in tip-sample distance changes the tunneling current by roughly e^{2κ × 0.1nm} ≈ e^1 ≈ 3. This three-fold current change per Ångstrom of height change is the basis for atomic resolution. The exponential sensitivity to distance, which makes tunneling practically useful, comes directly from the e^{-2κL} form.

**The decibel example from the source is a secondary application** — it uses the same log-ratio structure but is not directly relevant to QM. Include it briefly as motivation (compressing large dynamic ranges), then pivot quickly to the tunneling context.

---

## F. Source file used

`/Users/bear/Documents/CoWork/bear-textbooks/books/quantum-mechanics-vol5/pantry/_lib_mfp2-01-logarithms-exponentials-and-scales.md`

---

## G. Gaps and flags

**No gaps in the source coverage for the core tool.** The source chapter covers: log laws, the natural exponential and its ODE, linearization via log-log and semi-log plots, worked examples in decay and Arrhenius contexts. This is exactly the toolkit needed for QM I·6 and III·4. The source is well-suited to this module.

**The WKB integral (non-rectangular barrier) is not in the source.** The source covers the exponential e^{-λt} and e^{-κx} as constant-exponent cases. The WKB formula T ≈ exp(-2/ℏ ∫√(2m(V-E)) dx) with a position-dependent exponent is a straightforward generalization but is not derived or discussed in the source. The module should present this as a named extension: "when the barrier height varies with position, the exponent becomes an integral." No new math — just the recognition that the same exponential structure applies with an integral replacing 2κL.

**No quantum tunneling examples in the source.** The source examples are: decibels (engineering), radioactive decay (nuclear physics), and Arrhenius reaction rates (chemistry). The tunnel-barrier application must be added fresh. The worked examples in section A4 and A6 above are not in the source and must be written for the module.

**Order-of-magnitude estimation section is thin in the source.** The source mentions orders of magnitude and the enormous dynamic range of physical quantities, but does not drill the "estimate the exponent first" habit. A compact table of e^{-n} for n = 1, 2, 5, 10, 20 (see D above) would be a useful addition not present in the source.

**FLAG — log(a+b) pitfall mentioned in source but only briefly.** The source warns that "there is no law for the logarithm of a sum" and flags it as the most common error. This deserves prominent placement in the module — perhaps a highlighted warning box — because QM students frequently attempt to log-linearize expressions of the form (E₁ + E₂) or (V - E), both of which are sums.
