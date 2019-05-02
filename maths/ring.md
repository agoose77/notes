Ring
====

A ring consists of a [set](set.md) $R$ combined with two binary operations $+$ and $\cdot$ that generalise the arithmetic operations of addition and multiplication respectively.
It is hence an [abelian group](groups.md#Abelian-Groups) under $+$, with an additional binary operation $\cdot$ that is associative, and distributive over the abelian group operation. In addition, $\cdot$ has an identity element. These conditions are summarised in the ring axioms:

1. $R$ is an [abelian group](groups.md#Abelian-Groups) under addition.
2. $R$ is a moniod under multiplication:
   * $(a\cdot b)\cdot c = a\cdot (b\cdot c)$ for all $a,b,c\in R$ (*multiplicative associativity)*.
   * $\exists 1\in R$ such that $a\cdot 1=a$ and $1\cdot a=a$ for all $a\in R$ (*multiplicative identity*).
3. Multiplication is distributive with respect to addition
   * $a\cdot(b+c)=(a\cdot b) + (a\cdot c)$ for all $a,b,c\in R$ (*left distributivity*)
   * $(b+c)\cdot a=(b\cdot a) + (c\cdot a)$ for all $a,b,c\in R$ (*left distributivity*)