# Solution
```
class Solution:
    def toLowerCase(self, str):
        newstr = ''
        for x in range(len(str)):
            vch = ord(str[x])
            if vch >= 65 and vch <= 90:
                newstr = newstr + chr(97 + vch - 65)
            else:
                newstr = newstr + str[x]
        return newstr
```
