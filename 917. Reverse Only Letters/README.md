# Solution
```
class Solution:
    def reverseOnlyLetters(self, S):
        revout = ''
        rev = ''
        for x in range(len(S)):
            osx = ord(S[x])
            if osx >= 65 and osx <= 90 or osx >= 97 and osx <= 122:
                rev = S[x] + rev
        i = 0
        for y in range(len(S)):
            osx = ord(S[y])
            if osx >= 65 and osx <= 90 or osx >= 97 and osx <= 122:
                revout = revout + rev[i]
                i += 1
            else:
                revout = revout + S[y]
        return revout
```
