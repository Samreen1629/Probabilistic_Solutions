# Task 9 — Gamma Distribution

# Introduction

The **gamma distribution** is a continuous probability distribution commonly used to model:

- waiting times,
- lifetimes of systems,
- arrival times of events,
- reliability problems.

It is a very important distribution in probability theory and statistics because it generalizes several other distributions, including the:

- exponential distribution,
- chi-square distribution.

The gamma distribution is defined only for positive real values:

$$
x \ge 0
$$

making it suitable for modeling quantities such as time, distance, and duration.

---

# Useful Definitions and Formulas

## Gamma Distribution

A random variable follows a gamma distribution if:

$$
X \sim \text{Gamma}(\alpha,\beta)
$$

where:

- $$\(\alpha > 0\)$$ is the **shape parameter**,
- $$\(\beta > 0\)$$ is the **rate parameter**.

Sometimes the scale parameter is used instead of the rate parameter.

---

# Probability Density Function (PDF)

The PDF of the gamma distribution is:

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

# Gamma Function

The gamma function generalizes the factorial function.

For positive integers:

$$
\Gamma(n)=(n-1)!
$$

Examples:

$$
\Gamma(1)=0!=1
$$

$$
\Gamma(4)=3!=6
$$

---

# Cumulative Distribution Function (CDF)

The CDF is:

$$
F(x)=P(X \le x)
$$

It represents the probability that the random variable is less than or equal to \(x\).

The gamma CDF usually requires numerical computation or software.

---

# 1. Description of the Experiment

The gamma distribution models the waiting time until several random events occur.

Example:

- waiting time until 3 customers arrive,
- waiting time until 5 machine failures occur,
- total service time in a queue.

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

The random variable directly represents the observed waiting time.

---

# 5. Support of the Distribution

The support of the gamma distribution is:

$$
[0,\infty)
$$

This means the random variable may take any nonnegative real value.

---

# 6. Shape of the Gamma Distribution

The shape of the gamma distribution depends mainly on:

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

The density decreases rapidly from its maximum near:

$$
x=0
$$

---

## Case 2 — Moderate Shape Parameter

When:

$$
\alpha=2
$$

the distribution becomes less skewed and develops a visible peak.

---

## Case 3 — Large Shape Parameter

When:

$$
\alpha=5
$$

the distribution becomes more symmetric and spread out.

---

# 7. PDF Graphs

The PDF changes significantly as the shape parameter changes.

---

## Example PDF Graphs

### Case 1

$$
\alpha=1
$$

The graph decreases exponentially.

---

### Case 2

$$
\alpha=2
$$

The graph has one peak and moderate skewness.

---

### Case 3

$$
\alpha=5
$$

The graph becomes smoother and more symmetric.

---

# 8. CDF Graphs

The CDF of the gamma distribution:

- starts at 0,
- increases continuously,
- approaches 1 as \(x \to \infty\).

---

## Example CDF Behavior

### Small \(\alpha\)

The CDF rises quickly near zero.

---

### Large \(\alpha\)

The CDF increases more gradually because larger waiting times become more likely.

---

# 9. Mean and Variance

## Mean

The expected value is:

$$
E[X]=\frac{\alpha}{\beta}
$$

---

## Variance

The variance is:

$$
\text{Var}(X)=\frac{\alpha}{\beta^2}
$$

---

# 10. Computing Probabilities

For continuous distributions, probabilities are computed using areas under the PDF curve.

---

## Lower Tail Probability

$$
P(X \le a)=F(a)
$$

This gives the probability that the waiting time is at most \(a\).

---

## Upper Tail Probability

$$
P(X \ge a)=1-F(a)
$$

This gives the probability that the waiting time exceeds \(a\).

---

## Interval Probability

$$
P(a \le X \le b)=F(b)-F(a)
$$

This gives the probability that the waiting time lies between \(a\) and \(b\).

---

# Example

Suppose:

$$
X \sim \text{Gamma}(2,1)
$$

Find:

$$
P(X \le 3)
$$

Using software or statistical tables:

$$
P(X \le 3)\approx0.8009
$$

---

# 11. Relation to Other Distributions

---

## Exponential Distribution

The exponential distribution is a special case of the gamma distribution:

$$
\text{Gamma}(1,\beta)
$$

---

## Chi-Square Distribution

The chi-square distribution is also a special case:

$$
\chi_n^2 \sim \text{Gamma}\left(\frac{n}{2},\frac{1}{2}\right)
$$

---

# 12. Practical Applications

The gamma distribution has many practical applications.

Examples include:

- waiting times in queueing systems,
- reliability engineering,
- insurance mathematics,
- rainfall modeling,
- telecommunications,
- medical survival analysis,
- machine lifetime analysis.

---

# 13. Comparison with Other Distributions

| Distribution | Type | Measures |
|---|---|---|
| Exponential | Continuous | Waiting time for one event |
| Gamma | Continuous | Waiting time for multiple events |
| Normal | Continuous | Symmetric measurements |
| Poisson | Discrete | Number of events |

---

# Conclusion

The gamma distribution is a flexible continuous distribution used primarily for modeling waiting times and lifetimes.

Its shape depends heavily on the parameter:

$$
\alpha
$$

while the rate parameter:

$$
\beta
$$

controls the spread and scale of the distribution.

The gamma distribution is closely related to the exponential and chi-square distributions and has many important real-world applications.
