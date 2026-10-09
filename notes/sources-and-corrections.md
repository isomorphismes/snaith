# Source access, corrections, and intellectual credit

Second-pass ledger, 2026-10-09. **This file qualifies and, where necessary, supersedes the first-pass notes.** Earlier notes remain in place so that the reading history is visible; their unfinished checklists are not claims that the work below remains undone.

## What this continuation actually read

| Work | Source examined | Reading status |
| --- | --- | --- |
| Daniel Snaith's thesis | [Imperial-hosted 55-page PDF](https://www.ma.imperial.ac.uk/~buzzard/maths/research/notes/sp2n.pdf) | Definitions, normalized coordinates, slope proposition, theta constructions, Weyl section, and complete numbered bibliography; not a full independent proof audit |
| Victor Snaith, Derived Langlands | [November 2016 author manuscript](https://victorsnaith.com/AdmobkWSci.pdf) | Preface and contents, Chapter 1 definitions and bar construction, selected local double-complex and lattice passages; not a complete reading or a comparison with the 2018 edition |
| Victor Snaith, 1979 cobordism memoir | [AMS catalogue](https://bookstore.ams.org/memo-21-221) | Bibliographic/contents evidence only in this pass; no successful full-text retrieval |
| Gepner–Snaith, motivic cobordism and K-theory | [Author-hosted 2007 v1](https://victorsnaith.com/acakArxiv.pdf) | Introduction and preliminary constructions; version distinguished from the later publication |
| Mathew, Snaith's Construction of Complex K-Theory | [2012 exposition](https://math.uchicago.edu/~amathew/snaith.pdf) | Short mathematical exposition examined; not Victor's original proof |
| Lin–Wang–Xu, Last Kervaire Invariant Problem | [arXiv:2412.10879v2](https://arxiv.org/abs/2412.10879v2) | Abstract and version metadata checked for the historical update; proof not audited |

The coordinate formulas and eight weight transforms in [Daniel's calculation note](daniel-calculations.md) have additional exact algebra checks. That does not upgrade every proposition in the thesis to independently verified status.

## Corrections and qualifications

### 1. The 1979 memoir's supposed open PDF

The first-pass book inventory labeled a Rochester URL a freely accessible copy. That access claim was not established by this continuation: retrieval failed, and the full text was not examined. Do not cite [our localization note](victor-cobordism-localization.md) as a close reading of the 1979 memoir. It explicitly uses later, identified sources instead.

### 2. The weight transformations are shifted

The eight genus-two weights should be calculated by the Weyl **dot action**, with \(\rho=[1,2]\) in torus-exponent coordinates or \((1,1)\) in the thesis's module coordinates. Their affine constants are essential. The finite Weyl action on weights is not an action by eight invertible operators on one cohomology group.

### 3. Multiplier is not determinant

For \(\operatorname{GSp}_4\), \(\det(g)=c(g)^2\). The explicit coefficient and theta identities use the appropriate powers of the similitude multiplier. Loose use of “determinant twist” in motivational prose must not replace the formula in Theorem 3.3.1. The example \(\operatorname{diag}(p,1,p^2,p^3)\) makes the factor-of-two discrepancy explicit.

### 4. Some proof claims need more careful labels

A Banach-linear complement is not automatically equivariant and does not automatically descend to group cohomology. Exactness after taking finite slopes requires justification beyond a vector-space splitting. Also, the equality of the two longest-word differential composites on thesis p. 47 is asserted with computational details omitted. The first pass's broad “proved in thesis” label should not be read as our independent verification of every supporting step.

### 5. Coordinate rings and derivative images

The normalized invariant \(y\)-relations are not the original matrix \(X\)-relations defining \(\operatorname{GSp}_4\). The calculation note treats the correct quotient. It also derives the sign required in the second coordinate chart without silently trusting a questionable extracted line on p. 49. For higher derivatives the image condition contains a product of consecutive integers, not just the first-derivative denominator.

### 6. Update the Arf–Kervaire reading chronology

The old book note correctly dates Victor's monograph to 2009 and HHR's published result to 2016, but its unchecked dimension-126 caveat is not an adequate current account.

**Weinan Lin, Guozhen Wang, and Zhouli Xu**, *On the Last Kervaire Invariant Problem*, arXiv:2412.10879, first submitted **14 December 2024**, revised **22 February 2025**, prove in that paper that \(h_6^2\) survives the Adams spectral sequence and obtain framed Kervaire-invariant-one manifolds in dimension 126. Their stated combined classification is dimensions **2, 6, 14, 30, 62, 126**. [Primary record, v2](https://arxiv.org/abs/2412.10879v2).

Our verification here concerns what that paper states and its version record, not an independent verification of its 66-page proof or a claim about journal acceptance. The next historical comparison must therefore be **Snaith 2009 → Hill–Hopkins–Ravenel → Lin–Wang–Xu**, rather than stopping in 2016.

## Daniel's numbered bibliography

The twenty items below have been checked against the thesis's bibliography on printed pp. 54–55. Names are given individually, retaining initials where expansion has not been independently checked. This is a record of what Daniel cites, not a claim that every cited source was read in this pass. It is also not a wholesale endorsement of the dates and pagination printed in that bibliography.

| Thesis item | Author or authors | Identifying work |
| --- | --- | --- |
| 1 | A. N. Andrianov | Quadratic Forms and Hecke Operators |
| 2 | Avner Ash; Glenn Stevens | p-adic Deformations of Cohomology Classes of Subgroups of GL(N, Z): The Non-Ordinary Case |
| 3 | Armand Borel; Jean-Pierre Serre | Corners and arithmetic groups |
| 4 | Siegfried Bosch; Ulrich Güntzer; Reinhold Remmert | Non-Archimedean Analysis |
| 5 | Kenneth S. Brown | Cohomology of Groups |
| 6 | Karsten Buecker | Congruences between Siegel modular forms on the level of group cohomology |
| 7 | Kevin Buzzard | On p-adic families of automorphic forms |
| 8 | Gaëtan Chenevier | Familles p-adiques de formes automorphes pour GLn |
| 9 | Robert Coleman | p-adic Banach spaces and families of modular forms |
| 10 | Robert Coleman | Classical and overconvergent modular forms |
| 11 | Gerd Faltings | On the Cohomology of Locally Symmetric Hermitian Spaces |
| 12 | William Fulton; Joe Harris | Representation Theory: A First Course |
| 13 | Roe Goodman; Nolan R. Wallach | Representations and Invariants of the Classical Groups |
| 14 | James E. Humphreys | Linear Algebraic Groups |
| 15 | R. L. Lipsman | Fourier Inversion on Borel Subgroups of Chevalley Groups: The Symplectic Group Case |
| 16 | Jean-Pierre Serre | Endomorphismes complètement continus des espaces de Banach p-adiques |
| 17 | Jean-Pierre Serre | Arithmetic Groups |
| 18 | Goro Shimura | Introduction to the Arithmetic Theory of Automorphic Functions |
| 19 | Glenn Stevens | Overconvergent Modular Symbols |
| 20 | Richard Taylor | On Congruences Between Modular Forms, PhD thesis |

For item 6, the [journal archive](https://www.numdam.org/articles/10.5802/aif.1533/) independently confirms **Karsten Buecker**, the correct title, and *Annales de l'Institut Fourier* 46 (1996), no. 4, 877–897. The misspelling of “Congruences” in the thesis bibliography is not propagated here. Other edition/date discrepancies should be checked against their own publisher or journal records before a final machine-readable bibliography is produced.

**Thank you to each of these authors:** A. N. Andrianov, Avner Ash, Glenn Stevens, Armand Borel, Jean-Pierre Serre, Siegfried Bosch, Ulrich Güntzer, Reinhold Remmert, Kenneth S. Brown, Karsten Buecker, Kevin Buzzard, Gaëtan Chenevier, Robert Coleman, Gerd Faltings, William Fulton, Joe Harris, Roe Goodman, Nolan R. Wallach, James E. Humphreys, R. L. Lipsman, Goro Shimura, and Richard Taylor.

Thank you also to **Daniel Snaith** for the thesis. **Matthew Emerton** is explicitly mentioned in its introduction; Kevin Buzzard's [research-notes page](https://www.ma.imperial.ac.uk/~buzzard/maths/research/notes/index.html) also identifies related work of **Jacques Tilouine and collaborators**. This is attribution of that connection, not an invented list of those collaborators or an assertion that the thesis proves results belonging to them.

For Victor's books, the complete per-book bibliography acknowledgement work remains unfinished. Coauthors, editors, prior authors, supervisors, and people thanked in a preface have different roles; none should be silently relabeled as a coauthor. No private addresses or inferred personal attributes are included.
