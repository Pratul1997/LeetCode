# Solution
```
class Solution:
    def intersect(self, num1, num2):
        num1.sort()
        num2.sort()
        i = j = 0
        out = []
        while i < len(num1) and j < len(num2):
            if num1[i] == num2[j]:
                out.append(num1[i])
                i += 1
                j += 1
            elif num1[i] > num2[j]:
                j += 1
            elif num1[i] < num2[j]:
                i += 1
        return out
```
