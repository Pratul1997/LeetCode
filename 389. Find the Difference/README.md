# Solution
```
class Solution(object):
    def findTheDifference(self, s, t):
        val = 0
        for x in range(len(s)):
            val = val ^ ord(s[x])
        for y in range(len(t)):
            val = val ^ ord(t[y])
        return chr(val)
```
