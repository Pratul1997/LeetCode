# Solution
```
class Solution:
    def fib(self, num):
        a0 = 0
        a1 = 1
        a2 = 0
        if num >= 2:
            for x in range(num - 1):
                a2 = a1 + a0
                a0 = a1
                a1 = a2
            return a2
        else:
            return num
```
