# Task 1 — Coin Tossing 

## Useful Definitions and Formulas

**Random Experiment**  
A process that produces an outcome that cannot be predicted with certainty in advance.

**Sample Space**  
The set of all possible outcomes of a random experiment.

$$
\Omega = \{ \text{all possible elementary outcomes} \}
$$

**Elementary Outcome**  
A single possible result of the experiment.

**Number of Outcomes for Coin Tosses**

If a fair coin is tossed \(n\) times, each toss has 2 possible outcomes:  
- \(H\) — Heads  
- \(T\) — Tails  

The total number of possible outcomes is

$$
|\Omega_n| = 2^n
$$

where \(n\) is the number of coin tosses.

The **order of outcomes matters**, meaning sequences like \(HT\) and \(TH\) are considered different.

---

# Step-by-Step Solution

## 1. Sample Space for One Coin Toss

A single coin toss can produce either **Heads (H)** or **Tails (T)**.

Therefore the sample space is

$$
\Omega_1 = \{H, T\}
$$

### Number of Elementary Outcomes

$$
|\Omega_1| = 2
$$

---

## 2. Sample Space for Two Coin Tosses

Each toss can result in \(H\) or \(T\), and the order matters.  
We list all possible ordered pairs:

$$
\Omega_2 = \{HH, HT, TH, TT\}
$$

### Number of Elementary Outcomes

$$
|\Omega_2| = 2^2 = 4
$$

---

## 3. Sample Space for Three Coin Tosses

Now we list all ordered triples of \(H\) and \(T\):

$$
\Omega_3 =
\{HHH, HHT, HTH, HTT, THH, THT, TTH, TTT\}
$$

### Number of Elementary Outcomes

$$
|\Omega_3| = 2^3 = 8
$$

---

## 4. Number of Elementary Outcomes Summary

| Number of Tosses | Sample Space Size |
|------------------|------------------|
| 1 | $$2^1 = 2$$ |
| 2 | $$2^2 = 4$$ |
| 3 | $$2^3 = 8$$ |

---

## 5. Meaning of an Elementary Outcome

An **elementary outcome** represents a **single complete sequence of results** from the experiment.

Examples:

- For one toss:  
  - \(H\) means the coin lands **Heads**.
  - \(T\) means the coin lands **Tails**.

- For two tosses:  
  - \(HT\) means **Heads on the first toss and Tails on the second**.

- For three tosses:  
  - \(THT\) means **Tails on the first toss, Heads on the second, Tails on the third**.

Each sequence represents **one possible way the experiment can occur**.
