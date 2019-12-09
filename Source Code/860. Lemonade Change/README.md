# Solution
```
class Solution:
    def lemonadeChange(self, bi):
        di = {5: 0, 10: 0}
        for x in range(len(bi)):
            if bi[x] == 5:
                di[5] += 1
            elif bi[x] == 10:
                if di[5] > 0:
                    di[5] -= 1
                    di[10] += 1
                else:
                    return False
            elif bi[x] == 20:
                if di[5] > 0 and di[10] > 0:
                    di[5] -= 1
                    di[10] -= 1
                elif di[5] > 2:
                    di[5] -= 3
                else:
                    return False
        return True
```
