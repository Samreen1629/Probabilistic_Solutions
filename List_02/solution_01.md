# Task 1 — Recognizing Counting Models

## Useful Definitions

Before identifying the correct counting model, we check:

1. Are **all objects used** or only some?
2. Does **order matter**?
3. Is **repetition allowed**?
4. Are objects **identical or distinct**?

Common models:

- **Permutation:** arranging all objects where order matters.

$$
n!
$$

- **Combination:** selecting objects where order does not matter.

$$
\binom{n}{k} = \frac{n!}{k!(n-k)!}
$$

- **k-permutation:** ordered selection without repetition.

$$
P(n,k) = \frac{n!}{(n-k)!}
$$

- **Sequence with repetition:** ordered selection with repetition.

$$
n^k
$$

- **Circular permutation:** arrangements around a circle.

$$
(n-1)!
$$

- **Permutation with repeated elements**

$$
\frac{n!}{n_1!n_2!\dots n_r!}
$$

---

## Solutions

### 1. Arranging 7 students in a line

All objects are arranged and order matters.

**Model:** permutation.

---

### 2. Choosing 4 members of a committee from 12 people

Order does not matter.

**Model:** combination.

---

### 3. Assigning gold, silver, bronze medals among 15 athletes

Order matters because medal ranking matters.

**Model:** k-permutation.

---

### 4. Forming a 6-digit PIN code

Digits may repeat and order matters.

**Model:** sequence with repetition.

---

### 5. Arranging the letters of BANANA

Some letters repeat.

**Model:** permutation with repeated elements.

---

### 6. Seating 6 people around a round table

Rotation does not matter.

**Model:** circular permutation.
