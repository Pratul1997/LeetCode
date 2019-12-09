# Solution
```
class Solution:
    def peakIndexInMountainArray(self, A):
        for x in range(len(A)):
            if not A[x] < A[x + 1]:
                break
        return x
```
