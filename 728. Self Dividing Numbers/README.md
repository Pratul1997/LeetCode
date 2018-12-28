# Solution
```
class Solution:
    def selfDividingNumbers(self, left, right):
        arr = []
        for x in range(left, right + 1):
            dummy = x
            flag = True
            while dummy > 0:
                if dummy % 10 == 0:
                    flag = False
                else:
                    if not x % (dummy % 10) == 0:
                        flag = False
                dummy = dummy // 10
            if flag == True:
                arr.append(x)
        return arr
```
