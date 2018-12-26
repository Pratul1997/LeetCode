# Solution
```
class Solution:
    def findDuplicate(self, nums):
        nums.sort()
        for x in range(len(nums) - 1):
            if nums[x] == nums[x + 1]:
                return nums[x]
```
