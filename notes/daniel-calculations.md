# Daniel Snaith — calculations behind the thesis

Second reading, 2026-10-09. Companion to [the first-pass overview](daniel-phd.md). [Source and correction ledger](sources-and-corrections.md).

**Source:** Daniel Snaith, [*Overconvergent Siegel Modular Symbols*](https://www.ma.imperial.ac.uk/~buzzard/maths/research/notes/sp2n.pdf). References below use printed page numbers, 1–55. The main inputs are the normalized relations on pp. 42–43, the weight conventions on pp. 13 and 41, and Proposition 2.9.2 on p. 37. The calculations below reconstruct consequences of those inputs; they do not certify the thesis's functional-analytic proofs.

## 1. Eliminate the redundant coordinates

Use four independent coordinates

\[
x=y_{11},\qquad a=y_{22},\qquad b=y_{23},\qquad c=y_{24}.
\]

The normalization has already set \(y_{12}=y_{21}=1\). Set

\[
y_{13}=a-xc,\qquad y_{14}=b+xa,\qquad
 y_{25}=-a,\qquad y_{26}=-bc-a^2.
\]

Substitute these expressions into the six relations:

\[
\begin{aligned}
y_{22}+y_{25}&=0,\\
y_{14}-y_{23}-y_{11}y_{22}&=0,\\
y_{26}+y_{13}y_{22}+y_{14}y_{24}&=0,\\
y_{11}y_{24}-y_{22}+y_{13}&=0,\\
y_{11}y_{26}-y_{13}y_{23}+y_{14}y_{22}&=0,\\
y_{26}+y_{23}y_{24}+y_{22}^{2}&=0.
\end{aligned}
\]

Every left-hand side becomes the zero polynomial. Conversely, four of the relations solve uniquely for the four eliminated variables. The two remaining relations then follow automatically. Thus the normalized analytic coefficient algebra has the explicit presentation

\[
A_F\cong\mathbb Q_p\langle x,a,b,c\rangle.
\]

Here angle brackets mean **restricted power series**: coefficients tend to zero in the \(p\)-adic norm. Polynomial substitutions with integral coefficients in both directions give bounded homomorphisms for the Gauss norms, so this is more than a bijection of sets of formal expressions.

This calculation concerns the normalized invariant-coordinate algebra. It does **not** identify the whole matrix group \(\operatorname{GSp}_4\) with four-dimensional affine space. It also does not identify this four-coordinate \(p\)-adic algebra with genus-two Siegel upper half-space, whose symmetric complex matrices have three independent entries.

### A sign check for the alternative chart

Take \(r=y_{13}\), \(s=y_{14}\), retaining \(x,c\). Then

\[
a=r+xc,\qquad b=s-xr-x^2c.
\]

Consequently

\[
y_{26}=-bc-a^2=-sc-r^2-xrc.
\]

The signs are forced by the original relations. For example, \(x=s=c=0,r=1\) gives \(a=1\) and \(y_{26}=-1\). A positive expression \(sc+r^2+xrc\) would make \(y_{26}+bc+a^2=2\), not zero over any \(\mathbb Q_p\). The text extraction of the second chart on p. 49 contains that positive expression; visual confirmation of that particular printed line remains pending. Our calculation establishes the required formula without relying on that extraction.

## 2. The two differential operators become elementary

In these coordinates the operators are

\[
D_1=\frac{\partial}{\partial x},\qquad
D_2=\frac{\partial}{\partial c}
+x\frac{\partial}{\partial a}
-x^2\frac{\partial}{\partial b}.
\]

For instance,

\[
D_1(y_{13})=-c,\quad D_1(y_{14})=a,\quad
D_2(a)=x,\quad D_2(b)=-x^2,\quad D_2(c)=1.
\]

A useful nontrivial consistency check is

\[
D_2(y_{26})=D_2(-bc-a^2)=x^2c-b-2xa
=-y_{14}-xy_{13}.
\]

Thus the action on the eliminated variable agrees with the action required by the presentation. This is how to check descent to the quotient, rather than merely defining derivatives on unrelated ambient variables.

For a monomial, the operations can be written without any implicit differentiation:

\[
D_1(x^i a^j b^k c^\ell)
=i x^{i-1}a^j b^k c^\ell,
\]

\[
\begin{aligned}
D_2(x^i a^j b^k c^\ell)
={}&\ell x^i a^j b^k c^{\ell-1}\\
&+j x^{i+1}a^{j-1}b^k c^\ell\\
&-k x^{i+2}a^j b^{k-1}c^\ell.
\end{aligned}
\]

Terms with zero coefficients are omitted. Since integers have \(p\)-adic norm at most one, these operations are bounded on the Tate algebra and preserve its integral unit ball.

## 3. The root directions do not commute

Define \([D,E]=D\circ E-E\circ D\). Direct calculation gives

\[
[D_1,D_2]=\partial_a-2x\partial_b,
\]

\[
[D_1,[D_1,D_2]]=-2\partial_b,
\]

\[
[D_1,[D_1,[D_1,D_2]]]=0,
\qquad [D_2,[D_2,D_1]]=0.
\]

For example, \([D_1,D_2](a)=1\), whereas two commuting operators would give zero. These calculations expose the two simple directions and their two additional bracket directions. They also explain why replacing all compositions by commuting partial derivatives would lose essential information.

All of this takes place over \(\mathbb Q_p\), including when \(p=2\). The coefficient \(-2\) is then nonzero; reducing the formulas modulo 2 changes the algebra and is a different question.

## 4. A shifted Weyl action explains the eight weights

Keep the **module weight** \(t=(m,n)\) separate from the four coordinates above. Its torus-exponent coordinates are

\[
P(m,n)=[n,m+n].
\]

For the positive roots \([2,0],[-1,1],[1,1],[0,2]\), half their sum is

\[
\rho_{\mathrm{torus}}=[1,2]=P(1,1).
\]

Hence \(\rho=(1,1)\) in module coordinates. The relevant action is

\[
w\mathbin{\cdot}t=P^{-1}\bigl(w(P(t)+[1,2])-[1,2]\bigr),
\]

not the unshifted linear action. Let \(r_1\) swap the two torus coordinates and \(r_2\) negate the first. Then

\[
r_1\mathbin{\cdot}(m,n)=(-m-2,m+n+1),
\]

\[
r_2\mathbin{\cdot}(m,n)=(m+2n+2,-n-2).
\]

For example, to derive the first formula, start with \([n+1,m+n+2]\), swap it, subtract \([1,2]\), and convert back with \(P^{-1}[A,B]=(B-A,A)\).

Composition now reproduces all eight weights. Products below act rightmost first.

| Index | Word | Transformed module weight | Multiplier exponent \(d_i\) |
| --- | --- | --- | --- |
| 1 | \(r_1\) | \((-m-2,m+n+1)\) | 0 |
| 2 | \(r_2\) | \((m+2n+2,-n-2)\) | \(-n-1\) |
| 3 | \(r_2r_1\) | \((m+2n+2,-m-n-3)\) | \(-m-n-2\) |
| 4 | \(r_1r_2\) | \((-m-2n-4,m+n+1)\) | \(-n-1\) |
| 5 | \(r_1r_2r_1\) | \((-m-2n-4,n)\) | \(-m-n-2\) |
| 6 | \(r_2r_1r_2\) | \((m,-m-n-3)\) | \(-m-2n-3\) |
| 7 | \(r_2r_1r_2r_1\) | \((-m-2,-n-2)\) | \(-m-2n-3\) |
| 8 | identity | \((m,n)\) | 0 |

The weight transformations satisfy \(r_1^2=r_2^2=(r_1r_2)^4=1\). That assertion is about the **weight lattice**. It does not say that differentiations with kernels are invertible, or that eight theta maps act as a group on one fixed cohomology space.

For \(t=(1,1)\), the transformed weights in this order are

\[
(-3,3),\ (5,-3),\ (5,-5),\ (-7,3),\
(-7,1),\ (1,-5),\ (-3,-3),\ (1,1).
\]

The corresponding exponents are \(0,-2,-4,-2,-4,-6,-6,0\). Negative target weights are expected here; they are not dominant classical highest weights.

The two candidate paths to the longest element use, in order of application,

\[
D_1^2,\ D_2^4,\ D_1^6,\ D_2^2
\quad\hbox{and}\quad
D_2^2,\ D_1^6,\ D_2^4,\ D_1^2.
\]

Matching their endpoints is a finite calculation. Equality of the resulting differential operators is a stronger identity. On p. 47 the thesis asserts that identity and describes a computational argument whose details are omitted; we have not independently supplied a general proof of it here.

## 5. A legal numerical small-slope example

Choose genus two and the admissible exponent vector

\[
\alpha=(1,0,2,3),\qquad u=\operatorname{diag}(p,1,p^2,p^3).
\]

The required inequalities hold:

\[
\alpha_2<\alpha_1<\alpha_3<\alpha_4,
\qquad \alpha_1+\alpha_3=\alpha_2+\alpha_4=3.
\]

The multiplier and determinant are different:

\[
c(u)=p^3,\qquad\det(u)=p^6=c(u)^2.
\]

For the thesis's bound, \(\beta_1=\alpha_2=0\), \(\beta_2=\alpha_2+\alpha_1=1\). With its special convention \(\alpha_0=\alpha_3\), both relevant differences equal 1. Therefore

\[
\lambda((m,n),\alpha)=n+\min(m+1,n+1).
\]

At \((m,n)=(1,1)\), this is **3**. Proposition 2.9.2 therefore places slope \(h=2\) in the comparison range, but gives no conclusion at \(h=3\). This is a substitution into an actual admissible case, replacing the first-pass hypothetical threshold.

### Check the coefficient action separately

Computing the weights of the normalized minors gives

\[
u(x,a,b,c)=(px,p^2a,p^3b,pc).
\]

The weight twist for \(S_{(m,n)}\) contributes \(p^n\). Thus its action on the displayed monomial basis is

\[
u(x^i a^j b^k c^\ell)=p^{n+i+2j+3k+\ell}x^i a^j b^k c^\ell.
\]

This is a statement about the diagonal **coefficient operator** \(u\), not a computation of the spectrum of the cohomological operator \(U_p=\operatorname{tr}\circ\Phi\circ\operatorname{res}\).

Both \(D_1\) and \(D_2\) lower the weighted polynomial degree \(i+2j+3k+\ell\) by 1 when their output is nonzero. For \(D_2^{n+1}\), the target twist is \(p^{-n-2}\); multiplying it by \(c(u)^{n+1}=p^{3(n+1)}\) restores the source exponent. This independently checks the sign and power of the multiplier in the coefficient intertwining relation. Replacing \(c(u)\) by \(\det(u)\) would double that exponent and fail the check.

## 6. Differentiation can have dense, nonclosed image

Here is a complete one-variable argument. In \(\mathbb Q_p\langle x\rangle\), let

\[
f(x)=\sum_{r\ge1}p^r x^{p^r-1}.
\]

Its coefficients tend to zero, so it belongs to the Tate algebra. If \(g'=f\), comparison of coefficients forces the coefficient of \(x^{p^r}\) in \(g\) to be 1 for every \(r\). Those coefficients do not tend to zero. Hence no such \(g\) belongs to this Tate algebra.

Nevertheless, every polynomial has a polynomial primitive over \(\mathbb Q_p\), and polynomials are dense for the Gauss norm. Therefore the derivative has **dense but nonclosed image**. Its continuity does not imply surjectivity or a bounded inverse.

For a higher derivative \(D^q\), with \(q\ge1\), a series \(f=\sum_{j\ge0}f_jx^j\) is in the image exactly when

\[
\frac{f_j}{(j+1)(j+2)\cdots(j+q)}\longrightarrow0
\quad\text{in }\mathbb Q_p.
\]

Indeed those are precisely the forced coefficients of a primitive of order \(q\); the first \(q\) coefficients may be chosen freely. A denominator \(j+1\) alone describes only the first derivative. This distinction matters when reading the higher powers used in the theta constructions.

## 7. Two arrow and exactness safeguards

The coefficient maps have direction \(\delta_i:S_t\to S_{t_i}\). Taking continuous duals reverses it:

\[
S_{t_i}^{*}\longrightarrow S_t^{*}.
\]

The corresponding cohomological maps therefore run from the \(t_i\)-coefficient group to the \(t\)-coefficient group. No inverse theta map is obtained merely by reversing the weight transformation.

Also, a continuous linear splitting of \(N_t\to N_t/B_t\) is not automatically a \(\Gamma\)-equivariant splitting. The nonclassical complement on p. 36 is expressly not \(\Delta\)-invariant. Consequently it cannot, by itself, supply maps both ways on group cohomology. Reconstructing the classicality proof requires the long exact sequence, compatible finite-slope decompositions, and vanishing of the quotient's small-slope groups in **both adjacent degrees**. The analytic details of that reconstruction remain an open reading task, not an asserted counterexample to the proposition.

## Verification boundary

The six substitutions, derivation formulas, commutator identities, eight affine weight transforms, and the example at \((1,1)\) were checked by exact symbolic arithmetic. The derivative-image argument is proved above. These are ordinary mathematical calculations, not an Agda formalization and not an independent proof of every theorem in the thesis.

Credit and thanks to **Daniel Snaith** and **Kevin Buzzard**. The [bibliographic ledger](sources-and-corrections.md#daniels-numbered-bibliography) names the authors of all twenty numbered thesis references separately from sources actually read in this pass.
