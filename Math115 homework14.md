name: kevin wong\
filename: Math115 homework14\
date: 05/05/2022\
desc: https://courses.csail.mit.edu/6.042/spring18/mcs.pdf (Links to an external site.) please do these problems: 15.2 15.4, 15.5, 15.12, additional problem


---
---

### 15.2 

In how many different ways is it possible to answer the next chapter’s practice problems if:

- the first problem has four *true/false* questions,

    First problem: $2 * 2 * 2 * 2 = 16$ different ways to answer.

- the second problem requires choosing one of four alternatives, and

    Second problem: $4$ different ways to answer.

- the answer to the third problem is an $integer \ge 15$ and $\le 20$?

    Third problem: $15, 16, 17, 18, 19, 20$ results in $6$ different ways to answer.

- This results in $16 * 4 * 6 = 384$ different ways to answer the next chapter’s practice problems via rule of product.

---
---

### 15.4

Let $X$ be the six element set $\{x_1, x_2, x_3, x_4, x_5, x_6\}$.

- a) How many subsets of $X$ contain $x_1$?

    - Considering subsets of $X$ of size zero through the max number of elements, six.

        Subset with zero elements of $X$: $0$ ways

        Subset with one elements of $X$: $1$ way

        Subset with two elements of $X$: $1 * 6 = 6$ ways

        Subset with three elements of $X$: $1 * 6 * 6 = 36$ ways

        Subset with four elements of $X$: $1 * 6 * 6 * 6 = 216$ ways

        Subset with five elements of $X$: $1 * 6 * 6 * 6 * 6 = 1296$ ways

        Subset with six elements of $X$: $1 * 6 * 6 * 6 * 6 * 6 = 7776$ ways

    - So there are $1 + 6 + 36 + 216 + 1296 + 7776 = 9331$ possible subsets of $X$ that can contain $x_1$ via rule of sum.


- b) How many subsets of $X$ contain $x_2$ and $x_3$ but do not contain $x_6$?

    - Considering subsets of $X$ of size zero through the max number of elements, six.

        Subset with zero elements of $X$: $0$ ways

        Subset with one elements of $X$: $0$ ways

        Subset with two elements of $X$: $1 * 1 = 1$ way

        Subset with three elements of $X$: $1 * 1 * 5 = 5$ ways

        Subset with four elements of $X$: $1 * 1 * 5  * 5= 25$ ways

        Subset with five elements of $X$: $1 * 1 * 5  * 5 * 5 = 125$ ways

        Subset with six elements of $X$: $1 * 1 * 5  * 5 * 5 * 5 = 625$ ways

    - So there are $1 + 5 + 25 + 125 + 625 = 781$ possible subsets of $X$ containing $x_2$ and $x_3$ but do not containing $x_6$ via rule of sum.

---
---

### 15.5

![](https://i.imgur.com/7CRgn4v.png)

---
---

### 15.12

Eight students—Anna, Brian, Caine,. . . —are to be seated around a circular table in a circular room. Two seatings are regarded as defining the same *arrangement* if each student has the same student on his or her right in both seatings: it does not matter which way they face. We’ll be interested in counting how many arrangements there are of these 8 students, given some restrictions.

- a) As a start, how many different arrangements of these 8 students around the table are there without any restrictions?
- b) How many arrangements of these 8 students are there with Anna sitting next to Brian?
- c) How many arrangements are there with if Brian sitting next to both Anna AND Caine?
- d) How many arrangements are there with Brian sitting next to Anna OR Caine?

---
---

### additional problem

![](https://i.imgur.com/XNztcJf.png)


---
---


*END*

---
---