# Solution
```
class Solution:
    def maximumProduct(self, nums):
        nums.sort()
        l = len(nums)
        return max(nums[l - 1] * nums[l - 2] * nums[l - 3], nums[0] * nums[1] * nums[l - 1])
```
