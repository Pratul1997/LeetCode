# Solution
```
class Solution:
    def findLengthOfLCIS(self, arr):
        if len(arr) == 0:
            return 0
        ml = 1
        dummy = 1
        for x in range(len(arr) - 1):
            if arr[x + 1] > arr[x]:
                dummy += 1
                if dummy > ml:
                    ml = dummy
            else:
                dummy = 1
        if dummy > ml:
            ml = dummy
        return ml
```
