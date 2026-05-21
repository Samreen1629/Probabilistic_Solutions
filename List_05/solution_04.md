# Task 4 — Geometric Distribution

## Introduction

The **geometric distribution** is a discrete probability distribution that models the number of independent Bernoulli trials needed to obtain the **first success**.

Typical examples include:

- Number of coin tosses until the first head appears
- Number of attempts until a machine works correctly
- Number of phone calls until someone answers

The geometric distribution is one of the simplest and most important discrete probability models.

---

# Useful Definitions and Formulas

## Bernoulli Trial

A **Bernoulli trial** is a random experiment with only two possible outcomes:

- Success
- Failure

If the probability of success is denoted by \(p\), then:

$$
P(\text{success}) = p
$$

and

$$
P(\text{failure}) = 1-p
$$

---

## Geometric Distribution

A random variable \(X\) has a geometric distribution if it represents the number of trials required to obtain the **first success**.

We write:

$$
X \sim \text{Geom}(p)
$$

where:

- \(p\) = probability of success in each trial
- \(1-p\) = probability of failure

---

## Probability Mass Function (PMF)

The PMF gives the probability that the first success occurs exactly on trial \(k\):

$$
P(X=k) = (1-p)^{k-1}p
$$

for:

$$
k = 1,2,3,\dots
$$

Explanation:

- The first \(k-1\) trials must be failures
- The \(k\)-th trial must be a success

---

## Cumulative Distribution Function (CDF)

The CDF gives the probability that the first success occurs on or before trial \(k\):

$$
P(X \le k) = 1-(1-p)^k
$$

---

## Tail Probability

The probability that more than \(k\) trials are needed:

$$
P(X>k) = (1-p)^k
$$

---

# 1. Description of the Experiment

We repeatedly perform independent Bernoulli trials until the first success occurs.

Each trial:

- has only two outcomes (success/failure),
- is independent of all previous trials,
- has the same probability of success \(p\).

The experiment stops as soon as the first success appears.

---

# 2. Sample Space

The sample space is denoted by:

$$
\Omega
$$

It contains all possible sequences ending with the first success:

$$
\Omega = \{S, FS, FFS, FFFS, \dots\}
$$

where:

- \(S\) = success,
- \(F\) = failure.

Examples:

- \(S\) means success on the first trial,
- \(FFS\) means two failures followed by success on the third trial.

---

# 3. Elementary Outcome

An elementary outcome is denoted by:

$$
\omega
$$

It represents one specific sequence from the sample space.

Example:

$$
\omega = FFFS
$$

Interpretation:

- first trial → failure,
- second trial → failure,
- third trial → failure,
- fourth trial → success.

---

# 4. Definition of the Random Variable

The random variable is denoted by:

$$
X(\omega)
$$

Definition:

$$
X(\omega) = \text{the trial number on which the first success occurs}
$$

Examples:

$$
X(S)=1
$$

$$
X(FS)=2
$$

$$
X(FFFS)=4
$$

Thus, the geometric random variable counts how long we wait for the first success.

---

# 5. Probability Mass Function (PMF)

To obtain the first success on trial \(k\):

1. The first \(k-1\) trials must be failures
2. The \(k\)-th trial must be a success

Therefore:

$$
P(X=k) = (1-p)^{k-1}p
$$

---

## Example

Suppose:

$$
p=0.3
$$

Find:

$$
P(X=4)
$$

### Step 1 — Write the formula

$$
P(X=k) = (1-p)^{k-1}p
$$

### Step 2 — Substitute values

$$
P(X=4) = (1-0.3)^3(0.3)
$$

### Step 3 — Simplify

$$
= (0.7)^3(0.3)
$$

$$
= 0.343 \times 0.3
$$

$$
= 0.1029
$$

### Answer

$$
P(X=4)=0.1029
$$

---

# 6. Cumulative Distribution Function (CDF)

The CDF gives the probability that the first success occurs by trial \(k\):

$$
P(X \le k)=1-(1-p)^k
$$

---

## Example

Let:

$$
p=0.3
$$

Find:

$$
P(X \le 4)
$$

### Step 1 — Write the formula

$$
P(X \le k)=1-(1-p)^k
$$

### Step 2 — Substitute values

$$
P(X \le 4)=1-(1-0.3)^4
$$

### Step 3 — Simplify

$$
=1-(0.7)^4
$$

$$
=1-0.2401
$$

$$
=0.7599
$$

### Answer

$$
P(X \le 4)=0.7599
$$

---

# 7. Support of the Distribution

The support is the set of all possible values of \(X\):

$$
\{1,2,3,\dots\}
$$

The support is infinite because there is no maximum number of failures before the first success.

Even though long waiting times become unlikely, they are still possible.

---

# 8. PMF Graphs for Different Values of \(p\)

Consider three values:

$$
p=0.2,\quad p=0.5,\quad p=0.8
$$

---

## Case 1 — Small \(p\)

When:

$$
p=0.2
$$

- success is rare,
- long waiting times are more likely,
- the PMF decreases slowly.

The graph has a long tail.

---

## Case 2 — Medium \(p\)

When:

$$
p=0.5
$$

- success and failure are equally likely,
- probabilities decrease moderately fast.

---

## Case 3 — Large \(p\)

When:

$$
p=0.8
$$

- success is very likely,
- most probability mass is concentrated near \(1\),
- the PMF decreases very quickly.

---

# 9. CDF Graphs for Different Values of \(p\)

The CDF always increases toward \(1\).

---

## Small \(p\)

The CDF rises slowly because success is unlikely.

---

## Large \(p\)

The CDF rises quickly because success occurs early with high probability.

---

# 10. How the Graphs Change as \(p\) Changes

## As \(p\) becomes larger

- waiting times become shorter,
- PMF becomes more concentrated near \(1\),
- CDF rises faster.

---

## As \(p\) becomes smaller

- waiting times become longer,
- PMF spreads out,
- tail probabilities become larger,
- CDF rises more slowly.

---

# 11. Computing Important Probabilities

---

# A. Probability of Exactly \(k\) Trials

Formula:

$$
P(X=k)=(1-p)^{k-1}p
$$

---

## Example

Find:

$$
P(X=3)
$$

when:

$$
p=0.4
$$

### Step 1

$$
P(X=3)=(1-0.4)^2(0.4)
$$

### Step 2

$$
=(0.6)^2(0.4)
$$

### Step 3

$$
=0.36 \times 0.4
$$

$$
=0.144
$$

### Answer

$$
P(X=3)=0.144
$$

---

# B. Probability of At Most \(k\) Trials

Formula:

$$
P(X \le k)=1-(1-p)^k
$$

---

## Example

Find:

$$
P(X \le 5)
$$

when:

$$
p=0.4
$$

### Step 1

$$
P(X \le 5)=1-(1-0.4)^5
$$

### Step 2

$$
=1-(0.6)^5
$$

### Step 3

$$
=1-0.07776
$$

$$
=0.92224
$$

### Answer

$$
P(X \le 5)=0.92224
$$

---

# C. Probability of More Than \(k\) Trials

Formula:

$$
P(X>k)=(1-p)^k
$$

---

## Example

Find:

$$
P(X>4)
$$

when:

$$
p=0.3
$$

### Step 1

$$
P(X>4)=(1-0.3)^4
$$

### Step 2

$$
=(0.7)^4
$$

### Step 3

$$
=0.2401
$$

### Answer

$$
P(X>4)=0.2401
$$

---

# D. Probability on an Interval

Formula:

$$
P(a \le X \le b)=P(X \le b)-P(X<a)
$$

Equivalent form:

$$
P(a \le X \le b)=(1-p)^{a-1}-(1-p)^b
$$

---

## Example

Find:

$$
P(2 \le X \le 5)
$$

when:

$$
p=0.3
$$

### Step 1

$$
P(2 \le X \le 5)=(1-0.3)^1-(1-0.3)^5
$$

### Step 2

$$
=0.7-0.16807
$$

### Step 3

$$
=0.53193
$$

### Answer

$$
P(2 \le X \le 5)=0.53193
$$

---

# 12. Interpretation of Tail Probabilities

The tail probability:

$$
P(X>k)=(1-p)^k
$$

means:

> the probability that no success occurs during the first \(k\) trials.

It represents the probability of waiting longer than \(k\) trials for the first success.

---

# 13. Practical Applications of the Geometric Distribution

The geometric distribution is widely used in practice.

Examples include:

- Number of coin tosses until the first head
- Number of login attempts until success
- Number of defective items checked before finding a good product
- Number of customer calls until a sale is made
- Number of transmitted packets until successful delivery
- Reliability testing in engineering
- Waiting time problems in computer science and telecommunications

---

# 14. Comparison with Other Distributions

The geometric distribution belongs to the family of waiting-time distributions.

Comparison:

| Distribution | Type | Measures |
|---|---|---|
| Bernoulli | Discrete | Single trial outcome |
| Geometric | Discrete | Waiting time until first success |
| Negative Binomial | Discrete | Waiting time until multiple successes |
| Exponential | Continuous | Continuous waiting time |

The geometric distribution is the discrete analogue of the exponential distribution.

---

# Conclusion

The geometric distribution models the number of trials required to obtain the first success in repeated independent Bernoulli trials.

Its key characteristics are:

- infinite support,
- exponentially decreasing probabilities,
- strong dependence on the parameter \(p\),
- practical importance in waiting-time problems.

The larger the probability of success \(p\), the shorter the expected waiting time for the first success.
