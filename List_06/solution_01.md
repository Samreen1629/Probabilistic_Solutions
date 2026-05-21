# Task List 06 — Algebra of Events and Conditional Probability

# Problem 1 — Event Algebra from a Two-Way Table

## 🌟 Key Definitions and Formulas

Before solving the problem, here are the most important probability concepts we will use.

### 1. Probability of an event
For an event $$\(A\$$):

$$
P(A) = \frac{\text{number of favorable outcomes}}{\text{total number of outcomes}}
$$

---

### 2. Complement of an event
If $$\(A\)$$ is an event, then its complement $$\(A^c\)$$ means “A does not happen”:

$$
P(A^c) = 1 - P(A)
$$

---

### 3. Intersection (AND)
$$\(A \cap B\)$$ means both events happen at the same time.

---

### 4. Union (OR)
$$\(A \cup B\)$$ means at least one of the events happens:

$$
P(A \cup B) = P(A) + P(B) - P(A \cap B)
$$

---

### 5. Conditional probability
Probability of $$\(A\)$$ given $$\(B\)$$:

$$
P(A \mid B) = \frac{P(A \cap B)}{P(B)}
$$

---

### 6. Independence
Two events are independent if:

$$
P(A \cap B) = P(A)\cdot P(B)
$$

---

## 📊 Step 1 — Interpret the table

| Student type | Submit on time (B) | Not on time (B^c) | Total |
|--------------|--------------------|-------------------|-------|
| Attends regularly (A) | 48 | 12 | 60 |
| Does not attend $$(A^c)$$ | 22 | 18 | 40 |
| Total | 70 | 30 | 100 |

Total students = 100

---

## 📌 Step 2 — Fill the disjoint regions

We directly identify the four joint events:

- $$\(A \cap B = 48\)$$
- $$\(A \cap B^c = 12\)$$
- $$\(A^c \cap B = 22\)$$
- $$\(A^c \cap B^c = 18\)$$

Convert to probabilities (divide by 100):

$$
P(A \cap B) = \frac{48}{100} = 0.48
$$

$$
P(A \cap B^c) = \frac{12}{100} = 0.12
$$

$$
P(A^c \cap B) = \frac{22}{100} = 0.22
$$

$$
P(A^c \cap B^c) = \frac{18}{100} = 0.18
$$

---

## 📌 Step 3 — Compute marginal probabilities

### Probability of attending lectures:

$$
P(A) = \frac{60}{100} = 0.6
$$

### Probability of submitting on time:

$$
P(B) = \frac{70}{100} = 0.7
$$

---

## 📌 Step 4 — Compute union $$\(P(A \cup B)\)$$

Using the formula:

$$
P(A \cup B) = P(A) + P(B) - P(A \cap B)
$$

Substitute values:

$$
P(A \cup B) = 0.6 + 0.7 - 0.48
$$

$$
P(A \cup B) = 0.82
$$

---

## 📌 Step 5 — Conditional probabilities

### 1. $$\(P(A \mid B)\)$$

$$
P(A \mid B) = \frac{P(A \cap B)}{P(B)}
$$

$$
P(A \mid B) = \frac{0.48}{0.7} \approx 0.6857
$$

---

### 2. $$\(P(B \mid A)\)$$

$$
P(B \mid A) = \frac{P(A \cap B)}{P(A)}
$$

$$
P(B \mid A) = \frac{0.48}{0.6} = 0.8
$$

---

## 📌 Step 6 — Are A and B mutually exclusive?

Mutually exclusive means they cannot happen together:

- Here $$\(A \cap B = 48 > 0\)$$

❌ Therefore, **A and B are NOT mutually exclusive**.

---

## 📌 Step 7 — Are A and B independent?

Check independence condition:

$$
P(A)P(B) = 0.6 \cdot 0.7 = 0.42
$$

But:

$$
P(A \cap B) = 0.48
$$

Since:

$$
0.48 \ne 0.42
$$

❌ Therefore, **A and B are NOT independent**.

---

## 🧠 Step 8 — Interpretations

### 1. Interpretation of $$\(P(A \mid B)\)$$

$$\(P(A \mid B) \approx 0.686\)$$ means:

> If a student submits homework on time, there is about a **68.6% chance** that they attend lectures regularly.

---

### 2. Interpretation of $$\(P(B \mid A)\)$$

$$\(P(B \mid A) = 0.8\)$$ means:

> If a student attends lectures regularly, there is an **80% chance** they submit homework on time.

---

## 🎯 Final Insight

This dataset shows a clear positive relationship between attending lectures and submitting homework on time — but not strong enough to make the events independent. Attendance improves submission behavior, but does not fully determine it.
