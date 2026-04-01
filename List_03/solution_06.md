## Task 6 — Binomial Model

Given:
- $n = 10$
- $p = 0.04$

---

### 1. Exactly 2 defective

$$
P(X = 2) = \binom{10}{2}(0.04)^2(0.96)^8
$$

$$
= 45 \cdot 0.0016 \cdot 0.721
\approx 0.0519
$$

---

### 2. At least one defective

$$
P(X \ge 1) = 1 - P(X = 0)
$$

$$
P(X = 0) = (0.96)^{10} \approx 0.6648
$$

$$
P(X \ge 1) \approx 1 - 0.6648 = 0.3352
$$
