# Solution
```
class Solution:
    def canConstruct(self, ran, mag):
        di = dict()
        for x in range(len(mag)):
            if mag[x] in di:
                di[mag[x]] += 1
            else:
                di[mag[x]] = 1
        flag = True
        for y in range(len(ran)):
            if ran[y] in di:
                if di[ran[y]] > 0:
                    di[ran[y]] -= 1
                else:
                    flag = False
                    break
            else:
                flag = False
                break
        return flag
```
