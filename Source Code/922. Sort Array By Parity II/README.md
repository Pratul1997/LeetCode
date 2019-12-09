# Solution
```
class Solution:
    def sortArrayByParityII(self, A):
        odd = []
        even = []
        for x in range(len(A)):
            if A[x] % 2 == 0:
                even.append(A[x])
            else:
                odd.append(A[x])
        for x in range(len(A)):
            if x % 2 == 0:
                A[x] = even.pop()
            else:
                A[x] = odd.pop()
        return A
```
