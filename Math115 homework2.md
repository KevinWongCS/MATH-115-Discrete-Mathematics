name: kevin wong\
filename: Math115 homework2\
date: 1/27/2022\
desc: https://courses.csail.mit.edu/6.042/spring18/mcs.pdf (Links to an external site.) please do these problems:  1.3, 1.7, 1.8, 1.10. x/c: 1.1, 1.4, 1.5

___
### first problem
Please do this problem first: 1. Prove ¬P ∨ (R → ¬Q) ≡ ¬(P ⋀ Q ⋀ R) without using a truth table.

```
Proof by equivalence chains (Patterns of Proof)
¬P ∨ (R → ¬Q)
¬P ∨ (¬R ∨ ¬Q))    Logical equivalency R → Q ≡ ¬R ∨ Q
¬P ∨ ¬(R ⋀ Q))     De Morgan's 2nd law
¬(P ⋀ (R ⋀ Q))     De Morgan's 2nd law
¬(P ⋀ R ⋀ Q)       Associative law

Conclusion: ¬P ∨ (R → ¬Q) ≡ ¬(P ⋀ Q ⋀ R) is plausible
 
```

___
### 1.3
Identify exactly where the bugs are in each of the following bogus proofs.

(a) Bogus Claim: 1/8 > 1/4

Bogus proof:\
3 > 2\
3log<sub>10</sub>(1/2) > 2log<sub>10</sub>(1/2)\
log<sub>10</sub>(1/2)<sup>3</sup> > log<sub>10</sub>(1/2)<sup>2</sup>\
(1/2)<sup>3</sup> > (1/2)<sup>2</sup>

```
It is a mathematical rule to flip the inequality sign when you multiply or divide both sides by a negative number. 
log(1/2) is a negative number, so the inequality symbol ">" should have flipped to "<" in step 2.

Also the math manipulation in the last step I don't believe is correct.
```

(b) Bogus proof : 
1¢ = $0.01 = ($0.1)<sup>2</sup> = (10¢)<sup>2</sup> = 100¢ = $1: 
```
(10¢)^2 = (10¢)(10¢), this expression doesn't mean anything in terms of U.S currency. So saying (10¢)^2 = 100¢ doesn't hold.
```
(c) Bogus Claim: If a and b are two equal real numbers, then a = 0.

Bogus proof:\
a = b\
a<sup>2</sup> = ab\
a<sup>2</sup> - b<sup>2</sup> = ab - b<sup>2</sup>\
(a-b)(a+b) = (a-b)b\
a + b = b\
a = 0
```
if a = b then dividing both sides by (a-b) is dividing by zero. Which is done in step 4 and isn't defined. 
```

___
### 1.7
Prove by cases that\
max(r, s) + min(r, s) = r + s \
for all real numbers r, s.

```
Prove by cases
r, s ∈ ℝ
case 1: r = s:
    max(r, s) + min(r, s)
    r + r = s + s = r + s
case 2: r > s:
    max(r, s) + min(r, s)
    r + s
case 3: r < s:
    max(r, s) + min(r, s)
    s + r
    r + s     commutative law

Based on the cases considered we can conclude that ∀r, ∀s ∈ ℝ.max(r, s) + min(r, s) = r + s 
```

___
### 1.8
If we raise an irrational number to an irrational power, can the result be rational?
Show that it can by considering $\sqrt{2}$<sup>$\sqrt{2}$</sup> and arguing by cases. 

___
 Prove by cases\
case 1:

irrational_number <sup>irrational_number</sup> = irrational_number

$\sqrt{2}$<sup>$\sqrt{2}$</sup> = 1.6325 

The above concludes an irrational number to the power of an irrational power can result in an irrational number.

case 2: 

irrational_number <sup>irrational_number</sup> = rational_number

($\sqrt{2}$<sup>$\sqrt{2}$</sup>)<sup>$\sqrt{2}$</sup> = 2<sup>1/2 *  $\sqrt{2}$ * $\sqrt{2}$</sup> = 2<sup>1/2 * 2<sup>1/2</sup> * 2<sup>1/2</sup></sup> = 2<sup>1/2 * 2<sup>1/2 + 1/2</sup></sup> = 2<sup>1/2 * 2<sup>2/2</sup></sup> = 2<sup>1/2 * 2</sup> = 2<sup>2/2</sup> = 2

The above concludes an irrational number to the power of an irrational power can result in a rational number.
___

___
### 1.10
Hint: An odd number equals 2m + 1 for some integer m, so its square equals
4(m<sup>2</sup> + m) + 1.

(a) Suppose that

a + b + c = d

where a, b, c, d ∈ ℤ<sup>+</sup>

Let P be the assertion that d is even. Let W be the assertion that exactly one among
a, b, c are even, and let T be the assertion that all three are even.

Prove by cases that
P IFF [W OR T]

P ↔ W ∨ T
___
___
proof by cases
* case 1: P → W or P → T\
Let P be True\
This implies d is an even positive integer and some multiple of 2.\
Let d = 2x, where x ∈ ℤ<sup>+</sup>\
2x = a + b + c\
Conclusion: Based on the above equation we can conclude that either a + b + c are all even satisfying assertion T or either only one of a, b, or c is even satisfying W to solve to an even number.

* case 2: W → P\
Let W be True\
This implies only one of a, b, or c is even.\
Let a, b, c = 2x, 2y + 1, 2z + 1\
where x, y, z ∈ ℤ<sup>+</sup>\
2x + (2y + 1) + (2z + 1) = d\
2(x + y + z) + 2 = d\
Conclusion: Based on the above equation we know d is some multiple of 2 plus 2 which implies d is a positive integer satisfying assertion P.

* case 3: T → P\
T is True
T is True implies a, b, and c are all even.\
a + b + c = d\
let a, b, c = 2x, 2y, 2z\
where x, y, z ∈ ℤ<sup>+</sup>\
2x + 2y + 2z = 2m\
2(x + y + z) = 2m\
Conclusion: Based on the above equation I don't believe P → R is true.
___
___
(b) Now suppose that

w<sup>2</sup> + x<sup>2</sup> + y<sup>2</sup> = z<sup>2</sup>

where w, x, y, z ∈ ℤ<sup>+</sup>

Let P be the assertion that z is even, and
let R be the assertion that all three of w, x, y are even. 

Prove by cases that P IFF R\
P ↔ R
___
___
* case 1: P → R\
Proof by case\
Let P be true, so z is even\
Let z = 2x\
where x ∈ ℤ<sup>+</sup>\
so, we get\
2x = $\sqrt{w^2 + x^2 + y^2}$
   * case 1 subcase 1: w, x, y are all odd.\
By substituting the hint given in the problem we get\
2x = $\sqrt{4(w^2 + w) + 1 + 4(x^2 + x) + 1 + 4(y^2 + y) + 1}$\
2x = $\sqrt{4(w^2 + w) + 4(x^2 + x) + 4(y^2 + y) + 3}$\
Using the above equation we know $\sqrt{4(w^2 + w) + 4(x^2 + x) + 4(y^2 + y) + 3}$ won't always solve to a rational number.
   * case 1 subcase 2: w, x are odd and y is even.\
By substituting the hint given in the problem we get\
2x = $\sqrt{4(w^2 + w) + 1 + 4(x^2 + x) + 1 + (2y)^2}$\
2x = $\sqrt{(4w^2 + 4w) + (4x^2 + 4x) + (2y)^2 + 2}$\
2x = $\sqrt{(4w^2 + 4w) + (4x^2 + 4x) + 4y^2 + 2}$\
2x = $\sqrt{2(2w^2 + 2w + 2x^2 + 2x + 2y^2 + 1)}$\
2x = $\sqrt{2}$ $\sqrt{2w^2 + 2w + 2x^2 + 2x + 2y^2 + 1}$\
Using the above equation we know $\sqrt{2}$ is an irrational number so anything multiplied by it will not be a perfect number.

   * case 1 subcase 3: w is odd and x, y are even.\
By substituting the hint given in the problem we get\
2x = $\sqrt{4(w^2 + w) + 1 + (2x)^2 + (2y)^2}$\
2x = $\sqrt{4(w^2 + w) + (2x)^2 + (2y)^2  + 1}$\
Using the above equation we know $\sqrt{4(w^2 + w) + (2x)^2 + (2y)^2  + 1}$ won't always solve to a rational number.

    * case 1 subcase 4: w, x, y are all even.\
By substituting the hint given in the problem we get\
let 2w, 2x, 2y represent even numbers\
2x = $\sqrt{4w^2 + 4x^2 + 4y^2}$\
2x = $\sqrt{4(w^2 + x^2 + y^2)}$\
2x = $\sqrt{2}$ $\sqrt{4(w^2 + x^2 + y^2)}$\
Using the above equation we know $\sqrt{2}$ $\sqrt{4(w^2 + x^2 + y^2)}$ will not solve to a rational number.

    * Conclusion: Based on case 1, I wouldn't say P → R. 

* case 2: R → P\
Let R be true, so w, x, y are even.\
let w, x, y = 2x, 2y, 2z\
where w, x, y, z ∈ ℤ<sup>+</sup>\
2x<sup>2</sup> + 2y<sup>2</sup> + 2z<sup>2</sup> = z<sup>2</sup>\
2x = $\sqrt{(2w)^2 + (2x)^2 + (2y)^2}$\
2x = $\sqrt{4w^2 + 4x^2 + 4y^2}$\
2x = $\sqrt{4(w^2 + x^2 + y^2)}$\
2x = $\sqrt{4}$ * $\sqrt{w^2 + x^2 + y^2}$\
2x = 2 * $\sqrt{w^2 + x^2 + y^2}$\
Based on the equation above we can conclude that there does exist an w, x, y where R → P would be true. For example 2 * $\sqrt{4^2 + 4^2 + 2^2}$ would equal to 2 * 6 = 12. But it's not true in every case. 

** Based on my line of reasoning I would have to say P ↔ R isn't true in every case, but there does exist cases were it is true.
___
___
