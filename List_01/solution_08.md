# Task 8 — Events and Probabilities in Card Drawing

## Probability Formula

$$
P(A)=\frac{|A|}{|\Omega|}
$$

---

# One Card

Total cards

$$
52
$$

### Heart

$$
P(A_1)=\frac{13}{52}=\frac14
$$

### King

$$
P(B_1)=\frac4{52}=\frac1{13}
$$

### Not Face Card

Face cards = 12

$$
P(C_1)=\frac{40}{52}=\frac{10}{13}
$$

---

# Two Cards With Replacement

Total outcomes

$$
52^2=2704
$$

### Both Hearts

$$
P(A_2)=\left(\frac{13}{52}\right)^2=\frac1{16}
$$

### Same Rank

$$
P(B_2)=\frac{52}{2704}=\frac1{52}
$$

### At Least One Ace

$$
P(C_2)=1-\left(\frac{48}{52}\right)^2
$$

---

# Two Cards Without Replacement

Total outcomes

$$
52\times51
$$

### Both Hearts

$$
P(A_3)=\frac{13}{52}\cdot\frac{12}{51}
$$

### Same Rank

$$
P(B_3)=\frac{13\times4\times3}{52\times51}
$$

### King and Queen

Possible ordered outcomes

$$
4\times4\times2=32
$$

$$
P(C_3)=\frac{32}{52\times51}
$$

---

### Additional Event

Event: **both cards are aces**

$$
P=\frac{4\times3}{52\times51}
$$
