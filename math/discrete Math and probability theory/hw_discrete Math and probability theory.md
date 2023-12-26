# Hw_1
## 1
- A
$$
\sum^\infty_{k=1} \frac{9}{2^k}=9\sum^\infty_{k=1} \frac{1}{2^k}=9\left( \sum^\infty_{k=0} \frac{1}{2^k}-1 \right)=9\times(2-1)=9
$$
- B
$$
\sum^{n-1}_{k}2k+1
$$
- C
$$
\int^\infty_{0} \sin(t)e^{-t} \, dt=-\int ^\infty_{0}\sin (t) \, de^{-t} 
$$
$$
=-\sin(t)e^{-t}|_{0}^\infty+\int ^\infty_{0}e^{-t}\cos(t) \, dt 
$$
$$
=1-\int ^\infty_{0}\cos(t) \, de^{-t} 
$$
$$
=1-e^{-t}\cos(t)|^\infty_{0}-\int ^\infty_{0}\sin(t)e^{-t} \, dt 
$$
$$
2\int ^\infty_{0}\sin(t)e^{-t} \, dt=1 
$$
$$
\int ^\infty_{0}\sin(t)e^{-t} \, dt=\frac{1}{2}
$$
- D
$$
f(x)=-x\cdot \ln x \quad(x>0)
$$
$$
f'(x)=-\ln x-1
$$
$$
f'(x)=0\qquad x=\frac{1}{e}
$$
$$
f_{max}(x)=f\left( \frac{1}{e} \right)=\frac{1}{e}
$$
$$
f''(x)=-\frac{1}{x}<0
$$

## 2
- A
$$
p(x)=x^2\qquad(\exists x \in \mathbb{R})((p(x)=0)\wedge((\forall y \in \mathbb{R})(p(y)=0)\Longrightarrow(x=y)))
$$
- B
$$
(\forall x,y \in \mathbb{Q})((x \not = y)\Longrightarrow((\exists z \in \mathbb{Q})((x<z<y)\lor (y<z<x))))
$$
- C
$$
(\forall x \in \mathbb{Z})((x^2>4)\Longrightarrow(x>2)\lor(x<-2))
$$
- D
	- All real numbers are complex number
- E
	- There is not integer to the equation $x^2+y^2=10$
- F
	- All even numbers bigger than two can write into two prime number
- 
## 3
- T
- T
- F
- T
- F
- N
- 
## 4
- A
	- $n^2+4n=n(n+4)$
	- $n=2k+1\qquad n^2+4n=4k^2+12k+5$
	- Above is odd
- B
	- $p=a\leq 11\lor b\leq 4$
	- $\neg p=a\geq 11\wedge b\geq 4$
	- $Q=a+b\leq15$
	- $\neg p \Longrightarrow \neg Q$ 
	- $p \Longrightarrow Q$
- C
	- If $r=\frac{a}{b}$
	- $\Rightarrow r^2=\frac{a^2}{b^2}$
	- $r^2$ is rational
	- So T
- D
	- $5n^3>n!$
	- $5n^2>(n-1)!$
	- $n=7\qquad 5n^2=245\quad (n-1)!=720$
	- F
	- 
## 5
- A
	- Every number $>3$ can from as $3k,3k+1,3k+2$
	- $3k-1$ is equal to $3k+2$
	- $3k$ is not possible to be prime
	- So that it come true
- B
	- If one number is Twin primes
	- Equal $3k-1$ or $3k+1$
	- It has two near primes just equal $3k+3,3k-2$ or $3k+1,3k-3$
	- So 5 is right answer
	- And for other $k\geq2$
	- We can see $3k+3$ and $3k-3$ can device by 3
## 6
- A 
	- ![upgit_20231225_1703471977.png](https://raw.githubusercontent.com/LLLLLUOTJ/img_ob/main/2023/12/upgit_20231225_1703471977.png)
	- This is the counterexample
	- The problem is meaning that in all case, there must be three people have same connection
- B
	- N equal 6, and the conditions of connection equal 2. 
	- We only talk about if the counterexample should be existed. 
	- So we suppose that there is a person $p$ . The others are divided into two groups. Strangers and friend. 
	- So we have two conditions based on stranger and friend has the same effect. 
	- The first is $p$ with the same condition with three or more people, so that they should be the opposite condition which is equal or more than three in the same condition group. 
	- The second is $p$ with two, which means that those two. And we will surprisingly found that the others' connection with $p$ just like the first one, it's the same!
	- So this proposition is true. Otherwise, it can proof A. 


## 7
- (a)
	- Suppose $x$ is $f(x)\in A \cup B$
		- $f(x)\in A \rightarrow x \in f^{-1}(A)\mid\mid f(x)\in B \rightarrow x \in f^{-1}(B)$
		- $\rightarrow x \in f^{-1}(A)\cup f^{-1}(B)$
		- $\rightarrow f^{-1}(A \cup B)\subseteq f^{-1}(A)\cup f^{-1}(B)$
	- Suppose $x\in f^{-1}(A)\cup f^{-1}(B)$
		- Suppose  $x \in f^{-1}(A) \rightarrow f(x)\in A\cup B$
		- $\rightarrow x \in f^{-1}(A \cup B)$
		- $\rightarrow f^{-1}(A)\cup f^{-1}(B)\subseteq f^{-1}(A\cup B)$
	- $\longrightarrow f^{-1}(A\cup B)=f^{-1}(A)\cup f^{-1}(B)$
- (b)
	- Suppose $x$ is $f(x)\in A \cap B$
		- $f(x)\in A \rightarrow x\in f^{-1}(A)\&\&f(x)\in B \rightarrow x\in f^{-1}(B)$
		- $\rightarrow x\in f^{-1}(A)\cap f^{-1}(B)$
		- $\to f^{-1}(A\cap B)\subseteq f^{-1}(A)\cap f^{-1}(B)$
	- Suppose $x \in f^{-1}(A)\cap f^{-1}(B)$
		- Suppose $x\in f^{-1}(A)\to f(x)\in A\cap B$
		- $\to x\in f^{-1}(A\cap B)$
		- $\to f^{-1}(A)\cap f^{-1}(B)\subseteq f^{-1}(A\cap B)$
	- $\longrightarrow f^{-1}(A\cap B)=f^{-1}(A)\cap f^{-1}(B)$
- (c)
	- Suppose $f(x)\in A\setminus B$
		- $f(x)\in A\ \&\&\ f(x)\not\in B\to x \in f^{-1}(A)\ \&\&\ x \not\in f^{-1}(B)$
		- $\to x \in f^{-1}(A)\setminus f^{-1}(B)$
		- $\to f^{-1}(A\setminus B)\subseteq f^{-1}(B){\setminus}f^{-1}(B)$
	- Suppose $x \in f^{-1}(A){\setminus}f^{-1}(B)$
		- $x \in f^{-1}(A)\to f(x)\in A,x \not\in f^{-1}(B)\to f(x)\not\in B$
		- $\to x \in A{\setminus}B$
		- $\to f^{-1}(A){\setminus}f^{-1}(B)\subseteq f^{-1}(A\setminus B)$
	- $\longrightarrow f^{-1}(A\setminus B)=f(A\setminus B)$
- (d)
	- Suppose $x\in A\cup B$
		- $x\in A\mid\mid x\in B$
		- $\to x\in A\cup B$
		- $\to f(x)\in f(A\cup B) \subseteq f(A)\cup f(B)$
	- Suppose $y \in f(A)\cup f(B)$
		- $y \in f(A)\to x \in A\mid\mid y \in f(B) \to x \in B$
		- $\to x \in A\cup B \to y=f(A\cup B)$
		- $\to f(A)\cup f(B)\subseteq f(A\cup B)$
	- $\longrightarrow f(A\cup B)=f(A)\cup f(B)$
- (e)
	- Suppose $x\in A\cap B$
		- $x\in A\ \&\&\ x\in B$
		- $\to x\in A\cap B$
		- $x\in A\cap B \subseteq A\cap B$
		- $\to f(x) \in f(A\cap B)\subseteq f(A)\cap f(B)$
	- Example
		- If the same $y$ has multiple $x$ lie in both A and B
- (f)
	- Suppose $y \in (A{\setminus}B)$
		- $y \not\in f(B)$
		- $x \in A\ \&\&\ x \not\in B$
		- $f(x)\in f(A\setminus B)$
	- Example
		- $B=\{ 0 \},A=\{ 1 \},f(0)=f(1)=0$
		- $A{\setminus}B={0}$
		- $f(A)=f(B)={0},f(A){\setminus}f(B)=\varnothing$

