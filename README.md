name: kevin wong\
filename: Math115 homework1\
date: 1/24/2022\
desc: https://courses.csail.mit.edu/6.042/spring18/mcs.pdf (Links to an external site.) Please do these problems: 3.5, 3.14, 3.26, 3.27, 3.28. x/c 3.29, 3.31, 3.33

___
### 3.5

| P | Q | R | P -> Q | Q -> R | R -> P | P -> Q ^ Q -> R ^ R -> P | P ^ Q ^ R |
|---|---|---|  :---:   |   :---:  |  :---:   | :---: | :---: |
| T | T | T | T | T | T | T | T |
| T | T | F | T | F | T | F | F |
| T | F | F | F | T | T | F | F |
| T | F | T | F | T | T | F | F |
| F | F | F | T | T | T | T | F |
| F | F | T | T | T | F | F | F |
| F | T | T | T | T | F | F | F |
| F | T | F | T | F | T | F | F |

```
Sloppy Joe is incorrect when he concluded "all three of P, Q and R are true," 
because "P -> Q ^ Q -> R ^ R -> P" is also true when P, Q and R are all false.
```
___
### 3.14
Problem 3.14.
Prove by truth table that OR distributes over AND, namely,
P OR (Q AND R) is equivalent to (P OR Q) AND (P OR R) 

| P | Q | R | Q ^ R | P v Q | P v R | P v (Q ^ R) | (P v Q) ^ (P v R) |
|---|---|---| :---:|   :---:  |  :---:   | :---: | :---: |
| T | T | T | T     | T | T | T | T | 
| T | T | F | F     | T | T | T | T |
| T | F | F | F     | T | T | T | T |
| T | F | T | F     | T | T | T | T |
| F | F | F | F     | F | F | F | F |
| F | F | T | F     | F | T | F | F |
| F | T | T | T     | T | T | T | T |
| F | T | F | F     | T | F | F | F |

```
Base on the truth table we can conclude that "P v (Q ^ R)" ≡ "(P v Q) ^ (P v R)" 
```
___
### 3.26
For each of the following propositions:\
(i) ⱯxƎy.2x-y=0\
(ii) ⱯxƎy.x-2y=0\
(iii) Ɐx.x < 10 -> (Ɐy.y < x -> y < 9)\
(iv) ⱯxƎy.[y > x ^ Ǝz.y + z = 100]

indicate which propositions are False when the variables range over:

(a) the nonnegative integers(ℤ+)\
(b) the integers(ℤ)\
(c) the real numbers(ℝ)

* (i)\
   (a) True, ⱯxƎy ∈ ℤ+.2x-y=0\
   (b) True, ⱯxƎy ∈ ℤ.2x-y=0\
   (c) True, ⱯxƎy ∈ ℝ.2x-y=0
- (ii)\
   (a) False, ⱯxƎy ∈ ℤ+.x-2y=0\
   (b) False, ⱯxƎy ∈ ℤ.x-2y=0\
   (c) True, ⱯxƎy ∈ ℝ.x-2y=0
- (iii)\
   (a) True, ⱯxⱯy ∈ ℤ+.x < 10 -> y < x -> y < 9\
   (b) True, ⱯxⱯy ∈ ℤ.x < 10 -> y < x -> y < 9\
   (c) True, ⱯxƎy ∈ ℝ.x < 10 -> y < x -> y < 9
- (iv)\
   (a) False, ⱯxƎyƎz ∈ ℤ+.[y > x ^ y + z = 100]\
   (b) True, ⱯxƎyƎz ∈ ℤ.[y > x ^ y + z = 100]\
   (c) True, ⱯxƎyƎz ∈ ℝ.[y > x ^ y + z = 100]

___
### 3.27
Let Q(x, y) be the statement "x has been a contestant on television show y."

The domain of discourse for x is the set of all students at your school and for y is
the set of all quiz shows that have ever been on television.

Indicate which of the following expressions are logically equivalent to the sentence:
“No student at your school has ever been a contestant on a television quiz show.”

(a) ⱯxⱯy.¬(Q(x,y)) Yes\
(b) ƎxƎy.¬(Q(x,y)) No\
(c) ¬(ⱯxⱯy.Q(x,y)) No\
(d) ¬(ƎxƎy.Q(x,y)) No

___
### 3.28
Express each of the following statements using quantifiers, logical connectives,
and/or the following predicates

P(x): x is a monkey,\
Q(x): x is a 6.042 TA,\
R(x): x comes from the 23rd century,\
S(x): x likes to eat pizza\

where x ranges over all living things.

(a) No monkeys like to eat pizza\
Ɐx(P(x)¬S(x))

(b) Nobody from the 23rd century dislikes eating pizza.\
Ɐx(R(x)S(x))

(c) All 6.042 TAs are monkeys.\
Ɐx(Q(x) -> P(x))

(d) No 6.042 TA comes from the 23rd century.\
Ɐx(Q(x)¬R(x))

(e) Does part (d) follow logically from parts (a), (b), (c)? If so, give a proof. If not, give a counterexample.\
"d" doesn't conflict with a, b, or c.

(f) Translate into English: (Ɐx)(R(x) OR S(x) IMPLIES Q(x)).\
All living things come from the 23rd century or like to eat pizza are a 6.042 TA

(g) Translate into English: [Ǝx.R(x) AND NOT(Q(x))] IMPLIES Ɐx.(P(x) IMPLIES S(s)).\
If some living things from the 23rd century are not a 6.042 TA, then if they are all monkeys then they like eating pizza.

___
### 3.29

___
### 3.31

___
### 3.33
