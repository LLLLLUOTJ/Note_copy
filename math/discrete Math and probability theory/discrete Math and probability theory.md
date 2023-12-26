# Review of Sets and Mathematical Notion
## Set
- A collection of objects
- Objects call **element** or **members** of set
- Objects can be anything 
- $\ni,\not\ni,\in,\notin$
- Rational number
	- $\mathbb{Q}=\left\{ \frac{a}{b}|a,b\ are intergers,b\not=0 \, dx \right\}$
#### Cardinality
- The size of a set
- Denoted by $\mid A\mid$
- $\mid A\mid=0$ denoted by $\emptyset$
#### Subsets and Proper Subsets
- $\subseteq,\subset$
#### Intersections and Unions
- $A \cap B$
- $A \cup B$
#### Complement
- Relative number of $A$ in $B$
	- $B-A$ or $B/A$
#### Significant Sets
- $\mathbb{N}$ denotes the set of all natural numbers
- $\mathbb{Z}$ denotes the set of all integer numbers
- $\mathbb{Q}$ denotes the set of all rational numbers
- $\mathbb{R}$ denotes the set of all real numbers
- $\mathbb{C}$ denotes the set of all complex numbers
#### Cartesian product (cross product)
- $A \times B=\{(a,b)\mid a \in A,b \in B\}$ 
- If $A=\{1,2,3\}$ and $B=\{u,v\}$
	- $A \times B=\{(1,u),(1,v),(2,u),\dots\}$
#### Power set
- $\mathscr{P}(S)$
- If $S=\{1,2,3\}$
	- $\mathscr{P}(S)=\{\{\},\{1\},\{2\},\{3\},\{1,2\},\dots\}$
## Mathematical notion
#### Sums and Products
- $\sum^n_{i=m}f(i)$
- $\prod^n_{i=m}f(i)$
#### Universal and existential quantifiers
-  $universal\ quantifier\ \forall$ ("for all")
- $existential\ quantife\ \exists$ ("there exists")


# Logic
## Propositional Logic
Proposition
- A statement which is either true or false
#### $proposition forms$
**Conjunction**
- $P\lor Q$ ("$P$ and $Q$")
- True only when both $P$ and $Q$ are true
**Disjunction**
- $P \wedge Q$ ("$P$ or Q")
- True when at least one of $P$ and $Q$ is true 
**Negation**
- $\neg P$ ("not $P$")
- True when $P$ is false
Law of the excluded middle
- Only two Conditions, true or false, for every proposition $P$
$tautology$
- Always true
$contradiction$
- Always false
**Truth table**
- |   $P$   |   $Q$   |  $P \wedge Q$   |
|---|---|:-------:|
| $T$ | $T$ | $T$ |
| $T$ | $F$ | $F$ |
| $F$ | $T$ | $F$ |
| $F$ | $F$ | $F$ |
Implication
- $P \Longrightarrow Q$ ("$P$ implies $Q$")
	- If $P$ than $Q$
	- $P$ is called the $hypothesis$ of the Implication
	- $Q$ is the $conclution$
	- $P \Longrightarrow Q$ is logically equivalent to $\neg P \lor Q$
- Both $P \Longrightarrow Q$ and $Q \Longrightarrow P$ right
	- "$P$ if and only if $Q$" (abbreviated "$P$ iff Q")
	- $P \Leftrightarrow Q$
- Given $P \Longrightarrow Q$
	- Contrapositive
		- $\neg Q \Longrightarrow \neg P$
	- Converse
		- $Q \Longrightarrow P$
## Quantifiers
-  $universal\ quantifier\ \forall$ ("for all")
-  $existential\ quantife\ \exists$ ("there exists")
## Much Ado About Negation
-  $P$ is false $\Longrightarrow$ $\neg P$ is true
- Negate conjunctions and Disjunctions 
	- $\neg(P \wedge Q)\equiv(\neg P \lor \neg Q)$
	- $\neg(P \lor Q)\equiv(\neg P \wedge \neg Q)$
	- Above is *De Morgan's laws*
	- $\neg(\forall xP(x))\equiv \exists x \neg P(x)$
	- $\neg(\exists xP(x))\equiv \forall x \neg P(x)$


# Proof
- A finite sequence of steps, called $logical\ deductions$, which establishes the truth of a desired statement
- The power of a it lies in the fact that using $finite$ means, we can guarantee the truth of a statement with $infinitely$ many cases
- Base on axioms or postulates which we accept without proof (the where we start)
## Notation and basic facts
- A set is $close$
	- The result between elements of a set under addition and multiplication will still be the element in it
- $a\mid b$
	- a divides $b$ iff there exists an integer $q$ such that $b=aq$
- $:=$
	- To indicate a definition

## Direct Proof
- Just proof directly
## Proof by Contraposition
- $\neg Q \Longrightarrow \neg P$
## Proof by Contradiction
- Assume $\neg P$, $\cdots R \cdots \neg R$
- Conclude $\neg P \Longrightarrow \neg R \wedge \neg R$, which is a contradiction. Thus, P
- For the condition that we want to show something don't exist
## Proof by Cases
- List all case which must have one true and prove all of them
## Common Errors When Writing Proof
- When writing proofs, do not assume the claim you aim to prove!
- In particular, never forget to consider the case where your variables take on the value 0
- Says to be careful when mixing negative numbers and inequalities
## Style and substance in proofs
- If you cannot explain clearly why the step is justified, you are making a leap and you need to go back and think some more
- In theory, each step in a proof must be justified by appealing to a definition or general axiom
-  A justification can be stated without proof only if you are absolutely confident that (1) it is correct and (2) the reader will automatically agree that it is correct
- $lemmas$
	- A subsidiary result that is useful in a more complex proof




# Induction

## Mathematical Induction

