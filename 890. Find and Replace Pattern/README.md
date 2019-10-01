# Solution
```
class Solution:
    def findAndReplacePattern(self, arr, val):
        out = []
        for x in range(len(arr)):
            di = dict()
            flag = True
            if len(val) == len(arr[x]):
                for y in range(len(val)):
                    if val[y] in di:
                        if di[val[y]] != arr[x][y]:
                            flag = False
                            break
                    else:
                        di[val[y]] = arr[x][y]
                if flag == True and len(list(di.values())) == len(set(di.values())):
                    out.append(arr[x])
        return out
```
