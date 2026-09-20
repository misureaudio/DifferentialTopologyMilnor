## 11. The Atiyah–Singer index theorem: the global counterpart of the straightening principle

*(Beyond Milnor; the global theorem that closes the grading.)*

So far the global calculus has appeared as *obstruction*: characteristic classes measure the failure of the global straightening, and the smooth structure is non-unique in dimension four. There is a complementary global theorem, and it is the one that most directly completes the straightness principle: it says that **when a straightening is given in the form of an elliptic operator, the global content of the straightening is not merely obstructed but canonically determined** — it is a unique, natural, topological invariant of the local straightening data. This is the Atiyah–Singer index theorem.

**Elliptic operators and the symbol as straightening.** Let $M$ be a closed smooth $n$-manifold, $E,F$ complex vector bundles over $M$, and $P:\Gamma(E)\to\Gamma(F)$ a differential operator of order $m$. The **principal symbol** $\sigma(P)\in\Gamma(T^*M\setminus 0,\mathrm{Hom}(\sigma E,\sigma F))$ is a bundle map over the punctured cotangent bundle, and it is the straightening of $P$: at each covector $\xi\neq 0$, $\sigma_\xi(P)$ is the linear operator that $P$ becomes when the manifold is straightened at $\xi$. The symbol is the part of $P$ that is invariant under lower-order perturbations — the part that survives the passage to the cotangent bundle. In the language of the essay, the symbol is the straightening of $P$, and it is canonical: it does not depend on any choice.

The operator $P$ is **elliptic** if $\sigma_\xi(P)$ is invertible for every $\xi\neq 0$; that is, if the straightening is invertible away from the zero section. Elliptic operators form an open set in the space of differential operators, and each elliptic $P$ is **Fredholm**: $\ker P$ and $\mathrm{coker}\,P$ are finite-dimensional, and the **index**
$$
\operatorname{ind} P \;=\; \dim\ker P - \dim\mathrm{coker}\,P
$$
is a stable integer, locally constant in the space of elliptic operators. The kernel and cokernel separately depend on the full operator (the higher-order terms, the moduli); the index does not. It depends only on the symbol, and the theorem that says so is the index theorem.

**Theorem (Atiyah–Singer, 1960–1968).** Let $P:\Gamma(E)\to\Gamma(F)$ be a complex elliptic operator on a closed smooth manifold $M$. Then
$$
\operatorname{ind} P \;=\; \int_M \operatorname{ch}(\sigma(P))\cdot \hat A(TM),
$$
where $\operatorname{ch}(\sigma(P))$ is the Chern character of the symbol (a class in even cohomology of $T^*M$), $\hat A(TM)=\prod_i \frac{x_i}{2\sinh(x_i/2)}$ is the $\hat A$-genus of $M$ (evaluated on the Chern roots $2x_i$ of the complexified tangent bundle), and the product is the cup product pushed forward to a number by the Thom isomorphism (equivalently, integration over $M$).

In its three classical special cases the theorem reduces to the three classical topological formulas, and each of them is a *straightening* in the language of the essay:

- **Gauss–Bonnet / Poincaré–Hopf.** For the de Rham complex (the Euler operator $d+d^*$), $\operatorname{ind}=\chi(M)=\int_M e(TM)$, the Euler class. The index of the de Rham straightening is the Euler characteristic.
- **Hirzebruch–Riemann–Roch.** For the Dolbeault operator $\bar\partial:\Omega^{0,\bullet}(L)\to\Omega^{0,\bullet+1}(L)$, $\operatorname{ind}\bar\partial=\int_M \operatorname{ch}(L)\cdot\operatorname{td}(TM)=\chi(M,L)$.
- **Hirzebruch signature theorem.** For the signature operator on a $4k$-manifold, $\operatorname{ind}=\langle L(TM),[M]\rangle=\operatorname{sign}(M)$, the signature.

**The heat kernel proof, and the local-to-global bridge.** The proof that makes the straightening principle explicit is the heat kernel proof (Atiyah–Singer II). The index can be written as
$$
\operatorname{ind} P \;=\; \operatorname{Tr}\big(e^{-tP^*P}-e^{-tPP^*}\big),
$$
and the trace is independent of $t$ (the two heat semigroups differ by a supercommutator, whose trace vanishes). As $t\to 0^+$, the heat kernel has the local asymptotics
$$
e^{-tP^*P}(x,x)\sim (4\pi t)^{-n/2}\sum_{j\ge 0} a_j(x)\,t^j,
$$
where each $a_j(x)$ is a local density, and the leading coefficient $a_0(x)$ is computed *in a straightening*: it is the value of the heat kernel of the constant-coefficient operator with principal symbol $\sigma(P)$ on $\mathbb{R}^n$ — the Gaussian $(4\pi t)^{-n/2}e^{-|x|^2/t}$. The **index density**
$$
a(x)\;=\;a_0^{P^*P}(x)-a_0^{PP^*}(x)
$$
is a canonical function on $M$, determined by the symbol alone, and the theorem is the assertion that
$$
\operatorname{ind} P \;=\; \int_M a(x).
$$
This is the purest form of the straightness principle: **the global topological invariant is the integral of the local straightening density.** The integrand is computed in $\mathbb{R}^n$ (the straightening), and the global index is its integral. No moduli, no choices: the local density is canonical, and the passage from local to global is an integration.

**The K-theoretic formulation.** The symbol $\sigma(P)$ defines a class $[\sigma(P)]\in K^0(T^*M\setminus 0)$, and the index is the homomorphism
$$
\operatorname{ind}: K^0(T^*M\setminus 0)\to \mathbb{Z}
$$
sending a symbol class to the index of any operator with that symbol. The K-theoretic Thom isomorphism $K^0(T^*M\setminus 0)\cong K^0(M)$ identifies the symbol class with a class on $M$, and the index is the pairing of that class with the fundamental class $[M]\in K_0(M)$. In this formulation the straightening is the symbol — a class over the cotangent bundle, the "momentum-space" straightening — and the index is the K-theoretic pairing with the fundamental class. The index homomorphism is **natural**: for a proper map $f:M\to N$, $\operatorname{ind}(f^*P)=f_*(\operatorname{ind} P)$ (pushforward in $K$-theory), which on a covering map of degree $d$ reads $\operatorname{ind}(f^*P)=d\cdot\operatorname{ind} P$. The index is the unique natural homomorphism from the category of symbol classes to $\mathbb{Z}$ whose restriction to a point is the ordinary dimension of the kernel. In the language of §1, where the derivative was the unique natural transformation from smooth maps to linear maps, the index is the unique natural transformation from straightenings (symbol classes) to integers.

**The physics of the index.** For the audience at hand the index theorem is not a curiosity; it is *the* theorem.

- **Chiral anomalies.** The Adler–Bell–Jackiw anomaly of a chiral fermion coupled to a gauge field $A$ is the index of the Dirac operator $D_A$: the anomalous divergence $\partial_\mu j^\mu$ is the index density, and the anomaly polynomial is the descent of $\operatorname{ch}(F_A)\cdot\hat A$. The anomaly is the index, and the index is the local straightening density, integrated.
- **Instantons.** On $\mathbb{R}^4$, the index of the Dirac operator coupled to a gauge field is
$$
\operatorname{ind} D_A \;=\; \int_{\mathbb{R}^4} \operatorname{ch}_2(F_A)\cdot\hat A(T\mathbb{R}^4) \;=\; \int_{\mathbb{R}^4} \operatorname{ch}_2(F_A),
$$
and for an $SU(2)$ instanton of topological charge $k$ this equals $2k$: the number of fermion zero modes is $2k$. The zero modes are the global content of the local straightening (the symbol of $D_A$), and the instanton number is the index. This is the mathematical content of the statement that the fermion determinant in an instanton background vanishes to order $2k$.
- **Witten index.** The Witten index of a supersymmetric quantum mechanics, $\operatorname{Tr}(-1)^F e^{-\beta H}$, is the index of the Dirac operator on the configuration space, and the Atiyah–Singer theorem computes it as $\int_M \hat A$. The Witten index is the index, and the index is topological: it is independent of the Hamiltonian (the straightening), depending only on the topological class of the symbol.
- **Index of a family.** For a family of elliptic operators $P_s$ parametrized by a space $B$, the index is a class in $K^0(B)$ — the index of the family is the obstruction to a family of sections of the kernel bundle. This is the theorem behind **anomaly inflow** and behind **global anomalies** (Witten's $SU(2)$ anomaly): the global anomaly is the mod-2 reduction of the index of the family of Dirac operators on the five-dimensional path space.

**Completion of the grading.** The index theorem completes the straightness principle. The grading was: first-order local $=$ unique and canonical; higher-order local $=$ moduli; global $=$ obstructed. The index theorem adds the fourth case: **when the straightening is given in the form of an elliptic operator, the global calculus is not merely obstructed but canonically determined** — the index is the unique, natural, topological invariant of the symbol. The "kind" of global calculus available is read off from the symbol: the symbol is a canonical object (the straightening), and the index is its unique global invariant. The straightness principle, in its final form, is: *the calculus is a local linearization, its uniqueness is graded by order, and its global content — when the straightening is elliptic — is the index, the unique natural topological invariant of the local straightening data.*
