# Solution
```
class Solution:
    def setZeroes(self, ma):
        store_row_zero = dict()
        len_of_row = len(ma[0])
        dummy_arr = []

        for x in range(len(ma)):
            flag_row = False
            for y in range(len(ma[0])):
                if ma[x][y] == 0:
                    flag_row = True
                    if not y in store_row_zero:
                        store_row_zero[y] = 0
            if flag_row == True:
                ma[x] = len_of_row * [0]

        for x in range(len(ma)):
            for y in range(len(ma[0])):
                if y in store_row_zero:
                    ma[x][y] = 0
```
