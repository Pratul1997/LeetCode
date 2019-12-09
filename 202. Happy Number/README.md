# Solution
```
class Solution:
    def isHappy(self, n):
        di = dict()
        while True:
            k = 0
            while n > 0:
                k += (n % 10) ** 2
                n = n // 10
            if k == 1:
                return True
            if k in di:
                return False
            else:
                di[k] = 1
            n = k
```
