# Solution
```
class Solution:
    def twoSum(self, nums, target):
        new_dic = dict()
        for x in range(len(nums)):
            sec = new_dic.get(target - nums[x], -1)
            if sec >= 0:
                return [sec, x]
            else:
                new_dic[nums[x]] = x
 ```
