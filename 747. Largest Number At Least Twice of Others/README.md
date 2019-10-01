# Solution
```
class Solution:
    def dominantIndex(self, nums):
        if len(nums) < 2:
            return 0
        max1 = -999999
        max2 = -999999
        for x in range(len(nums)):
            if nums[x] > max1:
                max2 = max1
                max1 = nums[x]
            elif nums[x] > max2:
                max2 = nums[x]
        if max1 >= 2 * max2:
            return nums.index(max1)
        else:
            return -1
```
