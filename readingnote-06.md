# Reading 6 - Problem Domain, Objects, and the DOM

## Chapter 3 - Object Literals

**object**- gather variables and function under one roof.

**property**- a variable is called a property if it is included in an *object*.

**method**- a function is called a property if it is included in an *object*.

**key**- names of the properties within the object.

**Dot Notation**- used to retreive within an object a *property* or *method*.

## Chapter 5 - Document Object Model

**DOM** - Document Object Model
How the browser should:
-establish a web page structure within the html document
-how the JavaScript will update the page based on different alterations and factors.

### Document Node

**DOM** node- everything within html

**Document** node- represents the entire content of the site.

**element** node

**attribute** node- part of the element and not a "child" of the element. 

**text** node- accessing elements through *methods*.
-getElementbyId('one')

**DOM queries**- method that locate elements within the DOM.
-querySelector('CSS Selector')- select one or more elements.

getElementsByClassName('class');

getElementsByTagName('tagName')

querySelectorAll('CSS selector')- ('CSS selector') is considered a *parameter*.

document.getElementbyId('one')
-object= document
-.= member operator
-getElementbyId('one')= method (the method being used to access something in the node)

**NodeList** - *DOM* method
-can retreive and return one or more elements.

### Selecting Elements From NodeList

**item()** method- returns singular node from the NodeList
1.Select elementby whatever method and store it in the variable.
2.Search elements with the .length property to locate the number of elements that have the same *class*, *tag*, or *id* name.
3.Define the variable and retreive desired element.

**array syntax**- retrieves specific nodes with the same method as *item()*, however it just uses [] brackets for items in the array.

### Looping Through Node List
-ie for loops
  varhotItems = document.querySelectorAll('li.hot');
  for(let i=0; i< hotItems.length; i++) {
    hotItems[i].classname = `cool`;
  }
  NodeList - list items that have a class attribute with value `hot`.
  querySelectorAll()- method in which items are being collected.
  .length- how many times loop should run.

### Previous and Next Sibling

Previous and Next Sibling- property method that locates the *previous* or *next* sibling of a node.
-to change value of a sibling: variableName.classname = `the attribute`

First and Last Child finds *first* and *last* child of the specified element.
-to change value: childVarName.setAttribute(`____`,`_____`)

### Changing Text Node

1.Get list item by naming the variable and declaring it with an object (document) method.
2.Through nodeValue, the text content is placed in another variable.
3.Use .replace to replace text and parameter with the actual value to start and the desired changed value second.
4.Update value.

**node value**- property returns text from the text node.

**.pop** - removes last element of an array

**.shift**- removes first element of array
-repostions the indexes of all other remaining items

**.push**- add to the end of an array
-can add multiple elements (even after using a .push before using . push)

**.unshift();**- inserts an element into the front of the array and reorders all elements after it.

**.splice();**- (start index, number of items to remove what to add)

## Problem Domain

-learning and understanding what the problem is.
  -Easier to get code once the problem domain is established by the coder. 
-Make the problem domain easier
-Become better at solving problem domains.

[<== Back](README.md)