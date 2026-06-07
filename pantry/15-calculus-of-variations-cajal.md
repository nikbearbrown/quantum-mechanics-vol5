# CAJAL Figure Intelligence — 15-calculus-of-variations

**Source:** `books/quantum-mechanics-vol5/chapters/15-calculus-of-variations.md`
**Scan mode:** /scan silent
**Date:** 2026-06-06

---

## Zones Detected

| Concept | Heuristic | Notes |
|---|---|---|
| Neighboring-path variation $\bar{y}(x) = y(x) + \varepsilon\eta(x)$ with endpoint pinning | VG | Prose describes wiggling a path and pinning its ends; this geometric claim is never drawn |
| Integration-by-parts step: boundary term vanishes because $\eta=0$ at endpoints | MC | The step has 3+ interdependent parts (IBP setup → boundary term → fundamental lemma); all in equations, no geometric anchor |
| Path-integral constructive/destructive interference: stationary path dominates | VG | "Phase varies rapidly far from stationary path, contributions cancel" is a geometric/oscillatory claim asserted in prose only |
| Variational upper bound: $\langle H\rangle \geq E_0$ proof via expansion in eigenstates | MC | Multi-step chain (expand in eigenbasis → multiply by $E_n \geq E_0$ → sum = 1) is the load-bearing argument; no visual |

**Density recommendation: 2 figures, Mechanistic density.**

---

## Figure 1 — Varied Paths and Fixed Endpoints

**Rank: CRITICAL**

**Concept statement:** The variation $\bar{y}(x) = y(x) + \varepsilon\eta(x)$ adds a smooth wiggle to the candidate stationary path while keeping both endpoints fixed, and the stationarity condition $\delta S = 0$ must hold for every such wiggle.

---

**Block 1 — Illustrae Paste Block**

Produce a single-column 89mm vector figure on a white background with a single coordinate plane. Draw a horizontal $x$-axis spanning from a left endpoint to a right endpoint; place two small filled circles (#000000, radius 3pt) at the left and right endpoints to mark the fixed boundary conditions. Draw one smooth curve connecting the two endpoints as the candidate stationary path in #0072B2 at 2pt weight; this curve should have a gentle single arch. Draw two additional smooth curves connecting the same two endpoints as trial variations: one curves slightly above the stationary path (stroke #E69F00, 1pt, dashed) and one curves slightly below (stroke #D55E00, 1pt, dashed). Between the stationary path and the upper variation, draw a short vertical double-ended segment with a small arrowhead at each end in #009E73 at 1pt, placed near the horizontal midpoint, to indicate the displacement $\varepsilon\eta$ at that $x$-value. All three curves share the same two endpoint dots. No text; unannotated.

---

**Block 2 — Full SCOPE Prompt**

[S] Single-column 89mm, single panel, vector, white background.

[C] The candidate stationary path $y(x)$ as a smooth arch connecting two fixed endpoints. Two trial variations $y(x) + \varepsilon\eta(x)$: one above, one below, each passing through the same two fixed endpoint dots. A displacement indicator at one interior $x$ value showing the magnitude $\varepsilon\eta$ between the stationary path and one variation. All geometry is directly from the chapter's section on The Variation.

[O] The fixed endpoint dots are the visual anchor — they establish the boundary condition $\eta(x_1) = \eta(x_2) = 0$ geometrically. The spread of variation curves around the stationary path makes the optimization domain legible. The displacement indicator connects the abstract $\varepsilon\eta$ notation to a geometric measurement.

[P] Flat vector. Okabe-Ito: #0072B2 2pt solid for stationary path; #E69F00 1pt dashed and #D55E00 1pt dashed for the two variations; #009E73 1pt for the displacement segment; #000000 3pt dots for endpoints. Unannotated.

[E] No text labels, no axis tick marks or values, no third variation curve, no shading between curves, no constraint force vectors, no specific function form imposed (curves are schematic, not computed), no caustics or conjugate points, no multiple stationary paths.

---

**Block 3 — Negative Prompt**

No shading between path curves, no labels for $x_1$, $x_2$, $y$, $\varepsilon$, $\eta$, no axis labels, no multiple minima or saddle-point scenarios, no constraint force arrows, no second-order variation geometry. text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, non-standard arrows, dual-headed arrows, hand-drawn styles, visual clutter, watermarks, red-green color combinations, 3D perspective distortion.

---

## Figure 2 — Path-Integral Phase Cancellation and Constructive Interference

**Rank: IMPORTANT**

**Concept statement:** In Feynman's path integral, paths far from the stationary action have rapidly varying phase and cancel by destructive interference, while paths near the stationary path have slowly varying phase and add constructively, so the classical trajectory dominates the sum.

---

**Block 1 — Illustrae Paste Block**

Produce a single-column 89mm vector figure on a white background with two side-by-side sub-panels connected by a horizontal layout. Left sub-panel: draw a family of five smooth curves connecting two fixed endpoint dots (#000000, 3pt), representing different paths in the path integral; color the central curve #0072B2 at 2pt (the stationary path), color the two nearest neighbors #009E73 at 1pt, and color the two outermost curves #E69F00 at 1pt. At the midpoint of each curve attach a small unit-circle phasor diagram (radius 6pt, stroke #000000 0.5pt) showing the phase angle of $e^{iS/\hbar}$ for that path: the two outermost phasors point in scattered directions (approximately opposing each other), the two inner phasors point in nearly the same direction as the stationary-path phasor, which points straight up. Right sub-panel: draw a vertical arrow-accumulation diagram showing the phasor addition: the two outer phasors (short, #E69F00) cancel, the two inner phasors (medium, #009E73) nearly align, and the stationary-path phasor (tall, #0072B2) stands dominant; the net resultant arrow is drawn in #0072B2 at 2pt pointing upward. No text; unannotated.

---

**Block 2 — Full SCOPE Prompt**

[S] Single-column 89mm, two equal sub-panels side by side, vector, white background.

[C] Left panel: five paths from endpoint to endpoint, representing the path-integral sum. The central path is the stationary action path. Phasor indicators at each path's midpoint showing that distant paths have scattered phase while near-stationary paths have coherent phase. Right panel: phasor addition diagram showing cancellation of distant-path contributions and survival of the near-stationary contribution. Concept directly from the chapter's path-integral section.

[O] Left-to-right: geometry of paths → consequence in phasor addition. The color coding carries the grouping: outer (canceling) paths in #E69F00, inner (coherent) paths in #009E73, stationary path in #0072B2.

[P] Flat vector. Okabe-Ito: #0072B2 for stationary path and its phasor; #009E73 for near-neighbor paths; #E69F00 for distant paths; #000000 for endpoint dots and phasor circle outlines. 1pt strokes on phasor circles. Unannotated.

[E] No labels for $S$, $\hbar$, or $\varepsilon$, no quantum field theory context, no saddle-point approximation details, no Morse theory, no specific Lagrangian form, no equations overlaid on the figure, no imaginary/real axis labels on phasors, no quantitative phase values.

---

**Block 3 — Negative Prompt**

No Feynman diagram vertices, no quantum field theory notation, no loop diagrams, no labels on paths or phasors, no axes labeled with $S$ or $\hbar$, no specific numerical phase values, no saddle-point contour deformations. text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, non-standard arrows, dual-headed arrows, hand-drawn styles, visual clutter, watermarks, red-green color combinations, 3D perspective distortion.

---

## Video Candidate Pass

No video candidates identified. The varied-path geometry (Figure 1) is a static spatial relationship, not a temporal process — showing it animated adds no conceptual content the static figure does not already convey. The integration-by-parts derivation is a sequential algebraic procedure; its sequential nature is captured in a printed derivation with annotation more cleanly than in a video. The path-integral phase cancellation (Figure 2) involves many simultaneous contributions rather than a causal chain with a return-to-start structure.

**Total video candidates: 0.**
