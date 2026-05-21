## Problem 8 — Bayes’ formula from a table

# 🌟 Key Definitions and Formulas

## 1. Conditional probability

$$
P(S \mid F) = \frac{P(S \cap F)}{P(F)}
$$

---

## 2. Law of total probability

$$
P(S) = P(S \mid F)P(F) + P(S \mid F^c)P(F^c)
$$

---

## 3. Bayes’ theorem

$$
P(F \mid S) = \frac{P(S \mid F)P(F)}{P(S)}
$$

---

## 4. Base rate
The prior probability:

$$
P(F)
$$

It represents how common fraud is *before* observing any evidence.

---

# 📊 Step 1 — Understand the data

Total transactions = **10,000**

| Type | Suspicious (S) | Not suspicious | Total |
|------|----------------|----------------|-------|
| Fraudulent (F) | 98 | 2 | 100 |
| Legitimate $$(F^c)$$ | 297 | 9603 | 9900 |
| Total | 395 | 9605 | 10000 |

---

# 📌 Step 2 — Compute basic probabilities

## 1. Fraud probability (base rate)

$$
P(F) = \frac{100}{10000} = 0.01
$$

---

## 2. Probability suspicious given fraud

$$
P(S \mid F) = \frac{98}{100} = 0.98
$$

---

## 3. Probability suspicious given legitimate

$$
P(S \mid F^c) = \frac{297}{9900} = 0.03
$$

---

# 📌 Step 3 — Compute $$\(P(S)\)$$ using total probability

$$
P(S) = P(S \mid F)P(F) + P(S \mid F^c)P(F^c)
$$

Substitute values:

$$
P(S) = (0.98)(0.01) + (0.03)(0.99)
$$

Compute each term:

$$
P(S) = 0.0098 + 0.0297
$$

$$
P(S) = 0.0395
$$

---

# 📌 Step 4 — Compute $$\(P(F \mid S)\)$$ using Bayes’ theorem

$$
P(F \mid S) = \frac{P(S \mid F)P(F)}{P(S)}
$$

Substitute:

$$
P(F \mid S) = \frac{0.98 \cdot 0.01}{0.0395}
$$

$$
P(F \mid S) = \frac{0.0098}{0.0395}
$$

$$
P(F \mid S) \approx 0.2481
$$

---

# 📌 Step 5 — Interpretation of result

Among suspicious transactions:

- Fraudulent: ~24.8%
- Legitimate: ~75.2%

✔ Most suspicious transactions are actually **legitimate**.

---

# ⚠️ Step 6 — Why does this happen?

Even though the system is very accurate:

- It detects **98% of frauds**
- It only wrongly flags **3% of legitimate transactions**

👉 The key issue is scale:
- Fraud is extremely rare (1%)

So even a small false-positive rate creates many false alarms.

---

# 📌 Step 7 — Role of the base rate $$\(P(F)\)$$

$$
P(F) = 0.01
$$

This is crucial because:

- Fraud is **rare**
- Legitimate transactions dominate the dataset

Even a highly accurate detector will produce:

- many more false positives (legitimate flagged as suspicious)
- than true positives (actual fraud detected)

---

# 🧠 Final Insight

This is a classic **base rate fallacy** situation:

- High sensitivity (98%) does NOT guarantee high trust in positive alerts
- Because the event being detected is extremely rare

👉 The system is good at detecting fraud, but most alerts are still false because fraud itself is uncommon.
