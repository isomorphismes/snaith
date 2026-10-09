# Victor Snaith — Bott localization, cobordism, and the category change

2026-10-09. Companion to [the book inventory](victor-books.md).

## Source boundary

The full 1979 memoir *Algebraic Cobordism and K-Theory* was **not successfully retrieved in this pass**. The Rochester PDF link in the first-pass inventory has not been verified. Its [AMS catalogue](https://bookstore.ams.org/memo-21-221) confirms the volume and four-part contents, not a completed reading of its proofs.

This note instead uses two accessible mathematical expositions, clearly distinguished from that memoir:

- **David Gepner and Victor Snaith**, [*On the motivic spectra representing algebraic cobordism and algebraic K-theory*](https://victorsnaith.com/acakArxiv.pdf), the author-hosted arXiv:0712.2817 **v1, 17 December 2007**, particularly §§1–2. Later publication is a separate version.
- **Akhil Mathew**, [*Snaith's Construction of Complex K-Theory*](https://math.uchicago.edu/~amathew/snaith.pdf), 11 June 2012, an exposition of an argument attributed to **Michael Hopkins**.

The calculations below explain the constructions; they are not a reconstruction of the unavailable memoir's proof.

## 1. Inverting a class changes the spectrum

Let \(R\) be a commutative ring spectrum and \(\beta\in\pi_2R\). Multiplication by \(\beta\), desuspended, gives a map

\[
R\longrightarrow\Sigma^{-2}R.
\]

Iterating it produces the homotopy telescope

\[
R[\beta^{-1}]
=\operatorname*{hocolim}
\bigl(R\to\Sigma^{-2}R\to\Sigma^{-4}R\to\cdots\bigr).
\]

On homotopy groups this has the expected graded-localization calculation:

\[
\pi_kR[\beta^{-1}]
\cong\operatorname*{colim}_{r\ge0}\pi_{k+2r}R.
\]

The transition map is multiplication by \(\beta\). An element represented by \(a\in\pi_{k+2r}R\) can be thought of as \(a/\beta^r\), of total degree \(k\). This bookkeeping immediately explains why localization can create negative-degree classes from an initially connective spectrum.

In particular, \(\Sigma^\infty_+\mathbb{CP}^{\infty}\) cannot be identified with periodic complex K-theory before this operation. The first is connective; periodic K-theory has nonzero negative even homotopy groups. No choice of a nice space-level picture repairs that mismatch.

## 2. State the two topological comparisons separately

The relevant comparisons are

\[
\bigl(\Sigma^\infty_+\mathbb{CP}^{\infty}\bigr)[\beta^{-1}]
\simeq KU
\]

and

\[
\bigl(\Sigma^\infty_+BU\bigr)[\beta^{-1}]
\simeq PMU,
\qquad
PMU=\bigvee_{j\in\mathbb Z}\Sigma^{2j}MU.
\]

Here \(PMU\) is **periodic** complex cobordism, not connective \(MU\). Gepner–Snaith discuss these earlier comparisons in their introduction; Mathew explains the first comparison.

The two multiplications are not interchangeable. On \(\mathbb{CP}^{\infty}\simeq BU(1)\), use tensor product of line bundles. On stable \(BU\), use direct sum of bundles. A proof has to identify the relevant multiplication and Bott class, not merely recognize familiar underlying spaces.

The displayed equivalences alone also do not automatically specify every possible higher-coherence enhancement. Record whether a source works with underlying spectra, ring objects in the homotopy category, or coherently commutative ring spectra before strengthening its statement.

## 3. Derive the multiplicative formal group law

Here is a direct calculation in periodic K-theory. Choose the convention

\[
x(L)=\beta^{-1}([L]-1)
\]

for a line bundle \(L\), where \(\beta\) has cohomological degree \(-2\). Then \([L]=1+\beta x(L)\). Since \([L\otimes M]=[L][M]\), expansion gives

\[
\begin{aligned}
1+\beta x(L\otimes M)
&=(1+\beta x(L))(1+\beta x(M)),\\
x(L\otimes M)
&=x(L)+x(M)+\beta x(L)x(M).
\end{aligned}
\]

Thus the formal group law in this coordinate is

\[
F(x,y)=x+y+\beta xy.
\]

Its inverse is

\[
\iota(x)=\frac{-x}{1+\beta x}
=-x+\beta x^2-\beta^2x^3+\cdots.
\]

Indeed \(F(x,\iota(x))=0\) by substitution. Tensoring a line bundle with itself \(r\) times yields

\[
[r]_F(x)=\frac{(1+\beta x)^r-1}{\beta}.
\]

For example,

\[
[2]_F(x)=2x+\beta x^2,
\qquad
[3]_F(x)=3x+3\beta x^2+\beta^2x^3.
\]

Choosing \(\beta^{-1}(1-[L])\) instead changes the cross-term sign. This is a coordinate convention, not a disagreement about tensor product.

The calculation explains what algebra the universal line bundle imposes on an orientation. It is **not by itself a proof of the spectrum equivalence**: existence of a map and agreement of this formal group law do not rule out additional homotopy groups. Mathew's exposition supplies further homotopical arguments rather than making that shortcut.

## 4. Motivic analogues require a different ambient category

Using the now-common motivic convention \(S^{2,1}\simeq\mathbb P^1\), write the comparisons as

\[
\bigl(\Sigma^\infty_+BGL\bigr)[\beta^{-1}]
\simeq PMGL
=\bigvee_{j\in\mathbb Z}\Sigma^{2j,j}MGL,
\]

\[
\bigl(\Sigma^\infty_+\mathbb P^\infty\bigr)[\beta^{-1}]
\simeq KGL.
\]

The 2007 draft uses a different bidegree convention: its two indices separately count simplicial-circle and multiplicative-group factors. Its \((1,1)\) Bott degree corresponds to \((2,1)\) above. Never combine a formula from one convention with suspension arithmetic from the other.

Gepner–Snaith work over a Noetherian base of finite Krull dimension and distinguish homotopy K-theory from ordinary algebraic K-theory on singular inputs. For example, a claim about an \(\mathbb A^1\)-invariant spectrum must not silently become a claim that arbitrary Quillen K-theory is \(\mathbb A^1\)-invariant for singular schemes. Regularity hypotheses matter.

An informative warning in their introduction is that the earlier attempt to use algebraic K-theory spaces in the **ordinary** stable category produced an oversized cobordism construction. The motivic result changes the ambient homotopy theory; it is not obtained merely by renaming \(BU\) as \(BGL\).

## 5. A precise reading test for the 1979 memoir

When the original becomes available, each claimed theorem should answer these questions:

1. What is the input space or spectrum, and which product is being used?
2. What class is inverted, and in what degree?
3. Is the result connective cobordism or its periodization?
4. Is the assertion a stable splitting, an equivalence of spectra, or a multiplicative refinement?
5. Does “algebraic” refer to a construction in ordinary stable homotopy or to a later motivic category?

These questions are now motivated by explicit algebra, not just keywords. They remain a reading checklist, not evidence that the original book has already been checked.

**Credit and thanks:** Victor P. Snaith; David Gepner; Akhil Mathew; Michael Hopkins. The Gepner–Snaith draft also acknowledges J. F. Jardine, Sarah Whitehouse, and John Greenlees. No source PDF has been copied into this repository.
