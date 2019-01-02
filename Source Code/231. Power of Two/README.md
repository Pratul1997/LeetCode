# Solution
```
class Solution:
    def isPowerOfTwo(self, x):
        if x == 0:
            return False
        return x & (x - 1) == 0
```
