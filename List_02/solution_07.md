# Task 7 — k-Permutations (Ordered Selections)

## Useful Definitions and Formulas

When we select objects **and order matters**, we use **k-permutations**.

The number of ordered selections of \(k\) objects from \(n\) objects is

$$
P(n,k) = \frac{n!}{(n-k)!}
$$

---

# Solutions

## 1. First three places among 12 runners

Gold, silver, and bronze correspond to an **ordered selection**.

Thus we use

$$
P(12,3)
$$

Compute:

$$
P(12,3) = \frac{12!}{9!}
$$

Simplifying:

$$
12 \cdot 11 \cdot 10 = 1320
$$

---

## 2. 4-digit numbers with distinct digits from 1–9

We choose 4 different digits from the set

$$
\{1,2,3,4,5,6,7,8,9\}
$$

Order matters, so we use

$$
P(9,4)
$$

Compute:

$$
9 \cdot 8 \cdot 7 \cdot 6 = 3024
$$

---

## 3. Numbers divisible by 5

A number is divisible by 5 if the last digit is **5**.

Thus the last digit is fixed.

Remaining digits must be chosen from the remaining 8 digits.

Number of possibilities:

$$
P(8,3)
$$

Compute:

$$
8 \cdot 7 \cdot 6 = 336
$$
