# Task 4 — Weekly Weather Observation

## Useful Definitions and Formulas

**Sample Space**

The set of all possible outcomes of an experiment.

$$
\Omega = \{\text{all elementary outcomes}\}
$$

**Elementary Outcome**

A single possible result of the experiment.

**Number of Outcomes in Repeated Experiments**

If an experiment has \(k\) possible results and is repeated \(n\) times, then

$$
|\Omega| = k^n
$$

---

# Step-by-Step Solution

## 1. Weather Observed on One Day

The weather can be:

- Sunny \(S\)
- Cloudy \(C\)
- Rainy \(R\)

Therefore

$$
\Omega_1 = \{S, C, R\}
$$

Number of elementary outcomes

$$
|\Omega_1| = 3
$$

---

## 2. Two Consecutive Days

Outcomes are ordered pairs.

$$
\Omega_2 =
\{(S,S),(S,C),(S,R),
(C,S),(C,C),(C,R),
(R,S),(R,C),(R,R)\}
$$

Number of outcomes

$$
|\Omega_2| = 3^2 = 9
$$

---

## 3. Seven Consecutive Days

Each day can be \(S,C,R\).

$$
\Omega_7 = \{(w_1,w_2,\dots,w_7) \mid w_i \in \{S,C,R\}\}
$$

Number of outcomes

$$
|\Omega_7| = 3^7 = 2187
$$

---

## 4. Summary

| Experiment | Number of Outcomes |
|---|---|
| One day | \(3\) |
| Two days | \(9\) |
| Seven days | \(2187\) |

---

## 5. Meaning of an Elementary Outcome

An elementary outcome represents **one specific sequence of weather conditions during the week**.

Example:

\[
(S,C,R,S,S,C,R)
\]

means

- Monday: Sunny  
- Tuesday: Cloudy  
- Wednesday: Rainy  
- Thursday: Sunny  
- Friday: Sunny  
- Saturday: Cloudy  
- Sunday: Rainy
