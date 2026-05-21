## Problem 3 — Conditional probabilities are not symmetric

# 🌟 Key Ideas and Formulas

## 1. Conditional probability
$$
P(A \mid B) = \frac{P(A \cap B)}{P(B)}
$$

This means: *“probability of A happening, given B already happened.”*

---

## 2. Important insight: direction matters
- $$\(P(A \mid B)\)$$ is NOT the same as $$\(P(B \mid A)\)$$
- They answer different real-world questions

---

# 📊 Step 1 — Understand the data

Total users = **150**

| Behavior | Passed quiz (Q) | Did not pass (Q^c) | Total |
|----------|----------------|---------------------|-------|
| Watched lecture (W) | 72 | 18 | 90 |
| Did not watch $$(W^c)$$ | 28 | 32 | 60 |
| Total | 100 | 50 | 150 |

---

# 📌 Step 2 — Compute $$\(P(Q \mid W)\)$$

We use:

$$
P(Q \mid W) = \frac{P(Q \cap W)}{P(W)}
$$

From the table:
- $$\(Q \cap W = 72\)$$
- $$\(W = 90\)$$

$$
P(Q \mid W) = \frac{72}{90}
$$

$$
P(Q \mid W) = 0.8
$$

---

# 📌 Step 3 — Compute $$\(P(W \mid Q)\)$$

$$
P(W \mid Q) = \frac{P(W \cap Q)}{P(Q)}
$$

From the table:
- $$\(W \cap Q = 72\)$$
- $$\(Q = 100\)$$

$$
P(W \mid Q) = \frac{72}{100}
$$

$$
P(W \mid Q) = 0.72
$$

---

# 📌 Step 4 — Compute $$\(P(Q \mid W^c)\)$$

$$
P(Q \mid W^c) = \frac{P(Q \cap W^c)}{P(W^c)}
$$

From the table:
- $$\(Q \cap W^c = 28\)$$
- $$\(W^c = 60\)$$

$$
P(Q \mid W^c) = \frac{28}{60}
$$

$$
P(Q \mid W^c) \approx 0.4667
$$

---

# 📌 Step 5 — Compute $$\(P(W \mid Q^c)\)$$

$$
P(W \mid Q^c) = \frac{P(W \cap Q^c)}{P(Q^c)}
$$

From the table:
- $$\(W \cap Q^c = 18\)$$
- $$\(Q^c = 50\)$$

$$
P(W \mid Q^c) = \frac{18}{50}
$$

$$
P(W \mid Q^c) = 0.36
$$

---

# 📌 Step 6 — Key interpretation: why they differ

### 🔁 $$\(P(Q \mid W)\)$$
> “Among users who watched the lecture, what fraction passed the quiz?”

This measures the **effect of watching** on performance.

---

### 🔁 $$\(P(W \mid Q)\)$$
> “Among users who passed the quiz, what fraction watched the lecture?”

This measures the **profile of successful users**, not the effect.

---

# ⚠️ Why they are not symmetric

Even though both use the same overlap (72 users), they normalize by different totals:

- $$\(P(Q \mid W)\)$$ divides by all watchers (90)
- $$\(P(W \mid Q)\)$$ divides by all passers (100)

So the denominator changes the meaning completely.

---

# 📌 Step 7 — Which is more useful?

## 🎯 To check whether watching helps:

✔ Use:

$$
P(Q \mid W)
$$

Because it directly compares success rates **given exposure to the lecture**.

---

## 🎯 To describe successful users:

✔ Use:

$$
P(W \mid Q)
$$

Because it tells us how many successful students **came from the watching group**.

---

# 🧠 Final Insight

- $$\(P(Q \mid W) = 0.8\)$$ suggests watching the lecture is associated with high success.
- $$\(P(Q \mid W^c) \approx 0.47\)$$ shows a strong drop without watching.

👉 This is a clear example of how conditional probability helps detect *learning impact*, but only when interpreted in the correct direction.
