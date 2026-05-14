# Task 1 — Discrete Distribution Given by a PMF Table

We are given a discrete random variable $X$ together with its probability mass function (PMF).

The PMF is specified by the table:

| $x$ | $-2$ | $0$ | $1$ | $3$ | $5$ |
|---|---|---|---|---|---|
| $P(X=x)$ | $0.10$ | $0.25$ | $0.30$ | $0.20$ | $0.15$ |

The PMF directly tells us how probability is distributed among the possible values of the random variable.

---

# 1. Constructing a Probability Space

We now construct one possible finite probability space $\Omega$ together with a random variable $X$ whose PMF is exactly the one given in the table.

---

## Step 1 — Define the sample space

One possible choice is:

$$
\Omega=\{\omega_1,\omega_2,\omega_3,\omega_4,\omega_5\}
$$

Each elementary outcome will correspond to one value of the random variable.

---

## Step 2 — Assign probabilities

We define:

| Outcome | Probability |
|---|---|
| $\omega_1$ | $0.10$ |
| $\omega_2$ | $0.25$ |
| $\omega_3$ | $0.30$ |
| $\omega_4$ | $0.20$ |
| $\omega_5$ | $0.15$ |

---

## Step 3 — Define the random variable

We define the mapping:

| Outcome | $X(\omega)$ |
|---|---|
| $\omega_1$ | $-2$ |
| $\omega_2$ | $0$ |
| $\omega_3$ | $1$ |
| $\omega_4$ | $3$ |
| $\omega_5$ | $5$ |

This construction ensures:

$$
P(X=-2)=0.10
$$

$$
P(X=0)=0.25
$$

$$
P(X=1)=0.30
$$

$$
P(X=3)=0.20
$$

$$
P(X=5)=0.15
$$

Thus the random variable has exactly the required PMF.

---

# 2. Verifying That This Is a Valid Probability Distribution

A valid probability distribution must satisfy two conditions:

1. every probability must be between 0 and 1,
2. the total probability must equal 1.

---

## Step 1 — Check Nonnegativity

All probabilities are nonnegative:

$$
0.10,\ 0.25,\ 0.30,\ 0.20,\ 0.15 \ge 0
$$

Thus the first condition is satisfied.

---

## Step 2 — Check Normalization

We compute:

$$
0.10+0.25+0.30+0.20+0.15
$$

$$
=1.00
$$

Therefore:

$$
\sum_x P(X=x)=1
$$

The PMF is valid.

---

# 3. Graph of the Probability Mass Function

The PMF assigns probability mass to isolated points.

Graphically:

```text
Probability

0.30 |                 ●
0.25 |         ●
0.20 |                           ●
0.15 |                                       ●
0.10 | ●
0.05 |
0.00 +------------------------------------------------
        -2          0          1          3         5
```

Each point represents the probability:

$$
P(X=x)
$$

for the corresponding value of $x$.

Unlike continuous distributions, probability is concentrated at separate points.

---

# 4. Constructing the Cumulative Distribution Function

The cumulative distribution function (CDF) is defined by:

$$
F(x)=P(X\le x)
$$

The CDF accumulates probability as we move from left to right along the real line.

---

## Step 1 — Compute Cumulative Probabilities

---

### For $x<-2$

No values are included yet:

$$
F(x)=0
$$

---

### For $-2\le x<0$

Only the value $-2$ is included:

$$
F(x)=0.10
$$

---

### For $0\le x<1$

We include $-2$ and $0$:

$$
F(x)=0.10+0.25=0.35
$$

---

### For $1\le x<3$

We include $-2,0,1$:

$$
F(x)=0.10+0.25+0.30
$$

$$
=0.65
$$

---

### For $3\le x<5$

We include $-2,0,1,3$:

$$
F(x)=0.85
$$

---

### For $x\ge5$

All probability is included:

$$
F(x)=1
$$

---

# 5. Table of the CDF

| Interval | $F(x)$ |
|---|---|
| $x<-2$ | $0$ |
| $-2\le x<0$ | $0.10$ |
| $0\le x<1$ | $0.35$ |
| $1\le x<3$ | $0.65$ |
| $3\le x<5$ | $0.85$ |
| $x\ge5$ | $1.00$ |

---

# 6. Graph of the CDF

The CDF is a step function.

```text
F(x)

1.00 |                                   ┌──────────
0.85 |                           ┌───────┘
0.65 |                   ┌───────┘
0.35 |           ┌───────┘
0.10 |   ┌───────┘
0.00 |───┘
      +------------------------------------------------
         -2        0        1        3        5
```

Important observations:

- the function never decreases,
- the function is right-continuous,
- jumps occur at attainable values of the random variable.

---

# 7. Relation Between PMF and CDF Jumps

For a discrete random variable:

$$
F(x)=P(X\le x)
$$

Whenever the random variable takes a value $a$, the CDF jumps upward by exactly:

$$
P(X=a)
$$

For example:

- jump at $-2$ has size $0.10$,
- jump at $0$ has size $0.25$,
- jump at $1$ has size $0.30$.

Mathematically:

$$
P(X=a)=F(a)-\lim_{x\to a^-}F(x)
$$

Thus:

- the PMF describes individual probability masses,
- the CDF describes accumulated probability.

---

# 8. Computing Probabilities from the PMF

---

## Example 1 — Computing $P(X=1)$

Directly from the PMF:

$$
P(X=1)=0.30
$$

---

## Example 2 — Computing $P(X\le1)$

We add all probabilities up to 1:

$$
P(X\le1)=0.10+0.25+0.30
$$

$$
=0.65
$$

---

## Example 3 — Computing $P(X<1)$

We include only values strictly smaller than 1:

$$
P(X<1)=0.10+0.25
$$

$$
=0.35
$$

---

## Example 4 — Computing $P(0<X\le3)$

Values satisfying this condition are:

$$
1,\ 3
$$

Thus:

$$
P(0<X\le3)=0.30+0.20
$$

$$
=0.50
$$

---

## Example 5 — Computing $P(X\ge1)$

Included values are:

$$
1,\ 3,\ 5
$$

Therefore:

$$
P(X\ge1)=0.30+0.20+0.15
$$

$$
=0.65
$$

---

# 9. Computing the Same Probabilities from the CDF

The same probabilities can also be obtained using cumulative values.

---

## Example — Computing $P(X\le1)$

From the CDF:

$$
F(1)=0.65
$$

---

## Example — Computing $P(X<1)$

We use the value immediately before the jump at 1:

$$
P(X<1)=0.35
$$

---

## Example — Computing $P(X=1)$

Using jumps:

$$
P(X=1)=F(1)-F(0)
$$

$$
=0.65-0.35
$$

$$
=0.30
$$

---

## Example — Computing $P(0<X\le3)$

Using cumulative probabilities:

$$
P(0<X\le3)=F(3)-F(0)
$$

$$
=0.85-0.35
$$

$$
=0.50
$$

---

# 10. Comparing the PMF and the CDF

The PMF and the CDF describe the same distribution, but from different perspectives.

---

## What Is Immediate from the PMF?

The PMF directly shows:

- probabilities of exact values,
- where probability mass is concentrated,
- which outcomes are most likely.

For example:

$$
P(X=1)=0.30
$$

is read immediately from the PMF.

---

## What Is Immediate from the CDF?

The CDF directly shows:

- cumulative probabilities,
- probabilities of intervals,
- probabilities involving inequalities.

For example:

$$
P(X\le3)=0.85
$$

is read immediately from the CDF.

---

# 11. Possible Interactive Application

This distribution could be implemented in a small application.

Possible features:

- user enters PMF values,
- automatic verification that probabilities sum to 1,
- automatic construction of the CDF,
- interactive PMF graph,
- interactive CDF graph,
- probability calculator for events such as:

$$
P(X=a),\quad P(X\le a),\quad P(a<X\le b)
$$

The program could dynamically show how cumulative probability is built from probability masses.

---

# Final Conceptual Observation

This task illustrates one of the central ideas of probability theory:

- the PMF describes how probability is distributed across individual outcomes,
- the CDF describes how probability accumulates across the real line.

For discrete random variables:

- the PMF determines the CDF,
- the CDF determines the PMF through its jumps.

Understanding the relation between these two viewpoints is fundamental for the study of probability distributions.
