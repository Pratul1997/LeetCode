# Solution
```
class Solution:
    def isAnagram(self, s, t):
        if len(s) != len(t):
            return False
        sdic = dict()
        for x in range(len(s)):
            if s[x] in sdic:
                sdic[s[x]] += 1
            else:
                sdic[s[x]] = 1
        for y in range(len(t)):
            if t[y] in sdic:
                if not sdic[t[y]] > 0:
                    return False
                else:
                    sdic[t[y]] -= 1
            else:
                return False
        return True
```
