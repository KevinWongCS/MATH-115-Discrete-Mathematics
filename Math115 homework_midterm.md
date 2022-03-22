name: kevin wong\
filename: Math115 Midterm\
date: 3/21/2022\
desc: 15 questions midterm review


---
---
### ***1***

State the definitions of the following concepts:

- a) proposition:

    A statement that is either true or false.

    - predicate: A preposition whose truth depends on the value of one or more variables
    
- b) rational number:
    
    The set of numbers that can be expressed as the ratio of two integers. Denominator cannot be divisible by zero.

    $S = \{ \frac{n}{m} | n, m \in \Z \}$
- c) even integer:

    A number that is divisble by 2.

    $S = \{ 2k | k \in \Z \}$

- d) odd integer:

    The set of integers that is not even.

    $S = \{ 2k+1 | k \in \Z \}$

- e) injective function:

    A function that maps distinct elements of the input set to distinct elements of the functions set.

    Often we here it expressed as "one to one" or "no two elements map to the same element in the functions set".

    $ \forall a_1, a_2 \in A, f(a_1) = f(a_2) \rightarrow a_1 = a_2 $

    note: passes the "vertical line test".

- f) surjective function:

    aka: onto function. When the whole set of the function is mapped to.

    $f: \R \rightarrow \R, f(x) = y$ has to cover all of $\R$

    Does not have to be "one to one".

    - Bijective: Both injective and surjective.
    
    note: you can draw the function without picking up your pencil or diverge to $-\infin$ and $\infin$.

- g) the union of two sets:

    Say there's two sets $A$ and $B$, the union of the two sets would be $A \bigcup B$.

    - The intersection would be $A \bigcap B$.
    - Other sets symbols: universe($U$) and empty set($\varnothing$)  
---
---

### ***2***
Two of the following three propositions are equivalent.  Which two?  Prove that they are equivalent using a truth table. $\urcorner(P \rightarrow Q), P \wedge \urcorner Q,(\urcorner P) \rightarrow \urcorner Q $.

| $P$  | $Q$  | $P \rightarrow Q$  | $\urcorner(P \rightarrow Q)$  | $P \wedge \urcorner Q$  | $(\urcorner P) \rightarrow \urcorner Q$  |
|---|---|---|---|---|---|
| T | T | T | F | F | T |
| T | F | F | T | T | T |
| F | T | T | F | F | F |
| F | F | T | F | F | T |

$\urcorner(P \rightarrow Q) \equiv P \wedge \urcorner Q$ $\checkmark$

---
---

### ***3***
Prove or disprove the following equivalences.

- a) $(P \rightarrow Q) \rightarrow R \equiv P \rightarrow (Q \rightarrow R)$

| $P$ | $Q$ | $R$ | $P \rightarrow Q$  | $(P \rightarrow Q) \rightarrow R$  | $Q \rightarrow R$  | $P \rightarrow (Q \rightarrow R)$ |
|:-:|:-:|:-:|:-:|:-:|:-:|---|
| T | T | T | T | T | T | T |
| T | T | F | T | F | F | F |
| T | F | T | F | T | T | T |
| T | F | F | F | T | T | T |
| F | T | T | T | T | T | T |
| F | T | F | F | F | F | T |
| F | F | T | F | T | T | T |
| F | F | F | T | F | T | T |

not equivalent "$(\urcorner \equiv)$"

$(P \rightarrow Q) \rightarrow R (\urcorner \equiv) P \rightarrow (Q \rightarrow R)$ $\checkmark$

- b) $(\urcorner P) \leftrightarrow (\urcorner Q) \equiv P \leftrightarrow Q$


| $P$ | $Q$ | $\urcorner P$  | $\urcorner Q$  | $  (\urcorner P) \leftrightarrow (\urcorner Q)$  | $P \leftrightarrow Q$  |
|:-:|:-:|:-:|:-:|:-:|:-:|
| T | T | F | F | T | T |
| T | F | F | T | F | F |
| F | T | T | F | F | F |
| F | F | T | T | T | T |


$(\urcorner P) \leftrightarrow (\urcorner Q) \equiv P \leftrightarrow Q$ $\checkmark$

---
---

### ***4***
Say $D_1$ is the domain of all students at CCSF, $D_2$ is the domain of all classes at CCSF. Say $T$ is a propositional function with domain $D_1$ x $D_2, T(x, y) := x$ has taken $y$. 

Express the negation of the following propositions in English. 

- a) $\forall x \in D_1, T(x,M115)$

    All students at CCSF have taken Math 115.

    negation: $\urcorner(\forall x \in D_1, T(x,M115))$

    Not all students have taken math 115.

- b) $\exist y \in D_2, \urcorner T(Felipe, y)$ 

    Felipe has not taken a class at CCSF.

    negation: $\urcorner (\exist y \in D_2, \urcorner T(Felipe, y))$

    Felipe has taken all classes at CCSF.

- c) $\forall x \in D_1, \exist y \in D_2, T(x,y)$

    All students at CCSF has at least taken one class at CCSF.

    negation: $\urcorner (\forall x \in D_1, \exist y \in D_2, T(x,y))$

    Not all students at CCSF have taken all classes at CCSF.

```
Statement 	                        Negation
----------------------------------------------------------
"A or B" 	                        "not A and not B"
"A and B" 	                        "not A or not B"
"if A, then B" 	                    "A and not B"
"For all x, A(x)"                   "There exist x such that not A(x)"
"There exists x such that A(x)" 	"For every x, not A(x)"

```
---
---

### ***5***
5. Prove or disprove the following claims.

- a) Given any two distinct integers there exists a rational number strictly between them. 

    Assume $a, b \in \Z$ and are not equal. You can just take the average of $a, b$ to produce a rational number between the 2 integers.

    $a, b \in \Z, \frac{a + b}{2} = RationalNumber$ 

- b) Given any two distinct integers there exists an irrational number strictly between them. 

    Assume $a, b \in \Z$ and $a < b$

    $0 < \frac{1}{\sqrt{2}} < 1$

    multiply all sides by $(b-a)$

    $(b-a)0 < (b-a) \frac{1}{\sqrt{2}} < (b-a)1$

    $0 < (b-a) \frac{1}{\sqrt{2}} < (b-a)1$

    add $a$ to both sides

    $a <  \frac{(b-a)}{\sqrt{2}} + a < b$

    Interpreting the expression in the middle, $ \frac{(b-a)}{\sqrt{2}}$ is an irrational number, and $a$ is a rational number. We know an irrational number plus an rational number is irrational. $\checkmark$

    note: a irrational number plus a irrational number can produce a rational number.

    $\pi + (1 - \pi) = 1$ $\checkmark$

- c) Given any two distinct irrational numbers there exists an integer strictly between them. 

    Using the equation from part b). 

    $a <  \frac{(b-a)}{\sqrt{2}} + a < b$ and $a, b \in \Z$ and $a < b$

    subtract $ \frac{(b-a)}{\sqrt{2}}$ from all sides.

    $a -  \frac{(b-a)}{\sqrt{2}} <  a < b -  \frac{(b-a)}{\sqrt{2}}$

    So we have a irrational number plus a rational, which is irrational, a rational number in the middle, and a irrational number plus a rational, which is irrational on the right side. 

    The problem with the equation is that if $a = 5$ and $b = 6$ we have:

    $5 - \frac{6 - 5}{\sqrt2} < integer < 6 - \frac{6 - 5}{\sqrt2}$

    $(5 - \frac{6 - 5}{\sqrt2}) - (6 - \frac{6 - 5}{\sqrt2}) = 1$

    The above we have the subtraction of two distinct irrational numbers and their difference is one. So this is a counter example to the claim because it can't just be any distinct irrational numbers. So I would have to conclude that the claim is invalid, but there are cases where it is true. $\checkmark$
    
---
---

### ***6*** 
Here are some sets contained in the universe $U =$ {$0, 1, 2, 3, 4, 5$}

$A = \{0, 5\}$

$B = \{2, 3, 4\}$

$C = \{1, 3, 5\}$

compute the following sets.

- a) $\overline{A \bigcup B}$ 

    $A \bigcup B = \{0, 2, 3, 4, 5\}$ 

    $\overline{A \bigcup B} = \{1\}$ 

- b) $(C-A) \bigcup (B-C)$ 

    $(C-A) \equiv (C \bigcap \overline{A}) = \{1, 3\}$

    $(B-C) \equiv (B \bigcap \overline{C}) = \{2, 4\}$

    $(C-A) \bigcup (B-C) = \{1, 2, 3, 4\}$ 

- c) $\overline{A} \bigcap B \bigcap \overline{C}$

    $\overline{A} = \{1, 2, 3, 4\}$

    $B = \{2, 3, 4\}$

    $\overline{C} = \{0, 2, 4\}$

    $\overline{A} \bigcap B \bigcap \overline{C} = \{2, 4\}$

---
---

### ***7***
Prove or disprove the following claims. In your arguments please rely on the definitions of $\bigcup, \bigcap, \subset$ and/or equality of sets.

- a) For all sets $A, B, C$ if $A \subseteq C$ and $B \subseteq C$, then $A \bigcup B \subseteq C$.
    
    - case 1:

        Suppose $x \in A$

        Because $x$ is in $A$ and $A$ is a subset of $C$ 

        We can conclude:

        $A$ or $B$ is a subset of $C$, aka $A \bigcup B \subseteq C$ $\checkmark$
    
    - case 2:
    
        Suppose $x \in B$

        Because $x$ is in $C$ and $B$ is a subset of $C$

        We can conclude that $B$ or $A$ is a subset of $C$.

        aka $B \bigcup A \subseteq C \equiv A \bigcup B \subseteq C$ $\checkmark$

    - case 3:
    
        Suppose $x \in A,B$
    
        Then just a combination of case 1 and 2. $\checkmark$

- b) For all sets $A, B, C$, if $A \bigcup C \subseteq B \bigcup C$, then $A \subseteq B$.

    - case 1: 
    
        Suppose $x \in A, x \notin B, x \notin C$
        
        $A \notin B$

        so  $A \nsubseteq B$ $\checkmark$

    - case 2:
    
        Suppose $x \in C, x \notin A, x \notin B$

        We know $x$ is in $C$, but $x$ isn't in $A$ or $B$.

        $x \notin A,B$

        so  $A \nsubseteq B$ $\checkmark$

    - case 3:
    
        Suppose $x \in A, x \in B, x \notin C$

        In this case because $x$ is in $A$ and $B$ we can conclude:

        $A \subseteq B$

    - conclusion, we can conclude there exist a possibility such that $A$ is a subset of $B$, where $x$ is in both $A$ and $B$, but this claim is invalid. $\checkmark$
    
        $\exist x : A \subseteq B | x \in A, x \in B$

        - example:

            $A = \{1\}$, $B = \{2\}$, $C = \{1, 3\}$
    
            $A \bigcup C = \{1, 3\}$, $B \bigcup C = \{1, 2, 3\}$
    
            $A \bigcup C \subseteq B \bigcup C$
    
            and $A \nsubseteq B$

c) If you have two sets $A$ and $B$, then $A \bigcup B = B$ *iff* $A \bigcap B = A$

- case 1:

    expression on left side of *iff*

    suppose $x$ in $A$, $x \in A$

    So $x$ is in $A$ or $B$, $A \bigcup B$

    Using our assumption $A$ or $B$ is $B$, $A \bigcup B = B$

    Then $A$ is a subset of $B$, $A \subseteq B$

    aka, all $x$ are in $B$, $x \in B$

    So, $A$ and $B$ is just $A$, $A \bigcap B = A$ $\checkmark$

- case 2: 

    expression on right side of *iff*

    Suppose $x$ in $A$, $x \in A$

    and $x$ in $A$ and $B$, $x \in A \bigcap B$

    Using our assumption $A$ and $B$ equals $A$, $A \bigcap B = A$

    then $A$ is a subset of $B$, $A \subseteq B$

    So, $A$ or $B$ is just $B$, $A \bigcup B = B$ $\checkmark$

- Conclusion the *iff* or $\leftrightarrow$ goes both ways in this preposition making this claim valid. $\checkmark$

    - example:

        $A = \{1\}, B = \{1, 2\}$

        $A \bigcup B = B$ and $A \bigcap B = A$ 

---
---

### ***8***
Use induction to prove that $n^2$ equals the sum of the first n positive odd integers. In other words $1 + 3 +...+(2n - 1) = n^2$ for all integers $n \geq 1$.

Prove by weak induction:

- base case: n = 1
    
    $1^2 = 1$ $\checkmark$

- inductive step: 
    
    Inductive hypothesis: Assume $n^2$ equals the sum of the first n positive odd integers or the equation above.

    Prove if $k^2 = 1 + 3 +...+(2k - 1), k \geq 1$ 

    then $(k + 1)^2 = 1 + 3 +...+(2(k + 1) - 1), k \geq 1$

    $= 1 + 3 +...+(2k + 1)$

    $(2k + 1)$ is the next odd number in sequence. $\checkmark$

---
---

### ***9***
Suppose $a_0 = 1, a_1 = 2, a_{n+2} = 5a_{n+1} - 6a_n$ for $n \in \N$

- a) compute $a_2, a_3, a_4, a_5$.

    $a_{0 + 2} = 5a_{0 + 1} - 6a_0$

    $= 10 - 6 = 4$

    - $a_2 = 4$

    $a_{1 + 2} = 5a_{1 + 1} - 6a_1$

    $= 20 - 12 = 8$

    - $a_3 = 8$

    $a_{2 + 2} = 5a_{2 + 1} - 6a_2$

    $= 40 - 24 = 8$

    - $a_4 = 16$
    
    $a_{3 + 2} = 5a_{3 + 1} - 6a_3$

    $= 80 - 48 = 32$

    - $a_5 = 32$

- b) Do you see a pattern in part a)? Maybe a hypothesis about $a_n$, then prove it using induction.

    After trial and error, I'm guessing $f(n) = 2^n$.

    - Prove by weak induction
    
    - Base case: 

        $2^0 = 1$ $\checkmark$

        $2^1 = 2$ $\checkmark$

    - inductive step:
    
        Assume if $f(k)  = 2^k$ is the function we are looking. Prove $k + 1$, $f(k + 1) = 2^{k+1} = 2^k * 2^1$

        $f(3 + 1) = 2^3 * 2 = 16$ $\checkmark$

        $f(4 + 1) = 2^4 * 2 = 32$ $\checkmark$

        - It appears $f(n) = 2^n$ can produce the same number pattern as the recursively defined set above.

---
---

### ***10***
The 2-3-averaged numbers($N23$) are a subset of real-number interval $[0, 1]$ defined as follows:

Base case: $0 \in N23, 1 \in N23$

Recursive case: if $x \in N23$ and $y \in N23$, then $\frac{2x + 3y}{5} \in N23$

- 10a) Use induction to show that $(\frac{3}{5})^n \in N23$ for all $n \in \N$.

    prove using weak induction 

    - base case: 
        
        $(\frac{3}{5})^0 = 1$ and $1 \in \N$ $\checkmark$

    - inductive step:

        Assume if $f(k) = (\frac{3}{5})^k \in N23$ for all $k \in \N$. Prove $f(k + 1) \in N23$.

        $f(k + 1) = (\frac{3}{5})^{k+1}$

        $= (\frac{3}{5})^k * (\frac{3}{5})^1$

        This is equivalent to or share the same form as:

        $\frac{2x + 3y}{5} = \frac{2x}{5} + \frac{3y}{5}$, where $x = 0$ 


        or $(rational <= 1)^2 \in [0, 1] \in N23$ $\checkmark$ 


- 10b) Use structural induction to show that 

    $\forall x, y \in [0, 1]$ if $x \in N23$ and $y \in N23$, then $xy \in N23$.

    Prove using structural induction

    - base case: $x = 0, y = 0$ $\checkmark$
    - inductive step: Assume if $y, x \in N23$ then $xy \in N23$. Prove that immediate and future descendants are also in $N23$.
    
        - case 1:

            Assume (or suppose) $y \in N23, x = 0$

            $y * 0 = 0$ and $0 \in N23$ $\checkmark$       

        - case 2:

            Assume $y \in N23, x = 1$

            $y * 1 = y$ and $y \in N23$ $\checkmark$       

        - case 3:
        
            Assume $y \in N23, x = y$

            $y * x = x^2 = y^2$ and $x^2, y^2 \in [0, 1] \in N23$ $\checkmark$

        - case 4:
        
            Assume $y \in N23, x > y$ or $x < y$

            $y * x$ and $(rational <= 1) * (rational <= 1) \in [0, 1] \in N23$ $\checkmark$

    - ~~Conclusion: The claim is true. $\checkmark$~~
    - note: instructor said we can't find $\frac{1}{2}$, therefore the claim should be false. $\checkmark$

---
---

### ***11***
One of the following functions is not a bijection.  Which one and why not?

- i) $f : R \rightarrow [1, \infin), f(x) = e^x + e^{-x}$

    - injective?
    
        if injective then $\forall x \in R, \forall y \in [1, \infin), f(x) = f(y) \rightarrow x = y$
    
        counter example:
        
        $x = 1, e^{1} + e^{-1} = 3.08616126963 $
    
        $y = -1, e^{-1} + e^{-(-1)} = 3.08616126963 $
        
        - conclusion: not injective, so not bijective. $\checkmark$
    
    - note: The surjective proof leads to an equation that is difficult to solve, requiring the quadratic formula.
    - also, you can argue, since my counter example is irrational, you won't know for sure how equal they are.

- ii) $g: [-2, 0] \rightarrow [0, 16], g(x) = x^4$

    - injective?

        if injective then $\forall x \in [-2, 0], \forall y \in [0, 16], f(x) = f(y) \rightarrow x = y$
    
        yes, if $[0, 16]$ is interpreted as a set of only 0 and 16.  $\checkmark$ 
    
        no, if $[0, 16]$ is interpreted as a range of 0 through 16, because $(-2)^4 = (2)^4 = 16$.  $\checkmark$ 

    - surjective?

        $f(x) = x^4$
    
        $x^4 = y$
    
        $x = \sqrt[4]{y}$
    
        $f(\sqrt[4]{y}) = (\sqrt[4]{y})^4 = y$ 

        So surjective. $\checkmark$ 

    - possible bijection, depending on how the injective case is interpreted.

- iii) $[0, \pi] \rightarrow [-1, 1], h(x) = cos(x)$

    - injective?
    
        if injective then $\forall x \in [0, \pi], \forall y \in [-1, 1], f(x) = f(y) \rightarrow x = y$

        This is true because of the cropped range of $h$.  $\checkmark$

    - surjective?
        
        $cos(x) = y$

        $x = cos^{-1}(y)$

        $f(cos^{-1}(y)) = cos(cos^{-1}(y)) = y$ 

        So injective. $\checkmark$

---
---

### ***12***
$p: R \rightarrow R, p(x) = 2x + 3$.

Prove that $p$ is a bijection.  Be sure to use definitions of injection and surjection in your proof. 

- prove injective:
    
    $\forall x,y \in R, f(x) = f(y) \rightarrow x = y$

    This is a linear function in $R$, so it is one to one. $\checkmark$
    
- prove surjective:

    $y = 2x + 3$

    $x = \frac{y - 3}{2}$

    $f(\frac{y - 3}{2}) = 2(\frac{y - 3}{2}) + 3$

    $= (\frac{2y - 6}{2}) + 3$

    $= (\frac{2y - 6}{2}) + \frac{3*2}{2}$

    $= (\frac{2y - 6 + 6}{2})$

    $= (\frac{2y}{2})$

    $f(x) = y$ 

    So surjective. $\checkmark$

    note: the above is basically the inverse.

    - note: we can also appeal to the intermediate value theorum(IVT) in this case because it's a continuous function and it diverges to $(-\infin, \infin)$ for $x$ in $R$. aka:

        $\forall x, y \in R | p(x) = y$

- conclusion: bijective $\checkmark$


---
---

### ***13***
Prove or disprove the following claims.

- a) If $f: R \rightarrow R$ is a function which satisfies $f(x) > x^2$ for all $x \in R$ then $f$ is injective.

    What if $f(x)$ is a straight line, but it won't always be greater than $x^2$, eventually $x^2$ will be larger than an equation of a line.

    - I believe any function greater than $x^2$ would have to have a similar shape, so that means it wouldn't pass the horizontal line test, meaning its not injective. $\checkmark$

- b) For all functions $f: A \rightarrow B$ and $g: B \rightarrow C$, if the composition $h = g \circ f: A \rightarrow C$ is injective, then $f$ is injective.

    Definition of composition:

    $h \circ f \equiv g(f(a)) = c$, where $a \in A, b \in B, c \in C$.

    - Proof: 

        - Assume if $h = g \circ f: A \rightarrow C$ is injective then prove $f$ is injective.

        - If $h$ is injective then $g(f(a))$ is injective, *definition of composition*

        - $\forall a_1,a_2 \in A, g(f(a_1)) = g(f(a_2)) \rightarrow a_1 = a_2$ is injective, *proof for injectivity*

         - So if $a_1 \neq a_2$ and map to the same $c$ in codomain $C$ then that goes against our assumption, therefore $f$ is injective.

       - conclusion: claim is valid. $\checkmark$

```
h: A -> C    not injective
f: A -> B    not injective
g: B -> C    injective

    f        g       
A   ->   B   ->   C
o ------ o ------ o

o ------ o ------ o
 /-------^
o        o        o

o ------ o ------ o

o ------ o ------ o

The above is an example of 2 elements from A mapping
to a single element in C, meaning not injective for
h: A -> C
```

- c) For all functions $f: A \rightarrow B$ and $g: B \rightarrow C$, if the composition $h = g \circ f: A \rightarrow C$ is injective, then $g$ is injective.

    - Proof: 
        
        piggy backing on part b), $g$ does need to be injective when mapping domain $B$ to codomain $C$. If two not equal $b$ elements map to the same $c$, this is equivalent to two not equal $a$ elements being mapped to the same $c$.

        $b_1 \neq b_2 \rightarrow_{map} c$ | $b_1, b_2 \in B, c \in C$
        
        $\equiv$        

        $a_1 \neq a_2 \rightarrow_{map} c$ | $a_1, a_2 \in A, c \in C$

    - conclusion: claim is valid. $\checkmark$

```
h: A -> C    not injective
f: A -> B    injective
g: B -> C    not injective

    f        g       
A   ->   B   ->   C
o ------ o ------ o

o ------ o ------ o
          /-------^
o ------ o        o

o ------ o ------ o

o ------ o ------ o

The above is an example of 2 elements from B mapping 
to a single element from C, which makes it two
A's mapping to a single C element, meaning not
injective h: A -> C
```
---
---

### ***14***
What is wrong with this proof.

Claim: $f: R \rightarrow R, f(x) = x^2$ is bijective.

Proof:

Using the function $g(x) = \sqrt x$ we see that if $f(x_1) = f(x_2)$, then $x_1^2 = x_2^2$ then

$x_1 = \sqrt{x_1^2} = \sqrt{x_2^2} = x_2$,

so $f$ is injective.

Also, if $y \in R$, then using $x = \sqrt{y}$ gives that $f(x) = (\sqrt{y})^2 = y$, so $f$ is surjective.

- Why the claim is not true:
    
    example:

    $x_1 = 1, -1 = \sqrt{x_1^2}$

    and

    $x_2 = 1, -1 = \sqrt{x_2^2}$

    $1 \neq -1$

- $f(x_1) = f(x_2) \rightarrow x_1 = x_2$. This isn't true because multiple values of $x$ can map to the same element in the codomain.

- I think the surjective part is questionable. The claim is $f: R \rightarrow R$, but the $f(x) = x^2$ only covers $[0, \infin)$. So this function is not surjective. $\checkmark$

---
---

### ***15***
What, if anything, is wrong with this proof? 

Claim: $A \bigcup (B_1 \bigcap B_2 \bigcap...\bigcap B_n) = (A \bigcup B_1) \bigcap (A \bigcup B_2) \bigcap...\bigcap (A \bigcup B_n)$

for all sets $A, B_1, B_2,..., B_n$ for all $n \in \N$.

Proof(induction on $n$):

Base Case: $n = 0$.

In this case there aren’t any sets $B_i$, both sides of the equation are equal to $A$, so the equation is true. 

Inductive Step: Suppose the claim is true when $n = k$ for some integer $k \ge 0$.

Then

$A \bigcup (B_1 \bigcap B_2 \bigcap...\bigcap B_{k+1})$

$= A \bigcup ((B_1 \bigcap B_2 \bigcap...\bigcap B_k) \bigcap B_{k+1})$

$= A \bigcup (B_1 \bigcap B_2 \bigcap...\bigcap B_k) \bigcap (A \bigcup B_{k+1}))$

$= ((A \bigcup B_1) \bigcap (A \bigcup B_2) \bigcap...\bigcap (A \bigcup B_k)) \bigcap (A \bigcap B_{K+1})$

$= (A \bigcup B_1) \bigcap (A \bigcup B_2) \bigcap...\bigcap (A \bigcup B_k) \bigcap (A \bigcap B_{K+1})$

By induction the claim is true for all $n \in \N$.

- Claim: I believe you need at least 2 base cases in order to do the inductive step. Or else we just have $A \bigcup \varnothing$. And we can't prove the claim with only $A$. 

---
---
*END*

---
---