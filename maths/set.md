# Set
A set is a well defined, unordered collection of _distinct_ objects, called elements.

## Definition
Sets may be built using set-builder notation:

|          Method         	|                                                 Definition $(S= \dots)$                                                	|
|:-----------------------:	|:----------------------------------------------------------------------------------------------------------------------:	|
|    Direct enumeration   	|                                                   $\{\, 1, 2, 5, 9, 3 \,\}$                                                  	|
| From a regular sequence 	|                                                  $\{\, 1, 2, \dots, 10 \,\}$                                                 	|
|        From prose       	|                                             the square of rational numbers                                             	|
|    Using a predicate    	| $$\begin{aligned}\{\, x: x^2\in T \,\} \\ \{\, x\in\mathbb{N}:x^2\in T \,\}\\\{\, x\in\mathbb{N}:x^2\in T \land P(x) \,\}\end{aligned}$$ 	|

Where $\land$ is logical AND.

## Membership

|   Expression   	|           Description           	|
|:--------------:	|:-------------------------------:	|
|    $x\in A$    	|         $A$ contains $x$        	|
|   $x \notin A$   	|     $A$ does not contain $x$    	|
| $A\subseteq B$ 	|      $A$ is a subset of $B$     	|
|  $A\subset B$  	|  $A$ is a proper subset of $B$  	|
| $A\supseteq B$ 	|     $A$ is a superset of $B$    	|
|  $A\supset B$  	| $A$ is a proper superset of $B$ 	|

## Operations

|         Name         	|      Expression     	|            Explicit Result            	|
|:--------------------:	|:-------------------:	|:-------------------------------------:	|
|         Union        	|      $A\cup B$      	|    $\{\, x:x\in A \lor x\in B \,\}$   	|
|     Intersection     	|      $A\cap B$      	|   $\{\, x:x\in A \land x\in B \,\}$   	|
|      Complement      	|    $A\setminus B$   	|  $\{\, x:x\in A \mid x\notin B \,\}$  	|
|   Cartesian product  	|     $A\times B$     	| $\{\, (x,y):x\in A \land y\in B \,\}$ 	|
| Symmetric Difference 	| $A\bigtriangleup B$ 	|  $(A\setminus B)\cup (B\setminus A)$  	|
|      Cardinality     	|  $\lvert A\rvert $  	|        Number of elements in A        	|

## Reserved Symbols

|    Symbol    	|                 Name                 	|
|:------------:	|:------------------------------------:	|
|  $\emptyset$ 	|               Empty set              	|
| $\mathbb{N}$ 	|               Naturals               	|
| $\mathbb{Z}$ 	|               Integers               	|
| $\mathbb{Q}$ 	|               Rationals              	|
| $\mathbb{R}$ 	|                 Reals                	|
| $\mathbb{C}$ 	|            Complex numbers           	|
| $\mathbb{U}$ 	| Universal set (superset of all sets) 	|