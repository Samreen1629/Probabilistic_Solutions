# Task 5 — Combinations

## Formula

$$
\binom{n}{k} = \frac{n!}{k!(n-k)!}
$$

---

## 1. Committees of 4 from 12

$$
\binom{12}{4} = 495
$$

---

## 2. Committees containing a particular student

Choose remaining 3 from 11.

$$
\binom{11}{3} = 165
$$

---

## 3. Committees containing at least one of two students

Total committees:

$$
\binom{12}{4}
$$

Committees with neither:

$$
\binom{10}{4}
$$

Result:

$$
495 - 210 = 285
$$

---

## 4. Exactly two women

Choose women and men.

$$
\binom{5}{2}\binom{7}{2}
$$

$$
10 \cdot 21 = 210
$$
