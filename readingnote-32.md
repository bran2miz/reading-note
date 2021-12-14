# Reading 4 - Topics of Recursion, Classes and Objects, and pytest

## Classes and Object

**Object**- compilation of variables and functions within a singular unit

**Classes**- classes are where objects get their *variables* and *functions* from.
-blueprint to recreate and form objects.

### Accessing Object Variables

1. Assign new object variable to the class
2. Call new variable within the class variable.
  ie class MyClass:
    variable = "blah"

    def function(self):
        print("This is a message inside the class.")

  myobjectx = MyClass()

  myobjectx.variable

- Also can create independent global objects that can change the variable within the class.
  ie. class MyClass:
        variable = "blah"

        def function(self):
          print("This is a message inside the class.")

      myobjectx = MyClass()
      myobjecty = MyClass()

      myobjecty.variable = "yackity"

   Then print out both values
      print(myobjectx.variable)
      print(myobjecty.variable)

**__init__()** - function that is called when class is launched.

## Thinking Recursively 

**recursive function**- function that defines itself with expressions relative to said function.
- also can be defined in smaller version of itself.

To maintain state in recursive functions:

-state should be *global*
-state should iterate through the recursive functions so it is part of the current function call.

Can add together recursive to return an array.
  ie. attach_head(1,
            attach_head(46,
                        attach_head(-31,
                                    attach_head("hello", []))))
    Expected Output: [1,46, -31, "hello"]
  
**@lru_cache** - decorator that caches results.
-positional and keyword arguments are required to be hashable (#).

Python has *limits*-no support for **tail-call-elimination**

## Pytest Fixtures and Coverage

**pytest**- "library" for testing out Python code.
- usually consists of tests with similar features and objects that are all encompassing.



**pytest.fixture**- decorator that is used with a function definition to run *pytest*.
  ie @pytest.fixture

- With pytest, you can include the defined pytest fixture in a test parameters list.

-*@pytest.fixture* executes when you implement it and the test runs.

-can have *decision-making* and *calculatory* features.

**StringIO**- file like object

**scope**- an object that is created and utilized several times w/o recreation.

**pytest -cov**- code coverage package on PyPI that you can install and run.

  ie run pytest --cov=mymul .
  - then turn it into a readable entity such as HTML file.

[<==BACK](README.md)
