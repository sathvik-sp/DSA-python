# Understanding Python Classes: The Cookie Analogy

Classes are a core concept in Python and are essential for building custom data structures. This guide explains the fundamentals of classes using a simple and relatable analogy: cookies and cookie cutters.

## What is a Class?
A **class** in Python is like a **cookie cutter**. It defines a template or blueprint for creating objects (cookies).

Just as you can use a cookie cutter to make many cookies of different colors or sizes, you can use a class to create multiple objects with different attributes.

## Built-in vs Custom Types
Python comes with built-in classes like `int`, `str`, and `list`. However, you can define your **own classes** to create custom data types.

## Defining a Cookie Class
```python
class Cookie:
    def __init__(self, color):
        self.color = color

    def get_color(self):
        return self.color

    def set_color(self, color):
        self.color = color
```

### Key Concepts
- `__init__`: This is the **constructor** method. It's called automatically when a new object is created.
- `self`: Refers to the specific instance of the class. It allows each object to maintain its own state.
- `get_color`: Returns the color of the cookie.
- `set_color`: Changes the color of the cookie.

## Creating Cookie Objects
```python
cookie_one = Cookie('green')
cookie_two = Cookie('blue')
```
- `cookie_one` and `cookie_two` are two separate objects created from the `Cookie` class.
- They are initialized with different colors.

## Accessing Object Data
```python
print('Cookie one is', cookie_one.get_color())
print('Cookie two is', cookie_two.get_color())
```
### Output:
```
Cookie one is green
Cookie two is blue
```

## Modifying Object Data
```python
cookie_one.set_color('yellow')

print('\nCookie one is now', cookie_one.get_color())
print('Cookie two is still', cookie_two.get_color())
```
### Output:
```
Cookie one is now yellow
Cookie two is still blue
```

## Why Are Classes Important?
In this course and real-world Python development, we use classes to create data structures like:
- Linked Lists
- Stacks
- Queues
- Trees
- Graphs

## Example: Linked List (Structure Only)
```python
class LinkedList:
    def __init__(self):
        # initialize linked list

    def append(self, value):
        # add value at the end

    def pop(self):
        # remove and return the last item

    def prepend(self, value):
        # add value at the beginning

    def insert(self, index, value):
        # insert value at index

    def remove(self, value):
        # remove first occurrence of value
```

## Summary
- Classes let you model real-world entities in code.
- You use constructors to initialize data.
- You use methods to interact with your objects.
- Classes are used in building all custom data structures in Python.

Keep this cookie analogy in mind, and you'll have a much easier time understanding and using classes!

