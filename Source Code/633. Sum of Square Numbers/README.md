# Solution
```
class Solution:
    def judgeSquareSum(self, c):
        for x in range(int(c ** 0.5) + 1):
            val = (c - x * x) ** 0.5
            if val == float(int(val)):
                return True
        return False
```
