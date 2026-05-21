# Problem 1 — Event Algebra from a Two-Way Table

## Useful Definitions and Formulas

### Probability of an event

$$
P(A)=\frac{\text{number of favorable outcomes}}{\text{total number of outcomes}}
$$

### Complement of an event

$$
P(A^c)=1-P(A)
$$

### Union of two events

$$
P(A\cup B)=P(A)+P(B)-P(A\cap B)
$$

### Conditional probability

$$
P(A\mid B)=\frac{P(A\cap B)}{P(B)}
$$

### Independence

Events \(A\) and \(B\) are independent if

$$
P(A\cap B)=P(A)P(B)
$$

### Mutually exclusive events

Events are mutually exclusive if

$$
A\cap B=\varnothing
$$

which means they cannot happen together.

---

# Step 1 — Probabilities of the four disjoint regions

Total number of students:

$$
100
$$

## Region 1: $$\(A\cap B\)$$

Students who attend regularly and submit on time:

$$
P(A\cap B)=\frac{48}{100}=0.48
$$

## Region 2: $$\(A\cap B^c\)$$

Students who attend regularly and do not submit on time:

$$
P(A\cap B^c)=\frac{12}{100}=0.12
$$

## Region 3: $$\(A^c\cap B\)$$

Students who do not attend regularly and submit on time:

$$
P(A^c\cap B)=\frac{22}{100}=0.22
$$

## Region 4: $$\(A^c\cap B^c\)$$

Students who do not attend regularly and do not submit on time:

$$
P(A^c\cap B^c)=\frac{18}{100}=0.18
$$

---

# Step 2 — Compute $$\(P(A)\)$$, $$\(P(B)\)$$, and $$\(P(A\cup B)\)$$

## Probability of attending lectures regularly

$$
P(A)=\frac{60}{100}=0.60
$$

## Probability of submitting homework on time

$$
P(B)=\frac{70}{100}=0.70
$$

## Probability of $$\(A\cup B\)$$

Using inclusion–exclusion:

$$
P(A\cup B)=P(A)+P(B)-P(A\cap B)
$$

Substitute the values:

$$
P(A\cup B)=0.60+0.70-0.48
$$

$$
P(A\cup B)=0.82
$$

---

# Step 3 — Conditional probabilities

## Compute $$\(P(A\mid B)\)$$

Using the conditional probability formula:

$$
P(A\mid B)=\frac{P(A\cap B)}{P(B)}
$$

Substitute the values:

$$
P(A\mid B)=\frac{0.48}{0.70}
$$

$$
P(A\mid B)\approx0.686
$$

## Compute $$\(P(B\mid A)\)$$

$$
P(B\mid A)=\frac{P(A\cap B)}{P(A)}
$$

Substitute the values:

$$
P(B\mid A)=\frac{0.48}{0.60}
$$

$$
P(B\mid A)=0.80
$$

---

# Step 4 — Are $$\(A\)$$ and $$\(B\)$$ mutually exclusive?

No.

The events are not mutually exclusive because:

$$
P(A\cap B)=0.48>0
$$

This means both events can occur together.

---

# Step 5 — Are $$\(A\)$$ and $$\(B\)$$ independent?

Check whether:

$$
P(A\cap B)=P(A)P(B)
$$

Compute:

$$
P(A)P(B)=0.60\times0.70=0.42
$$

But:

$$
P(A\cap B)=0.48
$$

Since:

$$
0.48\ne0.42
$$

the events are **not independent**.

---

# Step 6 — Interpretation

## Interpretation of $$\(P(A\mid B)\)$$

$$
P(A\mid B)\approx0.686
$$

This means:

> Among students who submit homework on time, about 68.6% attend lectures regularly.

## Interpretation of $$\(P(B\mid A)\)$$

$$
P(B\mid A)=0.80
$$

This means:

> Among students who attend lectures regularly, 80% submit homework on time.
