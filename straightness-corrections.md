# Corrected statements for "The Straightness of the Calculus"

All mathematical notation below is LaTeX (`$...$` and `$$...$$`), with no Unicode math characters, so it can be pasted into the essay's Markdown as is. The Fraktur letter needs `\mathfrak` (amssymb/amsfonts in LaTeX; built into MathJax and KaTeX). Each item is either **Replace** (substitute the text) or **Delete**. Items follow the essay's section order.

---

## Framing (plan blockquote, abstract, table)

- **Replace (Milnor's coverage).** Milnor's *Topology from the Differentiable Viewpoint* treats smooth manifolds and maps, regular values, the Sard–Brown theorem, the degree mod 2, oriented manifolds and the Brouwer degree, vector fields and the Euler number, and framed cobordism and the Hopf theorem. It does not treat flows, jets, general transversality, Whitney embedding or Smale–Hirsch. Cite Hirsch, *Differential Topology*, and Lee, *Introduction to Smooth Manifolds*, for those. Remove the "Milnor, Ch. X, §Y" citations, and drop the "Milnor reference" column of the §12 table (or fill it from Hirsch and Lee).
- **Replace (publication).** Milnor's book appeared with the University Press of Virginia (1965); Princeton reprinted it in 1997.
- **Replace (abstract, parallelization).** "The tangent bundle $TS^n$ is trivial if and only if $n\in\{0,1,3,7\}$ (Bott–Milnor, Kervaire, Adams). For general manifolds parallelizability depends on the manifold, not only on its dimension: tori, Lie groups and orientable $3$-manifolds are parallelizable."
- **Replace (abstract, moduli).** "The spaces of connections and of metrics are affine or convex spaces of choices; the corresponding moduli spaces are their quotients by the gauge group or by $\mathrm{Diff}(M)$."

---

## §1. First-order calculus

- **Replace (cotangent space).** $T_p^*M\cong\mathfrak{m}_p/\mathfrak{m}_p^{2}$, and $T_pM=(\mathfrak{m}_p/\mathfrak{m}_p^{2})^{*}$ is its dual.
- **Replace (differential).** $df_p$ is the unique linear map $L$ such that, in charts, $f(p+h)=f(p)+Lh+o(\lVert h\rVert)$. The chain rule $d(g\circ f)_p=dg_{f(p)}\circ df_p$ says that $(M,f)\mapsto(TM,df)$ is a functor. Delete "unique natural transformation" here and in §11.
- **Replace (exterior derivative).** $d$ is the unique antiderivation of degree $+1$ on $\Omega^\bullet(M)$ that agrees with the differential on functions; $d^2=0$ then follows. (The phrase "antisymmetric first-order operator with $d^2=0$" does not determine $d$, since $\lambda d$ also satisfies it.)
- **Replace (Lie derivative).** $\mathcal{L}_X$ is the unique derivation of the tensor algebra that commutes with contractions, satisfies $\mathcal{L}_Xf=Xf$ on functions, and satisfies $\mathcal{L}_XY=[X,Y]$ on vector fields. Without the last condition any covariant derivative $\nabla_X$ meets the other requirements.

---

## §2. The inverse function theorem

- **Replace (higher-order behaviour of the inverse).** $D(f^{-1})_{f(p)}=(Df_p)^{-1}$. More generally, the $k$-jet of $f^{-1}$ at $f(p)$ is determined by the $k$-jet of $f$ at $p$ (formal inversion of the Taylor series). Delete "Two functions with the same $2$-jet at $p$ can have inverses that differ to second order." What finite jets do not determine is the germ itself (for $C^\infty$ non-analytic $f$). If $f$ is real-analytic or holomorphic, $f^{-1}$ is analytic and its Taylor series converges.
- **Replace (attribution of the proof).** The standard proof is a contraction-mapping argument (see Rudin, Dieudonné or Lee). I do not believe Milnor proves it, so remove the attribution.
- **Replace (the "Principle (grading by order)" box).** "First derivatives of a map between manifolds are canonical: $df$ is a bundle map $TM\to f^*TN$. Higher derivatives are not canonical as tensors: $k$-jets transform non-linearly under coordinate changes, and splitting them requires extra structure, such as a connection. Canonical exceptions occur at special loci, for example the Hessian at a critical point."
- **Delete.** "The 'curvature' of a constant-rank map is zero, locally."
- **Replace (Palais).** A proper local diffeomorphism between connected manifolds is a covering map; if the target is simply connected it is a diffeomorphism. Properness implies the covering property, and the two are not equivalent.

---

## §3. Immersions and embeddings

- **Replace (Whitney, strong form).** Every smooth $n$-manifold (closed or not) embeds in $\mathbb{R}^{2n}$, and immerses in $\mathbb{R}^{2n-1}$ for $n>1$.
- **Replace (general position, "weak Whitney").** For a generic smooth map $M^n\to\mathbb{R}^m$ the rank-deficient locus has codimension $m-n+1$ in $M$, and double points have expected dimension $2n-m$. Hence a generic map is an immersion for $m\ge 2n$ and an embedding for $m\ge 2n+1$ (compact $M$). Generic maps $M^n\to\mathbb{R}^{2n-1}$ have Whitney-umbrella singularities. The numbers $2n$ and $2n+1$ come from this dimension count, not from "the dimension of the space of jets".
- **Replace (Smale–Hirsch).** For $m>n$, or $M$ open, the map $\mathrm{Imm}(M,N)\to\mathrm{Mono}(TM,TN)$, $f\mapsto df$, is a weak homotopy equivalence. In particular immersions up to *regular homotopy*, not isotopy, correspond to bundle monomorphisms up to homotopy.
- **Replace (embeddings).** Isotopy classes of embeddings are not determined by $df$ (knots in $S^3$ are the standard example). Delete the row "Embedding (global) | order $1$" from the table.

---

## §4. Regular values, transversality, Morse theory

- **Replace (Sard).** For almost every $c\in\mathbb{R}^k$, $f^{-1}(c)$ is a smooth submanifold of dimension $n-k$. Delete "generic hyperplane section" and the remark about time slices.
- **Replace (Thom transversality).** For any submanifold $W$ of the jet bundle $J^k(M,N)$, the set of maps $f$ with $j^kf\pitchfork W$ is residual (hence dense) in the Whitney $C^\infty$ topology. Statements about families are the *parametric* transversality theorem.
- **Replace (Morse lemma).** If $p$ is a nondegenerate critical point, there are coordinates with
 $$f=f(p)-y_1^2-\cdots-y_k^2+y_{k+1}^2+\cdots+y_n^2 .$$
 The index $k$ is the only invariant (Sylvester). The charts are not canonical. The linear symmetry group of the normal form is $O(k,n-k)$, not $O(n)$.
- **Replace (stationary phase).**
 $$\int e^{i\lambda f(x)}a(x)\,dx\sim\Bigl(\tfrac{2\pi}{\lambda}\Bigr)^{n/2}\lvert\det\mathrm{Hess}f(p)\rvert^{-1/2}\,e^{i\lambda f(p)}\,e^{i\pi\,\mathrm{sgn}(\mathrm{Hess}f(p))/4}\,a(p),$$
 where $\mathrm{sgn}=n-2k$ and $k$ is the number of negative eigenvalues.

---

## §5. Vector fields, flows, Darboux

- **Replace (flow).** The equation $\dot\gamma=X(\gamma)$ is a nonlinear autonomous ODE; uniqueness is Picard–Lindelöf. The flow is defined for all $t\in\mathbb{R}$ only if $X$ is complete.
- **Replace (Liouville).** If $\mathcal{L}_{X_H}\omega=0$ then $\mathcal{L}_{X_H}\omega^n=0$, and $\omega^n/n!$ is the volume form. Darboux's theorem is not involved.
- **Replace (Darboux).** Near every point of a symplectic manifold $(M^{2n},\omega)$ there are coordinates in which $\omega=\sum_{i=1}^n dx^i\wedge dx^{n+i}$. These charts are highly non-unique: the freedom is the group of local symplectomorphisms. The theorem holds because $d\omega=0$ (Moser's trick), not because "the first jet determines $\omega$". Delete "sharpest possible uniqueness" and "the straightening is canonical".

---

## §6. The tangent bundle

- **Replace (parallelizable spheres).** $TS^n$ is trivial if and only if $n\in\{0,1,3,7\}$. The non-existence for other $n$ is due to Bott–Milnor and Kervaire (1958); Adams's Hopf-invariant-one theorem (1960) and his work on vector fields on spheres (1962) give the sharp form. Delete "a function of its dimension".
- **Replace (division algebras).** The normed division algebras $\mathbb{R},\mathbb{C},\mathbb{H},\mathbb{O}$ have dimensions $1,2,4,8$, and $S^0,S^1,S^3,S^7$ are their unit spheres. Maps $S^{2n-1}\to S^n$ of Hopf invariant one exist only for $n\in\{1,2,4,8\}$.
- **Replace (characteristic classes).** The Euler class $e(E)\in H^n(M;\mathbb{Z})$ is the primary obstruction to a nonvanishing section of an oriented rank-$n$ bundle. Vanishing of the Stiefel–Whitney, Pontryagin and Euler classes is necessary for triviality but not sufficient: $S^5$ is stably parallelizable, so all these classes vanish, yet $S^5$ is not parallelizable. Pontryagin classes $p_i(E)=(-1)^ic_{2i}(E\otimes\mathbb{C})\in H^{4i}(M;\mathbb{Z})$ are defined for every real bundle. A complex structure on $E$ imposes relations on them, but they are not "the obstruction" to one.
- **Replace (the $TS^2$ remark).** As a complex line bundle over $\mathbb{CP}^1$, $TS^2\cong\mathcal{O}(2)$, so $e(TS^2)=c_1=2$. The Hopf bundle is $\mathcal{O}(-1)$. Delete the Riemann–Roch sentence.
- **Replace (products).** $\Omega^\bullet(M_1)\otimes\Omega^\bullet(M_2)$ is dense in $\Omega^\bullet(M_1\times M_2)$, with equality after completing the tensor product. The Künneth isomorphism holds in cohomology, and $\chi(M_1\times M_2)=\chi(M_1)\chi(M_2)$.

---

## §7. Jets

- **Replace (definition).** $j^k_pf$ is the class of $f$ in $C^\infty_p/\mathfrak{m}_p^{k+1}$. The $1$-jet is $(f(p),df_p)$. The bundle $J^k$ has transition functions that are polynomial in the higher derivatives of the coordinate change. The splitting "gradient $+$ Hessian" is coordinate-independent only at a critical point, or given a connection.
- **Replace (moduli of straightenings).** Jets of *functions* are not "moduli of straightenings". The freedom in a $k$-th order straightening is measured by $k$-jets of coordinate changes, i.e. by the group $G^k$ of $k$-jets of diffeomorphisms of $\mathbb{R}^n$ at $0$, an extension of $GL_n(\mathbb{R})$ by a unipotent group. A torsion-free connection is a $GL_n$-equivariant splitting of the second-order frame bundle onto the first-order frame bundle.
- **Replace (formal inverse).** Delete "it is not determined by any finite jet, and it does not always converge". See §2 above.
- **Replace (Morse–Bott).** In a tubular neighbourhood of a nondegenerate critical manifold $C$,
 $$f=f|_C+\lvert y\rvert^2-\lvert z\rvert^2,$$
 where $y,z$ are fibre coordinates on the positive and negative eigenbundles of the normal Hessian. This generalizes Morse's lemma to degenerate critical *manifolds*; it is not a "higher-order" generalization.
- **Replace (Morse homology).** For a Morse function $f$ and a metric such that $(f,g)$ is Morse–Smale, the Morse–Smale–Witten complex computes $H_*(M)$ (Smale, Milnor, Witten, Floer). Delete "Morse–Weyl theorem", which is not a standard name.
- **Replace (physics paragraph).** A bounce's single negative mode produces the imaginary part of the energy, i.e. the decay rate. The one-loop prefactor is the quadratic-fluctuation determinant, and higher-order terms give higher loops. The $\theta$-dependence comes from the topological charge, and fermion zero modes come from the index.

---

## §8. Connections, curvature, Nash

- **Replace (space of connections).** On a vector bundle $E$, connections form an affine space modelled on $\Omega^1(M;\mathrm{End}\,E)$; on a principal $G$-bundle $P$, on $\Omega^1(M;\mathrm{ad}\,P)$. The moduli space is the quotient by the gauge group.
- **Replace (Levi-Civita proof).** Metric compatibility and zero torsion force the Koszul formula
 $$2g(\nabla_XY,Z)=Xg(Y,Z)+Yg(X,Z)-Zg(X,Y)+g([X,Y],Z)-g([X,Z],Y)-g([Y,Z],X),$$
 so $\nabla$ is unique. The formula defines a connection with both properties, so $\nabla$ exists. Delete the "three unknowns" paragraph.
- **Replace (curvature in normal coordinates).**
 $$R_{ijkl}(p)=\tfrac12\bigl(\partial_j\partial_kg_{il}+\partial_i\partial_lg_{jk}-\partial_i\partial_kg_{jl}-\partial_j\partial_lg_{ik}\bigr)(p),$$
 with $R_{ijkl}=g_{im}R^m{}_{jkl}$.
- **Replace (geodesics).** Uniqueness of the Levi-Civita connection says that the metric determines the connection. Uniqueness of the geodesic with given initial data is ODE theory. Connections with torsion can have the same geodesics as Levi-Civita.
- **Replace (Bianchi and tensoriality).** $R(X,Y)Z$ is a tensor because it is $C^\infty(M)$-linear in $X$, $Y$ and $Z$. The Bianchi identities ($d_\nabla R=0$) are differential identities, not the reason for tensoriality.
- **Replace (Nash, history).**
 - $C^1$ isometric embeddings: Nash (1954) for $N\ge n+2$; Kuiper (1955) for $N\ge n+1$.
 - Nash (1956) proved the $C^k$ case for $3\le k\le\infty$, with $N=n(3n+11)/2$ for compact $M$ and $N=n(n+1)(3n+11)/2$ for noncompact $M$. His $C^\infty$ proof uses his own smoothing iteration.
 - Moser (1961) isolated the method for other problems, and Hamilton (1982) gave the abstract Nash–Moser inverse function theorem.
 - Later work (Gromov, Günther) lowered $N$ substantially. Delete the "1965, $C^\infty$ via Nash–Moser" line and "$k\ge1$".
- **Replace (non-uniqueness of embeddings).** Isometric embeddings are far from unique, even modulo rigid motions: the $C^1$ case is flexible (Nash–Kuiper), while some $C^2$ cases are rigid (convex surfaces). Delete "unique up to rigid motions".

---

## §9. Smooth structures and exotic spheres

- **Replace (exotic $\mathbb{R}^4$).** Freedman's classification of simply connected topological $4$-manifolds, together with Donaldson's theorem on smooth $4$-manifolds with definite intersection form, yields a smooth structure on $\mathbb{R}^4$ that is not diffeomorphic to the standard one (Freedman–Donaldson, early 1980s). Gompf (1985) constructed infinitely many, and Taubes (1987) uncountably many, using gauge theory on end-periodic manifolds. Delete "Mazur, 1966" from the theorem and table, and delete the Mazur–$B^4$ gluing paragraph and the "uncountable space of embeddings" argument. Optional replacement note: Mazur (1961) constructed compact contractible smooth $4$-manifolds $W$ whose boundary is a homology $3$-sphere with nontrivial $\pi_1$. Such a $W$ is not diffeomorphic to $B^4$, although $W\times[0,1]\cong B^5$.
- **Replace (uniqueness of $\mathbb{R}^n$).** The smooth structure on $\mathbb{R}^n$ is unique up to diffeomorphism for $n\le 2$ (classical), for $n=3$ (Moise), and for $n\ge5$ (Stallings and smoothing theory). It is not the Poincaré conjecture that gives $n=3$.
- **Replace (Milnor's spheres).** Milnor's paper is from 1956. He considered $S^3$-bundles over $S^4$ with Euler number $1$, which are homotopy $7$-spheres. A Morse function with two critical points shows they are homeomorphic to $S^7$, and an invariant built from the signature theorem and $p_1^2$ shows that some are not diffeomorphic to $S^7$. Triviality of $TS^7$ is not used.
- **Replace ($\Theta_7$).** $\Theta_7\cong\mathbb{Z}/28$ is due to Kervaire–Milnor (1963), and the classes are distinguished by the Eells–Kuiper invariant $\mu$, not by the Euler number (which equals $1$ for every homotopy sphere in the family). The bundle spheres realize $16$ of the $28$ classes: in Milnor's family $\mu\equiv m(m+1)/2\pmod{28}$.
- **Replace ($\Theta_n$).** $\Theta_n$ is finite for $n\ge5$ but often nonzero. Exotic spheres and exotic $\mathbb{R}^n$ are different phenomena: an exotic $S^n$ minus a point is standard $\mathbb{R}^n$ for $n\ge5$. Delete "and it vanishes in the sense that...".
- **Replace (Poincaré conjecture, dimension 4).** Freedman: every simply connected closed topological $4$-manifold homotopy equivalent to $S^4$ is homeomorphic to $S^4$. The smooth version, with "diffeomorphic to $S^4$", is open. The existence of exotic $\mathbb{R}^4$ does not by itself imply the existence of an exotic $S^4$.
- **Replace (physics).** Witten's interpretation of Donaldson invariants as correlation functions of the topologically twisted $\mathcal{N}=2$ theory is 1988. The 1994 paper is the Seiberg–Witten (monopole) work. The instanton number $c_2$ is topological; what depends on the smooth structure is the instanton moduli space and the Donaldson invariants. Delete the "vacuum structure" sentence.

---

## §10. Infinite dimensions

- **Replace (Hamilton's theorem).** Let $F$ be a smooth tame map between tame Fréchet spaces. If $DF(x)$ is invertible for all $x$ near $x_0$ and the inverses form a smooth tame family, then $F$ is a local diffeomorphism with smooth tame inverse. Tameness is extra structure (a grading and smoothing operators), not "a topology slightly weaker than $C^\infty$".
- **Replace (derivative loss and smoothing).** In Nash–Moser settings the right inverse satisfies $\lVert(DF_x)^{-1}y\rVert_s\lesssim\lVert y\rVert_{s+r}$ for a fixed $r$ (for example $r=1$ or $2$ for isometric embedding, $r=\tau$ for KAM), so plain Newton loses $r$ derivatives per step. Smoothing operators $S_\theta$ satisfy
 $$\lVert S_\theta u\rVert_{s+a}\lesssim\theta^{a}\lVert u\rVert_s,\qquad\lVert(1-S_\theta)u\rVert_s\lesssim\theta^{-a}\lVert u\rVert_{s+a}.$$
 The iteration $x_{n+1}=x_n-S_{\theta_n}(DF_{x_n})^{-1}F(x_n)$ with $\theta_n$ growing fast converges superexponentially. Delete the passage saying the inverse "loses derivatives" and "gains $k$ derivatives".
- **Replace (isometric embedding operator).** $F(f)=f^*\delta-g$, and for $h\in C^\infty(M,\mathbb{R}^N)$
 $$DF_f(h)(u,v)=\langle df(u),dh(v)\rangle+\langle dh(u),df(v)\rangle .$$
 The Lie-derivative formula describes only the tangential variations $h=df(X)$. At "free" maps (Gromov), which requires $N\ge n(n+3)/2$, the linearization has a right inverse that is a differential operator.
- **Replace (KAM).** A frequency $\omega$ is Diophantine if $\lvert\omega\cdot k\rvert\ge\gamma\lvert k\rvert^{-\tau}$ for all $k\in\mathbb{Z}^n\setminus\{0\}$, with $\tau\ge n-1$ (and $\tau>n-1$ for full measure). Then $1/\lvert\omega\cdot k\rvert\le\lvert k\rvert^{\tau}/\gamma$, so the inverse of $\omega\cdot\partial_\theta$ loses about $\tau$ derivatives. Add the Kolmogorov nondegeneracy condition $\det(\partial\omega/\partial I)\ne0$. In the analytic case (Kolmogorov, Arnold) a quadratically convergent Newton scheme works without smoothing; smoothing is needed for finite differentiability (Moser). Conclusion: invariant tori with Diophantine frequencies persist, conjugate to linear flows, and form a Cantor family of large measure. Delete "the smoothing operator is a canonical transformation".
- **Delete/replace (Moser's stability theorem).** Moser's stability theorem (deformations of volume or symplectic forms) is unrelated to Nash–Moser.
- **Replace (regularity).** The Banach inverse function theorem holds for $C^k$ maps for every $k\ge1$. What fails is the Fréchet-space setting combined with derivative loss, not "$C^\infty$ versus $C^1$".

---

## §11. The index theorem

- **Replace (the formula).**
 $$\mathrm{ind}\,P=(-1)^n\int_{T^*M}\mathrm{ch}(\sigma(P))\,\mathrm{Td}(TM\otimes\mathbb{C}),\qquad\mathrm{ch}(\sigma(P))\in H^*_c(T^*M).$$
 The $\hat{A}$-genus appears for Dirac operators twisted by a bundle $V$:
 $$\mathrm{ind}\,D_V=\int_M\hat{A}(TM)\,\mathrm{ch}(V),\qquad\hat{A}=\prod_j\frac{x_j/2}{\sinh(x_j/2)},$$
 where $\pm x_j$ are the formal roots of $TM\otimes\mathbb{C}$.
- **Replace (heat-kernel proof).** $\mathrm{ind}\,P=\mathrm{Tr}\,e^{-tP^*P}-\mathrm{Tr}\,e^{-tPP^*}$ for every $t>0$ (McKean–Singer). The local expansion is $(4\pi t)^{-n/2}\sum_{j\ge0}a_j(x)t^j$, and $a_0$ is just the fibre rank. The index density is the $t^0$ coefficient, i.e. $a_{n/2}(P^*P;x)-a_{n/2}(PP^*;x)$ (for $n$ even). It is a universal polynomial in curvature and in the derivatives of the coefficients. Identifying it with the Atiyah–Singer integrand is due to Patodi, Gilkey and Atiyah–Bott–Patodi (1973), and to Getzler's rescaling for Dirac operators. It is not "Atiyah–Singer II".
- **Replace (consequence for the thesis).** The integrand is built from curvature, a second-order and metric-dependent quantity. The index is a case in which second-order local data integrate to a metric-independent integer. Delete "computed in $\mathbb{R}^n$ (the straightening)", "no moduli, no choices" and "canonical straightening density".
- **Replace (K-theory).** The symbol class lives in compactly supported K-theory, $[\sigma(P)]\in K_c(T^*M)=K(D^*M,S^*M)$. The analytic index is a homomorphism $K_c(T^*M)\to\mathbb{Z}$. The topological index uses an embedding $M\subset\mathbb{R}^N$, the Thom isomorphism (the total space of $T^*M$ is stably almost complex) and Bott periodicity. Pairing with $[M]\in K_0(M)$ requires a $K$-orientation of $M$. For a finite covering $\pi$ of degree $d$, $\mathrm{ind}(\pi^*P)=d\cdot\mathrm{ind}\,P$; delete the claim about $f_*$ for proper maps. The Atiyah–Singer axioms (normalization and functoriality) characterize the index; that is a different sense of "unique" from the chain-rule statement in §1.
- **Replace (instantons).** For an $SU(2)$ instanton of charge $k$, $\mathrm{ind}\,D_A=k$ in the fundamental representation and $4k$ in the adjoint; in general it is $2T(R)k$. The zero-mode count is $k$, not $2k$, and the fermion determinant vanishes to order $k$ in the mass.
- **Replace (anomalies).** The anomaly is obtained from the anomaly polynomial $[\hat{A}\,\mathrm{ch}(F)]$ by descent (not the reverse). Witten's $SU(2)$ anomaly is a mod-$2$ index of the Dirac operator on a $5$-dimensional mapping torus, related to $\pi_4(SU(2))=\mathbb{Z}/2$. For families, the index is a class in $K^0(B)$, and the anomaly is carried by its determinant line bundle: curvature gives the local part and holonomy the global part. It is not "an obstruction to a family of sections".
- **Replace (dates and references).** Atiyah–Singer I and III: *Ann. of Math.* **87** (1968); II (Atiyah–Segal): **87** (1968); IV and V: **93** (1971). The heat-kernel proof is Atiyah–Bott–Patodi, *Invent. Math.* **19** (1973), "On the heat equation and the index theorem".

---

## §12. The table and the thesis

**Replace the table** (the old "Order" and "Milnor reference" columns are dropped; existence and uniqueness are now separate):

| Object | Exists? | Unique? | Freedom or obstruction |
|---|---|---|---|
| Tangent space $T_pM$ | yes | canonical | none |
| Differential $df_p$ | yes | canonical | none |
| Exterior derivative $d$ | yes | unique antiderivation extending $df$ | none |
| Lie derivative $\mathcal{L}_X$ | yes | unique derivation commuting with contractions, with $\mathcal{L}_XY=[X,Y]$ | none |
| Local inverse | yes if $Df_p$ invertible | yes; $k$-jet of $f^{-1}$ determined by $k$-jet of $f$ | none |
| Flow of a vector field | locally (globally if complete) | yes (Picard–Lindelöf) | none |
| Flow-box chart | yes if $X\neq0$ | no | diffeomorphisms $\psi$ with $\psi_*\partial_1=\partial_1$ |
| Darboux chart | yes | no | local symplectomorphisms; the only obstruction to flatness is $d\omega\neq0$ |
| Morse chart | at nondegenerate critical points | index unique, chart not | index $k$ is the only invariant |
| $k$-jet of a function, $k\ge2$ | yes (a section of $J^k$) | not determined by lower jets | splitting into tensors needs a connection |
| Immersions ($m>n$) | h-principle | regular homotopy classes $\leftrightarrow$ monomorphisms $TM\to TN$ | none beyond the bundle data |
| Embeddings | for $m\ge2n$ | no | knotting; isotopy class not determined by $df$ |
| Parallelization of $S^n$ | iff $n\in\{0,1,3,7\}$ | when it exists, parallelizations differ by maps $S^n\to GL_n(\mathbb{R})$ | Bott–Milnor, Kervaire, Adams |
| Riemannian metric | yes | no (a choice) | convex cone; moduli $=$ quotient by $\mathrm{Diff}(M)$ |
| Levi-Civita connection | yes | unique given $g$ | none |
| Curvature $R^\nabla$ | defined for every $\nabla$ | determined by $\nabla$ | obstruction to local flatness |
| Smooth structure on $\mathbb{R}^n$, $n\ne4$ | yes | unique up to diffeomorphism | none |
| Smooth structure on $\mathbb{R}^4$ | yes | no: uncountably many | exotic $\mathbb{R}^4$ (Freedman–Donaldson, Gompf, Taubes) |
| Exotic $7$-spheres | yes | $\Theta_7\cong\mathbb{Z}/28$ | Eells–Kuiper invariant $\mu$ |
| Banach inverse function theorem | yes | local diffeomorphism unique | none |
| Fréchet inverse function theorem | fails in general | n/a | derivative loss |
| Nash–Moser (Hamilton) | for tame families with tame inverses | yes | smoothing operators; Diophantine condition in KAM |
| Atiyah–Singer index | elliptic $P$ on closed $M$ | depends only on $[\sigma(P)]\in K_c(T^*M)$ | none |

**Replace (the "straightness principle" box and the concluding paragraphs).**

> **The straightness principle (revised).** A geometric structure on $M$ is a reduction of the frame bundle to a subgroup $G\subset GL_n(\mathbb{R})$. It is locally flat, i.e. locally equivalent to the model on $\mathbb{R}^n$, exactly when it is integrable, and the obstruction has a definite order. For symplectic structures ($G=Sp_{2n}$) the only obstruction is $d\omega\ne0$, a first-order condition, and Darboux's theorem gives normal forms with no local invariants. For Riemannian structures ($G=O(n)$) the intrinsic torsion always vanishes (Levi-Civita), so the first obstruction is the curvature, a second-order condition. For almost complex structures the obstruction is the Nijenhuis tensor (first order; Newlander–Nirenberg). Global obstructions are characteristic classes. In infinite dimensions, the Banach inverse function theorem works, and Nash–Moser (Hamilton) repairs it for tame Fréchet maps. For elliptic operators, the index is the case in which curvature-built local densities integrate to a metric-independent integer.

**Replace (closing paragraph for physicists).** When you expand about a background $x_0$ and keep the linear term, you use the canonical linearization $DF_{x_0}$. It is canonical as a map, but it depends on $x_0$. At a critical point the Hessian is also canonical (this is the Morse lemma); away from critical points, second derivatives require a connection. Curvature is the first local invariant of a metric and appears at second order. When you compute the index of an elliptic operator (the chiral anomaly, the number of instanton zero modes, the Witten index), you integrate a curvature-built local density and obtain an integer that does not depend on the metric.

---

## References (corrected or added)

Keep the ones you have already checked, and verify pages against the originals:

- J. Milnor, "On manifolds homeomorphic to the $7$-sphere," *Ann. of Math.* **64** (1956), 399–405.
- M. Kervaire and J. Milnor, "Groups of homotopy spheres: I," *Ann. of Math.* **77** (1963), 504–537.
- J. Milnor, "On the existence of a connection with curvature zero," *Comment. Math. Helv.* **32** (1958), 215–223.
- R. Bott and J. Milnor, "On the parallelizability of the spheres," *Bull. Amer. Math. Soc.* **64** (1958), 87–89.
- M. Kervaire, "Non-parallelizability of the $n$-sphere for $n>7$," *Proc. Nat. Acad. Sci. USA* **44** (1958), 280–283.
- J. F. Adams, "On the non-existence of elements of Hopf invariant one," *Ann. of Math.* **72** (1960), 20–104; "Vector fields on spheres," *Ann. of Math.* **75** (1962), 603–632.
- J. Nash, "$C^1$ isometric imbeddings," *Ann. of Math.* **60** (1954), 383–396; "The imbedding problem for Riemannian manifolds," *Ann. of Math.* **63** (1956), 20–63.
- N. Kuiper, "On $C^1$-isometric imbeddings I, II," *Indag. Math.* **17** (1955), 545–556, 683–689.
- J. Moser, "A new technique for the construction of solutions of nonlinear differential equations," *Proc. Nat. Acad. Sci. USA* **47** (1961), 1824–1831.
- R. Hamilton, "The inverse function theorem of Nash and Moser," *Bull. Amer. Math. Soc.* **7** (1982), 65–222.
- M. Hirsch, "Immersions of manifolds," *Trans. Amer. Math. Soc.* **93** (1959), 242–276.
- B. Mazur, "A note on some contractible $4$-manifolds," *Ann. of Math.* **73** (1961), 221–228.
- R. Gompf, "An infinite set of exotic $\mathbb{R}^4$'s," *J. Differential Geom.* **21** (1985), 283–300.
- C. H. Taubes, "Gauge theory on asymptotically periodic $4$-manifolds," *J. Differential Geom.* **25** (1987), 363–430.
- R. Gompf and A. Stipsicz, *$4$-Manifolds and Kirby Calculus*, AMS, 1999.
- E. Witten, "Topological quantum field theory," *Comm. Math. Phys.* **117** (1988), 353–386; "Monopoles and four-manifolds," *Math. Res. Lett.* **1** (1994), 769–796.
- M. Atiyah and I. Singer, "The index of elliptic operators: I, III," *Ann. of Math.* **87** (1968), 484–530, 546–604; "IV, V," **93** (1971), 119–138, 139–149. M. Atiyah and G. Segal, "The index of elliptic operators: II," *Ann. of Math.* **87** (1968), 531–545.
- M. Atiyah, R. Bott and V. K. Patodi, "On the heat equation and the index theorem," *Invent. Math.* **19** (1973), 279–330.

Entries from the original bibliography that I could not match to real publications, and would remove unless you can locate them: "Differentiable structures on $S^7$" (*Proc. AMS* 1961), Nash "II (1963)", Moser 1963 and 1965, Hirsch 1961, Witten 1992 (*J. Geom. Phys.*), the Zumino–Witten 1983 entry, Atiyah–Patodi–Singer "Spectral asymptotics and the index theorem" (1973), Donaldson *Lectures on the Topology of 4-Manifolds*, and the Palais 1966 entry.
