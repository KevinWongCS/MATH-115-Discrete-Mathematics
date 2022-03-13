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
A robot named Wall-E wanders around a two-dimensional grid. He starts out at
$(0, 0)$ and is allowed to take four different types of steps:

1. $(+2, -1)$
1. $(+1, -2)$
1. $(+1, +1)$
1. $(-3, 0)$

Wall-E’s true love, the fashionable and high-powered robot, Eve, awaits at $0, 2)$.

(a) Describe a state machine model of this problem. What are the states? The
transitions?

(b) Will Wall-E ever find his true love? If yes, find a path from Wall-E to Eve. If
no, use the Invariant Principle to prove that no such path exists, being sure to clearly
state and prove your preserved invariant. Hint: The value $x-y$ is not preserved, but how can it change? 

---
---
- a) Describe a state machine model of this problem. What are the states? The
transitions? 

The start state is $(0, 0)$

The transitions are given by rules:

$(0,0) \rightarrow \left\{ \begin{array}{rcl}{step1(+2, -1)} &\\ {step2(+1, -2)} &\\ {step3(+1, +1)}&\\ {step4(-3, +0)}\end{array}\right.$

- b) Unfortunately, Wall-E will never find his true love. After some trial and error it appears all steps result in coordinates where the difference of $(x, y)$ will always be a multiple of 3. So Eve is at $(0, 2)$ so Wall-E will never reach those coordinates because $0 - 2$ is not divisible by 3.

   - Base case: $P(0) = (0,0)$

   - Inductive Step: Assume $(a, b) \in \Z^2$


      - step 1: $(a + 2, b - 1): a + 2 - (b - 1) = a - b + 3$

        case 1: if $a = b$ then step 3 occurs resulting in a 3.

        case 2: if $a \neq b$ then steps 1, 2, 4 occur and those steps are always changing the coordinates where the their difference is a multiple of 3.

      - step 2: $(a + 1, b - 2): a + 1 - (b - 2) = a - b + 3$
      
        cases are same as above.

     - step 3: $(a + 1, b + 1): a + 1 - (b + 1) = a - b$

         case 1: if $a = b$ we have 0

         case 2: if $a \neq b$ then steps 1, 2, 4 occur and those steps are always changing the coordinates where the their difference is a multiple of 3.

     - step 4: $(a - 3, b + 0): a - 3 - b = a - b - 3$
     
       cases are analogous to inductive step 1. Either way we are left with the difference of $x, y$ being a multiple of 3.

   

```
# simple program that test the rule
import random

WallE = [0,0]

random.randint(1, 4)

for x in range(10000000):
    
    step = random.randint(1, 4) # gets random num 1 <= x <= 4

    if step == 1: # (+2, -1)
        WallE[0] = WallE[0] + 2
        WallE[1] = WallE[1] - 1

    elif step == 2: # (+1, -2)
        WallE[0] = WallE[0] + 1
        WallE[1] = WallE[1] - 2

    elif step == 3: # (+1, +1)
        WallE[0] = WallE[0] + 1
        WallE[1] = WallE[1] + 1

    elif step == 4: # (-3, +0)
        WallE[0] = WallE[0] + 3
        WallE[1] = WallE[1] + 0

    
    # print coordinates if a step isn't a factor of 3
    diff = WallE[0] - WallE[1]
    if (diff % 3) != 0:
        print("(",WallE[0], WallE[1], ")")

# There is no output, meaning in ten million steps not one step doesn't follow the rule.
    
```

- This concludes that Wall-E will never find Eve.

---
---

### 6.12 

### 6.15 (parts b and c)