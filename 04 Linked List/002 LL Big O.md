# Linked Lists: Big O Overview

This document outlines the Big O time complexity for common operations in a linked list, along with comparisons to Python lists.

## Linked List Operations and Their Complexities

### Append to End
- **Operation**: Add a node to the end of the list
- **Steps**:
  - Set the `next` pointer of the current tail to the new node
  - Update the tail pointer to the new node
- **Complexity**: `O(1)`
- **Reason**: Constant time because we already have a reference to the tail

### Remove from End
- **Operation**: Remove the last node
- **Steps**:
  - Traverse the list from head to find the second-to-last node
  - Set tail to the second-to-last node
- **Complexity**: `O(n)`
- **Reason**: We must iterate through the entire list to locate the second-to-last node

### Add to Beginning
- **Operation**: Add a node to the front of the list
- **Steps**:
  - Set `new_node.next = head`
  - Set `head = new_node`
- **Complexity**: `O(1)`
- **Reason**: Direct access to the head allows constant time insertion

### Remove from Beginning
- **Operation**: Remove the first node
- **Steps**:
  - Set `head = head.next`
- **Complexity**: `O(1)`
- **Reason**: Constant time because we already have access to the head

### Insert in Middle
- **Operation**: Insert a node after a given node (e.g., after node with value 23)
- **Steps**:
  - Traverse from head to find the target node
  - Set `new_node.next = target.next`
  - Set `target.next = new_node`
- **Complexity**: `O(n)`
- **Reason**: We need to traverse the list to find the correct position

### Remove from Middle
- **Operation**: Remove a node in the middle
- **Steps**:
  - Traverse from head to find the node before the one to remove
  - Set `prev.next = target.next`
- **Complexity**: `O(n)`
- **Reason**: List traversal is required

### Lookup by Value or Index
- **Operation**: Search for a node by value or index
- **Steps**:
  - Iterate through the list until the value or index is found
- **Complexity**: `O(n)`
- **Reason**: No direct access like in arrays, traversal required

## Comparison Table: Linked List vs Python List

| Operation                | Linked List | Python List |
|-------------------------|-------------|-------------|
| Append           | O(1)        | O(1)        |
| Pop          | O(n)        | O(1)        |
| Prepend       | O(1)        | O(n)        |
| Pop first  | O(1)        | O(n)        |
| Insert        | O(n)        | O(n)        |
| Remove     | O(n)        | O(n)        |
| Lookup by value         | O(n)        | O(n)        |
| Lookup by index         | O(n)        | O(1)        |

## Summary
Linked lists excel at operations at the beginning of the list due to their pointer-based structure. However, they perform worse than arrays when it comes to end removal and indexed lookup. Understanding these trade-offs is crucial when choosing a data structure for a given problem.


