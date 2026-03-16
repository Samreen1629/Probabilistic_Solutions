# Task 9 — Digit Restrictions

## Useful Definitions

A **5-digit number** cannot start with 0.

Digits available:

$$
0,1,2,3,4,5,6,7,8,9
$$

---

# Solutions

## 1. Number of 5-digit numbers

The first digit has 9 possibilities (1–9).

The remaining four digits each have 10 possibilities.

Thus:

$$
9 \cdot 10^4
$$

$$
= 90000
$$

---

## 2. Even numbers

The last digit must be even:

$$
0,2,4,6,8
$$

Thus there are 5 possibilities.

The remaining positions:

- first digit: 9 choices
- three middle digits: \(10^3\)

Total:

$$
9 \cdot 10^3 \cdot 5
$$

$$
= 45000
$$

---

## 3. Numbers with no repeated digits

First digit:

$$
9
$$

Second digit:

$$
9
$$

Third digit:

$$
8
$$

Fourth digit:

$$
7
$$

Fifth digit:

$$
6
$$

Total:

$$
9 \cdot 9 \cdot 8 \cdot 7 \cdot 6 = 27216
$$

---

## 4. Numbers with at least one repeated digit

Total numbers:

$$
90000
$$

Numbers with no repeated digits:

$$
27216
$$

Thus

$$
90000 - 27216 = 62784
$$
