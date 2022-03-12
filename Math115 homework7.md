name: kevin wong\
filename: Math115 homework7\
date: 3/12/2022\
desc: https://courses.csail.mit.edu/6.042/spring18/mcs.pdf (Links to an external site.) please do these problems:  7.3, 7.10, 6.3, 6.12, 6.15 (parts b and c); optional extra credit problems: 7.23 (1.5pts), 6.4 (1pt), 6.5(1pt), 6.15(part a; 0.5 pts).

### 7.3
The *reversal* of a string is the string written backwards, for example, $rev(abcde) = edcba$.

a) Give a simple recursive definition of $rev(s)$ based on the recursive definitions 7.1.1 of $s \in A^*$ and of the concatenation operation 7.1.3.

b) Prove that 

$rev(s \cdot t) = rev(t) \cdot rev(s)$

for all strings $r,s,t \in A^*$

---
---

- a) Give a simple recursive definition of $rev(s)$.

    - Base case: $ \lambda \in A^* $ where $\lambda$ is an empty string.

      \# the reverse of an empty string is itself, an empty string.

   - Constructor cases: 

       If $s,\lambda \in A^*$ then $rev(s \cdot \lambda) ::= rev(s) ::= s$ 
   
      If $s,t  \in A^*$ then $rev(s \cdot t) ::= rev(t) \cdot rev(s) ::= t \cdot s$

     

- b) Prove by structural induction

   - Base case: If $t \in A^*$ and $t = \lambda$ then $rev(t) = t = \lambda$

   - Inductive step

        Assume $s, t \in A^*$ and $rev(s \cdot t) = t \cdot s $.

        - case 1:  

            Suppose $x \cdot y, s, t \in A^*$ and $rev(x \cdot y \cdot s \cdot t) = t \cdot s \cdot y \cdot x.$ Where $x, y$ represent any combination of immediate or future descendants in $A^*$.
        
            $rev(x \cdot y \cdot s \cdot t) = rev(t) \cdot rev(s) \cdot rev(x \cdot y)$

            by definition of $rev()$

            $ = rev(t) \cdot rev(s) \cdot rev(y) \cdot rev(x) $ 

            by definition of $rev()$
         
            $ = t \cdot s \cdot y \cdot x $

        - case 2: 
        
            Suppose $x \cdot y ,s, t \in A^*$, $y = \lambda$ and $x$ represent any combination of immediate or future descendants in $A^*$.

            $rev(x \cdot y, s, t) = rev(t) \cdot rev(s) \cdot rev(x \cdot y)$

            by the definition of concatenation (with an empty string)

            $ = rev(t) \cdot rev(s) \cdot rev(x)$ 

            by definition of $rev()$

            $ = t \cdot s \cdot x$

        - other cases: 

            Similar cases follow for the concatenation with empty strings($\lambda$), where utilizing the definition of concantenation with the definition of $rev()$ will result in the reverse string.

        - This proves that the immediate descendant and future descendants will be concantenated on the right side of the string, creating a string that is the reverse of the string produced by the definition of concatenation on the same set. $\checkmark$
---
---

### 7.10
Fractals are an example of mathematical objects that can be defined recursively. In this problem, we consider the Koch snowflake. Any Koch snowflake can be constructed by the following recursive definition.

- Base case: An equilateral triangle with a positive integer side length is a
Koch snowflake.

- Constructor case: Let $K$ be a Koch snowflake, and let $l$ be a single edge
of the snowflake. Remove the middle third of $l$, and replace it with two line
segments of the same length as the middle third, as shown in Figure 7.8
The resulting figure is also a Koch snowflake.

- a) Find a single Koch snowflake that has exactly 9 edges and includes at least 3
different edge lengths.

- b) Prove using structural induction that the area inside any Koch snowflake is of
the form $q\sqrt{3}$, where $q$ is a rational number. Be sure to clearly label your induction
hypothesis and other necessary assumptions during your proof.

- Hint: If you require other facts about Koch snowflakes, be sure to prove those by
structural induction too.

---
---
- a) Find a single Koch snowflake that has exactly 9 edges and includes at least 3
different edge lengths.
```
░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░     edges 1, 2 are the same length
░░░░░░░░░░░░░░░░░░░█░░░░░░░░░░░░░░░░░░░     edges 3, 4, 9 are the same length
░░░░░░░░░░░░░░░░░░█░█░░░░░░░░░░░░░░░░░░     edges 5, 6, 7, 8 are the same length
░░░░░░░░░░░░░░░░░█░░░█░9░░░░░░░░░░░░░░░
░░░░░░░░░░░░░░░░█░░░░░█░░░░7░░█░░6░░░░░
░░░░░░░░░░░░░░░█░░░░░░░█░░░░░█░█░░░░░░░
░░░░░░░░░░░░░░█░░░░░░░░░█░8░█░░░█░5░░░░
░░░░░░░░░░░░░█░░░░░░░░░░░███░░░░████░░░
░░░░░░░░░░░░█░░░░░░░░░░░░░░░░░░░░░█░░░░
░░░░░░░░1░░█░░░░░░░░░░░░░░░░░░░░░█░░░░░
░░░░░░░░░░█░░░░░░░░░░░░░░░░░░░░░█░░4░░░
░░░░░░░░░█░░░░░░░░░░░░░░░░░░░░░█░░░░░░░
░░░░░░░░█░░░░░░░░░░░░░░░░░░░░░█░░░░░░░░
░░░░░░░█░░░░░░░░░░░░░░░░░░░░░░░█░░░░░░░
░░░░░░█░░░░░░░░░░░░░░░░░░░░░░░░░█░░3░░░
░░░░░█░░░░░░░░░░░░░░░░░░░░░░░░░░░█░░░░░
░░░░█░░░░░░░░░░░░░░░░░░░░░░░░░░░░░█░░░░
░░░█████████████████████████████████░░░
░░░░░░░░░░░░░░░░░░░2░░░░░░░░░░░░░░░░░░░
░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░
```
- B) Prove using structural induction

The area of an equilateral triangle is $Area = \frac{\sqrt{3}}{4} l^2$, where $l$ is the length of an edge. We are to prove the area of any Koch snowflake is consistent with the given equation $q \sqrt{3}$ where $q$ is a rational number.

   - Base case: 
      
       Using the definition of an equilateral triangle:

       $n = 1$ and $ n \in \Z^+$
        
       $Area = \frac{\sqrt{3}}{4}1^2 = \frac{\sqrt{3}}{4} = \frac{1}{4}\sqrt3$ $\checkmark$

      The base case is consistent with the given equation for area inside any Kock snowflake:

       $q\sqrt3$ where $q$ is a rational number $Q$. $\checkmark$

   - Inductive step:

     Inductive hypothesis: Assume the area inside a single equilateral triangle is $Area = \frac{\sqrt{3}}{4} l^2$, Need to show that adding any immediate descendants or future descendants using recursive case is of form $q\sqrt3$ where $q$ is a rational number $Q$. Using the recursive case we can derive the area of every descendent triangle, because we know it's edge length is one third the length of its parent triangle's edge. Using that knowledge we have the equation below:

     Let $n,k, j \in \N$ and $j$ is a factor of 3.

     $\sum_{n=1}^{k+1} = Area_1 + Area_2 + ... + Area_{k+1}$

     $= \frac{\sqrt{3}}{4}1^2 + \frac{\sqrt{3}}{4}(\frac{1}{3})^2 + ... + \frac{\sqrt{3}}{4}(\frac{1}{j})^2$, 

     factor out $\sqrt{3}$ 


     $= \sqrt{3} ( \sum_{n=1}^{k+1} = \frac{1}{4}1^2 + \frac{1}{4}(\frac{1}{3})^2 + ... + \frac{1}{4}(\frac{1}{j})^2 )$

     $= \sqrt{3} ($ some rational number $ ) $  $\checkmark$

     So from $n = 1$ up to the $k+1$ generation we have an equation where we can always factor out a $\sqrt3$ and we are left with a rational number which is consistent with the given $q\sqrt3$ where $q$ is a rational number $Q$. $\checkmark$

   

---
---


### 6.3

### 6.12 

### 6.15 (parts b and c)