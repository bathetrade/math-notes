---
header-includes: |
    - \let\vec\mathbf
    - \let\M\parenMatrixstack
    - \let\;\quad
    - \def\nullsp{\mathcal{N}}
    - \def\qed{\hfill\blacksquare}
    - \DeclareMathOperator\sgn{sgn}
    - \DeclareMathOperator\dim{dim}
    - \DeclareMathOperator\row{row}
    - \DeclareMathOperator\col{col}
    - \DeclareMathOperator\span{span}
    - \DeclareMathOperator\ker{ker}
    - \DeclareMathOperator\im{im}
    - \DeclareMathOperator\rank{rank}
    - \DeclareMathOperator\det{det}
    - \DeclareMathOperator\Rot{Rot}
---

# $σᵢ(A)$ Formula

First note that the determinant is multi-linear, so we can write
$$ A = \M{
    a₁₁ - x, ⋯  ;
    ⋯, aₙₙ - x
} = \M{
    a₁₁, ⋯  ;
    ⋯, aₙₙ
} - \M{
    x, ⋯    ;
    ⋯, aₙₙ
} - \M{
    x, ⋯    ;
    ⋯, aₙₙ
} + \M{
    x, ⋯    ;
    ⋯, x
} $$

Assume we have a single $aᵢᵢ = x$. We are only interested in the coefficient for $x$.
Fixing $π$ and using the Leibniz formula, we get
$$ k = -x ∑_{π ∈ S(n) : π(i)=i} \sgn(π) a_{1π(1)} ⋯ a_{(i-1)π(i-1)} a_{(i+1)π(i+1)} ⋯ a_{nπ(n)} $$
Using the same argument as for the Laplace expansion, when we have $P_π$, and delete the $i$th column and row,
then $P_π' = P_{π'}$ corresponds to a valid $π' ∈ S(n - 1)$. Then $\sgn(π) = \sgn(π')$, since the element
at $π(i) = i$ is already in the identity position.
$$ k = -x \det(Aᵢᵢ) $$
Using the multilinearity we see
$$ σ₁(A) = -x ∑ᵢ₌₁ⁿ \det(Aᵢᵢ) $$

We can generalize the argument above, by fixing $π(i₁) = i₁, …, π(iₘ) = iₘ$. Then we sum over the permutations
for the remaining minor matrices $A₍ₙ₋ₘ₎₍ₙ₋ₘ₎$. Note that in the multilinear expansion, the leading unit is $(-1)ᵐ$.

Thus we get the generalized formula for characteristic polynomial.
