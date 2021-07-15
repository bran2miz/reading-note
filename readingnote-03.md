# HTML Lists, Control Flow with JS, and the CSS Box Model

## Chapter 13

### Boxes

**Box Dimensions**- use width and height properties to modify the size of the box. 
-**important**- use pixels, percentages, or ems to assign a value to the width or height. 
  -*note*- percentage changes the size of the box in relation to the browser window, while em is based on the text-size.

### Limiting Width

Limiting Width
-can help the text's legibility.
-to expand or shrink the page based on the user's browser window, use *min-width* or *max-width*.

**Min-Width**- clarifies how small the user's box should be when condensing the screen's width. 

**Max-Width**- specifies how large a box can be when enlarging the browser.

### Limiting Height

Limiting height is similar to *limiting width* just with height dimensions.

**min-height**- squeezing the page vertically. Affects how small the box will get.

**max-height**- specifies how large a box can be when enlarging the box up and down.

### Overflowing Content

**overflow**- property that helps contribute to "overflowing" content within the box.

**hidden** property- just hides overflowing content.

**scroll** property- adds to the box a scrolling feature to see the rest of the content that could not fit in the defeault box.

### Border, Margin, Padding

#### Border

**Border Properties**- box has a border already implemented.
-border properties separate other boxes.

**border-width**- border property to widen the border.
-3 different values of border-width.
1. Thin
2. Medium
3. Thick
-4 Values to border location using pixels (px).
  -ie 10px, 30px, 10px, 30px (top, right, bottom, left)

**border-style**- stylized border property.
-Examples include
  -solid
  -dotted
  -dashed
  -double
  -groove
  -ridge
  -inset
  -outset
  -hidden

**border-color**- property that colors the border.

**shorthand border**- can assign different property values on line.
  -ie p {100px red}

#### Padding

**Padding**- space between border and the acutal content within the box.
-Specified in pixels.
-Can specify where padding goes.
  -ie *padding-top* or padding: 10px 5px 3px 1px;

#### Margin

**Margin**- beyond edge of border
-allows spacing between boxes.
-allows the text legibility.

### Center Content

**Center Content**- content is centered by setting the left and right margin to auto. 

### Display

**display** property- transform an inline element into a block level element or a block-level element into an inline one.

**none** attribute- hides element completely without the addition of any space to replace it.

### Visibility

**visibility** property- hide boxes but leaves a space to indicate where that content would be. 

### CSS3: Border-Image

**Border-Image**- image border outside of box

**box-shadow** property- allows the addition of a shadow to the box
-add 3 values (for either the left right top or bottom) and a color to whatever side to place the shadow.

### CSS3: Border-Radius

**Border-Radius**- *CSS3* introduced this new feature

**Rounded Corners**- a border with a rounded shape.

**elliptical shape**- a border with a customized, complex shape. 

## Loops

**LOOP**- checks the expression
-if the statement is true, then run the code.
-repeats until the condition returns as false. 
-Three types of loops

### For Loops

**for** loops
-runs the code for a set amount of times
-loops through a set of values in an array

### While Loops

**while** loops
-the loop continuously runs until the condition runs false.

### Do While Loops

**do while** loops
-runs whatever is inside the curly braces, regardless if the condition is false.
-condition is placed after  the statement.

[<== Back](README.md)


