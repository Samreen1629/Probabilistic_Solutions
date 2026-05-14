## Task 1 — Discrete Distribution Given by a PMF Table

### Setup

The PMF is given by:

| $x$ | $-2$ | $0$ | $1$ | $3$ | $5$ |
|---|---|---|---|---|---|
| $P(X=x)$ | $0.10$ | $0.25$ | $0.30$ | $0.20$ | $0.15$ |

---

### Step 1 — Constructing a Probability Space $\Omega$

We need a finite sample space $\Omega$ and a random variable $X:\Omega\to\mathbb{R}$ that produces the given PMF.

The simplest construction: let $\Omega$ consist of five elementary outcomes, one for each value in the support:

$$\Omega = \{\omega_1, \omega_2, \omega_3, \omega_4, \omega_5\}$$

Define the probability of each outcome to match the desired PMF:

$$P(\{\omega_1\}) = 0.10,\quad P(\{\omega_2\}) = 0.25,\quad P(\{\omega_3\}) = 0.30,\quad P(\{\omega_4\}) = 0.20,\quad P(\{\omega_5\}) = 0.15$$

Define the random variable:

$$X(\omega_1) = -2,\quad X(\omega_2) = 0,\quad X(\omega_3) = 1,\quad X(\omega_4) = 3,\quad X(\omega_5) = 5$$

Then by construction $P(X = x) = P(\{\omega : X(\omega) = x\})$ recovers the table exactly.

---

### Step 2 — Validity Check

A PMF is valid if and only if:
1. All probabilities are non-negative.
2. They sum to 1.

**Check non-negativity:** $0.10, 0.25, 0.30, 0.20, 0.15$ — all positive. ✓

**Check normalization:**

$$0.10 + 0.25 + 0.30 + 0.20 + 0.15 = 1.00 \checkmark$$

The distribution is valid.

---

### Step 3 — Graph of the PMF

The PMF is a set of isolated vertical spikes ("lollipops") at each support point.

### PMF — Probability Mass Function
P(X=x)

    0.35 |
    0.30 |              █
    0.25 |         █    █
    0.20 |         █    █         █
    0.15 |    █    █    █         █         █
    0.10 | █  █    █    █         █         █
    0.05 | █  █    █    █         █         █
    0.00 +--+------+----+---------+---------+----→ x
           -2      0    1         3         5

  Each █ column is a spike of height P(X = x).
  There is zero probability between the support points.

---

### Step 4 — Constructing the CDF

The CDF is defined as $F(x) = P(X \leq x)$. It is a right-continuous step function that jumps at each support point by the corresponding PMF value.

**For $x < -2$:**

$$F(x) = 0$$

**For $-2 \leq x < 0$:**

$$F(x) = P(X = -2) = 0.10$$

**For $0 \leq x < 1$:**

$$F(x) = 0.10 + 0.25 = 0.35$$

**For $1 \leq x < 3$:**

$$F(x) = 0.35 + 0.30 = 0.65$$

**For $3 \leq x < 5$:**

$$F(x) = 0.65 + 0.20 = 0.85$$

**For $x \geq 5$:**

$$F(x) = 0.85 + 0.15 = 1.00$$

**Summary table:**

| Interval | $F(x)$ |
|---|---|
| $x < -2$ | $0$ |
| $-2 \leq x < 0$ | $0.10$ |
| $0 \leq x < 1$ | $0.35$ |
| $1 \leq x < 3$ | $0.65$ |
| $3 \leq x < 5$ | $0.85$ |
| $x \geq 5$ | $1.00$ |

---

### Step 5 — Graph of the CDF

The CDF is a right-continuous staircase function. Filled circles (•) mark the value the function takes at the jump point (right endpoint); open circles (○) show the value just before the jump.

### CDF — Cumulative Distribution Function
F(x)

    1.00 |                                   ●────────
    0.95 |
    0.90 |
    0.85 |                         ●────────○
    0.80 |
    0.75 |
    0.70 |
    0.65 |              ●─────────○
    0.60 |
    0.55 |
    0.50 |
    0.45 |
    0.40 |
    0.35 |         ●───○
    0.30 |
    0.25 |
    0.20 |
    0.15 |
    0.10 | ●───────○
    0.05 |
    0.00 ○─────────────────────────────────────────→ x
         -3   -2   -1    0    1    2    3    4    5    6

  ● = value taken at the jump point (right-continuous)
  ○ = left-hand limit just before the jump

---

### Step 6 — Relationship Between CDF Jumps and PMF

At every support point $a$, the CDF has a jump of size:

$$\Delta F(a) = F(a) - F(a^-) = P(X = a)$$

where $F(a^-)$ denotes the left-hand limit. Between support points the CDF is flat — no probability mass lies there.

Concretely:

| Point $a$ | $F(a^-)$ | $F(a)$ | Jump $= P(X=a)$ |
|---|---|---|---|
| $-2$ | $0$ | $0.10$ | $0.10$ |
| $0$ | $0.10$ | $0.35$ | $0.25$ |
| $1$ | $0.35$ | $0.65$ | $0.30$ |
| $3$ | $0.65$ | $0.85$ | $0.20$ |
| $5$ | $0.85$ | $1.00$ | $0.15$ |

**The CDF encodes the entire PMF in its jumps.** Wherever the CDF is flat, there is no probability mass.

---

### Step 7 — Computing Probabilities

We use $a = 1$ and $b = 3$ as representative values.

**$P(X = 1)$:** read directly from the PMF:

$$P(X = 1) = 0.30$$

Via CDF: $F(1) - F(1^-) = 0.65 - 0.35 = 0.30$. ✓

**$P(X \leq 1)$:**

$$P(X \leq 1) = F(1) = 0.65$$

**$P(X < 1)$:**

$$P(X < 1) = F(1^-) = F(1) - P(X=1) = 0.65 - 0.30 = 0.35$$

Equivalently: sum of PMF values at $\{-2, 0\}$: $0.10 + 0.25 = 0.35$. ✓

**$P(1 < X \leq 3)$:**

$$P(1 < X \leq 3) = F(3) - F(1) = 0.85 - 0.65 = 0.20$$

This picks up exactly the mass at $x = 3$.

**$P(X \geq 1)$:**

$$P(X \geq 1) = 1 - P(X < 1) = 1 - F(1^-) = 1 - 0.35 = 0.65$$

Equivalently: $0.30 + 0.20 + 0.15 = 0.65$. ✓

**$P(-2 \leq X \leq 3)$:**

$$P(-2 \leq X \leq 3) = F(3) - F(-2^-) = 0.85 - 0 = 0.85$$

Or directly: $0.10 + 0.25 + 0.30 + 0.20 = 0.85$. ✓

---

### Step 8 — Comparison: PMF vs CDF

| Task | PMF approach | CDF approach |
|---|---|---|
| $P(X = a)$ | Read directly | $F(a) - F(a^-)$ |
| $P(X \leq a)$ | Sum all $p(x)$ for $x \leq a$ | $F(a)$ directly |
| $P(X < a)$ | Sum all $p(x)$ for $x < a$ | $F(a) - P(X=a)$ |
| $P(a < X \leq b)$ | Sum $p(x)$ on $(a,b]$ | $F(b) - F(a)$ |
| $P(X \geq a)$ | Sum all $p(x)$ for $x \geq a$ | $1 - F(a^-)$ |

The PMF is more natural for point probabilities and small sums; the CDF is more efficient for cumulative or interval probabilities.
      
        PMF spike        CDF jump         Cumulative total
     ─────────────────────────────────────────────────────────────
    P(X = -2) = 0.10  →  0.00 ──→ 0.10   (total so far: 0.10)
    P(X =  0) = 0.25  →  0.10 ──→ 0.35   (total so far: 0.35)
    P(X =  1) = 0.30  →  0.35 ──→ 0.65   (total so far: 0.65)
    P(X =  3) = 0.20  →  0.65 ──→ 0.85   (total so far: 0.85)
    P(X =  5) = 0.15  →  0.85 ──→ 1.00   (total so far: 1.00)
     ─────────────────────────────────────────────────────────────
         Sum = 1.00                             F(∞) = 1.00

> **Key insight:** The PMF shows *where* probability sits as isolated spikes.
> The CDF shows *how much has accumulated* up to each point.
> Every spike height in the PMF equals exactly the jump size in the CDF at that same point.
> Between the support points {-2, 0, 1, 3, 5} the PMF is zero and the CDF is flat.
