# Basics of HTML, CSS & JS

## Chapter 2 "Text"

**Structural** Markup - elements in the paragraph or heading

**Semantic** Markup - the extraneous features 

### Structural Markup

Heading or **< h>** tag - controls the font- size and part of *structural* markup.
- 6 numeric headngs from 1-6
  - i.e. < h1> (main heading), < h2>, etc, < h6> (subheadings)

**< p>** tag- Paragraph element

**< b>** - **BOLD** tag
  *note*- both the paragraph and the bold element are considered **inline** elements that can be placed within the text itself. 

**< i>** - *italic* tag

**< sup>** - superscript tag
- Suffixes that are used like dates and numbered phrases.
  - ie 3<sup>rd</sup>

**< sub>** - subscript tag
- Suffixes that appear below the sentence line. 

White space - spacing for codes to read html easier
- Essentially, spacing text doesn't really matter in code as the computer treats the sentence within a tag as one value.

**< br />** - line break tag
- Breaks text so all the content after the element appears on the next line. 

**< hr />**- horizontal rules 
- breaks text and adds a horizontal line break in order to separate sections. 

### Visual Editors and Code Views

**Visual Editors**- are word processors that:
  1) Contain heading that are highlighted
  2) Bold and Italic text are highlighted. 

**Code Views**- shows code to edit your webpage in real-time. 
  - ie Live Server in VS Code
- very helpful in seeing the code and the edits within the page. 

### Semantic Markup

**semantic markup**- the extra features

**< strong>** element- similar to the **bold** element
- what specific part of a paragraph that you want highlighted. 

**< em>** element- similar to the *italic* tag.
- lightly highlights part of the paragraph. 

### Quotations

**< blockquote>** - indents the sentence.
  *note* use CSS to do this instead of placing within the HTML document. 

**< q> < /q>** - shorter way to quote a phrase with quotation marks, rather than indentation. 

**< abbr>** element- used to show the actual unabreviating string of words of an acornym. 
  - when the mouse cursor hovers over the word, the actual word phrase fo the acronym appears. 

**< cite>**- citation element
- indicates where the citation is from.
- *italicize* the phrase.

**< dfn>**- definition tag
  - defines the term

**< address>**- address tag 
  - provides the actual address and contact information of the author. 

### Changes to Content

**< ins>** - underline the word or phrase that is *inserted* in the text. 

**< del>**- crosses out the word or phrase that is going to be *deleted*. 

**< s>**- crosses out information that is incorrect. 

## Chapter 10 - Introduction to CSS

### CSS- Cascading Style Sheet

**CSS RULE**- contanins a *selector* and a *declaration*
  - ie: p { font-family:Arial; }
      (p is the selector)   (the delcaration is within the curly braces)

**selector**- class, id, or a specific part of the html document that the coder wants to make visual alterations.

**declaration**- how the coder wants the selector to appear on the page. 

### CSS property and value

**property**- what specifically does the developer want to change. 
  - ie- color, font-size, font-style, add borders, etc. 

**value**- the *value* that the coder wants to assign to a property
  - ie the **actual** color that you want to assign to the selector (green, red, blue, etc).

### External CSS

< link> - to link another page of CSS to the main html document.
  *note* this is the preferred way to organize the web page. 

- link element can include things like:
  1. *href*- way to add the actual link to the CSS (ie link href="mystyle.css")

  2. *type*- what type of document that the page is directing towards. 
    ie. style/css

  3. *rel*- the **relationship** between the two pages being linked together.
    ie "stylesheet".

### Internal CSS

**internal CSS**- one can add CSS directly to the html document.
  *more specfically* add the **< style>** element within the **< head>** element.

**< style>** element- should include the type of document, just like external CSS. 

### CSS Selectors

**Universal** selector- all elements under one umbrella.
  - *{}

**Type** selector- type of element 
  - ie h1, h2, h3 {}

**Class** selector- **class** attribute needs to be *defined* in the element.
  - ie p.note {}, .note- class name is implemented within the beginning tag of the element that the user wants to change.

**Id** selector- uses a #whatever {}
  - affects elements with an id of the phrase "whatever". 

**Child** selector- couples together an element that has the same *child* within said element. 
  - ie li> a {}- target a elements that are within an < li> element. 

**descendant selector**- targets an element that is within another element.
- Descendant selectors aren't solely exclusive in including the child of the selected element. 
  - ie. p a {}

### CSS Rules

 *last* rule- the latter rule presides over the previously included rules in the text. 

 *specific* rule- a more specific selector will preside over a less specific one.

 *inheritance*- apply to a more broad element (ie < body>), then most likley the child element will apply that selector. 

 ## Chapter 2- Basic JavaScript Instructions

### Statements

**statements**- each *statement* is a part of a step-by-step instruction of code in JavaScript. 
- Statements should always end with a semi colon.
- Each statement starts on a new line. 
- Statements include *code blocks* using the curly braces {}.

**Comments** (//) - two backspaces
- Comments are used to respond to things like what exactly is the code doing without disrupting how it runs. 

### Variables

**Variables**- where the data is stored. 
- Variables are data the coder wants to be rememebered.
- Data can change each time a script is initiated. 
- Variables can be represented as umbers or other kinds of data, similar to algebra. 

**DECLARING A VARIABLE**- define the variable with a unique name. Then assign a value to that variable. 
  ie var (or let) keyword;
  (var or let is the variable keyword) (keyword is the variable name)

**ASSIGNING A VALUE TO THE VARIABLE**- invoke it using just the variable name and not the actual value.
  ie var (or let) keyword= 3;
  (the equal sign is an assignment operator) (the number 3 is the variable value)

**Changing value of Variable**- no need to use var or let to change the variable.
- add *variable* name and the *new value*.

### Data Types

**numeric** data type- the actual numerical value.

**string** data type- use single quotes and a phrase. 

**boolean** data type- true or false. 

Shorthand- makes it easier to type code out in JavaScript.
  *note* not the preferred method; pretty difficult to follow.

### Rules for Naming Variable. 

1. Start with a letter, dollar sign ($), or (_) underscore. 

2. Don't use a (-) dash or a period in the variable name. 

3. Case Sensitive

4. Don't use keywords or reserved words
  ie. naming the variable (var or let)

5. Use a name that describes the information the variable is storing. 

6. If using capital letters, only use one after the first lowerCase word. 

### Array

**Array**- ability to store *lists* as values. 
  *note* use [] brackets and a lists of numbers, strings, and/or booleans. 

  *Example:*
    var colors;
    colors= ['white', 'black', 'custom'];
    var el = document.getElementById('colors');
    el.textContent = colors[0];

In the example: 
- variable has a return value of 0
- 0 is the starting value
- Therefore, it would return the string 'white'.

**Changing Value in Array**- simple include, after the array,
1. Variable Name
2. Value that is to be changed
3. New Value

### Expression

**Expressions** add varaibles together to form a single value. 
- *Assign* a value to variable. 
- Adds two or more variables and pushes a single value. 
- There are two types of expressions. 

### Operators

**Operators**- one value from multiple values. 
- Essentially, combines, assigns, or arithmetizes values into one value. 

*String* Operator- adds strings by two or more values. 

*Arithmetic* Operator- mathmatical equations. 

## Chapter 4- Decisions and Loops

*Decision Making*- asking the question of "What Path to Take Next"

**Decisive Factors**
1. Expression is ran and returns a value. 
  *note* if the expression is true, the code tells the computer to essentially "run the code". 
2. Conditional Statement- what the next step will be.
- Use **if/then/else** statements 

### If/Then/Else

**if** statements- *if* code conditions are all good

**then** statements- *then* the code runs some expression

**else** statements- *else* the code will do something different. 

### Comparison Operators

**Comparison** Operators- retun single values of *true* or *false*

== - is equal to
!== - is **not** equal to 
=== - **strict** equal to 
!== - strict **not** equal to
> - greater than
< - less than
>= - greater than or equal to 
<= - less than or equal to

Result will be a boolean that runs true or false
  - ie score >= pass
    - score and pass are the operands
    - the entire expression is an enclosing expression
    - the greater than or equal to symbol represents a comparison operator 

### Logical Operator

**Logical** Operator- compare two or more comparison operators. 

1. && - logical *and*
- runs more than one codition as true or false. 

2. || - logical *or*
- runs at least one condition

3. ! - logical not
- runs one Boolean Value and reverses its value. 

### Conclusion

- **if** statements- checks whether an expression is *true*.

- if the condition value is *true*, then it will run the sequence. 

- *else* statements- if the *first* condition is not met, run a separate sequence. 

[<== Back] (README.md)
