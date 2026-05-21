# Task 5 — Poisson Distribution

## Introduction

The **Poisson distribution** is a discrete probability distribution that models the number of random events occurring in a fixed interval of time, distance, area, or volume.

Examples include:

- Number of phone calls received in one hour
- Number of accidents at an intersection per day
- Number of typing errors on a page
- Number of customers arriving at a store

The Poisson distribution is commonly used when events occur:

- independently,
- randomly,
- with a constant average rate.

---

# Useful Definitions and Formulas

## Poisson Distribution

A random variable \(X\) follows a Poisson distribution if it counts the number of events occurring in a fixed interval.

We write:

$$
X \sim \text{Poisson}(\lambda)
$$

where:

$$
\lambda > 0
$$

is the average number of events in the interval.

---

## Probability Mass Function (PMF)

$$
P(X=k)=\frac{e^{-\lambda}\lambda^k}{k!}
$$

for:

$$
k=0,1,2,\dots
$$

where:

- \(e \approx 2.71828\),
- \(k!\) is the factorial.

---

## Cumulative Distribution Function (CDF)

$$
P(X \le k)=\sum_{i=0}^{k}\frac{e^{-\lambda}\lambda^i}{i!}
$$

---

# 1. Description of the Experiment

Suppose we observe the number of customers entering a store during one hour.

Events occur:

- independently,
- randomly,
- with average rate \(\lambda\).

---

# 2. Sample Space

The sample space is:

$$
\Omega=\{0,1,2,3,\dots\}
$$

because any nonnegative number of events may occur.

---

# 3. Elementary Outcome

An elementary outcome is denoted by:

$$
\omega
$$

Example:

$$
\omega=4
$$

meaning that 4 events occurred during the interval.

---

# 4. Definition of the Random Variable

Define:

$$
X(\omega)=\text{number of events occurring in the interval}
$$

Example:

$$
X(4)=4
$$

---

# 5. Probability Mass Function (PMF)

The PMF of the Poisson distribution is:

$$
P(X=k)=\frac{e^{-\lambda}\lambda^k}{k!}
$$

---

## Example

Suppose:

$$
\lambda=3
$$

Find:

$$
P(X=2)
$$

### Step 1 — Write the formula

$$
P(X=k)=\frac{e^{-\lambda}\lambda^k}{k!}
$$

### Step 2 — Substitute values

$$
P(X=2)=\frac{e^{-3}3^2}{2!}
$$

### Step 3 — Simplify

$$
=\frac{e^{-3}\cdot 9}{2}
$$

$$
\approx \frac{0.0498\cdot 9}{2}
$$

$$
\approx 0.224
$$

### Answer

$$
P(X=2)\approx0.224
$$

---

# 6. Support of the Distribution

The support is:

$$
\{0,1,2,3,\dots\}
$$

The support is infinite because any number of events may occur.

---

# 7. PMF Graphs for Different Values of $$\(\lambda\)$$

Consider:

$$
\lambda=1,\quad \lambda=4,\quad \lambda=10
$$

---

## Small $$\(\lambda\)$$

When:

$$
\lambda=1
$$

- probabilities are concentrated near 0,
- small counts are most likely.

---

## Medium $$\(\lambda\)$$

When:

$$
\lambda=4
$$

- the distribution becomes wider,
- probabilities spread across several values.

---

## Large $$\(\lambda\)$$

When:

$$
\lambda=10
$$

- the distribution becomes more symmetric,
- it starts resembling the normal distribution.

---

# 8. CDF Graphs

The CDF increases from 0 to 1.

As \(\lambda\) increases:

- the curve spreads farther to the right,
- cumulative probabilities grow more slowly for small \(k\).

---

# 9. Computing Important Probabilities

## A. Exact Probability

$$
P(X=k)=\frac{e^{-\lambda}\lambda^k}{k!}
$$

---

## B. Cumulative Probability

$$
P(X \le k)=\sum_{i=0}^{k}\frac{e^{-\lambda}\lambda^i}{i!}
$$

---

## C. Upper Tail Probability

$$
P(X \ge k)=1-P(X \le k-1)
$$

---

## D. Interval Probability

$$
P(a \le X \le b)=P(X \le b)-P(X<a)
$$

---

# 10. Comparing CDF and Direct Summation

The CDF can be computed:

1. directly from the PMF by summing probabilities,
2. using statistical software or tables.

Both methods produce the same result.

---

# 11. Practical Applications

Applications include:

- customer arrivals,
- radioactive decay,
- traffic flow,
- insurance claims,
- defects in manufacturing,
- network packet arrivals.

---

# 12. Conclusion

The Poisson distribution models counts of random events in fixed intervals.

Its most important parameter is:

$$
\lambda
$$

which controls both:

- the average number of events,
- and the spread of the distribution.
