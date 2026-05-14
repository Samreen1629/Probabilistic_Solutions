# Task 2 — Discrete Distribution Given by a CDF Table

We are given a discrete random variable \(X\) together with its cumulative distribution function (CDF).

The values of the CDF are:

| \(x\) | \(-1\) | \(0\) | \(2\) | \(4\) | \(6\) |
|---|---|---|---|---|---|
| \(F(x)\) | \(0.15\) | \(0.35\) | \(0.60\) | \(0.85\) | \(1.00\) |

Recall that the cumulative distribution function is defined by

$$
F(x)=P(X\le x).
$$

For a discrete random variable, the CDF is a **step function**.  
It remains constant between attainable values of the random variable and jumps at the points where the random variable has positive probability.

---

# 1. Constructing a Probability Space

We now construct one possible finite probability space \(\Omega\) together with a random variable \(X\) that produces exactly the given CDF.

---

## Step 1 — Reconstruct the probabilities

For a discrete random variable, the probability at a point equals the jump of the CDF at that point.

Thus:

$$
P(X=-1)=F(-1)=0.15
$$

because there was no probability before \(-1\).

Next:

$$
P(X=0)=F(0)-F(-1)=0.35-0.15=0.20
$$

Similarly:

$$
P(X=2)=0.60-0.35=0.25
$$

$$
P(X=4)=0.85-0.60=0.25
$$

$$
P(X=6)=1.00-0.85=0.15
$$

---

## Step 2 — Verify total probability

We check:

$$
0.15+0.20+0.25+0.25+0.15=1.00
$$

Thus the probabilities form a valid probability distribution.

---

## Step 3 — Construct a sample space

One possible probability space is:

$$
\Omega=\{\omega_1,\omega_2,\omega_3,\omega_4,\omega_5\}
$$

Assign probabilities:

| Outcome | Probability |
|---|---|
| \(\omega_1\) | \(0.15\) |
| \(\omega_2\) | \(0.20\) |
| \(\omega_3\) | \(0.25\) |
| \(\omega_4\) | \(0.25\) |
| \(\omega_5\) | \(0.15\) |

Define the random variable:

| Outcome | \(X(\omega)\) |
|---|---|
| \(\omega_1\) | \(-1\) |
| \(\omega_2\) | \(0\) |
| \(\omega_3\) | \(2\) |
| \(\omega_4\) | \(4\) |
| \(\omega_5\) | \(6\) |

This construction produces exactly the required CDF.

---

# 2. Reconstructing the PMF from the CDF

The probability mass function (PMF) is:

$$
p(x)=P(X=x)
$$

Using the jumps computed above:

| \(x\) | \(-1\) | \(0\) | \(2\) | \(4\) | \(6\) |
|---|---|---|---|---|---|
| \(p(x)\) | \(0.15\) | \(0.20\) | \(0.25\) | \(0.25\) | \(0.15\) |

---

# 3. Graph of the PMF

The PMF is represented by isolated probability masses.

ASCII representation:

```text
Probability
0.25 |                 ●           ●
0.20 |         ●
0.15 | ●                               ●
0.10 |
0.05 |
0.00 +----------------------------------------
        -1          0          2    4      6
```

Each point represents:

$$
P(X=x)
$$

for the corresponding value of \(x\).

---

# 4. Graph of the CDF

The CDF is a step function.

Between jump points it remains constant.

Graphically:

```text
F(x)

1.00 |                             ┌──────────
0.85 |                     ┌───────┘
0.60 |             ┌───────┘
0.35 |     ┌───────┘
0.15 |─────┘
0.00 +----------------------------------------
       -1        0        2        4        6
```

Important observations:

- the function is nondecreasing,
- the function is right-continuous,
- jumps occur exactly where probability mass exists.

---

# 5. Points Where the CDF Jumps

The CDF jumps at:

$$
x=-1,\quad 0,\quad 2,\quad 4,\quad 6
$$

These are exactly the values that the random variable can take.

---

# 6. Why the Jump Size Equals the Probability

For a discrete random variable:

$$
F(x)=P(X\le x)
$$

Suppose the function jumps at \(x=a\).

Immediately before \(a\), the probability \(P(X=a)\) is not yet included.

At \(a\), it suddenly becomes included.

Therefore:

$$
P(X=a)=F(a)-\lim_{x\to a^-}F(x)
$$

Thus:

- the jump size equals the probability mass at that point.

This is one of the most important conceptual properties of discrete distributions.

---

# 7. Computing Probabilities Using the CDF

---

## Example 1 — \(P(X\le 2)\)

By definition:

$$
P(X\le2)=F(2)=0.60
$$

---

## Example 2 — \(P(X<2)\)

We include only values strictly smaller than \(2\):

$$
P(X<2)=P(X=-1)+P(X=0)
$$

Thus:

$$
P(X<2)=0.15+0.20=0.35
$$

Equivalently:

$$
P(X<2)=\lim_{x\to2^-}F(x)=0.35
$$

---

## Example 3 — \(P(X=2)\)

We use the jump:

$$
P(X=2)=F(2)-F(0)
$$

Thus:

$$
P(X=2)=0.60-0.35=0.25
$$

---

## Example 4 — \(P(0<X\le4)\)

Allowed values:

$$
2,\ 4
$$

Thus:

$$
P(0<X\le4)=0.25+0.25=0.50
$$

Using the CDF:

$$
P(0<X\le4)=F(4)-F(0)
$$

Hence:

$$
0.85-0.35=0.50
$$

---

## Example 5 — \(P(X>0)\)

We use the complement:

$$
P(X>0)=1-P(X\le0)
$$

Therefore:

$$
P(X>0)=1-0.35=0.65
$$

---

# 8. Comparing PMF and CDF

The PMF and the CDF describe the same distribution, but they emphasize different aspects.

---

## Information immediate from the PMF

From the PMF we immediately see:

- exact probabilities of individual values,
- which values are most likely,
- how probability mass is distributed.

For example:

$$
P(X=4)=0.25
$$

is read directly from the PMF.

---

## Information immediate from the CDF

From the CDF we immediately see:

- cumulative probabilities,
- probabilities of intervals,
- probabilities of inequalities.

For example:

$$
P(X\le4)=0.85
$$

is read directly from the CDF.

The CDF also immediately shows:

- monotonicity,
- accumulation of probability,
- total probability approaching 1.

---

# 9. Extending an Application to Accept CDF Input

If an application originally accepted only PMF input, it can be extended to accept a CDF table.

The procedure would be:

1. read the ordered CDF values,
2. compute successive jumps,
3. reconstruct the PMF automatically,
4. use the PMF internally for calculations.

Algorithmically:

$$
P(X=x_i)=F(x_i)-F(x_{i-1})
$$

with the convention:

$$
F(x_{-1})=0
$$

This allows the program to work with either representation of a discrete distribution.

---

# Final Conceptual Observation

This task illustrates the deep relationship between:

- elementary probabilities,
- cumulative probabilities,
- and graphical representations of distributions.

The PMF describes how probability is distributed across individual values.

The CDF describes how probability accumulates as we move along the real line.

For discrete random variables, these two descriptions are completely equivalent:

- the PMF determines the CDF,
- and the CDF determines the PMF through its jumps.

Understanding this relationship is one of the central conceptual ideas in probability theory.
