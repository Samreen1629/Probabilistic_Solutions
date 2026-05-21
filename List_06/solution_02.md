## Problem 2 — Four regions of a sample space

---

# 🌟 Key Definitions and Formulas

## 1. Probability of an event
$$
P(A) = \frac{\text{number of favorable outcomes}}{\text{total outcomes}}
$$

---

## 2. Complement rule
$$
P(A^c) = 1 - P(A)
$$

---

## 3. Intersection (AND)

$$
A \cap B
$$

means both events happen simultaneously.

---

## 4. Union (OR)
$$
P(A \cup B) = P(A) + P(B) - P(A \cap B)
$$

---

## 5. Conditional probability
$$
P(A \mid B) = \frac{P(A \cap B)}{P(B)}
$$

---

## 📊 Step 1 — Understand the data

Total tickets = **350**

| Ticket type | Solved (S) | Not solved (S^c) | Total |
|-------------|------------|------------------|-------|
| Technical (T) | 90 | 60 | 150 |
| Non-technical $$(T^c)$$ | 160 | 40 | 200 |
| Total | 250 | 100 | 350 |

---

## 📌 Step 2 — Four disjoint regions

We divide the sample space into four parts:

### 1. Technical and solved
$$
P(T \cap S) = \frac{90}{350} = 0.2571
$$

---

### 2. Technical and not solved
$$
P(T \cap S^c) = \frac{60}{350} = 0.1714
$$

---

### 3. Non-technical and solved
$$
P(T^c \cap S) = \frac{160}{350} = 0.4571
$$

---

### 4. Non-technical and not solved
$$
P(T^c \cap S^c) = \frac{40}{350} = 0.1143
$$

---

## ✅ Step 3 — Verify total probability

We check:

$$
0.2571 + 0.1714 + 0.4571 + 0.1143 = 1.0000
$$

✔ The four regions form a complete partition of the sample space.

---

## 📌 Step 4 — Compute $$\(P(T \cup S)\)$$

Using:

$$
P(T \cup S) = P(T) + P(S) - P(T \cap S)
$$

### First compute marginals:

$$
P(T) = \frac{150}{350} = 0.4286
$$

$$
P(S) = \frac{250}{350} = 0.7143
$$

$$
P(T \cap S) = 0.2571
$$

---

### Now compute union:

$$
P(T \cup S) = 0.4286 + 0.7143 - 0.2571
$$

$$
P(T \cup S) = 0.8858
$$

---

## 📌 Step 5 — Compute $$\(P(T^c \cup S)\)$$

We use:

$$
P(T^c \cup S) = 1 - P(T \cap S^c)
$$

From earlier:

$$
P(T \cap S^c) = 0.1714
$$

So:

$$
P(T^c \cup S) = 1 - 0.1714 = 0.8286
$$

---

## 📌 Step 6 — Conditional probabilities

### 1. Probability solved given technical

$$
P(S \mid T) = \frac{P(T \cap S)}{P(T)}
$$

$$
P(S \mid T) = \frac{0.2571}{0.4286} = 0.6
$$

---

### 2. Probability solved given non-technical

$$
P(S \mid T^c) = \frac{P(T^c \cap S)}{P(T^c)}
$$

$$
P(S \mid T^c) = \frac{0.4571}{0.5714} \approx 0.8
$$

---

## 📌 Step 7 — Interpretation

### 🔍 Does being technical change the probability of being solved first contact?

Yes — clearly.

- $$\(P(S \mid T) = 0.6\)$$
- $$\(P(S \mid T^c) = 0.8\)$$

👉 Non-technical tickets are **more likely** to be solved on first contact than technical ones.

---

## 🎯 Final Insight

This result suggests an operational pattern:

- Technical issues are harder or require escalation.
- Non-technical issues are more routine and faster to resolve.

So, **ticket type strongly influences resolution success at first contact**.
