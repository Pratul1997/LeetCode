# Solution  
```
class Solution:
    def hammingDistance(self, x, y):
        sx=bin(x)[2:]
        sy=bin(y)[2:]
        if(len(sx)>len(sy)):
            sy='0'*(len(sx)-len(sy))+sy
        else:
            sx='0'*(len(sy)-len(sx))+sx
        count=0
        for i in range(len(sx)):
            if(sx[i] != sy[i]):
                count+=1
        return (count)
```
