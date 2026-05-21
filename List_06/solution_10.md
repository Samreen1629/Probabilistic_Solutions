## Problem 10 — Comprehensive problem: event algebra, conditioning, independence, and Bayes

# 🌟 Key Definitions and Formulas

## 1. Joint probability (from counts)

$$
P(A \cap B) = \frac{\text{count in both A and B}}{\text{total}}
$$

---

## 2. Marginal probability

$$
P(A) = \sum P(A \cap B_i)
$$

---

## 3. Conditional probability

$$
P(A \mid B) = \frac{P(A \cap B)}{P(B)}
$$

---

## 4. Union (inclusion–exclusion)

$$
P(A \cup B) = P(A) + P(B) - P(A \cap B)
$$

---

## 5. Independence

$$
A \perp B \iff P(A \cap B) = P(A)P(B)
$$

---

## 📊 Step 1 — Understand the data

Total users = **500**

| Group | Completed (C) | Not completed (C^c) | Total |
|------|--------------|---------------------|-------|
| Tutorial (T) | 180 | 70 | 250 |
| No tutorial $$(T^c)$$ | 120 | 130 | 250 |
| Total | 300 | 200 | 500 |

---

# 📌 Step 2 — Four disjoint regions

Convert counts to probabilities:

## 1. Tutorial and completed

$$
P(T \cap C) = \frac{180}{500} = 0.36
$$

---

## 2. Tutorial and not completed

$$
P(T \cap C^c) = \frac{70}{500} = 0.14
$$

---

## 3. No tutorial and completed

$$
P(T^c \cap C) = \frac{120}{500} = 0.24
$$

---

## 4. No tutorial and not completed

$$
P(T^c \cap C^c) = \frac{130}{500} = 0.26
$$

---

# 📌 Step 3 — Compute marginals

## 1. $$\(P(T)\)$$

$$
P(T) = \frac{250}{500} = 0.5
$$

---

## 2. $$\(P(C)\)$$

$$
P(C) = \frac{300}{500} = 0.6
$$

---

## 3. $$\(P(T \cup C)\)$$

$$
P(T \cup C) = P(T) + P(C) - P(T \cap C)
$$

$$
P(T \cup C) = 0.5 + 0.6 - 0.36
$$

$$
P(T \cup C) = 0.74
$$

---

# 📌 Step 4 — Conditional probabilities

## 1. $$\(P(C \mid T)\)$$

$$
P(C \mid T) = \frac{P(T \cap C)}{P(T)}
$$

$$
P(C \mid T) = \frac{0.36}{0.5} = 0.72
$$

---

## 2. $$\(P(C \mid T^c)\)$$

$$
P(C \mid T^c) = \frac{0.24}{0.5} = 0.48
$$

---

## 3. $$\(P(T \mid C)\)$$

$$
P(T \mid C) = \frac{P(T \cap C)}{P(C)}
$$

$$
P(T \mid C) = \frac{0.36}{0.6} = 0.6
$$

---

## 4. $$\(P(T \mid C^c)\)$$

$$
P(T \mid C^c) = \frac{P(T \cap C^c)}{P(C^c)}
$$

First:

$$
P(C^c) = 1 - 0.6 = 0.4
$$

Now:

$$
P(T \mid C^c) = \frac{0.14}{0.4} = 0.35
$$

---

# 📌 Step 5 — Independence check

Compare:

$$
P(T)P(C) = 0.5 \cdot 0.6 = 0.3
$$

But:

$$
P(T \cap C) = 0.36
$$

❌ Not equal → events are **not independent**

---

# 📌 Step 6 — Does tutorial help completion?

Compare conditional probabilities:

$$
P(C \mid T) = 0.72
$$

$$
P(C \mid T^c) = 0.48
$$

✔ Yes — receiving a tutorial increases completion probability significantly.

---

# 📌 Step 7 — Key conceptual difference

## 1. $$\(P(C \mid T)\)$$

> Probability of completing onboarding given tutorial

- measures **effect of tutorial on success**
- causal direction (treatment → outcome)

---

## 2. $$\(P(T \mid C)\)$$

> Probability user had tutorial given they completed onboarding

- measures **composition of successful users**
- diagnostic direction (outcome → origin)

---

# ⚠️ Why they differ

They normalize by different totals:

- $$\(P(C \mid T)\)$$: divide by all tutorial users
- $$\(P(T \mid C)\)$$: divide by all completed users

So they answer fundamentally different questions.

---

# 🎯 Final Interpretation

- Tutorial significantly improves onboarding success:
  - 72% vs 48%
- Users who complete onboarding are more likely to have had the tutorial (60%)
- Events are not independent → tutorial has a measurable effect

👉 Overall conclusion: **the tutorial is strongly associated with better onboarding performance, but conditional probabilities must be interpreted carefully depending on direction.**
