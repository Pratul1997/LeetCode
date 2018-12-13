# Solution
```
class Solution(object):
    def subsets(self, nums):
        rearr = []
        pvl = pow(2, len(nums))
        for x in range(pvl):
            st_bi = bin(x)[2:]
            st_bi = '0' * (len(nums) - len(st_bi)) + st_bi
            sbarr = []
            for y in range(len(st_bi)):
                if st_bi[y] == '1':
                    sbarr.append(nums[y])
            rearr.append(sbarr)
        return rearr
```
