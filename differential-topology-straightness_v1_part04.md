
---

## 8. Connections, curvature, and the uniqueness of the Levi-Civita connection: the second-order straightening

*(Beyond Milnor; the chapter the 1965 book leaves implicit.)*

Milnor's book stops at the level of the tangent bundle and the jet bundle. But the straightening theme demands one more chapter, because it is the chapter that answers the physicist's most direct question: *given a metric, is the connection unique?* The answer is **yes, at the level of the connection, and no, at the level of the metric**, and the distinction is the sharpest possible statement of the grading.

**Definition.** A **connection** on a vector bundle $E\to M$ is a $\mathbb{R}$-linear map $\nabla : \Gamma(E)\to \Gamma(T^*M\otimes E)$ satisfying the Leibniz rule $\nabla(fs) = df\otimes s + f\nabla s$. In a local frame, $\nabla$ is given by a $1$-form with values in the Lie algebra of the structure group: $\nabla = d + A$, where $A\in \Omega^1(M;\mathfrak{g})$ is the **connection form**.

The **space of connections** on a fixed bundle $E$ is an affine space modeled on $\Omega^1(M;\mathrm{ad}\,E)$. That is, there is no canonical connection: the connections are in bijection with $\Omega^1(M;\mathrm{ad}\,E)$, which is an infinite-dimensional vector space. The straightening at the level of the connection is *not unique*: there is a moduli space of connections, and the moduli space is the affine space of $\mathfrak{g}$-valued $1$-forms.

But now impose a metric. Let $(M,g)$ be a Riemannian (or pseudo-Riemannian) manifold. A connection $\nabla$ is **metric-compatible** if $\nabla g = 0$ (i.e., the connection preserves the metric: $\nabla_X g(Y,Z) = g(\nabla_X Y, Z) + g(Y, \nabla_X Z)$). A connection is **torsion-free** if $\nabla_X Y - \nabla_Y X = [X,Y]$ (i.e., the connection is symmetric in its arguments).

**Theorem (Levi-Civita).** There is a **unique** connection on $TM$ that is both metric-compatible and torsion-free. It is given, in local coordinates, by the **Christoffel symbols**
$$
\Gamma^k_{ij} = \frac{1}{2}\,g^{k\ell}\big( \partial_i g_{j\ell} + \partial_j g_{i\ell} - \partial_\ell g_{ij} \big).
$$
The proof is a direct computation: the two conditions (metric-compatibility and torsion-freeness) give two linear equations for the three unknowns $\Gamma^k_{ij}$, $\Gamma^k_{ji}$, and the antisymmetric part of $\Gamma^k_{ij}$, and the unique solution is the Christoffel formula. The straightening is unique: *given the metric, there is exactly one connection that straightens the manifold in the metric sense (parallel transport preserves lengths and angles) and the symmetry sense (no torsion).*

This is the central uniqueness theorem of the essay, and it is the answer to the physicist's question. The **Riemannian metric** is a choice (a section of $S^2 T^*M$), and the space of metrics is an infinite-dimensional convex cone. But **given a metric, the connection is unique**: the Levi-Civita connection is the unique metric-compatible, torsion-free connection. The straightening at the level of the connection is canonical, once the metric is fixed. The freedom has moved up one level: it is not in the connection (which is unique) but in the metric (which is a moduli space).

The **curvature** $R^\nabla \in \Omega^2(M;\mathrm{End}(TM))$ is the obstruction to the connection being flat, and it is the first non-vanishing local invariant of the metric, appearing at second order. In a normal coordinate system at a point $p$ (geodesic coordinates), $g_{ij}(p) = \delta_{ij}$ and $\Gamma^k_{ij}(p) = 0$, but $\partial_k g_{ij}(p) = 0$ while $\partial_k\partial_\ell g_{ij}(p) \neq 0$ in general, and the curvature is
$$
R^i_{\,jkl}(p) = \partial_k \Gamma^i_{jl}(p) - \partial_l \Gamma^i_{jk}(p) + \Gamma^i_{mk}(p)\Gamma^m_{jl}(p) - \Gamma^i_{ml}(p)\Gamma^m_{jk}(p) = \partial_k\partial_l g_{jk}(p) - \partial_k\partial_j g_{lk}(p) + \cdots.
$$
The curvature is a second-order invariant: it is invisible to the first jet of $g$ (which is zero at $p$ in normal coordinates), but visible to the second jet. This is the Riemannian analogue of the symplectic contrast: the symplectic form has no local invariants (its first jet determines it), while the Riemannian metric has local invariants starting at second order (the curvature). The straightening of the Riemannian manifold is unique at a point (the metric is Euclidean, the connection is flat, in normal coordinates), but not on an open set (the curvature is the obstruction).

The **Ricci tensor** and the **scalar curvature** are the contractions of the curvature, and they are the invariants that appear in the Einstein–Hilbert action
$$
S_{\mathrm{EH}}[g] = \int_M R\,\mathrm{vol}_g.
$$
The **Einstein equations** $G_{ij} + \Lambda g_{ij} = 8\pi T_{ij}$ are the critical point equations of this action, and they are, in the language of the straightening, the equations that the metric must satisfy for the straightening to be "as flat as possible" in the presence of matter. The uniqueness of the Levi-Civita connection is the mathematical content of the statement that *given the metric, the geodesics are unique*: the straight lines of the curved space are the geodesics of the unique connection, and they are the unique curves that are "as straight as possible" in the metric sense.

The **Nash embedding theorem** is the global straightening result for Riemannian manifolds:

**Theorem (Nash, 1956, $C^k$; 1965, $C^\infty$ via Nash–Moser).** Every $n$-dimensional Riemannian manifold $(M,g)$ is isometrically embeddable in $\mathbb{R}^N$ for $N$ sufficiently large. Nash's original $1956$ result gives a $C^k$ isometric embedding ($k\ge 1$) for $N = n(3n+11)/2$, and his $1965$ $C^\infty$ result (which requires the Nash–Moser method, §10) achieves the same dimension $N = n(3n+11)/2$ in the $C^\infty$ category. (Improved, and in some regimes optimal, bounds are known, but the precise sharp value of $N$ for $C^\infty$ isometric embedding is a separate and largely open question.)

In words: *every curved space can be straightened, globally, by embedding it in a sufficiently high-dimensional flat space.* The isometric embedding is the global straightening: the metric $g$ is the restriction of the Euclidean metric on $\mathbb{R}^N$ to the image of $M$. The straightening is unique up to rigid motions of $\mathbb{R}^N$ (the isometry group), but the embedding itself is not unique: there are many isometric embeddings of the same $(M,g)$ into $\mathbb{R}^N$, and the moduli space of embeddings is a genuine moduli space. The $C^\infty$ case requires the Nash–Moser method, which I will describe in §10.

The **Bianchi identities** $\nabla_{[a} R_{bc]de} = 0$ and $\nabla^a R_{abcd} = \nabla_c R_{bd} - \nabla_d R_{bc}$ are the integrability conditions for the curvature, and they are the statement that the curvature is "the derivative of the connection" in a sense that is compatible with the Leibniz rule. They are the higher-order integrability conditions that the straightening must satisfy, and they are the reason the curvature is a tensor (coordinate-independent) rather than just a collection of coordinate-dependent quantities.

<!-- CONT -->
