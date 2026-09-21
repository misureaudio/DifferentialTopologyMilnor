# differential topology - straightness - v0 - review 4

Below, each item is a replacement statement you can drop into the essay, in section order. A few are hedged where I'm not fully certain, and the reference details need checking against the originals.

## Framing

- **Plan blockquote.** Milnor's book covers smooth manifolds and maps, regular values, Sard–Brown, degree mod 2, oriented manifolds and the Brouwer degree, vector fields and the Euler number, and framed cobordism and the Hopf theorem. Flows, jets, transversality in full, Whitney embedding and Smale–Hirsch should be cited to Hirsch, *Differential Topology*, and Lee, *Introduction to Smooth Manifolds*. Drop the "Milnor reference" column from the §12 table or fill it in with those sources.
- **Publication.** Milnor's book is University Press of Virginia (1965), reprinted by Princeton in 1997.

## §1–§2 First-order calculus and the inverse function theorem

- **Cotangent space.** $T_p^*M \cong \mathfrak{m}_p / \mathfrak{m}_p^{2}$, and TₚM is its dual.

- **Differential.** dfₚ is the unique linear map satisfying f(p+h) = f(p) + Lh + o(|h|). The chain rule says (M,f) ↦ (TM,df) is a functor. Delete "unique natural transformation".
- **Exterior derivative.** d is the unique antiderivation of degree +1 on Ω• that agrees with the differential on functions. Then d² = 0 follows automatically.
- **Lie derivative.** 𝓛_X is the unique derivation of the tensor algebra that commutes with contractions, acts as X on functions, and acts as [X,·] on vector fields. Without the last condition, any ∇_X qualifies.
- **Inverse function theorem.** D(f⁻¹) = (Df)⁻¹, and the k-jet of f⁻¹ at f(p) is determined by the k-jet of f at p. Only in the trivial sense are finite jets not enough: a C^∞ germ is not determined by its jets. If f is real-analytic (or holomorphic), f⁻¹ is analytic and its Taylor series converges.
- **Palais.** A proper local diffeomorphism between connected manifolds is a covering map. If the target is simply connected, it is a diffeomorphism. Properness implies covering; the two are not equivalent.

## §3 Immersions and embeddings

- **General position.** For a generic smooth map Mⁿ → ℝᵐ, singularities occur in codimension m−n+1. So generic maps are immersions for m ≥ 2n and embeddings for m ≥ 2n+1 (compact M). The Whitney numbers come from this dimension count, not from "jets".
- **Strong Whitney.** Every smooth n-manifold (closed or not) embeds in ℝ²ⁿ, and immerses in ℝ²ⁿ⁻¹ for n > 1.
- **Smale–Hirsch.** For m > n (or M open), Imm(M,N) → Mono(TM,TN), f ↦ df, is a weak homotopy equivalence. In particular, immersions up to *regular homotopy*, not isotopy, correspond to bundle monomorphisms up to homotopy.
- **Embeddings.** Isotopy classes of embeddings are not determined by df (knots in S³). Remove the "Embedding (global) | order 1" row.

## §4 Transversality and Morse theory

- **Sard.** For almost every c, f⁻¹(c) is a submanifold. Delete "generic hyperplane section" and the time-slice remark.
- **Thom transversality.** For any submanifold W of Jᵏ(M,N), the set of f with jᵏf ⋔ W is residual in the Whitney C^∞ topology. Families are the parametric transversality theorem.
- **Morse lemma.** There are coordinates with f = f(p) − y₁² − … − yₖ² + yₖ₊₁² + … + yₙ². The index k is the invariant (Sylvester). The charts are not canonical; the linear symmetry group of the normal form is O(k, n−k), not O(n).
- **Stationary phase.** ∫e^{iλf}a dx ~ (2π/λ)^{n/2} |det Hess f(p)|^{-1/2} e^{iλf(p)} e^{iπ·sgn(Hess f(p))/4} a(p), with sgn = n − 2k.

## §5 Flows, Darboux

- **Flow.** γ̇ = X(γ) is a nonlinear autonomous ODE; uniqueness is Picard–Lindelöf. The flow is global only if X is complete.
- **Liouville.** L_{X_H}ω = 0 implies L_{X_H}ωⁿ = 0, and ωⁿ/n! is the volume form. Darboux is not involved.
- **Darboux.** Near every point there are coordinates in which ω = Σ dxⁱ∧dxⁿ⁺ⁱ. These coordinates are wildly non-unique: the freedom is the whole local symplectomorphism group. The theorem holds because dω = 0 (Moser's trick), not because "the first jet determines ω".

## §6 The tangent bundle

- **Abstract and §6.** TSⁿ is trivial iff n ∈ {0,1,3,7}. This is Bott–Milnor and Kervaire (1958) plus Adams (Hopf invariant one, 1960; vector fields on spheres, 1962). For general manifolds parallelizability depends on the manifold: tori, Lie groups and orientable 3-manifolds are parallelizable. Delete "a function of its dimension".
- **Division algebras.** ℝ, ℂ, ℍ, 𝕆 have dimensions 1, 2, 4, 8, and S⁰, S¹, S³, S⁷ are their unit spheres. Hopf-invariant-one maps S²ⁿ⁻¹ → Sⁿ exist only for n = 1, 2, 4, 8.
- **Characteristic classes.** The Euler class is the primary obstruction to a nonvanishing section of an oriented rank-n bundle. Vanishing of Stiefel–Whitney, Pontryagin and Euler classes is necessary for triviality but not sufficient: S⁵ is stably parallelizable but not parallelizable. Pontryagin classes pᵢ(E) = (−1)ⁱc₂ᵢ(E⊗ℂ) are defined for every real bundle. A complex structure on E imposes relations on them, but they are not "the obstruction" to one.
- **TS².** As a complex line bundle over ℂP¹, TS² ≅ O(2), so e = c₁ = 2. The Hopf bundle is O(−1). Delete the Riemann–Roch sentence.
- **Products.** Ω(M₁)⊗Ω(M₂) is dense in Ω(M₁×M₂) (equal after completed tensor product). Künneth holds on cohomology.

## §7 Jets

- **Jets are jets of functions.** jᵏₚf is the class of f in C^∞ₚ/𝔪ₚᵏ⁺¹. The 1-jet is (f(p), dfₚ). Jᵏ is a bundle whose transition functions are polynomial in higher derivatives of the coordinate change. The splitting "gradient + Hessian" is coordinate-independent only at a critical point, or given a connection.
- **Moduli of straightenings.** The freedom in a higher-order straightening is measured by jets of coordinate changes, i.e. the group Gᵏ of k-jets of diffeomorphisms, an extension of GLₙ by a unipotent group. A torsion-free connection is a GLₙ-equivariant splitting of the second-order frame bundle onto the first-order one.
- **Morse–Bott.** f = f|_C + |y|² − |z|², where y, z are fibre coordinates on the positive and negative eigenbundles of the normal Hessian. It generalizes Morse to degenerate critical manifolds, not to "higher order".
- **Morse homology.** For a Morse function f and a metric with (f,g) Morse–Smale, the Morse–Smale–Witten complex computes H_*(M) (Witten, Floer, Smale/Milnor). There is no "Morse–Weyl theorem".
- **Physics.** A bounce's single negative mode gives the imaginary part of the energy (the decay rate). The one-loop prefactor comes from the quadratic fluctuation determinant, and higher-order terms give higher loops. θ-dependence comes from topological charge, and fermion zero modes come from the index.

## §8 Connections and curvature

- **Space of connections.** On a vector bundle it is an affine space over Ω¹(M; End E); for a principal G-bundle, over Ω¹(M; ad P). The moduli space is the quotient by the gauge group.
- **Levi-Civita proof.** Koszul: 2g(∇_XY,Z) = Xg(Y,Z) + Yg(X,Z) − Zg(X,Y) + g([X,Y],Z) − g([X,Z],Y) − g([Y,Z],X). Metric-compatibility and zero torsion force this, so ∇ is unique; the formula defines it, so ∇ exists.
- **Normal coordinates.** Rᵢⱼₖₗ(p) = ½(∂ⱼ∂ₖgᵢₗ + ∂ᵢ∂ₗgⱼₖ − ∂ᵢ∂ₖgⱼₗ − ∂ⱼ∂ₗgᵢₖ).
- **Geodesics.** Uniqueness of Levi-Civita says the metric determines the connection. Uniqueness of a geodesic with given initial data is ODE theory. Connections with torsion can share geodesics with Levi-Civita.
- **Bianchi and tensoriality.** R(X,Y)Z is a tensor because it is C^∞(M)-linear in X, Y, Z. The Bianchi identities are differential identities (d_∇R = 0), not the reason for tensoriality.
- **Nash.**
  - C¹ isometric embeddings: Nash 1954 (N ≥ n+2), Kuiper 1955 (N ≥ n+1).
  - Nash 1956 proved the C^k case for 3 ≤ k ≤ ∞ with N = n(3n+11)/2 for compact M and n(n+1)(3n+11)/2 for noncompact. His C^∞ case uses his own smoothing iteration.
  - Moser (1961) isolated the method, and Hamilton (1982) gave the abstract theorem.
  - Later work (Gromov, Günther) lowered N substantially.
- **Non-uniqueness.** Isometric embeddings are far from unique, even up to rigid motion: C¹ is flexible (Nash–Kuiper), while some C² cases are rigid (convex surfaces). Delete "unique up to rigid motions".

## §9 Smooth structures and exotic spheres

- **Exotic ℝ⁴.** Freedman's classification plus Donaldson's theorem give the first exotic ℝ⁴ (early 1980s). Gompf (1985) found infinitely many and Taubes (1987) uncountably many, via gauge theory on end-periodic manifolds. Mazur's 1961 contractible manifold is a compact smooth contractible 4-manifold with non-simply-connected boundary, so it is not a 4-ball. It is not the exotic-ℝ⁴ construction. I'd delete the Mazur–B⁴ gluing paragraph and the uncountability argument, and cite Gompf–Stipsicz instead.
- **Uniqueness of ℝⁿ.** It is classical for n ≤ 2, Moise for n = 3 (not Perelman), and Stallings/smoothing theory for n ≥ 5.
- **Exotic spheres.** Milnor's paper is 1956. It uses S³-bundles over S⁴ with Euler number 1, which are homotopy 7-spheres. A Morse function with two critical points shows they are homeomorphic to S⁷, and a Hirzebruch-signature/Pontryagin-class invariant shows some are not diffeomorphic to it. Θ₇ ≅ ℤ/28 is Kervaire–Milnor (1963), with the Eells–Kuiper invariant μ. As I recall, only 16 of the 28 classes arise as bundle spheres. TS⁷ is not used.
- **Θₙ.** It is finite for n ≥ 5 but often nonzero. Exotic spheres and exotic ℝⁿ are different phenomena: an exotic Sⁿ minus a point is standard ℝⁿ for n ≥ 5.
- **Poincaré, 4D.** Freedman: every simply connected closed topological 4-manifold homotopy equivalent to S⁴ is homeomorphic to S⁴. The smooth version is open. Exotic ℝ⁴ does not by itself imply exotic S⁴.
- **Physics.** Witten's TQFT reading of Donaldson invariants is 1988; the 1994 paper is the Seiberg–Witten monopole equations. The instanton number c₂ is topological. The instanton moduli space and the Donaldson invariants are what depend on the smooth structure. Delete the "vacuum structure" sentence.

## §10 Infinite dimensions

- **Hamilton's theorem.** For a smooth tame map F between tame Fréchet spaces, if DF(x) is invertible for all x near x₀ and the inverse forms a smooth tame family, then F is a local diffeomorphism with smooth tame inverse. Tameness is extra structure (grading and smoothing operators), not a weaker topology.
- **Derivative loss.** In Nash–Moser settings the right inverse of DF satisfies ‖(DF_x)⁻¹y‖ₛ ≲ ‖y‖ₛ₊ᵣ for a fixed r (r = 1 or 2 for isometric embedding, τ for KAM). Plain Newton loses r derivatives per step. Smoothing operators S_θ satisfy ‖S_θu‖ₛ₊ₐ ≲ θᵃ‖u‖ₛ and ‖(1−S_θ)u‖ₛ ≲ θ⁻ᵃ‖u‖ₛ₊ₐ. The iteration xₙ₊₁ = xₙ − S_{θₙ}(DF_{xₙ})⁻¹F(xₙ), with θₙ growing fast, converges superexponentially.
- **Isometric embedding.** F(f) = f*δ − g, and DF_f(h)(u,v) = ⟨df u, dh v⟩ + ⟨dh u, df v⟩ for h ∈ C^∞(M,ℝᴺ). The Lie-derivative formula belongs to tangential h = df(X). The linearization has a differential-operator right inverse at "free" maps, which need N ≥ n(n+3)/2.
- **KAM.** Diophantine means |ω·k| ≥ γ|k|^{-τ} (τ ≥ n−1, and τ > n−1 for full measure). So 1/|ω·k| ≤ |k|^τ/γ, and the inverse of ω·∂_θ loses about τ derivatives. Add the Kolmogorov nondegeneracy condition (det ∂ω/∂I ≠ 0). In the analytic case (Kolmogorov, Arnold) a quadratic Newton scheme works without smoothing. Smoothing is needed for finite differentiability (Moser). The conclusion is that invariant tori with Diophantine frequencies persist, symplectically conjugate to linear flows, forming a Cantor family of large measure. Delete "the smoothing operator is a canonical transformation".
- **Moser's stability theorem.** It is the volume/symplectic-form deformation result and is unrelated to Nash–Moser.
- **Regularity.** The Banach inverse function theorem holds for C^k maps for every k. What fails is the Fréchet topology plus lost derivatives, not "C^∞ vs C¹".

## §11 Index theorem

- **Formula.** ind P = (−1)ⁿ ∫_{T*M} ch(σ(P)) · Td(TM⊗ℂ), with ch(σ(P)) ∈ H_c*(T*M). Â appears for twisted Dirac operators: ind D_V = ∫_M Â(TM) ch(V), with Â = ∏ (xⱼ/2)/sinh(xⱼ/2) over the formal roots ±xⱼ of TM⊗ℂ.
- **Heat kernel.** The index is Tr e^{−tP*P} − Tr e^{−tPP*} for every t > 0. The local expansion is (4πt)^{-n/2} Σ aⱼ(x)tʲ, with a₀ the fibre rank. The index density is a_{n/2}(P*P;x) − a_{n/2}(PP*;x), the t⁰ coefficient. It is a universal polynomial in curvature and coefficient derivatives. Proving it equals the Atiyah–Singer integrand is Patodi/Gilkey/Atiyah–Bott–Patodi (1973), with Getzler's rescaling later for Dirac operators.
- **Consequence for the thesis.** The integrand is built from curvature, a second-order and metric-dependent quantity. The index is the case where second-order data integrate to a metric-independent invariant. Delete "computed in ℝⁿ", "no moduli" and "canonical straightening density".
- **K-theory.** [σ(P)] ∈ K_c(T*M) = K(D*M, S*M). The analytic index is a homomorphism K_c(T*M) → ℤ. The topological index uses an embedding M ⊂ ℝᴺ, the Thom isomorphism (T*M is stably almost complex), and Bott periodicity. Pairing with [M] ∈ K₀(M) requires a K-orientation. For a finite covering π of degree d, ind(π*P) = d·ind P; drop the "f_* for proper maps" claim. The index is characterized by normalization and functoriality (the Atiyah–Singer axioms). That is a different sense of "unique" from the chain rule in §1.
- **Instantons.** For an SU(2) instanton of charge k, ind D_A = k in the fundamental representation and 4k in the adjoint (2T(R)k in general). The zero-mode count is k, not 2k.
- **Anomalies.**
  - The anomaly is obtained from the anomaly polynomial [Â ch(F)] by descent, not the other way round.
  - Witten's SU(2) anomaly is a mod-2 index of the Dirac operator on a 5-dimensional mapping torus (π₄(SU(2)) = ℤ₂).
  - For families, the index is a K-class, and its determinant line bundle carries the anomaly: curvature gives the local part, holonomy the global part. It is not an "obstruction to a family of sections".
- **AS I–V.** I and III are Ann. Math. 87 (1968); II (Atiyah–Segal) is 87 (1968); IV and V are 93 (1971). "ABP" is *Invent. Math.* 19 (1973), "On the heat equation and the index theorem".

## §12 Table and thesis

- **Table rows.**
  - Exterior derivative: unique antiderivation extending df.
  - Lie derivative: unique commuting-with-contractions derivation with [X,·] on vector fields.
  - Inverse: kᵗʰ jet of f⁻¹ determined by kᵗʰ jet of f.
  - Symplectic: Darboux normal form exists; charts form a torsor for local symplectomorphisms.
  - Morse: normal form exists; index unique; charts non-unique.
  - Immersions: regular homotopy classes ↔ monomorphisms.
  - Parallelization of Sⁿ: existence iff n ∈ {0,1,3,7}. When it exists, parallelizations differ by maps Sⁿ → GLₙ.
  - Fréchet: fails in general; Nash–Moser (Hamilton) works for tame families.
  - Index: depends only on the class of σ(P) in K_c(T*M).
  - Add an "existence vs uniqueness" column. The current table mixes the two.
- **Thesis.** Replace "graded by order: unique vs moduli" with the integrability of G-structures. A straightening of a G-structure exists locally iff the structure is integrable, and the obstruction has a definite order:
  - Symplectic (Sp): integrable iff dω = 0, a first-order condition. Darboux has no local invariants.
  - Riemannian (O(n)): integrable iff curvature vanishes, a second-order condition. Its first local invariant is curvature.
  - Complex: integrable iff the Nijenhuis tensor vanishes (Newlander–Nirenberg).
  - Global obstructions are characteristic classes.

  This organizes the essay's actual examples, and the Hessian and Levi-Civita cases no longer contradict it.
- **Closing paragraph for physicists.** The linearization Dfₓ is canonical as a map but depends on the background x. The Hessian at a critical point is canonical. Away from critical points, second derivatives need a connection. Curvature is a local invariant of the metric. The index is where curvature integrates to a topological number.

## References

I'm confident of these:
- Milnor, *Ann. Math.* 64 (1956) 399–405.
- Kervaire–Milnor, *Ann. Math.* 77 (1963) 504–537.
- Milnor, *Comment. Math. Helv.* 32 (1958) 215–223.
- Nash, *Ann. Math.* 60 (1954) and 63 (1956) 20–63.
- Moser, *PNAS* 47 (1961).
- Hamilton, *Bull. AMS* 7 (1982).
- Bott–Milnor, *Bull. AMS* 64 (1958).
- Kervaire, *PNAS* 44 (1958).
- Adams, *Ann. Math.* 72 (1960) and 75 (1962).
- Witten, *JDG* 17 (1982), *CMP* 117 (1988), *Math. Res. Lett.* 1 (1994).

For Hirsch, use "Immersions of manifolds", *Trans. AMS* 93 (1959); I'm less sure of the page range. I'd remove the entries I flagged as unmatched last time rather than repair them from memory.

If it would help, I can put the corrected essay into a file, with these fixes applied in place.