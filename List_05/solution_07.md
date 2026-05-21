# Task 7 — Negative Binomial Distribution

## Introduction

The **negative binomial distribution** models the number of trials required to achieve the \(r\)-th success.

It generalizes the geometric distribution.

---

# Useful Definitions and Formulas

## Negative Binomial Distribution

We write:

$$
X \sim \text{NB}(r,p)
$$

where:

- \(r\) = target number of successes,
- \(p\) = probability of success.

---

## PMF

$$
P(X=k)=\binom{k-1}{r-1}p^r(1-p)^{k-r}
$$

for:

$$
k=r,r+1,r+2,\dots
$$

---

# 1. Description of the Experiment

Repeated Bernoulli trials are performed until the \(r\)-th success occurs.

---

# 2. Sample Space

$$
\Omega=\{\text{all sequences ending with the } r\text{-th success}\}
$$

---

# 3. Elementary Outcome

Example:

$$
\omega=FFSFS
$$

If:

$$
r=2
$$

then the second success occurs on trial 5.

---

# 4. Random Variable

$$
X(\omega)=\text{trial number of the } r\text{-th success}
$$

---

# 5. PMF

$$
P(X=k)=\binom{k-1}{r-1}p^r(1-p)^{k-r}
$$

---

## Example

Suppose:

$$
r=3,\quad p=0.4
$$

Find:

$$
P(X=5)
$$

### Step 1

$$
P(X=5)=\binom{4}{2}(0.4)^3(0.6)^2
$$

### Step 2

$$
=6 \cdot 0.064 \cdot 0.36
$$

### Step 3

$$
=0.13824
$$

### Answer

$$
P(X=5)=0.13824
$$

---

# 6. Support

$$
\{r,r+1,r+2,\dots\}
$$

---

# 7. Effect of Parameter Changes

## Increasing \(p\)

- successes occur faster,
- probabilities move toward smaller values.

---

## Increasing \(r\)

- waiting times become longer,
- distribution spreads out.

---

# 8. Important Probabilities

## Exact Probability

$$
P(X=k)=\binom{k-1}{r-1}p^r(1-p)^{k-r}
$$

---

## Cumulative Probability

$$
P(X \le k)=\sum_{i=r}^{k}P(X=i)
$$

---

## Tail Probability

$$
P(X>k)=1-P(X \le k)
$$

---

## Interval Probability

$$
P(a \le X \le b)=\sum_{i=a}^{b}P(X=i)
$$

---

# 9. Relation to the Geometric Distribution

The geometric distribution is a special case of the negative binomial distribution with:

$$
r=1
$$

---

# 10. Applications

Applications include:

- reliability testing,
- sales attempts,
- sports statistics,
- biological experiments,
- epidemiology.

---

# Conclusion

The negative binomial distribution models waiting time until the \(r\)-th success and generalizes the geometric distribution.
