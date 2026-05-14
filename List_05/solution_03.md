# Task 3 — Binomial Distribution $Bin(n,p)$

The binomial distribution is one of the most important discrete probability distributions.

It models situations in which:

- an experiment is repeated a fixed number of times,
- each repetition has two possible outcomes,
- the repetitions are independent,
- the probability of success remains constant.

A single trial with two outcomes is called a **Bernoulli trial**.

The Bernoulli distribution is the special case:

$$
Bin(1,p)
$$

The general binomial distribution counts the number of successes in $n$ Bernoulli trials.

---

# 1. Modeling the Experiment

Suppose we perform:

$$
n
$$

independent Bernoulli trials.

Each trial produces:

- success with probability $p$,
- failure with probability $1-p$.

---

## Example Interpretation

Examples of Bernoulli trials:

- tossing a coin,
- checking whether a product is defective,
- whether a customer buys a product,
- whether a machine fails.

Suppose:

- success = “defective product,”
- failure = “non-defective product.”

We inspect $n$ products independently.

---

# 2. Sample Space $\Omega$

Each elementary outcome is a sequence of successes and failures.

For example, for:

$$
n=3
$$

the sample space is:

$$
\Omega=
\{
SSS,\,
SSF,\,
SFS,\,
SFF,\,
FSS,\,
FSF,\,
FFS,\,
FFF
\}
$$

where:

- $S$ = success,
- $F$ = failure.

The number of elementary outcomes equals:

$$
2^n
$$

---

# 3. One Elementary Outcome

An elementary outcome is one complete sequence.

Example:

$$
\omega=(S,F,S,S,F)
$$

This means:

- success in trial 1,
- failure in trial 2,
- success in trial 3,
- success in trial 4,
- failure in trial 5.

---

# 4. Defining the Random Variable

Define:

$$
X(\omega)=\text{number of successes in }\omega
$$

Example:

If

$$
\omega=(S,F,S,S,F)
$$

then:

$$
X(\omega)=3
$$

because there are three successes.

Thus the random variable counts successes.

---

# 5. Probability Mass Function (PMF)

The PMF of the binomial distribution is:

$$
P(X=k)=\binom{n}{k}p^k(1-p)^{n-k}
$$

where:

- $n$ = number of trials,
- $k$ = number of successes,
- $p$ = probability of success.

---

# 6. Interpretation of the Formula

The PMF consists of three parts.

---

## Choosing positions of successes

$$
\binom{n}{k}
$$

counts the number of ways to place $k$ successes among $n$ trials.

---

## Probability of successes

$$
p^k
$$

because each success contributes a factor $p$.

---

## Probability of failures

$$
(1-p)^{n-k}
$$

because there are:

$$
n-k
$$

failures.

---

# 7. Support of the Distribution

The random variable can take values:

$$
0,1,2,\dots,n
$$

Thus the support is:

$$
\{0,1,2,\dots,n\}
$$

---

# 8. PMF Graphs

The PMF graph shows the probability assigned to each possible number of successes.

---

# Case 1 — Fixed $n$, Different $p$

Suppose:

$$
n=10
$$

We compare several values of $p$.

---

## (a) $p=0.2$

Most probability mass is concentrated near small values.

```text
P(X=k)

0.30 ┤
0.25 ┤ ███
0.20 ┤ █████
0.15 ┤ ███████
0.10 ┤ ████████
0.05 ┤ █████████
0.00 └────────────────────────────────
       0 1 2 3 4 5 6 7 8 9 10
```

### Interpretation

Small numbers of successes are most likely because success probability is low.

The distribution is skewed to the right.

---

## (b) $p=0.5$

```text
P(X=k)

0.30 ┤
0.25 ┤           █
0.20 ┤         ███
0.15 ┤       █████
0.10 ┤     ███████
0.05 ┤   █████████
0.00 └────────────────────────────────
       0 1 2 3 4 5 6 7 8 9 10
```

### Interpretation

The distribution becomes approximately symmetric.

The highest probability occurs near:

$$
k=5
$$

---

## (c) $p=0.8$

```text
P(X=k)

0.30 ┤
0.25 ┤                 ███
0.20 ┤               █████
0.15 ┤             ███████
0.10 ┤           █████████
0.05 ┤         ███████████
0.00 └────────────────────────────────
       0 1 2 3 4 5 6 7 8 9 10
```

### Interpretation

Large numbers of successes become most likely.

The distribution is skewed to the left.

---

# 9. Effect of Increasing $p$

As $p$ increases:

- probability mass shifts to the right,
- larger numbers of successes become more likely,
- the distribution changes from right-skewed to left-skewed.

---

# 10. Effect of Increasing $n$

Suppose:

$$
p=0.5
$$

Compare:

- $n=5$,
- $n=20$,
- $n=50$.

As $n$ increases:

- the graph becomes smoother,
- the shape becomes more bell-like,
- probabilities spread across more values.

This illustrates the connection between the binomial and normal distributions.

---

# 11. Cumulative Distribution Function (CDF)

The cumulative distribution function is:

$$
F(k)=P(X\le k)
$$

Thus:

$$
F(k)=\sum_{i=0}^{k}\binom{n}{i}p^i(1-p)^{n-i}
$$

The CDF accumulates probabilities from left to right.

---

# 12. Example CDF Graph

For a binomial distribution, the CDF is a step function.

```text
F(k)

1.00 ┤                             ██████████
0.90 ┤                        █████
0.80 ┤                     ███
0.70 ┤                  ███
0.60 ┤               ███
0.50 ┤            ███
0.40 ┤         ███
0.30 ┤      ███
0.20 ┤   ███
0.10 ┤ ███
0.00 └────────────────────────────────
       0 1 2 3 4 5 6 7 8 9 10
```

---

# 13. How the CDF Changes

---

## When $p$ increases

The CDF rises more slowly at small values because larger numbers of successes become more likely.

---

## When $n$ increases

The CDF becomes smoother and more gradual.

---

# 14. Computing Probabilities

Assume:

$$
X\sim Bin(5,0.4)
$$

Thus:

- $n=5$,
- $p=0.4$.

---

# Example 1 — Computing $P(X=2)$

Using the PMF:

$$
P(X=2)=\binom52(0.4)^2(0.6)^3
$$

Compute:

$$
\binom52=10
$$

Thus:

$$
P(X=2)=10(0.16)(0.216)
$$

$$
=0.3456
$$

---

# Example 2 — Computing $P(X\le2)$

We sum probabilities:

$$
P(X\le2)=P(X=0)+P(X=1)+P(X=2)
$$

Compute each term.

---

## First term

$$
P(X=0)=(0.6)^5
$$

$$
=0.07776
$$

---

## Second term

$$
P(X=1)=\binom51(0.4)(0.6)^4
$$

$$
=5(0.4)(0.1296)
$$

$$
=0.2592
$$

---

## Third term

$$
P(X=2)=0.3456
$$

Therefore:

$$
P(X\le2)=0.07776+0.2592+0.3456
$$

$$
=0.68256
$$

---

# Example 3 — Computing $P(X\ge3)$

Using complements:

$$
P(X\ge3)=1-P(X\le2)
$$

Thus:

$$
P(X\ge3)=1-0.68256
$$

$$
=0.31744
$$

---

# Example 4 — Computing $P(1\le X\le4)$

We can compute:

$$
P(1\le X\le4)
$$

using:

$$
P(X\le4)-P(X\le0)
$$

or by directly summing:

$$
P(X=1)+P(X=2)+P(X=3)+P(X=4)
$$

---

# 15. PMF vs CDF

---

## PMF

The PMF is most useful for:

- exact probabilities,
- individual outcomes,
- identifying the most likely values.

Example:

$$
P(X=3)
$$

---

## CDF

The CDF is most useful for:

- inequalities,
- interval probabilities,
- cumulative probabilities.

Example:

$$
P(X\le3)
$$

---

# 16. Practical Applications

The binomial distribution appears in many practical situations.

---

## Quality Control

Counting defective products.

---

## Medicine

Counting successful treatments.

---

## Marketing

Counting customers who purchase a product.

---

## Reliability Engineering

Counting system failures.

---

## Elections

Counting votes for a candidate.

---

## Genetics

Counting inherited traits.

---

# 17. Possible Interactive Application

An application could allow the user to:

- choose $n$,
- choose $p$,
- generate PMF graphs,
- generate CDF graphs,
- compare two distributions on one plot,
- compute probabilities interactively.

Possible interface elements:

- sliders for parameters,
- automatic graph updates,
- probability calculators.

---

# Final Conceptual Observation

The binomial distribution models repeated independent experiments with two outcomes.

The key idea is:

- counting successes among repeated trials.

The PMF describes:

- probabilities of exact numbers of successes.

The CDF describes:

- accumulated probabilities.

As parameters change:

- the location,
- spread,
- and symmetry

of the distribution also change.

The binomial distribution therefore serves as one of the foundational models of discrete probability theory.
