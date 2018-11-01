# Solution
```
class Solution:
    def reverseWords(self, s):
        new_arr=[ w[::-1] for w in s.split(' ') ]
        return  ' '.join(new_arr)
```
