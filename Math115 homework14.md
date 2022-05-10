name: kevin wong\
filename: Math115 homework14\
date: 05/05/2022\
desc: https://courses.csail.mit.edu/6.042/spring18/mcs.pdf (Links to an external site.) please do these problems: 15.2 15.4, 15.5, 15.12, additional problem


---
---

### 15.2 

In how many different ways is it possible to answer the next chapter’s practice problems if:

- the first problem has four *true/false* questions,

    First problem: $2 * 2 * 2 * 2 = 16$ different ways.

- the second problem requires choosing one of four alternatives, and

    Second problem: $4$ different ways.

- the answer to the third problem is an $integer \ge 15$ and $\le 20$?

    Third problem: $15, 16, 17, 18, 19, 20$ results in $6$ different ways.

- This results in $16 * 4 * 6 = 384$ different ways to answer the next chapter’s practice problems via rule of product.

---
---

### 15.4

Let $X$ be the six element set $\{x_1, x_2, x_3, x_4, x_5, x_6\}$.

- a) How many subsets of $X$ contain $x_1$?
 
    Subsets of $X$ containing $x_1$: $1 * 2 * 2 * 2 * 2 * 2 = 2^5 = 32$ ways.


- b) How many subsets of $X$ contain $x_2$ and $x_3$ but do not contain $x_6$?

    Subsets of $X$ containing $x_2$ and $x_3$ but do not containing $x_6$: $(1 * 1 * 2 * 2 * 2 * 2) - (1 * 1 * 2 * 2 * 2) = 2^4 - 2^3 = 8$ ways.

---
---

### 15.5

A license plate consists of either:

- 3 letters followed by 3 digits(standard plate)

    combinations: $26 * 26 * 26 * 10 * 10 * 10 = 17576000$ .

- 5 letter (vanity plate)

    combinations: $26 * 26 * 26 * 26 * 26 = 11881376$.

- 2 characters-letters or numbers (big shot plate)

    case 1: 2 characters-letters: $26 * 26 = 676$ combinations.

    case 2: 2 numbers: $10 * 10 = 100$ combinations.

    case 3: 1 character-letter and 1 number: $26 * 10 = 260$ combinations.

    case 4: 1 number and 1 character-letter: $10 * 26 = 260$ combinations.

    Total combinations for 2 characters-letters or numbers: $676 + 100 + 260 + 260 = 1296$.

Let $L$ be the set of all possible license plates.

- a) Express $L$ in terms of 

    $\mathcal{A} = \{A, B, C,...,Z\}$

    $\mathcal{D} = \{0, 1, 2,...,9\}$

    using unions $(\cup)$ and set products $(\times)$.

    - $L = (\mathcal{A}^3 \times \mathcal{D}^3) \cup (\mathcal{A}^5)\cup ((\mathcal{A}^2) \cup (\mathcal{D}^2) \cup (\mathcal{A} \times \mathcal{D}) \cup (\mathcal{D} \times \mathcal{A}))$

- b) Compute $|L|$, the number of different license plates, using the sum and product rules.

    - The total number of combinations for different license plates is $17576000 + 11881376 + 1296 = 29458672$.
    - or $|L| = 29458672$

---
---

### 15.12

Eight students—Anna, Brian, Caine,. . . —are to be seated around a circular table in a circular room. Two seatings are regarded as defining the same *arrangement* if each student has the same student on his or her right in both seatings: it does not matter which way they face. We’ll be interested in counting how many arrangements there are of these 8 students, given some restrictions.

- a) As a start, how many different arrangements of these 8 students around the table are there without any restrictions?
 
     Each arrangement has 8 equivalent arrangements because of the circular table. No restrictions combinations: $8!/8 =  7! = 5040$ ways with unique arrangements.

- b) How many arrangements of these 8 students are there with Anna sitting next to Brian?

    There are $(1 * 2 * 6!) / 8 = 180$ ways.

- c) How many arrangements are there with if Brian sitting next to both Anna AND Caine?

    There are $(1 * 2 * 1 * 5!) / 8 = 30$ ways.

- d) How many arrangements are there with Brian sitting next to Anna OR Caine?

    combinations with Brian sitting next to Anna OR Caine: $180 + 180 - 30 = 330$ ways.

---
---

### 5

Students A, B, C, D, E, F, G are running a footrace.

One possible outcome to the race is (G, D, F, A, E, D, C).

Compute the probability that...

- a. A comes in first.

    Let $E$ be the event that A comes in first.

    $P(E) = \frac{6!}{7!} = 0.14$

- b. A or B come in first.

    Let $E_1$ be the event that A comes in first and $E_2$ be the event that B comes in first.

    $P(E_1 \cup E_2) = \frac{(1 * 6! + 1 * 6!)}{7!} = 0.28$

- c. A comes in first or last.
    
    Let $E_1$ be the event that A comes in first and $E_2$ be the event that A comes in last.

    $P(E_1 \cup E_2) = \frac{1 * 6! + 6! * 1}{7!} = 0.28$

- d. A comes in first or B comes in last.
    
    Let $E_1$ be the event that A comes in first and $E_2$ be the event that B comes in last.

    $P(E_1 \cup E_2) = \frac{((1 * 6!) + (1 * 6!) - (1 * 5! * 1))}{7!} = 0.26$

- e. A doesn't finish in the top four.

    Let $E$ be the event that A doesn't finish in the top four.

    $P(E) = \frac{(6! * 1) * 3}{7!} = 0.42$

- f. A finishes before B.

    Let $E$ be the event that A finishes before B.
    
    Case A is 1st: $6!$ outcomes have B after.

    Case A is 2nd: $5 * 5!$ outcomes have B after.

    Case A is 3rd: $4 * 5!$ outcomes have B after.

    Case A is 4th: $3 * 5!$ outcomes have B after.

    Case A is 5th: $2 * 5!$ outcomes have B after.

    Case A is 6th: $1 * 5!$ outcomes have B after.

    Case A is 7th: $0 * 5!$ outcomes have B after.
    
    $P(E) = \frac{5!(6 + 5 + 4 + 3 + 2 + 1)}{7!} = 0.50$

- g. A finishes before B, given that B is not last.

    Case A is 1st: $6!$ outcomes have B after.
    Case A is 2nd: $5 * 5!$ outcomes have B after.

    Case A is 3rd: $4 * 5!$ outcomes have B after.

    Case A is 4th: $3 * 5!$ outcomes have B after.

    Case A is 5th: $2 * 5!$ outcomes have B after.

    Case A is 6th: $0 * 5!$ outcomes have B after.

    Case A is 7th: $0 * 5!$ outcomes have B after.

    $P(E) = \frac{5!(5 + 4 + 3 + 2 + 1)}{7!} = 0.35$

---
---


*END*

---
---