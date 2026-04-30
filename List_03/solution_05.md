## Task 5 — Multinomial Model

---

## 🔹 Random Experiment

We roll a fair die **5 times**.

Each outcome is grouped into categories:
- **Small (S):** 1 or 2  
- **Medium (M):** 3 or 4  
- **Large (L):** 5 or 6  

So instead of tracking exact numbers, we track **categories**.

---

## 🎯 Key Idea

Each roll has **3 possible categories**, and we repeat the experiment 5 times.

This makes it a **Multinomial Experiment**, which is a generalization of the binomial distribution (more than 2 outcomes).

---

## 🔸 Sample Space

The sample space consists of **all possible sequences of 5 outcomes**, where each outcome is:

\[
\{S, M, L\}
\]

Example outcomes:
- (S, S, M, L, M)
- (L, L, S, M, S)
- (M, M, M, S, L)

Instead of listing all sequences, we summarize results using **counts**:
- \( X_1 \): number of Small outcomes  
- \( X_2 \): number of Medium outcomes  
- \( X_3 \): number of Large outcomes  

---

## 📌 Probabilities of Each Category

Since the die is fair:

- \( P(S) = \frac{2}{6} = \frac{1}{3} \)
- \( P(M) = \frac{2}{6} = \frac{1}{3} \)
- \( P(L) = \frac{2}{6} = \frac{1}{3} \)

All categories are **equally likely**.

---

## 🔸 Multinomial Distribution Formula

The probability of getting:
- \( k_1 \) Small  
- \( k_2 \) Medium  
- \( k_3 \) Large  

(where \( k_1 + k_2 + k_3 = 5 \)) is:

$$
P(X_1 = k_1, X_2 = k_2, X_3 = k_3)
= \frac{5!}{k_1! \, k_2! \, k_3!}
\left(\frac{1}{3}\right)^{k_1}
\left(\frac{1}{3}\right)^{k_2}
\left(\frac{1}{3}\right)^{k_3}
$$

---

## 🧠 Understanding the Formula

### 1. The factorial term:

$$
\[
\frac{5!}{k_1!k_2!k_3!}
\]
$$

This counts how many **different sequences** produce the same counts.

Example:  
If \( k_1 = 2, k_2 = 2, k_3 = 1 \), this tells us how many ways we can arrange:
- 2 S’s  
- 2 M’s  
- 1 L  

---

### 2. The probability terms:

$$
\[
\left(\frac{1}{3}\right)^{k_1}
\left(\frac{1}{3}\right)^{k_2}
\left(\frac{1}{3}\right)^{k_3}
\]
$$

These represent the probability of each category occurring the required number of times.

Since all probabilities are equal, this simplifies to:

$$
\[
\left(\frac{1}{3}\right)^5
\]
$$

---

## 🔸 Example Calculation

Suppose:
- \( k_1 = 2 \) (Small)
- \( k_2 = 2 \) (Medium)
- \( k_3 = 1 \) (Large)

### Step 1: Count arrangements

$$
\[
\frac{5!}{2!2!1!} = \frac{120}{4} = 30
\]
$$

### Step 2: Compute probability

$$
\[
P = 30 \times \left(\frac{1}{3}\right)^5
\]
$$

$$
\[
= 30 \times \frac{1}{243}
= \frac{30}{243}
\approx 0.1235
\]
$$

---

## 🔸 Parameters Interpretation

- \( n = 5 \): total number of trials  
- \( p_1 = p_2 = p_3 = \frac{1}{3} \): probability of each category  
- \( k_1, k_2, k_3 \): counts of each category  
- Constraint:
  \[
  k_1 + k_2 + k_3 = 5
  \]

---

## 🧠 Key Insights

- This is a **multinomial distribution** because:
  - More than 2 outcomes per trial  
  - Fixed number of trials  
  - Constant probabilities  

- When all probabilities are equal:
  - The distribution is **symmetric**

- The factorial term handles **combinatorics (arrangements)**  
- The power terms handle **probability of each outcome**

---

## 🚀 Quick Summary

- Replace outcomes with categories  
- Count how many times each category occurs  
- Use multinomial formula to compute probability  
- Always check:
  \[
  k_1 + k_2 + k_3 = n
  \]
