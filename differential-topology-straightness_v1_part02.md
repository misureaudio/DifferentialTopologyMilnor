
---

## 3. Immersions and embeddings: straightening the *map*, not the space

*(Milnor, Ch. 2, §§2.1–2.3.)*

Up to now the straightening has been of the *space*: a chart straightens a neighborhood in $M$. The next move — and the one that most directly answers a physicist's question, "can I put my curved thing into flat space?" — is to straighten a *map*.

**Definition.** A smooth map $f:M^n\to N^m$ is an **immersion** if $df_x$ is injective for every $x\in M$; it is an **embedding** if, in addition, it is a homeomorphism onto its image $f(M)\subset N$.

An immersion says: *at every point, the tangent space of $M$ sits inside the tangent space of $N$ without collapsing.* An embedding says: *and moreover the global picture has no self-intersections.* The distinction is the distinction between "locally straight" and "globally straight": an immersion is a local straightening of the map (the image is locally a submanifold of $N$), while an embedding is a global one (the image is a submanifold everywhere, with no self-contact).

The local content is again a straightening theorem:

**Theorem (local form of an immersion).** If $f:M^n\to N^m$ is an immersion, then for each $x\in M$ there are charts of $M$ and $N$ in which
$$
f(y_1,\dots,y_n) = (y_1,\dots,y_n, 0,\dots,0).
$$
That is, *locally, an immersion is a straight linear inclusion.* The proof is the inverse function theorem applied to a coordinate projection of $f$. So an immersion is, locally, as straight as the word "straight" allows: it is a linear subspace inclusion, up to a re-straightening of source and target.

The global content is where the freedom reappears, and where the moduli live. The **hairy ball theorem** and its relatives show that the re-straightening cannot be done globally in general:

**Theorem (hairy ball).** $S^2$ admits no nonvanishing continuous tangent vector field.

In the language of straightening: there is no global nonvanishing "direction of straightness" on $S^2$. The tangent bundle $TS^2$ is not trivial, so one cannot choose, continuously and everywhere, a parallelization — a global frame in which the manifold looks, in each direction, like $\mathbb{R}^2$. The Euler class $e(TS^2)\in H^2(S^2;\mathbb{Z})\cong\mathbb{Z}$ evaluates to $\pm 2$ (the Euler characteristic), which is the precise obstruction. The straightening exists locally (charts), but the *global frame* in which the manifold would be uniformly straight does not exist. This is the first appearance of the graded-uniqueness theme at the global level: the local straightening is canonical, the global straightening is obstructed, and the obstruction is a characteristic class.

The **embedding** theorems measure how much flat space is needed to straighten a given manifold globally.

**Theorem (Whitney embedding).** Every closed smooth $n$-manifold embeds in $\mathbb{R}^{2n}$, and immerses in $\mathbb{R}^{2n-1}$.

**Theorem (general position / weak Whitney).** For $n\ge 3$, a generic smooth map $M^n\to\mathbb{R}^{2n-1}$ is an immersion, and a generic map $M^n\to\mathbb{R}^{2n}$ is an embedding.

The numbers $2n$ and $2n-1$ are not deep invariants; they are the dimension of the space of jets needed to make self-intersections "generic" and hence removable. What *is* deep is the question of whether a given immersion is *isotopic* to an embedding, and how many embeddings of a fixed isotopy class exist. That is a moduli question, and the moduli are governed by the **Smale–Hirsch theorem**:

**Theorem (Smale–Hirsch).** The map
$$
\{\text{immersions } M^n\to N^m\}/\text{isotopy} \;\longrightarrow\; \{\text{monomorphisms } TM\hookrightarrow TN\}/\text{homotopy}
$$
is a weak homotopy equivalence (for $m>n$).

In words: *an immersion is determined up to isotopy by its linear part — by the bundle monomorphism $df:TM\hookrightarrow f^*TN$.* This is the straightening principle at the level of maps: the higher-order (the actual image) carries no information beyond the first-order (the derivative), as long as one works up to isotopy. The calculus of immersions is, in this sense, a first-order calculus, and it is unique. The moment one asks for the actual geometric image (up to ambient isotopy, or with a fixed metric), the higher-order information reappears, and the moduli open up.

---

## 4. Submanifolds, regular values, and transversality: the straightening that is *defined* by a map

*(Milnor, Ch. 3, §§3.1–3.3; transversality in Ch. 4.)*

A submanifold is the most common object a physicist encounters as "straight inside a curved ambient space": the world-sheet of a string in spacetime, the constraint surface in phase space, the critical manifold of a variational problem. The clean definition is via the **regular value theorem**.

**Theorem (regular value / preimage of a regular value is a submanifold).** Let $f:M^n\to\mathbb{R}^k$ be smooth and $q\in\mathbb{R}^k$ a regular value (i.e., $df_x$ is surjective for every $x\in f^{-1}(q)$). Then $f^{-1}(q)$ is a closed embedded submanifold of $M$ of dimension $n-k$.

The proof is the constant rank theorem: $f$ has constant (maximal) rank on $f^{-1}(q)$, so locally $f$ is a projection, and the preimage of a point is a linear subspace. The submanifold is, locally, *exactly* a straight subspace of $\mathbb{R}^n$. This is the sense in which "submanifold" and "locally straight" are the same notion: a submanifold is a subset that is, in a neighborhood of each of its points, the zero set of a submersion — i.e., a linear subspace up to straightening.

The **Sard theorem** is the analytic heart that makes regular values abundant:

**Theorem (Sard).** The set of critical values of a smooth $f:M^n\to\mathbb{R}^k$ is a Lebesgue null set (in fact, has measure zero in a strong sense).

So for a generic target value, the preimage is a submanifold. In the straightening language: *a generic hyperplane section of a manifold is a straight submanifold.* This is the theorem that justifies, in physics, the practice of "restricting to a generic slice" — for instance, taking a generic time-slice of a field configuration and asserting it is a smooth submanifold of configuration space.

**Transversality** is the relative version, and it is the workhorse of global differential topology.

**Definition.** A map $f:M\to N$ is **transverse** to a submanifold $S\subset N$, written $f\pitchfork S$, if for every $x$ with $f(x)\in S$,
$$
df_x(T_xM) + T_{f(x)}S \;=\; T_{f(x)}N.
$$
In words: the image of the tangent space of $M$ and the tangent space of $S$ together span the ambient tangent space. The map $f$ "meets" $S$ as straightly as possible — not tangentially, but at the maximal angle allowed.

**Theorem (transversality / Thom).** If $f\pitchfork S$, then $f^{-1}(S)$ is a submanifold of $M$ of codimension equal to that of $S$ in $N$. Moreover, the class of maps transverse to a fixed $S$ is dense in $C^\infty(M,N)$ (in the Whitney $C^\infty$ topology).

The density statement is the global straightening result: *a generic map is as straight as possible relative to any prescribed submanifold.* The consequence that makes transversality the engine of the subject is the **Thom transversality theorem**, which says that a generic *family* of maps is transverse to a fixed submanifold of the jet space. This is the theorem behind the existence of generic Morse functions, generic immersions, generic vector fields, and — in physics — behind the assertion that a generic perturbation of a potential has only non-degenerate critical points, so that the critical point set is a discrete, countable, and stably defined object.

The **Morse lemma** is the local straightening of a critical point, and it is the sharpest form of the first-order rigidity:

**Theorem (Morse lemma).** If $f:M^n\to\mathbb{R}$ has a non-degenerate critical point at $p$ (i.e., the Hessian $d^2f_p$ is nondegenerate), then in some chart centered at $p$,
$$
f = -y_1^2 - \cdots - y_k^2 + y_{k+1}^2 + \cdots + y_n^2.
$$
That is, *locally, a non-degenerate critical point is a straight quadratic form, and the only invariant is the index $k$.* The straightening is canonical up to an orthogonal change of coordinates — i.e., up to the action of $O(n)$ on the quadratic form. The higher-order terms of $f$ are *completely invisible* to the local model: the Morse lemma erases them. This is the purest example of the grading: the second-order behavior is canonical (the index), and the third-and-higher-order behavior is irrelevant to the local type.

For a physicist: the Morse lemma is the mathematical content of the *stationary phase* and *saddle point* approximations. The leading term in the asymptotic expansion of
$$
\int e^{i\lambda f(x)}\,a(x)\,dx
$$
as $\lambda\to\infty$ is determined by the Hessian at the critical points — the straight quadratic — and the index $k$ determines the phase factor $e^{i\pi k/2}$. The higher-order terms contribute only to the subleading coefficients. The calculus of asymptotics is, at its leading order, a first-order (well, second-order, in $f$) calculus, and it is unique.

---

## 5. Vector fields, flows, and the uniqueness of the infinitesimal straightening

*(Milnor, Ch. 3, §3.4, and the flow box theorem.)*

A vector field $X$ on $M$ is a choice, for each $p\in M$, of a tangent vector $X_p\in T_pM$, varying smoothly. A vector field is, pointwise, a "direction of straightness": it tells you which direction, at each point, is the preferred direction of motion. The **flow** of $X$ is the family of diffeomorphisms $\{\varphi_t\}_{t\in\mathbb{R}}$ generated by integrating $X$, satisfying $\frac{d}{dt}\varphi_t(p) = X_{\varphi_t(p)}$ and $\varphi_0 = \mathrm{id}$.

The **flow box theorem** is the straightening result for vector fields:

**Theorem (flow box).** Let $X$ be a nonvanishing vector field and $p\in M$. Then there is a chart $\varphi:U\to\mathbb{R}^n$ about $p$ in which $X$ is the constant vector field $\partial/\partial x^1$.

In words: *locally, a nonvanishing vector field is a straight line field, and its flow is straight translation in the $x^1$ direction.* The straightening is unique up to the action of the group of diffeomorphisms that fix the $x^1$-direction — i.e., up to the "vertical" re-straightening of the transverse variables. So the flow is locally as straight as possible, and the only freedom in the straightening is the freedom to reparametrize the transverse coordinates.

The **uniqueness of the flow** is the key fact: given $X$, the flow $\{\varphi_t\}$ is the *unique* one-parameter group of diffeomorphisms with $\varphi_t'(0) = X$. This is the uniqueness theorem for the first-order linear ODE $\dot\gamma = X_\gamma$ with the group constraint. It is the dynamical content of the straightening: the vector field determines the flow, and the flow determines the vector field (as its infinitesimal generator), and this correspondence is bijective. There is no moduli: the flow is the unique "integration" of the straightening.

For a physicist, this is the content of the statement that a Hamiltonian vector field determines a Hamiltonian flow, and that the flow is the unique symplectomorphism group with that generator. The **Liouville equation** and the preservation of the symplectic form (and hence of volume, by the Darboux theorem) are consequences of the straightening being canonical.

The **Darboux theorem** is the symplectic straightening, and it is the sharpest possible uniqueness:

**Theorem (Darboux).** Every $2n$-dimensional symplectic manifold $(M,\omega)$ is, locally, diffeomorphic to $(\mathbb{R}^{2n}, \omega_0 = \sum_{i=1}^n dx^i\wedge dx^{n+i})$.

In words: *locally, every symplectic form is the standard flat form, and the straightening is canonical.* This is the symplectic analogue of the fact that every Riemannian metric is, at a point, the Euclidean metric — but stronger: for the symplectic form, the straightening holds on an open set, not just at a point. The reason is that the symplectic form has no local invariants (no curvature, in the Riemannian sense); its first jet determines it completely. This is the purest form of the first-order rigidity: the symplectic structure is a first-order object, and it is locally unique.

The contrast with the Riemannian case, which I will develop in §8, is the central contrast of the essay: the symplectic straightening is locally unique (no local invariants), while the Riemannian straightening is locally unique only at a point (the curvature is the first local invariant, and it appears at second order).

<!-- CONT -->
