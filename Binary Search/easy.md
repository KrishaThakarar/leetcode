

# Lower Bound


 otbvainuifbanva

## implement through bisect

```python
import bisect

arr = [1, 3, 3, 5, 7]
target = 3

idx = bisect.bisect_left(arr, target)
print(idx)   # 1

```


## Lower Bound using Binary Search

```python
def lower_bound(arr, target):
    left, right = 0, len(arr)

    while left < right:
        mid = (left + right) // 2

        if arr[mid] < target:
            left = mid + 1
        else:
            right = mid

    return left
```
