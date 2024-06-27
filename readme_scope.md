1. What is scope in JavaScript, and why is it important?
Ans
Scope in JavaScript refers to the context or environment in which variables are declared and can be accessed. It dictates the visibility and lifetime of a variable, determining where in your code a particular variable is valid and accessible.

2. Can you explain the difference between global scope and local scope?
Ans
Variables with global scope are available from all other scopes within the JavaScript code. Variables with local scope are available only within a specific local context (eg. a function)and are created by keywords, such as var , let , and const .


3. How does JavaScript handle scope in functions compared to block-level scope?
Ans
Scope Boundary: Function scope encompasses the entire function body and any nested functions, while block-level scope (with let and const) is limited to the nearest enclosing {} block.

Hoisting: Variables declared with var are hoisted to the top of their function scope, while variables declared with let and const are not hoisted and remain inaccessible until their declaration statement.

4. How do var, let, and const differ in terms of scope?
Ans
var: Function-scoped, hoisted to the top of its function, accessible globally if not in strict mode.
let: Block-scoped, not hoisted to the top of its block, and allows reassignment of values.
const: Block-scoped, not hoisted to the top of its block, requires initialization with a value, and its reference cannot be reassigned (though object properties can be mutated).

5. What are the implications of declaring a variable without any keyword (i.e., no var, let, or const)?
Ans

Variables which are declared without the var keyword are automatically created in the global scope.They can cause several issues such as:
1.Namespace Pollution: Implicit global variables can lead to namespace pollution, where variables     unintentionally overwrite or conflict with each other, especially in large applications.
2.Accidental Modifications: Since implicit global variables are accessible from anywhere, they can be inadvertently modified by unrelated parts of your code, leading to unexpected behavior and bugs.
3.Debugging Complexity: Identifying and debugging issues related to implicit global variables can be challenging because their scope and potential modifications may not be immediately apparent.

6. What is the scope chain, and how does JavaScript use it to resolve variable access?
Ans
The scope chain in JavaScript refers to the hierarchical structure of nested scopes that determines the accessibility of variables and identifiers during runtime. 
The scope chain in JavaScript is fundamental to how variables are accessed and resolved during program execution. It ensures that variables are accessed in the correct scope based on their lexical environment, providing encapsulation and efficient variable resolution. Understanding the scope chain helps developers write clearer, more maintainable code by leveraging JavaScript's scoping rules effectively.

7. What are some differences between lexical scope and dynamic scope? Which one does JavaScript use?
Ans 
Lexical scope and dynamic scope are two different ways of resolving variable access in programming languages.This is what JavaScript uses.
Dynamic scope determines variable accessibility based on the current execution context or the call stack.
Lexical scope offers more predictability and easier debugging because variable access is determined by the lexical structure of the code, making it easier to reason about variable scope.


8. What is a closure, and how does it relate to scope in JavaScript?
Ans
A closure in JavaScript is a combination of a function and the lexical environment within which that function was declared.Closures are directly related to lexical scope because they capture and retain references to variables in their lexical environment (outer scope) at the time of their creation.
 Closures allow inner functions to access variables from their outer scope, even when those variables are not directly passed as parameters or defined within the inner function itself.
 Closures help in achieving encapsulation and data privacy by allowing variables to be accessed and modified only through functions that were originally in the same scope chain.