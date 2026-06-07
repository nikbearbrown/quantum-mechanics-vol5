# CAJAL Figure Intelligence — 18-trigonometry-waves-and-the-harmonic-model

**Source:** `books/quantum-mechanics-vol5/chapters/18-trigonometry-waves-and-the-harmonic-model.md`
**Scan mode:** /scan silent
**Date:** 2026-06-06

---

## Zones Detected

| Concept | Heuristic | Notes |
|---|---|---|
| Superposition of two waves with phase difference $\delta$: amplitude $2A|\cos(\delta/2)|$ | VG | Prose derives the amplitude formula but never draws the constructive/destructive result geometrically |
| Phase velocity $v_\text{ph} = v/2$ vs. group velocity $v_g = v$ for de Broglie matter waves | VG | The distinction between a fast phase pattern and a slow wave-packet envelope is stated algebraically; the two-velocity geometry is never drawn |
| Double-slit interference fringe pattern $I(\theta) = 4A^2\cos^2(\delta/2)$ | PQ | Specific intensity formula with quantitative $\cos^2$ shape; pattern never plotted |
| Beats / group velocity: fast carrier and slow envelope from two nearby-frequency waves | MC | Three-stage mechanism: sum → product form → identify two separate velocities; the envelope/carrier structure is the learning target |

**Density recommendation: 3 figures, Mixed density.**

---

## Figure 1 — Superposition: Constructive, Destructive, and Partial Interference

**Rank: CRITICAL**

**Concept statement:** The superposition of two equal-amplitude waves with phase difference $\delta$ yields amplitude $2A|\cos(\delta/2)|$, which equals $2A$ at $\delta = 0$ (constructive), $0$ at $\delta = \pi$ (destructive), and an intermediate value for general $\delta$.

---

**Block 1 — Illustrae Paste Block**

Produce a full-width 120mm vector figure on a white background with three stacked panels of equal height, each showing one full wavelength of the wave pattern in $x$. In each panel draw the two component waves as thin curves (#E69F00 and #0072B2, 1pt dashed) and the resultant sum wave as a thicker solid curve (#009E73, 2pt). Top panel: $\delta = 0$ — both component waves are in phase; the resultant has amplitude $2A$ (the tallest curve); use a short vertical double-headed segment (#000000, 1pt) to indicate the amplitude $2A$ at the peak. Middle panel: $\delta = \pi$ — the two components are exactly anti-phase; the resultant is a flat line at zero amplitude along the $x$-axis (#009E73, 2pt, coincident with the axis). Bottom panel: $\delta = \pi/2$ — the components are offset by a quarter cycle; the resultant has intermediate amplitude $A\sqrt{2}$; use a short vertical double-headed segment (#000000, 1pt) at the peak. All panels share the same $x$-axis scale spanning one full wavelength; the $y$-axis in each panel is symmetric about zero and scaled so amplitude $2A$ fits comfortably. No text; unannotated.

---

**Block 2 — Full SCOPE Prompt**

[S] Full-width 120mm, three equal stacked panels, vector, white background. Shared $x$-axis scale.

[C] Three interference cases from the chapter's superposition section: $\delta = 0$ (constructive, resultant amplitude $2A$), $\delta = \pi$ (destructive, resultant amplitude $0$), $\delta = \pi/2$ (partial, resultant amplitude $A\sqrt{2}$). Each panel shows the two component waves and their sum. The $2A$ and $A\sqrt{2}$ amplitude indicators are consistent with the formula $2A|\cos(\delta/2)|$ derived in the chapter.

[O] Top-to-bottom stacking orders by interference outcome: maximum → zero → intermediate. The consistent color assignment (component 1 = #E69F00, component 2 = #0072B2, resultant = #009E73) lets the reader track how the sum changes as $\delta$ varies. Amplitude indicators at peaks make the $2A$ and $A\sqrt{2}$ values readable without labels.

[P] Flat vector. Okabe-Ito: #E69F00 1pt dashed (wave 1), #0072B2 1pt dashed (wave 2), #009E73 2pt solid (resultant), #000000 1pt for amplitude segments. $y$-axis symmetric about zero. Unannotated.

[E] No text on panels, no phase-offset annotation on the $x$-axis, no more than two component waves per panel, no standing wave patterns, no time-dependence shown (snapshot in $x$ only), no specific physical medium.

---

**Block 3 — Negative Prompt**

No standing-wave nodes/antinodes, no time-evolution animation frames, no three-wave superpositions, no beat-frequency patterns in this figure (handled in Figure 3), no labeled phase arrows, no phasor diagrams. text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, non-standard arrows, dual-headed arrows, hand-drawn styles, visual clutter, watermarks, red-green color combinations, 3D perspective distortion.

---

## Figure 2 — Double-Slit Fringe Intensity Pattern

**Rank: CRITICAL**

**Concept statement:** The double-slit intensity pattern $I(\theta) = 4A^2\cos^2\!\bigl(\pi d\sin\theta / \lambda\bigr)$ oscillates between 0 and $4A^2$ with bright fringes at $d\sin\theta = n\lambda$, and the fringe spacing $\Delta y = \lambda L/d$ shrinks as momentum (and hence $\lambda$) decreases.

---

**Block 1 — Illustrae Paste Block**

Produce a single-column 89mm vector figure on a white background with a single-panel line plot. The horizontal axis spans $\sin\theta$ from $-3\lambda/d$ to $+3\lambda/d$ (i.e., three fringe orders to each side). The vertical axis starts at zero and spans from 0 to $4A^2$, normalized so $4A^2 = 1$. Plot the intensity curve $I \propto \cos^2(\pi d \sin\theta / \lambda)$ as a smooth solid curve in #0072B2 at 1.5pt. The curve peaks at $\sin\theta = 0, \pm\lambda/d, \pm2\lambda/d, \pm3\lambda/d$ (seven peaks total) and reaches zero at the midpoints. Overlay a second intensity curve for a source with twice the momentum (half the wavelength) as a dashed curve in #E69F00 at 1.5pt — this curve has twice as many fringes in the same angular range. Draw a horizontal reference line at $I = 0$ (#000000, 0.5pt). The $y$-axis starts at zero. No text; unannotated.

---

**Block 2 — Full SCOPE Prompt**

[S] Single-column 89mm, single-panel line plot, vector, white background.

[C] Double-slit intensity $I(\theta) = 4A^2\cos^2(\pi d\sin\theta/\lambda)$ from the chapter's double-slit worked example, normalized to peak 1. Seven peaks for the primary wavelength ($n = 0, \pm1, \pm2, \pm3$). A second curve at $\lambda/2$ (double momentum) showing twice the fringe density, illustrating the chapter's statement "the faster the electrons, the finer the fringes." Both curves confirmed in the chapter.

[O] Two overlaid curves with different fringe spacing make the $\Delta y \propto \lambda \propto 1/p$ relationship visible without calculation. The $y$-axis from zero correctly shows the zeros of the intensity. The angular axis symmetric about zero shows the symmetric fringe pattern.

[P] Flat vector. Okabe-Ito: #0072B2 1.5pt solid for primary $\lambda$ curve; #E69F00 1.5pt dashed for $\lambda/2$ curve; #000000 0.5pt reference line at $I=0$. $y$-axis from zero. Unannotated.

[E] No single-slit diffraction envelope, no label for central maximum or order numbers, no finite-slit-width corrections, no three-slit patterns, no off-axis intensity normalization not derived from the $\cos^2$ formula, no photon-detection dots.

---

**Block 3 — Negative Prompt**

No single-slit diffraction envelope, no finite aperture corrections, no three-or-more-slit patterns, no photon-detection probability dots, no 2D fringe images, no secondary diffraction maxima from slit width. text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, non-standard arrows, dual-headed arrows, hand-drawn styles, visual clutter, watermarks, red-green color combinations, 3D perspective distortion.

---

## Figure 3 — Group Velocity vs. Phase Velocity: Carrier and Envelope

**Rank: IMPORTANT**

**Concept statement:** The superposition of two waves with nearby frequencies produces a fast-oscillating carrier traveling at phase velocity $v_\text{ph} = \omega/k$ modulated by a slow envelope traveling at group velocity $v_g = d\omega/dk$; for a non-relativistic de Broglie matter wave, $v_\text{ph} = v/2$ while $v_g = v$ equals the particle's classical speed.

---

**Block 1 — Illustrae Paste Block**

Produce a single-column 89mm vector figure on a white background with two stacked equal-height panels sharing a common horizontal $x$-axis. Top panel: draw the fast carrier wave $\cos(kx - \omega t)$ as a smooth sinusoidal curve in #0072B2 at 1pt for one snapshot in time (many oscillations visible, approximately 12 cycles across the panel); draw the slow envelope $|\cos(\frac{dk}{2}x - \frac{d\omega}{2}t)|$ as a smooth bell-shaped modulation curve in #E69F00 at 2pt, tracing the amplitude outline of the carrier; the envelope width spans roughly half the panel width. Below the carrier curve add a short rightward arrow (#0072B2, 1.5pt) indicating the phase velocity $v_\text{ph}$ pointing in the direction of carrier motion, positioned near a carrier crest; below the envelope peak add a longer rightward arrow (#E69F00, 1.5pt) at half the length of the phase-velocity arrow to indicate the group velocity $v_g$ (the group velocity is half the phase velocity for a non-relativistic matter wave with $v_\text{ph} = v/2$, $v_g = v$ — wait, actually $v_g > v_\text{ph}$; use the correct ratio: $v_g = 2v_\text{ph}$ for the non-relativistic case, so the group-velocity arrow is twice as long as the phase-velocity arrow). Bottom panel: draw the same carrier and envelope but shifted rightward in time, showing the envelope has moved a smaller distance than the carrier phase pattern; a thin vertical dashed reference line at the initial envelope peak position (#000000, 0.5pt) in the top panel should align to show that the envelope peak has advanced further than the carrier crest per unit time. No text; unannotated.

---

**Block 2 — Full SCOPE Prompt**

[S] Single-column 89mm, two equal stacked panels with shared $x$-axis, vector, white background.

[C] Top panel: snapshot at $t = 0$ of the carrier wave $\cos(kx)$ and the envelope $|\cos(dk \cdot x/2)|$. Bottom panel: snapshot at a later $t$ showing that the envelope peak has moved by $v_g \cdot \Delta t$ while the carrier crests have moved by $v_\text{ph} \cdot \Delta t$, with $v_g = 2v_\text{ph}$ for the non-relativistic de Broglie dispersion $\omega = \hbar k^2/(2m)$ (i.e., $v_\text{ph} = \hbar k/(2m) = v/2$ and $v_g = \hbar k/m = v$). Two velocity arrows in the top panel with lengths proportional to the actual velocities. A reference dashed line anchored at the top-panel envelope peak. All values from the chapter's group velocity section and the matter-waves application.

[O] Two-panel stacked snapshot sequence gives the key evidence that carrier and envelope move at different speeds without requiring animation. Velocity arrows with correct length ratio ($v_g = 2v_\text{ph}$) embed the quantitative fact geometrically. The reference dashed line makes the differential displacement readable.

[P] Flat vector. Okabe-Ito: #0072B2 1pt for carrier wave; #E69F00 2pt for envelope; #0072B2 1.5pt for phase-velocity arrow; #E69F00 1.5pt for group-velocity arrow (twice as long); #000000 0.5pt for reference dashed line. Unannotated.

[E] No specific dispersion relation curve, no relativistic case, no quantum tunneling, no three-or-more component waves, no beating in the time domain, no spatial-frequency axis, no energy labeling.

---

**Block 3 — Negative Prompt**

No dispersion relation $\omega(k)$ plot in this figure, no relativistic treatment, no frequency-domain spectrum, no labeled velocities or values, no comparison to light speed. text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, non-standard arrows, dual-headed arrows, hand-drawn styles, visual clutter, watermarks, red-green color combinations, 3D perspective distortion.

---

## Video Candidate Pass

**VIDEO CANDIDATE — Wave Packet Propagation: Phase vs. Group Velocity**

The separation between phase velocity and group velocity for a matter wave is a process where time evolution is the concept — it is literally about what moves where over time. A single-electron wave packet propagating rightward with its fast-oscillating phase pattern outrunning (or in the non-relativistic case running at half the speed of) the envelope satisfies both the sequential causal stages criterion (packet forms → carrier advances ahead of envelope → envelope arrives at detector → particle detected at envelope location, not carrier location) and the cyclic-return structure criterion (repeated oscillations). Crucially, the chapter explicitly flags this as the resolution of a paradox ("Without the beats analysis, $v_\text{ph} = v/2$ seems surprising"), indicating the mechanism is the learning target.

**Total video candidates: 1.**
**Recommendation:** Animate a Gaussian-modulated matter-wave packet propagating rightward, with a colored dot tracking the phase velocity of a carrier crest (#0072B2) and a second colored dot tracking the envelope peak (#E69F00), over approximately two envelope widths of travel. Overlay the de Broglie dispersion $\omega = \hbar k^2 / 2m$ in a small inset panel that updates in real time.
