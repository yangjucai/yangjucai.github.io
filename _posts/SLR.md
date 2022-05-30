1.考虑下面文法，构造 SLR 分析表（5）

E→E+T|T

T→TF|F
F → F *| a | b

解答：

增广文法位：

E' -> E	(1)
E -> E+T (2)
E->T (3)
T→TF (4) 
T -> F (5)
F → F * (6)
F ->  a (7)
F ->  b (8)

I0:
E' -> ·E
E -> ·E + T
E -> ·T
T -> ·TF
T -> ·F
F -> ·F*
F -> ·a
F -> ·b

I1：
E' -> E·
E ->E·+T

I2:
E -> T·
T -> T·F
F -> ·F*
F -> ·a
F -> ·b

I3:
T -> F·
F -> F·*

I4:
F -> a·

I5:
F -> b·

I6：
E -> E+·T
T -> ·TF
T -> ·F
F -> ·F*
F -> ·a
F -> ·b

I7:
T -> TF·
F -> F·*

I8:
F -> F*·

I9：
E -> E+T·
T -> T·F
F -> ·F*
F -> ·a
F -> ·b

FOLLOW(E) = {\$,+}
FOLLOW(T) = {a,b,\$,+}
FOLLOW(F) = {*, a, b, $, +}

 SLR语法分析表：
![image-20220523212140945](https://cdn.jsdelivr.net/gh/yangjucai/yangjucai.github.io@main/images/postsimage-20220523212140945.png)

2.对文法，证明它是 LL(1)文法但不是 SLR(1)文法（5）

S→AaAb | BbBa

A→ε

B→ε

解答：
FIRST集：
$$
FIRST(S) = \{a, b\}\\
FIRST(A) = \{\epsilon\}\\
FIRST(B) = \{\epsilon\}
$$
FOLLOW集：
$$
FOLLOW(S) = \{$\}\\
FOLLOW(A) = \{a,b\}\\
FOLLOW(B) = \{a,b\}
$$
LL(1)预测分析表位：

|      | a               | b               | $    |
| ---- | --------------- | --------------- | ---- |
| S    | S -> AaAb       | S->BbBa         |      |
| A    | A -> $\epsilon$ | A -> $\epsilon$ |      |
| B    | B -> $\epsilon$ | B -> $\epsilon$ |      |

无冲突，符合LL(1)文法

SLR（1）分析表：
增广文法：
S' -> S (1)
S -> AaAb (2)
S -> BbBa (3)
A -> $\epsilon$ （4）
B -> $\epsilon$ （5）

I0:
S' ->·Ｓ
S -> ·AaAb
S -> ·BbBa
A -> ·
B -> ·

此时， M[0, a] 可以时r4 或r5, M[0,b]可以是r4或r5, 因此产生规约/规约冲突，所以不是SLR文法。

