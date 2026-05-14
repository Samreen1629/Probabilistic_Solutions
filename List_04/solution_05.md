## Problem 5 — From Recorded Frequencies to Probability

### Setup

A die was rolled $n = 1000$ times. Recorded counts:

| Outcome | $n(\omega)$ |
|---------|------------|
| 1 | 168 |
| 2 | 154 |
| 3 | 181 |
| 4 | 167 |
| 5 | 160 |
| 6 | 170 |
| **Total** | **1000** |

The observed frequency of any event $A \subseteq \Omega$ is defined as:

$$f(A) = \frac{n(A)}{1000}$$

---

### Part A — From Elementary Outcomes to Events

**Event $A = \{2,4,6\}$** (even outcomes)

$$n(A) = n(2) + n(4) + n(6) = 154 + 167 + 170 = 491$$

$$f(A) = \frac{491}{1000} = 0.491$$

**Event $B = \{1,2,3\}$**

$$n(B) = 168 + 154 + 181 = 503$$

$$f(B) = \frac{503}{1000} = 0.503$$

**Event $C = \{5,6\}$**

$$n(C) = 160 + 170 = 330$$

$$f(C) = \frac{330}{1000} = 0.330$$

**Event $D = \{1,3,5\}$** (odd outcomes)

$$n(D) = 168 + 181 + 160 = 509$$

$$f(D) = \frac{509}{1000} = 0.509$$

**Event $E = \{1,2,3,4\}$**

$$n(E) = 168 + 154 + 181 + 167 = 670$$

$$f(E) = \frac{670}{1000} = 0.670$$

---

### Part B — How Frequencies Combine

**Relationship 1:** $f(\{2,4,6\}) = f(\{2\}) + f(\{4\}) + f(\{6\})$

$$f(\{2\}) + f(\{4\}) + f(\{6\}) = \frac{154}{1000} + \frac{167}{1000} + \frac{170}{1000} = \frac{491}{1000} = 0.491 = f(\{2,4,6\})\ \checkmark$$

**Why it holds:** The events $\{2\}$, $\{4\}$, $\{6\}$ are pairwise disjoint — no throw can produce two outcomes at once. The count $n(\{2,4,6\})$ is simply the sum of the individual counts. Dividing each by 1000 and summing gives the frequency of the union.

---

**Relationship 2:** $f(\{1,2,3,4\}) = f(\{1,2\}) + f(\{3,4\})$

$$f(\{1,2\}) = \frac{168+154}{1000} = \frac{322}{1000},\quad f(\{3,4\}) = \frac{181+167}{1000} = \frac{348}{1000}$$

$$f(\{1,2\}) + f(\{3,4\}) = \frac{322+348}{1000} = \frac{670}{1000} = f(\{1,2,3,4\})\ \checkmark$$

**Why it holds:** $\{1,2\}$ and $\{3,4\}$ are disjoint and their union is $\{1,2,3,4\}$, so again we are just partitioning a count.

---

**Relationship 3:** $f(\{1,3,5\}) + f(\{2,4,6\}) = 1$

$$\frac{509}{1000} + \frac{491}{1000} = \frac{1000}{1000} = 1\ \checkmark$$

**Why it holds:** $\{1,3,5\}$ and $\{2,4,6\}$ are complementary — they partition $\Omega$ into two disjoint parts covering all 1000 throws. Every throw belongs to exactly one of them, so their counts sum to 1000.

---

**Relationship 4:** $f(\{5,6\}) = 1 - f(\{1,2,3,4\})$

$$1 - f(\{1,2,3,4\}) = 1 - 0.670 = 0.330 = f(\{5,6\})\ \checkmark$$

**Why it holds:** $\{5,6\}$ and $\{1,2,3,4\}$ are complementary events. Every throw either belongs to $\{1,2,3,4\}$ or to $\{5,6\}$, never to both. So $n(\{5,6\}) = 1000 - n(\{1,2,3,4\})$, and dividing by 1000 gives the frequency identity.

---

### Part C — When Simple Addition Works and When It Fails

**Check for disjoint events:**

$$f(\{1,2\}) = \frac{168+154}{1000} = \frac{322}{1000},\quad f(\{5,6\}) = \frac{160+170}{1000} = \frac{330}{1000}$$

$$f(\{1,2\} \cup \{5,6\}) = \frac{168+154+160+170}{1000} = \frac{652}{1000}$$

$$f(\{1,2\}) + f(\{5,6\}) = \frac{322+330}{1000} = \frac{652}{1000}\ \checkmark$$

This works because $\{1,2\}$ and $\{5,6\}$ are **disjoint** — no overlap.

---

**Now consider overlapping events** $M = \{1,2,3\}$ and $N = \{3,4,5\}$:

$$f(M) = \frac{168+154+181}{1000} = \frac{503}{1000} = 0.503$$

$$f(N) = \frac{181+167+160}{1000} = \frac{508}{1000} = 0.508$$

$$M \cup N = \{1,2,3,4,5\},\quad f(M \cup N) = \frac{168+154+181+167+160}{1000} = \frac{830}{1000} = 0.830$$

$$f(M) + f(N) = 0.503 + 0.508 = 1.011 \neq 0.830$$

**Why do they differ?** The outcome $3 \in M \cap N$ is counted in $n(M)$ and again in $n(N)$. So the sum $f(M)+f(N)$ counts $n(\{3\}) = 181$ twice. To correct this:

$$f(M \cup N) = f(M) + f(N) - f(M \cap N)$$

$$= 0.503 + 0.508 - \frac{181}{1000} = 1.011 - 0.181 = 0.830\ \checkmark$$

This is the **inclusion-exclusion principle**: when events overlap, the intersection must be subtracted to avoid double-counting.

---

### Part D — Covering the Whole Sample Space

**1. Sum of all six elementary frequencies:**

$$\sum_{k=1}^{6} f(\{k\}) = \frac{168+154+181+167+160+170}{1000} = \frac{1000}{1000} = 1$$

**2. Why must this equal 1?**
Every one of the 1000 throws produced exactly one outcome in $\{1,2,3,4,5,6\}$. So the six counts partition the total count of 1000. Dividing by 1000, the frequencies must sum to 1.

**3. Partition $\Omega$ into three disjoint events:** $\{1,2\}$, $\{3,4\}$, $\{5,6\}$.

$$f(\{1,2\}) + f(\{3,4\}) + f(\{5,6\}) = \frac{322}{1000} + \frac{348}{1000} + \frac{330}{1000} = \frac{1000}{1000} = 1\ \checkmark$$

**4. Why is the sum again 1?**
$\{1,2\}$, $\{3,4\}$, $\{5,6\}$ are pairwise disjoint and cover $\Omega$ entirely. Every throw is counted in exactly one of the three groups.

**5. General statement:**

> If $A_1, A_2, \ldots, A_k$ are pairwise disjoint events with $A_1 \cup A_2 \cup \cdots \cup A_k = \Omega$, then:
>
> $$\sum_{i=1}^{k} f(A_i) = 1$$
>
> This holds because the counts $n(A_i)$ partition the total $n$: each trial is counted in exactly one $A_i$, so $\sum n(A_i) = n$, and dividing by $n$ gives the result.

---

### Part E — From Observed Frequency to Probability

From Parts A–D, observed frequency $f$ has the following properties:

1. **Non-negativity:** $f(A) \geq 0$ for all $A \subseteq \Omega$, because $n(A) \geq 0$ always.

2. **Impossible event:** If $A = \emptyset$, no throw can produce an outcome in $A$, so $n(\emptyset) = 0$ and $f(\emptyset) = 0$.

3. **Normalization:** Every throw lands in $\Omega$, so $n(\Omega) = n$ and $f(\Omega) = 1$.

4. **Finite additivity:** For disjoint $A \cap B = \emptyset$:

$$f(A \cup B) = f(A) + f(B)$$

   because a throw in $A \cup B$ is in exactly one of them: $n(A \cup B) = n(A) + n(B)$.

5. **Complement rule:** Since $A$ and $A^c$ are disjoint and $A \cup A^c = \Omega$:

$$f(A) + f(A^c) = f(\Omega) = 1 \implies f(A^c) = 1 - f(A)$$

We now want a **mathematical object** — a function $P$ defined on all subsets of $\Omega$ — that captures these properties in an idealized, exact way, freeing us from any particular experiment. Such a function is called a **probability measure**, and it is defined precisely by these properties as axioms.

---

### Part F — Connecting the Three Levels

The three levels are connected as a progression from concrete experience to abstract formalism:

1. **Elementary outcomes and events (the structural level).**
   We begin by describing the possible results of an experiment and organizing them into a sample space $\Omega$. Events are subsets of $\Omega$. Logical relationships between statements (AND, OR, NOT) translate directly into set operations ($\cap$, $\cup$, complement). This level is purely structural — no numbers appear yet.

2. **Observed frequencies from a real experiment (the empirical level).**
   When we actually run an experiment many times, we observe how often each event occurs. The function $f(A)$ assigns a concrete number to each event based on real data. We discovered that this function is non-negative, equals 1 on $\Omega$, equals 0 on $\emptyset$, and is additive over disjoint events. These are **patterns observed in data**, not assumptions.

3. **Probability as a mathematical abstraction (the axiomatic level).**
   We notice that the properties of $f$ do not depend on the specific numbers obtained in one experiment — they reflect something deeper about the structure of the situation. We abstract away the particular data and declare that any function $P : 2^\Omega \to \mathbb{R}$ satisfying those properties shall be called a probability measure. This gives us a mathematical object that is exact, general, and independent of any particular experimental run.

The movement is: **concrete experiment → observed regularities → axiomatic abstraction**. Probability does not describe any single experiment; it is the idealized limit of what frequencies converge to as the number of trials grows without bound.
