# Task 2 — Rolling a Die 

## Useful Definitions and Formulas

**Random Experiment**  
A process that produces an outcome that cannot be predicted with certainty before it occurs.

**Sample Space**  
The set of all possible outcomes of a random experiment.

$$
\Omega = \{\text{all possible elementary outcomes}\}
$$

**Elementary Outcome**  
A single possible result of a random experiment.

**Fair Six-Sided Die**  
A die with six faces numbered from 1 to 6, where each outcome has the same probability.

**Number of Outcomes in Repeated Experiments**

If an experiment with \(k\) possible outcomes is repeated \(n\) times and the **order matters**, the number of elementary outcomes is

$$
|\Omega_n| = k^n
$$

For a six-sided die:

$$
k = 6
$$

Thus,

$$
|\Omega_n| = 6^n
$$

---

# Step-by-Step Solution

## 1. Sample Space for One Roll of a Die

When rolling a fair six-sided die once, the possible outcomes are the numbers on the die.

$$
\Omega_1 = \{1,2,3,4,5,6\}
$$

### Number of Elementary Outcomes

$$
|\Omega_1| = 6
$$

---

## 2. Sample Space for Two Consecutive Rolls

Each roll can produce any number from 1 to 6.  
Since the **order matters**, outcomes are represented as ordered pairs.

$$
\Omega_2 =
$$

{  (1,1), (1,2), (1,3), (1,4), (1,5), (1,6),  

(2,1), (2,2), (2,3), (2,4), (2,5), (2,6),  

(3,1), (3,2), (3,3), (3,4), (3,5), (3,6),  

(4,1), (4,2), (4,3), (4,4), (4,5), (4,6),  

(5,1), (5,2), (5,3), (5,4), (5,5), (5,6),  

(6,1), (6,2), (6,3), (6,4), (6,5), (6,6)  }

### Number of Elementary Outcomes

$$
|\Omega_2| = 6^2 = 36
$$

---

## 3. Sample Space for Three Consecutive Rolls

For three rolls, outcomes are ordered triples.

$$
\Omega_3 = \{(i,j,k) \mid i,j,k \in \{1,2,3,4,5,6\}\}
$$

### Number of Elementary Outcomes

$$
|\Omega_3| = 6^3 = 216
$$

---

## 4. Number of Elementary Outcomes Summary

| Number of Rolls | Number of Outcomes |
|-----------------|-------------------|
| 1 | \(6^1 = 6\) |
| 2 | \(6^2 = 36\) |
| 3 | \(6^3 = 216\) |

---

## 5. Meaning of an Elementary Outcome

An **elementary outcome** represents one **specific sequence of die results**.

Examples:

- For one roll: \(4\) means the die shows **4**.
- For two rolls: \((2,5)\) means the **first roll is 2 and the second roll is 5**.
- For three rolls: \((6,1,3)\) means the **first roll is 6, the second roll is 1, and the third roll is 3**.

Each elementary outcome describes **one exact way the experiment can occur**.
