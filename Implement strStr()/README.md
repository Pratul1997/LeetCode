# Solution

```
class Solution:
    def strStr(self, haystack, needle):
        if len(needle) == 0:
            return 0
        for i in range(len(haystack) - len(needle) + 1):
            if haystack[i:i + len(needle)] == needle:
                return i
        return -1
```
