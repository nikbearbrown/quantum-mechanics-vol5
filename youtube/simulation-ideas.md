# Simulation Ideas — quantum-mechanics-vol5

Medhavy-register "Claude Code + Manim" workflow reels.

---

## Sim-01 — Fourier Series: Building a Square Wave from Sines
- Source: `quantum-mechanics-vol5/chapters/05-fourier-series-and-the-wave-equation.md`
- Topic: CLAUDE CODE · MANIM
- Physical rule: f(x) = Σ_n (4/nπ) sin(nπx/L) for odd n; each term a harmonic; convergence improves as N → ∞
- Concrete numbers: N=1 term: pure sine; N=3: closer to square; N=9: sharp edges (Gibbs 9% overshoot); N=99: overshoot persists at 9%
- Visual artifact: partial sums animated incrementally; see the square wave emerge; Gibbs overshoot marked at the corner
- Two testable predictions: P1: the Gibbs overshoot is always ≈9% regardless of N (does NOT go away with more terms); P2: at x=L/2 all odd harmonics contribute sin(nπ/2) = ±1, converges to 1.0 exactly
- Sim slug: medhavy-vol5-fourier-square
- Status: BUILT
- Watch: `open /Users/bear/Documents/CoWork/bear-textbooks/books/quantum-mechanics-vol5/youtube/medhavy-vol5-fourier-square/medhavy-vol5-fourier-square-review.mp4`

---

## Sim-02 — Fourier Transform: Bandwidth-Duration Uncertainty
- Source: `quantum-mechanics-vol5/chapters/06-the-fourier-transform.md`
- Topic: CLAUDE CODE · MANIM
- Physical rule: σ_t · σ_ω ≥ 1/2; Gaussian in time has Gaussian FT; width in time × width in frequency = 1/2 (minimum)
- Concrete numbers: Gaussian pulse σ_t = 1 ps → σ_ω = 0.5/(1 ps) = 5×10¹¹ rad/s → bandwidth Δν ≈ 80 GHz; compress to 0.5 ps → bandwidth doubles
- Visual artifact: two panels — pulse in time and its Fourier transform in frequency; drag slider to narrow/widen pulse and watch FT widen/narrow reciprocally
- Two testable predictions: P1: σ_t × σ_ω = 0.5 for a pure Gaussian (minimum uncertainty); P2: halving σ_t exactly doubles σ_ω (inverse proportionality)
- Sim slug: medhavy-vol5-fourier-uncertainty
- Status: BUILT
- Watch: `open /Users/bear/Documents/CoWork/bear-textbooks/books/quantum-mechanics-vol5/youtube/medhavy-vol5-fourier-uncertainty/medhavy-vol5-fourier-uncertainty-review.mp4`

---

## Sim-03 — Group vs Phase Velocity: Wave Packet Dispersion
- Source: `quantum-mechanics-vol5/chapters/18-trigonometry-waves-and-the-harmonic-model.md`
- Topic: CLAUDE CODE · MANIM
- Physical rule: v_phase = ω/k; v_group = dω/dk; for quadratic dispersion ω=ℏk²/2m: v_group = ℏk₀/m, v_phase = ℏk₀/2m (group travels twice as fast as phase)
- Concrete numbers: electron k₀ = 1 nm⁻¹; ω₀ = ℏk₀²/2m ≈ 6×10¹³ rad/s; v_group = ℏk₀/m ≈ 1.2×10⁵ m/s; v_phase = v_group/2
- Visual artifact: carrier wave crests (moving at v_phase) and envelope (moving at v_group = 2×v_phase); clearly visible mismatch — crests slide backward through the envelope
- Two testable predictions: P1: for quadratic dispersion v_group = 2 v_phase exactly (from dω/dk = 2×ω/k); P2: group velocity = centroid velocity of |ψ|² (envelope peak tracks ⟨x⟩(t))
- Sim slug: medhavy-vol5-group-phase-velocity
- Status: BUILT
- Watch: `open /Users/bear/Documents/CoWork/bear-textbooks/books/quantum-mechanics-vol5/youtube/medhavy-vol5-group-phase-velocity/medhavy-vol5-group-phase-velocity-review.mp4`

---

## Sim-04 — Multiplicity and the Peak: Combinatorics of Quantum States
- Source: `quantum-mechanics-vol5/chapters/14-combinatorics-and-multiplicity.md`
- Topic: CLAUDE CODE · MANIM
- Physical rule: multiplicity Ω(N,n) = C(N,n); peaks at n=N/2; ln Ω sharply peaked → entropy maximized at equilibrium
- Concrete numbers: N=10 spins: Ω peaks at n=5 with C(10,5)=252; next bin C(10,4)=210 (16% lower); N=100: peak/half-peak ratio >> 1000
- Visual artifact: bar chart of Ω vs n for N=10, then N=50; peak sharpens dramatically — the "why equilibrium is stable" visual
- Two testable predictions: P1: peak at exactly n=N/2 for any N (symmetry of Pascal's triangle); P2: peak height C(N,N/2) ≈ 2^N/√(πN/2) (Stirling estimate)
- Sim slug: medhavy-vol5-multiplicity-peak
- Status: BUILT
- Watch: `open /Users/bear/Documents/CoWork/bear-textbooks/books/quantum-mechanics-vol5/youtube/medhavy-vol5-multiplicity-peak/medhavy-vol5-multiplicity-peak-review.mp4`
- Note: CROSS-REFERENCE — vox-multiplicity-peak is an explainer in quantum-mechanics-vol5. This simulation workflow reel is new; build it.
