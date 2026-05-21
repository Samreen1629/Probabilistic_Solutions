## Problem 5 — Independence from data

# 🌟 Key Definitions and Formulas

## 1. Probability of an event

$$
P(A) = \frac{\text{number of favorable outcomes}}{\text{total outcomes}}
$$

---

## 2. Intersection

$$
A \cap B
$$

means both events happen together.

---

## 3. Conditional probability

$$
P(M \mid A) = \frac{P(A \cap M)}{P(A)}
$$

---

## 4. Independence
Two events are independent if:

$$
P(A \cap M) = P(A)\cdot P(M)
$$

or equivalently:

$$
P(M \mid A) = P(M)
$$

---

# 📊 Step 1 — Understand the data

Total users = **200**

| Account type | Watched (M) | Not watched (M^c) | Total |
|-------------|-------------|-------------------|-------|
| Premium (A) | 84 | 36 | 120 |
| Free $$(A^c)$$ | 56 | 24 | 80 |
| Total | 140 | 60 | 200 |

---

# 📌 Step 2 — Compute basic probabilities

## 1. Probability of premium account

$$
P(A) = \frac{120}{200} = 0.6
$$

---

## 2. Probability of watching a movie

$$
P(M) = \frac{140}{200} = 0.7
$$

---

## 3. Probability of both premium and watched

$$
P(A \cap M) = \frac{84}{200} = 0.42
$$

---

# 📌 Step 3 — Conditional probabilities

## 1. Probability of watching given premium

$$
P(M \mid A) = \frac{P(A \cap M)}{P(A)}
$$

$$
P(M \mid A) = \frac{0.42}{0.6} = 0.7
$$

---

## 2. Probability of watching given free account

First compute:

$$
P(A^c) = \frac{80}{200} = 0.4
$$

$$
P(A^c \cap M) = \frac{56}{200} = 0.28
$$

Now:

$$
P(M \mid A^c) = \frac{0.28}{0.4} = 0.7
$$

---

# 📌 Step 4 — Check independence

We test:

## Method 1:

$$
P(A)\cdot P(M) = 0.6 \cdot 0.7 = 0.42
$$

Compare:

$$
P(A \cap M) = 0.42
$$

✔ They are equal.

---

## Method 2:

$$
P(M \mid A) = 0.7
$$

$$
P(M) = 0.7
$$

✔ They are equal.

---

# 📌 Step 5 — Conclusion

✔ Events \(A\) and \(M\) are **independent**.

---

# 🧠 Step 6 — Interpretation in words

Independence means:

> Knowing whether a user has a premium account does NOT change the probability that they watched a movie.

And vice versa:

> Premium users and free users watch movies at the same rate (70%).

---

# 🎯 Final Insight

Even though premium users have more features, in this dataset:

- both groups behave the same in terms of watching movies
- subscription type does not influence viewing behavior

👉 This is a textbook example of **statistical independence in real data**.
