# Solution
```
class Solution:
    def repeatedNTimes(self, A):
        try:
            for x in range(len(A) - 1):
                if A[x] == A[x + 1] or A[x] == A[x + 2]:
                    return A[x]
        except:
            return A[len(A) - 1]
```
