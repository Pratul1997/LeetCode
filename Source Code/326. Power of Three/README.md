# Solution
```
class Solution:
    def isPowerOfThree(self, n):
        if n < 0:
            return False
        val = 0
        if n == 0:
            return False
        if n == 1:
            return True
        while n > 1:
            if n % 3 == 0:
                n = n // 3
            else:
                return False
        return val == 0
```
