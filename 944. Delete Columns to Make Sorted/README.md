# Solution  
```
class Solution:
    def minDeletionSize(self, A):
        nr = len(A)
        nc = len(A[0])
        count = 0
        for i in range(0, nc):
            for j in range(1, nr):
                if A[j][i] < A[j - 1][i]:
                    count += 1
                    break
        return count
```
