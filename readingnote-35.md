# Reading 7 - Game of Greed 2

## Python Scope

### Scope

**scope**- how variables and names are found in one's code.

*Global* vs *Local* scope

**Global**- defined names are available anywhere in one's code

**Local** - defined names are only avaiable within the particular code within the scope.

a scope is defined by the **LEGB** rule

### LEGB (Local Enclosing Global Built-in)

**Local** scope- names defined inside the function, and can only be seen from that contained function.

**Enclosing** scope (non-local)- encompassing scope for the outer function of nested functions.

**Global** scope- names are defined and are available anywhere in the code.

**Built-in** scope- formed when the script is executed or an interactive session is opened.

#### Local Scope

**Local** scope- created when function is called.
-new local scopes are formed when a function is called.

#### Enclosing or non-local scope

**Enclosing** scope- function within a function (nesting)
-takes form of local scope of any enclosing function's local scopes.
-Names within enclosing Python scope are called non-local names

### Python Keywords

#### Global

A *global* statement modifies behavior and defines a variety of names that will be altered to be *global* names.

statement format- start with global keyword
-1 or more names separated by commas


#### Nonlocal

A *nonlocal* statement modifies behavior and define names that will considered nonlocal.

statement format- start with nonlocal keyword.
-1 or more names separated by commas

*note* can't use nonlocal outside of a enclosed function

### Closures

**Closures**- nested function that contains information about the parent or enclosing scope.
-retain state information.

### Built-in functions

**globals()**- returns a reference to current global scope.

**locals()**- updates and returns a dictionary containing information on the current state of the local Python scope.

## Don’t be CONFUSED by BIG O notation anymore!

**Big O**- At the basic level, *Big O* is considered to be a measure of how long an algorithm takes to do something. It also considers how much memory does it take to run the code successfully.

**Time**- how an algorithm will respond to an increasing amount of data.

**Space complexity**- when the computer runs out of memory.

Big O - **worst case** scenarios of the length of time it will take to run the code with how much space.

### Complexity cases

**O(1)**- constant running time

**O(logn)**- logarithmic running time

**O(n)**- linear running time

**O(nlogn)**- Log-linear running time

**O(n^2)**- Polynomial running time

**O(c^n)**- Exponential running time

### Examples

O(logn) - scales really slowly for inputs which is a good thing.

Quadratic- takes a long time based on inputs (not manageable).

### Binary Search

**Binary search**- takes a list(ascending order) and has unique values.
-halves the length of the list, repeats the halving until it gets to one constituent. Then it will tell you if it contains the number you are looking for.
-looks at the middle component of list and then narrows it down until it gets the right number.

[<==BACK](README.md)