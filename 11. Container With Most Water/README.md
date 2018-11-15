# Solution
```
class Solution:
    def maxArea(self, height):
        s = 0
        l = len(height) - 1
        maxarea = 0
        while s < l:
            if height[l] > height[s]:
                if height[s] * (l - s) > maxarea:
                    maxarea = height[s] * (l - s)
                s += 1
            else:
                if height[l] * (l - s) > maxarea:
                    maxarea = height[l] * (l - s)
                l = l - 1
        return maxarea
```
