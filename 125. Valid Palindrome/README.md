# Solution
```
class Solution(object):
    def isPalindrome(self, s):
        s = re.sub('[^a-zA-Z0-9]', '', s).lower()
        return s == s[::-1]
```
