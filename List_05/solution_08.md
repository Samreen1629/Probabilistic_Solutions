# Task 8 — Beta Distribution

# Introduction

The **beta distribution** is a continuous probability distribution defined on the interval:

$$
[0,1]
$$

It is one of the most flexible continuous distributions because its shape changes significantly depending on its parameters.

The beta distribution is commonly used to model:

- probabilities,
- proportions,
- percentages,
- uncertainty about probabilities,
- success rates.

Examples include:

- probability that a customer buys a product,
- proportion of defective items,
- accuracy of a classifier,
- click-through rates in online advertising.

---

# Useful Definitions and Formulas

## Beta Distribution

A random variable \(X\) follows a beta distribution if:

$$
X \sim \text{Beta}(\alpha,\beta)
$$

where:

$$
\alpha > 0
$$

and

$$
\beta > 0
$$

are shape parameters.

---

# Probability Density Function (PDF)

The PDF of the beta distribution is:

$$
f(x)=\frac{x^{\alpha-1}(1-x)^{\beta-1}}{B(\alpha,\beta)}
$$

for:

$$
0 \le x \le 1
$$

where:

$$
B(\alpha,\beta)
$$

is the beta function:

$$
B(\alpha,\beta)=\frac{\Gamma(\alpha)\Gamma(\beta)}{\Gamma(\alpha+\beta)}
$$

and:

$$
\Gamma(\cdot)
$$

is the gamma function.

---

# Cumulative Distribution Function (CDF)

The CDF is:

$$
F(x)=P(X \le x)
$$

It gives the probability that the random variable is less than or equal to \(x\).

The beta CDF usually requires numerical methods or software to compute.

---

# 1. Description of the Experiment

Consider a continuous experiment where a value between 0 and 1 is observed.

Examples:

- proportion of successful outcomes,
- probability estimate,
- percentage converted into decimal form.

---

# 2. Sample Space

The sample space is:

$$
\Omega=[0,1]
$$

because all possible outcomes lie between 0 and 1.

---

# 3. Elementary Outcome

An elementary outcome is denoted by:

$$
\omega
$$

Example:

$$
\omega=0.72
$$

Interpretation:

- the observed proportion equals 0.72,
- or the observed probability estimate equals 72%.

---

# 4. Definition of the Random Variable

Define:

$$
X(\omega)=\omega
$$

This means the random variable directly equals the observed value.

---

# 5. Support of the Distribution

The support of the beta distribution is:

$$
[0,1]
$$

This means:

$$
0 \le X \le 1
$$

The random variable cannot take values outside this interval.

---

# 6. Shape of the Beta Distribution

The beta distribution can take many different shapes depending on the parameters:

$$
\alpha
$$

and

$$
\beta
$$

---

# A. Symmetric Distribution

When:

$$
\alpha=\beta
$$

the distribution is symmetric.

---

## Example

If:

$$
\alpha=\beta=2
$$

the distribution is bell-shaped and symmetric around:

$$
x=0.5
$$

---

# B. Left-Skewed Distribution

When:

$$
\alpha>\beta
$$

the density is concentrated near:

$$
x=1
$$

This means larger values are more likely.

---

## Example

$$
\alpha=5,\quad \beta=2
$$

---

# C. Right-Skewed Distribution

When:

$$
\alpha<\beta
$$

the density is concentrated near:

$$
x=0
$$

This means smaller values are more likely.

---

## Example

$$
\alpha=2,\quad \beta=5
$$

---

# D. Density Concentrated Near Endpoints

When:

$$
\alpha<1
$$

and

$$
\beta<1
$$

the density becomes concentrated near both 0 and 1.

---

## Example

$$
\alpha=0.5,\quad \beta=0.5
$$

This produces a U-shaped distribution.

---

# 7. CDF Graphs

The CDF always:

- starts at 0,
- increases continuously,
- ends at 1.

---

## Effect of Parameters on the CDF

### Large $$\(\alpha\)$$

The CDF grows more slowly near 0 and faster near 1.

---

### Large $$\(\beta\)$$

The CDF rises quickly near 0 and slows down later.

---

### Symmetric Parameters

The CDF grows symmetrically around:

$$
x=0.5
$$

---

# 8. Computing Probabilities

Because the beta distribution is continuous, probabilities are computed using areas under the PDF curve.

---

# A. Lower Tail Probability

Find:

$$
P(X \le a)
$$

This equals the CDF value:

$$
P(X \le a)=F(a)
$$

---

# B. Upper Tail Probability

Find:

$$
P(X \ge a)
$$

Using the complement rule:

$$
P(X \ge a)=1-F(a)
$$

---

# C. Interval Probability

Find:

$$
P(a \le X \le b)
$$

Using the CDF:

$$
P(a \le X \le b)=F(b)-F(a)
$$

---

# Example

Suppose:

$$
X \sim \text{Beta}(2,5)
$$

Find:

$$
P(X \le 0.4)
$$

Using numerical software or statistical tables:

$$
F(0.4)\approx0.7667
$$

Therefore:

$$
P(X \le 0.4)\approx0.7667
$$

---

# 9. Why Probabilities Are Areas Under the Curve

For continuous distributions:

$$
P(X=a)=0
$$

because a single point has zero width and therefore zero area.

Probabilities are obtained from intervals:

$$
P(a \le X \le b)
$$

which correspond to areas under the density curve.

---

# 10. Mean and Variance

## Mean

The expected value is:

$$
E[X]=\frac{\alpha}{\alpha+\beta}
$$

---

## Variance

The variance is:

$$
\text{Var}(X)=
\frac{\alpha\beta}
{(\alpha+\beta)^2(\alpha+\beta+1)}
$$

---

# 11. Practical Applications of the Beta Distribution

The beta distribution is widely used in many fields.

Applications include:

- Bayesian statistics,
- machine learning,
- reliability analysis,
- modeling probabilities,
- quality control,
- A/B testing,
- finance,
- biological proportions.

---

# 12. Parameter Sliders in Applications

In visualization applications, sliders for:

$$
\alpha
$$

and

$$
\beta
$$

allow users to observe how the distribution changes shape dynamically.

This helps illustrate:

- symmetry,
- skewness,
- concentration near boundaries,
- spread of the distribution.

---

# 13. Comparison of Different Parameter Choices

| Parameters | Shape |
|---|---|
| $$\(\alpha=\beta=2\)$$ | Symmetric |
| $$\(\alpha>\beta\)$$ | Left-skewed |
| $$\(\alpha<\beta\)$$ | Right-skewed |
| $$\(\alpha<1,\beta<1\)$$ | U-shaped |
| Large $$\(\alpha,\beta\)$$ | Concentrated near center |

---

# Conclusion

The beta distribution is an extremely flexible continuous distribution defined on:

$$
[0,1]
$$

Its shape depends heavily on the parameters:

$$
\alpha
$$

and

$$
\beta
$$

making it ideal for modeling probabilities, proportions, and uncertainty in many practical applications.
