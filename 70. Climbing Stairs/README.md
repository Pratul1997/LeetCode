# Solution
```
class Solution:
    def climbStairs(self, n):
        tot = 0
        k = n
        while k >= 0:
            tot += Solution.Com(n, k)
            n -= 1
            k -= 2
        return tot

    def Com(n, k):
        c = math.factorial(n) // (math.factorial(n - k) * math.factorial(k))
        return int(c)
```
