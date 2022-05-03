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
with an edge from chicken $u$ to chicken $v$ precisely when $u$ pecks $v$. *In the graph in Figure 10.11, three of the four chickens are kings. Chicken $c$ is not a king in this example since it does not peck chicken $b$ and it does not peck any chicken that pecks chicken $b$. Chicken $a$ is a king since it pecks chicken $d$ , who in turn pecks chickens $b$ and $c$.*

In general, a *tournament digraph* is a digraph with exactly one edge between each pair of distinct vertices.

![](https://i.imgur.com/F6ywU5K.png)

- a) Define a 10-chicken tournament graph with a king chicken that has outdegree 1.
    
    In the graph below all the edges between pairs not used in this problem were omitted to demonstrate a 1 outdegree king-chicken. So chicken $a$ is a king by only pecking an adjacent chicken $b$ and $b$ in turn pecks every other chicken $c, d, e, f, g, h, i$ and $j$. So as long as a chicken in the digraph has outdegrees analogous to $\{(a, b), (b,c), (b, d), (b, e), (b, f), (b, g), (b, h), (b, i), (b, j)\}$, this 1 outdegree king-chicken will exist.
    
![](https://i.imgur.com/4NOUWEj.png)

- b) Describe a 5-chicken tournament graph in which every player is a king.

    In the 5-chicken tournament graph below every chicken is king because every chicken pecks every other chicken either directly adjacent or indirectly via pecking an adjacent chicken that pecks the remaining chicken(s).

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

    - This is true. If there are $n$ chickens and and there exist a chicken $a$ that has the maximum out-degree of $n - 1$. Then chicken $a$ is a exclusive or the only king-chicken because no other chicken can have an edge directed back at chicken $a$. $\checkmark$

--- 
---

### 10.57

Prove Theorem 10.10.4: The equivalence classes of an equivalence relation form a partition of the domain.

Namely, let $R$ be an *equivalence relation($R$)* on a set $A$ and *define the equivalence class of an element* $a \in A$ to be

$[a]_R ::= \{b \in A |$ $a$ $R$ $b\}$

That is, $[a]_R = R(a)$

```
Visual of the problem

    similar to a file system

    Assume "set A" contains {a, b, c, d,...}

    domain("set A")
        |
        |-- equivalence class a ([a]_R)
        |        |
        |        |-- [a]_R = {a, d}
        |        so this means "a" and "d" have an equivalence relation.
        |
        |-- equivalence class b ([b]_R)
        |        |
        |        |-- [b]_R = {b}
        |        so this means "b" only has an equivalence relation with itself.
        |
        |-- equivalence class c ([c]_R)
        |        |
        |        |-- [c]_R = {c}
        |
        |-- equivalence class d ([d]_R)
        |        |
        |        |-- [d]_R) = {d, a}
        |
        |-- etc...
        |
        |
    
The equivalence classes (or partitions or blocks) are formed based on equivalence relations of the elements in "set A".

So every equivalence class is a subset of the domain or "set A".
        
```

- a) Prove that every block is nonempty and every element of A is in some block.

    Assuming $A \ne \emptyset$. For an element $b \in A$, $b$ is reflexive, symmetric and transitive to itself or an equivalence relation. So at minimal $b$ is in a equivalence class by itself, $[b]_R$ containing itself $b$. $\checkmark$
    
    - equivalence relation
        
        Reflexive: $\forall b \in A$, $(b, b) \in R$

        Symmetric: $\forall b, b \in A$, $(b, b) \in R \rightarrow (b,b) \in R$

        Transitive: $\forall b, b , b \in A$ $(b,b) \in R \wedge (b,b) \in R \rightarrow (b,b) \in R$

        so,

        The equivalence class: $[b]_R ::= \{b \in A |$ $b$ $R$ $b\}$ 

        and 

        The equivalence class contains: $[b]_R = \{b\}$
        - Also depicted in the visual above.

- b) Prove that if $ [a]_R \cap [b]_R \neq \emptyset $, then $a$ $R$ $b$. Conclude that the sets $[a]_R$ for $a \in A$ are a partition of $A$.

    If $ [a]_R \cap [b]_R = \emptyset $ then there does not exist a equivalence relation $\forall a \in [a]_R$ and $\forall b \in [b]_R$.

    - Case 1: $ [a]_R \cap [b]_R \neq \emptyset $ implies there does exist elements $a \in [a]_R$ and $b \in [b]_R$ that have equivalence relations. $\checkmark$

    ![](https://i.imgur.com/7hJlrzF.png)

    - Case 2: $[a]_R \cap [b]_R = [a]_R = [b]_R$. For this to occur $\forall a \in [a]_R$ and $\forall b \in [b]_R$ have to form equivalence relations.
    
    ![](https://i.imgur.com/iHPFSme.png)

    - Case 3: I guess I can also consider a case where $[a]_R \cap [b]_R = A$. Which would imply case 2.

    - And sets $[a]_R$ for $a \in A$ are a partition of $A$ by the definition of a equivalence class or part A of this question.

- c) Prove that $a$ $R$ $b$ iff $[a]_R = [b]_R$.
    
    - $a$ $R$ $b$ $\rightarrow$ $[a]_R = [b]_R$.
    
        If $a$ has an equivalence relation to $b$ then by the definition of a equivalence class $a$ is a member of $[a]_R$ and a member of $[b]_R$. Also by the same equivalence relation and by the definition of a equivalence class $b$ is a member of $[b]_R$ and a member of $[a]_R$. $\checkmark$

    - $a$ $R$ $b$ $\leftarrow$ $[a]_R = [b]_R$.
    
        For two equivalence classes $[a]_R$ and $[b]_R$ to be equal the equivalence classes elements $a$ and $b$ would have needed to have an equivalence relation to be a member of each others equivalent class according to the definition of an equivalence class. So $a \in [a]_R$ has to have an equivalence relation to $b \in [b]_R$, implying $(a, b) \in R$ or $a$ $R$ $b$. $\checkmark$

- Theorem 10.10.4 (for reference)

![](https://i.imgur.com/YZEu2Mv.png)

---
---
### 3
![](https://i.imgur.com/RULadVP.png)

- a) $A = \{x : x$ is a student at CCSF $\}$, $R = \{(x, y) : x$ and $y$ attend the same class $\}$

    - Reflexive: $\forall x \in A$, $(x, x) \in R$ 
    
        Student x and student x are both students at CCSF, and the same student has obviously attended the same class, so reflexive. $\checkmark$

    - Symmetric: $\forall x, y \in A$, $(x, y) \in R \rightarrow (y,x) \in R$

        If students $x, y$ are both at CCSF, if $x$ attends the same class as $y$, then $y$ would also attend the same class as $x$, so symmetric. $\checkmark$

    - Transitive: $\forall x, y ,z \in A$ $(x,y) \in R \wedge (y,z) \in R \rightarrow (x,z) \in R$

        For students $x, y, z$ at CCSF. If student $x$ and $y$ are both taking Math 115 and student $y$ and student $z$ are both taking Art 101, this is a counter example to transitivity, so not transitive. $\checkmark$

    - Conclusion: It's not an equivalence relation $\checkmark$

- b) $A = \{s : s$ is a bit string of length 10 $\}$, $R = \{(s_1, s_2) : s_1$ and $s_2$ have same first bit or the same last bit $\}$

    - Reflexive: $\forall s \in A$, $(s, s) \in R$

        Bit string $s$ and $s$ are both bit strings of length ten. Since they are the same bit string they both also begin and end with the same bit, so reflexive. $\checkmark$

    - Symmetric: $\forall s_1, s_2 \in A$, $(s_1, s_2) \in R \rightarrow (s_2,s_1) \in R$

        If two bit strings are of length ten and bit string $s_1$ begins or ends with the same bit as $s_2$, then $s_2$ would also begin or end with the same bit as $s_1$. This is valid, so symmetric. $\checkmark$

    - Transitive: $\forall s_1, s_2 ,s_3 \in A$ $(s_1,s_2) \in R \wedge (s_2,s_3) \in R \rightarrow (s_1,s_3) \in R$
    
        If the first pair of bit strings $s_1$ and $s_2$ are $1...1$ and $1...0$ respectively and $s_2$ and $s_3$ are $1...0$ and $0...0$ respectively, then $s_1$ and $s_3$ are $1...0$ and $0...0$. So I'm concluding this function is not transitive. $\checkmark$

    - Conclusion: It's not an equivalence relation $\checkmark$

- c) $A = \{f : \R \rightarrow \R \}$, $R = \{(f, g) : f(1) = g(2)$ and $f(2) = g(1) \}$

    - Reflexive: $\forall f \in A$, $(f, f) \in R$

        If $f$ maps from $\R$ to $\R$. But would $f$ satisfy $R$ such that $f(1) = f(2)$ and $f(2) = f(1)$. If $f = x^2$, then $f(1) = 1 \ne f(2) = 4$, So not reflexive. $\checkmark$

    - Symmetric: $\forall f, g \in A$, $(f, g) \in R \rightarrow (g,f) \in R$ $\checkmark$

        If $f, g \in A$ and $f, g \in R$, then $f(1) = g(2)$ and $f(2) = g(1)$ is true. The reverse is also true $g(1) = f(2)$ and $g(2) = f(1)$. So this is symmetric. $\checkmark$

    - Transitive: $\forall f, g ,h \in A$ $(f,g) \in R \wedge (g,h) \in R \rightarrow (f,h) \in R$

        If $f, g ,h \in A$ and $(f,g) \in R \wedge (g,h) \in R$, then $f(1) = g(2)$ and $f(2) = g(1)$ is true and $g(1) = h(2)$ and $g(2) = h(1)$ is true. Then we have $f(1) = h(2)$ and $f(2) = h(1)$, substituting in the above expression we get $f(1) = g(1)$ and $f(2) = g(2)$. There is cases where this might be true, but there are cases where this is also false. So not transitive. $\checkmark$

    - Conclusion: It's not an equivalence relation $\checkmark$

---
---

### 4

- a) State the definition of a graph isomorphism from a graph $G$ to a graph $H$.

    $G$ and $H$ are isomorphic if there is a bijection from the vertex set of $G$ to the vertex set of $H$ that preserves adjacency and nonadjacency.

- b) Use that definition to prove that the relation $R = \{(G, H): G$ is isomorphic to $H$ $\}$ is an equivalence relation on the set of undirected graphs.

    $A = \{G_{set} : G_{set}$ set of undirected graphs $\}$

    - Reflexive: $\forall G \in A$, $(G, G) \in R$ 
    
        If graph $G$ is an undirected graph, $G$ would map each vertex to itself in another $G$, so $G$ is isomorphic to $G$, so reflexive. $\checkmark$

    - Symmetric: $\forall G, H \in A$, $(G, H) \in R \rightarrow (H, G) \in R$

        If graph $G$ and $H$ are undirected graphs and ($G$, $H$) is isomorphic, then ($H$, $G$) would also be isomorphic via an inverse(or reverse) of the function that mapped $G$ to $H$. So symmetric. $\checkmark$

    - Transitive: $\forall G, H, I \in A$ $(G, H) \in R \wedge (H, I) \in R \rightarrow (G, I) \in R$

        If $G$, $H$ and $I$ are undirected graphs and ($G$, $H$) and ($H$, $I$) are isomorphic, then ($G$, $I$) are isomorphic because of bijectivity and the preserved adjacencies. So transitive. $\checkmark$

        In a different scenario where ($G$, $H$) is only bijective and ($H$, $I$) is only bijective, and ($G$, $I$) is bijective. This doesn't imply ($G$, $I$) is isomorphic, because a bijection only requires a one to one mapping of vertices and that every vertex in the other graph is mapped. These alone doesn't meet the extra requirements for an isomorphism.
    
    - Conclusion: It's an equivalence relation $\checkmark$

---
---

### 5

![](https://i.imgur.com/TgXWJdz.png)

- a)
 
| $M$ | a | b | c | d | e |
|---|---|---|---|---|---|
| a | 0 | 1 | 0 | 0 | 1 |
| b | 0 | 0 | 0 | 1 | 1 |
| c | 1 | 1 | 0 | 1 | 0 |
| d | 1 | 0 | 0 | 0 | 1 |
| e | 0 | 0 | 1 | 0 | 0 |

- b)

| $M$ | a | b | c | d | e |   | $M$ | a | b | c | d | e |   | $M^2$ | a | b | c | d | e |
|-----|---|---|---|---|---|---|-----|---|---|---|---|---|---|-------|---|---|---|---|---|
| a   | 0 | 1 | 0 | 0 | 1 |   | a   | 0 | 1 | 0 | 0 | 1 |   | a     | 0 | 0 | 1 | 1 | 1 |
| b   | 0 | 0 | 0 | 1 | 1 |   | b   | 0 | 0 | 0 | 1 | 1 |   | b     | 1 | 0 | 1 | 0 | 1 |
| c   | 1 | 1 | 0 | 1 | 0 | * | c   | 1 | 1 | 0 | 1 | 0 | = | c     | 1 | 1 | 0 | 1 | 3 |
| d   | 1 | 0 | 0 | 0 | 1 |   | d   | 1 | 0 | 0 | 0 | 1 |   | d     | 0 | 1 | 1 | 0 | 1 |
| e   | 0 | 0 | 1 | 0 | 0 |   | e   | 0 | 0 | 1 | 0 | 0 |   | e     | 1 | 1 | 0 | 1 | 0 |

| $M^2$ | a | b | c | d | e |   | $M$ | a | b | c | d | e |   | $M^3$ | a | b | c | d | e |
|-------|---|---|---|---|---|---|-----|---|---|---|---|---|---|-------|---|---|---|---|---|
| a     | 0 | 0 | 1 | 1 | 1 |   | a   | 0 | 1 | 0 | 0 | 1 |   | a     | 2 | 1 | 1 | 1 | 1 |
| b     | 1 | 0 | 1 | 0 | 1 |   | b   | 0 | 0 | 0 | 1 | 1 |   | b     | 1 | 2 | 1 | 1 | 1 |
| c     | 1 | 1 | 0 | 1 | 3 | * | c   | 1 | 1 | 0 | 1 | 0 | = | c     | 1 | 1 | 3 | 1 | 3 |
| d     | 0 | 1 | 1 | 0 | 1 |   | d   | 1 | 0 | 0 | 0 | 1 |   | d     | 1 | 1 | 1 | 2 | 1 |
| e     | 1 | 1 | 0 | 1 | 0 |   | e   | 0 | 0 | 1 | 0 | 0 |   | e     | 1 | 1 | 0 | 1 | 3 |


| $M^3$ | a | b | c | d | e |   | $M$ | a | b | c | d | e |   | $M^4$ | a | b | c | d | e |
|-------|---|---|---|---|---|---|-----|---|---|---|---|---|---|-------|---|---|---|---|---|
| a     | 2 | 1 | 1 | 1 | 1 |   | a   | 0 | 1 | 0 | 0 | 1 |   | a     | 2 | 3 | 1 | 2 | 4 |
| b     | 1 | 2 | 1 | 1 | 1 |   | b   | 0 | 0 | 0 | 1 | 1 |   | b     | 2 | 2 | 1 | 3 | 4 |
| c     | 1 | 1 | 3 | 1 | 3 | * | c   | 1 | 1 | 0 | 1 | 0 | = | c     | 4 | 4 | 3 | 4 | 3 |
| d     | 1 | 1 | 1 | 2 | 1 |   | d   | 1 | 0 | 0 | 0 | 1 |   | d     | 3 | 2 | 1 | 2 | 4 |
| e     | 1 | 1 | 0 | 1 | 3 |   | e   | 0 | 0 | 1 | 0 | 0 |   | e     | 1 | 1 | 3 | 1 | 3 |


| $M^4$ | a | b | c | d | e |   | $M$ | a | b | c | d | e |   | $M^5$ | a | b | c | d | e  |
|-------|---|---|---|---|---|---|-----|---|---|---|---|---|---|-------|---|---|---|---|----|
| a     | 2 | 3 | 1 | 2 | 4 |   | a   | 0 | 1 | 0 | 0 | 1 |   | a     | 3 | 3 | 4 | 4 | 7  |
| b     | 2 | 2 | 1 | 3 | 4 |   | b   | 0 | 0 | 0 | 1 | 1 |   | b     | 4 | 3 | 4 | 3 | 7  |
| c     | 4 | 4 | 3 | 4 | 3 | * | c   | 1 | 1 | 0 | 1 | 0 | = | c     | 7 | 7 | 3 | 7 | 12 |
| d     | 3 | 2 | 1 | 2 | 4 |   | d   | 1 | 0 | 0 | 0 | 1 |   | d     | 3 | 4 | 4 | 3 | 7  |
| e     | 1 | 1 | 3 | 1 | 3 |   | e   | 0 | 0 | 1 | 0 | 0 |   | e     | 4 | 4 | 3 | 4 | 3  |

- c)
There are three hamiltonian cycles that start and end at vertex $a$.

- d) No, there is not a closed walk of length five that isn't a Hamiltonian cycle. The reason requires two cases.

    - case 1: 
        A hamiltonian cycle of length 3 and length 2 would have to exist. But the $M^2$ matrix shows there isn't a hamiltonian cycle of length 2.

    - case 2:
        A hamiltonian cycle of length 4 and length 1 would have to exist. But the $M^1$ or $M$ matrix shows there isn't a hamiltonian cycle of length 1.

    I believe these two cases are enough to justify there is not a closed walk of length five.

---
---


*END*

---
---