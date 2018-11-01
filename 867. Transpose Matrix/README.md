# Solution
```
class Solution:
    def findMaxConsecutiveOnes(self, A):
        count=0
        previous=0
        for x in range(len(A)):
            if(A[x]==1):
                previous+=1
            else:
                if(previous>count):
                    count=previous
                previous=0
                
        if(previous>count):
            count=previous
        return count  
```
