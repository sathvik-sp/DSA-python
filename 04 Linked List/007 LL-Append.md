### 🧾 `append` Method - Add to End of Linked List

```python
def append(self, value):
    new_node = Node(value)
    if self.head is None:
        self.head = new_node
        self.tail = new_node
    else:
        self.tail.next = new_node
        self.tail = new_node
    self.length += 1
    return True  # optional but useful for other methods
```

---

### 📘 Purpose

* The `append` method **adds a new node to the end** of the linked list.
* It handles two scenarios:

  1. **Empty list**
  2. **Non-empty list**

---

### 🔄 Step-by-Step Breakdown

#### 1. **Create a new node**

```python
new_node = Node(value)
```

* A new node is instantiated with the value passed into the method.

---

#### 2. **Check if the list is empty**

```python
if self.head is None:
```

* If the list is empty:

  * Set both `head` and `tail` to the new node.

```python
self.head = new_node
self.tail = new_node
```

---

#### 3. **List already has elements**

* Update the current `tail`'s `.next` to point to the new node.
* Move the `tail` pointer to the new node.

```python
self.tail.next = new_node
self.tail = new_node
```

---

#### 4. **Update the length**

```python
self.length += 1
```

---

#### 5. **Return value**

```python
return True
```

* Returning `True` is optional, but useful when other methods rely on confirmation that `append` worked.

---

### 🧪 Example Usage

```python
my_linked_list = LinkedList(1)   # Creates: 1
my_linked_list.append(2)         # Appends: 2 → now 1 → 2
my_linked_list.print_list()      # Output: 1\n2
```

#### ✅ Output:

```
1
2
```

---

### 📌 Notes

* This method is part of the `LinkedList` class.
* Designed to support dynamic growth at the **tail end** of the list.
* Excellent for **queue-style** additions or building a list iteratively.

---
