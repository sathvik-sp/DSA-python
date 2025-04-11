
# Linked List Constructor in Python

In this section, we'll create a constructor for a linked list using classes in Python. We'll start by defining the classes and constructors for both the `Node` and the `LinkedList`.

## Node Class

The `Node` class is a simple class used to represent a node in the linked list. Each node contains a `value` and a `next` pointer which defaults to `None`.

```python
class Node:
    def __init__(self, value):
        self.value = value
        self.next = None
```

- `value`: Stores the data for the node.
- `next`: Points to the next node in the list. Initially set to `None`.

## LinkedList Constructor

Now that we have a class to create nodes, we can build the constructor for our `LinkedList` class.

```python
class Node:
    def __init__(self, value):
        self.value = value
        self.next = None

# LinkedList class definition
class LinkedList:
    def __init__(self, value):
        new_node = Node(value)
        self.head = new_node
        self.tail = new_node
        self.length = 1
```

### Explanation:

1. **`new_node = Node(value)`**:
   - Creates the first node using the `Node` class and assigns it the provided value.

2. **`self.head = new_node`**:
   - Points the head of the linked list to the newly created node.

3. **`self.tail = new_node`**:
   - Points the tail of the linked list to the same node, as it's the only node currently.

4. **`self.length = 1`**:
   - Initializes the length of the linked list to 1.

## Creating a Linked List

To create a new linked list, you can do the following:

```python
my_linked_list = LinkedList(4)
```

This creates a new linked list with one node that contains the value `4`. Both `head` and `tail` point to this node.

## Accessing Values

To access the value of the head node:

```python
print(my_linked_list.head.value)  # Output: 4
```
---

