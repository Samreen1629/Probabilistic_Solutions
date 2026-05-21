## Problem 9 — Law of total probability without a full table

# 🌟 Key Definitions and Formulas

## 1. Partition of a sample space

Events $$\(W, A, H\)$$ form a partition if:

- They are mutually exclusive:
- 
$$
W \cap A = W \cap H = A \cap H = \emptyset
$$

- They cover all outcomes:
- 
$$
W \cup A \cup H = \Omega
$$

---

## 2. Law of total probability

If $$\(W, A, H\)$$ form a partition:

$$
P(C) = P(C \mid W)P(W) + P(C \mid A)P(A) + P(C \mid H)P(H)
$$

---

## 3. Bayes’ theorem

$$
P(W \mid C) = \frac{P(C \mid W)P(W)}{P(C)}
$$

---

# 📊 Step 1 — Why $$\(W, A, H\)$$ form a partition

They represent all possible order channels:

- every order comes from exactly one channel
- no order can come from more than one channel

So:

$$
W \cup A \cup H = \Omega
$$

and

$$
W \cap A = W \cap H = A \cap H = \emptyset
$$

✔ Therefore, $$\(W, A, H\)$$ form a **partition of the sample space**.

---

# 📌 Step 2 — Given probabilities

$$
P(W) = 0.50,\quad P(A) = 0.35,\quad P(H) = 0.15
$$

$$
P(C \mid W) = 0.04,\quad P(C \mid A) = 0.06,\quad P(C \mid H) = 0.10
$$

---

# 📌 Step 3 — Compute $$\(P(C)\)$$

Using total probability:

$$
P(C) = (0.04)(0.50) + (0.06)(0.35) + (0.10)(0.15)
$$

Compute each term:

$$
P(C) = 0.02 + 0.021 + 0.015
$$

$$
P(C) = 0.056
$$

---

# 📌 Step 4 — Compute posterior probabilities

## 1. Website

$$
P(W \mid C) = \frac{P(C \mid W)P(W)}{P(C)}
$$

$$
P(W \mid C) = \frac{0.04 \cdot 0.50}{0.056}
$$

$$
P(W \mid C) = \frac{0.02}{0.056} \approx 0.3571
$$

---

## 2. Mobile app

$$
P(A \mid C) = \frac{0.06 \cdot 0.35}{0.056}
$$

$$
P(A \mid C) = \frac{0.021}{0.056} \approx 0.3750
$$

---

## 3. Phone

$$
P(H \mid C) = \frac{0.10 \cdot 0.15}{0.056}
$$

$$
P(H \mid C) = \frac{0.015}{0.056} \approx 0.2679
$$

---

# 📌 Step 5 — Which channel dominates cancelled orders?

Comparing:

- Website: ~0.357
- Mobile app: ~0.375
- Phone: ~0.268

✔ Most cancelled orders come from the **mobile app**.

---

# ⚠️ Step 6 — Is this the same as highest cancellation rate?

No.

We compare cancellation rates:

- Website: 0.04
- Mobile app: 0.06
- Phone: 0.10 (highest rate)

---

# 🧠 Key insight

Even though phone has the highest cancellation rate, it contributes fewer cancellations overall because:

- it has a small share of orders (15%)

Mobile app dominates cancellations because:

- it has a large share of orders (35%)
- and a moderate cancellation rate

---

# 🎯 Final Conclusion

- The mobile app produces the most cancelled orders overall
- The phone channel is the riskiest per order
- These are different questions:

## 🔁 Important distinction:

- $$\(P(C \mid \text{channel})\)$$ → risk per order
- $$\(P(\text{channel} \mid C)\)$$ → composition of cancelled orders

👉 This shows why base rates matter: both probability and volume determine outcomes.
