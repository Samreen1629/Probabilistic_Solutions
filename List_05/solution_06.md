# Task 6 — Hypergeometric Distribution

## Introduction

The **hypergeometric distribution** models sampling **without replacement** from a finite population.

It is used when:

- the population size is fixed,
- some objects are distinguished,
- objects are sampled without replacement.

Examples:

- Drawing cards from a deck
- Quality control inspection
- Lottery sampling
- Selecting students from a group

---

# Useful Definitions and Formulas

## Hypergeometric Distribution

A random variable \(X\) follows a hypergeometric distribution if it counts the number of distinguished objects selected in a sample drawn without replacement.

We write:

$$
X \sim \text{Hypergeometric}(N,K,n)
$$

where:

- \(N\) = population size,
- \(K\) = number of distinguished objects,
- \(n\) = sample size.

---

## Probability Mass Function (PMF)

$$
P(X=k)=\frac{\binom{K}{k}\binom{N-K}{n-k}}{\binom{N}{n}}
$$

---

# 1. Description of the Experiment

Suppose a box contains:

- \(N=20\) balls,
- \(K=7\) red balls,
- \(13\) blue balls.

We randomly select:

$$
n=5
$$

balls without replacement.

---

# 2. Sample Space

The sample space is:

$$
\Omega=\{\text{all possible samples of size } n\}
$$

---

# 3. Elementary Outcome

An elementary outcome is denoted by:

$$
\omega
$$

Example:

$$
\omega=\{\text{red, red, blue, blue, blue}\}
$$

---

# 4. Definition of the Random Variable

Define:

$$
X(\omega)=\text{number of distinguished objects in the sample}
$$

Example:

$$
X(\omega)=2
$$

if the sample contains 2 red balls.

---

# 5. PMF of the Hypergeometric Distribution

$$
P(X=k)=\frac{\binom{K}{k}\binom{N-K}{n-k}}{\binom{N}{n}}
$$

---

## Example

Suppose:

$$
N=20,\quad K=7,\quad n=5
$$

Find:

$$
P(X=2)
$$

### Step 1 — Write the formula

$$
P(X=k)=\frac{\binom{K}{k}\binom{N-K}{n-k}}{\binom{N}{n}}
$$

### Step 2 — Substitute values

$$
P(X=2)=\frac{\binom{7}{2}\binom{13}{3}}{\binom{20}{5}}
$$

### Step 3 — Compute combinations

$$
=\frac{21 \cdot 286}{15504}
$$

$$
=\frac{6006}{15504}
$$

$$
\approx 0.3874
$$

### Answer

$$
P(X=2)\approx0.3874
$$

---

# 6. Support of the Distribution

The support depends on the parameters:

$$
\max(0,n-(N-K)) \le X \le \min(n,K)
$$

---

# 7. Effect of Parameter Changes

## Increasing Sample Size

- distribution becomes wider,
- larger counts become possible.

---

## Increasing Number of Distinguished Objects

- probabilities shift toward larger values,
- larger counts become more likely.

---

# 8. Important Probabilities

## Exact Probability

$$
P(X=k)=\frac{\binom{K}{k}\binom{N-K}{n-k}}{\binom{N}{n}}
$$

---

## Cumulative Probability

$$
P(X \le k)=\sum_{i=0}^{k}P(X=i)
$$

---

## Upper Tail Probability

$$
P(X \ge k)=1-P(X \le k-1)
$$

---

## Interval Probability

$$
P(a \le X \le b)=\sum_{i=a}^{b}P(X=i)
$$

---

# 9. Comparison with the Binomial Distribution

## Hypergeometric Distribution

- sampling without replacement,
- probabilities change after each draw.

---

## Binomial Distribution

- sampling with replacement,
- trials are independent.

The hypergeometric model becomes similar to the binomial model when the population is very large.

---

# 10. Practical Applications

Applications include:

- quality control,
- card games,
- biological sampling,
- election auditing,
- lottery problems.

---

# Conclusion

The hypergeometric distribution models sampling without replacement from a finite population.

Its probabilities depend strongly on:

- population size,
- sample size,
- number of distinguished objects.
