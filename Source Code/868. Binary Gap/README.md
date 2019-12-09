# Solution
```
class Solution:
    def binaryGap(self, N):
        bv = bin(N)[2:]
        flag = False
        prev = 0
        mc = 0
        for x in range(len(bv)):
            if bv[x] == '1':
                if flag == False:
                    flag = True
                if flag == True:
                    if x - prev > mc:
                        mc = x - prev
                prev = x
        return mc
```
