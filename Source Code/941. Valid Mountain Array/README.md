# Solution
```
class Solution:
    def validMountainArray(self, arr):
        if len(arr) < 3:
            return False
        flag = False
        for x in range(len(arr) - 1):
            if flag == False:
                if arr[x] == arr[x + 1]:
                    return False
                elif arr[x] > arr[x + 1]:
                    if x == 0:
                        return False
                    flag = True
            else:
                if arr[x] <= arr[x + 1]:
                    return False
        return flag
```
