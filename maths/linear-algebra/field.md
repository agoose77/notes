Field
=====

A field is a [set](set.md) $F$ together with two operations of _addition_ and _multiplication_. An operation is a mapping which associates any pair of elements of the set to another element of the set. Concisely, it is a [ring](../ring.md) with the additional property that all the elements besides the additive identity $0$ form an [abelian group](../group.md#Abelian-Groups) under multiplication.

The operations of the field are required to satisfy the following set of _field axioms_:

Axioms
------

| Name                                           | Definition                                                                                      |
| ---------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| Associativity of addition and multiplication   | $$\begin{aligned}a + (b + c) &= (a + b) + c\\a\cdot(b\cdot c)&=(a\cdot b)\cdot c\end{aligned}$$ |
| Commutativity of addition and multiplication   | $$\begin{aligned}a+b&=b+a\\a\cdot b&=b\cdot a\end{aligned}$$                                    |
| Additive and multiplicative identity           | $$\begin{aligned}\exists\, 0, 1\,\in F:a+0&=a \\ a\cdot 1 &= a\end{aligned}$$                   |
| Additive inverses                              | $\forall a\in F \,\exists\,{-a}\in F:a+{-a}=0$                                                  |
| Multiplicative inverses                        | $\forall a\notin F\,\exists\,{a^{-1}}\in F: a\cdot a^{-1}=1$                                    |
| Distributivity of multiplication over addition | $a\cdot(b+c)=(a\cdot b)+(a\cdot c)$                                                             |

These axioms may be summarised by stating:

- A field has two operations, _addition_ and _multiplication_.
- $0$ is the additive identity, $1$ is the multiplicative identity.
- It is an [abelian group](group.md/#Abelian-Groups) under addition, and its nonzero elements an abelian group under multiplication.
- The multiplication is distributive over the addition.

Difference with Vector Space 
----------------------------
> One of the field axioms says that any nonzero element c∈F has a multiplicative inverse, namely an element c−1∈F such that c×c−1=1=c−1×c. There is no corresponding property among the vector space axioms.
[^1]

[^1]: https://math.stackexchange.com/a/969737/354098