name: kevin wong\
filename: Math115 homework15\
date: 05/16/2022\
desc: https://courses.csail.mit.edu/6.042/spring18/mcs.pdf (Links to an external site.) please do these problems: 15.16, 15.37, 15.58, 15.73, 15.79


---
---

### 15.16
![](https://i.imgur.com/KKgK8Nj.png)

- a) $k = (3!)^4$, a $(3!)^4$-to-1 mapping
- b) $j = 4!$, a $4!$-to-1 mapping
- c) $\frac{12!}{4! * (3!)^4} = 15400$ possible group assignments
- d) 3n students can be broken up into $\frac{3n!}{n! * (3!)^n}$ possible group assignments
---
---

### 15.37

![](https://i.imgur.com/kfqazip.png)
![](https://i.imgur.com/RqC1o16.png)

- a) There are 41 edges in $C_{41}$ and $\frac{41(41-1)}{2} = 820$ edges in $K_{41}$

    
- b) There are $41!$ isomorphisms from $K_{41}$ to $K_{41}$. Basically all permutations of the vertices in the graph. Any of the vertices in this graph can be interchanged and the adjacencies will be preserved.
- c) There are $41!$ isomorphisms from $C_{41}$ to $C_{41}$, same reason as part b.
- d) $ \chi (K_{41})$ = 41 because every vertex has an edge to each vertex in the graph.
- e) $ \chi (C_{41})$ = 3 because this graph has an old number of vertices with each vertex having degree 2.
- f) There are 40 edges in a spanning tree of $K_{41}$
- g) If a graph is created by adding a single edge between nonadjacent vertices of a tree with 41 vertices, the largest number of cycles the graph would have would be 1 because a tree is acyclic.
- h) The smallest number of leafs possible in a spanning tree of $K_{41}$ is 2. Basically $C_{41}$ with any one edge removed.
- i) The largest number of leafs possible in a spanning tree of $K_{41}$ is 40. 40 leafs branching off a vertex.
- j) $C_{41}$ can have a maximum of 41 spanning trees, by removing anyone of the 41 edges.
- k) A complete graph can have a maximum of $n^{n-2}$ spanning trees, so $K_{41}$ has $41^{41-2}$ spanning trees.
- l) There are 40 edges for each vertex in $K_{41}$, so $40 * 40 * 40 * 40 * 40 * 40 * 40 * 40 * 40 * 40$ length-10 paths in $K_{41}$ 
- m) There are 40 edges for each vertex in $K_{41}$, so $40 * 39 * 38 * 37 * 36 * 35 * 34 * 33 * 32 * 31$ length 10 cycles in $K_{41}$

---
---

### 15.58

![](https://i.imgur.com/R9YBrRP.png)

- a) $\frac{50!}{20! * (50 - 20)!} = P$. The same as 50 choose 20. The order of going right and up don't matter in this problem.
- b) | paths that go to (10,10) | + | paths the go from (10, 10) to (20, 30) |
    
    $\frac{20!}{10! * (20 - 10)!} + \frac{30!}{10! * (30 - 10)!}  = N_1$

- c) $P - N_1 - N_2$
    
    The paths that go through $(15, 20)$ are 

    | paths that go to (15,20) | + | paths the go from (15, 20) to (20, 30) |

    are $\frac{35!}{15! * (35 - 15)!} + \frac{15!}{5! * (15 - 5)!} = N_2$

    So the paths from (0,0) to (20, 30) that do not go through either (10,10) and (15,20) are calculated using the expression below.

    $\frac{50!}{20! * (50 - 20)!} - 
(\frac{20!}{10! * (20 - 10)!} + \frac{30!}{10! * (30 - 10)!}) 
-(\frac{35!}{15! * (35 - 15)!} + \frac{15!}{5! * (15 - 5)!})$



---
---

### 15.73

![](https://i.imgur.com/2Q1XZ22.png)

- Let $n$ and $m$ be the number of decisions in two different sets. In the time you have you can only accomplish $k$ decisions.

- RHS, only allowed to make $k$ decisions from either the $n$ pool or the $m$ pool.

- LHS, if $r$ is increased by one, that takes away a decision from the $m$. Summing 0 to $n$ counts all possible decisions or cases from $r$ equal to 0 to $r$ equal to $n$.

- So the LHS and the RHS are both counting $k$ decisions possible out of $n + m$ number of decisions.

---
---

### 15.79

![](https://i.imgur.com/yHVEvdM.png)

- The below is just a guess, I don't know, but I believe the math works out with what I have below.

- The LHS is equal to $\sum_{i = 0}^{n} i^2 - i = RHS$. This counts all the sets of $i^2 - i$ from 0 to $n$.

- The RHS is counts all the elements for $n + 1$ choose 3 elements two times. The elements chosen have to be in a specific order to satisfy the elements of the rows in the table below.

- The both seem to count the sum of the elements in row 1 in the image below.



```
0*1 + 1*2 + 2*3 + 3*4 + 4*5 + 5*6 + 6*7 + 7*8+...+ (n-1)n

difference between each number forms this triangle shape with 3 rows:

0   2   6   12  20  30  42  56 ... "row 1"
  2   4   6   8   10  12  14 ...   "row 2"
    2   2   2   2   2   2 ...      "row 3"
      0   0   0   0   0...
```

---
---

*END*

---
---