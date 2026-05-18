```python
def rotate_right(items, k):
    """
    Rotate `items` to the right by `k` steps and return the result.
    Original list is left unchanged.

    >>> rotate_right([1, 2, 3, 4, 5], 2)
    [4, 5, 1, 2, 3]
    """
    if not items:
        return items            # handle empty list
    k %= len(items)             # compress oversized shifts
    return items[-k:] + items[:-k]
```
### Why it works
- `k %= len(items)` converts any `k` larger than the list into its minimal equivalent shift.
- Slicing trick:
    - `items[-k:]` grabs the last `k` elements.
    - `items[:-k]` grabs everything before those.
    - Concatenate to complete the rotation.
#### In‑place variant (mutates the original list)
```python
def rotate_right_inplace(items, k):
    if not items:
        return
    k %= len(items)
    items[:] = items[-k:] + items[:-k]
```

Both versions run in O(n) time and O(k) extra space (effectively O(n) for the slicing result), which is optimal for a straightforward rotation in Python.