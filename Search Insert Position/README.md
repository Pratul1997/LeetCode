# Solution
```
class Solution:
    def searchInsert(self, nums, target):   
        for x in range(len(nums)):
            if(target<=nums[x]):
                return x
        return len(nums)
```
