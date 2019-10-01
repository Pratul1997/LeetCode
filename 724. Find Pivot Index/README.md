# Solution
```
class Solution:
    def pivotIndex(self, num):
        if len(num) == 0:
            return -1
        if len(num) == 1:
            return 0
        s = sum(num)
        sl = 0
        for x in range(0, len(num)):
            if sl == s - num[x] - sl:
                return x
            sl += num[x]
        return -1
```
