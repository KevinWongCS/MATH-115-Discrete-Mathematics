name: kevin wong\
filename: Math115 homework8\
date: 04/12/2022\
desc: https://courses.csail.mit.edu/6.042/spring18/mcs.pdf (Links to an external site.) please do these problems: 12.6, 12.7, 12.8, 12.10, additional problem

### 12.6

For each of the following pairs of simple graphs, either define an isomorphism between them, or prove that there is none. (We write $ab$ as shorthand for $(a — b)$.)

- (a)
    
    $G_1$ with $V_1 = \{1, 2, 3, 4, 5, 6\}, E_1 = \{12, 23, 34, 14, 15, 35, 45\}$

    $G_2$ with $V_2 = \{1, 2, 3, 4, 5, 6\}, E_2 = \{12, 23, 34, 45, 51, 24, 25\}$


```
G_1
           ___________
          |     _____ |
          |    |     ||
1----2----3----4-----5      6
||_____________|     |
|____________________|

1 degree is 3
2 degree is 2
3 degree is 3
4 degree is 4
5 degree is 4
6 degree is 0


G_2
    
      ______________
     | ________     |
     ||        |    |
1----2----3----4----5       6
|                   |
|___________________|

1 degree is 2
2 degree is 4
3 degree is 2
4 degree is 3
5 degree is 3
6 degree is 0
```

The pair of simples graphs above aren't isomorphic because they don't share equal number of vertices with the same degree. $\checkmark$

- (b)

    $G_3$ with $V_3 = \{1, 2, 3, 4, 5, 6\}, E_3 = \{12, 23, 34, 14, 45, 56, 26\}$

    $G_4$ with $V_4 = \{a, b, c, d, e, f\}, E_4 = \{ab, bc, cd, de, ae, ef, cf\}$

```
G_3
      ___________________
     |                   |
1----2----3----4----5----6
|______________|

1 degree is 2
2 degree is 3
3 degree is 2
4 degree is 3
5 degree is 2
6 degree is 2

G_4
 ___________________
|                   |
a----b----c----d----e----f
          |______________|

a degree is 2
b degree is 2
c degree is 3
d degree is 2
e degree is 3
f degree is 2

note: G_4 looks like a mirror image of G_3 

```

$f_3: V_{G_3} \rightarrow  V_{G_4}$ $f = {(1, f),(2, e),(3, d),(4, c),(5, b),(6, a)}$

Adjacencies matrix for $G_3$
| $G_3$: | 1 | 2 | 3 | 4 | 5 | 6 |
|--------|---|---|---|---|---|---|
| 1      | 0 | 1 | 0 | 1 | 0 | 0 |
| 2      | 1 | 0 | 1 | 0 | 0 | 1 |
| 3      | 0 | 1 | 0 | 1 | 0 | 0 |
| 4      | 1 | 0 | 1 | 0 | 1 | 0 |
| 5      | 0 | 0 | 0 | 1 | 0 | 1 |
| 6      | 0 | 1 | 0 | 0 | 1 | 0 |

Adjacencies matrix for $G_4$ (doesn't match $G_3$)
| $G_4$: | a | b | c | d | e | f |
|--------|---|---|---|---|---|---|
| a      | 0 | 1 | 0 | 0 | 1 | 0 |
| b      | 1 | 0 | 1 | 0 | 0 | 0 |
| c      | 0 | 1 | 0 | 1 | 0 | 1 |
| d      | 0 | 0 | 1 | 0 | 1 | 0 |
| e      | 1 | 0 | 0 | 1 | 0 | 1 |
| f      | 0 | 0 | 1 | 0 | 1 | 0 |

Adjacencies matrix for $f_3(G3)$ (matches $G_3$)
| $f_3(G_3)$: | f | e | d | c | b | a |
|------------|---|---|---|---|---|---|
| f          | 0 | 1 | 0 | 1 | 0 | 0 |
| e          | 1 | 0 | 1 | 0 | 0 | 1 |
| d          | 0 | 1 | 0 | 1 | 0 | 0 |
| c          | 1 | 0 | 1 | 0 | 1 | 0 |
| b          | 0 | 0 | 0 | 1 | 0 | 1 |
| a          | 0 | 1 | 0 | 0 | 1 | 0 |

$f_3$ respects the number of vertices, edges, degree of vertex, adjacency, and cycles of a particular length, so it is an isomorphic pair of graphs. $\checkmark$

### 12.7

List all the isomorphisms between the two graphs given in Figure 12.23. Explain why there are no others.


```
     1
    / \   
   /   \
  /     \
 /       \
/         \
3----2----4
|         |
|         |
5---------6

1 degree is 2
2 degree is 2
3 degree is 3
4 degree is 3
5 degree is 2
6 degree is 2

     a
    / \   
   /   \
  /     \
 /       \
/         \
c----b----d
|         |
|         |
e---------f

a degree is 2
b degree is 2
c degree is 3
d degree is 3
e degree is 2
f degree is 2

Figure 12.23
```

$f_1$ $f = {(1, a),(2, b),(3, c),(4, d),(5, e),(6, f)}$

swapped $a \leftrightarrow b$:$\checkmark$

$f_2$ $f = {(1, b),(2, a),(3, c),(4, d),(5, e),(6, f)}$

swapped $c \leftrightarrow d$, $e \leftrightarrow f$:$\checkmark$

$f_3$ $f = {(1, a),(2, b),(3, d),(4, c),(5, f),(6, e)}$

swapped $a \leftrightarrow b$, $c \leftrightarrow d$, $e \leftrightarrow f$:$\checkmark$

    
$f_4$ $f = {(1, b),(2, a),(3, d),(4, c),(5, f),(6, e)}$

- Below are a few that aren't isomorphisms:

    ~~swapped $a \leftrightarrow b$, $c \leftrightarrow d$:~~
    
    $f_5$ $f = {(1, b),(2, a),(3, d),(4, c),(5, e),(6, f)}$
    
    ~~swapped $a \leftrightarrow b$, $e \leftrightarrow f$:~~
    
    $f_6$ $f = {(1, b),(2, a),(3, c),(4, d),(5, f),(6, e)}$
    
    ~~swapped $c \leftrightarrow d$:~~
    
    $f_7$ $f = {(1, a),(2, b),(3, d),(4, c),(5, e),(6, f)}$
    
    ~~swapped $e \leftrightarrow f$:~~
    
    $f_8$ $f = {(1, a),(2, b),(3, c),(4, d),(5, f),(6, e)}$

It seems the reason the two graphs only have the isomorphisms above is because of their symmetry along $(1, 2)$ or $(a, b)$. Imagine a line crossing $(1, 2)$ and $(a, b)$. The only "mappings" that allow are those that "mirror one side to the other". For example $(3, 5)$ can be mapped to $(d,f)$ and $(4, 6)$ can be mapped to $(c, e)$. Also $(a, b)$ exists on the center line, so its properties are preserved. This might be a preserved invariant argument or a path argument, but I currently can figure it out.

### 12.8

Determine which among the four graphs pictured in Figure 12.24 are isomorphic.
For each pair of isomorphic graphs, describe an isomorphism between them. For
each pair of graphs that are not isomorphic, give a property that is preserved under
isomorphism such that one graph has the property, but the other does not. For
at least one of the properties you choose, *prove* that it is indeed preserved under
isomorphism (you only need prove one of them).


![figure12.24](https://i.imgur.com/QXfQcZC.png)


- Adjacency matrices are too tedious for this problem.

|       | vertex $\rightarrow$ | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 | Edges |
|-------|----------------------|---|---|---|---|---|---|---|---|---|----|-------|
| $G_1$ | degrees              | 3 | 3 | 3 | 3 | 3 | 3 | 3 | 3 | 3 | 3  | 15    |
| $G_2$ | degrees              | 3 | 3 | 3 | 3 | 3 | 3 | 3 | 3 | 3 | 3  | 15    |
| $G_3$ | degrees              | 3 | 3 | 3 | 3 | 3 | 3 | 3 | 4 | 3 | 4  | 16    |
| $G_4$ | degrees              | 3 | 3 | 3 | 3 | 3 | 3 | 3 | 3 | 3 | 3  | 15    |

We eliminate $G_3$ because 2 vertices doesn't share the same degree compared to the other three.

- Having ten vertices is a preserved property amongst $G_1, G_2, G_3, G_4$.

- Having vertices with a degree of three is a preserved property amongst $G_1, G_2, G_3$.

- Having fifteen edges is a preserved property amongst $G_1, G_2, G_3$, the remaining possible isomorphisms.

- A Hamiltonian path is a preserved property amongst the $G_1, G_2, G_3, G_4$.

    $G_1{Hamiltonian Path} = 1, 2, 3, 4, 5, 8, 7, 6, 10, 9$
    
    $G_2{Hamiltonian Path} = 1, 2, 3, 4, 5, 9, 10, 8, 7, 6$
    
    $G_3{Hamiltonian Path} = 1, 2, 3, 4, 5, 9, 10, 6, 8, 7$
    
    $G_4{Hamiltonian Path} = 1, 2, 6, 5, 9, 8, 3, 4, 10, 7$



### 12.10

Let’s say that a graph has “two ends” if it has exactly two vertices of degree 1 and
all its other vertices have degree 2. For example, here is one such graph:

(a) A *line graph* is a graph whose vertices can be listed in a sequence with edges
between consecutive vertices only. So the two-ended graph above is also a line
graph of length 4.
Prove that the following theorem is false by drawing a counterexample.
**False Theorem**. *Every two-ended graph is a line graph.*

(b) Point out the first erroneous statement in the following bogus proof of the false
theorem and describe the error.

*Bogus proof.* We use induction. The induction hypothesis is that every two-ended graph with n edges is a line graph.

**Base case** $(n = 1)$: The only two-ended graph with a single edge consists of two vertices joined by an edge:

Sure enough, this is a line graph.

**Inductive case**: We assume that the induction hypothesis holds for some $n \ge 1$
and prove that it holds for $n + 1$. Let $G_n$ be any two-ended graph with $n$ edges.
By the induction assumption, $G_n$ is a line graph. Now suppose that we create a
two-ended graph $G_{n+1}$ by adding one more edge to $G_n$. This can be done in only
one way: the new edge must join one of the two endpoints of $G_n$ to a new vertex;
otherwise, $G_{n+1}$ would not be two-ended.

### RSA encryption problem
You have intercepted some messages sent on a popular dating site.  The person sending these messages has the address $(n_1, e_1) = (96403, 31)$.  The person receiving these messages has the address $(n_2, e_2) = (405319, 29)$.

Message1:

[227631, 175041, 262106, 49893, 67508, 265405, 112056, 15517, 346109, 269901, 363337, 112056, 80936, 175102, 266472]

Message2:

[227631, 175041, 269901, 131833, 298318, 304995, 334924, 264584, 107159, 173412, 296042, 222009, 293529]

Message3:

[227631, 175041, 238656, 269901, 88066, 173412, 202240, 191529, 102893, 15585, 175448, 67508, 265405, 222009, 136179, 259370, 139802]

You've discovered that the modulus in the receiver's public key, $n=405319$, is the product of the primes $409$ and $991$.  Use this information to break the RSA encryption.  Pick one of the above questions (or more if you want), decrypt it, and send a reply to the sender.  

- Going to decrypt message 3:

    Modulus recievers public key, $n = 405319$.

    Product of primes $409$ and $991$.

    $(n, e) = (409, 991)

    To decrypt this, we need to computer the inverse of "$e^{-1}$  $mod (p - 1)(q - 1)$"

    $(p - 1)(q - 1) = 408 * 990 = 403920$
    
- extended Euclidean algorithm:

    $a = r_{-1}, b = r_0$
    
    $a * s_i + b * t_i = r_i$, then iterate until $r_i$ equals to zero.
    
    $i$ is the index
    
    $q_i$ is the quotient
    
    $r_i$ is the remainder
    
    $s_i, t_i$ are the Bezout coefficients

| $i$ | $q_i$                | $r_i$      | $s_i$              | $t_i$                         |
|-----|----------------------|------------|--------------------|-------------------------------|
| -1  | -                    | 403920     | 1                  | 0                             |
| 0   | -                    | 29         | 0                  | 1                             |
| 1   | 403920 // 29 = 13928 | 8          | 1 - (13928)(0) = 1 | 0 - (13928)(1) = -13928       |
| 2   | 29 // 8 = 3          | 29 % 8 = 5 | 0 - (3)(1) = -3    | 1 - (3)(-13928) = 41785       |
| 3   | 8 // 5 = 1           | 8 % 5 = 3  | 1 - (1)(-3) = 4    | -13928 - (1)(41785) = -55713  |
| 4   | 5 // 3 = 1           | 5 % 3 = 2  | -3 - (1)(4) = -7   | 41785 - (1)(-55713) = 97498   |
| 5   | 3 // 2 = 1           | 3 % 2 = 1  | 4 - (1)(-7) = 11   | -55713 - (1)(97498) = -153211 |
| 6   | 2 // 1 = 2           | 0          | -                  | -                             |

$gcd = (11)403920 + (-153211)29$

An inverse of $29$ $mod 403920$ is $-153211$, which is congruent to $250709$ $mod 403920$

So the description exponent, $e^{-1} = 250709$

Then take the $MessageElement^{e^{-1}}$ $mod$ $n$ for each element in the message.


- Finished the rest via python below:
```
n = 405319
e = 250709

message_encrypted = [227631, 175041, 238656, 269901, 88066, 173412, 202240, 191529, 102893, 15585, 175448, 67508, 265405, 222009, 136179, 259370, 139802]

message_decrypted = []

# decryption loop
for i in range(len(message_encrypted)):
    message_decrypted.append(str(message_encrypted[i]**e % n))

message_decrypted_wZero = []

# add zeros loop
for message in message_decrypted:
    while len(message) < 4:
        message = "0" + message
    
    message_decrypted_wZero.append(message)

# print decrypted message with zeros
print("message_decrypted_wZero:", message_decrypted_wZero)

cipher = {
"00":"A", "01":"B", "02":"C", "03":"D", "04":"E", "05":"F", "06":"G", "07":"H", "08":"I", "09":"J", "10":"K", "11":"L", "12":"M", "13":"N", "14":"O", "15":"P", "16":"Q", "17":"R", "18":"S", "19":"T", "20":"U", "21":"V", "22":"W", "23":"X", "24":"Y", "25":"Z", "26":"-"}

decrypted_message = []

# mapping decrypted message to a letter via cipher
for message in message_decrypted_wZero:
    first_key = message[0] + message[0+1]
    second_key = message[0+2] + message[0+3]
    
    if first_key in cipher:
        decrypted_message.append(cipher[first_key])
    
    if second_key in cipher:
        decrypted_message.append(cipher[second_key])

message = ""

# loop to print string
for letters in decrypted_message:
    message += letters
    
print("message3:", message)

############# output #############
message_decrypted_wZero: ['2207', '0019', '2608', '1826', '1907', '0426', '0104', '1819', '2612', '1421', '0804', '2624', '1420', '2104', '2618', '0404', '1326']
message3: WHAT-IS-THE-BEST-MOVIE-YOUVE-SEEN-
```
Reply to senders address $(n_1, e_1) = (96403, 31)$:

0813 1904 1718 1904 1111 0017

---
---

*END*

---
---