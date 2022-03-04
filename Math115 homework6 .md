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

- prove $f(n) = p(n) = (n-1)^2$

    prove by weak induction

    - base case $ n \in \N $ and $n=1,2,3,4,5$ for $p(n)$
    
    $p(1) = (1 - 1)^2 = 0$ $\checkmark$ 
   
    $p(2) = (2 - 1)^2 = 1$ $\checkmark$  

    $p(3) = (3 - 1)^2 = 4$ $\checkmark$ 

    $p(4) = (4 - 1)^2 = 9$ $\checkmark$

    $p(5) = (5 - 1)^2 = 16$ $\checkmark$

    so for $n=1,2,3,4,5$, $p(n) = f(n)$ in each case.

    - inductive step
    
    *inductive hypothesis*: $k \in \N$ and $k \ge 5$ and $p(k) = (k - 1)^2 $. If $ p(k) \rightarrow p(k + 1) \in \N $

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

    so $p(k + 1) = p(n) + 2k - 1 = f(k + 1)$ in the recursive case $ \checkmark$


---
---

### \#2
