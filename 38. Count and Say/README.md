# Solution
```
class Solution:
    def countAndSay(self, n):
        val = '1'
        for x in range(1, n):
            nval = ''
            count = 1
            for y in range(len(val) - 1):
                if val[y] == val[y + 1]:
                    count += 1
                else:
                    nval += str(count) + val[y]
                    count = 1
            nval += str(count) + val[len(val) - 1]
            val = nval
        return val
```
