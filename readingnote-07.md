# Reading 7 Object-Oriented Programming, HTML Tables

## Chapter 6 - Tables

block in grid = table cell

**< table>** element - table is made through this element with a layout consisting of multiple rows.

**< tr>** element - table row element where the row of a table begins.

**< td>** element - table data element that includes a table with specific items that are within individual cells.

**< th>** element- table heading element on top of the table or on the side.

**colespan** - an attribute that is within a < td> or < th> element that allows a cell to "span" across multiple rows.

**rowspan** - an attribute that is within a *< td>* or *< th>* element that allows a cell to "span" down the table.

**< thead>** - element in which the top heading is located in.

**< tbody>** - body table cells are stored within the *< tbody>* element.

**< tfoot>** - element in which the bottom footer is located in.

## Chapter 3 - Function Methods and Objects

var hotel = new Object();
  hotel = new object
  object() = constructor function

hotel.name = `Quay`;
hotel.rooms = 40;
hotel.booked = 25;
hotel.checkAvailability = function {
  return this.rooms - this.booked;
};

Update certain properties, specficially the value, the dot notation or the array brackets are implemented.

**Delete** keyword - deletes property

### Construction Notation

**instances**- constructor function
   ie let quay hotel = Hotel(`Quay`, 40, 25);

**+=** operator is used to add content to an existing variable.

**This** keyword - indicates one *object*

**Arrays**- an array is an *object*
-*index* number- Array have "keys" for every value.

**Built in Objects**
1.Browser Object Model
  -Window
  -Document - Web Page
  -History
  -Location
  -Navigator - information of browser
  -Screen

2.Document Object Model
-html

3.Global JavaScript Objects
-strings, number, booleans
-date, math, regex

**Date** Object- Date() is used as a obejct constructor method.

[<== Back](README.md)