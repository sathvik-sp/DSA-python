## 🔄 Linked List: `pop()` Method Notes

### 📌 Objective:

Remove the **last node** from a singly linked list and **return it**.

---

## 🧠 Conceptual Understanding

### 🚩 Why `pop()` is harder than `append()`:

* Singly linked lists only point forward (via `.next`).
* To remove the **last node**, we must find the **second-last** node.
* The `tail` needs to move **backward**, which means traversing **from `head`**.

---

## 🧪 Edge Cases

1. **Empty list (`length == 0`)**: return `None`.
2. **One node**: reset both `head` and `tail` to `None`.
3. **Multiple nodes**:

   * Use two pointers: `temp` (current), `pre` (previous).
   * Traverse till `temp.next == None` (last node).
   * Update `tail = pre`, set `tail.next = None`, return `temp`.

---

## ⚙️ Implementation Logic

### 🔄 Traversal with two pointers

```python
temp = self.head
pre = self.head
while temp.next:
    pre = temp
    temp = temp.next
```

### 📉 Decrement the length

```python
self.length -= 1
```

### 🚫 Handle last node deletion (length becomes 0)

```python
if self.length == 0:
    self.head = None
    self.tail = None
```

### ✅ Return the popped node

```python
return temp
```

---

## ✅ Full `pop()` Method Code

```python
def pop(self):
    if self.length == 0:
        return None

    temp = self.head
    pre = self.head

    while temp.next:
        pre = temp
        temp = temp.next

    self.tail = pre
    self.tail.next = None
    self.length -= 1

    if self.length == 0:
        self.head = None
        self.tail = None

    return temp
```

---

## 🧪 Testing Scenarios

### Setup

```python
my_linked_list = LinkedList(1)
my_linked_list.append(2)
```

### Calls

```python
print(my_linked_list.pop().value)  # ➜ 2
print(my_linked_list.pop().value)  # ➜ 1
print(my_linked_list.pop())        # ➜ None
```

### ✅ Output

```
2
1
None
```

---

## 🧵 Summary of Pointer Roles

| Pointer | Purpose                                                   |
| ------- | --------------------------------------------------------- |
| `temp`  | Used to find the **last node** (to return).               |
| `pre`   | Used to find the **second-last node** (to update `tail`). |

---

Let me know if you’d like similar notes for other linked list operations (like `shift()`, `unshift()`, `insert()`, etc.) or want this in a downloadable format (like PDF or markdown).
