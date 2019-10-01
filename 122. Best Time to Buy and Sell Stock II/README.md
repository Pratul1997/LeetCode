# Solution

```
class Solution:
    def maxProfit(self, arr):
        buy = -1
        profit = 0
        flag = False
        for x in range(len(arr) - 1):
            if flag == False:
                if arr[x] < arr[x + 1]:
                    buy = x
                    flag = True
            else:
                if arr[x] > arr[x + 1]:
                    profit += arr[x] - arr[buy]
                    flag = False
        if flag == True:
            profit += arr[-1] - arr[buy]
        return profit
```
