# Solution
```
class Solution:
    def maxSubArray(self, arr):
        maxsum = arr[0]
        dummysum = 0
        for x in range(len(arr)):
            dummysum += arr[x]
            if dummysum > maxsum:
                maxsum = dummysum
            if dummysum < 0:
                dummysum = 0
        return maxsum
```
