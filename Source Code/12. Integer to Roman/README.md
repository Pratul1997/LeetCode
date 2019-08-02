# Solution  
```
class Solution:
    def intToRoman(self, num):
        romans = {
            1: {1: "I", 4: "IV", 5: "V", 9: "IX"},
            10: {1: "X", 4: "XL", 5: "L", 9: "XC"},
            100: {1: "C", 4: "CD", 5: "D", 9: "CM"},
            1000: {1: "M"}
        }
        (key, res) = (1, '')
        while num > 0:
            (num, digit) = divmod(num, 10)
            if digit == 4:
                res = romans[key][4] + res
            elif digit == 9:
                res = romans[key][9] + res
            else:
                res = ((romans[key][1] * digit if digit < 5 else romans[key][5] + romans[key][1] * (digit - 5))) + res
            key = key * 10
        return res
```
