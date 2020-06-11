# Solution
```
class Solution:
    def removeDuplicates(self, arr):
        i = 0
        la = len(arr)
        count = 1
        while i < la - 1:
            if arr[i] == arr[i + 1]:
                count += 1
            else:
                count = 1
            if count > 2:
                arr.pop(i)
                count -= 1
                la -= 1
            else:
                i += 1
        return len(arr)
```
