# Solution
```
class Solution:
    def isPerfectSquare(self, num):
        check = 0
        i = 2
        val = num
        while num > 1:
            if i * i > val:
                return False
            x = num % i
            if x == 0:
                check = check ^ i
                num = num // i
            else:
                i += 1
        return check == 0
```
