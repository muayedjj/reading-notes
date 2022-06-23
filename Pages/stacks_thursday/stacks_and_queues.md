# Stacks and Queues

## What is a Stack

A stack is a data structure that consists of Nodes.Each Node references the next Node in the stack, but does not reference its previous. [1]

### Common terminology
- Push - Nodes or items that are put into the stack are pushed
- Pop - Nodes or items that are removed from the stack are popped. When you attempt to pop an empty stack an exception will be raised.
- Top - This is the top of the stack.
- Peek - When you peek you will view the value of the top Node in the stack. When you attempt to peek an empty stack an exception will be raised.
- IsEmpty - returns true when stack is empty otherwise returns false.

### Important Concepts

1. **FILO**

    _**F**irst **I**n **L**ast **O**ut_

This means that the first item added in the stack will be the last item popped out of the stack.

2. **LIFO**

    _**L**ast **I**n **F**irst **O**ut_

This means that the last item added to the stack will be the first item popped out of the stack.

3. **Stack Visualization**
The photo below shows an example of what a stack looks like.

![stack_visualization](./stack_visualization.png)

## Stack Operations

### **Push** _O(1)_

When adding a `Node`, you `push` it into the stack by assigning it as the new `top`, with its `next` property equal to the original `top`.

This will always be an **_O(1)_** operation because it takes the same amount of time no matter how many `Nodes` `(n)` you have in the stack.


### **Pop** _O(1)_

`Popping a Node off` a stack is the action of removing a `Node` from the `top`. When conducting a `pop`, the `top` `Node` will be re-assigned to the `Node` that lives below and the `top` `Node` is returned to the user. [1]


### **Peek** _O(1)_

_Conducting a peek, will only be inspecting the top Node of the stack._



- The pseudocode for a peek looks like:
        
        ALGORITHM peek()
        // INPUT <-- none
        // OUTPUT <-- value of top Node in stack
        // EXCEPTION if stack is empty

            return top.value


### **IsEmpty** _O(1)_

- Here is the pseudocode for isEmpty

        ALGORITHM isEmpty()
        // INPUT <-- none
        // OUTPUT <-- boolean

        return top = NULL

- Typically, one would check isEmpty before conducting a `peek` or a `push`. This will ensure that an exception is not raised. Alternately, we can wrap the call in a try/catch block.

#



# **Queues**

## Common Terminology

- `Enqueue` - Nodes or items that are added to the queue.
- `Dequeue` - Nodes or items that are removed from the queue. _If called when the queue is empty an exception will be raised._
- `Front` - This is the front/first Node of the queue.
- `Rear` - This is the rear/last Node of the queue.
- `Peek` - When you `peek` you will view the value of the front Node in the queue. If called when the queue is empty an exception will be raised.
- `IsEmpty` - returns true when queue is empty otherwise returns false.

### Queues follow these concepts:

1. **FIFO**

    _**F**irst **I**n **F**irst **O**ut_

This means that the first item in the queue will be the first item out of the queue. [1]

2. **LILO**

    _**L**ast **I**n **L**ast **O**ut_

This means that the last item in the queue will be the last item out of the queue. [1]

### Queue Visualization

Here is what a Queue looks like:

![queue_visualization](./queue_visualization.png)


## **Pseudocodes**

### Here is the pseudocode for the `enqueue` method:

        ALGORITHM enqueue(value)
        // INPUT <-- value to add to queue
            (will be wrapped in Node internally)
        // OUTPUT <-- none
            node = new Node(value)
            rear.next <-- node
            rear <-- node

### Here is the pseudocode for the `dequeue` method:

        ALGORITHM dequeue()
        // INPUT <-- none
        // OUTPUT <-- value of the removed Node
        // EXCEPTION if queue is empty

            Node temp <-- front
            front <-- front.next
            temp.next <-- null

            return temp.value






_For more on the subject of **Stacks and Queues**, check this [**GREAT** Article](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/stacks_and_queues.html)  on codefellows_


## Things I want to know more about:
1. Data Structures.
2. Python's Data Model.
3. Nodes & Queues.




[1]: https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/stacks_and_queues.html