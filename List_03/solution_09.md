## Task 9 — Poisson Model

### 🔹 Given:
- Mean rate (λ) = **5 requests per interval**

The Poisson distribution is used to model the number of events occurring in a fixed interval of time when:
- Events happen independently  
- The average rate (λ) is constant  

The probability formula is:

$$
P(X = k) = \frac{\lambda^k e^{-\lambda}}{k!}
$$

---

## 🔸 1. Probability of exactly 3 requests

We want the probability that **exactly 3 requests** occur:

$$
P(X = 3) = \frac{5^3 e^{-5}}{3!}
$$

### Step-by-step:
- \( 5^3 = 125 \)
- \( 3! = 6 \)

$$
P(X = 3) = \frac{125 \cdot e^{-5}}{6}
$$

Using \( e^{-5} \approx 0.0067 \):

$$
P(X = 3) \approx \frac{125 \times 0.0067}{6}
$$

$$
P(X = 3) \approx 0.1404
$$

### ✅ Interpretation:
There is about a **14.04% chance** that exactly 3 requests occur in this interval.

---

## 🔸 2. Probability of at least one request

“At least one” means:

$$
P(X \ge 1)
$$

Instead of calculating multiple probabilities, we use the complement:

$$
P(X \ge 1) = 1 - P(X = 0)
$$

---

### Step 1: Find \( P(X = 0) \)

$$
P(X = 0) = \frac{5^0 e^{-5}}{0!}
$$

- \( 5^0 = 1 \)
- \( 0! = 1 \)

$$
P(X = 0) = e^{-5} \approx 0.0067
$$

---

### Step 2: Apply complement rule

$$
P(X \ge 1) = 1 - 0.0067
$$

$$
P(X \ge 1) \approx 0.9933
$$

---

### ✅ Interpretation:
There is a **99.33% chance** that **at least one request** occurs.

This makes sense because:
- The average rate (λ = 5) is relatively high  
- So getting zero requests is very unlikely  

---

## 🧠 Key Insights

- **Low k vs high λ:**  
  When λ = 5, getting very small values (like 0 or 1) is unlikely.

- **Peak behavior:**  
  The most probable values will be around **k = 5**.

- **Complement trick:**  
  For “at least one”, always use:
  $$
  1 - P(X = 0)
  $$
  It’s faster and avoids unnecessary calculations.
