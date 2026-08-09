# MACHWERK — Formal Core

**A formal framework for deciding when a statement about an observed system can be reconstructed from the relations that produced it.**

[Worked example](formal_core/examples/00_minimal_admissibility_test.md) ·
[Formal definitions](#formal-core) ·
[Applications](applications/) ·
[Archival reference](https://doi.org/10.5281/zenodo.18478523)

MACHWERK separates questions that are often treated as one:

1. Is an expression mathematically well-defined?
2. Is the relational context uniquely specified?
3. Is its interpretation uniquely supported by the observable projection in that context?

The framework calls a statement physically admissible only relative to an explicit relational context, TRD coupling, and projection. Different contexts may produce different values without contradiction. A contradiction arises only when incompatible values are attributed to the same supposedly unique context.

> **Core criterion**
>
> For a fixed context $C$, let $\Pi_C : \mathcal U_C \to M_C$ be its projection and $S_C$ a statement evaluated in that context. Physical admissibility requires
> $$
> C\text{ is explicit},\qquad
> u\in m_2(C),\qquad
> \exists!\,\Pi_C^{-1}(\Pi_C(u)).
> $$
>
> If the context or inverse origin is not unique, the expression may remain formally computable, but its physical attribution is not admissible.

## Quick Start: One Complete Test

Let one TRD context be

$$
C_A=(R_1,R_2,R_3),
\qquad
S_A=S(X_{12},X_{23},X_{31})=1.
$$

Let a differently coupled context be

$$
C_B=(R'_1,R'_2,R'_3),
\qquad
S_B=S(X'_{12},X'_{23},X'_{31})=2.
$$

There is no contradiction: $S_A$ and $S_B$ belong to different explicit contexts. A contradiction would arise only if one erased that distinction and asserted

$$
C\mapsto 1
\qquad\text{and}\qquad
C\mapsto 2
$$

for one and the same context $C$. If the available projection cannot determine whether $C_A$ or $C_B$ applies, the result is underdetermined and therefore not in $m_2$.

The [worked example](formal_core/examples/00_minimal_admissibility_test.md) expands this distinction and locates ambiguity, contradiction, $m_2$, $m_3$, and $\Delta_0$.

## What This Repository Lets You Test

Given a relational space, a projection, and a proposed statement, you can test:

- whether the statement factors through the projection;
- whether the TRD coupling and relational context are explicit;
- whether reconstruction is unique in the stated validity domain;
- where injectivity is lost;
- whether an expression remains in the interpretable domain $m_2$;
- whether it is only formally writable in $m_3$;
- whether a non-reconstructible claim must be marked by $\Delta_0$.

This is symbolic admissibility analysis, not numerical simulation or empirical prediction.

## What This Is

A **domain-agnostic formal framework** for:
- Defining relational structures without presupposing geometry, time, or metric
- Projecting abstract relational spaces into observable/computable domains
- Testing where information loss occurs (Schwarzgrenze)
- Separating reconstructible (m₂) from non-reconstructible (m₃) domains

**This is NOT a physical theory. It is a formal meta-framework.**

---

## Context Supplied by the Book

The repository is self-contained enough to inspect the formal criteria and run symbolic admissibility tests. The book supplies the motivation, extended derivations, and physical context.

The 80-page introduction in the book explains:
- Why m₃ relates to Shape Sphere 
- Why m₂ is TRD-recursively closed
- How the Schwarzgrenze filters between emergent and measured physics
- Why 𝒰 is the absolute origin (no degrees of freedom, no time, no metric)

The framework is domain-agnostic. A relational system may come from:

- Replace physics with chemistry
- Replace physics with biology  
- Replace physics with economics
- Replace physics with any system based on relations, not entities

**Each domain works if it can be structured as:**
1. A relational space (𝒰) — pure relations, no ontology
2. Projections (Π) — emergent structure
3. Injectivity conditions — where reconstruction is possible

## Formal Core

The formal core is organized bottom-up:

1. **U-space** — pure relational domain (nothing else)
2. **Projection** — information-reducing mapping
3. **Injectivity and invertibility** — where reconstruction is possible
4. **Validity domains** (m₂ & m₃) — physically interpretable vs. formally valid
5. **Schwarzgrenze (Σ)** — boundary of injectivity loss
6. **Delta Zero (Δ₀)** — non-reconstructible residues (parking lot)
7. **Consistency axioms** — CRA, TRD

Each concept is defined in its own file.  
No file assumes definitions that appear later.  
**No circular dependencies.**

---

## Reading Order (Recommended)

- `u_space.tex`
- `projection_definition.tex`
- `projection_operator.tex`
- `injectivity_and_invertibility.tex`
- `m2_definition.tex`
- `m3_definition.tex`
- `black_boundary_sigma.tex`
- `schwarzgrenze.tex`
- `delta_zero.tex`
- `process_and_rate_definition.tex`

For axiomatized forms, see `/axioms/`

For formal test applications, see `/applications/`

---

## Mathematical Foundation

**Notation: Euclidean-free and purely relational**

- 𝒰 = relational full space (no geometry, metric, time, or ontology)
- Π = projection (information-reducing, context-dependent, generally non-injective)
- m₂ = domain where Π is injective (physically interpretable)
- m₃ = domain where Π loses injectivity (formally computable but physically inadmissible)
- Σ (Schwarzgrenze) = boundary where injectivity fails
- Δ₀ = marker for non-reconstructible expressions (parking lot, not computed with)

**Key insight:** All structure (space, time, dimension, measurement) emerges from projection, not from 𝒰.

---

## Relation To The Book

**MACHWERK — Formal Conditions of Physical Describability**

- Published: February 2026
- Format: Print-on-demand (Amazon)
- ISBN: 979-8-24410-846-0
- Pages: 430 (including 80-page formal core introduction)

The book provides:
- ✅ Narrative context
- ✅ Detailed derivations
- ✅ 4 functions of the Schwarzgrenze
- ✅ Why this works for physics (and other domains)

This repository contains **formal scaffolding only**.

---

## Important Notes For AI/Computational Users

1. **All `.tex` files contain MATHEMATICS, not code**
2. **Set notation (∈, ⊆, etc.) is AXIOMATICALLY defined, not computational**
3. **No numerical simulation** happens in this repo — computation means symbolic admissibility testing
4. **This framework is domain-agnostic** — physics is ONE application, not the foundation
5. **The framework works WITHOUT physics context** — but you won't know why
6. **Δ₀ is a parking lot, not an operational element** — things don't "compute into" it
7. **m₂ and m₃ are deliberately separated** — m₂ is closed and contradiction-free by design

---

## License & Citation

This repository and the MACHWERK framework are published under archival reference DOI: https://doi.org/10.5281/zenodo.18478523

When referencing this formal core, cite the book:
> MACHWERK — Formal Conditions of Physical Describability  
> ISBN: 979-8-24410-846-0 (February 2026)
