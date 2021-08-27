# Reading 10

## In Memory Storage

### JavaScript Call Stack

#### Citations for Notes Below: [Free Code Camp](https://www.freecodecamp.org/news/understanding-the-javascript-call-stack-861e41ae61d4/)

1. What is a ‘call’?
    - Single, Function(s) Execution, Function Invocation

2. How many ‘calls’ can happen at once?
    -  One at a time, from top to bottom. It means the call stack is synchronous

3. What does LIFO mean?
    - Last In, First Out
    - It means that the last function that gets pushed into the stack is the first to be pop out, when the function returns

4. Draw an example of a call stack and the functions that would need to be invoked to generate that call stack.
          
         function firstFunction(){
            throw new Error('Stack Trace Error');
              }

        function secondFunction(){
            firstFunction();
              }

        function thirdFunction(){
            secondFunction();
              }

        thirdFunction();

5. What causes a Stack Overflow?
      - A stack overflow occurs when there is a recursive function (a function that calls itself) without an exit point. The browser (hosting environment) has a maximum stack call that it can accomodate before throwing a stack error.

### JS Error Messages & Debugging

#### Citation for Notes Below: [CodeBurst](https://codeburst.io/javascript-error-messages-debugging-d23f84f0ae7c)

1. What is a ‘refrence error’?
    - Common thing when using const and let, they are hoisted like var and function but there is a time between the hoisting and being declared so when you try to access them a reference error occurs, the fact that this happens to let and const is called Temporal Dead Zone (TDZ)

2. What is a ‘syntax error’?
    - Occurs when you have something that cannot be parsed in terms of syntax, like when you try to parse an invalid object using JSON.parse

3. What is a ‘range error’?
    - When you manipulate an object with some kind of length and give it an invalid length and this kind of errors will show up.

4. What is a ‘type error’?
    - This type of error show up when the types (number, string and so on) you are trying to use or access are incompatible, like accessing a property in an undefined type of variable

5. What is a breakpoint?
    - A defining point within your code that anything below the current code block that cannot be executed due to some 'error'

6. What does the word ‘debugger’ do in your code?
    - The breakpoint can be achieved by putting a debugger statement in your code in the line you want to break.
