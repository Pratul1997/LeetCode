# Solution  
```
class Solution:
    def compress(self, chars):
        i = 0
        count = 1
        for x in range(len(chars) - 1):
            if chars[x] == chars[x + 1]:
                count += 1
            else:
                chars[i] = chars[x]
                i += 1
                if count > 1:
                    for v in range(len(str(count))):
                        chars[i] = str(count)[v]
                        i += 1
                count = 1
        chars[i] = chars[len(chars) - 1]
        i += 1
        if count > 1:
            for v in range(len(str(count))):
                chars[i] = str(count)[v]
                i += 1
        return i
```
