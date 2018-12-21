# Solution
```
class Solution:
    def findDisappearedNumbers(self, nums):
        arr = set()
        for x in range(len(nums)):
            arr.add(x + 1)
        return list(arr - set(nums))
```
