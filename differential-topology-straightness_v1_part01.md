# The Straightness of the Calculus

## Differential Topology after Milnor, and the Uniqueness of the Infinitesimal

*An essay for mathematical physicists and analysts*

> **On the plan.** This essay follows the architecture of John Milnor's *Topology from the Differentiable Viewpoint* (Princeton, 1965): differentiable maps and the inverse function theorem (§1–§2), immersions and embeddings (§3), submanifolds and regular values (§4), vector fields and flows (§5), the tangent bundle (§6), and transversality and jets (§7). To that skeleton I add three chapters that the 1965 book leaves implicit but that the theme demands: connections, curvature, and the uniqueness of the Levi-Civita connection (§8); the non-uniqueness of the smooth structure — the exotic $\mathbb{R}^4$ and the exotic spheres (§9); and the failure, then repair, of the straightening in infinite dimensions — the Banach and Fréchet inverse function theorems and the Nash–Moser method (§10). A single idea runs through the whole: *the calculus is what remains when the manifold is straightened, and the question of which calculi exist, and which of them are unique, is precisely the question of how much of the straightening is canonical.*

### Abstract

The differential calculus on a smooth manifold is a local linearization: a chart "straightens" the manifold to $\mathbb{R}^n$, and the tangent space, the exterior derivative, and the Lie derivative are the invariants of that straightening. This essay argues that the notion of *straightness* — the existence of a local affine model — is the organizing principle of differential topology, and that its consequences amount to a taxonomy of the possible calculi together with a precise accounting of which of them are unique (canonical) and which are not.

The first-order calculus is unique: the tangent space is the same object whether defined as equivalence classes of curves or as derivations, and the Fréchet derivative is the unique best linear approximation to a map at a point. The higher-order calculus is not unique: the $k$-jet for $k\ge 2$ is not determined by the $1$-jet, and the spaces of connections and of metrics are genuine moduli spaces. The global calculus is obstructed: a parallelization of the tangent bundle exists only in dimensions $0,1,3,7$ (Adams), and the smooth structure on $\mathbb{R}^n$ is unique for $n\neq 4$ but is *not* unique in dimension $4$, where there are uncountably many exotic $\mathbb{R}^4$'s. In infinite dimensions the straightening succeeds in Banach spaces (the inverse function theorem) but fails in Fréchet spaces, and is repaired by the Nash–Moser implicit function theorem — the method behind the $C^\infty$ Nash isometric embedding theorem and the KAM theory. We close with a table of calculi and their uniqueness, and with the observation that straightness is, in the end, the notion of a local linear model, and that the "kind" of calculus a space admits is read off from how rigidly that model is determined.

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

*(Milnor, Ch. 1, §§1.1–1.2.)*

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
the dual of the quotient of the maximal ideal by its square. The quotient $\mathfrak{m}_p/\mathfrak{m}_p^2$ is the **first-order neighborhood** of $p$ in the algebraic sense: it is what remains of the ring of functions once one throws away everything of order $\ge 2$. That this quotient is independent of any analytic input — no metric, no connection, no chart — is the algebraic content of the statement that *the first-order structure is canonical*.

**The derivative as unique best linear approximation.** Let $f : M \to N$ be smooth and $p\in M$. The differential $df_p : T_pM \to T_{f(p)}N$ is characterized by the following uniqueness property: it is the **unique** linear map $L : T_pM \to T_{f(p)}N$ such that, in charts,
$$
f(p+h) = f(p) + L h + o(\|h\|) \qquad (h\to 0).
$$
This is the Fréchet characterization. The point for our theme is the word *unique*. Given the straightening (a pair of charts), the first-order behavior of $f$ is captured by exactly one linear map. There is no choice, no moduli, no moduli space: the linear part of the Taylor expansion is a **functor** of the straightening, and the chain rule
$$
d(g\circ f)_p = dg_{f(p)} \circ df_p
$$
says that the assignment $f \mapsto df$ respects composition. The derivative is the unique natural transformation from the functor of smooth maps to the functor of linear maps between tangent spaces. In the language of the audience at hand: $df$ is the unique natural transformation, and the chain rule is the statement of its naturality.

Two consequences are worth isolating.

- **The exterior derivative.** The $1$-form $df$ on $M$ (for $f:M\to\mathbb{R}$) is the pullback of the standard $1$-form $dx$ on $\mathbb{R}$ under the straightening. Its coordinate-free definition, $df_p(v) = D_v f$ for $v\in T_pM$, is chart-independent for the same reason the tangent space is: it is a first-order object, and first-order objects are canonical. The full de Rham complex $\Omega^\bullet(M)$, built from $df$ by alternation, is therefore a canonical first-order calculus. This is the calculus that a physicist uses when writing $dA = F$ for a gauge potential $A$: the $d$ is the unique first-order operator that is antisymmetric in its arguments and satisfies $d^2=0$.

- **The Lie derivative.** For a vector field $X$ and a tensor field $T$, the Lie derivative $\mathcal{L}_X T$ is the infinitesimal action of the flow of $X$ on $T$. It is again a first-order object: it depends on $X$ and $T$ only through their values and first derivatives at a point. Its uniqueness is the statement that there is a unique derivation of the algebra of tensor fields along a given vector field that agrees with the ordinary derivative on functions. The Lie derivative is, in this sense, the unique "infinitesimal straightening of the frame" generated by $X$.

So at the local, first-order level, the straightening is rigid. Every object one can define — $T_pM$, $T_p^*M$, $\Omega^\bullet(M)$, $\mathcal{L}_X$, the differential — is canonical, independent of the chart, and unique. The calculus at first order is **the** calculus, not *a* calculus.

---

## 2. The inverse function theorem: local straightening, and its uniqueness up to higher order

*(Milnor, Ch. 1, §1.2, and the constant rank theorem.)*

The inverse function theorem is the engine that turns the *definition* of a manifold into a *theorem* about it, and it is where the "uniqueness up to higher order" theme first appears.

**Theorem (inverse function theorem).** Let $f: U\subset\mathbb{R}^n \to \mathbb{R}^n$ be $C^1$, and suppose $Df(p)$ is invertible. Then there are neighborhoods $V\ni p$ and $W\ni f(p)$ such that $f|_V : V \xrightarrow{\;\sim\;} W$ is a $C^1$ diffeomorphism.

The proof (Milnor's is a contraction argument) shows something stronger than the statement: the inverse is constructed explicitly, and its first derivative is
$$
D(f^{-1})_{f(p)} = (Df_p)^{-1}.
$$
That is, the first-order behavior of the inverse is *exactly* the inverse of the first-order behavior of the map. The straightening and its un-straightening agree to first order, canonically. What the theorem does **not** control is the higher-order behavior: the inverse function is determined, to all orders, by the formal inverse of the Taylor series of $f$, but the actual (convergent) inverse is not determined by any finite jet of $f$. Two functions with the same $2$-jet at $p$ can have inverses that differ to second order. The straightening is unique to first order, and only *formally* unique to higher order.

This is the germ of the theme. Let me state it as a principle that will recur:

> **Principle (grading by order).** The straightening of a manifold at a point is *canonical* in degree $1$, *formal* (determined up to a choice of coordinates) in degree $\ge 2$, and *obstructed* globally. The calculi that live in degree $1$ are unique; the calculi that live in degree $\ge 2$ are moduli.

The **constant rank theorem** is the inverse function theorem with the invertibility hypothesis weakened to a constant-rank hypothesis, and it is the workhorse that produces submanifolds.

**Theorem (constant rank).** If $f:U\subset\mathbb{R}^n\to\mathbb{R}^m$ has constant rank $r$ near $p$, then there are coordinates in which
$$
f(x_1,\dots,x_n) = (x_1,\dots,x_r,0,\dots,0).
$$
In words: *locally, a constant-rank map is straight.* This is the strongest local form of the theme. A map of constant rank is, after a change of coordinates on source and target (i.e., after re-straightening), exactly a projection. The "curvature" of a constant-rank map is zero, locally. What the theorem does not say — and what the rest of the essay is about — is that the re-straightening is not unique, and that the failure of global straightness is measured by invariants (curvature, characteristic classes) that are invisible to the constant rank theorem.

The inverse function theorem has a global cousin that a functional analyst will recognize: **Palais's global inverse function theorem**, which gives conditions under which a local diffeomorphism that is a proper map (equivalently, a covering map with suitable hypotheses) is a global diffeomorphism. The moral is the same: local straightening, plus a global topological hypothesis (properness, simply-connectedness of the target), upgrades to global straightening. The gap between the local and the global is exactly the gap that characteristic classes measure.

