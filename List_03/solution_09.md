## Task 9 — Poisson Model

Given:
- $\lambda = 5$

---

### 1. Exactly 3 requests

$$
P(X = 3) = \frac{5^3 e^{-5}}{3!}
$$

$$
= \frac{125 e^{-5}}{6}
\approx 0.1404
$$

---

### 2. At least one request

$$
P(X \ge 1) = 1 - P(X = 0)
$$

$$
P(X = 0) = e^{-5} \approx 0.0067
$$

$$
P(X \ge 1) \approx 1 - 0.0067 = 0.9933
$$
