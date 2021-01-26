# Javascript chapter 10 Error Handling and Debugging

Execution Context: A concept the js interpreter uses to track state. There is a global execution context and within a functions are more.


### Execution Context and hoisting

Every new execution context comes with it 2 phases of activity that happen..
1. Prepare phase- `the new scope is created. Variables, functions, and arguments are created. The value of the this keyword is determined.
2. Execute phase- `Now it can assign values to variables. Reference functions and ru ntheir code. Execute statements. 

Each execution context creates its own `variables object`

Imagine that each function is a nesting doll.
The children can ask the parents for information in
their variables. But the parents cannot get variables
from their children. Each child will get the same
answer from the same parent.

If a parent is not found in the variables abject for the current execution context it can look in the parents execution context, or further up the stack. 
`ideally` variables are created in the function that uses them for performance sake. 

### Exception handling
Exception-handling code should inform users when there is a problem. 

When the interpreter comes across an error it will look for error-handling code. If none is found it will go higher 
up the stack looking for error handling code until it reaches the global execution context and creates an error object and the script stops.

#### Properties of an error object when created

| name       | type of exection         |
|------------|--------------------------|
| message    | description              |
| fileNumber | Name of js file          |
| lineNumber | line number of the error |

#### 7 Different types of errors

| Object          | Description                                                     |
|-----------------|-----------------------------------------------------------------|
| Error           | Generic error- the other errors are all based upon this error   | 
| syntax error    | syntax has not been followed                                    |
| reference error | tried to reference a variable that is not declared/within scope |
| TypeError       | An unexpected data type that cannot be coerced                  |
| RangeError      | NUmbers not in acceptable range                                 |
| URIError        | encodeUrI(), decodeURi, and similar methods used incorrectly    |
| EvalError       | eval() FUNCTION used incorrectly                                |



### Dealing with errors

1. Debug the script to fix errors
1. Handle errors using `try, catch, throw, finally` statements


