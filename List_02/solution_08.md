# Task 8 — Sequences with Repetition

## Useful Definitions and Formulas

If we form sequences of length \(k\) using \(n\) symbols and repetition is allowed, the number of sequences is

$$
n^k
$$

For PIN codes:

- digits available: 0–9
- number of digits: 5

---

# Solutions

## 1. Number of possible 5-digit PIN codes

Each position has 10 possible digits.

Thus the number of codes is

$$
10^5
$$

$$
= 100000
$$

---

## 2. Codes containing at least one repeated digit

First compute the total number of codes:

$$
10^5
$$

Now compute codes with **all digits different**.

This is an ordered selection:

$$
P(10,5)
$$

Compute:

$$
10 \cdot 9 \cdot 8 \cdot 7 \cdot 6 = 30240
$$

Therefore codes with **at least one repeated digit**:

$$
100000 - 30240 = 69760
$$

---

## 3. Codes with all digits different

From above:

$$
P(10,5) = 30240
$$
