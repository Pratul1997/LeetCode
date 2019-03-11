# Solution
```
class Solution:
    def maxChunksToSorted(self, arr):
        count = 0
        insum = 0
        arrsum = 0
        for x in range(len(arr)):
            insum += x
            arrsum += arr[x]
            if insum == arrsum:
                count += 1
                insum = 0
                arrsum = 0
        return count
```
