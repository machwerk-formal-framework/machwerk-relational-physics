# Minimal Context-Admissibility Test

This example separates three cases that must not be conflated:

1. different values in different explicit contexts;
2. an underdetermined context;
3. incompatible values asserted in one fixed context.

## 1. Two explicit TRD contexts

Let

$$
C_A=(R_1,R_2,R_3)
$$

be one explicitly specified TRD coupling, with

$$
X_{12}=\frac{R_1}{R_2},\qquad
X_{23}=\frac{R_2}{R_3},\qquad
X_{31}=\frac{R_3}{R_1}.
$$

Suppose the statement evaluated in this context is

$$
S_A=S(X_{12},X_{23},X_{31})=1.
$$

Let

$$
C_B=(R'_1,R'_2,R'_3)
$$

be a differently coupled or differently referenced TRD context, producing

$$
S_B=S(X'_{12},X'_{23},X'_{31})=2.
$$

There is no contradiction:

$$
C_A\mapsto 1,
\qquad
C_B\mapsto 2,
\qquad
C_A\ne C_B.
$$

Each result may be admissible in its own validity domain, provided the corresponding projection is injective and CRA is satisfied.

## 2. Context-relative validity domains

For each explicit context define its projection separately:

$$
\Pi_A:\mathcal U_A\to M_A,
\qquad
\Pi_B:\mathcal U_B\to M_B.
$$

Then

$$
m_2(C_A)=\{u\in\mathcal U_A\mid\Pi_A\text{ is injective at }u\}
$$

and

$$
m_2(C_B)=\{u\in\mathcal U_B\mid\Pi_B\text{ is injective at }u\}.
$$

The values `1` and `2` do not compete for one assignment because they belong to different explicitly identified relational contexts.

## 3. Underdetermined context

Assume an observable description does not determine whether $C_A$ or $C_B$ applies. It therefore supports the alternatives

$$
(C_A,S_A=1)
\qquad\text{or}\qquad
(C_B,S_B=2)
$$

without selecting one of them.

This is not yet a logical contradiction. It is contextual underdetermination:

$$
\nexists!\,C.
$$

Because the applicable relational origin and coupling cannot be reconstructed uniquely, the attribution is not admissible in $m_2$. It may remain formally represented in $m_3$.

## 4. Contradiction inside one fixed context

Now suppose the context, coupling, projection, and relational state are all fixed, but the same statement is assigned two incompatible values:

$$
S_C(u)=1
\qquad\text{and}\qquad
S_C(u)=2.
$$

Because $1\ne2$, these assertions cannot both hold under the same fixed conditions. This is a genuine contradiction and is excluded from $m_2(C)$.

## 5. CRA diagnosis

CRA requires all quantities in a physical statement to share:

- one relational validity domain;
- one projection boundary;
- one explicit relational context;
- one TRD coupling;
- no implicit category transition.

Treating $S_A$ and $S_B$ as if they belonged to one context violates CRA. Keeping $C_A$ and $C_B$ explicit preserves consistency.

## 6. Role of TRD

TRD supplies the minimal comparison structure

$$
S=S(X_{12},X_{23},X_{31}).
$$

It is invariant under a global rescaling

$$
(R_1,R_2,R_3)\mapsto(\lambda R_1,\lambda R_2,\lambda R_3),
$$

because the ratios remain unchanged. A different coupling or reference structure, however, defines a different context and must be labeled accordingly.

## 7. Decision rule

For any proposed physical statement:

1. State the relational context and TRD coupling explicitly.
2. State the projection associated with that context.
3. Test whether the relational origin is uniquely reconstructible.
4. Evaluate all quantities inside the same context and validity domain.
5. If different values arise from different explicit contexts, retain both as context-relative results.
6. If the context cannot be selected uniquely, mark the attribution as underdetermined and outside $m_2$.
7. If incompatible values are asserted in the same fixed context, reject the statement as contradictory.

The framework therefore keeps $m_2$ contradiction-free without requiring different relational contexts to produce identical values.
