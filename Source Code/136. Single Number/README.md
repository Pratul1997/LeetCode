# Solution
```
class Solution:
    def singleNumber(self, nums):
        val = 0
        for x in nums:
            val = val ^ x
        return val
```
