# Welcome to Linked Lists

This is our first data structure.

To explain it, let's start by looking at a built-in Python list:

```python
my_list = [10, 20, 30, 40]
```

## Difference 1: Indexes

A **Python list** has indexes that allow O(1) access to any element:
```python
my_list[2]  # returns 30
```

A **linked list** does not use indexes. Instead, you access elements by traversing the list from the head.

## Difference 2: Memory Allocation

Python lists are **contiguously allocated in memory**, meaning elements are stored side-by-side in memory. This allows efficient indexing.

Linked lists are **non-contiguous**. Each element (called a node) can be anywhere in memory, but it maintains a link (a pointer) to the next node.

## Visual Representation:

### Python List:
```
[10] -> [20] -> [30] -> [40] (contiguous memory)
```

### Linked List:
```
Head -> (10) -> (20) -> (30) -> (40) -> None
```
Each node points to the next one. The last node points to `None`, indicating the end of the list.

## Key Terminology
- **Node**: An element of a linked list that contains data and a pointer to the next node.
- **Head**: A pointer/reference to the first node in the list.
- **Tail**: A pointer/reference to the last node (optional, for efficiency).

## Summary
| Feature           | Python List         | Linked List        |
|------------------|---------------------|--------------------|
| Indexes          | Yes (O(1) access)   | No (O(n) access)   |
| Memory           | Contiguous          | Non-contiguous     |
| Traversal        | Random access       | Sequential only    |
| Insertion/Deletion (middle) | O(n)             | O(1) (with pointer) |

Linked lists offer advantages in scenarios where dynamic memory allocation or frequent insertions/deletions are required.

