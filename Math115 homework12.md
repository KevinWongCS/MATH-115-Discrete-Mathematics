name: kevin wong\
filename: Math115 homework12\
date: 04/20/2022\
desc: https://courses.csail.mit.edu/6.042/spring18/mcs.pdf (Links to an external site.) please do these problems: additional problem, 12.23, 12.56ab, 12.57, 12.63.

---
---

### Character Frequency Problem

![](https://i.imgur.com/HEchBHq.png)

- a) $b = 0100, e = 11, a = 10, d = 0110$

    bead is encoded with bit string $0100$  $11 10$ $0110$.

- b) The average number of bits used per character is $2(0.26) + 4(0.02) + 4(0.09) + 4(0.08) + 2(0.30) + 2(0.14) + 4(0.11) = 2.6 $

- c) Using Hoffman coding to get the optimal encoding.

    Heavier weight goes on left.
    
    Lighter weight on right.

    Branching left is assigned a zero bit.

    Branching right is assigned a one bit.

```
a: 0.26    b: 0.02    c : 0.09    d : 0.08    e : 0.30    f : 0.14    g : 0.11

a: 0.26    cb: 0.11    d : 0.08    e : 0.30    f : 0.14    g : 0.11
           /\ 
          c  b  

a: 0.26    cbd: 0.19    e : 0.30    f : 0.14    g : 0.11
            /\
           /\ d
          c  b   

a: 0.26    cbd: 0.19    e : 0.30    fg : 0.25
            /\                      /\ 
           /\ d                    f  g 
          c  b   

a: 0.26    fgcbd: 0.44    e : 0.30
            / \
           /   \       
          /     \
         /\     /\                      
        f  g   /\  d                   
              c  b   

          fgcbd: 0.44    ea : 0.56
           / \           /\ 
          /   \         e  a  
         /     \
        /\     /\                      
       f  g   /\  d                   
             c  b

          eafgcbd: 1
             /\
            /  \
          0/    \1
          /      \
        0/\1    / \           
        e  a  0/   \1         
              /     \
            0/\1   0/ \1 
            f  g  0/\1 \   
                  c  b  d 
```
A lower average number of bits used per character is $2(0.26) + 4(0.02) + 4(0.09) + 3(0.08) + 2(0.30) + 3(0.14) + 3(0.11) = 2.55$

---
---

### 12.23 
![](https://i.imgur.com/vywqYuf.png)


---
---


### 12.56ab

---
---


### 12.57

---
---


### 12.63


---
---

*END*

---
---