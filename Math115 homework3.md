name: kevin wong\
filename: Math115 homework3\
date: 2/5/2022\
desc: https://courses.csail.mit.edu/6.042/spring18/mcs.pdf (Links to an external site.) please do these problems:  1.12, 1.13, 1.15, 1.17

___
### 1.12
Prove that for any $\ n \gt 0 $, if $\ a^{n}$ is even, then $\ a$ is even.

___
___
Prove by contradiction

There exist a positive $\ a$ where $\ a^{n}$ is even and $\ a$ is odd.

We know that any odd number to the power of any positive integer will be odd. 

If we substitute (2m + 1) to represent an odd number, where "m" is in the same domain as "n". Upon expanding the any $\ (2m + 1)^{n}$ we are always left with a odd number.

This is an invalid contradiction meaning the preposition is true.

___
___

___
### 1.13
Prove that if $\ a*b = n$, then either $\ a $ or $\ b$ must be $\le$ $\sqrt{n}$, where a, b, and n are non-negative real numbers.

___
___
Prove by contradiction

There exist an $\ a * b =n$ where $a \gt \sqrt{n}$ and $b \gt \sqrt{n}$

so there exist a $\ a \gt \sqrt{n}$ and $\ b \gt \sqrt{n}$

or so there exist a $\ a^{2} \gt n$ and $\ b^{2} \gt n$

then set $\ a^{2} \gt n = a*b$ 
and $\ b^{2} \gt n = a*b$ 

The product of two non-negative real numbers real numbers is always larger than its factors. So if $\ a$ is set to a larger number, $\ b$ has to become smaller to satisfy the equation. There is no combination where $\ a$ and $\ b$ can be large enough to make both equations true. 

So, I'm concluding the contradiction is invalid meaning the initial preposition is valid.
___
___

### 1.15
Give an example of two distinct positive integers m, n such that $\ n^{2}$ is a multiple of m, but n is not a multiple of m. How about have m be less than n?
___
___
example 1

$\ n = 6 $ and $\ m = 9 $, $\ n^{2} = 36 $

$\ n^{2} $ is multiple of m, but n is not a multiple of m. 

example 2

$\ n = 6 $ and $\ m = 4 $, $\ n^{2} = 36 $

$\ n^{2} $ is multiple of m, n is not a multiple of m, and $\ m \lt n$ 
___
___

### 1.17
Prove that $\ log_4{6} $ is irrational.
___
___

prove by contradiction 

There exist $\ log_4{6} $ is rational

let m/n be represent a rational number where m and n are integers

we'll set $\ log_4{6} = \frac{m}{n}$

raise both sides by 4, $\ 4^{log_4{6}} = 4^{\frac{m}{n}}$

we end up with $\ 6 = 4^{\frac{m}{n}}$

square root both sides by n, $\ 6^{n} = 4^{m}$

divide both sides by $\ 2^{n}$, $\ 3^{n} = 2^{m}$

We know that an odd number to the power of any integer is an odd and an even number to the power of any integer is an even so the contradiction is not valid meaning the preposition is valid.
___
___

### Boolean Function problem
| X | Y | Z | G |
|---|---|---|---|
| 1 | 1 | 1 | 0 |
| 1 | 1 | 0 | 1 |
| 1 | 0 | 1 | 0 |
| 1 | 0 | 0 | 1 | 
| 0 | 1 | 1 | 1 | 
| 0 | 1 | 0 | 0 | 
| 0 | 0 | 1 | 1 | 
| 0 | 0 | 0 | 0 | 

a) Find the sum-of-products and product-of-sums expansion for this Boolean Function G(x,y,z).
___
___
sum of products expansion

$\ G(x,y,z) = xy\overline{z} + x\overline{y} \overline{z} + \overline{x}yz + \overline{x}\overline{y}z $

product of sums expansion

$\ G(x,y,z) = (\overline{x} + \overline{y} + \overline{z}) * (\overline{x} + y + \overline{z}) * (x + \overline{y} + z) * (x + y + z) $
___
___
