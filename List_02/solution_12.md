# Task 12 — Mixed Counting Problems

## 1. Student ID Codes

Two letters from:

$$
\{A,B,C,D,E\}
$$

Three digits from:

$$
0–9
$$

---

### (a) Letters and digits may repeat

Letters:

$$
5^2
$$

Digits:

$$
10^3
$$

Total:

$$
5^2 \cdot 10^3
$$

$$
25 \cdot 1000 = 25000
$$

---

### (b) Letters cannot repeat

Letters:

$$
P(5,2)
$$

Digits:

$$
10^3
$$

Total:

$$
20 \cdot 1000 = 20000
$$

---

### (c) No repetition at all

Letters:

$$
P(5,2)
$$

Digits:

$$
P(10,3)
$$

Total:

$$
20 \cdot 720 = 14400
$$

---

## 2. Medal Assignment

### (a)

Ordered medals:

$$
P(12,3) = 1320
$$

---

### (b)

Two particular runners must receive medals.

Choose positions for them:

$$
P(3,2)
$$

Choose the third medal winner:

$$
10
$$

Total:

$$
6 \cdot 10 = 60
$$

---

## 3. Committee Selection

### (a)

$$
\binom{10}{4} = 210
$$

---

### (b)

Exactly two women:

$$
\binom{4}{2}\binom{6}{2}
$$

$$
6 \cdot 15 = 90
$$

---

### (c)

At least one woman.

Total committees:

$$
210
$$

All-men committees:

$$
\binom{6}{4} = 15
$$

Result:

$$
210 - 15 = 195
$$

---

## 4. Circular Seating

### (a)

$$
(7-1)! = 720
$$

---

### (b)

Two people sit together.

$$
5! \cdot 2 = 240
$$

---

## 5. Passwords

Characters available:

- 10 digits
- 26 letters

Total:

$$
36
$$

---

### (a) Repetition allowed

$$
36^5
$$

---

### (b) No repetition

$$
P(36,5)
$$

---

### (c)

- repetition allowed → **sequence with repetition**
- no repetition → **k-permutation**
