### 🧾 `print_list` Method - Linked List Traversal

```python
def print_list(self):
    temp = self.head
    while temp is not None:
        print(temp.value)
        temp = temp.next
```

---

### 📘 Explanation

* The `print_list` method is designed to **traverse a linked list** and **print all values** stored in its nodes.
* It's **not a built-in method**—this is a **custom method** created for educational and debugging purposes.

---

### 🔄 Step-by-Step Walkthrough

1. **Initialization**:

   * `temp = self.head`
   * Sets a temporary pointer `temp` to the head of the linked list.

2. **While Loop**:

   * Runs as long as `temp is not None`.
   * This ensures that we haven’t reached the end of the list.

3. **Printing Values**:

   * Inside the loop, `print(temp.value)` outputs the value of the current node.

4. **Moving Forward**:

   * `temp = temp.next` shifts the pointer to the next node in the list.

5. **Termination**:

   * Loop ends when `temp` becomes `None`, i.e., we’ve traversed the entire list.

---

### 🧪 Example

If the linked list has the values:
`11 → 3 → 23 → 7`

The output of `print_list()` would be:

```
11
3
23
7
```

---

### 📌 Notes

* This method is used frequently throughout linked list operations for **visual verification**.
* Similar print methods are created for other data structures in the course (like `print_graph`).
* Those are also **user-defined** and will not be covered in detail, but they work similarly.

---
