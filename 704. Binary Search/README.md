# Solution
```
class Solution:
    def search(self, nums, target):
        start = 0
        end = len(nums)
        forendloop = 0
        while end - start > 0:
            mid = (start + end) // 2
            if nums[mid] == target:
                return mid
            elif nums[mid] < target:
                start = mid
            elif nums[mid] > target:
                end = mid
            if end - start == 1:
                forendloop += 1
                if forendloop == 2:
                    break
        return -1
```
