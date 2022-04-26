# Reading 41 Pythonisms

## Dunder Methods

**dunder methods** - emulate the behavior of built-in-types.

```python
class LenSupport:
    def __len__(self):
        return 42

>>> obj = LenSupport()
>>> len(obj)
42
```

**__init__** - similar to a constructor function in javascript. Takes care of setting up the object.

**__repr__** - official string representation of an object. (Make an object of the class)

**__str__** - informal or nicely printable string representation of an object.

```python
def __repr__(self):
        return 'Account({!r}, {!r})'.format(self.owner, self.amount)

    def __str__(self):
        return 'Account of {} with starting amount: {}'.format(
            self.owner, self.amount)
```

```python
__add__
```

**__sum__** - for integers it sums, for strings it concatenates.

**__call__** - make an object callable like a regular function by adding the `__call__` dunder method.

## Iterators

**iterator** - provide sequence interface to Python objects that's memory efficient and considered Pythonic.

RepeaterIterator returns same value over and over. Get rid of iterator altogether and implement an iterable object with a single Python class. 

```python
class Repeater:
    def __init__(self, value):
        self.value = value

    def __iter__(self):
        return self

    def __next__(self):
        return self.value
```

Object needs to implement iterator protocol by provide the `__iter__` and `__next__` dunder methods.

Generators and generator expressions.

## Generators

**generators** - look like regular functions but instead of using the return statment, they use yield to pass data back to the caller.

```python
def repeat(value):
    while True:
      yield value
```

### Generators that stop generating.

`yield` - statement that allows you to temporarily suspend execution of a generator function and pass back values of it.

`StopIteration` - singals that it has no more values to provide.

```python
def bounded_repeater(value, max_repeats):
    count = 0
    while True:
        if count >= max_repeats:
            return
        count += 1
        yield value
```

```python
def bounded_repeater(value, max_repeats):
    for i in range(max_repeats):
        yield value
```

^^ shortens code.

[<==BACK](README.md)
