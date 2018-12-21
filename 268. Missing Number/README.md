# Solution
```
class Solution(object):
    def missingNumber(self, nums):
        check = 0
        for x in range(len(nums)):
            check = check ^ x ^ nums[x]
        return check ^ (x + 1)
```
