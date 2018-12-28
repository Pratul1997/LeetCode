# Solution
```
class Solution:
    def reachNumber(self, target):
        if target < 0:
            target = -target
        # Here in next line solved quadratic equation of k=n(n+1)/2
        i = int((-1 + (1 + 8 * target) ** 0.5) // 2)
        csum = int(i * (i + 1) // 2)
        fsum = int((i + 1) * (i + 2) // 2)
        if target == csum:
            return i
        elif csum < target < fsum:
            diff = fsum - target
            if diff % 2 == 0:
                return i + 1
            else:
                if (i + 1) % 2 == 0:
                    return i + 2
                else:
                    return i + 3
        else:
            i += 1
```
