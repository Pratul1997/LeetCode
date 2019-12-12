# Solution
```
class Solution:
    def convertToBase7(self, num):
        flag = True
        if num < 0:
            flag = False
            num = -1 * num
        out = ''
        while num >= 7:
            out = str(num % 7) + out
            num = int(num // 7)
        out = str(num) + out
        if flag == False:
            out = '-' + out
        return out
```
