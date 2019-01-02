# Solution
```
class Solution:
    def grayCode(self, n):
        out = ['0', '1']
        if n == 0:
            return [0]
        i = 1
        while i != n:
            out = out + out[::-1]
            for x in range(len(out)):
                if x < len(out) // 2:
                    out[x] = '0' + out[x]
                else:
                    out[x] = '1' + out[x]
            i += 1
        for x in range(len(out)):
            out[x] = int(out[x], 2)
        return out
```
