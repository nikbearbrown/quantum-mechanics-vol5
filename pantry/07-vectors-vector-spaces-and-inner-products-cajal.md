# CAJAL Figure Report — Module M-07 — Vectors, Vector Spaces, and Inner Products

Recommended: 3 figures, Mixed density.

---

## Figure 1 — From Arrows to Abstract Spaces: Three Realizations of a Vector Space

**Heuristic:** VG — Verification Gap
**Rank:** Critical

---

**BLOCK 1 — ILLUSTRAE PASTE BLOCK**

Draw three side-by-side vertical panels representing three distinct realizations of a vector space, connected by a horizontal progression arrow. In the first panel, render a 2D Cartesian grid with a single arrow from the origin showing a concrete 3D geometric vector decomposed along two labeled axes, with a right-angle bracket indicating its component projections onto each axis. In the second panel, show a column of stacked horizontal rectangles representing a column vector in C^n, with two vector columns side by side and a third illustrating their sum. In the third panel, render two smooth wave-like curves on a horizontal axis representing function-space elements, with a third curve beneath them showing their pointwise sum. Connect all three panels with a rightward arrow indicating the progression from concrete to abstract. A small arc bracket above all three panels signals that all three satisfy the same closure, identity, and inverse structure. Use flat vector rendering with uniform 1pt strokes, white background, and no baked text.

**BLOCK 2 — FULL SCOPE**

- `[S — SPECIFICATION]` Single-column 89mm width, 300 DPI, vector (SVG/EPS), white background. Three-panel horizontal layout.
- `[C — CONTENT]` (1) Geometric arrow vector in R^2/R^3 with component projections onto orthogonal axes; (2) Column vectors in C^n with addition illustrated; (3) Square-integrable functions on R with pointwise addition. A bracketing element above all three signals shared vector-space structure (closure, zero element, additive inverse). The rightward progression arrow indicates increasing abstraction. No cross product; no divergence; no curl.
- `[O — ORGANIZATION]` Three equally spaced vertical panels arranged left-to-right, sharing a common baseline. A single horizontal arrow below the panels indicates the direction of abstraction. A large arc or bracket above all three panels is the only structural connector. No panel has more than 4 visual entities.
- `[P — PRESENTATION]` Flat vector, Okabe-Ito palette. Panel 1 arrow: Blue `#0072B2`. Panel 2 column-vector rectangles: Sky Blue `#56B4E9`. Panel 3 function curves: Bluish Green `#009E73` for first curve, Orange `#E69F00` for second, Reddish Purple `#CC79A7` for sum. Progression arrow: neutral light gray. Arc bracket: light gray. Uniform 1pt strokes, white background.
- `[E — EXCLUSIONS]` Omit: cross product, dot product formula, inner product structure (that belongs in Figure 2), tensor products, coordinate labels or numbers, dual space, any function-space completeness or norm notation, Hilbert space label.

**BLOCK 3 — NEGATIVE PROMPT**

3D perspective, cross product arrow, inner product bracket, tensor product symbol, dual space arrow, norm notation, completeness symbols, coordinate grid numbers, text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, dual-headed arrows, hand-drawn styles, human figures, visual clutter, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion.

---

## Figure 2 — Gram–Schmidt Orthonormalization: Three-Step Mechanism

**Heuristic:** MC — Mechanism/Process
**Rank:** Critical

---

**BLOCK 1 — ILLUSTRAE PASTE BLOCK**

Draw a three-panel horizontal sequence illustrating the Gram–Schmidt orthonormalization process in a 2D vector space. In the first panel, place two non-orthogonal arrows from a common origin at an acute angle — the initial linearly independent but non-orthonormal pair. In the second panel, show the first arrow normalized to unit length (a dashed circle of unit radius centered at the origin confirms its length), and a second arrow at the same angle as before, but now also draw a dashed projection line dropped perpendicularly from the tip of the second arrow onto the first, plus a short orthogonal remainder arrow pointing away from the first direction. In the third panel, show two arrows from the same origin that are exactly perpendicular, both with a small right-angle square at their base, indicating the completed orthonormal pair. A leftward-to-rightward numbered sequence (1, 2, 3) marks the progression. Use flat vector rendering, uniform 1pt strokes, white background, and no baked text.

**BLOCK 2 — FULL SCOPE**

- `[S — SPECIFICATION]` Single-column 89mm width, 300 DPI, vector (SVG/EPS), white background. Three-panel horizontal layout with step numbers.
- `[C — CONTENT]` Step 1: two non-orthonormal vectors u1, u2 from common origin. Step 2: u1 normalized to e1 (unit circle shown as dashed arc), projection of u2 onto e1 shown as a dashed component arrow, residual component shown as an arrow perpendicular to e1. Step 3: completed orthonormal pair e1 and e2, right-angle square at their junction. Sequential numbered markers 1, 2, 3 beneath each panel.
- `[O — ORGANIZATION]` Left-to-right three-panel progression. Each panel is a small 2D coordinate system (no axis labels). Dashed lines used only for the unit circle and projection components. Step numbers (1, 2, 3) are the only numeric elements; they are rendered as simple geometric shapes (circled dots or indexed triangles) without embedded text.
- `[P — PRESENTATION]` Flat vector, Okabe-Ito. First input vector: Blue `#0072B2`. Second input vector: Orange `#E69F00`. Normalized e1: Blue `#0072B2`. Projection dashed arrow: light gray. Residual arrow: Vermillion `#D55E00` (the "remainder" to subtract). Completed e2: Bluish Green `#009E73`. Right-angle square: Sky Blue `#56B4E9`. Unit-circle arc: light gray dashed. Uniform 1pt strokes.
- `[E — EXCLUSIONS]` Omit: inner-product formula, coordinate axis labels, numeric vector components, complex vector notation, algebraic steps, the resolution of the identity, 3D vectors.

**BLOCK 3 — NEGATIVE PROMPT**

algebraic formula overlay, coordinate axis labels, complex number notation, inner product angle brackets in image, 3D arrows, text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, dual-headed arrows, hand-drawn styles, human figures, visual clutter, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion.

---

## Figure 3 — Resolution of the Identity: Projectors Tiling the Space

**Heuristic:** VG — Verification Gap
**Rank:** Important

---

**BLOCK 1 — ILLUSTRAE PASTE BLOCK**

Draw a single panel showing a 2D vector space with an orthonormal basis of two perpendicular unit arrows. A general state vector is shown as an arrow at an oblique angle from the origin. Two dashed perpendicular projection lines drop from the tip of the state vector onto each basis direction, landing at right-angle brackets, creating two component shadow arrows along the basis directions. Each shadow arrow is rendered as a filled arrow of a distinct color, and the two component arrows combine — shown by a parallelogram construction — to reconstruct the original state vector. A small enclosing rectangle or arc in the corner of the panel signals that the two projectors together cover the entire plane. Use flat vector rendering, uniform 1pt strokes, white background, and no baked text.

**BLOCK 2 — FULL SCOPE**

- `[S — SPECIFICATION]` Single-column 89mm width, 300 DPI, vector (SVG/EPS), white background. Single panel.
- `[C — CONTENT]` Two orthonormal basis vectors e1 and e2 from origin (right-angle marker between them). A general state vector psi from origin at oblique angle. Dashed projection lines from tip of psi perpendicular to e1 and e2, landing with right-angle brackets on each axis. Component arrows c1*e1 and c2*e2 along each axis. Parallelogram construction showing c1*e1 + c2*e2 = psi. A small shaded or outlined region in the corner indicating the plane is fully tiled by the two projectors. No more than 6 labeled visual elements total (basis arrows, state arrow, two component shadows, parallelogram).
- `[O — ORGANIZATION]` Single 2D diagram. Basis vectors along horizontal and vertical, state vector diagonal. Dashed lines for projections only. Parallelogram completion uses light gray outline. The "tiling" indicator is a subtle shaded square or arc in the interior of the angle between the two basis vectors.
- `[P — PRESENTATION]` Flat vector, Okabe-Ito. Basis arrows e1, e2: Sky Blue `#56B4E9`. State vector psi: Blue `#0072B2`. Component c1*e1: Bluish Green `#009E73`. Component c2*e2: Orange `#E69F00`. Projection dashes: light gray. Parallelogram outline: light gray. Tiling shading: very light gray fill, no border. Uniform 1pt strokes.
- `[E — EXCLUSIONS]` Omit: summation formula, Dirac notation angle brackets, Born rule, probability interpretation, continuous resolution of the identity, Dirac delta, infinite-dimensional notation.

**BLOCK 3 — NEGATIVE PROMPT**

summation formula overlay, Dirac notation symbols baked in, Born rule probability annotation, continuous basis or delta function symbols, text labels, words, gibberish letters, titles, captions, decorative borders, realistic textures, drop shadows, gradient backgrounds, photographic elements, dual-headed arrows, hand-drawn styles, human figures, visual clutter, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion.

---

## Video Candidate Pass

**Figure 1 — From Arrows to Abstract Spaces:** STATIC SUFFICIENT. The three panels form a spatial comparison, not a temporal process. The reader scans left-to-right at their own pace; no transition mechanism is the learning target.

**Figure 2 — Gram–Schmidt Orthonormalization:** VIDEO CANDIDATE. Criterion: ≥3 sequential causal stages, and the transformation mechanism (subtract projection, normalize, repeat) is the learning target. Watching the residual arrow shrink and the right-angle emerge from a non-perpendicular pair conveys the causal sequence better than three frozen frames. **Recommended as the single video for this module.**

**Figure 3 — Resolution of the Identity:** STATIC SUFFICIENT. The projection geometry is fully legible as a static parallelogram diagram. The concept (projectors tile the space) is spatial, not temporal.
