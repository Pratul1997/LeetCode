# Solution
```
class Solution:
    def mySqrt(self, x):
        if x == 1:
            return 1
        start = 0
        end = x
        while end - start > 1:
            mid = (start + end) // 2
            if mid * mid == x:
                return mid
            elif mid * mid < x:
                start = mid
            elif mid * mid > x:
                end = mid
        return start
```
