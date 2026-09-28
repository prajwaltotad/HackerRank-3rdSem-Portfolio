# Dynamic Array

## Approach

Use a 2D list to store the sequences. For each query, calculate the sequence index using bitwise XOR and modulo, then perform the required append or retrieval operation.

## Complexity

* Time: O(N + Q)
* Space: O(N)

## Solution

```python
def dynamicArray(n, queries):
    arr = [[] for _ in range(n)]
    lastAnswer = 0
    answers = []

    for query in queries:
        type, x, y = query

        idx = (x ^ lastAnswer) % n

        if type == 1:
            arr[idx].append(y)

        elif type == 2:
            lastAnswer = arr[idx][y % len(arr[idx])]
            answers.append(lastAnswer)

    return answers
```

## HackerRank

[Dynamic Array](https://www.hackerrank.com/challenges/dynamic-array/problem)
