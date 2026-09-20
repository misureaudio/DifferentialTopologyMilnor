# differential topology - straightness v2 - review 2

##

I'll start by looking at how to read the file.**Short answer:** the essay is well organized, and most of its standard textbook statements are correct. It also has a lot of mistakes: misattributions, garbled proofs, some outright false statements, and a thesis that its own examples contradict. I wouldn't circulate it as is, especially to an audience of analysts and mathematical physicists who will notice.

## What holds up

These are correct as stated:

- The local forms (constant rank, immersion, flow box).
- Sard and the regular value theorem.
- The Levi-Civita theorem and the Christoffel formula.
- The second Bianchi identity and its contraction.
- Θ₇ ≅ ℤ/28.
- The existence of uncountably many exotic ℝ⁴'s.
- The openness of the smooth 4D Poincaré conjecture.
- The Banach/Fréchet dichotomy.
- The KAM homological equation.
- The McKean–Singer formula and the three classical special cases of index theory.

## Framing and attribution

- **Milnor's book.** The essay says it follows Milnor's architecture and cites specific sections. As I recall, that book is about Sard–Brown, degree, the Euler number, framed cobordism and the Hopf theorem. It doesn't treat flows, jets, Whitney embedding, or a tangent-bundle chapter, so the "Milnor, Ch. X §Y" citations, including the table's last column, don't check out. The book was originally published by the University Press of Virginia; Princeton reprinted it in 1997.
- **Adams.** The sphere result is usually credited to Bott–Milnor and Kervaire (1958), with Adams giving the sharp Hopf-invariant/vector-field treatment.

## Errors in the local calculus (§1–§5)

- **§2 and §7 (inverse function theorem).** The essay says two functions with the same 2-jet can have inverses that differ at second order. This is false, and it contradicts the sentence before it: the k-jet of f⁻¹ is determined by the k-jet of f. The claim that the formal inverse "doesn't always converge" is also misleading, since the inverse of an analytic map is analytic.
- **§1 (Lie derivative).** The claimed uniqueness of a derivation of the tensor algebra along X that agrees with X on functions is false. Any covariant derivative ∇_X does that too, which undercuts the essay's own point about connections.
- **§3 (weak Whitney).** Off by one. Generic maps Mⁿ→ℝ²ⁿ are immersions, and generic maps to ℝ²ⁿ⁺¹ are embeddings. Generic maps to ℝ²ⁿ⁻¹ have Whitney-umbrella singularities.
- **§3 (Smale–Hirsch).** It concerns regular homotopy, not isotopy.
- **§4 (Morse lemma).** The symmetry group of the normal form is O(k, n−k), not O(n). The stationary-phase phase is e^{iπ·sgn(Hess)/4}, not e^{iπk/2}.
- **§4 (transversality).** "Generic hyperplane section" is loose, and the Thom transversality theorem is about a single map's jet extension, not "families".
- **§5 (flow and Darboux).**
  - The ODE γ̇ = X(γ) is nonlinear, not "linear".
  - Volume preservation follows from ω^n being the volume form, not from Darboux.
  - Darboux charts are hugely non-unique, so "sharpest possible uniqueness" and "canonical" are wrong. Darboux holds because dω = 0, not because "the first jet determines ω".

## Errors in global topology (§6, §8, §9)

- **§6 (parallelizability).** The abstract says a parallelization exists "only in dimensions 0, 1, 3, 7". That is true for spheres only; tori and Lie groups are parallelizable in every dimension. The claim that global straightening is "a function of its dimension" is likewise wrong.
- **§6 (division algebras).** The normed division algebras have dimensions 1, 2, 4, 8, not 1, 3, 7.
- **§6 (characteristic classes).** Pontryagin classes are not obstructions to a complex structure. And Euler and Pontryagin classes are not "the obstructions to parallelization": every sphere has vanishing Pontryagin and Stiefel–Whitney classes, yet only three are parallelizable.
- **§6 (Riemann–Roch).** The Riemann–Roch remark about TS² is garbled.
- **§8 (connections).** The space of connections is affine; the moduli space is its quotient by the gauge group. The Bianchi identities are not why curvature is a tensor.
- **§8 (curvature formula).** It has repeated indices.
- **§9 (the exotic ℝ⁴ construction).** As written it is incoherent. The interior of a Mazur manifold is not ℝ⁴ minus a point, and you can't glue a B⁴ onto a boundary that isn't S³. The invoked "h-cobordism in dimension 3" isn't a thing here, and the uncountability argument ("uncountable space of embeddings") isn't a valid argument.
- **§9 (dates and attributions).**
  - Milnor's exotic sphere paper is 1956, not 1961.
  - Gompf gave infinitely many exotic ℝ⁴'s in 1985, and Taubes gave uncountably many in 1987.
  - ℝ³ has a unique smooth structure by Moise, not by the Poincaré conjecture.
- **§9 (exotic 7-spheres).** The 28 classes are not distinguished by the bundle's Euler number, which equals 1 for homotopy spheres; the Eells–Kuiper/Milnor invariant does that. Not all 28 arise as S³-bundles over S⁴. Milnor's construction doesn't use the triviality of TS⁷.
- **§9 (physics).** Witten's TQFT reading of Donaldson invariants is 1988; 1994 is Seiberg–Witten. The instanton number is topological, so "topological and sensitive to smooth structure" is contradictory.

## Errors in the infinite-dimensional analysis (§10)

- **Nash and Moser history.**
  - Nash's C¹ theorem is 1954 (Kuiper 1955).
  - Nash proved the C^∞ case in his 1956 paper.
  - Moser's abstraction is 1961–66.
  - The N = n(3n+11)/2 bound is for compact manifolds and C^k with k ≥ 3, not "k ≥ 1".
- **The linearization.** DF_f is written as a Lie derivative on tangent vector fields. It is actually h ↦ symmetrized (df·dh) for h ∈ C^∞(M, ℝᴺ).
- **Derivatives lost or gained.** The essay says (DF)⁻¹ "loses derivatives" and then that it "gains k".
- **Tame Fréchet spaces.** These are not "a topology slightly weaker than C^∞".
- **KAM.**
  - 1/(ω·k) grows like |k|^{+τ}, not |k|^{−τ}.
  - The Kolmogorov nondegeneracy hypothesis is missing.
  - The analytic case needs no smoothing.
- **Moser's stability theorem.** It is unrelated to Nash–Moser.

## Errors in the index theorem (§11)

- **The formula.** The general formula uses the Todd class of TM⊗ℂ with the symbol's Chern character on T*M. Â belongs to Dirac-type operators.
- **The heat-kernel index density.** The essay says it is a₀^{P*P} − a₀^{PP*}. But a₀ is just the fiber rank; the index density is the a_{n/2} coefficient, and it is built from curvature. This undermines the essay's punchline that the density is "computed in the flat straightening".
- **The heat-kernel proof.** It is Atiyah–Bott–Patodi (1973), not "Atiyah–Singer II".
- **K-theory.** The symbol class lives in compactly supported K(T*M), not K⁰(T*M∖0). The pairing with a fundamental class needs a K-orientation, and the "f_* vs f*" naturality statement is incoherent.
- **Instantons.** An SU(2) instanton of charge k gives k fundamental zero modes (4k in the adjoint), not 2k.

## References

Several entries don't match publications I know: the Atiyah–Singer I–V volumes and dates are wrong. The "Spectral asymptotics and the index theorem" title, "Differentiable structures on S⁷", Nash "II (1963)", the two Moser entries, the Hirsch 1961 paper, the 1992 Witten paper, and the Zumino–Witten entry all look wrong. Milnor's flat-connection paper is *Comment. Math. Helv.* 32 (1958), not *Pacific J. Math.* Please check all of them against MathSciNet.

## The central thesis

The "grading by order" (first order unique, higher order moduli, global obstructed) is a useful slogan but not a theorem, and the essay's own examples break it:

- The Hessian at a critical point is canonical, which the Morse section itself says.
- Levi-Civita is unique at order 2.
- The index density is a curvature quantity.
- The table mixes existence questions ("parallelization of Sⁿ: No") with uniqueness questions.
- The closing claim that a linearization is "independent of the background" is false. Perturbation theory about different backgrounds gives different results.
- Much of what it calls "moduli" is a choice of extra structure (a metric, a connection), not non-uniqueness of a straightening.

I can go through these and give corrected statements, or write a cleaned-up version, if you'd like.
