# Snaith — research reading order and mathematical questions

**No visual design yet.** This file organizes the mathematics we need to understand or verify before selecting any visual representation. It is a reading map, not a feature list.

Companion notes: [Victor's books](victor-books.md) · [edited collections and manuscripts](victor-edited-and-other.md) · [Daniel's thesis](daniel-phd.md).

## A. Three structural lines in Victor's work

### A1. Stable splittings, Bott inversion and spectra

- Begin with Victor's 1974 “A stable decomposition of ΩⁿSⁿX” (listed as #12 in [Jardine's bibliography](https://doi.org/10.1112/blms.12802)).
- Read his contribution to *Topics in K-Theory* (1975), the 1979 *Algebraic Cobordism and K-Theory*, and the 1983 *Algebraic K-Theory and Localised Stable Homotopy Theory*.
- Questions: which stable natural equivalences are actual maps of spectra? Which powers/classes become invertible, and in what category? How does the familiar James-type splitting lead to the Snaith stable splitting? What is the difference between an equivalence of underlying spectra and an equivalence of structured ring spectra?

Basic identity to place carefully (schematic, with correct suspension/localization conventions to verify from the papers):
\[
KU\simeq \Sigma^\infty_+\mathbb{CP}^{\infty}[\beta^{-1}].
\]
Depending on model, CP∞_+ and \(\Sigma^\infty\mathbb{CP}^\infty\) conventions and Bott grading differ. **Do not use this as an unchecked implementation axiom.**

### A2. From topology to arithmetic

- From *Topological Methods in Galois Representation Theory* → *Explicit Brauer Induction* → *Galois Module Structure* → *Algebraic K-Groups as Galois Modules* → *The Second Chinburg Conjecture for Quaternion Fields*.
- Questions: Which characteristic class of an orthogonal Galois representation is compared with the class of a symmetric form? How does integral failure of a normal basis become a class in a group-ring class group? How is a symplectic root number converted into a class-group obstruction? Which operations respect induction, restriction and transfer?

A finite arithmetic example should be computed **both** over Q[G] and over Z[G], to see why integral structure carries information the rational representation misses.

### A3. Finite Brauer induction → derived monomial resolution

- Work through the representation-ring theorem in *Explicit Brauer Induction* and identify its **virtual** minus signs.
- Read the finite-mod-centre chapter of *Derived Langlands*, then the GL₂ local-field chapter.
- Question: can a virtual character identity be refined to a functorial chain complex in a suitable category, with admissibility and derived invariants preserved? Which components are theorems, which constructions, and which programmatic expectations?
- Read Robert Boltje's monomial-resolution work alongside the book; this relation is acknowledged in the obituary and must not be credited solely to Victor.

## B. Daniel's thesis — proof reconstruction order

Before thinking about diagrams, check seven exact mathematical relationships:

1. **Symplectic relation:** \(g^{\mathsf T}Jg=c(g)J\) and the multiplier character, for 2×2 and 4×4 examples.
2. **Weight indexing:** compare torus weights, highest weights and classical Siegel modular-form weights (there is a nontrivial reindexing).
3. **Inclusion/quotient:** identify the embedding of classical finite-dimensional modules inside p-adic analytic Banach modules; specify the dual arrows.
4. **Cochain definition:** build a degree-k group-cohomology complex using a finite-type Γ-resolution; separate cocycles, coboundaries and the Hausdorff/Banach completion issues.
5. **Hecke:** derive \(U_p=\operatorname{tr}\circ\Phi\circ\operatorname{res}\) and the fact that the maps land in the correct cohomology groups; record a specific diagonal element and α.
6. **Classicality:** calculate the actual bound λ(t,α), show that nonclassical quotient classes have slopes at least λ, and check the strict inequality \(h<λ\).
7. **Theta:** explicitly verify the defining quotient ideal is preserved by ∂₁,∂₂; check weights t_i and twists d_i, then verify dual arrows yield \(\Theta_i\) on H³.

The result *not* to silently assume: that the constructed analytic/cohomological symbols are geometrically the same as all subsequent notions of overconvergent Siegel eigenforms.

## C. What the two generations actually share — and do not

**Shared mathematical language:** representation rings, torus weights, arithmetic group actions, induced/equivariant constructions, and topology/cohomology as a means of extracting invariants from representation theory.

**Different immediate mechanisms:**
- Victor's books include **stable homotopy theory**, **Bott localization**, **Galois module obstructions**, **Brauer induction**, **arithmetic K-theory**, and **derived admissible representation resolutions**.
- Daniel's thesis deals with **p-adic analytic representation spaces**, **group cohomology**, **compact Hecke operators and slopes**, and **explicit genus-two theta operators**.

No evidence yet establishes a mathematical theorem directly connecting Victor's *Derived Langlands* monomial resolutions to Daniel's specific genus-two theta maps. This would be a **research question**, not a pre-existing connection to advertise.

## D. Preliminary source-to-proof queue

| Priority | Primary source to retrieve/read | Concrete output |
| --- | --- | --- |
| First | Daniel's thesis §§2.8–2.9, 3.1–3.4 | Verify proposition 2.9.2 and theorem 3.3.1 with normalizations |
| First | Victor's *Algebraic Cobordism and K-Theory* (open PDF) | Write each main theorem with its conditions and map |
| Next | *Topics in K-Theory* and mathematical corrections | Dyer–Lashof operation identities and limitations |
| Next | *Explicit Brauer Induction*, ch. 2–3 | Concrete Brauer decomposition for small groups |
| Next | *Galois Module Structure* and Chinburg memoir | Exact class-group comparison and quaternionic case |
| Next | *Algebraic K-Groups as Galois Modules*, ch. 2, 5, 7 | Higher K module classes and annihilators |
| Next | *Stable Homotopy Around the Arf-Kervaire Invariant* | 2009 claims vs 2016 HHR results |
| Next | *Derived Langlands*, ch. 1–2, 4 | Explicit monomial resolution differential and proof of exactness |
| Pending source | *An Introduction to Global Analysis* | Genuine table of contents, then mathematical notes |
| Pending copy | *The Yukiad* | Reading notes on its actual narrative, without inventing plot |

## E. Source provenance

For a complete book note, record the exact edition, author/coauthor/editor roles, chapter/printed page, proposition number, definitions and proof assumptions, citations to predecessors, and whether the source is a book, memoir, article, preprint, or unpublished manuscript. Treat a title-list summary as **not yet a close reading**.

Foundational bibliography: **J. F. Jardine**, [Victor Percy Snaith, 1944–2021](https://doi.org/10.1112/blms.12802), with substantive historical research commentary by **J. P. C. Greenlees** and **Sir Martin Taylor**. Other original sources are linked within each note.
