---

## 6. The tangent bundle: the straightening as a *bundle*

*(Milnor, Ch. 4, §§4.1–4.3.)*

So far the straightening has been pointwise: $T_pM$ at each $p$. The **tangent bundle**
$$
TM = \bigsqcup_{p\in M} T_pM, \qquad \pi : TM \to M
$$
is the *total space* of the straightening: it is the manifold that records, over every point of $M$, the whole linear space in which $M$ is straight at that point. $TM$ is itself a smooth $2n$-manifold, and the projection $\pi$ is a submersion whose fiber over $p$ is the linear space $T_pM \cong \mathbb{R}^n$.

The straightening theme now takes a new form: **is $TM$ trivial?** That is, is there a global frame — $n$ everywhere-independent vector fields $X_1,\dots,X_n$ such that $\{X_1(p),\dots,X_n(p)\}$ is a basis of $T_pM$ for every $p$? If so, $TM \cong M \times \mathbb{R}^n$, and the manifold is **parallelizable**: it is, globally, as straight as a product. The answer is the first major global straightening theorem, and it is a theorem about *dimensions*:

**Theorem (Adams, 1962).** $S^n$ is parallelizable if and only if $n \in \{0,1,3,7\}$.

The proof uses the $K$-theory of the Hopf fibration and the fact that a parallelization of $S^n$ is equivalent to the existence of $n$ linearly independent vector fields on $S^n$; the answer is read off from the Hopf invariant, which is non-zero only in dimensions $1,3,7$ (the dimensions of the normed division algebras $\mathbb{R},\mathbb{C},\mathbb{H},\mathbb{O}$). The straightening of the sphere is global if and only if the sphere is one of the three Hopf spheres. This is the sharpest possible statement of the theme at the global level: *the kind of global straightening a space admits is a function of its dimension, and the function is as rigid as the existence of division algebras.*

The **Euler class** and the **Pontryagin classes** are the obstructions to parallelization in general. For an oriented rank-$n$ bundle $E\to M$, the Euler class $e(E)\in H^n(M;\mathbb{Z})$ is the obstruction to the existence of a nonvanishing section; the Pontryagin classes $p_i(E)\in H^{4i}(M;\mathbb{Z})$ are the obstructions to the existence of a complex structure on the real bundle. These are the invariants that measure, in cohomology, the failure of the global straightening. For a physicist: the Euler class of $TS^2$ is the index of the Riemann–Roch formula for the Hopf line bundle, and the Pontryagin classes are the indices that appear in the anomaly polynomial of gauge theory.

The **tangent bundle of a product** is the model case: if $M = M_1 \times M_2$, then $TM = TM_1 \times TM_2$ (pulled back to the product), and the straightening of the product is the product of the straightenings. This is why the calculus on a product is the tensor product of the calculi on the factors: the de Rham complex satisfies $\Omega^\bullet(M_1\times M_2) \cong \Omega^\bullet(M_1)\otimes \Omega^\bullet(M_2)$, and the Euler characteristic is multiplicative, $\chi(M_1\times M_2) = \chi(M_1)\chi(M_2)$.

---

## 7. Transversality and jets: the straightening, and its *failure to be unique*, measured by the jet

*(Milnor, Ch. 4, §4.4; the jet bundle, §7 of the present essay.)*

The **$k$-jet** of a smooth function $f:M\to\mathbb{R}$ at a point $p$ is the equivalence class of $f$ under the relation "agree up to order $k$ at $p$." Formally,
$$
j^k_p f \;=\; f \big/ \mathfrak{m}_p^{\,k+1},
$$
the image of $f$ in the quotient of the ring of germs by the $(k+1)$-st power of the maximal ideal. The $1$-jet is the tangent space (up to dualization); the $2$-jet is the Hessian (plus the gradient); and so on.

The **jet bundle** $J^k(M,\mathbb{R})$ is the bundle whose fiber over $p$ is the space of $k$-jets at $p$. It is a finite-dimensional vector bundle of rank $\binom{n+k}{k}$, and the **jet prolongation** $j^k : M \to J^k(M,\mathbb{R})$ is a smooth section. The **Thom transversality theorem**, in its full form, says that a generic function has a $k$-jet section that is transverse to the subbundle of degenerate jets — i.e., a generic function has non-degenerate critical points (for $k=2$), and more generally a generic function has a $k$-jet that avoids a prescribed submanifold of the jet bundle.

The **non-uniqueness of the higher-order straightening** is now precise. The $1$-jet of $f$ at $p$ is a single point of $T_p^*M$; it is unique, canonical, and determined by the germ of $f$. The $2$-jet of $f$ at $p$ is a point of the symmetric square $S^2 T_p^*M \oplus T_p^*M$; it is *not* determined by the $1$-jet, and two functions with the same $1$-jet can have different $2$-jets. The $k$-jet for $k\ge 2$ is a *genuine invariant* of the germ, and the space of $k$-jets is a *moduli space* of higher-order straightenings.

This is the precise sense in which the calculus is "graded": the $1$-jet is a point (unique), the $2$-jet is a vector (a choice of quadratic form), and the $k$-jet for $k\ge 3$ is a tensor of rank $k$ (a choice of $k$-linear form). The higher the order, the more freedom, and the more the moduli space grows. The **formal inverse** of a function (the inverse of its Taylor series) is a formal power series in the $k$-jets, and it is unique as a formal object — but it is not determined by any finite jet, and it does not always converge. The higher-order straightening is *formally* unique (the formal inverse is unique) but *not analytically* unique (the convergent inverse is not determined by any finite jet).

The **Morse–Bott theorem** is the higher-order generalization of the Morse lemma, and it makes the grading explicit:

**Theorem (Morse–Bott).** If $f:M\to\mathbb{R}$ has a critical submanifold $C$ (i.e., the set of critical points is a submanifold, and the Hessian is nondegenerate in the normal directions), then in a tubular neighborhood of $C$,
$$
f = f|_C + \sum_{i=1}^k y_i^2 - \sum_{j=1}^{k'} z_j^2,
$$
where the $y_i$ are normal coordinates and the $z_j$ are also normal coordinates. The only invariant is the index $k'$ of the normal Hessian. The higher-order terms are again invisible: the Morse–Bott lemma erases them, and the local model is a straight quadratic form on the normal bundle.

The **Morse index** and the **Morse homology** are the global invariants built from the higher-order straightening. The Morse homology $MH_*(M)$ is the homology of the chain complex generated by the critical points of a generic Morse function $f$, with differential counting the gradient flow lines between critical points of adjacent index. The **Morse–Weyl theorem** says that $MH_*(M) \cong H_*(M;\mathbb{Z})$ (for a generic $f$). This is the global straightening result: the higher-order calculus (the Morse complex) computes the same thing as the global topology (the singular homology), and the straightening is canonical up to chain homotopy.

For a physicist, this is the mathematical content of the *instanton* and *bounce* calculations in quantum field theory: the leading contribution to the path integral comes from the critical points of the action (the classical solutions), and the index of the Hessian (the number of negative modes) determines the fermion determinant and the $\theta$-angle dependence. The higher-order terms (the fluctuations around the classical solution) contribute to the prefactor, but the leading order is determined by the straight quadratic model.

<!-- CONT -->
