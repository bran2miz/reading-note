# Reading 2 - State and Props

1. Based off the diagram, what happens first, the ‘render’ or the ‘componentDidMount’?
  'render' occurs before 'componentDidMount' during the process of mounting.


2. What is the very first thing to happen in the lifecycle of React?
  Mounting is the first part of the lifecycle of React.

3. Put the following things in the order that they happen: componentDidMount, render, constructor, componentWillUnmount, React Updates
    1.Constructor
    2.Render
    3.componentDidMount
    4.React Updates
    5.componentWillUnmount (only method in the unmounting phase; 'polishes' the DOM)

4. What does componentDidMount do?

   When the component is formed and implemented within the DOM, componentDidMount happens during the *mounting* phase. This particular method occurs right after it is mounted, and it is the perfect time to *load* or set up network request or start up the DOM. (source: https://medium.com/@joshuablankenshipnola/react-component-lifecycle-events-cb77e670a093).

## Video on State and Props

1. What types of things can you pass in the props?
  You pass the props you want to give to components that are being created or rendered. Similar to passing thing to functions, props are what you want your component to *appear* like; *initialize* your component to. In the video's example, the counter's initial number of zero would be passed into the props. Storing a title and subtile can also be passed and stored in the props. Props are similar to passing things globally like arguments to functions.

2. What is the big difference between props and state?
  State is *within* the component, whereas props are what are being passed *into* a component.

3. When do we re-render our application?
  When the **state** is altered or modified, it re-renders the section within the application.

4. What are some examples of things that we could store in state?
  If for example, someone wanted to change a particular aspect in one's application, it would be stored within the state, so that the application is re-rendered. In the video's example with the counter application, the numbers continually re-render and updates within the state, based on user input. A form is also a great example; it is constantly updated/re-rendered and needs to be able to store information (user input, checkboxes, etc). (source: https://www.youtube.com/watch?v=IYvD9oBCuJI)

## Things I want to know more about

When to Use *state*(inside) vs *props*(outside).

Actual examples (understand the concepts, but would like to see the actual difference between state and props)

[<==BACK](README.md)