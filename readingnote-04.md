# HTML Links, JS Functions, and Intro to CSS Layout

## Chapter 4 - Links

**URL** - Uniform Resource Locator

**< a>** element - to implement a link into a webpage

**href** - the attribute within the tag where you store the link.

the actual link is known as the *absolute URL*

**Relative** Url - used link to not only other websites, but also other pages on page.

### Email Links

**email links** - email the page creator or whomever. 
  -ie < a href = "mailto: bran2miz@gmail.com">

### Link to New Window

**target** attribute- link that opens a new window
-the value should be blank. 

### Link on Same Page

To *link* on the same page, use selectors as the href.
-ie < a href= "#interlude">

## Chapter 15 - Layout

### Block-level & Inline Box

**Block-level** elements - begin each section on a new line.
-Examples elements:
  1.< h1>
  2.< p>
  3.< ul>
  4.< li>

**inline** elements- elements that can be implemented within the text itself.

**containing** or **parent** element - a *block-level* element that can "contain" another *block-level* element inside of it.

### Element Position

**Normal Flow** - appears naturally, with one paragraph following the next, including a space between each *block-level* element.

**Relative Positioning**- all *block-level* elements except the selected one remains the same.
-can shift the position of the *block-level* element top, right, bottom, or left.

**Absolute Positioning**- element is positioned so that it doesn't move as the user scrolls through the webpage. 
-Out of the *normal-flow*.

**Box Offset**- where a specific box should be positioned.

**fixed positioning**- does not move form the position the element was placed at.
-out side of *normal flow*.

**floating element**- positioned to the far left or right. 
-all other *block-level* elements can flow through the floating element. 

## Chapter 3 Function, Methods, Objects

**Functions**- combines expression statements into one.

When someone **calls a function**, the developer is telling the computer to execute the task.
-call the function in html using the < script> element
-add the function within JS

**Parameters**- information within a function that can perform a function.

**Return Value**- response from invoking a function.

**Function Declaration**- name, keyword, code-block
- ie function sayHello() {
   document.write('Hello');
}
- function= function keyword, sayHello()= function name, code within the curly braces= code-block.

**Calling the function**- In order for the code to run, we must call the function by writing code within the curly braces, telling what function is to be executed.

**Parameters**- similar to variables
-embedded in the parathesis of the function name.
-specific information for the function.

**Values**- values in parameters are *arguments*.

**Arguments** can be implemented in a function as *values* or *variables*. 

**funnction declaration**- can call a function to be carried out later. 
- need a *named function*

**Variable Scope**- the function can only be performed once a person declares it within a function. 

**Two types of Variable Scopes**
-*Local* scope- can only be accessed within the function
-*Global* scope- can be accessed anywhere with in the JS. 

## Paired Programming

**Pair Programming**- two coders sharing a common-area to perform tasks together.

### Driver and Navigator

The *driver* types, while the *navigator* does all the writing code, text editing, etc.

### Reasons to Use Paired Programming

1. Greater Efficiency- "two heads are better than one".
-come up with ideas and solutions together.

2. Engaged Collaboration- far better driven and more attentive to the task at hand.

3. Learn from fellow students- allows for better learning tips and tools for both developers to gain access to.

4. Social Skills- having a better grasp at communication and working together.

5. Job interview readiness- employee and studen paired programming allows companies to see how you work with others.

6. Work Environment Readiness- Code Fellows helps skip the step of paried aptitude, as opposed to computer science graduates who have not do this.

[<==Back](README.md)

