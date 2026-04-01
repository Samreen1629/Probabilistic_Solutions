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

Graphical representation:

       H    T
    H  HH   HT
    T  TH   TT

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

        H   T
    H   .   X
    T   X   .
---

#### 2. Both tosses are the same

Possible outcomes:

$$
B = \{HH, TT\}
$$

        H   T
    H   X   .
    T   .   X
---

#### 3. At least one head

This includes all outcomes except TT:

$$
C = \{HH, HT, TH\}
$$

        H   T
    H   X   X
    T   X   .
  
---

#### 4. The first toss is tails

We take all outcomes where the first coordinate is T:

$$
D = \{TH, TT\}
$$

        H   T
    H   .   .
    T   X   X
  
---

#### 5. The second toss is heads

We take all outcomes where the second coordinate is H:

$$
E = \{HH, TH\}
$$

        H   T
    H   X   .
    T   X   . 
---

### Part B — Interpretation

---

#### Case 1

        H   T
    H   X   X
    T   .   . 
    
All marked outcomes lie in the first row.

This means:

> the **first toss is heads**, regardless of the second toss.

---

#### Case 2

        H   T
    H   .   X
    T   X   .  
    
This corresponds to:

$$
\{HT, TH\}
$$

Interpretation:

> the two tosses give **different results**, i.e. exactly one head occurs.
