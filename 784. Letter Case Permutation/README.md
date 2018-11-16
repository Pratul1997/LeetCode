# Solution
```
class Solution(object):
    def letterCasePermutation(self, S):
        ch = ''
        out = []
        for x in range(len(S)):
            if not (ord(S[x]) > 47 and ord(S[x]) < 58):
                ch = ch + S[x]
        ttn = pow(2, len(ch))

        for y in range(ttn):
            bival = bin(y)[2:]
            bival = (len(bin(ttn)[2:]) - len(bival) - 1) * '0' + bival
            k = 0
            w = ''
            for m in range(len(S)):
                if not (ord(S[m]) > 47 and ord(S[m]) < 58):
                    if bival[k] == '0':
                        w = w + S[m].lower()
                    elif bival[k] == '1':
                        w = w + S[m].upper()
                    k += 1
                else:
                    w = w + S[m]
            out.append(str(w))
        return out
```
