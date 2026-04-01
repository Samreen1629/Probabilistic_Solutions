## Task 5 — Multinomial Model

### Random Experiment
Roll a die 5 times and classify outcomes:
- Small (1–2)
- Medium (3–4)
- Large (5–6)

---

### Sample Space
All sequences of 5 categorized outcomes.

---

### Distribution

$$
P(X_1 = k_1, X_2 = k_2, X_3 = k_3)
= \frac{5!}{k_1!k_2!k_3!}
\left(\frac{1}{3}\right)^{k_1}
\left(\frac{1}{3}\right)^{k_2}
\left(\frac{1}{3}\right)^{k_3}
$$

---

### Parameters Interpretation

- $n = 5$ trials  
- $p_1 = p_2 = p_3 = \frac{1}{3}$  
- $k_1 + k_2 + k_3 = 5$
