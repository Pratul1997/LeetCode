# Solution
```
class Solution:
    def transpose(self, A):
        r = len(A)
        b = len(A[0])
        nA = []
        for fa in range(b):
            nA.append([])
        for i in range(r):
            for j in range(b):
                nA[j].append(A[i][j])
        return nA
```
