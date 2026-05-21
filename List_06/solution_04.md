## Problem 4 — Inclusion–Exclusion and Double Counting

# 🌟 Key Definitions and Formulas

## 1. Probability of an event

$$
P(A) = \frac{\text{number of outcomes in } A}{\text{total outcomes}}
$$

---

## 2. Intersection (overlap)

$$
A \cap B
$$

means elements that belong to both sets.

---

## 3. Inclusion–Exclusion Principle
This corrects double counting:

$$
P(A \cup B) = P(A) + P(B) - P(A \cap B)
$$

---

## 4. Conditional probability
$$
P(A \mid B) = \frac{P(A \cap B)}{P(B)}
$$

---

# 📊 Step 1 — Understand the data

Total employees = **200**

- $$|A| = 130$$  
- $$|B| = 90$$  
- $$|A \cap B| = 60$$  

---

# 📌 Step 2 — Compute basic probabilities

## 1. Probability of A

$$
P(A) = \frac{130}{200} = 0.65
$$

---

## 2. Probability of B

$$
P(B) = \frac{90}{200} = 0.45
$$

---

## 3. Probability of both A and B

$$
P(A \cap B) = \frac{60}{200} = 0.30
$$

---

# 📌 Step 3 — Compute union using inclusion–exclusion

$$
P(A \cup B) = P(A) + P(B) - P(A \cap B)
$$

Substitute:

$$
P(A \cup B) = 0.65 + 0.45 - 0.30
$$

$$
P(A \cup B) = 0.80
$$

---

# 📌 Step 4 — Remaining regions

## 1. A only (A \ B)

$$
P(A \setminus B) = P(A) - P(A \cap B)
$$

$$
P(A \setminus B) = 0.65 - 0.30 = 0.35
$$

---

## 2. B only (B \ A)

$$
P(B \setminus A) = P(B) - P(A \cap B)
$$

$$
P(B \setminus A) = 0.45 - 0.30 = 0.15
$$

---

## 3. Neither A nor B

First compute union:

$$
P(A \cup B) = 0.80
$$

So complement:

$$
P(A^c \cap B^c) = 1 - 0.80 = 0.20
$$

---

# 📌 Step 5 — Conditional probabilities

## 1. $$\(P(A \mid B)\)$$

$$
P(A \mid B) = \frac{P(A \cap B)}{P(B)}
$$

$$
P(A \mid B) = \frac{0.30}{0.45} = 0.6667
$$

---

## 2. $$\(P(B \mid A)\)$$

$$
P(B \mid A) = \frac{P(A \cap B)}{P(A)}
$$

$$
P(B \mid A) = \frac{0.30}{0.65} \approx 0.4615
$$

---

# 📌 Step 6 — Why is union NOT simple addition?

We compare:

### Incorrect idea:

$$
P(A) + P(B) = 0.65 + 0.45 = 1.10
$$

But probabilities cannot exceed 1.

---

### Correct idea:
We subtract overlap:

$$
P(A \cup B) = 0.80
$$

---

# ⚠️ Why the difference happens

The overlap $$A \cap B$$ is counted twice:

- once inside $$P(A)$$  
- once inside $$P(B)$$  

So:

👉 We must subtract it once to fix double counting.

---

# 📌 Step 7 — Which group is counted twice?

The group counted twice is:

$$
A \cap B
$$

✔ These are employees who use **both tools**

---

# 🎯 Final Insight

- 30% of employees use both tools — this overlap is significant.
- Without correcting for overlap, we overestimate total users.
- Inclusion–exclusion ensures we count each employee exactly once.

👉 This is a foundational idea in probability: **correcting for overlap is essential in all real-world counting problems.**
