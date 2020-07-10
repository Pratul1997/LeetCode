# Solution
```
class Solution:
    def findPeakElement(self, arr):
        arr = [-9999999999] + arr + [-9999999999]
        start = 0
        end = len(arr) - 1
        while start < end:
            mid = int((start + end) // 2)
            print (mid, start, end)
            if arr[mid - 1] < arr[mid] and arr[mid] > arr[mid + 1]:
                return mid - 1
            elif arr[mid - 1] < arr[mid] and arr[mid] < arr[mid + 1]:
                start = mid
            else:
                end = mid
```
