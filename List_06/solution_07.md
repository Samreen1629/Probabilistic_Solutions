## Problem 7 — Conditional probability with three categories

# 🌟 Key Definitions and Formulas

## 1. Partition of a sample space
Events $$\(H, M, L\)$$ form a partition if:

- They are **mutually exclusive**:
- 
$$
H \cap M = \emptyset,\quad H \cap L = \emptyset,\quad M \cap L = \emptyset
$$

- They are **collectively exhaustive**:
- 
$$
H \cup M \cup L = \Omega
$$

---

## 2. Conditional probability

$$
P(R \mid A) = \frac{P(R \cap A)}{P(A)}
$$

---

## 3. Law of total probability
If \(H, M, L\) form a partition:

$$
P(R) = P(R \mid H)P(H) + P(R \mid M)P(M) + P(R \mid L)P(L)
$$

---

## 4. Bayes’ theorem (for reversal of conditioning)

$$
P(H \mid R) = \frac{P(R \mid H)P(H)}{P(R)}
$$

---

# 📊 Step 1 — Understand the data

Total customers = **400**

| Activity level | Renewed (R) | Not renewed | Total |
|----------------|-------------|-------------|-------|
| High (H) | 80 | 20 | 100 |
| Medium (M) | 90 | 60 | 150 |
| Low (L) | 30 | 120 | 150 |
| Total | 200 | 200 | 400 |

---

# 📌 Step 2 — Why $$\(H, M, L\)$$ form a partition

They satisfy:

### 1. No overlap
A customer cannot be in two activity levels at the same time:

$$
H \cap M = H \cap L = M \cap L = \emptyset
$$

### 2. Complete coverage
Every customer belongs to exactly one category:

$$
H \cup M \cup L = \Omega
$$

✔ Therefore, $$\(H, M, L\)$$ form a **partition of the sample space**.

---

# 📌 Step 3 — Compute probabilities

## 1. Activity level probabilities

$$
P(H) = \frac{100}{400} = 0.25
$$

$$
P(M) = \frac{150}{400} = 0.375
$$

$$
P(L) = \frac{150}{400} = 0.375
$$

---

# 📌 Step 4 — Conditional probabilities of renewal

## 1. High activity

$$
P(R \mid H) = \frac{80}{100} = 0.8
$$

---

## 2. Medium activity

$$
P(R \mid M) = \frac{90}{150} = 0.6
$$

---

## 3. Low activity

$$
P(R \mid L) = \frac{30}{150} = 0.2
$$

---

# 📌 Step 5 — Compute $$\(P(R)\)$$ using total probability

$$
P(R) = P(R \mid H)P(H) + P(R \mid M)P(M) + P(R \mid L)P(L)
$$

Substitute values:

$$
P(R) = (0.8)(0.25) + (0.6)(0.375) + (0.2)(0.375)
$$

Compute each term:

$$
P(R) = 0.2 + 0.225 + 0.075
$$

$$
P(R) = 0.5
$$

---

# 📌 Step 6 — Compute posterior probabilities

## 1. $$\(P(H \mid R)\)$$

$$
P(H \mid R) = \frac{P(R \mid H)P(H)}{P(R)}
$$

$$
P(H \mid R) = \frac{0.8 \cdot 0.25}{0.5}
$$

$$
P(H \mid R) = \frac{0.2}{0.5} = 0.4
$$

---

## 2. $$\(P(M \mid R)\)$$

$$
P(M \mid R) = \frac{0.6 \cdot 0.375}{0.5}
$$

$$
P(M \mid R) = \frac{0.225}{0.5} = 0.45
$$

---

## 3. $$\(P(L \mid R)\)$$

$$
P(L \mid R) = \frac{0.2 \cdot 0.375}{0.5}
$$

$$
P(L \mid R) = \frac{0.075}{0.5} = 0.15
$$

---

# 📌 Step 7 — Interpretation of key difference

## 1. $$\(P(R \mid H)\)$$

$$
P(R \mid H) = 0.8
$$

👉 “Given high activity, probability of renewal”

- Focus: behavior *within a group*

---

## 2. $$\(P(H \mid R)\)$$

$$
P(H \mid R) = 0.4
$$

👉 “Given renewal, probability customer was high activity”

- Focus: composition of renewals

---

# ⚠️ Key insight

These are NOT the same because:

- One conditions on **activity level**
- The other conditions on **renewal outcome**

---

# 🎯 Final Conclusion

- High activity users renew most often (80%)
- But among all renewals, only 40% are high activity users
- Medium activity dominates the renewal pool due to its size

👉 This is a classic example of how **Bayes’ theorem reverses perspective between cause and effect**.
