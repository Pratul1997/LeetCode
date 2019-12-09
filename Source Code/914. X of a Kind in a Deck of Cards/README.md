# Solution
```
class Solution:
    def hasGroupsSizeX(self, deck):
        di = dict()
        for x in range(len(deck)):
            if deck[x] in di:
                di[deck[x]] += 1
            else:
                di[deck[x]] = 1
        ls = list(di.values())
        for y in range(2, min(ls) + 1):
            Flag = True
            for u in range(len(ls)):
                if not ls[u] % y == 0:
                    Flag = False
            if Flag == True:
                return True
        return False
```
