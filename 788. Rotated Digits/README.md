# Solution
```
class Solution(object):
    def rotatedDigits(self, N):
        count = 0
        for x in range(1, N + 1):
            revnum = 0
            check = True
            arr=[0,0,5,0,0,2,9,0,0,6]
            c = 0
            val = x
            while x > 0:
                num = x % 10
                if num == 3 or num == 4 or num == 7:
                    check = False
                    break
                elif num == 2 or num == 5 or num == 6 or num == 9:
                    revnum = revnum + arr[num] * pow(10, c)
                else:
                    revnum = revnum + num * pow(10, c)
                c += 1
                x = x // 10
            if revnum == val:
                check = False
            if check == True:
                count += 1
        return count
```
