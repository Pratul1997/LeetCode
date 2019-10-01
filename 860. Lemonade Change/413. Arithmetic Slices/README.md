# Solution
```
class Solution:
    def numberOfArithmeticSlices(self, arr):
        if len(arr) < 3:
            return 0
        tot = 0
        count = 1
        diff = arr[1] - arr[0]
        for x in range(len(arr) - 1):
            if arr[x + 1] - arr[x] == diff:
                count += 1
            else:
                if count > 2:
                    tot += int((count - 2) * (count - 1) // 2)
                diff = arr[x + 1] - arr[x]
                count = 2
        if count > 2:
            tot += int((count - 2) * (count - 1) // 2)
        return tot
```
