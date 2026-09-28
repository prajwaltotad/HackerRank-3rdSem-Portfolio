# Time Conversion

## Approach

Check whether the time is AM or PM and adjust the hour accordingly to convert the 12-hour format into 24-hour format.

## Complexity

* Time: O(1)
* Space: O(1)

## Solution

```python
def timeConversion(s):
    period = s[-2:]
    hour = int(s[:2])

    if period == "AM":
        if hour == 12:
            hour = 0
    else:
        if hour != 12:
            hour += 12

    return f"{hour:02d}" + s[2:-2]
```

## HackerRank

[Time Conversion](https://www.hackerrank.com/challenges/time-conversion/problem)
![alt text](image.png)