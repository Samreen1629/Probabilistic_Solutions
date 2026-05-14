## Problem 6 — The Axiomatic Point of View

### Introduction

Throughout Problems 1–5 we worked at two levels: the structural level of events as subsets of a sample space, and the empirical level of observed frequencies. The axiomatic formulation of probability — due to Andrey Kolmogorov (1933) — is the step that turns the patterns observed at those two levels into a precise mathematical theory.

---

### The Kolmogorov Axioms

Let $\Omega$ be a sample space and let $\mathcal{F}$ be a collection of subsets of $\Omega$ (called events) that is closed under the relevant operations. A **probability measure** is a function

$$P : \mathcal{F} \to \mathbb{R}$$

satisfying the following three axioms:

**Axiom 1 — Non-negativity:**

$$P(A) \geq 0 \quad \text{for all } A \in \mathcal{F}$$

**Axiom 2 — Normalization:**

$$P(\Omega) = 1$$

**Axiom 3 — Countable additivity ($\sigma$-additivity):**

For any sequence of pairwise disjoint events $A_1, A_2, A_3, \ldots \in \mathcal{F}$:

$$P\!\left(\bigcup_{i=1}^{\infty} A_i\right) = \sum_{i=1}^{\infty} P(A_i)$$

---

### What Our Earlier Work Already Suggested

**Non-negativity** appeared immediately. The observed frequency $f(A) = n(A)/n$ is a ratio of a non-negative count to a positive total — it can never be negative. Any function intended to measure "how often" an event occurs must therefore be non-negative. Axiom 1 is not an arbitrary choice; it is the direct formalization of this observation.

**Normalization** followed just as naturally. In Part D of Problem 5, we saw that $f(\Omega) = 1$ because every trial produces exactly one outcome in $\Omega$, so $n(\Omega) = n$ always. Axiom 2 captures this exactly: the certain event has probability 1.

**Finite additivity** — the statement that for disjoint $A \cap B = \emptyset$:

$$P(A \cup B) = P(A) + P(B)$$

— was verified repeatedly in Problem 5. It holds for frequencies because no trial can simultaneously fall into two disjoint sets, so counts simply add. The general finite case follows by induction: for any finite collection of pairwise disjoint events $A_1, \ldots, A_k$:

$$P\!\left(\bigcup_{i=1}^{k} A_i\right) = \sum_{i=1}^{k} P(A_i)$$

This was precisely the content of Part D's general statement about decompositions of $\Omega$.

---

### What Goes Beyond Finite Experiments: Countable Additivity

Finite additivity is enough when the sample space $\Omega$ is finite — as in all our examples (a die, two coins, a week of weather). In that setting, every event is a finite union of elementary outcomes, and the finite additivity of $P$ on singletons determines $P$ on all events.

However, many important probability spaces have **infinitely many outcomes**. Consider, for example, counting how many coin tosses are needed until the first head, or modeling the exact time at which a radioactive atom decays. In these cases $\Omega$ is countably or uncountably infinite, and finite additivity alone is insufficient to handle limits and infinite unions.

**Countable additivity** strengthens the requirement: the probability of a countably infinite union of disjoint events must equal the sum of the infinite series of probabilities. This is a non-trivial analytic assumption — it is equivalent to saying that $P$ is **continuous from above** (or below) with respect to decreasing (or increasing) sequences of events:

$$A_n \searrow \emptyset \implies P(A_n) \to 0$$

This continuity property cannot be derived from finite experiments or finite sample spaces. No matter how many trials we run, we observe finitely many outcomes. The passage from "finitely additive" to "countably additive" is therefore a genuine **mathematical idealization**: we are asserting that probability behaves well under limiting operations, which is necessary for the full apparatus of mathematical analysis — integrals, expectations, limit theorems — to apply.

---

### Why the Axioms Are Minimal and Natural

The Kolmogorov axioms are remarkable for what they do **not** say. They do not require that outcomes be equally likely. They do not specify how $P$ is assigned — whether by symmetry, by limiting frequencies, by subjective belief, or by physical theory. They only impose the structural constraints that any coherent notion of "likelihood" must satisfy.

From these three axioms alone, all standard consequences follow immediately:

- $P(\emptyset) = 0$ (the impossible event has probability zero)
- $P(A^c) = 1 - P(A)$ (complement rule)
- $P(A \cup B) = P(A) + P(B) - P(A \cap B)$ (inclusion-exclusion)
- $A \subseteq B \implies P(A) \leq P(B)$ (monotonicity)

Each of these was already visible at the level of observed frequencies. The axioms package all of them into a single coherent structure.

---

### Summary

The axiomatic approach completes the journey traced across Problems 1–5:

- We began with **concrete outcomes** organized into a sample space.
- We described **events** as subsets and translated logical operations into set operations.
- We observed that **frequencies** always satisfy non-negativity, normalization, and finite additivity.
- We recognized these as structural features that any measure of likelihood should have.
- We **abstracted** these features into axioms, freeing probability from any single experiment.
- Finally, we extended finite additivity to **countable additivity**, which is the crucial step that makes probability a branch of rigorous mathematical analysis rather than merely an empirical summary.

The Kolmogorov axioms are not a description of the world. They are a precise mathematical framework within which probability — however it is interpreted or assigned — must operate consistently.
