# Solution
```
class Solution:
    def isMonotonic(self, A):
        if Solution.incmo(A) + Solution.decmo(A) > 0:
            return True
        else:
            return False

    def incmo(arr):
        flag = True
        for x in range(len(arr) - 1):
            if not arr[x] <= arr[x + 1]:
                flag = False
                break
        print flag
        if flag == True:
            return 1
        else:
            return 0

    def decmo(arr):
        flag = True
        for x in range(len(arr) - 1):
            if not arr[x] >= arr[x + 1]:
                flag = False
                break
        if flag == True:
            return 1
        else:
            return 0
```
