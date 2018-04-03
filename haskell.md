Haskell has no statements, only expressions!

- Pure functional programming languages don’t have any statements — no assignments, no jumps.
- Instead, all computation is performed by evaluating expressions

Function applications

- Expressions can contain function calls.
- A function takes argument(s), performs some computation, and produces result(s).

### A model of program execution

- A programmer needs a concrete model for how a program is executed.
- For imperative programs, we can execute statement by statement, keeping track of the values of variables (the stack) and where we are in the program (the program counter).
- Functional programs don’t have statements!
- The mechanism for executing functional programs is reduction.

### Reduction

Reduction is the process of converting an expression to a simpler form. Conceptually, an expression is reduced by simplifying one reducible expression (called “redex”) at a time. Each step is called a reduction, and we’ll use -- > to show the result. 

