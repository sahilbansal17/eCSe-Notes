---
title: "MTL105: Algebra - Introduction class"
date: 2019-01-10
---
{% include lib/mathjax.html %}

The following books are recommended for Algebra course - 
1. Topics in Algebra by **I.N. Herstein**
2. Contemporary Abstract Algebra by **Joseph A. Gallian**

The course mainly deals with - 
1. Group Theory
2. Ring Theory
3. Field Theory

## Preliminaries
Much of abstract algebra involves properties of integers and sets. 

#### Definitions - Set
A set is a collection of well-defined **distinct** objects.
for e.g. :

$$ \mathbb{Z} = \left \{0, \pm 1, \pm 2, ...  \right \} $$

An important property of the integers is the **well-ordering principle.**

### Well-Ordering Principle
Every non-empty set of positive integers contains a smallest member.

If we had included negative numbers also, then establishing the  notion of smallest number would not have been possible.

The concept of divisibility also plays a fundamental role in the number theory. We write $$ t \mid s $$, i.e. t divides s, if $$ s = tu $$.

### Division Algorithm
Let **a** and **b** be integers with **b > 0**. Then there exist unique integers **q** and **r** with the property that:
$$ a = bq + r, 0\leq r < b $$

#### Definitions - Greatest Common Divisor
Two numbers *a* and *b* are said to have a GCD equal to *d* if -
- $$ d \mid a $$ and $$ d \mid b $$
- If $$ e \mid a $$ and $$ e \mid b $$ => $$ e \mid d $$

*Question* : What is *gcd(0, 0) =* ?

#### Definitions - Prime Number
A positive integer greater than 1 whose only positive divisors are 1 and the number itself is said to be prime.

Two numbers *a* and *b* are said to be relatively prime if 
$$ gcd(a, b) = 1. $$

### GCD is a Linear Combination
For $$ a \neq 0, b \neq 0 $$, there exists integers *s* and *t* such that $$ gcd(a, b) = as + bt $$. Moreover, gcd(a, b) is the smallest positive integer of the form $$ as + bt $$.

### Euclid's Lemma p|ab implies p|a or p|b
If p is a prime that divides ab, then p divides a or p divides b.

*Proof:*

Let $$ p \nmid a $$, i.e. p does not divide a. We must show that p divides b. Since p does not divide a, $$ gcd(p, a) = 1 $$.

So, we can write $$ 1 = as + pt $$. Multiplying both sides by b, $$ b = abs + ptb $$, and since p divides the right-hand side of this equation, thus p divides b also. 

- It was mentioned that there are 6 different proofs to show that **there are infinitely many primes**.

**Primes are the building blocks of all integers.** The following property convinces us so.

### Fundamental Theorem of Arithmetic
Every integer greater than 1 is either a prime or a product of primes. This product is unique, except for the order in which the factors appear. That is, if $$ n = p_{1}p_{2}...p_{r} $$ and $$ n = q_{1}q_{2}...q_{s} $$, where the p's and q's are primes, then $$ r = s $$ and, after renumbering the q's we have $$ p_{i} = q_{i} $$ for all i.

#### Definitions - Least Common Multiple
Two nonzero integers *a* and *b* are said to have *s* as their LCM if 
- $$ a \mid s $$ and $$ b \mid s $$. 
- If $$ a \mid t $$ and $$ b \mid t $$ => $$ s \mid t $$.

## Mathematical Induction
### 1. First Principle of Mathematical Induction
Let S be a set of integers containing a. Suppose S has the property that whenever some integer $$ n \geq a $$ belongs to S, then the integer $$ n + 1 $$ also belongs to S. Then, S contains every integer greater than or equal to a.

### 2. Second Principle of Mathematical Induction
Let S be a set of integers containing a. Suppose S has the property that n belongs to S whenvever every integer less than n and greater than or equal to a belongs to S. Then, S contains every integer greater than or equal to a.