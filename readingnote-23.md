# Reading 09 - Functional Programming

## Functional Programming Concepts

1. What is functional programming?
  Functional programming formulates the structure and elements of computer programs; data processing is evaluated as mathematical functions and does not include alteration of state.

2. What is a pure function and how do we know if something is a pure function?
  A pure function is "deterministic" in that it will return the same thing when passed the exact matched arguments. We can also know if something is a pure function if it does produce any negative after effects. They are *stable*, *consistent*, and *predictable*.

3. What are the benefits of a pure function?
  -Easier to test
  -No need to mack a copy or anything of the sort.
4. What is immutability?
  Once the data is immutable, the state cannot be changed once it is created.

5. What is Referential transparency?
  Pure functions + immutable data = **referential transparency**

## Node JS Tutorial for Beginners #6 - Modules and require()

1. What is a module?
  A **module** is sort of like a *component* in REACT; a different individual part of the back end that has different functionality in the app.

2. What does the word ‘require’ do?
  Similar to import in REACT, the require function on Node.JS brings other modules into wherever you need to pass it into. However, you have to define specifically what other areas in you code you want to make the module available.

3. How do we bring another module into the file the we are working in?
  let counter = require('./count'); (in place you want to add the module into)

4. What do we have to do to make a module available?
  module.exports = counter; (specify in the count.js file)

## Things I want to know more about

What are more benefits other than easier test for pure functions?

[<==BACK](README.md)
