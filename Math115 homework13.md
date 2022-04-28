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
    defeated by another player x, then at least he/she defeats some third player that
    defeats x. In this sense, the player with the most victories has some sort of bragging
    rights over every other player. Unfortunately, as Figure 10.11 illustrates, there can
    be many other players with such bragging rights, even some with fewer victories.

--- 
---


---
---

*END*

---
---