# Reading 5 - Linked Lists

## What I learned

### Essence of Linked List

**Node**- Independent items(elements) or links that are located within a linked list.

### What are Linked Lists

**Linked List**- essentially a road map that contains nodes that connect from one node to the next one all in a list.

*Linked lists* are considered to be:
-Linear data structures
-*Dynamic* data structures- memory isn't contiguous: it is actually scattered.
-ability to enlarge or condense its size.

### How many References?

**Singly**- one reference that directs to the proceeding node.
  Data-->Reference to the next Node(**Next**)

**Doubly**- two references that correlate with the previous and the next node in sequence.

**Circular**- the value doesn't evaluate with a empty value, but rather, it loops around back to the "tail", which is a previous node.

### Bones of the Linked List

  Sculpture of a Linked List:

  Head-->Node-->Node-->Node-->Null
  entry-point-->-->-->empty value

**Current**- present node that the user is looking at.

**Next**- property value that is the reference to the next node.

** What is something that I learned **

**Something that is important to note!**- in linked lists, there are no *foreach* loops, but instead the implementation of *Next* is utilized. However, *while* loops paired with **Next** is encouraged.
ex. 
  ALGORITHM Includes (value)
  // INPUT <-- integer value
  // OUTPUT <-- boolean

  1.  Current <-- Head

  2.  WHILE Current is not NULL
  3.   IF Current.Value is equal to value
  5.    return TRUE

  4.    Current <-- Current.Next

  6.  return FALSE

**Teaching something I learned**

1. Created a **head** that uses **current** so that when this runs, the code starts from the beginning.

2. Implementing a while loop, it iterates through the current *node* if does not evaluate to null (if the current node is not an empty value).

3. Within the while loop, it is checking to see if the **current** value is equal to the **value** that is defined earlier as a parameter. If this is true, the output should return a **truthy** statement.

4. If the value is not the same, the code will then skip to the next *node* that is being referenced. With the while loop, it will continue to iterate through each node until the two expected values match.

5. Once both values match, it will return *True* and the code will break

6. If there aren't any matches, it will return as a **Falsey** statement.

### Big O

**What**- Big O(**order**) is essentially taking into consideration the time it takes for a code, function, or algorithm to run.

**Why**- There are so many different lengths of code, functions, or algorithms, so it could take a very long time or even crash the computer.

**How**:

**O(1)** function- the time is always going to be "constant" and remain the same. The quantity or quality does not affect the way that the function is run.

**O(n)** function- **linear** and not constant. As the function grows, the **space** and **time** correlates exponentially as well.

**O(n²)** function- **AVOID** takes a very long time and a lot of memory.

**lgn**- logarithmic complexity growth. As the value grows, it begins to decrease in "complexity growth".

[<==BACK](README.md)
