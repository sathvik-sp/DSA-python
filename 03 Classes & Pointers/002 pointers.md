# Understanding Pointers and Data Types in Python

In this guide, we explore how **pointers** behave differently in Python depending on the **data type** (mutable vs immutable).

---

## Table of Contents

- [Pointers and Integers (Immutable)](#pointers-and-integers-immutable)
- [Pointers and Dictionaries (Mutable)](#pointers-and-dictionaries-mutable)
- [Garbage Collection](#garbage-collection)
- [Why Pointers Matter in Data Structures](#why-pointers-matter-in-data-structures)

---

## Pointers and Integers (Immutable)

```python
num1 = 11
num2 = num1

print("Before num2 value is updated:")
print("num1 =", num1)
print("num2 =", num2)

print("\nnum1 points to:", id(num1))
print("num2 points to:", id(num2))

num2 = 22

print("\nAfter num2 value is updated:")
print("num1 =", num1)
print("num2 =", num2)

print("\nnum1 points to:", id(num1))
print("num2 points to:", id(num2))
```

### Key Takeaways
- Integers are **immutable** in Python.
- `num1` and `num2` originally point to the same memory address.
- After assigning a new value to `num2`, it points to a **new memory location**.
- `num1` remains unaffected.

---

## Pointers and Dictionaries (Mutable)

```python
dict1 = {'value': 11}
dict2 = dict1

print("\n\nBefore value is updated:")
print("dict1 =", dict1)
print("dict2 =", dict2)

print("\ndict1 points to:", id(dict1))
print("dict2 points to:", id(dict2))

# Modify dict2
dict2['value'] = 22

print("\nAfter value is updated:")
print("dict1 =", dict1)
print("dict2 =", dict2)

print("\ndict1 points to:", id(dict1))
print("dict2 points to:", id(dict2))
```

### Key Takeaways
- Dictionaries are **mutable**.
- `dict1` and `dict2` point to the **same memory location**.
- Changing the value via `dict2` also updates `dict1`.
- Memory address remains the same.

---

## Garbage Collection

```python
dict3 = {'value': 33}
dict2 = dict3
# Now dict2 no longer points to the original dictionary
# dict1 still points to old dictionary

# If we now do this:
dict1 = dict2
# No variable is pointing to the old dictionary
# Python will remove it using garbage collection
```

### Explanation
- When no variables reference an object in memory, Python **automatically deletes it**.
- This process is called **Garbage Collection**.

---

## Why Pointers Matter in Data Structures

- Pointers are crucial in understanding how data structures like **Linked Lists**, **Trees**, and **Graphs** work.
- Example: In a linked list, updating a node through one variable will reflect in all other variables pointing to the same node.

```python
node1 = {'value': 22, 'next': None}
node2 = node1
node2['value'] = 44
print(node1['value'])  # Outputs 44
```

- This behavior mimics how references work in data structures where we pass around objects and mutate them.

---

## Summary
- **Immutable types** (e.g., int, str, tuple): Changing the value creates a new object.
- **Mutable types** (e.g., dict, list): Changes affect all variables referencing the object.
- Understanding references and memory is essential for working efficiently with data structures.

