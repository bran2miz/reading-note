# Reading 3 - FileIO & Exceptions

## Read & Write Files in Python

**File**- sequential group of bytes that are utilized to store data.

*Files* are comprised of **three** parts:
1. Header - the "about me" of the file
2. Data - content made by the editor
3. End of File - specific character that marks the termination of said file.

**File Path**- string that serves as the specific target of that file.

The file path is comprised of *three* parts:
1. Folder Path - location of the file folder. Folders are divided by a forward slash (/) or backslash (\ )
2. File Name - actual name of the file
3. Extension - includes a period and then the file type

### Open and Close File in Python

**open()** - built in function that opens a file

*note* - make sure file that is opened is properly closed

.close() - close method but also use:
  try:
    #something here
  finally:
    something.close()

*note* use the *with* open() because it auto closes the open file.

### Reading and Writing Opened Files

**.read(size=1)**- reads file based on "size of bytes.

**.readline(size=1)**- reads most size number of characters.

**readlines()**- reads the last parts of the line from file and transforms them into lists.

### Method to Write a File

**.write(string)**- writes string to file

**.writelines(seq)**- writes sequence to file

**__file__**- pathname of file where the module was loaded

### Create Context Manager

**__enter__()**- invoked when implementing *with*

**__exit__()**- invoked when implementing *with block*

## Python Exceptions

**syntax error**- parser identifies the wrong type of statement

**exception error**- the code is syntactically correct, but still runs an error.

**raise**- can bypass error and add exception
  ie raise Exception(something here)

**assert**- asserts that a particular condition is met.

**try** and **except** Block- same concept as the try and catch method learned in course 301 JavaScript.

**try** this or else **except** the error and write and statement.

**else**- used after try and except that is ran only if exceptions are absent.

**finally** - bypass everything and always runs the code.

[<==BACK](README.md)