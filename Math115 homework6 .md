name: kevin wong\
filename: Math115 homework6\
date: 2/21/2022\
desc: https://courses.csail.mit.edu/6.042/spring18/mcs.pdf (Links to an external site.) please do these problems:  1, 2, 3

### \#1
Here is a recursively defined function, $ f : $ { $ n \in \N : n \ge 1 $ } $\rightarrow \N $.

Base case: $f(1) = 0$.

Recusive case: $f(n + 1) = f(n) + 2n - 1$

a) Compute $f(n) $ for $n = 2, 3, 4, 5 $.

b) This function is equal to a polynomial function $p$. Find $p$ and prove that $f(n) = p(n)$ for all $n \ge 1$.

---
---
-  a)  Compute $f(n) $ for $n = 2, 3, 4, 5 $.
   
   -  $n = 1$

      $f(1 + 1) = f(1) + (2*1) - 1$ 

      $f(2) = 0 + 2 - 1$

      $f(2) = 1$

   - $n = 2$

      $f(2 + 1) = f(2) + (2*2) - 1$ 

      $f(3) = 1 + 4 - 1$

      $f(3) = 4$

   - $n = 3$
      
      $f(3 + 1) = f(3) + (2*3) - 1$ 

      $f(4) = 4 + 6 - 1$

      $f(4) = 9$

   - $n = 4$
   
      $f(4 + 1) = f(4) + (2*4) - 1$ 

      $f(5) = 9 + 8 - 1$

      $f(5) = 16$

   - $n = 5$
   
      $f(5 + 1) = f(5) + (2*5) - 1$ 

      $f(6) = 16 + 10 - 1$

      $f(6) = 25$
    
- evaluated base cases for $n=1,2,3,4,5$ for $f(n)$, so now we want an explicit formula for the recursive function.


- b) finding $p(n)$

   Assume $n \in \N$ and $p(n) = n^2 - 2n + 1$ and $p(n) \in \N$ (found through trial and error).

    Using the recursive case equation:  

    $p(n + 1) = p(n) + 2n - 1$

    substituting $p(n) =n^2 - 2n + 1$
     
    $= (n^2 -2n + 1) + 2n - 1$

    $= n^2$ 
    
    so, $p(n + 1) = n^2$ $\checkmark$

    and $p(n) = (n-1)^2 $ $\checkmark $

- prove $f(n) = p(n)$

    *reminder*: $f(n) = f(n + 1) - 2n + 1$ and $p(n) = (n-1)^2$

    prove by weak induction

    - base case $ n \in \N $ and $n=1,2,3,4,5$ for $p(n)$
    
        $p(1) = (1 - 1)^2 = 0$ $\checkmark$ 
        
        $p(2) = (2 - 1)^2 = 1$ $\checkmark$  
    
        $p(3) = (3 - 1)^2 = 4$ $\checkmark$ 
    
        $p(4) = (4 - 1)^2 = 9$ $\checkmark$
    
        $p(5) = (5 - 1)^2 = 16$ $\checkmark$
    
        so for $n=1,2,3,4,5$, $p(n) = f(n)$ in each case.

    - inductive step
    
        *inductive hypothesis*: Assume $k \in \N$, $k \ge 5$ and $1 \le n \le k $ and $p(k) = (k - 1)^2 $. Also assume $ p(k) \rightarrow p(k + 1) \in \N $.
    
        $ p(n) = (n - 1)^2$
     
        so $ p(k + 1) = ((k + 1) - 1)^2 $
        
        $= k^2 $
    
        $= (k + 1 - 1)^2 $ 
    
        $= ((k - 1) + 1)^2 $
    
        $ = ((k - 1) + 1) * ((k - 1) + 1) $ 
    
        $ = (k-1)^2 + 2(k-1) + 1 $
    
        $ = (k-1)^2 + 2k - 2 + 1 $
    
        $ = (k-1)^2 + 2k - 1 $
    
        $ = p(n) + 2k - 1 $ 
    
        so $p(k + 1) = p(n) + 2k - 1 = f(k + 1)$  $ \checkmark $


---
---

### \#2
Here is a recursively defined set, $S$.

Base cases: $ 5, 9 \in S$

Recursive Case: If $x \in S$ and $y \in S$, then $ x + y \in S$

a) Give a non-recursive definition, $R$, of the set $S$.

b) Prove that your set $R$ in part (a) equals the set $S$.

---
---
- a) non-recursive definition, $R$
    
    $ R ::= $ { $ x, y \in S : \exists n \in \N_1,  \exists m \in \N_0: nx + my  = z : z \in S$ } $\bigcap$ { $x = 5$ or $9, y = 5$ or $9$ }
    
    english: "if $x, y$ are both in $S$, there exist an $n$ in $\N_1$ and a $m$ in $\N_0$ where $nx + my = z$ such that $z$ is in $S$, and $x$ and $y$ can equal 5 or 9."

- b) prove by structural induction

    - base cases
    
       -  $n = 1, m = 0, x = 5$
        
          $ n*x = 1*5 = 5 \in S$ and $\in R$ $\checkmark$

        -  $n = 1, m = 0, x = 9$
    
            $ n*x = 1*9 = 9 \in S$ and $\in R$ $\checkmark$

   - induction step
 
        - case 1: 
             Assume $n \in \N_0, m \in \N_1, m = (m + 1)^{th}$ generation, $ n = (n + 1)^{th}$ generation and $x$ and $y$ can equal 5 or 9 

            subcase 1: $nx + my = (n + 1)^{th}(5)+ (m + 1)^{th}(9) \in R$ and any sum of the multiples of 5 and 9 are in $S$. $\checkmark$

            subcase 2: $nx + my = (n + 1)^{th}(5)+ (m + 1)^{th}(5) \in R$ and any sum of multiples of 5 are in $S$. $\checkmark$

             subcase 3: $nx + my = (n + 1)^{th}(9)+ (m + 1)^{th}(9) \in R$ and any sum of multiples of 9 are in $S$. $\checkmark$

        - $S \subseteq R$ and $R \subseteq S$

---
---

### 7.5
Here is a simple recursive definition of the set $E$ of even integers:

Definition. Base case: $0 \in E$.

Constructor cases: If $n \in E$, then so are $n + 2$ and $-n$.

Provide similar simple recursive definitions of the following sets:

---
---
- a) $S ::=$ {$2^k 3^m 5^n \in \N | k, m ,n \in \N $}
    
    Definition. Base case: $1 \in \N$

    Constructor cases: If $ k, m, n \in \N^* $, then $2^{k+1} 3^{m+1} 5^{n+1} \in \N^*$

- b) $S ::=$ {$2^k 3^{2k+m} 5^{m+n} \in \N | k, m ,n \in \N $}
    
    Definition. Base case: $1 \in \N$
    
    Constructor cases: If $ k, m, n \in \N^* $, then $2^{k+1} 3^{2k+m+2} 5^{m+n+2} \in \N^* $

- c) $L ::=$ { $(a,b) \in \Z^2 | (a-b) $ is a multiple of 3 }
    
    Definition. Base case: $0 \in \Z^2$

    Constructor cases: If $a - b$ is a multiple of 3, then $(a+1)(b+1) \in \Z^2 $
    
- d) $L'$ is the recursive definition given in \(c)


---
---