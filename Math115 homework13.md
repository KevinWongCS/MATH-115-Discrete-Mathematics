name: kevin wong\
filename: Math115 homework13\
date: 04/27/2022\
desc: https://courses.csail.mit.edu/6.042/spring18/mcs.pdf (Links to an external site.) please do these problems: 10.13, 10.57, 3, 4, 5.

---
---
### 10.13
Chickens are rather aggressive birds that tend to establish dominance over other
chickens by pecking them—hence the term “pecking order.” So for any two chick-
ens in a farmyard, either the first pecks the second, or the second pecks the first, but
not both. We say that chicken $u$ virtually pecks chicken $v$ if either:

- Chicken $u$ pecks chicken $v$, or
- Chicken $u$ pecks some other chicken $w$ who in turn pecks chicken $v$. 

A chicken that virtually pecks every other chicken is called a *king chicken*.

We can model this situation with a chicken digraph whose vertices are chickens,
with an edge from chicken $u$ to chicken $v$ precisely when $u$ pecks $v$. **In the graph in Figure 10.11, three of the four chickens are kings. Chicken $c$ is not a king in this example since it does not peck chicken $b$ and it does not peck any chicken that pecks chicken $b$. Chicken $a$ is a king since it pecks chicken $d$ , who in turn pecks chickens $b$ and $c$.**

In general, a *tournament digraph* is a digraph with exactly one edge between each pair of distinct vertices.

![](https://i.imgur.com/F6ywU5K.png)

- a) Define a 10-chicken tournament graph with a king chicken that has outdegree 1.
    
    In the graph below all the edges between pairs not used in this problem were omitted to demonstrate a 1 outdegree king-chicken. So chicken $a$ is a king by only pecking an adjacent chicken $b$ and $b$ in turn pecks every other chicken $c, d, e, f, g, h, i$ and $j$. So as long as the digraph has outdegrees equivalent to $\{(a, b), (b,c), (b, d), (b, e), (b, f), (b, g), (b, h), (b, i), (b, j)\}$, this 1 outdegree king-chicken will exist.
    
![](https://i.imgur.com/4NOUWEj.png)

- b) Describe a 5-chicken tournament graph in which every player is a king.

    In the 5-chicken tournament graph below every chicken is king because every chicken pecks every other chicken either directly adjacent or indirectly via pecking an adjacent chicken that pecks the remaining chicken.

![](https://i.imgur.com/bBfvv6q.png)

| chicken | a       | b       | c       | d       | e       |
|---------|---------|---------|---------|---------|---------|
|         | a, b    | b, d, a | c, e, a | d, a    | e, a    |
|         | a, c    | b, c    | c, e, b | d, a, b | e, b    |
|         | a, c, d | b, d    | c, d    | d, a ,c | e, b, c |
|         | a, c, e | b, d, e | c, e    | d, e    | e, b, d |

- c) Prove

    **Theorem** (King Chicken Theorem). Any chicken with maximum out-degree in a
tournament is a king.

    The King Chicken Theorem means that if the player with the most victories is
    defeated by another player x, then at least he/she defeats some third player that defeats x. In this sense, the player with the most victories has some sort of bragging rights over every other player. Unfortunately, as Figure 10.11 illustrates, there can be many other players with such bragging rights, even some with fewer victories.

    - This is true. If there are $n$ chickens and and there exist a chicken $a$ that has the maximum out-degree of $n - 1$. Then $a$ is a exclusive or the only king-chicken because no other chicken can have an edge pointing back at chicken $a$. $\checkmark$

--- 
---

### 10.57

Prove Theorem 10.10.4: The equivalence classes of an equivalence relation form a
partition of the domain.

Namely, let $R$ be an equivalence relation on a set $A$ and define the equivalence
class of an element $a \in A$ to be

$[a]_R ::= \{b \in A |$ $a$ $R$ $b\}$

That is, $[a]_R = R(a)$

- a) Prove that every block is nonempty and every element of A is in some block.
- b) Prove that if $ [a]_R \cap [b]_R \neq \emptyset $, then $a$ $R$ $b$. Conclude that the sets [a]_R for $a \in A$ are a partition of $A$.
- c) Prove that $a$ $R$ $b$ iff $[a]_R = [b]_R$.


- Theorem 10.10.4

![](https://i.imgur.com/YZEu2Mv.png)

---
---
### 3
![](https://i.imgur.com/RULadVP.png)

- a) $\forall x \in A$, $(x, x) \in R$ 
    
    Student x and student x are both students at CCSF, and the same student has obviously attended the same class, so reflexive. $\checkmark$

    $\forall x, y \in A$, $(x, y) \in R \rightarrow (y,x) \in R$

    $\forall x, y ,z \in A$ $(x,y) \in R \wedge (y,z) \in R \rightarrow (x,z) \in R$

- b) $\forall s \in A$, $(s, s) \in R$ 

    Bit string $s$ and $s$ are both bit strings of length ten. Since they are the same bit string they both also begin and end with the same bit, so reflexive. $\checkmark$

    $\forall s_1, s_2 \in A$, $(s_1, s_2) \in R \rightarrow (s_2,s_1) \in R$

    If two bit strings are of length ten and bit string $s_1$ begins or ends with the same bit as $s_2$, then $s_2$ would also begin or end with the same bit as $s_1$. This is valid, so symmetric.

    $\forall x, y ,z \in A$ $(x,y) \in R \wedge (y,z) \in R \rightarrow (x,z) \in R$

- c) $\forall x \in A$, $(x, x) \in R$ 

    $\forall x, y \in A$, $(x, y) \in R \rightarrow (y,x) \in R$

    $\forall x, y ,z \in A$ $(x,y) \in R \wedge (y,z) \in R \rightarrow (x,z) \in R$

---
---

*END*

---
---