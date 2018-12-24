# Solution
```
class Solution(object):
    def isValid(self, s):
        arr = []
        flag = True
        opbr = ['(', '{', '[']
        clbr = [')', '}', ']']
        for x in range(len(s)):
            if s[x] in opbr:
                arr.append(opbr.index(s[x]))
            else:
                if len(arr) == 0:
                    return False
                else:
                    if arr[len(arr) - 1] == clbr.index(s[x]):
                        arr.pop()
                    else:
                        return False
        return (flag and len(arr) == 0)
```
