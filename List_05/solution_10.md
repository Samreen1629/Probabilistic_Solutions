# Task 10 — Normal Distribution

## Introduction

The **normal distribution** is one of the most important probability distributions in statistics.

It is also called the:

- Gaussian distribution,
- bell-shaped distribution.

Many natural measurements approximately follow a normal distribution, including:

- heights,
- weights,
- IQ scores,
- exam results,
- measurement errors.

The normal distribution is continuous and symmetric.

---

# Useful Definitions and Formulas

## Normal Distribution

A random variable follows a normal distribution if:

$$
X\sim N(\mu,\sigma^2)
$$

where:

- $$\(\mu\)$$ is the mean,
- $$\(\sigma^2\)$$ is the variance,
- $$\(\sigma\)$$ is the standard deviation.

---

## Probability Density Function (PDF)

$$
f(x)=\frac{1}{\sigma\sqrt{2\pi}}
e^{-\frac{(x-\mu)^2}{2\sigma^2}}
$$

for:

$$
-\infty<x<\infty
$$

---

## Cumulative Distribution Function (CDF)

$$
F(x)=P(X\le x)
$$

The CDF gives cumulative probabilities.

---

# 1. Description of the Experiment

Suppose we measure the heights of students.

Most students have heights close to the average height, while very small or very large heights are less common.

This behavior is modeled by the normal distribution.

---

# 2. Sample Space

$$
\Omega=\mathbb{R}
$$

because any real value is theoretically possible.

---

# 3. Elementary Outcome

An elementary outcome is denoted by:

$$
\omega
$$

Example:

$$
\omega=172.5
$$

meaning a measured height of 172.5 cm.

---

# 4. Definition of the Random Variable

Define:

$$
X(\omega)=\omega
$$

The random variable directly represents the measurement.

---

# 5. Support of the Distribution

The support is:

$$
(-\infty,\infty)
$$

Thus, all real values are theoretically possible.

---

# 6. Shape of the Normal Distribution

The normal distribution has several important properties.

---

## Symmetry

The graph is symmetric around:

$$
x=\mu
$$

---

## Bell Shape

The graph has a bell-shaped appearance.

Most observations are concentrated near the mean.

---

## Infinite Tails

The tails extend infinitely in both directions.

---

# 7. Graph of the PDF

ASCII representation:

```text
Density

1.0 |                /\
    |              /    \
    |            /        \
    |          /            \
    |________/                \________
0.0 +--------------------------------------> x
```

Important observations:

- the graph is symmetric,
- the peak occurs at the mean,
- probabilities decrease away from the center.

---

## Effect of the Mean

Changing:

$$
\mu
$$

moves the graph left or right.

---

## Effect of the Standard Deviation

Changing:

$$
\sigma
$$

changes the spread of the graph.

- small $$\(\sigma\)$$ → narrow curve,
- large $$\(\sigma\)$$ → wider curve.

---

# 8. Graph of the CDF

The CDF:

- starts near 0,
- increases continuously,
- approaches 1.

ASCII representation:

```text
CDF

1.0 |                            ________
    |                        ___/
    |                    ___/
    |                ___/
    |            ___/
0.0 +___________/______________________> x
```

Important observations:

- the CDF is always increasing,
- the steepest growth occurs near the mean,
- probabilities accumulate continuously.

---

# 9. Standard Normal Distribution

A special case occurs when:

$$
\mu=0
$$

and

$$
\sigma=1
$$

This is called the standard normal distribution:

$$
Z\sim N(0,1)
$$

---

# 10. Standardization

Any normal random variable can be transformed into a standard normal variable using:

$$
Z=\frac{X-\mu}{\sigma}
$$

---

# Example

Suppose:

$$
X\sim N(100,15^2)
$$

Find the standardized value for:

$$
X=130
$$

---

## Step 1

Use the formula:

$$
Z=\frac{X-\mu}{\sigma}
$$

---

## Step 2

Substitute values:

$$
Z=\frac{130-100}{15}
$$

---

## Step 3

Simplify:

$$
Z=2
$$

---

# 11. Computing Probabilities

---

## Lower Tail Probability

$$
P(X\le a)=F(a)
$$

---

## Upper Tail Probability

$$
P(X\ge a)=1-F(a)
$$

---

## Interval Probability

$$
P(a\le X\le b)=F(b)-F(a)
$$

---

# Example

Suppose:

$$
X\sim N(0,1)
$$

Find:

$$
P(X\le1)
$$

Using standard normal tables:

$$
P(X\le1)\approx0.8413
$$

---

# 12. Empirical Rule

For normal distributions:

- approximately 68% of values lie within:

$$
\mu\pm\sigma
$$

- approximately 95% lie within:

$$
\mu\pm2\sigma
$$

- approximately 99.7% lie within:

$$
\mu\pm3\sigma
$$

---

# 13. Applications

Applications include:

- statistics,
- finance,
- engineering,
- biology,
- psychology,
- quality control,
- machine learning.

---

# 14. Comparing Normal and Gamma Distributions

| Distribution | Shape |
|---|---|
| Normal | Symmetric |
| Gamma | Right-skewed |

The normal distribution is symmetric, while the gamma distribution is usually skewed.

---

# Final Conceptual Observation

The normal distribution is one of the most important distributions in probability and statistics.

Its bell-shaped symmetric graph appears naturally in many real-world phenomena and statistical models.
