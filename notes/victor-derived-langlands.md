# Victor Snaith — reading Derived Langlands through explicit examples

2026-10-09. Sources: Victor P. Snaith, [author-hosted November 2016 manuscript](https://victorsnaith.com/AdmobkWSci.pdf) of *Derived Langlands: Monomial Resolutions of Admissible Representations*. This is a **draft**, not a verified electronic copy of the 2018 printed edition. All chapter, section, and printed-page references below refer to that draft.

The definitions are from Chapter 1, §§1–5; the local-field double complex is from Chapter 2, §3, pp. 39–41. The examples and low-degree checks below are our calculations using those definitions. We have not read or verified all 352 PDF pages.

## 1. What a character identity forgets

Suppose a finite complex representation has an equality

\[
[V]=\sum_i n_i[\operatorname{Ind}_{H_i}^{G}\chi_i]
\quad\text{in }R(G),\qquad n_i\in\mathbb Z.
\]

Negative coefficients are permitted in this Grothendieck group. The equality does not specify vector spaces in each chain degree, differentials between them, their kernels, or maps associated with changing \(V\).

A bounded exact augmented complex supplies such an equality by its alternating sum. The converse is not a procedure for choosing all the missing data. Even specifying an exact complex of ordinary representations need not meet a stronger, separately defined notion of monomial resolution.

Snaith builds on **Robert Boltje's** monomial category. Objects retain a decomposition into rank-one lines permuted by the group. Morphisms retain more information than an arbitrary equivariant linear map. This additional structure is the first thing to understand before the word “derived.” [Draft, Chapter 1, §§1–2.]

## 2. Two different fixed-space constructions

Write a monomial object as

\[
M=\bigoplus_{i\in I}L_i.
\]

For a subgroup-character pair \((H,\chi)\), distinguish

\[
M^{(H,\chi)}=\{v:hv=\chi(h)v\text{ for every }h\in H\}
\]

from

\[
M^{((H,\chi))}
=\bigoplus_{\substack{i:\,H\text{ preserves }L_i\\H\text{ acts on }L_i\text{ by }\chi}}L_i.
\]

The second construction selects the **already specified lines**. The first may contain sums of vectors from lines that \(H\) permutes. In particular, the second space need not equal the first.

The book's morphisms preserve the double-parentheses spaces for every allowed pair. A monomial resolution additionally requires exactness after these tests, ending at the ordinary eigenspace of the target:

\[
\cdots\to M_1^{((H,\chi))}\to M_0^{((H,\chi))}
\to V^{(H,\chi)}\to0.
\]

In the fixed-central-character version, the allowed subgroups contain the centre and the characters restrict to the specified central character. Do not drop this condition when selecting examples. [Draft, Definition 2.3, printed p. 8.]

### A fully explicit S3 example

Take \(G=S_3\), \(k=\mathbb C\), and its permutation representation

\[
M=\mathbb C e_1\oplus\mathbb C e_2\oplus\mathbb C e_3,
\qquad \sigma e_i=e_{\sigma(i)}.
\]

The centre of \(S_3\) is trivial, so the example satisfies the central-character condition without forcing a scalar action of the whole group.

Its ordinary invariant space is

\[
M^{(G,1)}=\mathbb C(e_1+e_2+e_3).
\]

But none of the three specified coordinate lines is preserved by every permutation, so

\[
M^{((G,1))}=0.
\]

Now consider

\[
j:\mathbb C_{\mathrm{triv}}\to M,\qquad
j(1)=e_1+e_2+e_3.
\]

This is an injective equivariant linear map. It is **not** a morphism in the monomial category with the displayed line decompositions: the source's double-parentheses space is all of \(\mathbb C\), whereas the target's is zero.

Let \(V=M/\mathbb C(e_1+e_2+e_3)\), the two-dimensional standard representation. Then

\[
0\to\mathbb C_{\mathrm{triv}}\xrightarrow{j}M\to V\to0
\]

is exact as a complex of ordinary representations, and

\[
[V]=[\operatorname{Ind}_{S_2}^{S_3}1]-[1].
\]

Nevertheless, this particular complex is not a monomial resolution with those choices of lines. It already fails the morphism requirement. The example does not assert that \(V\) has no monomial resolution; it isolates why an ordinary exact sequence and a character identity are insufficient.

## 3. Why move to a functor category?

The monomial category is additive but is not an abelian category with all the kernels and cokernels one would like to use. For a representation \(V\), consider the contravariant functor

\[
I(V)(M)=\operatorname{Hom}_{kG}(\operatorname{underlying}(M),V).
\]

There is also a representable functor

\[
J(M)=\operatorname{Hom}_{\mathrm{mon}}(-,M).
\]

These two Hom symbols use **different categories**. Replacing one by the other erases precisely the restriction demonstrated in the \(S_3\) calculation.

Here is the basic projectivity argument, independently spelled out. Suppose \(F\to H\) is a pointwise-surjective natural transformation. By Yoneda, a map \(J(M)\to H\) corresponds to an element of \(H(M)\). Lift that element to \(F(M)\); Yoneda turns the lift into \(J(M)\to F\). Thus representable functors are projective in this functor setting. This is the elementary mechanism behind Chapter 1, Proposition 3.6—not a claim that every underlying induced representation is projective as a \(kG\)-module.

## 4. A bar differential really carries extra data

For a right \(A\)-module \(W\) and a left \(A\)-module \(N\), the first two bar groups are

\[
B_0=W\otimes_k N,\quad
B_1=W\otimes_k A\otimes_k N,\quad
B_2=W\otimes_k A\otimes_k A\otimes_k N.
\]

The differentials are

\[
d_1(w\otimes a\otimes n)=wa\otimes n-w\otimes an,
\]

\[
d_2(w\otimes a\otimes b\otimes n)
=wa\otimes b\otimes n-w\otimes ab\otimes n+w\otimes a\otimes bn.
\]

Applying \(d_1\) to the latter gives six terms. They cancel in pairs because \((wa)b=w(ab)\) and \(a(bn)=(ab)n\). This proves \(d_1d_2=0\) in degree two without concealing the sign or module-action conventions.

A bar construction has this associativity built into all degrees. For the usual augmented case \(N=A\), inserting a unit gives a contracting homotopy on the underlying \(k\)-complex. **Exactness** and **freeness over \(A\)** are separate assertions: calling every term free needs the appropriate freeness hypotheses on the coefficient \(k\)-modules. Working over a field avoids one source of trouble, but does not justify deleting assumptions from the ring-valued version.

The draft applies this machinery to endomorphisms of a sum of monomial objects and to the associated functors. One must retain which endomorphism ring, left/right convention, and line decomposition were chosen. [Chapter 1, §§4–5, printed pp. 15–23.]

## 5. Local-field geometry contributes a second degree

For the \(\operatorname{GL}_2(K)\) lattice-tree example, take a discrete valuation ring \(\mathcal O\), uniformizer \(\pi\), and residue field \(\mathbb F_q\). A vertex is a homothety class of lattices in \(K^2\). Neighbors of the standard class can be represented by

\[
\pi L\subsetneq L'\subsetneq L,\qquad
L'/\pi L\text{ a one-dimensional subspace of }L/\pi L.
\]

Since \(L/\pi L\cong\mathbb F_q^2\), the choices are \(\mathbb P^1(\mathbb F_q)\): exactly \(q+1\) neighbors. This is also the concrete correspondence used in the draft, Chapter 2, §4, printed p. 43.

For \(q=2\), three representatives are

\[
\mathcal O e_1+\pi\mathcal O e_2,\quad
\pi\mathcal O e_1+\mathcal O e_2,\quad
\mathcal O(e_1+e_2)+\pi\mathcal O e_2.
\]

The standard vertex stabilizer in \(\operatorname{GL}_2(K)\) is \(K^\times\operatorname{GL}_2(\mathcal O)\), compact modulo the scalar centre. Passing to a subdivision handles inversions of simplices when defining the coefficient complex; pointwise and setwise edge stabilizers must not be confused.

A local monomial resolution is placed over each simplex. The resulting complex has a **bar degree** and a **simplex degree**. If \(d_{\mathrm{bar}}\) lowers bar degree and \(d_{\mathrm{geom}}\) lowers simplex degree, and the incidence maps are chain maps, then on simplex degree \(s\) use

\[
d_{\mathrm{tot}}=d_{\mathrm{geom}}+(-1)^s d_{\mathrm{bar}}.
\]

Indeed,

\[
d_{\mathrm{tot}}^2
=d_{\mathrm{geom}}^2+d_{\mathrm{bar}}^2
+(-1)^s d_{\mathrm{geom}}d_{\mathrm{bar}}
+(-1)^{s-1}d_{\mathrm{bar}}d_{\mathrm{geom}}=0.
\]

The mixed terms cancel because the incidence maps commute with the local differential. Without the sign, they add instead. Nor does an attractive lattice tree alone specify the subgroup maps, local resolutions, or this compatibility.

## 6. Status and reading limits

The draft's preface credits **Robert Boltje** for the finite monomial framework and **Ian Leary** for the proper-action-space insight behind the building construction. Chapter 2 constructs the double complex; Chapter 4 addresses its resolution property for \(\operatorname{GL}_n\). These are distinct from a proof of the full Langlands program.

Chapter 5, Conjecture 2.4, concerning the Deligne-representation construction, is explicitly left conjectural. Chapter 6 presents proposed routes toward arithmetic invariants; Chapter 8 investigates functorial descent. We have not independently verified the general exactness argument, compared theorem numbers against the printed edition, or established the conjectural extensions.

**Next precise mathematical task:** reconstruct the augmentation and the subgroup-character exactness tests for one complete finite example, then trace the same tests through the local double complex. The \(S_3\) example above diagnoses what must be preserved; it is not that finished reconstruction.

Credit and thanks to **Victor P. Snaith**, **Robert Boltje**, and **Ian Leary**. The building background also credits **François Bruhat**, **Jacques Tits**, and **Jean-Pierre Serre**. This is not a completed transcription of the entire book's bibliography.
