# Solution
```
class Solution(object):
    def findErrorNums(self, nums):
        set_nums = set(nums)
        rep = sum(nums) - sum(set_nums)
        original = len(nums) * (len(nums) + 1) // 2 - sum(set_nums)
        return [rep, original]
```
