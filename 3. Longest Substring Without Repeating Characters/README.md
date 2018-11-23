# Solution
```
class Solution:
    def lengthOfLongestSubstring(self, s):
        if len(s) == 0:
            return 0
        s = s.strip()
        if len(s) == 0:
            return 1
        maxlen = 0
        arr = ''
        for x in range(len(s)):
            if s[x] in arr:
                if len(arr) > maxlen:
                    maxlen = len(arr)
                arr = arr[arr.index(s[x]) + 1:] + s[x]
            else:
                arr += s[x]
        if len(arr) > maxlen:
            return len(arr)
        else:
            return maxlen
```
