# Sparse Arrays

## Approach

Use a dictionary to store the frequency of each input string, then look up the frequency of each query string.

## Complexity

* Time: O(N + Q)
* Space: O(N)

## Solution

```python
def matchingStrings(strings, queries):
    frequency = {}

    for string in strings:
        frequency[string] = frequency.get(string, 0) + 1

    return [frequency.get(query, 0) for query in queries]
```

## HackerRank

[Sparse Arrays](https://www.hackerrank.com/challenges/sparse-arrays/problem)
