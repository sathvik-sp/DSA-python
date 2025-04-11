
# Linked Lists Under the Hood

## What is a Node?

A **Node** in a linked list is made up of:
- A **value**
- A **pointer** to the next node (commonly called `next`)

### Conceptual Representation:
```python
node = {
    "value": 4,
    "next": None
}
```

When you append a new node, you simply make the `next` of the previous node point to the new node:
```python
seven_node["next"] = four_node
```

## Chaining Nodes Together

Each node is a dictionary-like structure:
```python
node1 = {"value": 11, "next": node2}
node2 = {"value": 3, "next": node3}
node3 = {"value": 23, "next": node4}
node4 = {"value": 7, "next": node5}
node5 = {"value": 4, "next": None}
```

Then, `head` points to `node1` and `tail` points to `node5`.

## Accessing Values

### Dictionary-style Access:
```python
head["next"]["next"]["value"]  # Returns 23
```

### Linked List Object Access:
If this were implemented using a LinkedList class:
```python
print(my_linked_list.head.next.next.value)  # Also returns 23
```

## Summary

- Each node is like a dictionary containing `value` and `next`.
- Nodes are linked together via `next`.
- Memory is non-contiguous.
- Think of it as nested dictionaries to visualize traversal.

