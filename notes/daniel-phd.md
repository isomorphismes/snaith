# Daniel Snaith — *Overconvergent Siegel Modular Symbols*

**Primary source:** Daniel Snaith, [*Overconvergent Siegel Modular Symbols*](https://www.ma.imperial.ac.uk/~buzzard/maths/research/notes/sp2n.pdf), PhD thesis, Imperial College London / University of London, **55-page publicly hosted PDF**. Thesis is often dated **about 2005** in secondary sources; **the cover of this PDF has no printed date**, so verify against university catalogues before a fixed formal citation.

**Advisor:** Kevin Buzzard, expressly thanked in the thesis acknowledgments (PDF p. 2). Buzzard's [notes on unpublished work](https://www.ma.imperial.ac.uk/~buzzard/maths/research/notes/index.html) provide retrospective context.

**Status of these notes:** direct first reading of introduction, contents, named propositions, differential-operator sections, theorem, and Weyl-group section. Not a line-by-line verification of every proof. Chapter and page references below use the **printed pages**, which are also the PDF page numbers (cover p. 1).

**One-sentence mathematical goal:** extend Chenevier's cohomological treatment of p-adic automorphic forms for GL_n-type groups to Siegel modular forms via GSp_{2n}, recover classical classes at sufficiently small U_p-slope, and for genus 2 construct theta-type operators indexed by Weyl-group symmetry.

## 1. What is actually proved, and what is motivation?

The **introduction (pp. 4–6)** states three aims:

1. Construct p-adic Banach representations containing finite-dimensional algebraic representations associated with Siegel modular forms; take cohomology of arithmetic groups to model overconvergent Siegel modular symbols.
2. Extend a suitable Hecke operator U_p to this cohomology, study compactness/slopes, and prove a classicality comparison below a weight-dependent slope bound.
3. In **genus 2** (n=2), construct analogues of Coleman's theta maps, compatible with Hecke actions up to explicit twists.

**Do not conflate the following:** A *proposed geometric theory* of overconvergent Siegel forms, a *cohomological model* built here, and a *Galois representation attached to an eigenform* are not the same claim. Chapter 3 treats Hodge–Tate weights and anticipated Galois representations **heuristically**. The eigenvariety construction mentioned in the introduction belongs to **Chenevier's preceding GL_n work**, not a theorem proved here for all Siegel forms.

## 2. Definitions and geometry (pp. 4–6)

Let K be a field and define
\[
J=\begin{pmatrix}0&-I_n\\I_n&0\end{pmatrix}.
\]
The symplectic similitude group is
\[
\operatorname{GSp}_{2n}(K)
=\{g\in\operatorname{GL}_{2n}(K):g^{\mathsf T}Jg=c(g)J,\ c(g)\in K^\times\}.
\]
The multiplier c(g) is a character. Its kernel is Sp_{2n}(K), the symplectic group.

A Siegel modular form of genus n lives over a Siegel upper-half-space domain of **symmetric complex n×n matrices with positive-definite imaginary part**; Sp_{2n} acts by fractional linear transformations. Genus 1 returns the familiar SL₂ setting. Genus 2 acts on 2×2 symmetric matrices, giving **complex dimension three**.

Classical scalar/vector-valued cusp forms of suitable weight map Hecke-equivariantly into degree
\[
d=\frac{n(n+1)}{2}
\]
arithmetic-group cohomology with algebraic coefficient module. The discussion on p. 6 writes a Hecke-equivariant inclusion with highest-weight module V_{t-(n+1)t_0}, where t₀=(1,…,1). Torsion in Γ is handled by passage to a finite-index torsion-free congruence subgroup and invariants.

**Important reasoning step:** For n=2, d=3. This is why the explicit theta maps in Chapter 3 act on **H³**. The degree is not chosen for a graphical interpretation.

## 3. Chapter 2 — constructing analytic coefficient spaces

### §2.1–2.3 (pp. 7–15): representation theory and weights

- Write down the affine coordinate algebra of GSp_{2n}: variables X_{ij} and a multiplier D satisfying \(X^{\mathsf T}JX=DJ\) and \(\det(X)=D^n\).
- Use a Borel subgroup consisting of a diagonal torus T and unipotent subgroup U, with left/right actions on coordinate functions.
- Identify highest-weight algebraic modules via U-invariants and torus weights. Coordinates built from appropriate minors are used.
- The genus-two explicit example supplies relations between coordinate functions; this is needed before differentiation can be shown to descend to the quotient algebra.

**Nontrivial distinction:** invariant functions in a coordinate ring, an irreducible highest-weight representation, and their p-adic completions are three different constructions.

### §2.4–2.6 (pp. 16–21): integrality, analytification, twists

- Replace finite polynomials by convergent p-adic power series on polydiscs, yielding nonarchimedean Banach spaces.
- Analyze integral lattices / unit balls and a Hecke semigroup Δ (extending the group action in controlled fashion).
- Construct analytic spaces N_t and their quotients S_t; classical subspaces B_t and F_t respectively carry finite-dimensional algebraic information.
- Record the importance of duals \(N_t^*,S_t^*\) for cohomology (they are not identical to N_t,S_t).

Schematic chain (notation follows the thesis; not every arrow is an equality):
\[
\text{algebraic highest-weight module}
\hookrightarrow
\text{p-adic analytic Banach module}
\;\longrightarrow\;
\text{dual module and a }\Gamma\text{-cohomology group}.
\]

### §2.7 (pp. 22–23): finiteness of the arithmetic subgroup

For Γ₀(p), a group of finite type \(FP_\infty\) supplies a free/projective resolution of the trivial module with each degree finitely generated. This makes the relevant continuous cochain spaces finite products of Banach modules in each degree and is used to put controlled Banach norms on cocycles/coboundaries/cohomology.

**Why it is not disposable:** a formal cohomology class does not carry the norm and complete-continuity structure needed for eigenvalue slopes without the functional-analytic argument.

## 4. The U_p operator and slope (Chapter 2 §§2.8–2.9, pp. 24–39)

The cohomological Hecke operator has the structure
\[
U_p=\operatorname{tr}\circ\Phi\circ\operatorname{res}.
\]
Here:
- **res** restricts cohomology along a finite-index subgroup;
- **Φ** implements conjugation/scaling by an appropriate diagonal element and action on the coefficient module;
- **tr** is transfer/corestriction back to Γ.

The chapter establishes norms and complete continuity, permitting a finite-slope theory on p-adic Banach cohomology. A slope h measures the p-adic valuations of the roots of an annihilating polynomial for U_p on an appropriate generalized eigenspace; for a simple eigenvector with U_p v=αv, h=v_p(α).

**Definition 2.9.1 (p. 37)** formalizes slope h and writes the corresponding summand as V^h. Take care with U_p=0: the slope of a zero eigenvalue is not a finite rational valuation.

### Proposition 2.9.2: small-slope classicality (p. 37)

**Precise *shape* of the claim:** Given a dominant algebraic weight t and a diagonal Hecke exponent vector α satisfying the preceding hypotheses, a computable bound λ(t,α) is defined. For rational h<λ, the slope-h parts of cohomology using infinite-dimensional analytic dual coefficient spaces agree with those of their finite-dimensional classical subspaces.

The proposition explicitly states isomorphisms of the form
\[
\bigl(H^k(\Gamma,(N_t^*)_0)\otimes_{\mathbb Z_p}\mathbb Q_p\bigr)^h
\;\simeq\; H^k(\Gamma,B_t^*)^h
\]
and
\[
\bigl(H^k(\Gamma,(S_t^*)_0)\otimes_{\mathbb Z_p}\mathbb Q_p\bigr)^h
\;\simeq\; H^k(\Gamma,F_t^*)^h.
\]

The explicit slope threshold in p. 37 is
\[
\lambda=
\sum_{j=1}^{n}t_j\left(\sum_{k=1}^{j}\alpha_{n-k+1}\right)
+
\min_{1\le i\le n}
(t_i+1)(\alpha_{n-i}-\alpha_{n-i+1}),
\qquad \alpha_0:=\alpha_{n+1}.
\]
**Notation warning:** This special convention for α₀ appears in the proposition. Do not substitute a usual α₀=0 rule.

**Proof architecture:**
1. Separate classical coefficients from nonclassical analytic directions using short exact sequences (e.g. B_t→N_t→Q_t and F_t→S_t→P_t, with corresponding dual exact sequences).
2. Show normalized U_p/p^λ preserves the unit ball on the nonclassical quotient's relevant cohomology; all its finite slopes are thus **≥λ**.
3. Restrict the long exact cohomology sequence to slope h<λ. The nonclassical quotient has no such slope part, leaving an isomorphism between overconvergent and classical parts.

The paper's precise finiteness/complete-continuity lemmas are needed for step 3. This is a **conditional and quantitative** theorem, not “every overconvergent form is classical.”

### A concrete slope toy calculation — *illustration, not from thesis*

Suppose U_p has an eigenvalue p²u with \(u\in\mathbb Z_p^\times\); then its slope is \(v_p(p²u)=2\). If the theorem's computed bound for the given weight and operator were λ=3, it would lie in the classical comparison range; if λ=2, the strict inequality h<λ would fail. Actual λ comes from Snaith's formula above and the chosen α, not from arbitrary choice.

## 5. Chapter 3 — genus-two theta maps (pp. 40–53)

The thesis fixes n=2 throughout. One classical modular-form starting point is Coleman's operator, often represented on q-expansions using \(q\,d/dq\), which raises or changes weights and twists Hecke eigenvalues. Daniel seeks analogues acting on the **cohomological Banach spaces** of genus-two Siegel forms.

### Motivation from Hodge–Tate weights (pp. 40–41)

A conjectural four-dimensional Galois representation associated with a classical genus-two eigenform of weight \([k_1,k_2]\) is discussed, with the expected Hodge–Tate multiset
\[
\{0,\;k_1-2,\;k_1+k_2-3,\;k_2-1\}.
\]
Twisting and reordering point toward a finite family of transformations of the weights. This **predicts** theta correspondences; it does **not** prove attached Galois representations exist in this generality.

The thesis emphasizes a convention switch: classical form weights \([k_1,k_2]\) and algebraic-module coordinates \(t=(k_2-k_1,k_1)\). Confusing these coordinate systems causes wrong theta exponents.

### §3.1 (pp. 42–43): explicit differential operators

Rather than leave the Weyl symmetries abstract, construct continuous differential operators \(\partial_1,\partial_2\) on the power-series coordinate algebra, check they **preserve its algebraic relations**, and derive twisted Δ-equivariance.

For instance the thesis defines \(\partial_1(y_{11})=1,\ \partial_1(y_{13})=-y_{24},\ \partial_1(y_{14})=y_{22},\ \partial_1(y_{2j})=0\). One must check the defining ideal is preserved before promoting a derivation from ambient variables to the quotient.

The operators \(\partial_i\) give maps between weights; suitable *powers/composites* \(\delta_i\) yield eight theta candidates. Their **twist factors** track the similitude multiplier c(g).

### §3.2 (pp. 44–49): subquotients and two chains

Finite-dimensional polynomial subspaces in selected coordinates sit inside analytic series spaces. Acting with \(\partial_i\) and taking kernels produces *proper chains* of Δ-invariant subspaces, not arbitrary equalities.

The thesis gives two composition sequences (p. 50):
\[
S_t\xrightarrow{\partial_1^{k_1+1}}S_{t_1}
\xrightarrow{\partial_2^{k_1+k_2+2}}S_{t_3}
\xrightarrow{\partial_1^{k_1+2k_2+3}}S_{t_5}
\xrightarrow{\partial_2^{k_2+1}}S_{t_7},
\]
and
\[
S_t\xrightarrow{\partial_2^{k_2+1}}S_{t_2}
\xrightarrow{\partial_1^{k_1+2k_2+3}}S_{t_4}
\xrightarrow{\partial_2^{k_1+k_2+2}}S_{t_6}.
\]

**Crucial limitation:** the maps are **not surjective** on the full analytic Banach spaces. The author gives an explicit p-adic series outside an image (p. 50). Thus these chains must *not* be interpreted as short exact sequences without additional statements.

### Theorem 3.3.1 (p. 51): cohomological maps

Eight maps (including identity) descend, by passing to duals and cohomology, to maps of Q_p-vector spaces
\[
\Theta_i:
H^3\bigl(\Gamma,(S_{t_i}^*)_0\bigr)\otimes_{\mathbb Z_p}\mathbb Q_p
\longrightarrow
H^3\bigl(\Gamma,(S_t^*)_0\bigr)\otimes_{\mathbb Z_p}\mathbb Q_p,
\quad 1\le i\le8.
\]
They satisfy the twisted action relation
\[
\Theta_i(g|_{t_i}f)=c(g)^{d_i}\;g|_t\,\Theta_i(f),\qquad g\in\Delta.
\]

**Pay attention to direction:** the underlying differential \(\delta_i:S_t\to S_{t_i}\) reverses direction on taking duals and passing to the cohomological theta map. Treating source/target as interchangeable loses a principal mathematical fact.

The eight *source* weights are given on p. 41. In the thesis's t=(k₁,k₂) **algebraic coordinate convention**:
\[
\begin{aligned}
t_1&=(-k_1-2,\ k_1+k_2+1),\\
t_2&=(k_1+2k_2+2,\ -k_2-2),\\
t_3&=(k_1+2k_2+2,\ -k_1-k_2-3),\\
t_4&=(-k_1-2k_2-4,\ k_1+k_2+1),\\
t_5&=(-k_1-2k_2-4,\ k_2),\\
t_6&=(k_1,\ -k_1-k_2-3),\\
t_7&=(-k_1-2,\ -k_2-2),\\
t_8&=(k_1,k_2).
\end{aligned}
\]
Twists, again following p. 41:
\[
d_1=d_8=0,\quad
d_2=d_4=-k_2-1,\quad
d_3=d_5=-k_1-k_2-2,\quad
d_6=d_7=-k_1-2k_2-3.
\]
These coordinates can be negative: overconvergent *weight modules* in this construction are not synonymous with classical dominant algebraic weights.

### §3.4 (pp. 51–53): Weyl group explanation

The root system of Sp₄ is type C₂; its Weyl group is **dihedral of order eight**, denoted \(D_8\) in the thesis. The positive roots for the chosen Borel are
\[
(2,0),\ (1,1),\ (0,2),\ (-1,1),
\]
with simple roots (2,0) and (-1,1).

In the usual two-coordinate picture the reflections generate signed permutations of (a,b), including
\[
(a,b)\mapsto (-a,b),\quad (a,b)\mapsto (b,a).
\]
The eight Weyl elements correspond to the eight theta constructions. The thesis lists explicit **4×4 group representatives** and the resulting **2-coordinate weight transformations**. The distinction matters: the 4×4 matrices act in the symplectic representation while the induced maps on weight space are two-dimensional.

Example in weight space:
\[
(a,b)\overset{s}{\mapsto}(-a,b)\overset{t}{\mapsto}(b,-a).
\]
Combining the two involutions gives an order-four rotation of the weight coordinates, explaining the eight-element dihedral structure.

## 6. Where the technical weight lies

- **Representation-theoretic:** integral coordinate rings and torus weights; explicit quotient relations for genus two.
- **Nonarchimedean analytic:** p-adic Tate algebras, Banach duals, unit balls, norms, complete continuity.
- **Homological:** finite-type Γ-resolutions; continuous group cohomology; restriction/transfer maps.
- **Arithmetic:** U_p-slopes; classicality inequality; determinant/similitude twists; predicted Hodge–Tate weights.
- **Coxeter-theoretic:** type C₂ roots, Weyl reflection data, compatibility of differential operators with representations.

It would be misleading to reduce the thesis to “eight pretty diagrams” before verifying the analytic and homological parts. The Weyl group is only its final, finite combinatorial layer.

## 7. Reproduce the mathematical arguments before attempting a visualization

1. For **n=1** verify GSp₂ = GL₂ and compare modular-symbol/Hecke conventions with classical GL₂ treatments.
2. For **n=2** explicitly check the six relations defining the GSp₄ coordinate ring and verify that ∂₁ and ∂₂ preserve the ideal (p. 42).
3. Implement/exhibit abstract matrices for the two Weyl generators on the **weight lattice**; verify \(s^2=t^2=(st)^4=1\) and exactly eight distinct elements.
4. Recompute the eight t_i from a base weight such as (k₁,k₂)=(1,1), including the d_i twists. Keep classical weight coordinates separate from algebraic coordinates.
5. Trace \(\delta_i:S_t\to S_{t_i}\), dualization, then \(\Theta_i:H^3(S_{t_i}^*)\to H^3(S_t^*)\) *without* reversing arrows accidentally.
6. Calculate a genuine λ(t,α) from the p. 37 bound for a legal example, then verify the normalized operator kills low-slope contributions of the nonclassical quotient.
7. Read the bibliography cited as [8] (Chenevier), [10] (Coleman), and the Ash–Stevens/Emerton material before judging novelty or long-term generalizations.

## 8. Proof-status and questions ledger

- **Proved in thesis:** analytic/cohomological construction; Banach and complete-continuity results; Proposition 2.9.2 classicality below explicit slope; genus-two theta operators and Theorem 3.3.1 with twists.
- **Heuristic/motivating:** attachment of Galois representations to arbitrary overconvergent Siegel Hecke eigenforms, and the Hodge–Tate argument anticipating the eight theta maps.
- **Not established by this thesis:** full geometric/eigenvariety theory for all Siegel modular forms or a general theorem for theta maps at all n.
- **Still to verify independently:** exact completion and density issues; assumptions on prime p and diagonal exponents; Hecke-operator compactness when passing through cohomology; how subsequent research treats this thesis (as Buzzard notes, its unpublished status matters); whether any operators agree with later BGG-type theta constructions under precise normalizations.
- **Editorial caution:** Some typeset/transcribed formulae in the thesis have slips; compare arguments with original PDF rather than silently correcting details.

## Sources and intellectual credit

- Daniel Snaith, [original thesis PDF](https://www.ma.imperial.ac.uk/~buzzard/maths/research/notes/sp2n.pdf).
- Kevin Buzzard, [unpublished research notes](https://www.ma.imperial.ac.uk/~buzzard/maths/research/notes/index.html), comments on Dan Snaith's thesis and on Chenevier's approach.
- J. F. Jardine (with research contributions by J. P. C. Greenlees and Sir Martin Taylor), [Victor Snaith obituary](https://doi.org/10.1112/blms.12802), for family/academic background.
- The thesis itself cites Gaëtan Chenevier, Robert Coleman, Avner Ash, Glenn Stevens, Matthew Emerton, and many others. For source-specific gratitude and full bibliographic names, **transcribe and verify the thesis's bibliography and its citations directly** rather than manufacturing a partial list.

No thesis pages, figures, or book scans are copied to this repository; these are independent mathematical notes with links to sources.
