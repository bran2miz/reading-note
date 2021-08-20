# Reading 13 - Local Storage

userData - stores up to 64kb of data per Domain

web storage= DOM storage
-stores *key*/*value* pairs

*note* use Modernizr in your code to detect HTML5 storage support.
  if (Modernizr.localstorage) {
  // window.localStorage is available!
  } else {
  // no native support for HTML5 storage :(
  // maybe try dojox.storage or a third-party solution
  }

**HTML5 storage**- stores and retrieves data with a key.

**setItem()**- function that overwrites previous value

*note* - instead of using methods and creating parameters within the parenthesis, use square brackets.
  var foo = localStorage["bar"];
  // ...
  localStorage["bar"] = foo;

## Storage Event Object

**key**- named key that was deleted added or altered. A named key is a *type* of *string*.

**oldValue**- previous value that was overwritten. An oldValue has a *type* of *any*.

**newValue**- the new value that is the overwritten value. A newValue has a *type* of *any*.

**url**- a web page that invoked a function(method) that created the overwritten value.

[<==Back](README.md)