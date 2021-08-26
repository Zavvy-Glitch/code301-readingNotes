# Reading 9

## Functional Programming

Notes taken from: [Concepts of Functional Programming in JavaScript](https://medium.com/the-renaissance-developer/concepts-of-functional-programming-in-javascript-6bc84220d2aa)

1. What is functional programming?
    - Functional programming is a programming paradigm. A style of building the structure and elements of computer programs that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data.

2. What is a pure function and how do we know if something is a pure function?
    - Returns the same result if given the arguments (Deterministic)
    - Does not cause any observable side effects
    - Pure functions are stable, consistent, and predictable. Given the same parameters, pure functions will always return the same result.

3. What are the benefits of a pure function?
    - The code’s definitely easier to test. We don’t need to mock anything.

4. What is immutability?
    - is where the state cannot be changed after it's been created

5. What is Referential transparency?
    - A function that constistently yields the same result for the same input.
    - Pure function + Immutable Data = Referential Transparency

## Node.JS Module & Require

Notes taken from: [Node.JS Tutorial for Beginners #6 - Modules and Require](https://www.youtube.com/watch?v=xHLd36QoS4k)

1. What is a module?
    - A componentized file that will contain the code of a certain functionality for the application.

2. What does the word ‘require’ do?
    - Allows you to use a module in a global setting

3. How do we bring another module into the file the we are working in?
    - Example: const variableName = require(./filepath)


4. What do we have to do to make a module available?
    - Example: module.exports = functionName
