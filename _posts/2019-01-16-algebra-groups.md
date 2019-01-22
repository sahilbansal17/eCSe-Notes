---
title: "MTL105: Algebra - Groups"
date: 2019-01-16
categories: [MTL105]
---
{% include lib/mathjax.html %}

### Binary Operation
Let G be a set. A binary operation on G is a function that assigns each ordered pair of elements of G an element of G.

$$ {\color{Red} \circ} : G \times G \rightarrow G $$

$$ (a, b) \mapsto a {\color{Red} \circ} b $$

for e.g. : addition, subtraction and multiplication operation on integers.

### Group
Let G be a set, i.e. $$ G (\neq \phi) $$ together with a binary operation $$ {\color{Red} \circ} : G \times G \rightarrow G $$. <br>
We say that G is a group under this operation if the foll. 3 conditions are satisfied:
1. **Associativity**: $$ a {\color{Red} \circ} (b {\color{Red} \circ} c) = (a {\color{Red} \circ} b) {\color{Red} \circ} c, \ \forall a, b, c \in G $$
2. **Identity**: $$ \exists e \in G \ s.t. \ a {\color{Red} \circ} e = e {\color{Red} \circ} a = a, \ \forall a \in G $$
3. **Inverse**: $$\forall a \in G, \ \exists b \in G \ s.t. \ a {\color{Red} \circ} b = b {\color{Red} \circ} a = e $$

Here, b is the inverse of a and e is known as the identity element.

The notation to denote that G is a group under the operation $$ {\color{Red} \circ} $$ is $$ (G, {\color{Red} \circ}) $$. 

#### Order of a group
It is the number of elements in the group denoted by $$ \left | G \right | $$. If $$ \left | G \right | $$ is finite, we say the group is **finite**, otherwise the group is **infinite**.

Some examples:
- The set of integers under ordinary multiplication is not a group sice inverse of every element doesn't exist.
- *Group of integers modulo n*: <br>
Let *n* be a +ve int, and $$ a \neq 0 $$ such that $$ a = nq + r, 0 \leq r < n $$. Then, $$ a \equiv r \ (mod \ n) $$. The congruent modulo n is an equivalence relation and the set of its equivalence classes is known as $$ \mathbb{Z}_{n} $$.

$$ \mathbb{Z}_{n} = \left \{ \bar{0}, \bar{1}, \bar{2}, ... , \bar{(n-1)} \right \} $$

$$ \mathbb{Z}_{n} $$ for $$ n \geq 1 $$ is a group under addition modulo n.

But, we cannot say that $$ \mathbb{Z}_{n} \setminus \left \{ 0 \right \} $$ is a group under multiplication modulo n, since there can be some elements without any inverse.

$$ \mathbb{Z}_{n} \setminus \left \{ 0 \right \} $$ is denoted by $$ \mathbb{Z}_{n}^{\star} $$.

- $$ \mathbf{(\mathbb{Z}_{n}^{\star}, \cdot_{m})} $$ where $$ \cdot_{m} $$ represents multiplication modulo m, is a group when n is prime. **So, if it is a group, can we say that n must be prime?**
- *General linear group of $$ 2 \times 2 $$ matrices over $$ \mathbb{R} $$:* <br>
$$
G L ( 2 , \mathbb { R } ) = \left\{ \left[ \begin{array} { l l } { a } & { b } \\ { c } & { d } \end{array} \right] | \  a , b , c , d \in \mathbb{ R } , a d - b c \neq 0 \right\}
$$
<br> This is a group under the operation matrix multiplication.
- Set of integers under subtraction is not a group since it does not follow Associativity property.
- $$ \mathbf{U(n)} $$ is defined to be a set of all positive integers less than n and relatively prime to n. It is a group under multiplication modulo n.

$$ U(n) = \left \{ \bar{a} \in {\mathbb{Z}_{n}}^{\star} \mid gcd(a, n) = 1 \right \} $$

### Abelian Group
Let $$ (G, {\color{Red}\circ}) $$ be a group. It is said to be **Abelian** iff: <br>
$$ a {\color{Red}\circ} b = b {\color{Red}\circ} a, \ \forall \ a, b \in G $$. 

**Question:** Which element must always exist in a group? <br>
**Answer:** The **identity** element.

The following theorems lead to some elementary properties of the groups:
#### Theorem 1: Uniqueness of the Identity 
``` In a group G, there is only one identity element.```

**Proof:** Let $$ (G, {\color{Red}\circ}) $$ be the group and let there be two identity elements $$ e_{1} $$ and $$ e_{2} $$

Then:
1. $$ a {\color{Red}\circ} e_{1} = e_{1} {\color{Red}\circ} a = a, \ \forall \ a \in G $$ 
2. $$ a {\color{Red}\circ} e_{2} = e_{2} {\color{Red}\circ} a = a, \ \forall \ a \in G $$

Using $$ a = e_{2} $$ in equation 1, we get $$ e_{2} {\color{Red}\circ} e_{1} = e_{2} $$ and using $$ a = e_{1} $$ in equation 2, we get $$ e_{2} {\color{Red}\circ} e_{1} = e_{1} $$, which means $$ e_{1} $$ and $$ e_{2} $$ are both equal.