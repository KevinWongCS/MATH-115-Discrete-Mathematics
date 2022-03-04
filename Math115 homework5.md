name: kevin wong\
filename: Math115 homework5\
date: 2/21/2022\
desc: https://courses.csail.mit.edu/6.042/spring18/mcs.pdf (Links to an external site.) please do these problems:  4.8, 4.9, 4.15, 4.19, 4.20

### 4.8

Let A, B and C be sets. Prove that

$A \bigcup B \bigcup C = (A - B) \bigcup (B - C) \bigcup (C - A) \bigcup (A \bigcap B \bigcap C))$

using a chain of IFF’s as Section 4.1.5.

---
---

$A \bigcup B \bigcup C = (A - B) \bigcup (B - C) \bigcup (C - A) \bigcup (A \bigcap B \bigcap C))$

converting minus signs to equivalent set expressions

iff $ \underline{ (A \bigcap \bar{B}) } $ $ \bigcup $ $\underline{ (B \bigcap \bar C) } $ $ \bigcup $ $\underline{ (C \bigcap \bar A) } $ $ \bigcup $ $ (A \bigcap B \bigcap C)) $

manipulating the right side, we get

iff $ (A \bigcap \bar{B}) $ $ \bigcup $ $ (B \bigcap \bar C) $ $ \bigcup $ $ (C \bigcap \bar A) $ $ \bigcup $ $ \underline{ ((A \bigcap B) \bigcup (B \bigcap C) \bigcup (C \bigcap A)) } $

iff $ (A \bigcap \bar{B}) $ $ \bigcup $ $ (B \bigcap \bar C) $ $ \bigcup $ $ (C \bigcap \bar A) $ $ \bigcup $ $ (A \bigcap B) $ $ \bigcup $ $ (B \bigcap C) $ $ \bigcup $ $ (C \bigcap A) $

Associative property to shuffle things around

iff $ (A \bigcap \bar{B}) $  $ \bigcup $ $ (A \bigcap B) $ $ \bigcup $ $ (B \bigcap \bar C) $ $ \bigcup $ $ (B \bigcap C) $ $ \bigcup $ $ (C \bigcap \bar A) $ $ \bigcup $ $ (C \bigcap A) $

Reverse distribute for $A, B, C$

iff $ (A \bigcap (\bar{B} \bigcup B)) $ $ \bigcup $ $ (B \bigcap (\bar C \bigcup C)) $ $ \bigcup $ $ (C \bigcap (\bar A \bigcup A)) $

Universe $ = set \bigcup \bar{set}$

iff $ (A \bigcap U ) $ $ \bigcup $ $ (B \bigcap U) $ $ \bigcup $ $ (C \bigcap U) $

Identity: $A \bigcap U = A$

$= A \bigcup B \bigcup C $

---
---

### 4.9
Union distributes over the intersection of two sets:

$ A \bigcup (B \bigcap C) = (A \bigcup B) \bigcap (A \bigcup C)$

Use (4.11) and the Well Ordering Principle to prove the Distributive Law of union over the intersection of n sets:

$ A \bigcup (B_1 \bigcap ... \bigcap B_{n-1} \bigcap B_n) = (A \bigcup B_1) \bigcap ...\bigcap (A \bigcup B_{n-1}) \bigcap (A \bigcap B_n) $

Extending formulas to an arbitrary number of terms is a common (if mundane)
application of the WOP.

---
---
Prove by contradiction/induction.

Let's say $P(n) \leftrightarrow Q(n)$

and let

$P(n) = A \bigcup (B_1 \bigcap ... \bigcap B_n)$ 

and 

$Q(n) = (A \bigcup B_1) \bigcap ...\bigcap (A \bigcap B_n) $

So the setup would be to assume $(B_1 \bigcap ... \bigcap B_n) \in P(n)$ and test $Q(n)$ to find a set (or sets) where $(B_1 \bigcap ... \bigcap B_n\bigcap ... \notin Q(n)$.

- Case 1: $P(0)$ case. Let a single set be represented as $B$. We'll say set $B \in P(n)$.
   
   Since $Q(n) = A \bigcup B$ 

   I would have to say $B \in Q(n)$
   
   so $B \in P(n) \bigcap Q(n)$

- Case 2: Lets $1$ to $n$ sets be represented by $B_1...B_n$ and $B_1...B_n \in P(n)$.

   Since $Q(n) = (A \bigcup B_1) \bigcap ...\bigcap (A \bigcap B_n) $.

   I would have to say $B_1...B_n \in Q(n)$

   so $B_1...B_n \in P(n) \bigcap Q(n)$

- Similar arguments follow if we assume $(B_1 \bigcap ... \bigcap B_n) \in Q(n)$ and tested $P(n)$ if the set(s) exist(s).

- Since I was unable to find a set that exist in $P(n)$ and not in $Q(n)$, I couldn't prove the contradiction. So the distibutive law is valid. 
---
---

### 4.15

a) Give a simple example where the following result fails, and briefly explain why:

False Theorem. For sets $A, B, C and D$, let

$L ::= (A \bigcup B) \times (C \bigcup D)$.

$R ::= (A \times C) \bigcup (B \times D)$.

Then $L = R$.

b) Identify the mistake in the following proof of the False Theorem.

*Bogus proof*. Since L and R are both sets of pairs, it’s sufficient to prove that

$(x, y) \in L \leftrightarrow (x,y) \in R$ for all $x,y$.

The proof will be a chain of iff implications: 

$(x,y) \in R$

iff $(x,y) \in (A \times C) \bigcup (B \times D)$

iff $(x,y) \in A \times C, or (x, y) \in B \times D$

iff $(x \in A$ and $y \in C)$ or else $ (x \in B $ and $ y \in D) $

iff either $x \in A$ or $x \in B$, and either $y \in C$ or $y \in D$

iff $x \in A \bigcup B$ and $y \in C \bigcup D$

iff $(x,y) \in L$.

c) Fix the proof to show that $R \subseteq L$.

---
---

- a) this proof is false because $L$ would have two times more combinations or products than $R$.

   For example if A, B, C and D have 2 elements each. $ L ::= (A \bigcup B) \times (C \bigcup D) $ would have 16 combinations total. $ R ::= (A \times C) \bigcup (B \times D) $ would have 8 combinations total.

- b) The step with "*iff either $x \in A$ or $x \in B$, and either $y \in C$ or $y \in D$*" is incorrect. Because this statement implies for $R$, $x$ can belong to $A$ or $B$ and $y$ can belong to either $C$ or $D$. But for $R$, if $x$ belongs to $A$ it has to belong to $C$ as well. So a combination such as $x \in A \bigcup B$ wouldn't be valid for $R$.

- c) $(x,y) \in R$

   iff $(x,y) \in (A \times C) \bigcup (B \times D)$

   iff $(x,y) \in A \times C, or (x, y) \in B \times D$

   iff $(x \in A$ and $y \in C)$ or else $ (x \in B $ and $ y \in D) $

   iff $(x \notin A$ and $y \notin C)$ or $(y \notin B$ and $ y \notin D)$

   iff $(x \in A$ and $y \in D)$ or $(y \in B$ and $ y \in C) $

   iff $x \in A \bigcup B$ and $y \in C \bigcup D$

   iff $(x,y) \subseteq L$

   $ \therefore R \subseteq L$.

---
---

### 4.19
For each of the following real-valued functions on the real numbers, indicate whether
it is a bijection, a surjection but not a bijection, an injection but not a bijection, or
neither an injection nor a surjection.

a) $ x \rightarrow x + 2$

b) $ x \rightarrow 2x$

c) $ x \rightarrow x^2$

d) $ x \rightarrow x^3$

e) $ x \rightarrow sin{(x)}$

f) $ x \rightarrow x sin{(x)}$

g) $ x \rightarrow e^x$

---
---
- a) bijective.

   $\forall x_1, x_2 \in \R: x \rightarrow x + 2$ 

   let $x_1$ and $x_2$ $\in$ $\R$ and $f(x_1) = f(x_2)$

   $x_1 + 2 = x_2 + 2$

   subtract $2$ from both sides

     $x_1 = x_2$

   $x_1$ has to equal $x_2$, this implies this function is injective. The function can continuously map an $x$ in its domain to the codomain through out $\R$, so by the intermediate value theorum the function is surjective as well.

    

- b) bijective.

   $\forall x_1, x_2 \in \R: x \rightarrow 2x$ 

   let $x_1$ and $x_2$ $\in$ $\R$ and $f(x_1) = f(x_2)$

   $2x_1= 2x_2$

   dividing $2$ on both sides

     $x_1 = x_2$

   $x_1$ has to equal $x_2$, this implies this function is injective. The function can continuously map an $x$ in its domain to the codomain through out $\R$, so by the intermediate value theorum the function is surjective as well.

- c) neither an injection nor a surjection.
    
   $\forall x_1, x_2 \in \R: x \rightarrow x^2$ 

    let $x_1$ and $x_2$ $\in$ $\R$ and $f(x_1) = f(x_2)$

   $(x_1)^2 = (x_2)^2$ 

   If $x_1 \ne x_2$ they can still map to the same element in the codomain, example -2 and 2 would both map to 4, so not injective. There also isn't mapping of an $f(x)$ to every $\R$ because $x^2$ is always positive, so not surjective.

- d) bijection.
   
   $\forall x_1, x_2 \in \R: x \rightarrow x^3$    

    let $x_1$ and $x_2$ $\in$ $\R$ and $f(x_1) = f(x_2)$

   if $x_1 \neq x_2$

   $(x_1)^3$ and $(x_2)^3$ would only be equal if $x_1 = x_2$, so this is injective.

  The function can continuously map an $x$ in its domain to the codomain through out $\R$, so by the intermediate value theorum the function is surjective as well.

- e) neither an injection nor a surjection.

   $\forall x_1, x_2 \in \R: x \rightarrow sin{(x)}$

    let $x_1$ and $x_2$ $\in$ $\R$ and $f(x_1) = f(x_2)$

    
   $sin{(x_1)} = sin{(x_2)}$

   This is not injective because multiple $x$ values can be mapped to $f(x)$. There isn't mapping of a $f(x)$ to every $\R$, so it is not surjective.

- f) surjection but not a bijection.
   
   the explanation is similar to e) but because of the multiplied by $x$, the function can span continuously to $\infty$ or -$\infty$, so by the intermediate value theorum, this function is surjective.

- g) injection but not a bijection.
   
   $\forall x_1, x_2 \in \R: x \rightarrow e^x$

    let $x_1$ and $x_2$ $\in$ $\R$ and $f(x_1) = f(x_2)$

   if $x_1 \neq x_2$, there is no combination $x_1$ and $x_2$ that can make $e^{x_1} = e^{x_2}$, therefore injective.

   if we take $e^x$ to $\infty$ or -$\infty$ there would not be a $e^x$ to map from $-\infty$ to $0$. So I would say it's not surjective.
---
---

### 4.20
Let $f : A \rightarrow B$ and $g : B \rightarrow C$ be functions and $h : A \rightarrow C$ be their composition, namely, $h(a) ::= g(f(a))$ for all $a \in A$.

a) Prove that if $f$ and $g$ are surjections, then so is $h$.

b) Prove that if $f$ and $g$ are bijections, then so is $h$.

c) If $f$ is a bijection, then so is $f^{-1}$.

---
---

- a) proof by deduction

   Assuming $f$ and $g$ are surjective, then $C$ is a subset of $B$ and $B$ is a subset of $A$. This implies $C$ would be a subset of $A$.

   so then $f \supseteq g \supseteq h$, which means $h$ has to be surjective as well.

- b) proof by deduction

    Assuming $f$ and $g$ are injective, a similar argument can be said compared to a). 
      
   let $x...x_n \in \R$ be in the set of $f : A \rightarrow B$ 
   
   and let $y...y_n \in \R$ be in the set of $g : B \rightarrow C$ 
   
   and let $z...z_n \in \R$ be in the set of $h : A \rightarrow C$ 

   if $f$ is in $\R$ and $g$ is in $\R$. Then $h$ would also have to be in $\R$.

- c) If $f$ is bijective $ \rightarrow f^{-1} $ is bijective. 

   let $\forall x, y \in \R: x \rightarrow f(x)$.

   $ f(x) = y $ and $ y \in \R $

   $ f^{-1}(y)=x $ and $  x \in \R $

   So the inverse function would just remap all $y$'s to $x$'s.


   example: $x \in \R: f(x)=x^3$

   let $x = 2n$, $n \in \R$

   $f(x) = (2n)^3$

   So $f^{-1} (x)= x^{\frac{1}{3}}$

   $((2n)^3)^{\frac{1}{3}} = (2n)^{\frac{3}{3}} = 2n$

   so we can say $(f^{-1}(f(x))) = x$, or a bijective functions inverse is bijective since it just undoes what the function did.

---
---