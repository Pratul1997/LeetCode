# Solution  
```
class Solution:
    def arrayPairSum(self, nums):
        nums.sort()
        sum=0
        for x in range(0,len(nums),2):
            sum=sum+nums[x]
        return sum
```
