# Solution
```
class Solution:
    def rotate(self, nums, k):
        la = len(nums)
        k = k % la
        nums[:] = nums[la - k:] + nums[:la - k]
```
