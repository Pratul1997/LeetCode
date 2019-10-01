# Solution
```
class Solution:
    def complexNumberMultiply(self, a, b):
        num1 = a.split('+')
        num2 = b.split('+')
        num1[0] = int(num1[0])
        num2[0] = int(num2[0])
        num1[1] = int(num1[1].split('i')[0])
        num2[1] = int(num2[1].split('i')[0])
        strout = str(num1[0] * num2[0] - num1[1] * num2[1]) + '+' + str(num1[0] * num2[1] + num1[1] * num2[0]) + 'i'
        return strout
```
