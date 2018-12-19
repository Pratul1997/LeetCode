# Solution
```
class Solution:
    def nextGreatestLetter(self, letters, target):
        flag = False
        value = ''
        for x in letters:
            if ord(x) > ord(target):
                return x
        return letters[0]
```
