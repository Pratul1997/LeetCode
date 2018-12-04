# Solution
```
class Solution:
    def judgeCircle(self, moves):
        st = moves
        up = down = left = right = 0

        for x in range(len(st)):
            if st[x] == 'R':
                right += 1
            elif st[x] == 'L':
                left += 1
            elif st[x] == 'U':
                up += 1
            elif st[x] == 'D':
                down += 1
        if up == down and left == right:
            return True
        else:
            return False
```
