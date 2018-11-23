# Solution
```
class Solution:
    def getRow(self, numRows):
        if numRows == 0:
            return [1]
        elif numRows == 1:
            return [1, 1]
        pr = [[1]]
        for x in range(numRows):
            tem = [1]
            lt = pr[len(pr) - 1]
            for i in range(len(lt) - 1):
                tem.append(lt[i] + lt[i + 1])
            tem.append(1)
            pr.append(tem)
            del pr[0]
        return pr[len(pr) - 1]
```
