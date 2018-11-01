# Solution
```
class Solution:
    def flipAndInvertImage(self, A):
        for x in range(len(A)):
            A[x].reverse()
            for y in range(len(A[x])):
                if(A[x][y]==1):
                    A[x][y]=0
                else:
                    A[x][y]=1
        return A
```
