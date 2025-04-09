# Time Complexity

## What is Time Complexity?
Time complexity is a measure of the amount of time an algorithm takes to complete as a function of the input size `n`. It helps in analyzing the efficiency of an algorithm.

## Best, Average, and Worst Time Complexity
- **Best Case (Ω)**: The scenario where the algorithm performs the minimum number of operations.
- **Average Case (Θ)**: The expected number of operations for a random input.
- **Worst Case (O)**: The maximum number of operations the algorithm can take.

## Types of Big O Notation
### 1. O(n) - Linear Time Complexity
**Example:**
```python
def print_items(n):
    for i in range(n):
        print(i)

print_items(10)
```
**Explanation:**
- The loop runs `n` times, making the time complexity O(n).

#### Drop Constants
**Example:**
```python
def print_items(n):
    for i in range(n):
        print(i)
    for i in range(n):
        print(i)

print_items(10)
```
**Explanation:**
- Two separate loops run `n` times each. Instead of `O(2n)`, we drop the constant and consider it as `O(n)`.

### 2. O(n²) - Quadratic Time Complexity
**Example:**
```python
def print_items(n):
    for i in range(n):
        for j in range(n):
            print(i, j)

print_items(10)
```
**Explanation:**
- Two nested loops run `n × n = n²` times, leading to O(n²) complexity.

#### Drop Non-Dominance
**Example:**
```python
def print_items(n):
    for i in range(n):
        for j in range(n):
            print(i, j)
    
    for k in range(n):
        print(k)

print_items(10)
```
**Explanation:**
- The nested loops contribute `O(n²)`, and the last loop runs `O(n)`. Since `O(n²)` dominates, we drop `O(n)` and keep `O(n²)`.

### 3. O(1) - Constant Time Complexity
**Example:**
```python
def add_items(n):
    return n + n

add_items(10)
```
**Explanation:**
- The function executes in constant time, regardless of input size, making it O(1).

### 4. O(log n) - Logarithmic Time Complexity
**Example:**
```python
def binary_search(arr, target):
    left, right = 0, len(arr) - 1
    while left <= right:
        mid = (left + right) // 2
        if arr[mid] == target:
            return mid
        elif arr[mid] < target:
            left = mid + 1
        else:
            right = mid - 1
    return -1

arr = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
print(binary_search(arr, 7))
```
**Explanation:**
- The input size is halved in each iteration, leading to `O(log n)` complexity.

### 5. O(n log n) - Linearithmic Time Complexity
**Example:**
```python
def merge_sort(arr):
    if len(arr) <= 1:
        return arr
    mid = len(arr) // 2
    left = merge_sort(arr[:mid])
    right = merge_sort(arr[mid:])
    return merge(left, right)

def merge(left, right):
    result = []
    i = j = 0
    while i < len(left) and j < len(right):
        if left[i] < right[j]:
            result.append(left[i])
            i += 1
        else:
            result.append(right[j])
            j += 1
    result.extend(left[i:])
    result.extend(right[j:])
    return result

arr = [5, 3, 8, 4, 2, 7, 6, 1]
print(merge_sort(arr))
```
**Explanation:**
- Merge Sort splits the input recursively `log n` times and merges `O(n)`, resulting in `O(n log n)` complexity.

