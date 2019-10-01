# Solution
```
class Solution:
    def maxIncreaseKeepingSkyline(self, arr):
        maxrow = []
        for x in range(len(arr)):
            mrow = -1
            for y in range(len(arr[0])):
                if mrow < arr[x][y]:
                    mrow = arr[x][y]
            maxrow.append(mrow)
        maxcol = []
        for x in range(len(arr[0])):
            mcol = -1
            for y in range(len(arr)):
                if mcol < arr[y][x]:
                    mcol = arr[y][x]
            maxcol.append(mcol)
        print (maxrow, maxcol)
        maxsum = 0
        for x in range(len(arr)):
            for y in range(len(arr[0])):
                mval = min(maxrow[x], maxcol[y])
                if mval > arr[x][y]:
                    maxsum += mval - arr[x][y]
        return maxsum
```
