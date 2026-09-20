
---

## 9. The non-uniqueness of the smooth structure: exotic $\mathbb{R}^4$ and the exotic spheres

*(Beyond Milnor; the chapter the 1965 book cannot contain.)*

Milnor's book is written in the $C^\infty$ category, and it assumes that the smooth structure on $\mathbb{R}^n$ is unique. This is true for $n \neq 4$, and it is **false** for $n = 4$. The failure of uniqueness in dimension four is the most dramatic and most mysterious of all the non-uniqueness results in differential topology, and it is the result that most directly answers the question "is the straightening unique?" with a resounding **no, in dimension four**.

**Definition.** A **smooth structure** on a topological $n$-manifold $M$ is an equivalence class of $C^\infty$ atlases, where two atlases are equivalent if the union is a smooth atlas. Two smooth structures on the same topological manifold are **exotic** if they are not diffeomorphic (even though they are homeomorphic).

**Theorem (Mazur, 1966; Freedman, 1982; Donaldson, 1983).** There exist exotic $\mathbb{R}^4$'s: smooth structures on the topological $4$-manifold $\mathbb{R}^4$ that are not diffeomorphic to the standard $\mathbb{R}^4$. Moreover, there are **uncountably many** such structures.

The construction of an exotic $\mathbb{R}^4$ proceeds as follows. Mazur constructed a compact contractible $4$-manifold $W$ (the **Mazur manifold**) with $\partial W$ a homology $3$-sphere that is not simply connected. The interior of $W$ is diffeomorphic to $\mathbb{R}^4$ minus a point. But the boundary $\partial W$ is not $S^3$, so $W$ cannot be the standard $4$-ball $B^4$. Gluing a copy of $B^4$ to $W$ along $\partial W$ (via a homeomorphism, which exists by the h-cobordism theorem in dimension $3$) gives a smooth structure on $\mathbb{R}^4$ that is not the standard one. The non-diffeomorphism is detected by the **Donaldson invariants** (for definite $4$-manifolds) or by the **Seiberg–Witten invariants** (for general $4$-manifolds), which are sensitive to the smooth structure and not to the homeomorphism type.

The **uncountability** comes from the fact that the set of exotic $\mathbb{R}^4$'s can be constructed by "small" modifications of the standard structure in arbitrarily small regions, and the set of such modifications is uncountable (parameterized by a subset of the space of embeddings of a $4$-ball into $\mathbb{R}^4$, which is uncountable). This is in stark contrast to $n\neq 4$: for $n\le 3$, the smooth structure on $\mathbb{R}^n$ is unique (the $n=3$ case is the Poincaré conjecture, proved by Perelman in 2003), and for $n\ge 5$, the smooth structure on $\mathbb{R}^n$ is unique by the $h$-cobordism theorem.

The **exotic spheres** are the higher-dimensional analogue, and they are the first example of non-uniqueness in the smooth category that Milnor himself discovered:

**Theorem (Milnor, 1956).** There exist smooth $7$-spheres that are not diffeomorphic to the standard $S^7$. In fact, the group $\Theta_7$ of diffeomorphism classes of smooth $7$-spheres (under connected sum) is isomorphic to $\mathbb{Z}/28\mathbb{Z}$.

Milnor's construction uses the **Hopf fibration** $S^3 \to S^7 \to S^4$ and the fact that the tangent bundle of $S^7$ is trivial (since $7\in\{0,1,3,7\}$). More generally, the exotic $7$-spheres arise as the total spaces of $S^3$-bundles over $S^4$; such bundles are classified by $\pi_3(SO(4)) \cong \mathbb{Z}\oplus\mathbb{Z}$, and the total spaces that are homotopy $7$-spheres fall into exactly $28$ diffeomorphism classes, distinguished by the **Euler number** of the bundle (equivalently, by the Milnor invariant $\mu$, a smooth invariant invisible to the homeomorphism type). The group $\Theta_7$ of diffeomorphism classes of smooth $7$-spheres under connected sum is $\mathbb{Z}/28\mathbb{Z}$. The group $\Theta_n$ of exotic $n$-spheres is finite for $n\ge 5$ (its order is known for many $n$), and it vanishes in the sense that $\mathbb{R}^n$ has a unique smooth structure for $n\neq 4$ — but the $n=4$ case is the exception, and the exception is uncountable.

The **$4$-dimensional Poincaré conjecture** (proved by Freedman in 1982, in the topological category) says that every simply-connected closed topological $4$-manifold homeomorphic to $S^4$ is homeomorphic to $S^4$. But the **smooth** $4$-dimensional Poincaré conjecture — that every simply-connected closed smooth $4$-manifold homeomorphic to $S^4$ is *diffeomorphic* to $S^4$ — is **open**. This is the single most important open problem in $4$-dimensional differential topology, and it is a direct question about the uniqueness of the straightening: *is the smooth structure on $S^4$ unique?* The existence of exotic $\mathbb{R}^4$'s suggests the answer is no, but a proof is lacking.

For a physicist, the relevance is direct: the **instanton number** in Yang–Mills theory on $\mathbb{R}^4$ is a topological invariant (the second Chern class of the associated bundle), and it is sensitive to the smooth structure. The existence of exotic $\mathbb{R}^4$'s means that the instanton moduli space depends on the smooth structure of the base, and the **Donaldson invariants** of a $4$-manifold are, in physics, the partition function of the $\mathcal{N}=2$ supersymmetric Yang–Mills theory on that $4$-manifold (Witten's interpretation, 1994). The non-uniqueness of the smooth structure is, in physics, the non-uniqueness of the vacuum structure of the gauge theory on the same topological manifold.

<!-- CONT -->
