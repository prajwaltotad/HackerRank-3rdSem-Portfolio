# Diagonal Difference

## Approach
Traverse the matrix once and calculate the sums of the primary and secondary diagonals.

## Complexity
- Time: O(N)
- Space: O(1)

## Solution
```python
def diagonalDifference(arr):
    n = len(arr)
    primary = 0
    secondary = 0

    for i in range(n):
        primary += arr[i][i]
        secondary += arr[i][n - 1 - i]

    return abs(primary - secondary)