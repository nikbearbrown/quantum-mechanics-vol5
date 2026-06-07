# CAJAL Figure Intelligence — 07-vectors-vector-spaces-and-inner-products

**Source:** /Users/bear/Documents/CoWork/bear-textbooks/books/quantum-mechanics-vol5/chapters/07-vectors-vector-spaces-and-inner-products.md
**Scan:** /scan silent
**Date:** 2026-06-06

---

## Zones Detected

| Concept | Zone | Rationale |
|---|---|---|
| From arrows to abstract vector spaces | VG | Structural claim: geometric arrows, column vectors in ℂⁿ, and L² functions all satisfy the same axioms — three realizations of one abstraction, no figure |
| Inner product in ℂⁿ requires conjugate on first slot | VG | Geometric/structural claim — without the conjugate, ⟨ψ|ψ⟩ need not be real; algebraic pitfall with no visual grounding |
| Gram–Schmidt orthonormalization | MC | 3-step mechanism: take vector → subtract projection onto prior basis → normalize → repeat; produces orthonormal set |
| Resolution of the identity | VG | Structural claim: projectors |n⟩⟨n| tile the space; each projects onto one direction and the sum reconstructs any vector |
| Born rule as projection | VG | P(aₙ) = |⟨aₙ|ψ⟩|² — squared inner product magnitude equals probability; geometric claim about projection length, no figure |
| Cauchy–Schwarz inequality | VG | |⟨φ|ψ⟩|² ≤ ‖φ‖²‖ψ‖² — geometric claim about maximum inner product; proof via residual-vector positivity |

**Density recommendation: 3 figures, Mixed density.**

---

## Figure 1 — CRITICAL

**Concept:** Three structurally identical vector spaces — geometric arrows in ℝ², column vectors in ℂⁿ, and square-integrable functions on ℝ — all obey the same addition and scaling axioms, showing that the abstract vector space concept is satisfied by objects as different as arrows and wave functions.

**Block 1 — Illustrae Paste Block:**
Draw on a single-column 89mm wide vector canvas with white background in three side-by-side panels of equal width. Left panel: draw a 2D Cartesian mini-grid with two orthogonal axes in #000000 at 0.5pt; draw a single arrow from origin to approximately (0.7, 0.6) in #0072B2 at 1.5pt; draw dashed projections to both axes in #000000 at 0.5pt with right-angle brackets. Middle panel: draw two narrow vertical rectangles side by side representing column vector components, each with three stacked horizontal segments in #56B4E9 at 1pt; draw a small plus sign (a cross shape made of two short lines) between them in #000000; draw a third rectangle to the right in #56B4E9 representing their sum. Right panel: draw a horizontal axis in #000000 at 0.5pt; draw a smooth sinusoidal curve in #009E73 at 1pt; draw a second smooth sinusoidal curve of different frequency in #E69F00 at 1pt; draw a third smooth curve below them in #CC79A7 at 1pt representing their pointwise sum. Draw a thin horizontal bracket or arc above all three panels in #000000 at 0.5pt. No text; unannotated.

**Block 2 — Full SCOPE Prompt:**
[S] Single-column 89mm wide three-panel vector figure, white background.
[C] Three realizations of vector spaces: (1) geometric arrow in ℝ² with component projections onto two orthogonal axes; (2) column vectors in ℂⁿ with addition shown as two columns plus a third sum column; (3) two smooth functions on ℝ with their pointwise sum shown as a third curve. A unifying bracket or arc above all three panels indicates shared vector-space structure.
[O] Three panels equal width and height; left panel arrow in first quadrant with dashed projections; middle panel two narrow column-segment stacks with a plus between and sum column to right; right panel three curves on shared axis with top two being summands and bottom being sum; bracket spans all three panels.
[P] Flat vector, Okabe-Ito hexes: geometric arrow #0072B2; column-vector rectangles #56B4E9; first function #009E73; second function #E69F00; sum function #CC79A7; projections and axes #000000; bracket #000000; unannotated.
[E] No cross product; no dot product formula; no inner product; no tensor product; no Hilbert space label; no coordinate number labels; no dual space; no norm notation; no ℝ³ perspective; no function labels f, g.

**Block 3 — Negative Prompt:**
No cross product arrows, no inner product angle brackets, no tensor product symbol, no coordinate axis numbers, no function name labels, no Hilbert space annotation, no 3D perspective on the arrow; text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, non-standard arrows, dual-headed arrows, hand-drawn styles, visual clutter, watermarks, red-green color combinations, 3D perspective distortion.

---

## Figure 2 — CRITICAL

**Concept:** The Gram–Schmidt procedure converts any linearly independent set into an orthonormal one through a three-step mechanism: normalize the first vector, subtract the projection of each subsequent vector onto the already-orthonormalized ones, then normalize the residual.

**Block 1 — Illustrae Paste Block:**
Draw on a single-column 89mm wide vector canvas with white background in three side-by-side panels. Left panel (step 1): draw two non-orthogonal arrows from a common origin at approximately 30° apart in #0072B2 (longer) and #E69F00 (slightly shorter) at 1.5pt each, neither unit length. Middle panel (step 2): draw the first arrow now shortened to unit length in #0072B2 at 1.5pt with a dashed arc of radius 1.0 in #000000 at 0.5pt indicating unit length; draw the second arrow in #E69F00 at 1.5pt unchanged; draw a dashed projection line from the tip of the second arrow perpendicularly onto the first arrow direction in #000000 at 0.5pt with a right-angle mark; draw a short residual arrow perpendicular to the first arrow in #D55E00 at 1.5pt. Right panel (step 3): draw two arrows from the same origin exactly perpendicular to each other in #0072B2 and #009E73 at 1.5pt, both ending at the same radius, with a small right-angle square between them in #000000 at 0.5pt. No text; unannotated.

**Block 2 — Full SCOPE Prompt:**
[S] Single-column 89mm wide three-panel vector figure, white background.
[C] Step 1 (left): two non-orthonormal vectors from shared origin — both at an acute angle, neither unit-length. Step 2 (middle): first vector normalized to unit length (unit-circle arc confirming length); second vector projected onto first with dashed perpendicular; residual arrow perpendicular to first. Step 3 (right): completed orthonormal pair — two arrows exactly perpendicular with right-angle square, both unit length.
[O] Three panels same size; left panel two arrows at acute angle; middle panel unit arc, projection dash, and residual arrow all present; right panel only two arrows at 90° with square; visual progression from non-orthonormal to orthonormal readable left to right.
[P] Flat vector, Okabe-Ito hexes: first vector #0072B2; second vector #E69F00; residual arrow #D55E00; completed orthonormal second #009E73; right-angle square #000000; unit arc #000000 dashed; projection dash #000000; unannotated.
[E] No inner product formula; no coordinate axis labels; no complex vector components; no algebraic step annotations; no Gram–Schmidt formula; no 3D vectors; no resolution of the identity in this figure.

**Block 3 — Negative Prompt:**
No algebraic formula overlays, no inner product angle bracket symbols, no complex number notation, no axis label text, no 3D arrow perspective; text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, non-standard arrows, dual-headed arrows, hand-drawn styles, visual clutter, watermarks, red-green color combinations, 3D perspective distortion.

---

## Figure 3 — IMPORTANT

**Concept:** The resolution of the identity asserts that an orthonormal basis tiles the space — each basis projector |n⟩⟨n| projects a state onto one direction, and the sum of all projections reconstructs the original vector exactly via the parallelogram law.

**Block 1 — Illustrae Paste Block:**
Draw on a single-column 89mm wide vector canvas with white background. Draw two orthogonal unit arrows from the origin at 0° and 90° in #56B4E9 at 1.5pt with a small right-angle square between them in #000000 at 0.5pt. Draw a general state arrow from origin to approximately (0.6, 0.7) in #0072B2 at 1.5pt. Draw dashed perpendicular lines from the tip of the state arrow to the horizontal axis and to the vertical axis in #000000 at 0.5pt, each with a right-angle mark at the foot. Draw two component arrows along the horizontal axis from origin to (0.6, 0) in #009E73 at 1.5pt and along the vertical axis from origin to (0, 0.7) in #E69F00 at 1.5pt. Draw a parallelogram outline connecting the two component tips and the state vector tip in #000000 at 0.3pt dashed, showing the reconstruction of the state from its components. Fill the interior angle between the two basis vectors with very light gray fill at 5% opacity. No text; unannotated.

**Block 2 — Full SCOPE Prompt:**
[S] Single-column 89mm wide vector figure, white background.
[C] Two orthonormal basis vectors along horizontal and vertical axes; right-angle square between them; a general state vector at oblique angle; dashed perpendicular projections from the state tip to each axis with right-angle marks; two component arrows along each basis direction; parallelogram construction showing the sum of components equals the state; very light fill in the first-quadrant plane region indicating space is tiled. Maximum 6 visual elements: two basis arrows, state arrow, two component arrows, parallelogram outline.
[O] Basis vectors along x and y; state in first quadrant; component horizontal clearly shorter than full vector; component vertical clearly shorter than full vector; parallelogram closes at state tip; fill subtle.
[P] Flat vector, Okabe-Ito hexes: basis arrows #56B4E9; state #0072B2; c₁e₁ component #009E73; c₂e₂ component #E69F00; right-angle square #000000; projections #000000 dashed; parallelogram #000000 dashed 0.3pt; fill light gray; unannotated.
[E] No summation formula; no Dirac notation angle brackets; no Born rule probability annotation; no continuous resolution with Dirac delta; no Cauchy–Schwarz inequality diagram; no infinite-dimensional notation; no axis tick numbers.

**Block 3 — Negative Prompt:**
No summation formula, no Dirac bra-ket notation, no Born rule labels, no Dirac delta spike, no infinite dimension annotations, no axis tick labels; text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, non-standard arrows, dual-headed arrows, hand-drawn styles, visual clutter, watermarks, red-green color combinations, 3D perspective distortion.

---

## Video Candidate Pass

**VIDEO CANDIDATE — Figure 2 (Gram–Schmidt orthonormalization):** The learning target is the sequential causal mechanism: take a vector → subtract its projection → normalize the residual → repeat. This is a 3-stage process where the intermediate state (non-orthonormal residual) exists only between steps and is not visible in any single frozen frame. Watching the acute-angle pair transform into a right-angle pair, with the projection and residual constructed dynamically, makes the algorithm's logic self-evident. The cyclic return (Step 1 → Step 2 → Step 3 with a clear start and end) further qualifies this as a strong video candidate.

**Count: 1 video candidate.**
**Recommendation:** Animate Figure 2 — start with two non-orthogonal arrows, animate the normalization of the first, draw the projection dynamically, then show the residual arrow pivoting to perpendicular and normalizing. A 4–6 second loop covering all three steps would replace the static three-panel diagram as the primary learning artifact.
