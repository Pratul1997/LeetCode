# Solution
```
class Solution:
    def findShortestSubArray(self, nums):
        m = {}
        m_freq = 0
        for num in nums:
            if num in m:
                m[num] += 1
            else:
                m[num] = 1
            m_freq = max(m_freq, m[num])

        if m_freq == 1:
            return 1
        cadd_list = []

        for key in m:
            if m[key] == m_freq:
                cadd_list.append(key)
        rs = len(nums)
        for cad in cadd_list:
            left = nums.index(cad)
            right = nums[::-1].index(cad)
            rs = min(len(nums) - left - right, rs)
        return rs
```
