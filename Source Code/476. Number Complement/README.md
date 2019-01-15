# Solution
```
class Solution:
    def findComplement(self, num):
        bi_num = bin(num)[2:]
        conj = ''
        for x in range(len(bi_num)):
            if bi_num[x] == '0':
                conj += '1'
            else:
                conj += '0'
        return int(conj, 2)
```
