# Putting it all together

## React Docs - Thinking in React

1. What is the single responsibility principle and how does it apply to components?
  The single responsibility principle is essentially the idea that a component should only serve one purpose. If the component is ever expanding, it should break apart and spread into different sub-components.
2. What does it mean to build a ‘static’ version of your application?
  To have a 'static' version of your app essentially means that one must have an app that have components that pass data into properties (props).

3. Once you have a static application, what do you need to add?
  *render()* methods.

4. What are the three questions you can ask to determine if something is state?
  a. Are the props being passed down from the parent?
  b. Is the application being altered over the course of creation?
  c. Within state or props within the component, can the data be successfully identified ?

5. How can you identify where state needs to live?
  a. Locate each component and determine what things render based on the state.
  b. Find commonality between all the components by identifying the highest parent component that requires state to be there.
  c. Parent presides over children to own state.


## Higher-Order Functions

1. What is a “higher-order function”?
  Functions "functioning" through other functions.
  By means of return or passing them as arguments.

2. Explore the greaterThan function as defined in the reading. In your own words, what is line 2 of this function doing?
  -The function greaterThan has a value of n. It is returning the another value m, and includes an argument that m is greater than m.
  -The user is creating another variable called greaterThan10 which is equal to greaterThan with the number value of 10. The user than console.logs the variable greaterThan10 that passes another value of 11.

3. Explain how either map or reduce operates, with regards to higher-order functions.
  a. **Map** operates by taking the *high-order* function by applying said function to all the elements to eventually create an entirely new array from the returned values. The map() method has the same length as the parent array, but contents are altered to creat a new form.
  b. **Reduce** takes an element (from the array) and combines it again and again with the current value. According to the article, *reduce* does this in order to "build" value" (source: https://eloquentjavascript.net/05_higher_order.html#h_xxCc98lOBK).

## Things I want to know more about

Reduce() methods

  [<==](README.md)
  