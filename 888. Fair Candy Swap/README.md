# Solution
```
class Solution:
    def fairCandySwap(self, A, B):
        sA = sum(A)
        sB = sum(B)
        new = int((sA + sB) // 2)
        di = dict()
        for x in range(len(B)):
            if not B[x] in di:
                di[B[x]] = x
        for y in range(len(A)):
            vl = new - (sA - A[y])
            if vl in di:
                return [A[y], vl]
```
