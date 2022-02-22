name: kevin wong\
filename: Math115 homework4\
date: 2/14/2022\
desc: https://courses.csail.mit.edu/6.042/spring18/mcs.pdf (Links to an external site.) please do these problems:  5.3, 5.11, 5.22, 5.28, 5.30 x/c 5.10, 5.17, 5.27

### Problem 5.3
Use induction to prove that

$1^3 + 2^3 +...+n^3 = (\frac{n(n+1)}{2})^2$ for all m $\ge$ 1

---
---

proof by induction

Let our induction hypothesis be $p(n) = 1^3 + 2^3 +...+n^3 = (\frac{n(n+1)}{2})^2$ for all m $\ge$ 1

- **base case**

   if $n=0$ then,

   $p(0) = 0^3 = (\frac{0(0+1)}{2})^2 = 0$
   
   So the base case is true

- **inductive step**
   
   Assumption: $p(n)\rightarrow p(n + 1)$ 

   I will assume the left side of the equation($p(n)$) above to be true to prove the right side($p(n+1)$).

   I add $(n+1)$ to both sides of the induction hypothesis and will try to prove the right side is true for all m $\ge$ 1

   $p(n + 1) = 1^3 + 2^3 +...+n^3 + (n + 1)^3 = (\frac{n(n+1)}{2})^2 + (n + 1)^3$

   simplifying the right side of equation:

    $ = (n + 1)^2((\frac{n}{2})^2 + (n + 1))$
    
    $ = (n + 1)^2(\frac{n^2}{4} + \frac{4(n + 1)}{4})$
    
    $ = (n + 1)^2(\frac{n^2 + 4n + 4}{4})$
    
    $ = (n + 1)^2(\frac{(n + 2)(n + 2)}{4})$
    
    so, $p(n + 1) = 1^3 + 2^3 +...+n^3 + (n + 1)^3 = (n + 1)^2(\frac{(n + 2)(n + 2)}{4})$

- I don't believe the induction holds for this hypothesis, so I would have to say $p(n)$ does not imply $p(n + 1)$
   
   A counter example would be if I set $ n = 2$ 

   $1^3 + 2^3 = (2 + 1)^2 * \frac{(2 + 2)(2 + 2)}{4}$
   
   $9 = (9)(\frac{16}{4}) = 36$ which doesn't hold true. 
- **Conclusion**: I think this cannot be proven by induction.
---
---

### Problem 5.11

Use induction on the number of squares to prove that the length of the periphery is always even, no matter how many squares Theory Hippotamus places or how he arranges them.

---
---
Prove by induction

Let our induction hypothesis be $p(n) = n$ where n is positive and even number and each new square shared an edge with at least one previously-placed square and no squares overlapped.

- **base case**

   if $n=0$ then,

   using our hypothesis $p(0) = 0 $ 
   
   Our base case passes, since there are zero squares which means zero edges.

- **inductive step**

    Assumption: $p(n)\rightarrow p(n + 1)$ where n is positive and even number, and each new square shared an edge with at least one previously-placed square and no squares overlapped.
    
    So to prove his theory I would have to fail at finding a counterexample. After playing around with different configurations I would have to say it is very difficult to find one if not impossible. In every combination I tried, the number of edges always came out to be even described by

   $ TotalOutSideEdges= (Total Number Of Squares * 4)-(Total Edges Touching * 2) $

- **Conclusion**:    So I couldn't disprove $p(n)\rightarrow p(n + 1)$. I would have to agree that induction does prove this hypothesis.
___
___

### Problem 5.22
The Fibonacci numbers F(n) are described in Section 5.2.2.

Indicate exactly which sentence(s) in the following bogus proof contain logical
errors? Explain.

False Claim. Every Fibonacci number is even.

*Bogus proof*. Let all the variables $n, m, k$ mentioned below be nonnegative integer valued. Let $Even(n)$ mean that $F(n)$ is even. The proof is by strong induction with
induction hypothesis $Even(n)$.

**base case**: $F(0) = 0$ is an even number, so $Even(0)$ is true.


**inductive step**: We assume may assume the strong induction hypothesis

   $ Even(k) for 0 \le k \le n$,

and we must prove $Even(n + 1)$

Then by strong induction hypothesis, $Even(n)$ and $Even(n - 1)$ are true, that is, $F(n) + F(n - 1)$ are both even. But by the definition, $F(n + 1)$ equals the sum $F(n) + F(n - 1)$ of two even numbers, and so it is also even. This proves $Even(n + 1)$ as required. 

Hence, F(m) is even for all $m \epsilon \N$  by the string induction principle.

___
___
- I agree with the base case.

- The inductive step is where we will probably find a error. I will try to find a counter example for $ Even(k) for 0 \le k \le n$. The claim *"Then by strong induction hypothesis, $Even(n)$ and $Even(n - 1)$ are true, that is, $F(n) + F(n - 1)$ are both even. But by the definition, $F(n + 1)$ equals the sum $F(n) + F(n - 1)$ of two even numbers, and so it is also even."* doesn't hold up because an even number can be the result of the sum of two odd numbers, which is the case in the set of Fibonacci numbers. 

- **Conclusion**: So the induction should have failed to prove every Fibonacci is even.
___
___

### Problem 5.28
A group of $ n \ge 1$ people can be divided into teams, each containing either 4 or
7 people. What are all the possible values of n? Use induction to prove that your
answer is correct.

___
___
prove by induction

   Let the induction hypothesis be $ p(n) = $ "team of $n$ people", where $n$ is $ n \ge 1$

- **base case** 

   

   if $n = 4$ 

   then $ p(4) = $ "team of $4$ people"

   The base case is okay, since the lowest amount of people in a group is 4.

- **inductive step**

   let $p(n) \rightarrow p(n+1)$

   so if $p(4)$ then $p(5)$

   The inductive step doesn't hold true for every $n$ where $ n \ge 1$ because $n$ would have to be a multiple of 4 or 7, or a common multiple of both, in order for the groups to be divided into 4 or 7 people. So I would say the inductive step fails.
 
- **Conclusion**: So induction cannot prove that all groups of $ n \ge 1$ people can be divided into teams with each containing either 4 or 7 people.
___
___

### Problem 5.30
The Fibonacci numbers F(n) are described in Section 5.2.2.

These numbers satisfy many unexpected identities, such as

$F(0)^2 + F(1)^2 + ... + F(n)^2 = F(n)F(n+1)$

Equation (5.21) can be proved to hold for all $n \epsilon \N$ by induction, using the equation itself as the induction hypothesis $P(n)$.

**(a)** Prove the base case $(n = 0)$

**(b)** Now prove the inductive step.
___
___
prove by induction

Let the induction hypothesis be 

$ p(n) = F(0)^2 + F(1)^2 + ... + F(n)^2 = F(n)F(n+1)$ for $n \epsilon \N$

- **base case**
   
   if $n = 0$
   
   then $p(0) = F(0)^2 = F(0)F(0+1) = 0 $

   So the base case is satisfied.

- **inductive step**
   
   let $p(n) \rightarrow p(n + 1)$

   We assume $p(n)$ is true to prove the $p(n+1)$. 

   I then add $F(n + 1)^2$ to both sides of the induction hypothesis above.

   $p(n + 1) = F(0)^2 + F(1)^2 + ... + F(n)^2 + F(n+1)^2= F(n)F(n+1) + F(n+1)^2$ for $n \epsilon \N$

   

   Simplifying the right side of the equation:

   $F(n)F(n+1) + F(n+1)^2$

   $= F(n + 1) * (F(n) + F(n+1))$

   Recombining the equations:

   $F(0)^2 + F(1)^2 + ... + F(n)^2 + F(n+1)^2 = F(n + 1) * (F(n) + F(n+1))$

   or 

   $\sum_{n = 0}^{n + 1} F(0)^2 + ...+ F(n + 1)^2 = F(n + 1) * (F(n) + F(n+1))$


- **Conclusion**: I couldn't figure out the mathematical manipulation to make the left side equal the right side, but after plugging in some numbers I believe this argument is valid for every for $n \epsilon \N$. So I would say by induction the hypothesis is true.
___
___

