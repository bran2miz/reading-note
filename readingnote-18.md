# Reading 04 - React and Forms

1. What is a ‘Controlled Component’?
  The value that is managed by react of an input form element.

2. Should we wait to store the users responses from the form into state when they submit the form OR should we update the state with their responses as soon as they enter them? Why.
  We should update the state with responses as soon as they enter them. Event handlers in react will run on every typed key and updates the state in react (the value also updates).

3. How do we target what the user is entering if we have an event handler on an input field?
  First set the state in the constructor using the *event.target.value* method. Then when you return the input field to render it, the value of input would be the setState (this.state.value).

The Conditional (Ternary) Operator Explained

1. Why would we use a ternary operator?
  To condense code, specifically for conditional statements.
    ie. if/else statements and for loops. (?=if, :=else)
2. Rewrite the following statement using a ternary statement:
  if(x===y){
 console.log(true);
  } else {
 console.log(false);
  }
**Answer**
  (x===y) ? console.log(true) : console.log(false);

## Things I want to know more about

Should we wait to store the users responses from the form into state when they submit the form OR should we update the state with their responses as soon as they enter them? **Why.** still confused about the why

[<==BACK](README.md)