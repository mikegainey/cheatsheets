## Notes from the FutureLearn course: Functional Programming in Haskell, University of Glasgow
 


### Haskell has no statements, only expressions!

- Pure functional programming languages don’t have any statements — no assignments, no jumps.
- Instead, all computation is performed by evaluating expressions

### Function applications

- Expressions can contain function calls.
- A function takes argument(s), performs some computation, and produces result(s).

### A model of program execution

- A programmer needs a concrete model for how a program is executed.
- For imperative programs, we can execute statement by statement, keeping track of the values of variables (the stack) and where we are in the program (the program counter).
- Functional programs don’t have statements!
- The mechanism for executing functional programs is reduction.

### Reduction

- Reduction is the process of converting an expression to a simpler form. Conceptually, an expression is reduced by simplifying one reducible expression (called “redex”) at a time. Each step is called a reduction, and we’ll use -- > to show the result. 
- Reduction is important because it is the sole means of execution of a functional program. There are no statements, as in imperative languages; all computation is achieved purely by reducing expressions.

### The Church-Rosser theorem ###

- Every terminating reduction path gives the same result
- This means that
  - Correctness doesn’t depend on order of evaluation.
  - The compiler (or programmer) can change the order freely to improve performance, without affecting the result.
  -  Different expressions can be evaluated in parallel, without affecting the result. As a result, functional languages are leading contenders for programming future parallel systems.

### How function application works
- Functions are the main way to abstract and encapsulate computation in Haskell.
- A function definition is an equation, e.g. f=∖x→x+1
- The left hand side gives the name of the function;
- The right hand side (the “body”) is an expression giving the formal parameters, and the value of the application. The expression may use the parameters.
- An application is an expression like f 31, where 31 is the argument.
- The application is evaluated by replacing it with the body of the function, where the formal parameters are replaced by the arguments. 

### Lists
- A list is a single value that contains several other values.
- List elements can be expressions. They are evaluated only when they are used.
- [5,3,8,7]  !! 2    -- > 8
- Recommendation: avoid using (head) and (tail), because you want to avoid undefined values so your programs are robust. Unless you’re doing something really sophisticated, you’re better off with pattern matching. There are, however, some cases where they are appropriate.

