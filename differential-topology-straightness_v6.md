# The Straightness of the Calculus

## Differential Topology after Milnor, and the Uniqueness of the Infinitesimal

*An essay for mathematical physicists and analysts*

> **On the plan.** This essay is organized around the classical local theory of smooth manifolds, following the architecture of John Milnor's *Topology from the Differentiable Viewpoint* (University Press of Virginia, 1965; Princeton University Press reprint, 1997). Milnor's book treats smooth manifolds and smooth maps, tangent spaces and derivatives, regular values and the Sard–Brown theorem, the degree mod 2, oriented manifolds and the Brouwer degree, vector fields and the Euler number, and framed cobordism and the Hopf theorem. It does **not** treat flows, jets, general transversality, Whitney embedding, or Smale–Hirsch; for those I follow Hirsch, *Differential Topology*, and Lee, *Introduction to Smooth Manifolds*, and cite them below where they are used. The essay's chapters are: differentiable maps and the tangent space (§1), the inverse function theorem (§2), immersions and embeddings (§3), submanifolds, regular values, and transversality (§4), vector fields, flows, and Darboux's theorem (§5), the tangent bundle (§6), transversality and jets (§7), connections, curvature, and the Levi-Civita connection (§8), the non-uniqueness of the smooth structure — exotic $\mathbb{R}^4$ and the exotic spheres (§9), the failure, then repair, of the straightening in infinite dimensions — the Banach and Fréchet inverse function theorems and the Nash–Moser method (§10), and the Atiyah–Singer index theorem as the global counterpart of the straightening principle (§11). A single idea runs through the whole: *the calculus is what remains when the manifold is straightened, and the question of which calculi exist, and which of them are unique, is precisely the question of how much of the straightening is canonical.*

### Abstract

The differential calculus on a smooth manifold is a local linearization: a chart "straightens" the manifold to $\mathbb{R}^n$, and the tangent space, the exterior derivative, and the Lie derivative are the invariants of that straightening. This essay argues that the notion of *straightness* — the existence of a local affine model — is the organizing principle of differential topology, and that its consequences amount to a taxonomy of the possible calculi together with a precise accounting of which of them are unique (canonical) and which are not.

The first-order calculus is unique: the tangent space is the same object whether defined as equivalence classes of curves or as derivations, and the Fréchet derivative is the unique best linear approximation to a map at a point. The higher-order calculus is not unique: the $k$-jet for $k\ge 2$ is not determined by the $1$-jet, and the spaces of connections and of metrics are affine or convex spaces of choices; the corresponding moduli spaces are their quotients by the gauge group or by $\mathrm{Diff}(M)$. The global calculus is obstructed: the tangent bundle $TS^n$ is trivial if and only if $n\in\{0,1,3,7\}$ (Bott–Milnor, Kervaire, Adams); for general manifolds parallelizability depends on the manifold, not only on its dimension — tori, Lie groups and orientable $3$-manifolds are all parallelizable. The smooth structure on $\mathbb{R}^n$ is unique for $n\neq 4$ but is *not* unique in dimension $4$, where there are uncountably many exotic $\mathbb{R}^4$'s. In infinite dimensions the straightening succeeds in Banach spaces (the inverse function theorem) but fails in Fréchet spaces, and is repaired by the Nash–Moser implicit function theorem — the method behind the $C^\infty$ Nash isometric embedding theorem and the KAM theory. We close with a table of calculi and their uniqueness, and with the observation that straightness is, in the end, the notion of a local linear model, and that the "kind" of calculus a space admits is read off from how rigidly that model is determined.

---

## 0. Introduction: what "straight" means, and why it is load-bearing

A physicist who computes in flat spacetime is, without meaning to, doing differential topology. The statement "the electron follows a straight line between interactions" is an assertion about the *affine* structure of Minkowski space: there is a family of preferred curves (the geodesics of the flat connection) such that the first-order Taylor expansion of any curve about a point agrees with a linear map. The whole machinery of perturbation theory — expand about a background, keep the linear term, treat the rest as a correction — is the assertion that **locally, to first order, the world is straight**.

Differential topology is the study of what survives, and what is lost, when one tries to make that assertion on a space that is not globally straight. A smooth $n$-manifold $M$ is, by definition, a space that is *locally* $\mathbb{R}^n$ in a controlled sense: there is an atlas of charts
$$
\varphi_\alpha : U_\alpha \hookrightarrow \mathbb{R}^n, \qquad U_\alpha \subset M,
$$
such that the transition maps $\varphi_\beta \circ \varphi_\alpha^{-1}$ are diffeomorphisms of open subsets of $\mathbb{R}^n$. A chart is a *straightening*: it replaces the curved $U_\alpha$ by a flat patch of $\mathbb{R}^n$. The word "diffeomorphism" does all the work — it says that the way two different straightenings agree is itself smooth, so that "straightness" is not an artifact of a particular chart but a property of the *system* of charts.

From this single sentence, three questions follow, and they are the questions of this essay:

1. **Existence.** Does a given space admit a straightening at all? (Smooth structures, embeddings, the isometric embedding problem.)
2. **Uniqueness.** If it admits one, is it unique — canonical, independent of choices? (The tangent space, the derivative, the flow, the Levi-Civita connection, the smooth structure of $\mathbb{R}^n$.)
3. **Obstruction.** If it does not admit one, or admits many, what measures the failure, or the freedom? (Characteristic classes, the hairy ball, exotic structures, moduli spaces.)

The surprising and, I want to argue, central fact is that the answer to (2) is *graded by order*. The **first-order** straightening is rigid: there is exactly one, and it is canonical. The **higher-order** straightening is flexible: there are many, and they form moduli spaces. And the **global** straightening is obstructed: it exists only in special dimensions, and in dimension four it exists in an uncountable family of mutually incompatible forms. The "kind" of calculus available on a space, and its uniqueness, is read off from this grading.

I will return to each of these. But first, the local theory.

---

## 1. The local straightening: differentiable maps and the tangent space

*(Milnor, Ch. 1, "Tangent spaces and derivatives"; the algebraic account of $T_p^*M$ and the uniqueness of the Lie derivative follow Lee, *Introduction to Smooth Manifolds*.)*

Let $M$ be a smooth $n$-manifold and $p \in M$. There are two standard definitions of the tangent space $T_pM$, and the fact that they agree is the first and most important uniqueness theorem of the subject.

**Definition by curves.** A tangent vector at $p$ is the equivalence class of a smooth curve $\gamma : (-\varepsilon,\varepsilon)\to M$ with $\gamma(0)=p$, where $\gamma \sim \gamma'$ if, for (equivalently, for every) chart $\varphi$ about $p$,
$$
\frac{d}{dt}\Big|_{t=0}\, \varphi(\gamma(t)) \;=\; \frac{d}{dt}\Big|_{t=0}\, \varphi(\gamma'(t)).
$$
The equivalence is well-defined precisely because the transition maps are diffeomorphisms: if the two curves agree to first order in one chart, the chain rule forces them to agree in every chart. The straightening has defined an equivalence relation on curves, and the relation is independent of the straightening.

**Definition by derivations.** A tangent vector at $p$ is a linear map $D : C^\infty(M)\to \mathbb{R}$ satisfying the Leibniz rule
$$
D(fg) = D(f)\,g(p) + f(p)\,D(g).
$$
The space of such derivations is a real vector space, and the map
$$
[\gamma] \longmapsto \big( f \mapsto \tfrac{d}{dt}\big|_{t=0} f(\gamma(t)) \big)
$$
is a linear isomorphism $T_pM \cong \mathrm{Der}_p(C^\infty(M))$. No choice of chart enters the second definition at all, which is why this is the definition a functional analyst reaches for: a tangent vector is a *continuous derivation* on the commutative algebra of smooth functions.

There is a third, purely algebraic, definition that makes the uniqueness transparent. Let $\mathfrak{m}_p \subset C^\infty_p(M)$ be the maximal ideal of germs of smooth functions vanishing at $p$. Then
$$
T_p^*M \;\cong\; \mathfrak{m}_p / \mathfrak{m}_p^{\,2},
$$
and $T_pM \cong (\mathfrak{m}_p/\mathfrak{m}_p^{2})^{*}$ is its dual. The quotient $\mathfrak{m}_p/\mathfrak{m}_p^2$ is the **first-order neighborhood** of $p$ in the algebraic sense: it is what remains of the ring of functions once one throws away everything of order $\ge 2$. That this quotient is independent of any analytic input — no metric, no connection, no chart — is the algebraic content of the statement that *the first-order structure is canonical*.

**The derivative as unique best linear approximation.** Let $f : M \to N$ be smooth and $p\in M$. The differential $df_p : T_pM \to T_{f(p)}N$ is characterized by the following uniqueness property: it is the **unique** linear map $L : T_pM \to T_{f(p)}N$ such that, in charts,
$$
f(p+h) = f(p) + L h + o(\|h\|) \qquad (h\to 0).
$$
This is the Fréchet characterization. The point for our theme is the word *unique*. Given the straightening (a pair of charts), the first-order behavior of $f$ is captured by exactly one linear map. There is no choice, no moduli, no moduli space: the linear part of the Taylor expansion is a **functor** of the straightening, and the chain rule
$$
d(g\circ f)_p = dg_{f(p)} \circ df_p
$$
says that $(M,f)\mapsto(TM,df)$ is a functor. The first-order calculus is canonical, and there is only one of it.

Two consequences are worth isolating.

- **The exterior derivative.** The $1$-form $df$ on $M$ (for $f:M\to\mathbb{R}$) is the pullback of the standard $1$-form $dx$ on $\mathbb{R}$ under the straightening. Its coordinate-free definition, $df_p(v) = D_v f$ for $v\in T_pM$, is chart-independent for the same reason the tangent space is: it is a first-order object, and first-order objects are canonical. The full de Rham complex $\Omega^\bullet(M)$, built from $df$ by alternation, is therefore a canonical first-order calculus. This is the calculus that a physicist uses when writing $dA = F$ for a gauge potential $A$: the $d$ is the unique antiderivation of degree $+1$ on $\Omega^\bullet(M)$ that agrees with the differential on functions **and satisfies $d^2=0$**. ($d^2=0$ does not follow from the other two properties: $D\alpha = d\alpha + \theta\wedge\alpha$ for a fixed $2$-form $\theta$ is again a degree-$+1$ antiderivation agreeing with $d$ on functions, but $(D^2)\alpha = 2\,d\theta\wedge\alpha$ in general, so $D^2\neq 0$ unless $\theta$ is closed.) (The phrase "antisymmetric first-order operator with $d^2=0$" does not determine $d$, since $\lambda d$ also satisfies it.)

- **The Lie derivative.** For a vector field $X$ and a tensor field $T$, the Lie derivative $\mathcal{L}_X T$ is the infinitesimal action of the flow of $X$ on $T$. It is again a first-order object: it depends on $X$ and $T$ only through their values and first derivatives at a point. Its uniqueness is the statement that $\mathcal{L}_X$ is the unique derivation of the tensor algebra that commutes with contractions, satisfies $\mathcal{L}_X f = Xf$ on functions, and satisfies $\mathcal{L}_X Y = [X,Y]$ on vector fields. Without the last condition any covariant derivative $\nabla_X$ meets the other requirements. The Lie derivative is, in this sense, the unique "infinitesimal straightening of the frame" generated by $X$.

So at the local, first-order level, the straightening is rigid. Every object one can define — $T_pM$, $T_p^*M$, $\Omega^\bullet(M)$, $\mathcal{L}_X$, the differential — is canonical, independent of the chart, and unique. We shall use the slogan: *the calculus at first order is the calculus, not a calculus* — a slogan, not a theorem, but one that the rest of the essay makes precise.

---

## 2. The inverse function theorem: local straightening, and its uniqueness up to higher order

*(The classical inverse function theorem, with a contraction-mapping proof; see Rudin, Dieudonné, or Lee. Milnor's book does not prove it.)*

The inverse function theorem is the engine that turns the *definition* of a manifold into a *theorem* about it, and it is where the "uniqueness up to higher order" theme first appears.

**Theorem (inverse function theorem).** Let $f: U\subset\mathbb{R}^n \to \mathbb{R}^n$ be $C^1$, and suppose $Df(p)$ is invertible. Then there are neighborhoods $V\ni p$ and $W\ni f(p)$ such that $f|_V : V \xrightarrow{\;\sim\;} W$ is a $C^1$ diffeomorphism.

The standard proof is a contraction-mapping argument (see Rudin, Dieudonné, or Lee), and it shows something stronger than the statement: the inverse is constructed explicitly, and its first derivative is
$$
D(f^{-1})_{f(p)} = (Df_p)^{-1}.
$$
More generally, the $k$-jet of $f^{-1}$ at $f(p)$ is determined by the $k$-jet of $f$ at $p$ (formal inversion of the Taylor series). What finite jets do **not** determine is the germ itself (for a $C^\infty$ non-analytic $f$): the germ of $f$ is not recoverable from any finite jet, so neither is the germ of $f^{-1}$. If $f$ is real-analytic or holomorphic, then $f^{-1}$ is analytic and its Taylor series converges to it. The straightening is unique to first order, and only *formally* unique to higher order.

This is the germ of the theme. Let me state it as a principle that will recur:

> **Principle (grading by order).** First derivatives of a map between manifolds are canonical: $df$ is a bundle map $TM\to f^*TN$. Higher derivatives are not canonical as tensors: $k$-jets transform non-linearly under coordinate changes, and splitting them requires extra structure, such as a connection. Canonical exceptions occur at special loci, for example the Hessian at a critical point.

The **constant rank theorem** is the inverse function theorem with the invertibility hypothesis weakened to a constant-rank hypothesis, and it is the workhorse that produces submanifolds.

**Theorem (constant rank).** If $f:U\subset\mathbb{R}^n\to\mathbb{R}^m$ has constant rank $r$ near $p$, then there are coordinates in which
$$
f(x_1,\dots,x_n) = (x_1,\dots,x_r,0,\dots,0).
$$
In words: *locally, a constant-rank map is straight.* This is the strongest local form of the theme. A map of constant rank is, after a change of coordinates on source and target (i.e., after re-straightening), exactly a projection. What the theorem does not say — and what the rest of the essay is about — is that the re-straightening is not unique, and that the failure of global straightness is measured by invariants (curvature, characteristic classes) that are invisible to the constant rank theorem.

The inverse function theorem has a global cousin that a functional analyst will recognize: a proper local diffeomorphism between connected manifolds is a covering map, and if the target is simply connected it is a diffeomorphism. Properness implies the covering property, and the two are not equivalent. The moral is the same: local straightening, plus a global topological hypothesis (properness, simply-connectedness of the target), upgrades to global straightening. The gap between the local and the global is exactly the gap that characteristic classes measure.

---

## 3. Immersions and embeddings: straightening the *map*, not the space

*(Hirsch, *Differential Topology*; Lee, *Introduction to Smooth Manifolds*; Smale–Hirsch: Hirsch, "Immersions of manifolds," Trans. AMS 93 (1959).)*

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

**Theorem (Whitney embedding).** Every smooth $n$-manifold (closed or not) embeds in $\mathbb{R}^{2n}$, and immerses in $\mathbb{R}^{2n-1}$ for $n>1$.

**Theorem (general position / weak Whitney).** For a generic smooth map $M^n\to\mathbb{R}^m$ the rank-deficient locus has codimension $m-n+1$ in $M$, and double points have expected dimension $2n-m$. Hence a generic map is an immersion for $m\ge 2n$ and an embedding for $m\ge 2n+1$ (with $M$ compact). Generic maps $M^n\to\mathbb{R}^{2n-1}$ have Whitney-umbrella singularities. The numbers $2n$ and $2n+1$ come from this dimension count, not from "the dimension of the space of jets".

What *is* deep is the question of whether a given immersion is *regular-homotopic* to an embedding, and how many embeddings of a fixed isotopy class exist. That is a moduli question, and the moduli are governed by the **Smale–Hirsch theorem**:

**Theorem (Smale–Hirsch).** For $m>n$, or $M$ open, the map
$$
\mathrm{Imm}(M,N)\;\longrightarrow\;\mathrm{Mono}(TM,TN),\qquad f\mapsto df,
$$
is a weak homotopy equivalence. In particular immersions up to *regular homotopy*, not isotopy, correspond to bundle monomorphisms up to homotopy.

In words: *an immersion is determined up to regular homotopy by its linear part — by the bundle monomorphism $df:TM\hookrightarrow f^*TN$.* This is the straightening principle at the level of maps: the higher-order (the actual image) carries no information beyond the first-order (the derivative), as long as one works up to regular homotopy. The calculus of immersions is, in this sense, a first-order calculus, and it is unique. The moment one asks for the actual geometric image (up to ambient isotopy, or with a fixed metric), the higher-order information reappears, and the moduli open up.

Isotopy classes of embeddings are *not* determined by $df$: knots in $S^3$ are the standard example. Two embedded circles with the same derivative data (a bundle monomorphism, unique up to homotopy) can be knotted differently. This is why the table in §12 lists embeddings as "not unique", with knotting as the freedom.

---

## 4. Submanifolds, regular values, and transversality: the straightening that is *defined* by a map

*(Milnor, Ch. 1, "Regular values"; transversality in Hirsch, *Differential Topology*, and Lee, *Introduction to Smooth Manifolds*.)*

A submanifold is the most common object a physicist encounters as "straight inside a curved ambient space": the world-sheet of a string in spacetime, the constraint surface in phase space, the critical manifold of a variational problem. The clean definition is via the **regular value theorem**.

**Theorem (regular value / preimage of a regular value is a submanifold).** Let $f:M^n\to\mathbb{R}^k$ be smooth and $q\in\mathbb{R}^k$ a regular value (i.e., $df_x$ is surjective for every $x\in f^{-1}(q)$). Then $f^{-1}(q)$ is a closed embedded submanifold of $M$ of dimension $n-k$.

The proof is the constant rank theorem: $f$ has constant (maximal) rank on $f^{-1}(q)$, so locally $f$ is a projection, and the preimage of a point is a linear subspace. The submanifold is, locally, *exactly* a straight subspace of $\mathbb{R}^n$. This is the sense in which "submanifold" and "locally straight" are the same notion: a submanifold is a subset that is, in a neighborhood of each of its points, the zero set of a submersion — i.e., a linear subspace up to straightening.

The **Sard theorem** is the analytic heart that makes regular values abundant:

**Theorem (Sard).** For a smooth $f:M^n\to\mathbb{R}^k$, for almost every $c\in\mathbb{R}^k$, $f^{-1}(c)$ is a smooth submanifold of dimension $n-k$.

So for a generic target value, the preimage is a submanifold. In the straightening language: *a generic level set of a map is a straight submanifold.* This is the theorem that justifies, in physics, the practice of "restricting to a generic slice" — for instance, taking a generic time-slice of a field configuration and asserting it is a smooth submanifold of configuration space.

**Transversality** is the relative version, and it is the workhorse of global differential topology.

**Definition.** A map $f:M\to N$ is **transverse** to a submanifold $S\subset N$, written $f\pitchfork S$, if for every $x$ with $f(x)\in S$,
$$
df_x(T_xM) + T_{f(x)}S \;=\; T_{f(x)}N.
$$
In words: the image of the tangent space of $M$ and the tangent space of $S$ together span the ambient tangent space. The map $f$ "meets" $S$ as straightly as possible — not tangentially, but at the maximal angle allowed.

**Theorem (transversality / Thom).** For any submanifold $W$ of the jet bundle $J^k(M,N)$, the set of maps $f$ with $j^k f\pitchfork W$ is residual (hence dense) in the Whitney $C^\infty$ topology. In the special case $W=S$ (viewed in $J^0(M,N)=N$), this says: if $f\pitchfork S$, then $f^{-1}(S)$ is a submanifold of $M$ of codimension equal to that of $S$ in $N$, and the class of maps transverse to a fixed $S$ is dense in $C^\infty(M,N)$.

The density statement is the global straightening result: *a generic map is as straight as possible relative to any prescribed submanifold.* The full **Thom transversality theorem** is the jet-bundle statement just given; statements about *families* of maps are the **parametric** transversality theorem. This is the engine behind the existence of generic Morse functions, generic immersions, generic vector fields, and — in physics — the assertion that a generic perturbation of a potential has only non-degenerate critical points, so that the critical point set is a discrete, countable, and stably defined object.

The **Morse lemma** is the local straightening of a critical point, and it is the sharpest form of the first-order rigidity:

**Theorem (Morse lemma).** If $p$ is a nondegenerate critical point of $f:M^n\to\mathbb{R}$, there are coordinates centered at $p$ with
$$
f = f(p) - y_1^2 - \cdots - y_k^2 + y_{k+1}^2 + \cdots + y_n^2 .
$$
The index $k$ (the number of negative eigenvalues of the Hessian) is the only invariant (Sylvester). The charts are not canonical. The linear symmetry group of the normal form is $O(k,n-k)$, not $O(n)$. The higher-order terms of $f$ are *completely invisible* to the local model: the Morse lemma erases them. This is the purest example of the grading: the second-order behavior is canonical (the index), and the third-and-higher-order behavior is irrelevant to the local type.

For a physicist: the Morse lemma is the mathematical content of the *stationary phase* and *saddle point* approximations. The leading term in the asymptotic expansion of
$$
\int e^{i\lambda f(x)}\,a(x)\,dx \;\sim\; \Bigl(\tfrac{2\pi}{\lambda}\Bigr)^{n/2}\lvert\det\mathrm{Hess}f(p)\rvert^{-1/2}\,e^{i\lambda f(p)}\,e^{i\pi\,\mathrm{sgn}(\mathrm{Hess}f(p))/4}\,a(p)
$$
as $\lambda\to\infty$ is determined by the Hessian at the critical points — the straight quadratic — where $\mathrm{sgn}=n-2k$ and $k$ is the number of negative eigenvalues. The higher-order terms contribute only to the subleading coefficients. The calculus of asymptotics is, at its leading order, a second-order (in $f$) calculus, and it is unique.

---

## 5. Vector fields, flows, and the uniqueness of the infinitesimal straightening

*(Vector fields and the flow box theorem: Hirsch, *Differential Topology*; Lee, *Introduction to Smooth Manifolds*. Darboux's theorem: standard symplectic geometry.)*

A vector field $X$ on $M$ is a choice, for each $p\in M$, of a tangent vector $X_p\in T_pM$, varying smoothly. A vector field is, pointwise, a "direction of straightness": it tells you which direction, at each point, is the preferred direction of motion. The **flow** of $X$ is the family of diffeomorphisms $\{\varphi_t\}$ generated by integrating $X$, satisfying $\frac{d}{dt}\varphi_t(p) = X_{\varphi_t(p)}$ and $\varphi_0 = \mathrm{id}$.

The **flow box theorem** is the straightening result for vector fields:

**Theorem (flow box).** Let $X$ be a nonvanishing vector field and $p\in M$. Then there is a chart $\varphi:U\to\mathbb{R}^n$ about $p$ in which $X$ is the constant vector field $\partial/\partial x^1$.

In words: *locally, a nonvanishing vector field is a straight line field, and its flow is straight translation in the $x^1$ direction.* The straightening is unique up to the action of the group of diffeomorphisms that fix the $x^1$-direction — i.e., up to the "vertical" re-straightening of the transverse variables. So the flow is locally as straight as possible, and the only freedom in the straightening is the freedom to reparametrize the transverse coordinates.

The **uniqueness of the flow** is the key fact. The equation $\dot\gamma = X(\gamma)$ is a nonlinear autonomous ODE; uniqueness of solutions is Picard–Lindelöf. Given $X$, the flow $\{\varphi_t\}$ is the *unique* one-parameter group of diffeomorphisms with $\varphi_t'(0) = X$. The flow is defined for all $t\in\mathbb{R}$ only if $X$ is complete. It is the dynamical content of the straightening: the vector field determines the flow, and the flow determines the vector field (as its infinitesimal generator), and this correspondence is bijective on complete fields. There is no moduli: the flow is the unique "integration" of the straightening.

For a physicist, this is the content of the statement that a Hamiltonian vector field determines a Hamiltonian flow, and that the flow is the unique symplectomorphism group with that generator. If $\mathcal{L}_{X_H}\omega=0$, then $\mathcal{L}_{X_H}\omega^n=0$, and $\omega^n/n!$ is the volume form. Darboux's theorem is not involved in this step.

The **Darboux theorem** is the symplectic straightening:

**Theorem (Darboux).** Near every point of a symplectic manifold $(M^{2n},\omega)$ there are coordinates in which $\omega=\sum_{i=1}^n dx^i\wedge dx^{n+i}$.

In words: *locally, every symplectic form is the standard flat form.* These charts are highly non-unique: the freedom is the group of local symplectomorphisms. The theorem holds because of the closedness ($d\omega=0$) and the non-degeneracy of the form, via Moser's trick: closedness lets one write the difference $\omega_1-\omega_0$ along a homotopy as $d\alpha$, while non-degeneracy of $\omega_t$ lets one solve the homological equation $\iota_{X_t}\omega_t = -\alpha$ for the vector field $X_t$, not because "the first jet determines $\omega$". The symplectic form has no local invariants (no curvature, in the Riemannian sense); the only obstruction to flatness is $d\omega\neq0$.

The contrast with the Riemannian case, which I will develop in §8, is the central contrast of the essay: the symplectic straightening has no local invariants, while the Riemannian straightening is locally unique only at a point (the curvature is the first local invariant, and it appears at second order).

---

## 6. The tangent bundle: the straightening as a *bundle*

*(Tangent bundles: Milnor, Ch. 4. Characteristic classes and parallelizability: Hirsch, *Differential Topology*; Milnor, *Characteristic Classes of Fiber Bundles*.)*

So far the straightening has been pointwise: $T_pM$ at each $p$. The **tangent bundle**
$$
TM = \bigsqcup_{p\in M} T_pM, \qquad \pi : TM \to M
$$
is the *total space* of the straightening: it is the manifold that records, over every point of $M$, the whole linear space in which $M$ is straight at that point. $TM$ is itself a smooth $2n$-manifold, and the projection $\pi$ is a submersion whose fiber over $p$ is the linear space $T_pM \cong \mathbb{R}^n$.

The straightening theme now takes a new form: **is $TM$ trivial?** That is, is there a global frame — $n$ everywhere-independent vector fields $X_1,\dots,X_n$ such that $\{X_1(p),\dots,X_n(p)\}$ is a basis of $T_pM$ for every $p$? If so, $TM \cong M \times \mathbb{R}^n$, and the manifold is **parallelizable**: it is, globally, as straight as a product. The answer, for the sphere, is the first major global straightening theorem:

**Theorem (Bott–Milnor, Kervaire, Adams).** $TS^n$ is trivial if and only if $n \in \{0,1,3,7\}$.

The non-existence for other $n$ is due to Bott–Milnor and Kervaire (1958); Adams's Hopf-invariant-one theorem (1960) and his work on vector fields on spheres (1962) give the sharp form. The normed division algebras $\mathbb{R},\mathbb{C},\mathbb{H},\mathbb{O}$ have dimensions $1,2,4,8$, and $S^0,S^1,S^3,S^7$ are their unit spheres. Maps $S^{2n-1}\to S^n$ of Hopf invariant one exist only for $n\in\{1,2,4,8\}$. The four parallelizable spheres are the three Hopf spheres together with $S^0$.

For a general manifold, parallelizability depends on the manifold, not only on its dimension: general Lie groups (including tori) and orientable $3$-manifolds are all parallelizable.

The **Euler class** is the primary obstruction to parallelization in general. For an oriented rank-$n$ bundle $E\to M$, the Euler class $e(E)\in H^n(M;\mathbb{Z})$ is the primary obstruction to the existence of a nonvanishing section. But vanishing of the Stiefel–Whitney, Pontryagin and Euler classes is necessary for triviality and not sufficient: $S^5$ is stably parallelizable, so all these classes vanish, yet $S^5$ is not parallelizable. The Pontryagin classes $p_i(E)=(-1)^i c_{2i}(E\otimes\mathbb{C})\in H^{4i}(M;\mathbb{Z})$ are defined for every real bundle $E$; a complex structure on $E$ imposes relations on them, but they are not "the obstruction" to one. For a physicist: as a complex line bundle over $\mathbb{CP}^1$, $TS^2\cong\mathcal{O}(2)$, so $e(TS^2)=c_1=2$ (the Hopf bundle is $\mathcal{O}(-1)$).

The **tangent bundle of a product** is the model case: if $M = M_1 \times M_2$, then $TM = TM_1 \times TM_2$ (pulled back to the product), and the straightening of the product is the product of the straightenings. This is why the calculus on a product is the tensor product of the calculi on the factors: $\Omega^\bullet(M_1)\otimes\Omega^\bullet(M_2)$ is dense in $\Omega^\bullet(M_1\times M_2)$, with equality after completing the tensor product; the Künneth isomorphism holds in cohomology, and the Euler characteristic is multiplicative, $\chi(M_1\times M_2) = \chi(M_1)\chi(M_2)$.

---

## 7. Transversality and jets: the straightening, and its *failure to be unique*, measured by the jet

*(Jets and the jet bundle: Lee, *Introduction to Smooth Manifolds*; Hirsch, *Differential Topology*.)*

The **$k$-jet** of a smooth function $f:M\to\mathbb{R}$ at a point $p$ is the class of $f$ in $C^\infty_p/\mathfrak{m}_p^{\,k+1}$, i.e. the equivalence class of $f$ under the relation "agree up to order $k$ at $p$." The $1$-jet is the pair $(f(p),df_p)$ (the value and the gradient); the $2$-jet adds the Hessian; and so on.

The **jet bundle** $J^k(M,\mathbb{R})$ is the bundle whose fiber over $p$ is the space of $k$-jets at $p$. It is a finite-dimensional vector bundle of rank $\binom{n+k}{k}$, with transition functions that are polynomial in the higher derivatives of the coordinate change. The **jet prolongation** $j^k : M \to J^k(M,\mathbb{R})$ is a smooth section. The splitting of a $k$-jet into "gradient $+$ Hessian $+$ …" is coordinate-independent only at a critical point, or given a connection; away from such data the splitting is not canonical. The **Thom transversality theorem**, in its full form, says that a generic function has a $k$-jet section that is transverse to the subbundle of degenerate jets — i.e., a generic function has non-degenerate critical points (for $k=2$), and more generally a generic function has a $k$-jet that avoids a prescribed submanifold of the jet bundle.

The **non-uniqueness of the higher-order straightening** is now precise. The $1$-jet of $f$ at $p$ is the pair $(f(p),df_p)$; it is unique, canonical, and determined by the germ of $f$. The $2$-jet of $f$ at $p$ is a point of the affine bundle of $2$-jets; it is *not* determined by the $1$-jet, and two functions with the same $1$-jet can have different $2$-jets. The $k$-jet for $k\ge 2$ is a *genuine invariant* of the germ.

One must be careful, however, about what the "moduli" are. Jets of *functions* are not "moduli of straightenings": the $k$-jet $j^k_p f$ is a canonical object determined by the germ of $f$. The freedom in a $k$-th order *straightening* (a choice of coordinates up to order $k$) is measured by $k$-jets of coordinate changes, i.e. by the group $G^k$ of $k$-jets of diffeomorphisms of $\mathbb{R}^n$ at $0$, an extension of $GL_n(\mathbb{R})$ by a unipotent group. A torsion-free connection is a $GL_n$-equivariant splitting of the second-order frame bundle onto the first-order frame bundle. This is the precise sense in which the calculus is "graded": the $1$-jet is a point (unique), the $2$-jet is not determined by the $1$-jet, and the higher the order, the more freedom there is in the straightening, and the larger the group $G^k$.

The **formal inverse** of a function (the inverse of its Taylor series) is a formal power series, and it is unique as a formal object: the $k$-jet of the formal inverse is determined by the $k$-jet of $f$ (see §2). It is not, however, recoverable from any finite jet of $f$ when $f$ is merely $C^\infty$ and non-analytic, and it does not always converge. The higher-order straightening is *formally* unique (the formal inverse is unique) but *not analytically* unique (the convergent inverse is not determined by any finite jet).

The **Morse–Bott theorem** is the higher-order generalization of the Morse lemma, and it makes the grading explicit:

**Theorem (Morse–Bott).** If $f:M\to\mathbb{R}$ has a nondegenerate critical submanifold $C$ (i.e., the set of critical points is a submanifold, and the Hessian is nondegenerate in the normal directions), then in a tubular neighbourhood of $C$,
$$
f = f|_C + |y|^2 - |z|^2,
$$
where $y,z$ are fibre coordinates on the positive and negative eigenbundles of the normal Hessian. This generalizes Morse's lemma to degenerate critical *manifolds*; it is not a "higher-order" generalization in the sense of introducing new invariants. The only invariant is the index of the normal Hessian. The higher-order terms are again invisible: the Morse–Bott lemma erases them, and the local model is a straight quadratic form on the normal bundle.

The **Morse index** and the **Morse homology** are the global invariants built from the higher-order straightening. The Morse homology $MH_*(M)$ is the homology of the chain complex generated by the critical points of a Morse function $f$, with differential counting the gradient flow lines between critical points of adjacent index. For a Morse function $f$ and a Riemannian metric $g$ such that $(f,g)$ is Morse–Smale, the **Morse–Smale–Witten complex** computes $H_*(M)$ (Smale, Milnor, Witten, Floer). This is the global straightening result: the higher-order calculus (the Morse complex) computes the same thing as the global topology (the singular homology), and the straightening is canonical up to chain homotopy.

For a physicist, this is the mathematical content of the *instanton* and *bounce* calculations in quantum field theory: the leading contribution to the path integral comes from the critical points of the action (the classical solutions). A bounce's single negative mode produces the imaginary part of the energy, i.e. the decay rate. The one-loop prefactor is the quadratic-fluctuation determinant, and higher-order terms give higher loops. The $\theta$-dependence comes from the topological charge, and fermion zero modes come from the index (see §11).

---

## 8. Connections, curvature, and the uniqueness of the Levi-Civita connection: the second-order straightening

*(Beyond Milnor; the chapter the 1965 book leaves implicit.)*

Milnor's book stops at the level of the tangent bundle and the jet bundle. But the straightening theme demands one more chapter, because it is the chapter that answers the physicist's most direct question: *given a metric, is the connection unique?* The answer is **yes, at the level of the connection, and no, at the level of the metric**, and the distinction is the sharpest possible statement of the grading.

**Definition.** A **connection** on a vector bundle $E\to M$ is a $\mathbb{R}$-linear map $\nabla : \Gamma(E)\to \Gamma(T^*M\otimes E)$ satisfying the Leibniz rule $\nabla(fs) = df\otimes s + f\nabla s$. In a local frame, $\nabla$ is given by a $1$-form with values in the Lie algebra of the structure group: $\nabla = d + A$, where $A\in \Omega^1(M;\mathfrak{g})$ is the **connection form**.

The **space of connections** on a vector bundle $E\to M$ is an affine space modelled on $\Omega^1(M;\mathrm{End}\,E)$; on a principal $G$-bundle $P\to M$, on $\Omega^1(M;\mathrm{ad}\,P)$. That is, there is no canonical connection: the connections are in bijection with that affine space, which is an infinite-dimensional vector space. The straightening at the level of the connection is *not unique*: there is a moduli space of connections, and the moduli space is the quotient of the affine space of $\mathfrak{g}$-valued $1$-forms by the gauge group.

But now impose a metric. Let $(M,g)$ be a Riemannian (or pseudo-Riemannian) manifold. A connection $\nabla$ is **metric-compatible** if $\nabla g = 0$ (i.e., the connection preserves the metric: $\nabla_X g(Y,Z) = g(\nabla_X Y, Z) + g(Y, \nabla_X Z)$). A connection is **torsion-free** if $\nabla_X Y - \nabla_Y X = [X,Y]$ (i.e., the connection is symmetric in its arguments).

**Theorem (Levi-Civita).** There is a **unique** connection on $TM$ that is both metric-compatible and torsion-free.

The proof is a direct computation: metric compatibility and zero torsion force the **Koszul formula**
$$
2g(\nabla_XY,Z)=Xg(Y,Z)+Yg(X,Z)-Zg(X,Y)+g([X,Y],Z)-g([X,Z],Y)-g([Y,Z],X),
$$
so $\nabla$ is uniquely determined. The formula defines a connection with both properties, so $\nabla$ exists. In local coordinates this reads as the **Christoffel symbols**
$$
\Gamma^k_{ij} = \frac{1}{2}\,g^{k\ell}\big( \partial_i g_{j\ell} + \partial_j g_{i\ell} - \partial_\ell g_{ij} \big).
$$
The straightening is unique: *given the metric, there is exactly one connection that straightens the manifold in the metric sense (parallel transport preserves lengths and angles) and the symmetry sense (no torsion).*

This is the central uniqueness theorem of the essay, and it is the answer to the physicist's question. The **Riemannian metric** is a choice (a section of $S^2 T^*M$), and the space of metrics is an infinite-dimensional convex cone. But **given a metric, the connection is unique**: the Levi-Civita connection is the unique metric-compatible, torsion-free connection. The straightening at the level of the connection is canonical, once the metric is fixed. The freedom has moved up one level: it is not in the connection (which is unique) but in the metric (which is a moduli space).

The **curvature** $R^\nabla \in \Omega^2(M;\mathrm{End}(TM))$ is the obstruction to the connection being flat, and it is the first non-vanishing local invariant of the metric, appearing at second order. In a normal coordinate system at a point $p$ (geodesic coordinates), $g_{ij}(p) = \delta_{ij}$ and $\Gamma^k_{ij}(p) = 0$ (so $\partial_k g_{ij}(p)=0$), while $\partial_k\partial_\ell g_{ij}(p) \neq 0$ in general. With $R_{ijkl}=g_{im}R^m{}_{jkl}$, the curvature is
$$
R_{ijkl}(p)=\tfrac12\bigl(\partial_j\partial_kg_{il}+\partial_i\partial_lg_{jk}-\partial_i\partial_kg_{jl}-\partial_j\partial_lg_{ik}\bigr)(p).
$$
The curvature is a second-order invariant: it is invisible to the first jet of $g$ (which is zero at $p$ in normal coordinates), but visible to the second jet. This is the Riemannian analogue of the symplectic contrast: the symplectic form has no local invariants, while the Riemannian metric has local invariants starting at second order (the curvature). The straightening of the Riemannian manifold is unique at a point (the metric is Euclidean, the connection is flat, in normal coordinates), but not on an open set (the curvature is the obstruction).

A word on the grading, since an analyst may balk at calling a metric "second-order": the metric $g$ is, algebraically, a $0$th-order object — a section of $S^2T^*M$, a tensor field with no derivatives in its definition. We grade it by the order at which its *invariants* appear in the normal-coordinate expansion, where $g_{ij}(p)=\delta_{ij}$, $\partial_k g_{ij}(p)=0$, and the first non-vanishing invariant, the curvature, is read off from $\partial_k\partial_\ell g_{ij}(p)$. So the metric is "second-order" in the sense that its straightening is canonical to first order (Euclidean, with zero first derivatives) and the moduli (the curvature) enter at second order — exactly the grading the essay is tracking. The connection, which is built from the first derivatives of $g$, is likewise graded by the order at which it is determined: it is first-order data in $g$, and its curvature is second-order.

The **Ricci tensor** and the **scalar curvature** are the contractions of the curvature, and they are the invariants that appear in the Einstein–Hilbert action
$$
S_{\mathrm{EH}}[g] = \int_M R\,\mathrm{vol}_g.
$$
The **Einstein equations** $G_{ij} + \Lambda g_{ij} = 8\pi T_{ij}$ are the critical point equations of this action, and they are, in the language of the straightening, the equations that the metric must satisfy for the straightening to be "as flat as possible" in the presence of matter. The uniqueness of the Levi-Civita connection says that the metric determines the connection. The uniqueness of the geodesic with given initial data is ODE theory. Connections with torsion can have the same geodesics as Levi-Civita.

The **Nash embedding theorem** is the global straightening result for Riemannian manifolds:

**Theorem (Nash, 1954/1956; analytic 1966).** Every $n$-dimensional Riemannian manifold $(M,g)$ is isometrically embeddable in $\mathbb{R}^N$ for $N$ sufficiently large. The $C^1$ isometric embeddings were proved by Nash (1954) for $N\ge n+2$ and by Kuiper (1955) for $N\ge n+1$. Nash's 1956 paper (*The imbedding problem for Riemannian manifolds*, Ann. of Math. $63$, 20–63) proved the $C^k$ case for $3\le k\le\infty$, with $N=n(3n+11)/2$ for compact $M$ and $N=n(n+1)(3n+11)/2$ for noncompact $M$; his $C^\infty$ proof uses his own smoothing iteration. Moser (1961) isolated the method for other problems, and Hamilton (1982) gave the abstract Nash–Moser inverse function theorem (§10). Later work (Gromov, Günther) lowered $N$ substantially.

In words: *every curved space can be straightened, globally, by embedding it in a sufficiently high-dimensional flat space.* The isometric embedding is the global straightening: the metric $g$ is the restriction of the Euclidean metric on $\mathbb{R}^N$ to the image of $M$. The isometric embeddings are *far from unique*, even modulo rigid motions: the $C^1$ case is flexible (Nash–Kuiper), while some $C^2$ cases are rigid (convex surfaces). The moduli space of embeddings is a genuine moduli space. The $C^\infty$ case requires the Nash–Moser method, which I will describe in §10.

The curvature is a **tensor** (coordinate-independent) because $R(X,Y)Z$ is $C^\infty(M)$-linear in $X$, $Y$ and $Z$. The **Bianchi identities** ($d_\nabla R=0$) are differential identities, not the reason for tensoriality. They are the higher-order integrability conditions that the straightening must satisfy.

---

## 9. The non-uniqueness of the smooth structure: exotic $\mathbb{R}^4$ and the exotic spheres

*(Beyond Milnor; the chapter the 1965 book cannot contain.)*

Milnor's book is written in the $C^\infty$ category, and it assumes that the smooth structure on $\mathbb{R}^n$ is unique. This is true for $n \neq 4$, and it is **false** for $n = 4$. The failure of uniqueness in dimension four is the most dramatic and most mysterious of all the non-uniqueness results in differential topology, and it is the result that most directly answers the question "is the straightening unique?" with a resounding **no, in dimension four**.

**Definition.** A **smooth structure** on a topological $n$-manifold $M$ is an equivalence class of $C^\infty$ atlases, where two atlases are equivalent if the union is a smooth atlas. Two smooth structures on the same topological manifold are **exotic** if they are not diffeomorphic (even though they are homeomorphic).

**Theorem (Freedman–Donaldson, early 1980s; Gompf 1985; Taubes 1987).** There exist exotic $\mathbb{R}^4$'s: smooth structures on the topological $4$-manifold $\mathbb{R}^4$ that are not diffeomorphic to the standard $\mathbb{R}^4$. Freedman's classification of simply connected topological $4$-manifolds, together with Donaldson's theorem on smooth $4$-manifolds with definite intersection form, yields a smooth structure on $\mathbb{R}^4$ that is not diffeomorphic to the standard one (Freedman–Donaldson, early 1980s). Gompf (1985) constructed infinitely many, and Taubes (1987) uncountably many, using gauge theory on end-periodic manifolds. There are **uncountably many** such structures.

*(Optional historical note: Mazur (1961) constructed compact contractible smooth $4$-manifolds $W$ whose boundary is a homology $3$-sphere with nontrivial $\pi_1$. Such a $W$ is not diffeomorphic to $B^4$, although $W\times[0,1]\cong B^5$. These Mazur manifolds are the building blocks behind the exotic $\mathbb{R}^4$'s, but the uncountability is a separate, deeper fact.)*

The **uncountability** is a deeper fact: there are uncountably many pairwise non-diffeomorphic smooth structures on the topological $\mathbb{R}^4$. This is in sharp contrast to the other dimensions: the smooth structure on $\mathbb{R}^n$ is unique up to diffeomorphism for $n\le 2$ (classical), for $n=3$ (Moise), and for $n\ge 5$ (Stallings and smoothing theory). It is not the Poincaré conjecture that gives $n=3$. Dimension four is the exceptional one: it is too low for the $h$-cobordism theorem and too high for the $3$-dimensional control that Moise's theorem provides.

The **exotic spheres** are the higher-dimensional analogue, and they are the first example of non-uniqueness in the smooth category that Milnor himself discovered:

**Theorem (Milnor, 1956).** There exist smooth $7$-spheres that are not diffeomorphic to the standard $S^7$. Milnor's paper is from 1956 (*On manifolds homeomorphic to the $7$-sphere*, Ann. of Math. $64$, 399–405). He considered $S^3$-bundles over $S^4$ with Euler number $1$, which are homotopy $7$-spheres. A Morse function with two critical points shows they are homeomorphic to $S^7$, and an invariant built from the signature theorem and $p_1^2$ shows that some are not diffeomorphic to $S^7$. Triviality of $TS^7$ is not used.

**Theorem (Kervaire–Milnor, 1963).** The group $\Theta_7$ of diffeomorphism classes of smooth $7$-spheres (under connected sum) is isomorphic to $\mathbb{Z}/28\mathbb{Z}$. The classes are distinguished by the **Eells–Kuiper invariant** $\mu$, not by the Euler number (which equals $1$ for every homotopy sphere in the family). The bundle spheres realize $16$ of the $28$ classes: in Milnor's family $\mu\equiv m(m+1)/2\pmod{28}$.

More generally, the group $\Theta_n$ of exotic $n$-spheres is finite for $n\ge 5$ (its order is known in many dimensions) but often nonzero. Exotic spheres and exotic $\mathbb{R}^n$ are different phenomena: an exotic $S^n$ minus a point is standard $\mathbb{R}^n$ for $n\ge 5$. The $n=4$ case is the exception, and the exception is uncountable.

The **$4$-dimensional Poincaré conjecture** (proved by Freedman in 1982, in the topological category) says that every simply-connected closed topological $4$-manifold homotopy equivalent to $S^4$ is homeomorphic to $S^4$. But the **smooth** $4$-dimensional Poincaré conjecture — that every simply-connected closed smooth $4$-manifold homeomorphic to $S^4$ is *diffeomorphic* to $S^4$ — is **open**. This is the single most important open problem in $4$-dimensional differential topology, and it is a direct question about the uniqueness of the straightening: *is the smooth structure on $S^4$ unique?* The existence of exotic $\mathbb{R}^4$'s suggests the answer is no, but a proof is lacking — and the existence of exotic $\mathbb{R}^4$'s does not by itself imply the existence of an exotic $S^4$.

For a physicist, the relevance is real but should be stated with care. On the mathematical side, the **Donaldson invariants** of a smooth $4$-manifold are, in physics, correlation functions of the topologically twisted $\mathcal{N}=2$ supersymmetric Yang–Mills theory on that manifold (Witten's interpretation, 1988); the 1994 paper is Witten's Seiberg–Witten (monopole) work. The instanton number $c_2$ is topological; what depends on the smooth structure is the instanton moduli space and the Donaldson invariants. That is a precise and well-established connection: the gauge-theoretic invariants that detect exotic smooth structures are themselves partition functions of a supersymmetric gauge theory. On the physical side, however, the question of whether exotic smooth structures on a spacetime manifold have observable consequences is a live and **speculative** topic: it is not settled whether a theory of quantum gravity distinguishes the uncountably many smooth structures on the same topological spacetime. We flag the distinction explicitly — the mathematical facts are firm, the physical implications are open.

---

## 10. The straightening in infinite dimensions: Banach, Fréchet, and Nash–Moser

*(The chapter that answers the functional analyst's question.)*

Everything so far has been finite-dimensional, and the straightening has been a diffeomorphism onto an open set of $\mathbb{R}^n$. The functional analyst's question is what happens when the "manifold" is an infinite-dimensional space of maps, and the "straightening" is the inverse function theorem for a nonlinear operator between such spaces. The answer is that the finite-dimensional straightening **succeeds in Banach spaces, fails in Fréchet spaces, and is repaired by the Nash–Moser method**.

**The Banach inverse function theorem.** Let $X,Y$ be Banach spaces and $F:X\to Y$ a $C^1$ map with $F(0)=0$. If $DF_0 : X\to Y$ is an **isomorphism** (bounded, bijective, with bounded inverse), then $F$ is locally a diffeomorphism: there are neighborhoods $U\ni 0$ in $X$ and $V\ni 0$ in $Y$ such that $F|_U : U\to V$ is a $C^1$ diffeomorphism. The theorem holds for $C^k$ maps for every $k\ge 1$.

The proof is the same contraction argument as in the finite-dimensional case, and it works because the derivative $DF_0$ is an *isomorphism of Banach spaces* — a bounded invertible linear map. The straightening is unique to first order (the derivative is the unique best linear approximation, as in §1), and the higher-order behavior is controlled by the same formal inverse as in §2. The Banach inverse function theorem is the infinite-dimensional straightening, and it is as canonical as the finite-dimensional one: the derivative is the unique first-order object, and the local diffeomorphism is unique.

**The failure in Fréchet spaces.** A **Fréchet space** is a complete metrizable locally convex space that is not, in general, a Banach space (it has no norm, only a countable family of seminorms). The space $C^\infty(M)$ of smooth functions on a compact manifold $M$, with its standard Fréchet topology (uniform convergence of all derivatives on compact sets), is the model example. The Banach inverse function theorem **fails** for Fréchet spaces: the derivative $DF_0$ may be a surjective continuous linear map with a continuous right-inverse (a *splitting*), but the nonlinear map $F$ need not be locally a diffeomorphism.

The reason is that the contraction argument requires a *norm* to control the error, and a Fréchet space has no norm — only a family of seminorms. The contraction constant, which is uniform in the finite-dimensional and Banach cases, is not uniform in the Fréchet case: the seminorms are independent, and a small error in one seminorm can be large in another. The straightening, which is uniform in the Banach case, is **not uniform** in the Fréchet case, and the local diffeomorphism can fail to exist.

**The Nash–Moser implicit function theorem.** The repair is the **Nash–Moser method**. Nash introduced the smoothing-operator / modified-Newton technique in his 1956 paper on isometric embedding (to overcome the derivative loss in the $C^\infty$ case); Moser (1961) isolated the method for other problems, and Hamilton (1982) gave the abstract Nash–Moser inverse function theorem. Let $F$ be a smooth tame map between tame Fréchet spaces. If $DF(x)$ is invertible for all $x$ near $x_0$ and the inverses form a smooth tame family, then $F$ is a local diffeomorphism with smooth tame inverse. Tameness is extra structure (a grading and smoothing operators), not "a topology slightly weaker than $C^\infty$". The key idea is to replace the Newton iteration of the Banach inverse function theorem with a **modified Newton iteration** that includes a *smoothing operator* at each step.

The standard Newton iteration for solving $F(x)=0$ is
$$
x_{n+1} = x_n - (DF_{x_n})^{-1} F(x_n).
$$
In Nash–Moser settings the right inverse satisfies $\lVert(DF_x)^{-1}y\rVert_s\lesssim\lVert y\rVert_{s+r}$ for a fixed $r$ (for example $r=1$ or $2$ for isometric embedding, $r=\tau$ for KAM), so plain Newton loses $r$ derivatives per step. The Nash–Moser fix is to insert a **smoothing operator** $S_\theta$ at each step — a family of bounded operators, parameterized by a parameter $\theta$ that grows — satisfying
$$
\lVert S_\theta u\rVert_{s+a}\lesssim\theta^{a}\lVert u\rVert_s,\qquad\lVert(1-S_\theta)u\rVert_s\lesssim\theta^{-a}\lVert u\rVert_{s+a},
$$
— into the iteration:
$$
x_{n+1} = x_n - S_{\theta_n}\big( (DF_{x_n})^{-1} F(x_n) \big).
$$
With $\theta_n$ growing fast, the smoothing compensates the derivative loss, and the iteration converges **superexponentially**. The convergence is in the **tame Fréchet** category, in which the smoothing operators and the inverse are *tame* maps, and the result is a local diffeomorphism in the tame category, which is sufficient for the applications.

**The $C^\infty$ Nash isometric embedding theorem** is the first and most celebrated application. The isometric embedding problem is to find a smooth map $f:M^n\to\mathbb{R}^N$ such that $f^*(\delta) = g$ (the pullback of the Euclidean metric $\delta$ is the given metric $g$). The relevant operator is
$$
F(f) = f^*(\delta) - g \;\in\; \Gamma(S^2 T^*M),
$$
and for $h\in C^\infty(M,\mathbb{R}^N)$ the derivative is
$$
DF_f(h)(u,v) = \langle df(u),dh(v)\rangle + \langle dh(u),df(v)\rangle ,
$$
a first-order differential operator. (The Lie-derivative formula $DF_f(h)=\mathcal{L}_h g$ describes only the tangential variations $h=df(X)$.) The operator $DF_f$ is a **first-order differential operator**, and it is surjective for $N$ sufficiently large (the surjectivity is the linearized isometric embedding theorem, proved by Nash); at "free" maps (Gromov), which requires $N\ge n(n+3)/2$, the linearization has a right inverse that is a differential operator. But that right inverse loses one derivative, and the standard Newton iteration does not converge in $C^\infty$. The Nash–Moser method, with its smoothing operators, gives the convergence, and the $C^\infty$ isometric embedding theorem follows.

**The KAM theorem** is the second great application, and it is the one that a mathematical physicist will recognize. The KAM theorem says that a **near-integrable** Hamiltonian system — a Hamiltonian $H = H_0 + \varepsilon H_1$ with $H_0$ integrable and $\varepsilon$ small — has, for $\varepsilon$ sufficiently small, a **Cantor set** of invariant tori on which the motion is quasi-periodic. The relevant operator is the **homological equation**
$$
\omega\cdot \partial_\theta u = f(\theta) - \bar f,
$$
where $\omega\in\mathbb{R}^n$ is the frequency vector, $f:\mathbb{T}^n\to\mathbb{R}$ is a smooth function, and $\bar f$ is its average. The operator $\omega\cdot\partial_\theta$ has a **small divisor problem**: its inverse is
$$
(\omega\cdot\partial_\theta)^{-1} f = \sum_{k\neq 0} \frac{f_k}{i\,\omega\cdot k}\, e^{ik\cdot\theta},
$$
and the denominators $\omega\cdot k$ can be arbitrarily small (the small divisors). A frequency $\omega$ is **Diophantine** if $\lvert\omega\cdot k\rvert\ge\gamma\lvert k\rvert^{-\tau}$ for all $k\in\mathbb{Z}^n\setminus\{0\}$, with $\tau\ge n-1$ (and $\tau>n-1$ for full measure); then $1/\lvert\omega\cdot k\rvert\le\lvert k\rvert^{\tau}/\gamma$, so the inverse of $\omega\cdot\partial_\theta$ loses about $\tau$ derivatives. The KAM theorem also requires the **Kolmogorov nondegeneracy condition** $\det(\partial\omega/\partial I)\neq 0$. In the analytic case (Kolmogorov, Arnold) a quadratically convergent Newton scheme works without smoothing; smoothing is needed for finite differentiability (Moser). The Nash–Moser method, with its smoothing operators and the Diophantine condition, gives the convergence, and the conclusion is: invariant tori with Diophantine frequencies persist, conjugate to linear flows, and form a Cantor family of large measure.

For a physicist, the KAM theorem is the mathematical content of the statement that *near-integrable systems are, to first order, integrable, and the perturbation theory (the Newton iteration) is valid up to a fixed number of derivatives, but the convergence requires the Diophantine condition and the smoothing operator*. The straightening of the near-integrable system is the integrable system $H_0$ (the flat connection, the straightening), and the perturbation $H_1$ is the curvature (the obstruction to the straightening being exact).

The two applications — the $C^\infty$ Nash isometric embedding theorem and the KAM theorem — are the pillars of the infinite-dimensional straightening. What fails is the Fréchet-space setting combined with derivative loss, not "$C^\infty$ versus $C^1$": the Banach inverse function theorem holds for $C^k$ maps for every $k\ge 1$. The $C^\infty$ calculus on an infinite-dimensional space requires the Nash–Moser method precisely because of the derivative loss, and the $C^1$ (Banach) straightening does not.

---

## 11. The Atiyah–Singer index theorem: the global counterpart of the straightening principle

*(Beyond Milnor; the global theorem that closes the grading.)*

So far the global calculus has appeared as *obstruction*: characteristic classes measure the failure of the global straightening, and the smooth structure is non-unique in dimension four. There is a complementary global theorem, and it is the one that most directly completes the straightness principle: it says that **when a straightening is given in the form of an elliptic operator, the global content of the straightening is not merely obstructed but canonically determined** — it is a unique, natural, topological invariant of the local straightening data. This is the Atiyah–Singer index theorem.

**Elliptic operators and the symbol as straightening.** Let $M$ be a closed smooth $n$-manifold, $E,F$ complex vector bundles over $M$, and $P:\Gamma(E)\to\Gamma(F)$ a differential operator of order $m$. The **principal symbol** $\sigma(P)\in\Gamma(T^*M\setminus 0,\mathrm{Hom}(\sigma E,\sigma F))$ is a bundle map over the punctured cotangent bundle, and it is the straightening of $P$: at each covector $\xi\neq 0$, $\sigma_\xi(P)$ is the linear operator that $P$ becomes when the manifold is straightened at $\xi$. The symbol is the part of $P$ that is invariant under lower-order perturbations — the part that survives the passage to the cotangent bundle. In the language of the essay, the symbol is the straightening of $P$, and it is canonical: it does not depend on any choice.

The operator $P$ is **elliptic** if $\sigma_\xi(P)$ is invertible for every $\xi\neq 0$; that is, if the straightening is invertible away from the zero section. Elliptic operators form an open set in the space of differential operators, and each elliptic $P$ is **Fredholm**: $\ker P$ and $\mathrm{coker}\,P$ are finite-dimensional, and the **index**
$$
\operatorname{ind} P \;=\; \dim\ker P - \dim\mathrm{coker}\,P
$$
is a stable integer, locally constant in the space of elliptic operators. The kernel and cokernel separately depend on the full operator (the higher-order terms, the moduli); the index does not. It depends only on the symbol, and the theorem that says so is the index theorem.

**Theorem (Atiyah–Singer, 1961–1971).** Let $P:\Gamma(E)\to\Gamma(F)$ be a complex elliptic operator on a closed smooth manifold $M$. Then
$$
\mathrm{ind}\,P=(-1)^n\int_{T^*M}\mathrm{ch}(\sigma(P))\,\mathrm{Td}(TM\otimes\mathbb{C}),\qquad\mathrm{ch}(\sigma(P))\in H^*_c(T^*M).
$$
The $\hat{A}$-genus appears for Dirac operators twisted by a bundle $V$:
$$
\mathrm{ind}\,D_V=\int_M\hat{A}(TM)\,\mathrm{ch}(V),\qquad\hat{A}=\prod_j\frac{x_j/2}{\sinh(x_j/2)},
$$
where $\pm x_j$ are the formal roots of $TM\otimes\mathbb{C}$.

In its three classical special cases the theorem reduces to the three classical topological formulas, and each of them is a *straightening* in the language of the essay:

- **Gauss–Bonnet / Poincaré–Hopf.** For the de Rham complex (the Euler operator $d+d^*$), $\operatorname{ind}=\chi(M)=\int_M e(TM)$, the Euler class. The index of the de Rham straightening is the Euler characteristic.
- **Hirzebruch–Riemann–Roch.** For the Dolbeault operator $\bar\partial:\Omega^{0,\bullet}(L)\to\Omega^{0,\bullet+1}(L)$, $\operatorname{ind}\bar\partial=\int_M \operatorname{ch}(L)\cdot\operatorname{td}(TM)=\chi(M,L)$.
- **Hirzebruch signature theorem.** For the signature operator on a $4k$-manifold, $\operatorname{ind}=\langle L(TM),[M]\rangle=\operatorname{sign}(M)$, the signature.

**The heat-kernel proof, and the local-to-global bridge.** The proof that makes the straightening principle explicit is the heat-kernel proof (Atiyah–Bott–Patodi, *Invent. Math.* **19** (1973), 279–330). The index can be written as
$$
\operatorname{ind} P \;=\; \operatorname{Tr}\, e^{-tP^*P}-\operatorname{Tr}\, e^{-tPP^*}
$$
for every $t>0$ (McKean–Singer), and the expression is independent of $t$ (the two heat semigroups differ by a supercommutator, whose trace vanishes). As $t\to 0^+$, the heat kernel has the local asymptotics
$$
e^{-tP^*P}(x,x)\sim (4\pi t)^{-n/2}\sum_{j\ge 0} a_j(x)\,t^j,
$$
where each $a_j(x)$ is a local density, and $a_0$ is just the fibre rank. The **index density** is the $t^0$ coefficient, i.e. $a_{n/2}(P^*P;x)-a_{n/2}(PP^*;x)$ (for $n$ even). It is a universal polynomial in curvature and in the derivatives of the coefficients. Identifying it with the Atiyah–Singer integrand is due to Patodi, Gilkey and Atiyah–Bott–Patodi (1973), and to Getzler's rescaling for Dirac operators. The theorem is the assertion that
$$
\operatorname{ind} P \;=\; \int_M a(x).
$$
This is the purest form of the straightness principle: **the global topological invariant is the integral of a local density.** But one must be precise about what the integrand is: it is built from *curvature*, a second-order and metric-dependent quantity. The index is a case in which second-order local data integrate to a metric-independent integer. The slogan "the index density is computed in $\mathbb{R}^n$ and is a canonical, choice-free straightening density" should be resisted: the density is a universal polynomial in curvature (and in the derivatives of the coefficients of $P$), so it depends on the metric at the level of the integrand, and only the integral is metric-independent. For the physicist this is the precise mathematical reason why the local chiral anomaly equation $\partial_\mu j_5^\mu = \text{density}$ depends on the local gauge field (and on the metric), while the integrated total anomalous charge is a topological invariant.

**The K-theoretic formulation.** The symbol class lives in compactly supported $K$-theory, $[\sigma(P)]\in K_c(T^*M)=K(D^*M,S^*M)$. The analytic index is a homomorphism $K_c(T^*M)\to\mathbb{Z}$. The topological index uses an embedding $M\subset\mathbb{R}^N$, the Thom isomorphism (the total space of $T^*M$ is stably almost complex) and Bott periodicity. Pairing with $[M]\in K_0(M)$ requires a $K$-orientation of $M$. For a finite covering $\pi$ of degree $d$, $\mathrm{ind}(\pi^*P)=d\cdot\mathrm{ind}\,P$. The Atiyah–Singer axioms (normalization and functoriality) characterize the index; that is a different sense of "unique" from the chain-rule statement in §1.

**The physics of the index.** For the audience at hand the index theorem is not a curiosity; it is *the* theorem.

- **Chiral anomalies.** The Adler–Bell–Jackiw anomaly of a chiral fermion coupled to a gauge field $A$ is the index of the Dirac operator $D_A$: the anomalous divergence $\partial_\mu j^\mu$ is the index density. The anomaly is obtained from the anomaly polynomial $[\hat{A}\,\mathrm{ch}(F)]$ by **descent** (not the reverse).
- **Instantons.** On $\mathbb{R}^4$, the index of the Dirac operator coupled to a gauge field is
$$
\operatorname{ind} D_A \;=\; \int_{\mathbb{R}^4} \operatorname{ch}_2(F_A)\cdot\hat{A}(T\mathbb{R}^4) \;=\; \int_{\mathbb{R}^4} \operatorname{ch}_2(F_A),
$$
and for an $SU(2)$ instanton of charge $k$, $\mathrm{ind}\,D_A=k$ in the fundamental representation and $4k$ in the adjoint; in general it is $2T(R)k$. The zero-mode count is $k$, not $2k$, and the fermion determinant vanishes to order $k$ in the mass. The zero modes are the global content of the local straightening (the symbol of $D_A$), and the instanton number is the index.
- **Witten index.** The Witten index of a supersymmetric quantum mechanics, $\operatorname{Tr}(-1)^F e^{-\beta H}$, is the index of the Dirac operator on the configuration space, and the Atiyah–Singer theorem computes it as $\int_M \hat{A}$. The Witten index is the index, and the index is topological: it is independent of the Hamiltonian (the straightening), depending only on the topological class of the symbol.
- **Index of a family.** For a family of elliptic operators $P_s$ parametrized by a space $B$, the index is a class in $K^0(B)$. The anomaly is carried by the determinant line bundle: curvature gives the local part and holonomy the global part. This is the theorem behind **anomaly inflow** and behind **global anomalies** (Witten's $SU(2)$ anomaly): the global anomaly is a mod-$2$ index of the Dirac operator on a five-dimensional mapping torus, related to $\pi_4(SU(2))=\mathbb{Z}/2$.

**Completion of the grading.** The index theorem completes the straightness principle. The grading was: first-order local $=$ unique and canonical; higher-order local $=$ moduli; global $=$ obstructed. The index theorem adds the fourth case: **when the straightening is given in the form of an elliptic operator, the global calculus is not merely obstructed but canonically determined** — the index is the unique, natural, topological invariant of the symbol. The "kind" of global calculus available is read off from the symbol: the symbol is a canonical object (the straightening), and the index is its unique global invariant. The straightness principle, in its final form, is: *the calculus is a local linearization, its uniqueness is graded by order, and its global content — when the straightening is elliptic — is the index, the unique natural topological invariant of the local straightening data.*

## 12. The table of calculi, and the straightness principle

We can now collect the results of the essay into a single table, organized by the order of the straightening and the uniqueness of the resulting calculus.

| Object | Exists? | Unique? | Freedom or obstruction |
|---|---|---|---|
| Tangent space $T_pM$ | yes | canonical | none |
| Differential $df_p$ | yes | canonical | none |
| Exterior derivative $d$ | yes | unique antiderivation extending $df$ with $d^2=0$ | none |
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

The pattern is the **straightness principle**, stated in its final form:

> **The straightness principle (revised).** A geometric structure on $M$ is a reduction of the frame bundle to a subgroup $G\subset GL_n(\mathbb{R})$. It is locally flat, i.e. locally equivalent to the model on $\mathbb{R}^n$, exactly when it is integrable, and the obstruction has a definite order. For symplectic structures ($G=Sp_{2n}$) the only obstruction is $d\omega\neq0$, a first-order condition, and Darboux's theorem gives normal forms with no local invariants. For Riemannian structures ($G=O(n)$) the intrinsic torsion always vanishes (Levi-Civita), so the first obstruction is the curvature, a second-order condition. For almost complex structures the obstruction is the Nijenhuis tensor (first order; Newlander–Nirenberg). Global obstructions are characteristic classes. In infinite dimensions, the Banach inverse function theorem works, and Nash–Moser (Hamilton) repairs it for tame Fréchet maps. For elliptic operators, the index is the case in which curvature-built local densities integrate to a metric-independent integer.

The straightness is, in the end, the notion of a **local linear model**, and the calculus is the **invariant** of that model. The first-order model is unique, so the first-order calculus is unique. The higher-order model is not unique, so the higher-order calculus is a moduli. The global model is obstructed, so the global calculus is obstructed. And the elliptic global model — the symbol of an elliptic operator — is canonically determined, so its global calculus (the index) is canonically determined: the index is the integral of a curvature-built local density, and it is the unique natural transformation from the straightening data to the integers. This is the content of the essay, and it is the content of differential topology.

**Limits of the principle.** We have argued that the straightening principle *organizes* the results of the essay, and we want to be precise about the force of that claim, because a differential topologist would be right to push back on a stronger reading. The principle is a **thesis, not a theorem**: it is a way of seeing the subject, a unifying vocabulary, not a proposition from which the individual results can be derived. In particular:

- *The principle is local and order-graded; it does not by itself produce the global theorems.* Adams' parallelization, the $h$-cobordism theorem, Freedman's classification of topological $4$-manifolds, and the Atiyah–Singer index theorem are deep, independent results. The straightening principle *names* the question each of them answers (does the global straightening exist, is it unique, what is its invariant?), but it does not *prove* them. The proof of the index theorem, for instance, is the heat-kernel or $K$-theoretic argument, not the straightening.
- *Not every phenomenon discussed is naturally organized by the principle.* The small-divisor analysis in KAM theory is a statement about the Diophantine arithmetic of the frequency vector, not about a local linear model; the uncountability of exotic $\mathbb{R}^4$'s is a statement about the failure of smoothing in dimension four, and it is the *obstruction* to the straightening rather than a consequence of it. These results are *compatible* with the principle (they sit in the "obstructed" and "moduli" rows of the table), but the principle is not what drives their proofs.
- *The principle is silent on the things that matter most in physics.* It tells you that the linear term is canonical and the quadratic term is a moduli, but it does not tell you *which* moduli appear in a given theory, or how they are quantized. The connection between the index and the anomaly is a physical theorem (Fujikawa), not a consequence of the straightening.

The honest statement is therefore: *the straightening principle is a powerful and accurate organizing idea for the local and order-graded content of differential topology, and a useful heuristic for the global content; but it is a lens, not a foundation, and the individual theorems it organizes stand or fall on their own proofs.* We present it as a thesis for that reason, and we invite the reader to judge, result by result, how much of it is load-bearing.

For the mathematical physicist, the moral is simple and load-bearing: **when you expand about a background $x_0$ and keep the linear term, you use the canonical linearization $DF_{x_0}$. It is canonical as a map, but it depends on $x_0$. At a critical point the Hessian is also canonical (this is the Morse lemma); away from critical points, second derivatives require a connection. Curvature is the first local invariant of a metric and appears at second order. When you compute the index of an elliptic operator (the chiral anomaly, the number of instanton zero modes, the Witten index), you integrate a curvature-built local density and obtain an integer that does not depend on the metric. The "straightness" of the calculus is what makes the linear term canonical, the "curvature" is the first local invariant that makes the higher-order term background-dependent, and the "index" is what the failure integrates to — a topological charge, canonical and metric-independent.**

---

## References

- J. Milnor, *Topology from the Differentiable Viewpoint*, University Press of Virginia, 1965; Princeton University Press reprint, 1997.
- J. Milnor, "On the existence of a connection with curvature zero," *Comment. Math. Helv.* **32** (1958), 215–223.
- J. Milnor, "On manifolds homeomorphic to the $7$-sphere," *Ann. of Math.* **64** (1956), 399–405.
- M. Kervaire and J. Milnor, "Groups of homotopy spheres: I," *Ann. of Math.* **77** (1963), 504–537.
- J. Milnor, *Characteristic Classes of Fiber Bundles*, Princeton University Press, 1958.
- R. Bott and J. Milnor, "On the parallelizability of the spheres," *Bull. Amer. Math. Soc.* **64** (1958), 87–89.
- M. Kervaire, "Non-parallelizability of the $n$-sphere for $n>7$," *Proc. Nat. Acad. Sci. USA* **44** (1958), 280–283.
- J. F. Adams, "On the non-existence of elements of Hopf invariant one," *Ann. of Math.* **72** (1960), 20–104; "Vector fields on spheres," *Ann. of Math.* **75** (1962), 603–632.
- M. Hirsch, *Differential Topology*, Springer, 1976.
- M. Hirsch, "Immersions of manifolds," *Trans. Amer. Math. Soc.* **93** (1959), 242–276.
- V. Guillemin and A. Pollack, *Differential Topology*, Prentice-Hall, 1974.
- J. M. Lee, *Introduction to Smooth Manifolds*, 2nd ed., Springer, 2013.
- M. Gromov, *Partial Differential Relations*, Springer, 1986.
- J. Nash, "$C^1$-isometric imbeddings," *Ann. of Math.* **60** (1954), 383–396.
- N. Kuiper, "On $C^1$-isometric imbeddings I, II," *Indag. Math.* **17** (1955), 545–556, 683–689.
- J. Nash, "The imbedding problem for Riemannian manifolds," *Ann. of Math.* **63** (1956), 20–63.
- J. Nash, "Analyticity of the solutions of implicit function problems with analytic data," *Ann. of Math.* **84** (1966), 345–355.
- J. Moser, "A new technique for the construction of solutions of nonlinear differential equations," *Proc. Nat. Acad. Sci. U.S.A.* **47** (1961), 1824–1831.
- J. Moser, "A rapidly convergent iteration method and non-linear partial differential equations – I," *Ann. Scuola Norm. Sup. Pisa* **20** (1966), 265–315.
- R. Hamilton, "The inverse function theorem of Nash and Moser," *Bull. Amer. Math. Soc.* **7** (1982), 65–222.
- S. Smale, "Differentiable dynamical systems," *Bull. Amer. Math. Soc.* **73** (1967), 747–817.
- B. Mazur, "A note on some contractible $4$-manifolds," *Ann. of Math.* **73** (1961), 221–228.
- R. Gompf, "An infinite set of exotic $\mathbb{R}^4$'s," *J. Differential Geom.* **21** (1985), 283–300.
- C. H. Taubes, "Gauge theory on asymptotically periodic $4$-manifolds," *J. Differential Geom.* **25** (1987), 363–430.
- R. Gompf and A. Stipsicz, *$4$-Manifolds and Kirby Calculus*, AMS, 1999.
- S. K. Donaldson and P. B. Kronheimer, *The Geometry of Four-Manifolds*, Oxford University Press, 1990.
- E. Witten, "Topological quantum field theory," *Comm. Math. Phys.* **117** (1988), 353–386.
- E. Witten, "Monopoles and four-manifolds," *Math. Res. Lett.* **1** (1994), 769–796.
- E. Witten, "Supersymmetry and Morse theory," *J. Differential Geom.* **17** (1982), 661–692.
- M. F. Atiyah and I. M. Singer, "The index of elliptic operators. I," *Ann. of Math.* **87** (1968), 484–530.
- M. F. Atiyah and G. B. Segal, "The index of elliptic operators. II," *Ann. of Math.* **87** (1968), 531–545.
- M. F. Atiyah and I. M. Singer, "The index of elliptic operators. III," *Ann. of Math.* **87** (1968), 546–604.
- M. F. Atiyah and I. M. Singer, "The index of elliptic operators. IV," *Ann. of Math.* **93** (1971), 119–138.
- M. F. Atiyah and I. M. Singer, "The index of elliptic operators. V," *Ann. of Math.* **93** (1971), 139–149.
- M. F. Atiyah, R. Bott and V. K. Patodi, "On the heat equation and the index theorem," *Invent. Math.* **19** (1973), 279–330.
- K. Fujikawa, "Path-integral measure for gauge-invariant fermion theories," *Phys. Rev. Lett.* **42** (1979), 1195–1198.
- K. Fujikawa, "Path integral for gauge theories with fermions," *Phys. Rev. D* **21** (1980), 2848–2858.

*End of essay.*
