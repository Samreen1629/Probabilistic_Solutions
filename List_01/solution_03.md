# Task 3 — Drawing Cards 

## Useful Definitions and Formulas

**Random Experiment**  
A process that produces an outcome that cannot be predicted with certainty beforehand.

**Sample Space**  
The set of all possible outcomes of a random experiment.

$$
\Omega = \{\text{all possible elementary outcomes}\}
$$

**Elementary Outcome**  
A single possible result of a random experiment.

**Standard Deck of Cards**

A standard deck contains:

- 4 suits: ♠ (spades), ♥ (hearts), ♦ (diamonds), ♣ (clubs)
- 13 ranks: A,2,3,4,5,6,7,8,9,10,J,Q,K

Thus the total number of cards is

$$
52 = 4 \times 13
$$

**Number of Outcomes in Repeated Experiments**

If an experiment with \(n\) possible outcomes is repeated \(k\) times and the **order matters**, then:

With replacement:

$$
n^k
$$

Without replacement:

$$
n(n-1)(n-2)\dots
$$

---

# Step-by-Step Solution

## 1. Sample Space for Drawing One Card

When drawing one card from a standard deck, every card in the deck is a possible outcome.

We represent cards as **(rank, suit)**.

$$
\Omega_1 =
\{(r,s) \mid r \in \{A,2,3,4,5,6,7,8,9,10,J,Q,K\},\;
s \in \{\spadesuit,\heartsuit,\diamondsuit,\clubsuit\}\}
$$

### Number of Elementary Outcomes

$$
|\Omega_1| = 52
$$

---

## 2. Sample Space for Two Draws **With Replacement**

With replacement means the card is returned to the deck before the second draw.  
Therefore both draws again have **52 possible cards**.

Each outcome is an **ordered pair of cards**.

$$
\Omega_2 = \{(c_1,c_2) \mid c_1,c_2 \in \Omega_1\}
$$

Example outcomes include:

- (A♠, K♦)
- (7♥, 7♥)
- (10♣, 3♠)

### Number of Elementary Outcomes

$$
|\Omega_2| = 52^2 = 2704
$$

---

## 3. Sample Space for Two Draws **Without Replacement**

Without replacement means the first drawn card is **not returned** to the deck.

Thus the second draw has **51 possible cards**.

Each outcome is an **ordered pair of distinct cards**.

$$
\Omega_2' = \{(c_1,c_2) \mid c_1,c_2 \in \Omega_1,\; c_1 \ne c_2\}
$$

Example outcomes include:

- (A♠, K♦)
- (7♥, 3♣)
- (10♣, Q♠)

The pair **(A♠, A♠)** is not possible because the card cannot appear twice.

### Number of Elementary Outcomes

$$
|\Omega_2'| = 52 \times 51 = 2652
$$

---

## 4. Number of Elementary Outcomes Summary

| Experiment | Number of Outcomes |
|-------------|-------------------|
| One draw | \(52\) |
| Two draws (with replacement) | \(52^2 = 2704\) |
| Two draws (without replacement) | \(52 \times 51 = 2652\) |

---

## 5. Meaning of an Elementary Outcome

An **elementary outcome** represents a **specific ordered sequence of drawn cards**.

Examples:

- For one draw:  
  \( (A♠) \) means the card drawn is the **Ace of Spades**.

- For two draws with replacement:  
  \( (7♥, 7♥) \) means the **Seven of Hearts was drawn twice**, since the card was replaced.

- For two draws without replacement:  
  \( (K♦, 3♣) \) means the **King of Diamonds was drawn first and the Three of Clubs second**.

Each elementary outcome describes **one exact sequence in which the experiment can occur**.
