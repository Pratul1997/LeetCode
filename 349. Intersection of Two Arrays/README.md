# Solution
```
class Solution:
    def intersection(self, num1, num2):
        num3 = set(num1).difference(set(num1).difference(set(num2)))
        return list(num3)
```
