# Task 6 — Combinations in Card Problems

## Useful Definitions and Formulas

When selecting cards from a deck, the **order of cards does not matter**, therefore we use **combinations**.

The number of ways to choose \(k\) objects from \(n\) objects is

$$
\binom{n}{k} = \frac{n!}{k!(n-k)!}
$$

A standard deck contains:

- 52 cards
- 13 hearts
- 39 non-hearts

---

# Solutions

## 1. Exactly 2 hearts in a 5-card hand

We must choose:

- 2 hearts from the 13 hearts
- 3 other cards from the 39 non-hearts

Number of ways:

$$
\binom{13}{2}\binom{39}{3}
$$

---

## 2. At least one heart

It is easier to compute the complement.

Total 5-card hands:

$$
\binom{52}{5}
$$

Hands with **no hearts**:

$$
\binom{39}{5}
$$

Therefore the number of hands with **at least one heart** is

$$
\binom{52}{5} - \binom{39}{5}
$$

---

## 3. No face cards

Face cards are:

- J
- Q
- K

There are 12 face cards.

Thus there are

$$
52 - 12 = 40
$$

non-face cards.

Number of 5-card hands with no face cards:

$$
\binom{40}{5}
$$
