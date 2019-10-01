# Solution
```
class Solution:
    def findUnsortedSubarray(self, nums):
        snums = []
        for y in range(len(nums)):
            snums.append(nums[y])
        snums.sort()
        first = -1
        second = -1
        flag = False
        for x in range(len(nums)):
            if nums[x] != snums[x]:
                if flag == False:
                    flag = True
                    first = x
                else:
                    second = x + 1
        return second - first
```
