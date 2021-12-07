# Reading 2 - Testing and Modules

## In Tests We Trust - TDD with Python

**Unit Tests** - code to monitor the input, output and behavior of code.

**TDD**- *test-driven-development*
-the action to write test first before starting to code.

**AAA** - *Arrange-Act-Assert*
-**Arrange**-compartmentalize the data that is being utilized for the code.
-**Act**- actually putting into effect the tested code
-**Assert**- check if the output matches the expected results.

**Cycle**- comprised of *three* steps:
1. Write test to fail
2. Write feature and make test check correctly (green-light)
3. Refracturing the code at the end.

*note* it is important to **Think about software design before anything that you do with testsing**

## If name equals main

### Why it is needed

If the module is part of the primary program, it must set the __name__ with a key/value pair and equal to "__main__". However, if it is part of a different module, set the __name__ to that particular module's names.

- In python, the files can be *recycled* or completely *separate* programs.

## Recursion

**Recursion**- when a function is called either from itself or relatively from somewhere else.

[source](https://www.geeksforgeeks.org/recursion/)

Example of *direct* recursion:

  void directRecFun()
    {
      // some code..
      void directRecFun();
      // some code..
    }

Example of *indirect*(calls another function within it) recursion:
  
  void indirectRecFun1()
  {
    //some code..
    indirectRecFun2();
    //some code..
  }
  void indirectRecFun2()
  {
    //some code..
    indirectRecFun1();
    //some code..
  }

**Tailed** recursive- the recursive call is at the end when the function runs.

### Disadvantages and Advantages of utilizing recursive

**Disadvantages**:
1. More space is needed
2. More time is needed

**Advantage**- clean and simpler technique for writing code.

## What on Earth is Recursion?

ie factorial(n) = n*factorial(n-1)
**endless succession**

factorial(1) = 1

fact(4) = 4 x 3 x 2 x 1

Recursively (need stack) or Iteratively

**note** factorial will *not* work for negative integers

In the example in the video, it shows how recursive is used, and how the code will run until the if statement is true and stops the code. Really enjoyed the real life example the professor used with how recursive stack using the rings.

[<==BACK](README.md)
