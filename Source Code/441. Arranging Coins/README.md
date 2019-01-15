# Solution
```
import math
class Solution:
    def arrangeCoins(self, n):
        if n == 0:
            return 0
        # Concept of Arithmetic Progression Sum=n*(n+1)/2
        return int((math.sqrt(1 + 8 * n) - 1) // 2)
```
