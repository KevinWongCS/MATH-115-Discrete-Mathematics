name: kevin wong\
filename: Math115 homework5\
date: 2/21/2022\
desc: https://courses.csail.mit.edu/6.042/spring18/mcs.pdf (Links to an external site.) please do these problems:  4.8, 4.9, 4.15, 4.19, 4.20

### 4.8

---
---
OMG
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

The well ordered principle(WOP) says that for every non-empty set of $\N$, it has a smallest element.

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

- a) this proof is false because $L$ would have two times more combinations than $R$. 

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
- b) bijective.
- c) surjective and not bijective.

   if $x_1 = 2$ and $x_2 = -2$

   $x_1 \neq x_2$

   but $f(x_1) = f(x_2) = 4$, so not injective, but there is mapping of an x to every $f(x)$, so surjective.

- d) bijective.
   
   if $x_1 \neq x_2$

   if $(x_1)^3$ and $(x_2)^3$ would only be equal if $x_1 = x_2$, so this is injective.

   there is also mapping of an $x$ to every $f(x) = x^3$, so surjective.

- e) surjective and not bijective.

   there is mapping of an x to every $f(x)$, but not injective because multiple $x$ values can be mapped to $f(x)$.
- f) surjective and not bijective.
   
   the explanation is similar to e).

- g) bijective.
   
   if $x_1 \neq x_2$

   There is no combination of $x_1 \neq x_2$ that would make $e^{x_1} = e^{x_2}$, so injective.

   if we take $e^x$ to $\infty$ or -$\infty$ there would be an $x$ to map to $e^x$, so I would say it's surjective.
---
---

### 4.20
Let $f : A \rightarrow B$ and $g : B \rightarrow C$ be functions and $h : A \rightarrow C$ be their composition, namely, $h(a) ::= g(f(a))$ for all $a \in A$.

a) Prove that if $f$ and $g$ are surjections, then so is $h$.

b) Prove that if $f$ and $g$ are bijections, then so is $h$.

c) If $f$ is a bijection, then so is $f^{-1}$.

---
---
---
---