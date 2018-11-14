# Solution
```
class Solution:
    def numJewelsInStones(self, J, S):
        Jl=[]
        for x in range(len(J)):
            Jl.append(J[x])
        count=0
        for y in Jl:
            count+=S.count(y)
        return count
```
