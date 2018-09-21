# Solution  
```
class Solution:
    def maxProfit(self, prices): 
        sma=1000000
        profit=0
        for x in range(len(prices)):
            if(sma>prices[x]):
                sma=prices[x]
            elif((prices[x]-sma)>profit):
                profit=prices[x]-sma      
        return profit
```
