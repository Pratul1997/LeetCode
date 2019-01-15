# Solution
```
class Solution:
    def checkPerfectNumber(self, num):
        if num < 2:
            return False
        sum_total = 1
        for x in range(2, int(num ** 0.5) + 1):
            if num % x == 0:
                if x != num // x:
                    sum_total += x + num // x
        return sum_total == num
```
