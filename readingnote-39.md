# Reading 11 - Data Analysis

## What is Jupyter Lab

**Jupyter Lab** - allows user to work w/ documents like Jupyter notebooks, text editors, terminals and custom components.

text editor- syntax highlighting and configurable indentation.

terminal- full support for system shell like power shell

## Common Formats

### Image

**image**- supported as stand alone files

#### Shortcuts

**-=** - zoom in/out

**[]** - rotate left/right

**0**- reset

.pdf and html viewed easily

### Jupyter Notebooks

**notebooks**- new way to work with data and code seamlessly together

#### Command mode

**command mode** -easy steering and alternations of notebook framework.

Framework of notebook comprised of cells that contain data and code.

#### Shortcuts

**^a** - adds a cell above

**b** - adds a cell below

**v** - paste cell

**x** - cut a cell

**c** - copy cell

**dd** - delete cell

**z** - undo

**shift + z** - redo

**y** - change format of cell to code

**m** - change format of cell to markdown

##### Markdown

**---** - creates a horizontal line

**`something`** - inline code

$ x^2 $ - equations

##### Python

**shift + enter** - run cell (code)
-if you can change a value later in another cell, it updates the output in the kernel.

---

## Numpy Tutorial

### NumPy

**NumPy** - common data analysis package.
-alleviates large workflow and speeds up processing time.

### Lists Of Lists for CSV Data

  import csv 
  with open('winequality-red.csv', 'r') as f:
    wines = list(csv.reader(f, delimiter=';'))
    open file with above statement

  -- import csv library --
  --create a new csv.reader object--
    --pass keyword argument to ensure records are parsed.
    - list gets rows from file
    - assign results to variable

Another Example:

  qualities = [float(item[-1]) for item in wines[1:]]
  sum(qualities) / len(qualities)

  --retrieve last element from each row after header row--
  --convert each extracted element to a float--
  --assign extracted elements to a list--
  --divide sum of list by total number of elements in list to get the mean

### 2 Dimensional Arrays

**2 dimensional arrays** are considered a *matrix*
-specify a row and column number to extract an element from matrix.

**matrix** - consists of rows and columns

**rank** - number of dimensions

**axis** - each dimension

row = first axis

column = second axis

### Create NumPy Array

*note* all elements in an array **MUST** be the same type. Thus elements must use the *float* method.

  import csv
  with open("winequality-red.csv", 'r') as f:
    wines = list(csv.reader(f, delimiter=";"))
  import numpy as np
  wines = np.array(wines[1:], dtype=np.float)

  import numpy package
  open file
     pass list of lists into array function
  exclude header row with list slicing
  in the function, dtype argument is converted to *float*.

**.shape** - check number of rows and columns

**.zero** - every element to zero
-useful for creating fixed sized arrays with no values

### NumPy to read files

**.genfromtxt** - function that reads csv or files into arrays.

### Indexing NumPy arrays

NumPy is *zero-indexed* - index of first row is 0; index of first column is 0

### Slicing NumPy arrays 

(:) - use colon to select the elements in column from start to end (not including ending index)

  array[start num in row: end num in row, start num in column : end num in column]

### 1 Dimensional Arrays

*1 dimensional arrays* are single index to retrieve elements (like finding a specific element in array)

### N Dimension Arrays

*N dimensional arrays* are greater than 3 dimensions

### NumPy Data Types

Data types *map* between Python and C (stores data different than python)

NumPy stores values using own data types

**Data Types**:
**float** - numeric floating point data
**int** - integer data
**string** - character data
**object** - Python Objects

*note* data types end with how much memory they take up.

### Converting Data Types

**numpy.ndarray.astype** - convert array to different type.

  int_wines = wines.astype(int)
  int_wines.dtype.name

  1. copy array
  2. return new array with ideal data type.

**np.int(bit memory)** - control how array is stored.

### NumPy Array Operations

**Single Array Math**:
  wines[:,11] + 10

  -use basic mathematical operation with array and value
  -applies to each element of array
  -returns new 1 dimensional array

  wines[:,11] += 10
  wines[:,11]
  += modifies array in place

### Multiple Array Math

  wines[:,11] + wines[:,11]
  Adds two arrays to return new array with the added amount at each index.

### Broadcasting

Steps:

1. Match elements for unequal lengths.

2. Last dimension of each array is compared
if Length of dimension is equal or one of the dimensions is a length of 1 -> continue

if length of dimension aren't equal and none of dimensions have length of 1 -> return error.

3. Check until shortest array is out of dimensions.

### NumPy Array Methods

**.sum** - find sum of all elements in an array

  wines[:,11].sum()
  returns --> 9012.0

**axis=0** - gives the sum of each column from the sums of the first axis. (axis is "going away"; desired row you want gone so you get rid of the column first.)

  wines.sum(axis=0)
  returns --> array([ 13303.1 , 843.985 , 433.29 , 4059.55 ,
  139.859 , 25384. , 74302. , 1593.79794,
  5294.47 , 1052.38 , 16666.35 , 9012. ])

Sum Methods:

**.mean** - mean of array
**.std** - standard deviation of array
**.min** - minimum value of array
**.max** - max value of array

### NumPy Array Comparisons (?)

  wines[:,11] > 5
  comparisons return *booleans*

### Subsetting

**Subsetting** selects the desired elements that have a value that is higher lower and/or equal to the desired amount.

  high_quality = wines[:,11] > 7
  wines[high_quality,:][:3,:]

  return --> array([[ 7.90000000e+00, 3.50000000e-01, 4.60000000e-01,
  3.60000000e+00, 7.80000000e-02, 1.50000000e+01,
  3.70000000e+01, 9.97300000e-01, 3.35000000e+00,
  8.60000000e-01, 1.28000000e+01, 8.00000000e+00],
  [ 1.03000000e+01, 3.20000000e-01, 4.50000000e-01,
  6.40000000e+00, 7.30000000e-02, 5.00000000e+00,
  1.30000000e+01, 9.97600000e-01, 3.23000000e+00,
  8.20000000e-01, 1.26000000e+01, 8.00000000e+00],
  [ 5.60000000e+00, 8.50000000e-01, 5.00000000e-02,
  1.40000000e+00, 4.50000000e-02, 1.20000000e+01,
  8.80000000e+01, 9.92400000e-01, 3.56000000e+00,
  8.20000000e-01, 1.29000000e+01, 8.00000000e+00]])

### Reshaping NumPy Arrays

**.transpose** - changes shape of array while still preserving elements.

rows -> columns | columns -> rows

[<==BACK](README.md)
