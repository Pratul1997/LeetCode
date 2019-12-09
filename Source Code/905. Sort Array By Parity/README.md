# Solution
```
class Solution:
    def sortArrayByParity(self, A):
        even = []
        odd = []
        for x in range(len(A)):
            if A[x] % 2 == 0:
                even.append(A[x])
            else:
                odd.append(A[x])
        return even + odd
```
