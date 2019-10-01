# Solution
```
class Solution:
    def backspaceCompare(self, S, T):
        S = Solution.ls(self, S)
        T = Solution.ls(self, T)
        if len(S) == len(T):
            for x in range(len(S)):
                if S[x] != T[x]:
                    return False
            return True
        else:
            return False

    def ls(self, arr):
        arr = list(arr)
        start = 0
        for x in range(len(arr)):
            if arr[x] == '#':
                if start > 0:
                    start -= 1
                else:
                    continue
            else:
                arr[start] = arr[x]
                start += 1
        return arr[:start]
```
