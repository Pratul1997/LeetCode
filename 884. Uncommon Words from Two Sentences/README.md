# Solution
```
class Solution:
    def uncommonFromSentences(self, A, B):
        A = A.split()
        B = B.split()
        di = dict()
        for x in range(len(A)):
            if A[x] in di:
                di[A[x]] += 1
            else:
                di[A[x]] = 1

        for x in range(len(B)):
            if B[x] in di:
                di[B[x]] += 1
            else:
                di[B[x]] = 1

        out = []
        for (key, value) in di.items():
            if value == 1:
                out.append(key)
        return out
```
