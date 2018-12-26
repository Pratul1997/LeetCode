# Solution
```
class Solution(object):
    def findRestaurant(self, list1, list2):
        di = dict()
        out = []
        length = 99999999
        for x in range(len(list1)):
            di[list1[x]] = x
        for y in range(len(list2)):
            if list2[y] in di:
                if di[list2[y]] + y < length:
                    out = [list2[y]]
                    length = di[list2[y]] + y
                elif di[list2[y]] + y == length:
                    out.append(list2[y])
        return out
```
