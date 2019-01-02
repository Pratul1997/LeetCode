# Solution
```
class Solution:
    def largeGroupPositions(self, s):
        arr = []
        start = 0
        end = 0
        for x in range(len(s) - 1):
            if s[x] != s[x + 1]:
                end = x
                if end - start >= 2:
                    arr.append([start, end])
                start = end = x + 1
        if start == end:
            if len(s) - 1 - start >= 2:
                arr.append([start, len(s) - 1])
        return arr
```
