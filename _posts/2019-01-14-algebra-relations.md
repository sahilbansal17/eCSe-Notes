---
title: "MTL105 Algebra - Equivalence Relations"
date: 2019-01-14
---
{% include lib/mathjax.html %}

### Equivalence Relations
The motivation behind such relations is that things that are different in one context may be same in some another. For e.g. 5 and 3 are different integers, but $$ 5 \equiv 1 (mod \ 2) $$ and $$ 3 \equiv 1 (mod \ 2) $$. In this, context they are related.

In physics, vectors of same length and magnitude may produce different effects, whereas in linear algebra, they are considered to be same.

So, to understand Equivalence relations, we first need to formally define a relation.

#### Definitions - Relation
A binary relation or a relation R from a set A into B is a subset of AxB, i.e. $$ R \subseteq A\times B $$. 

A relation R **on a set A** is defined as $$ R \subseteq A\times A $$.

#### Definitions - Equivalence Relation
R is a relation on set A; then R is an Equivalence relation, if the following properties hold:
1. **Reflexive**: $$ (a, a) \in R , \forall a \in A $$
2. **Symmetric**: $$ (a, b) \in R \Rightarrow (b, a) \in R $$.
3. **Transitive**: $$ (a, b) \in R \ and \ (b, c) \in R \Rightarrow (a, c) \in R $$

There is a convention to write $$ a \sim b $$ if $$ (a, b) \in R $$ where R is an equivalence relation. It can also be written as $$ aRb $$.

#### Definitions - Equivalence Class
If $$ \sim $$ is an equivalence relation on a set A and $$ a \in A $$, then the set 

$$ [a] = \left \{ x \in A \mid x \sim a \right \} $$

is called the *equivalence class of $$ \sim $$ containing a*.

Example:
Let S be the set of all polynomials with real coefficients. If $$ f, g \in S $$, define $$ f \sim g $$ if $$ f' = g' $$, where $$ f' $$ is the derivative of $$ f $$. Then, $$ \sim $$ is an equivalence relation on S. 

Since two polynomials with equal derivatives differ by a constant, we can say that equivalence class of f, i.e.

$$ [f] = \left \{ f + c \mid c \ is \ real \right \} $$

#### Theorem - Equivalence Classes Partition
The equivalence class of an equivalence relation on a set S constitutes a partition of S.

First, we define what is a **Partition of a set S**.

**Partition**

A partition of a set S is a collection of non-empty disjoint subsets of S whose union is S.

Mathematically, it is a collection $$ \mathbb{P} $$ of non-empty subsets of S, such that:
- $$ \bigcup_{B \in \mathbb{P}}^{B} = \mathbf{S} $$
- If $$ A, B \in \mathbb{P} $$, then either $$ A = B $$ or $$ A\cap B = \phi $$ 

Coming to the proof the the theorem above,

- Let $$ \sim $$ be an equivalence relation on a set A. For any $$ a \in A $$, the reflexive property shows that $$ a \in [a] $$ since $$ a \sim a $$. So, $$ [a] $$ is non empty and the union of all equivalence classes is A. 
- Now, suppose that $$ [a] $$ and $$ [b] $$ are two equivalence classes. Then, there are two possible cases: either $$ (a, b) \in \sim $$ or $$ (a, b) \not\in \sim $$.
    - Case 1: $$ (a, b) \in \sim $$
    
    Let $$ x \in [a] $$. So, $$ x \sim a $$. Also, we have $$ a \sim b $$. Using transitivity, $$ x \sim b $$. Thus, $$ x \in [b] $$. This means, $$ [a] \subseteq [b] $$. Analogously, $$ [b] \subseteq [a] $$. This shows that $$ [a] = [b] $$.
    
    - Case 2: $$ (a, b) \not\in \sim $$

    Let $$ c \in [a] \cap [b] \neq \phi $$. So, $$ c \sim a $$ and $$ c \sim b $$. Thus, $$ a \sim c $$ also by symmetry. Using transitivity, $$ a \sim b $$ which is an contradiction. Thus, $$ [a] \cap [b] = \phi $$.

#### Converse of theorem - 
For any partition $$ \mathbb{P} $$ of S, there is an equivalence relation on S whose equivalence classes are the elements of $$ \mathbb{P} $$.

**Proof**:

We define $$ a \sim b $$ if *a* and *b* belong to the same subset in the collection $$ \mathbb{P} $$. We need to show that $$ \sim $$ is an equivalence relation on a set S. This is left as **homework**.

#### Exercises:
1. The following relations are defined on the set $$ \mathbb{R} $$ of real numbers. Find whether these relations are reflexive, symmetric or transitive.
    1. $$ a \sim b $$ iff $$ \mid \ a - b \mid > 0 $$
    2. $$ a \sim b $$ iff $$ 1 + ab > 0 $$
    3. $$ a \sim b $$ iff $$ \mid \ a \mid \leq b $$
2. Let S be a finite set of n elements. Prove that number of reflexive relations that can be defined on S is $$ 2^{n^{2} - n} $$. Similarly, prove the following -
    1. No. of symmetric relations are $$ 2^{\frac{n(n+1)}{2}} $$
    2. No. of relations which are both symmetric and reflexive are $$ 2^{\frac{n(n-1)}{2}} $$
3. What is the remainder when $$ 11^{40} $$ is divided by $$ 8 $$ ?
4. What is the remainder when $$ 1! + 2! + 3! + ... + n! $$ is divided by 18 ?

The later part covered an introduction to **group theory**. 