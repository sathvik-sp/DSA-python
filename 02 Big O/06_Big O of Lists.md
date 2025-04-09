## Big O of Lists (Python)
| Operation       | Time Complexity |
|---------------|----------------|
| Indexing (arr[i]) | O(1) |
| Appending (arr.append(x)) | O(1) |
| Popping last element (arr.pop()) | O(1) |
| Inserting at beginning/middle (arr.insert(i, x)) | O(n) |
| Deleting an element by index (del arr[i]) | O(n) |
| Iterating through a list (for x in arr) | O(n) |
| Sorting (arr.sort()) | O(n log n) |
| Searching for an element (x in arr) | O(n) |
| Copying a list (arr.copy()) | O(n) |

**Explanation:**
- Indexing and appending are `O(1)`, meaning they take constant time.
- Inserting or deleting elements (except at the end) requires shifting, making them `O(n)`.
- Sorting requires `O(n log n)`, the best time complexity for comparison-based sorts.
- Searching requires `O(n)` unless using a sorted list with binary search (`O(log n)`).

