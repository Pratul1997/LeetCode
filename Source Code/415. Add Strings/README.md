# Solution
```
class Solution:
    def addStrings(self, num1, num2):
        if len(num1) > len(num2):
            num2 = ('0' * (len(num1) - len(num2)) + num2)[::-1]
            num1 = num1[::-1]
        else:
            num1 = ('0' * (len(num2) - len(num1)) + num1)[::-1]
            num2 = num2[::-1]
        tot = 0
        carry = 0
        for x in range(len(num1)):
            val = (int(num1[x]) + int(num2[x]) + carry) % 10
            carry = (int(num1[x]) + int(num2[x]) + carry) // 10
            tot = str(val) + str(tot)
        if carry == 1:
            tot = str(carry) + str(tot)
        return tot[:-1]
```
