## Problem 1 — Coin × Coin

### Description of the experiment

We consider an experiment consisting of **two successive coin tosses**.  
Each toss has two possible outcomes:

- H — head  
- T — tail  

An elementary outcome is an **ordered pair**:
- first toss result,
- second toss result.

Thus, the sample space is:

$$
\Omega = \{HH, HT, TH, TT\}
$$

Representation:
  H   T
  
H HH HT

T TH TT

Each cell corresponds to one elementary outcome.

---

### Part A — Marking events

We translate each verbal statement into a **set of outcomes**.


---

#### 1. Exactly one head

We need outcomes where:
- one toss is H,
- the other is T.

Thus:

$$
A = \{HT, TH\}
$$

  
---

#### 2. Both tosses are the same

Possible outcomes:

$$
B = \{HH, TT\}
$$

  
---

#### 3. At least one head

This includes all outcomes except TT:

$$
C = \{HH, HT, TH\}
$$

  
---

#### 4. The first toss is tails

We take all outcomes where the first coordinate is T:

$$
D = \{TH, TT\}
$$

  
---

#### 5. The second toss is heads

We take all outcomes where the second coordinate is H:

$$
E = \{HH, TH\}
$$

  
---

### Part B — Interpretation

---

#### Case 1
  
All marked outcomes lie in the first row.

This means:

> the **first toss is heads**, regardless of the second toss.

---

#### Case 2
  
This corresponds to:

$$
\{HT, TH\}
$$

Interpretation:

> the two tosses give **different results**, i.e. exactly one head occurs.
