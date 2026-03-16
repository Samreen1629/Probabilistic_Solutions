# Task 10 — Urn Models

## Problem Setup

The urn contains:

- 5 red balls
- 4 blue balls
- 3 green balls

Total balls:

$$
5 + 4 + 3 = 12
$$

---

# Solutions

## 1. Three balls drawn, order ignored

This is a combination.

$$
\binom{12}{3}
$$

$$
= 220
$$

---

## 2. Exactly two red balls

Choose:

- 2 red balls from 5
- 1 non-red ball from 7

Thus

$$
\binom{5}{2}\binom{7}{1}
$$

Compute:

$$
10 \cdot 7 = 70
$$

---

## 3. Order of colors recorded

Now the order matters.

Thus we count permutations of 3 balls from 12.

$$
P(12,3)
$$

$$
12 \cdot 11 \cdot 10 = 1320
$$

---

## 4. Exactly two red balls (ordered)

First choose positions of the non-red ball.

There are

$$
3
$$

possible positions.

Choose the red balls:

$$
P(5,2)
$$

Choose the non-red ball:

$$
7
$$

Total:

$$
3 \cdot P(5,2) \cdot 7
$$

$$
3 \cdot 20 \cdot 7 = 420
$$
