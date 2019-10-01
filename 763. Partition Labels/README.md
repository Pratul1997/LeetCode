# Solution
```
class Solution:
    def partitionLabels(self, S):
        i = 0
        last = 0
        out = []
        while len(S) > 0:
            index = len(S) - 1 - S[::-1].index(S[i])
            if last < index:
                last = index
            if i == last:
                out.append(last + 1)
                if i == len(S) - 1:
                    break
                S = S[i + 1:]
                last = 0
                i = 0
            else:
                i += 1
        return out
```
