# Solution
```
class Solution:
    def generate(self, numRows):
        if numRows == 0:
            return []
        elif numRows == 1:
            return [[1]]
        elif numRows == 2:
            return [[1], [1, 1]]
        elif numRows == 3:
            return [[1], [1, 1], [1, 2, 1]]
        pr = [[1], [1, 1], [1, 2, 1]]
        for x in range(numRows - 3):
            tem = [1]
            lt = pr[len(pr) - 1]
            for i in range(len(lt) - 1):
                tem.append(lt[i] + lt[i + 1])
            tem.append(1)
            pr.append(tem)
        return pr
```
