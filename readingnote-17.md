# Reading 03 - Passing Functions as Props

## .map()

1. What does .map() return?
  The .map() returns a newly created array and elements. As a result of the .map function, the new elements are created.

2. If I want to loop through an array and display each value in JSX, how do I do that in React?
  Loop through an array by first creating the array
    ie. const numbers = [1,2,3,4,5];
  Then create a variable that utilizes the .map() function to return elements.
    ie. const listItems = numbers.map((number) => <li>{number}</li>); )
  Afterwards, to render to the DOM, we use the ReactDOM.render() function and wrap the item that we want to appear.
    ie ReactDOM.render(<ul>{listItems}</ul>, document.getElementById('root)); )

3. Each list item needs a unique ____.
  key

4. What is the purpose of a key?
  Key help identify for React the changes being made (ie what sort of things have been added or deleted). It also provides elements a "stable identity". (source: https://reactjs.org/docs/lists-and-keys.html)

The Spread Operator

1. What is the spread operator?
  Spread operators use three periods before the parameter of a function to enlarge an object into the "lists of arguments" (source: https://medium.com coding-at-dawn/how-to-use-the-spread-operator-in-javascript-b9e4a8b06fab)
2. List 4 things that the spread operator can do.
  1.Copying an array
  2.Combines objects
  3.Adds an item to a list
  4.Coverts NodeList to an array

3. Give an example of using the spread operator to combine two arrays.
  const hello = ['red','blue','yellow','green'];
  const world = [1,2,3,4];
  const totalArr = [...hello,...world]
  console.log(...totalArr)
  // expected outcome: red,blue,yellow,green,1,2,3,4

4. Give an example of using the spread operator to add a new item to an array.
  const fruits = ['apple','banana','grape','cherry']
  const moreFruits = ['watermelon','orange',..fruits];
  console.log(moreFruits);
  //expected outcome: ['watermelon','orange','apple','banana','grape','cherry']

5. Give an example of using the spread operator to combine two objects into one.
  const objectOne = {hello:"Brandon"};
  const objectTwo = {world:"CodeFellows"};
  const objectThree = {...objectOne, ...objectTwo, laugh:'haha'};
  
  console.log(objectThree) // Object {hello:'Brandon',world:'CodeFellows', laugh:'haha' };

## How to Pass Functions Between Components

1. In the video, what is the first step that the developer does to pass functions between components?
  The first step to pass functions between components is to create the function after the state that we are going to alter.

2. In your own words, what does the increment function do?
  An increment is a type of function that takes in a value, called name, and through the use of the arrow method, defines a variable (called ppl) that utilizes the .map() function. Within the .map() function we have a value, called p, that uses the arrow method to loop through the different names; if the p.name unequivocally equals the name within the Component's constructor, increase the count by 1, and return the newly created number (p). To finally set the state, we use the this.state() notation to modify the value people to the increment function's value, ppl.

3. How can you pass a method from a parent component into a child component?

  You use the this.prop (properties) method within the parent component (Person) and define the function that you want to change like this: this.prop *.increment()*.

4. How does the child component invoke a method that was passed to it from a parent component?

  You also want to define within the prop the *name* so that the value is sent back. To do this, within the .prop method, you can also include the this.props.name.

## Things I want to know more about

How does the child component invoke a method that was passed to it from a parent component.

[<==BACK](README.md)
