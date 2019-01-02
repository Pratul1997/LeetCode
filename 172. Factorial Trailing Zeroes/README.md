# Solution
```
class Solution:
    def trailingZeroes(self, n):
        if n < 5:
            return 0
        count = 0
        j = 5
        while True:
            if n // j > 0:
                count += n // j
                j *= 5
            else:
                break
        return count
```
