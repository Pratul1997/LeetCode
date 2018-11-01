# Solution
```
class Solution:
    def isToeplitzMatrix(self, matrix):
        condition=True
        for x in range(len(matrix)-1):
            if(matrix[x][:-1]!=matrix[x+1][1:]):
                condition=False
        return condition
```
