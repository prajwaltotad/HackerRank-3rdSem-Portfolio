# Compare the Triplets

## Approach

Compare Alice's and Bob's scores element by element and maintain their respective scores.

## Complexity

* Time: O(1)
* Space: O(1)

## Solution

```python
def compareTriplets(a, b):
    alice = 0
    bob = 0

    for i in range(3):
        if a[i] > b[i]:
            alice += 1
        elif a[i] < b[i]:
            bob += 1

    return [alice, bob]
```

## HackerRank

[Compare the Triplets](https://www.hackerrank.com/challenges/compare-the-triplets/problem)
