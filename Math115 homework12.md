name: kevin wong\
filename: Math115 homework12\
date: 04/20/2022\
desc: https://courses.csail.mit.edu/6.042/spring18/mcs.pdf (Links to an external site.) please do these problems: additional problem, 12.23, 12.56ab, 12.57, 12.63.

---
---

### Character Frequency Problem

![](https://i.imgur.com/HEchBHq.png)

- a) $b = 0100, e = 11, a = 10, d = 0110$

    bead is encoded with bit string $0100$  $11 10$ $0110$.

- b) The average number of bits used per character is $2(0.26) + 4(0.02) + 4(0.09) + 4(0.08) + 2(0.30) + 2(0.14) + 4(0.11) = 2.6 $

- c) Using Hoffman coding to get the optimal encoding for characters into bit strings given their frequencies in a text.

    Heavier weight goes on left.
    
    Lighter weight on right.

    Branching left is assigned a zero bit.

    Branching right is assigned a one bit.

```
a: 0.26    b: 0.02    c : 0.09    d : 0.08    e : 0.30    f : 0.14    g : 0.11

a: 0.26    cb: 0.11    d : 0.08    e : 0.30    f : 0.14    g : 0.11
           /\ 
          c  b  

a: 0.26    cbd: 0.19    e : 0.30    f : 0.14    g : 0.11
            /\
           /\ d
          c  b   

a: 0.26    cbd: 0.19    e : 0.30    fg : 0.25
            /\                      /\ 
           /\ d                    f  g 
          c  b   

a: 0.26    fgcbd: 0.44    e : 0.30
            / \
           /   \       
          /     \
         /\     /\                      
        f  g   /\  d                   
              c  b   

          fgcbd: 0.44    ea : 0.56
           / \           /\ 
          /   \         e  a  
         /     \
        /\     /\                      
       f  g   /\  d                   
             c  b

          eafgcbd: 1
            /  \
          0/    \1
          /      \
        0/\1    / \           
        e  a  0/   \1         
              /     \
            0/\1   0/ \1 
            f  g  0/\1 \   
                  c  b  d 
```
A lower average number of bits used per character is $2(0.26) + 4(0.02) + 4(0.09) + 3(0.08) + 2(0.30) + 3(0.14) + 3(0.11) = 2.55$

---
---

### 12.23 
![](https://i.imgur.com/vywqYuf.png)

I think it's logical to work from a smaller chromatic number, $\chi(G)$ to a larger one. This graph has more than one edge, we know $\chi(G) \ne 1$. We can also conclude that $\chi(G) \ne 2$ because in this graph there exist a triangle and a pentagon, and we know $\chi(Cycle_{odd}) = 3$. If the most bottom edge wasn't there, the chromatic number of $3$ ($\chi(G) = 3$) would be the minimal colors needed for all adjacent vertices to not have the same colors, but since that edge exist one additional color has to be added to create a valid coloring for graph $G$. So $\chi(G) = 4$.


---
---


### 12.56ab

![](https://i.imgur.com/AxTNE7L.png)
![](https://i.imgur.com/E2H6LNA.png)

- a) 
![](https://i.imgur.com/nd8Zqxh.png)

- b)
![](https://i.imgur.com/hXmtjw3.png)


---
---


### 12.57

![](https://i.imgur.com/XycPU3u.png)

- a) Assume the left side. Prove right side. If $G$ is 2-colorable that means we can select any vertex in a closed cycle and assign it a color ($color_1$) and it's adjacent vertex a different color ($color_2$). As we walk along the graph we assign $color_1$ and $color_2$ in an alternating fashion until we reach a point at the end of the cycle where every vertex is assigned either $color_1$ or $color_2$ and no adjacent vertex has the same color. This is only possible if the cycle is even because an odd cycle has an odd chromatic number ($\chi(C_{odd}) = 3$).$\checkmark$
    
- b) If a connected component was has an odd number closed walk then we know that cycle requires a minimum of 3 colors for a valid coloring or else two adjacent vertices would have the same color. This can be used as a counter example to disprove or prove a graph is not 2-colorable or bipartite. $\checkmark$

- c) To 2-color any tree, select two colors, $color_1$ and $color_2$. Assign the parent a color, then assign all descendants the other color. Then continuously alternate the colors each generation. This is possible because tree graphs are acyclic, meaning there doesn't exist a cycle in the graph, so we don't have to account for even or odd cycles.

- d) If all edges in $T$ connect different colored vertices(assuming we are only using two colors), then we know $T$ is 2-colorable and we know 2-colorable graphs have an even number of closed cycles. This is consistent with the theorum.

    If $T$ has an edge that connects two same colored vertices or an additional third color to get a valid coloring, that means there exist an odd number closed cycle in $T$ and that isn't consistent with what the theorum above, so the *iff* doesn't hold in these cases.$\checkmark$


---
---


### 12.63
How many 5-vertex non-isomorphic trees are there? Explain.

I believe there are only three non-isomorphic threes.

```
Starting with the lowest degree per vertex a line:

1---2---3---4---5

    5
    |
1---2---3---4

and 

    2
    |
1---5---3
    |
    4

Any kind of deletion and addition of an edge must preserve the connectedness and acyclicness of the graph to still be a tree.
```
At this point I don't believe it is possible to find another non-isomorphic tree. Any other manipulation will lead to a connected graph, a disconnected graph, or an isomorphism. $\checkmark$

---
---

*END*

---
---