# Solution
```
class Solution:
    def containsNearbyDuplicate(self, nums, k):
        flag = False
        re = dict()
        for x in range(len(nums)):
            if nums[x] not in re:
                re[nums[x]] = x
            else:
                if x - re[nums[x]] <= k:
                    return True
                re[nums[x]] = x
        return flag
```
