# Task 10 — Buffon's Needle Probabilities

Needle length \(L\), line distance \(d\).

Variables

- \(X\in[0,d/2]\)
- \(\theta\in[0,\pi/2]\)

Both uniform.

---

## Intersection Condition

Needle intersects a line if

$$
X\le \frac{L}{2}\sin\theta
$$

---

## Event A — Needle Intersects a Line

Classical Buffon result

$$
P(A)=\frac{2L}{\pi d}
$$

---

## Event B — No Intersection

$$
P(B)=1-\frac{2L}{\pi d}
$$

---

## Event C — Angle < π/6

Since θ uniform

$$
P(C)=\frac{\pi/6}{\pi/2}=\frac13
$$

---

## Event D — Distance < d/4

$$
P(D)=\frac{d/4}{d/2}=\frac12
$$

---

## Event E — Intersection and Angle > π/4

Approximate probability

$$
P(E)=\int_{\pi/4}^{\pi/2}\frac{2L}{\pi d}\sin\theta\,d\theta
$$

---

## Additional Event

Event: **angle greater than π/3**

$$
P=\frac{\pi/2-\pi/3}{\pi/2}=\frac13
$$
