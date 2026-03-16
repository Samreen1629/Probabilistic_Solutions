# Task 2 — Permutations

## Key Formula

A permutation of \(n\) objects:

$$
n!
$$

---

## Solutions

### 1. Arranging 8 different books

We arrange all books.

$$
8! = 40320
$$

---

### 2. Two particular people must sit next to each other

Treat the pair as one block.

Objects to arrange:

- the pair
- the remaining 6 people

Total objects:

7

$$
7!
$$

Inside the pair the two people can swap.

$$
2!
$$

Total arrangements:

$$
7! \cdot 2 = 5040 \cdot 2 = 10080
$$

---

### 3. Two people must NOT sit next to each other

Total arrangements:

$$
8! = 40320
$$

Subtract cases where they sit together:

$$
40320 - 10080 = 30240
$$

---

### 4. First question fixed

Only remaining 9 questions can change.

$$
9! = 362880
$$
