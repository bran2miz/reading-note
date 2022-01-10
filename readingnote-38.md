# Implementation: Stacks and Queues

## What is a Stack?

**stack**- data structure that is compiled of Nodes.

**Node**- reference next Node in stack but not the previous

### Common terminology for Stack

**Push**- Node or items placed into a stack are *pushed*.
-pushing a Node will be an O(1) operation because the time it takes to run will be always be the same.

**Pop**- Node or items removed from a stack are *popped*.

**isEmpty**- returns True if empty stack; False if not empty.

**Top**- seen at the "top" of stack

**Peek**- exception is raised and can view the top Node's value.

#### FILO vs LIFO

**FILO**- FIRST IN LAST OUT
-first item added to the stack will be the last item *popped* out of stack.

**LIFO**- LAST IN FIRST OUT
-last item added to the stack will be last item popped out of stack.

#### Push O(1)

**temp**- reference name that points to the same top Node in order to remove item from stack.

To *pop* the current top stack, you need to reassign top value to the next value in stack.

*note* clear the next value within the recent *popped* item as Null.

Peek- check with isEmpty first
-check top Node in stack

## What is a Queue

### Common terminology for Queue

**Enqueue**- Node or items placed into queue

**Dequeue**- Node or items removed from the queue.

**Front**- first Node of queue.

**Rear**- last Node of queue

**Peek**- view first Node of the queue.

**isEmpty**- returns true when queue is empty; false if not empty.

#### FIFO vs LILO

**FIFO**- FIRST IN FIRST OUT
-first item in queue will be first item out of queue

**LILO**- LAST IN LAST OUT
-last item in queue will be last item out of queue

#### Add to Queue

**Steps**:
1.change next value of the rear to desired item to be added.
  ie rear.next = Node(i)
2.change rear reference to point to Node I.
3.can continue to enqueue Nodes and keep reference to where the rear is.

#### Remove from Queue

**Steps**:
1.create a reference type named temp and give same value as top(based on FIFO principle)
2.Reassign front to next value that the current front Node is referencing
3.temp.next = Null
4.Return value of temp Node.

[<==BACK](README.md)
