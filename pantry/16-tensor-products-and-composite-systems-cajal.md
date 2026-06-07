# CAJAL Figure Intelligence — 16-tensor-products-and-composite-systems

**Source:** `books/quantum-mechanics-vol5/chapters/16-tensor-products-and-composite-systems.md`
**Scan mode:** /scan silent
**Date:** 2026-06-06

---

## Zones Detected

| Concept | Heuristic | Notes |
|---|---|---|
| Dimension multiplication: $\dim(V \otimes W) = mn$ vs. $\dim(V \oplus W) = m+n$ | VG | Chapter states the multiplicative growth rule; the dimensional contrast between $\oplus$ and $\otimes$ is never visualized |
| Exponential growth of state-space with qubit count: $2^N$ amplitudes for $N$ qubits | PQ | Specific numbers given (30 qubits = $10^9$ amplitudes = 16 GB; 50 qubits = 16 petabytes) — quantitative comparison never charted |
| CNOT gate converts product state to Bell state (entanglement creation) | MC | Three interdependent steps: apply H → product state → apply CNOT → entangled state; all algebraic |
| Partial trace of $|\Phi^+\rangle$: reduced state is maximally mixed $I/2$ | VG | "Information is in correlations, not individual qubits" is a geometric/structural claim asserted in prose only |

**Density recommendation: 3 figures, Mixed density.**

---

## Figure 1 — Dimension Contrast: Direct Sum vs. Tensor Product

**Rank: CRITICAL**

**Concept statement:** The direct sum $V \oplus W$ of two $2$-dimensional spaces produces a $4$-dimensional space with basis elements that separately belong to $V$ or $W$, while the tensor product $V \otimes W$ produces a $4$-dimensional space whose basis elements are all ordered pairs — and only the tensor product generates entangled states.

---

**Block 1 — Illustrae Paste Block**

Produce a single-column 89mm vector figure on a white background divided into two equal side-by-side panels separated by a thin vertical divider line (#000000, 0.5pt). Left panel: show the direct sum $V \oplus W$ by drawing two separate vertical stacks of basis-vector rectangles, one stack for $V$ (two rectangles, #0072B2 fill at 40% opacity, each 22pt wide by 14pt tall) and one stack for $W$ (two rectangles, #E69F00 fill at 40% opacity, same size), with the two stacks horizontally adjacent; draw a horizontal bracket below spanning both stacks to indicate the total of 4 dimensions; the space between the stacks is 4pt. Right panel: show the tensor product $V \otimes W$ by drawing a $2 \times 2$ grid of rectangles where each cell represents a basis pair $|ij\rangle$ — the top-left is $|00\rangle$, top-right $|01\rangle$, bottom-left $|10\rangle$, bottom-right $|11\rangle$; fill grid cells using a blend encoding: top-left and top-right cells have a thin #0072B2 top border and #E69F00 right border (as L-shaped corner marks 3pt wide) to indicate the $V \otimes W$ pairing; the cell bodies are white; outer grid lines are #000000 1pt. Below the right panel grid draw a small additional rectangle in #CC79A7 at 40% opacity (same dimensions as one cell) to indicate that this space also contains non-product (entangled) elements not captured by the grid alone. No text; unannotated.

---

**Block 2 — Full SCOPE Prompt**

[S] Single-column 89mm, two side-by-side equal panels, vector, white background.

[C] Left panel: direct sum $V \oplus W$ with $\dim = 2 + 2 = 4$, depicted as two separate stacks of basis elements. Right panel: tensor product $V \otimes W$ with $\dim = 2 \times 2 = 4$, depicted as a $2 \times 2$ grid of ordered-pair basis elements, with an additional indicator for non-product (entangled) elements. All content directly from the chapter's first three sections.

[O] Side-by-side contrast is the visual argument: the left panel shows independent stacking (addition), the right panel shows pairwise combination (multiplication). The entangled-element indicator in the right panel signals that the tensor product contains more than its simple-tensor basis.

[P] Flat vector. Okabe-Ito: #0072B2 for $V$ elements, #E69F00 for $W$ elements, #CC79A7 for the entangled-state indicator, #000000 for outlines and divider. 1pt strokes. Unannotated.

[E] No text inside cells, no mathematical notation, no specific qubit states labeled, no higher-dimensional examples ($N > 2$), no density matrix diagrams, no operator matrices.

---

**Block 3 — Negative Prompt**

No Venn diagrams, no circuit diagrams, no Bloch sphere, no density matrix grids, no higher-dimensional hypercubes, no abstract category-theory notation, no labels of any kind. text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, non-standard arrows, dual-headed arrows, hand-drawn styles, visual clutter, watermarks, red-green color combinations, 3D perspective distortion.

---

## Figure 2 — Exponential State-Space Growth with Qubit Count

**Rank: IMPORTANT**

**Concept statement:** The classical memory required to represent an $N$-qubit state scales as $2^N$ complex amplitudes, growing from 4 for $N=2$ to $\sim 10^9$ for $N=30$ and $\sim 10^{15}$ for $N=50$, making exact classical simulation exponentially intractable.

---

**Block 1 — Illustrae Paste Block**

Produce a single-column 89mm vector figure on a white background with a single-panel bar chart. The horizontal axis spans integer values $N = 1$ to $N = 10$ (qubit count). The vertical axis starts at zero and shows the number of complex amplitudes $2^N$ on a linear scale from 0 to 1024. Draw one vertical bar per integer $N$; fill all bars with #0072B2 at 80% opacity; bar width is uniform with 2pt gaps between bars. At $N = 2$ draw a small filled diamond marker (#009E73, 5pt) at the top of the bar to mark the two-qubit space discussed in the chapter. At $N = 10$ the bar reaches 1024 and should be the tallest in the panel. The $y$-axis starts at zero with no break. No text; unannotated.

---

**Block 2 — Full SCOPE Prompt**

[S] Single-column 89mm, single bar-chart panel, vector, white background.

[C] Bar heights are $2^N$ for $N = 1$ through $N = 10$. The $y$-axis is linear from 0 to 1024 to correctly represent the exponential growth shape without distortion. The two-qubit case ($N=2$, 4 amplitudes) is marked because it is the primary example throughout the chapter. Values come directly from the chapter's statement about $2^N$ amplitudes.

[O] Linear $y$-axis from zero allows the exponential growth curve to be read directly from bar heights; the steepening rightward profile makes the scaling argument visual. The $N=2$ marker connects to the worked example.

[P] Flat vector. Okabe-Ito: #0072B2 bars; #009E73 diamond marker at $N=2$; #000000 for axis lines. $y$-axis from zero. Bar chart only — no line overlay. Unannotated.

[E] No logarithmic axis, no memory-unit annotations (GB, PB), no bars beyond $N=10$ (the chart would require log scale beyond this range which is excluded), no color-coding by application, no comparison to classical bits.

---

**Block 3 — Negative Prompt**

No logarithmic $y$-axis, no memory unit labels (GB, petabytes), no line plot overlaid on bars, no second $y$-axis, no comparison curve for classical bits, no $N > 10$ on a linear axis. text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, non-standard arrows, dual-headed arrows, hand-drawn styles, visual clutter, watermarks, red-green color combinations, 3D perspective distortion.

---

## Figure 3 — Partial Trace: From Pure Entangled State to Mixed Reduced State

**Rank: IMPORTANT**

**Concept statement:** Tracing out subsystem $B$ from the Bell state $|\Phi^+\rangle$ leaves subsystem $A$ in the maximally mixed state $I/2$, showing that all information about correlations is lost when only one half of an entangled pair is accessible.

---

**Block 1 — Illustrae Paste Block**

Produce a single-column 89mm vector figure on a white background arranged as a three-stage horizontal flow. Stage 1 (left): draw a 2x2 grid of cells representing the joint density matrix $\rho_{AB} = |\Phi^+\rangle\langle\Phi^+|$ in the $\{|00\rangle, |01\rangle, |10\rangle, |11\rangle\}$ basis; fill the top-left cell (row $|00\rangle$, column $|00\rangle$) and the bottom-right cell (row $|11\rangle$, column $|11\rangle$) and the top-right off-diagonal (row $|00\rangle$, column $|11\rangle$) and bottom-left off-diagonal (row $|11\rangle$, column $|00\rangle$) with #0072B2 at 70% opacity (these are the four nonzero entries of $|\Phi^+\rangle\langle\Phi^+|$); leave remaining cells white; grid outlines #000000 1pt. Draw a rightward arrow (#000000, 1.5pt) from Stage 1 to Stage 2 with a downward-curved arc over the right two columns of the grid, indicating the trace-over-$B$ operation removing those columns. Stage 2 (center): draw a 2x2 grid for $\rho_A$ in the $\{|0\rangle, |1\rangle\}$ basis; fill the diagonal cells (top-left and bottom-right) with #009E73 at 70% opacity to indicate $\frac{1}{2}I$; off-diagonal cells white; same grid style. Stage 3 (right): draw a small 2x2 grid with both diagonal cells filled #D55E00 at 40% opacity and off-diagonal white, adjacent to Stage 2, representing a generic mixed (unentangled) state for contrast. A thin vertical dashed separator (#000000, 0.5pt) separates Stage 2 from Stage 3. No text; unannotated.

---

**Block 2 — Full SCOPE Prompt**

[S] Single-column 89mm, three-stage horizontal flow, vector, white background.

[C] Stage 1: $4 \times 4$ density matrix $\rho_{AB}$ for $|\Phi^+\rangle\langle\Phi^+|$ with exactly four nonzero entries (the diagonal and anti-diagonal elements corresponding to $|00\rangle\langle00|$, $|00\rangle\langle11|$, $|11\rangle\langle00|$, $|11\rangle\langle11|$ at equal weight $\frac{1}{2}$). Stage 2: $2 \times 2$ reduced state $\rho_A = \frac{1}{2}I$ with equal diagonal entries. Stage 3: generic mixed state (diagonal-only fill) for contrast. The specific matrix entries follow directly from the partial trace calculation in the chapter.

[O] Left-to-right flow with an arc arrow emphasizing which indices are traced out. The color change from blue (entangled joint state) to green (uniform diagonal) conveys the loss of structure. Stage 3 contrast reinforces that the maximally-mixed outcome is the extreme case.

[P] Flat vector. Okabe-Ito: #0072B2 for joint state entries; #009E73 for reduced state diagonal entries; #D55E00 for contrast generic mixed state; #000000 for grid outlines and arrow. 1pt grid strokes. Unannotated.

[E] No specific numerical values shown inside cells, no additional Bell states beyond $|\Phi^+\rangle$, no von Neumann entropy formula, no bloch sphere, no multi-step trace computation grid, no operator notation overlaid.

---

**Block 3 — Negative Prompt**

No Bloch sphere, no complex-amplitude numerical annotations inside cells, no additional density matrix examples beyond the three stages, no von Neumann entropy calculation overlaid, no circuit diagram. text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, non-standard arrows, dual-headed arrows, hand-drawn styles, visual clutter, watermarks, red-green color combinations, 3D perspective distortion.

---

## Video Candidate Pass

**VIDEO CANDIDATE — CNOT Gate Creating Entanglement: Step-by-Step State Evolution**

The three-step sequence $|+\rangle|0\rangle \xrightarrow{H \otimes I} |+\rangle|0\rangle \xrightarrow{\text{CNOT}} |\Phi^+\rangle$ is a sequential causal transformation where each gate application irreversibly changes the structural character of the state (product to superposition to entangled), and the mechanism of entanglement creation — a two-qubit gate correlating previously independent subsystems — is the learning target. Each stage has a distinct geometric/algebraic character that benefits from being shown transitioning: the amplitude table at each step changes in a way that static side-by-side panels partially but not fully convey. This satisfies the 3+ sequential causal stages criterion.

**Total video candidates: 1.**
**Recommendation:** Animate the $4$-component amplitude vector $(c_{00}, c_{01}, c_{10}, c_{11})$ as a bar chart through three frames: (1) initial state $|+\rangle|0\rangle$ with two equal bars; (2) intermediate after $H \otimes I$ (same two bars); (3) final Bell state $|\Phi^+\rangle$ with $c_{00}$ and $c_{11}$ nonzero and $c_{01}=c_{10}=0$, showing the CNOT's selective action. Highlight which amplitude moves at each step.
