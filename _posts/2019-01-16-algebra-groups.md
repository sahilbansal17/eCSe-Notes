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