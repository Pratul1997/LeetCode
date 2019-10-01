# Solution
```
class Solution:
    def isIsomorphic(self, s, val):
        di = dict()
        flag = True
        if len(val) == len(s):
            for y in range(len(val)):
                if val[y] in di:
                    if di[val[y]] != s[y]:
                        flag = False
                        break
                else:
                    di[val[y]] = s[y]
            if flag == True and len(list(di.values())) \
                == len(set(di.values())):
                return True
        return False
```
