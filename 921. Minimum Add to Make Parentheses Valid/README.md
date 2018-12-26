# Solution
```
class Solution:
    def minAddToMakeValid(self, text):
        stack = []
        count = 0
        for x in range(len(text)):
            if text[x] == '(':
                stack.append('(')
            else:
                if len(stack) == 0:
                    count += 1
                else:
                    stack.pop()
        count += len(stack)
        return count
```
