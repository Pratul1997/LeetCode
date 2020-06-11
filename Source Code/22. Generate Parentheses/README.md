# Solution
```
class Solution:
    def generateParenthesis(self, n):
        if n == 0:
            return []
        arr = [['(', n - 1, n]]
        tot = arr[0][1] + arr[0][2]
        while tot > 0:
            dummy = []
            tot = 0
            for x in range(len(arr)):
                if arr[x][1] > 0:
                    dummy.append([arr[x][0] + '(', arr[x][1] - 1,
                                 arr[x][2]])
                    tot += arr[x][1] + arr[x][2] - 1
                if arr[x][2] > arr[x][1]:
                    dummy.append([arr[x][0] + ')', arr[x][1], arr[x][2]
                                 - 1])
                    tot += arr[x][1] + arr[x][2] - 1
            arr = dummy
        for y in range(len(arr)):
            arr[y] = arr[y][0]
        return arr
```
