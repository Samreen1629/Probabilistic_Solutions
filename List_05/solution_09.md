# Task 9 — Gamma Distribution

## Introduction

The **gamma distribution** is a continuous probability distribution used mainly to model:

- waiting times,
- lifetimes of systems,
- arrival times of events,
- reliability and queueing problems.

It is defined only for positive values:

$$
x \ge 0
$$

The gamma distribution generalizes the exponential distribution and is closely related to the chi-square distribution.

---

# Useful Definitions and Formulas

## Gamma Distribution

A random variable follows a gamma distribution if:

$$
X \sim \text{Gamma}(\alpha,\beta)
$$

where:

- $$\(\alpha>0\)$$ is the shape parameter,
- $$\(\beta>0\)$$ is the rate parameter.

---

## Probability Density Function (PDF)

$$
f(x)=\frac{\beta^\alpha x^{\alpha-1}e^{-\beta x}}{\Gamma(\alpha)}
$$

for:

$$
x \ge 0
$$

where:

$$
\Gamma(\alpha)
$$

is the gamma function.

---

## Gamma Function

The gamma function generalizes factorials:

$$
\Gamma(n)=(n-1)!
$$

Examples:

$$
\Gamma(1)=1
$$

$$
\Gamma(4)=3!=6
$$

---

## Cumulative Distribution Function (CDF)

$$
F(x)=P(X\le x)
$$

The CDF gives cumulative probabilities and usually requires numerical computation.

---

# 1. Description of the Experiment

The gamma distribution models waiting time until several events occur.

Examples:

- waiting time until 5 customers arrive,
- total repair time of machines,
- time until several phone calls are received.

---

# 2. Sample Space

The sample space is:

$$
\Omega=[0,\infty)
$$

because waiting times cannot be negative.

---

# 3. Elementary Outcome

An elementary outcome is denoted by:

$$
\omega
$$

Example:

$$
\omega=3.5
$$

meaning a waiting time of 3.5 units.

---

# 4. Definition of the Random Variable

Define:

$$
X(\omega)=\omega
$$

The random variable directly represents the waiting time.

---

# 5. Support of the Distribution

The support is:

$$
[0,\infty)
$$

Thus, the random variable may take any nonnegative real value.

---

# 6. Shape of the Gamma Distribution

The shape depends mainly on the parameter:

$$
\alpha
$$

---

## Case 1 — Small Shape Parameter

When:

$$
\alpha=1
$$

the gamma distribution becomes the exponential distribution.

The graph decreases rapidly from its maximum near:

$$
x=0
$$

---

## Case 2 — Moderate Shape Parameter

When:

$$
\alpha=2
$$

the graph develops a visible peak and becomes less skewed.

---

## Case 3 — Large Shape Parameter

When:

$$
\alpha=5
$$

the graph becomes smoother and more symmetric.

---

# 7. Graph of the PDF

The PDF changes shape depending on the parameter:

$$
\alpha
$$

ASCII representation:

```text
Density

α=1
1.0 |\
    | \
    |  \
    |   \
0.0 +-----------------------------> x

α=2
1.0 |     /\
    |    /  \
    |   /    \
    |__/      \____
0.0 +-----------------------------> x

α=5
1.0 |          /\
    |         /  \
    |        /    \
    |_______/      \_______
0.0 +-----------------------------> x
```

Observations:

- larger $$\(\alpha\)$$ shifts the peak to the right,
- the distribution becomes less skewed,
- the spread increases.

---

# 8. Graph of the CDF

The CDF:

- starts at 0,
- increases continuously,
- approaches 1 as $$\(x\to\infty\)$$.

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

- the function is increasing,
- cumulative probability approaches 1,
- larger $$\(\alpha\)$$ produces slower accumulation.

---

# 9. Mean and Variance

## Mean

$$
E[X]=\frac{\alpha}{\beta}
$$

---

## Variance

$$
\text{Var}(X)=\frac{\alpha}{\beta^2}
$$

---

# 10. Computing Probabilities

Probabilities correspond to areas under the PDF curve.

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
X\sim\text{Gamma}(2,1)
$$

Find:

$$
P(X\le3)
$$

Using statistical software:

$$
P(X\le3)\approx0.8009
$$

---

# 11. Relation to Other Distributions

---

## Exponential Distribution

The exponential distribution is a special case:

$$
\text{Gamma}(1,\beta)
$$

---

## Chi-Square Distribution

The chi-square distribution is also a special case:

$$
\chi_n^2\sim\text{Gamma}\left(\frac{n}{2},\frac12\right)
$$

---

# 12. Applications

Applications include:

- reliability engineering,
- queueing systems,
- insurance mathematics,
- telecommunications,
- machine lifetime analysis,
- rainfall modeling,
- survival analysis.

---

# 13. Comparing Gamma and Exponential Distributions

| Distribution | Measures |
|---|---|
| Exponential | Waiting time for one event |
| Gamma | Waiting time for multiple events |

The gamma distribution generalizes the exponential model.

---

# Final Conceptual Observation

The gamma distribution is one of the most important continuous distributions for modeling waiting times.

Its flexibility comes from the shape parameter:

$$
\alpha
$$

which controls the shape and skewness of the distribution.

The gamma distribution connects several important probability models, including:

- exponential distributions,
- chi-square distributions,
- queueing and reliability models.
