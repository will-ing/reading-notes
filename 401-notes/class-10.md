# Stacks and Queues

A `stack` is a data structure that consists of nodes

1. **Push** - Nodes or items that are put into the stack are pushed
1. **Pop** - Nodes or items that are removed from the stack are popped. When you attempt to pop an empty stack an exception will be raised.
1. **Top** - This is the top of the stack.
1. **Peek** - When you peek you will view the value of the top Node in the stack. When you attempt to peek an empty stack an exception will be raised.
1. **IsEmpty** - returns true when stack is empty otherwise returns false.

Stacks follow two concepts
1. First in first out
2. Last in first out

> Pushing a node on stack will always be O(1)

steps

1. You need the node you want to add
2. You need to assign the next property of the top node
3. Reassign to the our top ref to the new node

```py
ALOGORITHM push(value)
// INPUT <-- value to add, wrapped in Node internally
// OUTPUT <-- none
   node = new Node(value)
   node.next <-- Top
   top <-- Node
```

> Popping a node is removing a node from the top

steps:

1. Create a reference named temp that points to the same Node that top points to.
2. Once you have created the new reference type, you now need to re-assign top to the value that the next property is referencing. We will re-assign top to be Node 4.
3. Clear the next property in your current temp ref. *This will ensure that no further references to Node 4 are floating around the heap. This will allow our garbage collector to cleanly and safely dispose of the Nodes correctly.*
4. We return the value of the temp Node that was just popped off.

```py
ALGORITHM pop()
// INPUT <-- No input
// OUTPUT <-- value of top Node in stack
// EXCEPTION if stack is empty

   Node temp <-- top
   top <-- top.next
   temp.next <-- null
   return temp.value
```

> When conducting a `peek`, you will only be inspecting the top Node of the stack.

```py
ALGORITHM peek()
// INPUT <-- none
// OUTPUT <-- value of top Node in stack
// EXCEPTION if stack is empty

   return top.value
```

isEmpty O(1)

```py
ALGORITHM isEmpty()
// INPUT <-- none
// OUTPUT <-- boolean

return top = NULL
```

## Queues

- When you add an item to a queue, you use the `enqueue` action.

```py
ALGORITHM enqueue(value)
// INPUT <-- value to add to queue (will be wrapped in Node internally)
// OUTPUT <-- none
   node = new Node(value)
   rear.next <-- node
   rear <-- node
```

- When you remove an item from a queue, you use the `dequeue` action.

```
ALGORITHM dequeue()
// INPUT <-- none
// OUTPUT <-- value of the removed Node
// EXCEPTION if queue is empty

   Node temp <-- front
   front <-- front.next
   temp.next <-- null

   return temp.value
```




[Main Page](https://will-ing.github.io/reading-notes)