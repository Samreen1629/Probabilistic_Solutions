## Problem 6 — Dependence from data

# 🌟 Key Definitions and Formulas

## 1. Probability of an event

$$
P(A) = \frac{\text{number of favorable outcomes}}{\text{total outcomes}}
$$

---

## 2. Intersection

$$A \cap B$$

means both events occur together.

---

## 3. Conditional probability

$$
P(D \mid I) = \frac{P(D \cap I)}{P(I)}
$$

---

## 4. Independence condition

$$
P(I \cap D) = P(I)\cdot P(D)
$$

or equivalently:

$$
P(D \mid I) = P(D)
$$

---

# 📊 Step 1 — Understand the data

Total parcels = **600**

| Parcel type | Delayed (D) | Not delayed | Total |
|-------------|------------|-------------|-------|
| Domestic $$(I^c)$$ | 24 | 376 | 400 |
| International (I) | 36 | 164 | 200 |
| Total | 60 | 540 | 600 |

---

# 📌 Step 2 — Compute basic probabilities

## 1. Probability parcel is international

$$
P(I) = \frac{200}{600} = \frac{1}{3} \approx 0.3333
$$

---

## 2. Probability parcel is delayed

$$
P(D) = \frac{60}{600} = 0.1
$$

---

## 3. Probability of both international and delayed

$$
P(I \cap D) = \frac{36}{600} = 0.06
$$

---

# 📌 Step 3 — Conditional probabilities

## 1. Probability delayed given international

$$
P(D \mid I) = \frac{P(I \cap D)}{P(I)}
$$

$$
P(D \mid I) = \frac{0.06}{0.3333} \approx 0.18
$$

---

## 2. Probability delayed given domestic

First compute:

$$
P(I^c) = \frac{400}{600} = 0.6667
$$

$$
P(I^c \cap D) = \frac{24}{600} = 0.04
$$

Now:

$$
P(D \mid I^c) = \frac{0.04}{0.6667} \approx 0.06
$$

---

# 📌 Step 4 — Check independence

We compare:

## Method 1: product test

$$
P(I)\cdot P(D) = 0.3333 \cdot 0.1 = 0.03333
$$

But:

$$
P(I \cap D) = 0.06
$$

❌ Not equal → not independent

---

## Method 2: conditional test

$$
P(D \mid I) = 0.18
$$

$$
P(D) = 0.1
$$

❌ Not equal → not independent

---

# 📌 Step 5 — Does international shipping increase delay probability?

Compare:

$$
P(D \mid I) = 0.18
$$

$$
P(D \mid I^c) = 0.06
$$

✔ Yes — international parcels are **3× more likely to be delayed**.

---

# 📌 Step 6 — Compute $$\(P(I \mid D)\)$$

$$
P(I \mid D) = \frac{P(I \cap D)}{P(D)}
$$

$$
P(I \mid D) = \frac{0.06}{0.1} = 0.6
$$

---

# 📌 Step 7 — Interpretation of $$\(P(I \mid D)\)$$

> Among delayed parcels, 60% are international.

---

# 📌 Step 8 — Difference between $$\(P(D \mid I)\)$$ and $$\(P(I \mid D)\)$$

## 1. $$\(P(D \mid I)\)$$

$$
P(D \mid I) = 0.18
$$

👉 “If a parcel is international, how likely is it to be delayed?”

- Focus: **risk of delay given type**

---

## 2. $$\(P(I \mid D)\)$$

$$
P(I \mid D) = 0.6
$$

👉 “If a parcel is delayed, how likely is it international?”

- Focus: **composition of delayed parcels**

---

# ⚠️ Key insight

Even though they use the same data:

- They normalize by different totals
- So they answer completely different questions

---

# 🎯 Final Conclusion

- International shipping increases delay probability significantly:
  - 18% vs 6%
- Events \(I\) and \(D\) are **not independent**
- Conditional probability direction matters:
  - $$\(P(D \mid I)\)$$ = risk
  - $$\(P(I \mid D)\)$$ = diagnosis of delayed group structure
