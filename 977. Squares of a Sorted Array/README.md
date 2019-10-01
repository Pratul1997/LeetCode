# Solution
```
class Solution:
    def sortedSquares(self, arr):
        if len(arr) == 0:
            return []
        elif len(arr) == 1:
            return [arr[0] ** 2]
        start = 0
        end = 0
        la = len(arr) - 1
        out = []
        if arr[0] >= 0:
            for x in range(len(arr)):
                out.append(arr[x] ** 2)
        elif arr[len(arr) - 1] < 0:
            for x in range(len(arr)):
                out.append(arr[la - x] ** 2)
        else:
            for x in range(len(arr)):
                if arr[x] >= 0:
                    start = x - 1
                    end = x
                    break
            flag = True
            while flag:
                if start == -1 and end == la + 1:
                    flag = False
                elif start == -1 and end < la + 1:
                    out.append(arr[end] ** 2)
                    end += 1
                elif start > -1 and end == la + 1:
                    out.append(arr[start] ** 2)
                    start -= 1
                elif start > -1 and end < la + 1:
                    if arr[end] < abs(arr[start]):
                        out.append(arr[end] ** 2)
                        end += 1
                    else:
                        out.append(arr[start] ** 2)
                        start -= 1
        return out
```
