# Solution  
```
class Solution:
    def romanToInt(self, s):
        d = {'M':1000, 'D':500, 'C':100, 'L':50, 'X':10, 'V':5, 'I':1}
        res, p = 0, 'I'
        for c in s[::-1]:
            if d[c] < d[p]:
                res, p = res - d[c] , c
            else :
                res, p = res + d[c] , c
        return res
```
