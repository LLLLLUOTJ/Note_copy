**Anatomy of a Call Expression**
```
add(2,3)
operator(operand,operand)
```
Evaluating Nested Expressions
```
mul(add(2, mul(4,6)),add(3, 5))
```
_Expression tree_
![[Pasted image 20231023222221.png]]

**Defining Functions**
Assignment
->binds names to values
Function definition
->binds names to expressions
```
def <name>(<formal parameters>):
	return <return expression>
```
Calling User-Defined Functions
- Add a local frame, forming a new environment
- Bind the function's formal parameters to its arguments in that frame
- Execute the body of the function in that new envirment
```
from operator import mul
def square(x):
	return mul(x, x)
square(-2)
```
![[Pasted image 20231023224142.png]]

Looking Up Names in Environments
- An environment is a sequece of frames
- A name evaluates to the value bound to that name in the earliest frame of the current encironment in which that name is found
**E.g**., to look up some in the body of the _square_ function:
- Look for that name in the local frame
- If not found, look for it in the global frame.
	(Built-in names like "max" are in the global frame too, but we don't draw them in environment diagrams. )	

Multiple Environments in One Diagram
- Every expression is evaluated in the context of an environment. 
- A name evaluates to the value bound to that name in the earliest frame of the current environment in which that name is found. 
![[Pasted image 20231026120844.png]]
*Names Have Different Meanings in Different Environments*

Conditional statements
- `S statement is executed by the interpreter to perform an active`
- ![[Pasted image 20231030152704.png]]

iteration example
The Fibonacci Sequence
![[Pasted image 20231030154111.png]]

![[Pasted image 20231030154857.png]]
Logical Operators
To evaluate the expression \<left\> and  \<right\>
- Evaluate the subexpression \<left>
- If the result is a false value v, then the expression evaluates to v
- Otherwise, the expression evaluates to the value of the subexpression \<right>

Higher-Order Function
Generalizing patterns with Argument
Generalizing Over Computational Processes

**Functions as return value**
![[Pasted image 20231030163043.png]]
![[Pasted image 20231030163155.png]]

The Purpose of Higher-Order Functions
- Functions are first-class: Functions can be manipulated as values in our programming language. 
- Higher-order function: A function that takes a function as an argument value or returns a function as a return value
- Higher-order functions:
	- Express general methods of computation
	- Remove repetition from programs
	- Separate concerns among functions

**env for Nested**
![[Pasted image 20231107124335.png]]
![[Pasted image 20231107125036.png]]
- Every user-defined function has a parent frame (often global)
- The parent of a function is the frame in which it was defined
- Every local frame has a parent frame (often global)
- The parent of a frame is the parent of the function called
How to Draw an Environment Diagram
- Create a function value: func \<name>(\<formal parameters>) \[parent=\<parent>]
- Its parent is the current frame. 
- ![[Pasted image 20231107125738.png]]
- Bind \<name> to the function value in the current frame
- When a function is called:
	- Add a local frame, title with the \<name> of the function being called. 
	- Copy the parent of the function to the local frame: \[parent=\<label>]
	- Bind the \<formal parameters> to the arguments in the local frame. 
	- Execute the body of the function in the environment that starts with the local frame. 

Local Names are not Visible to other(Non-Nested) Function
![[Pasted image 20231107130545.png]]

**Function Composition**
![[Pasted image 20231107153940.png]]
**Lambda Expression**
![[Pasted image 20231107154424.png]]
![[Pasted image 20231107154817.png]]
**Currying**
![[Pasted image 20231107155211.png]]
![[Pasted image 20231107155259.png]]

##### Sound
![[Pasted image 20231113152605.png]]
