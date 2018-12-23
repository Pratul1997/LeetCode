# Solution
```
# Definition for singly-linked list.
# class ListNode:
#     def __init__(self, x):
#         self.val = x
#         self.next = None

class Solution:

    def splitListToParts(self, head, k):
        dummylength = head
        count = 0
        while dummylength is not None:
            count += 1
            dummylength = dummylength.next
        arr = []
        if count >= k:
            for x in range(k):
                if count % k > 0:
                    arr.append(count // k + 1)
                    count -= 1
                else:
                    arr.append(count // k)
        else:
            for x in range(count):
                arr.append(1)
        prarr = []

        for y in range(len(arr)):
            last = temppush = head
            for z in range(arr[y]):
                last = head
                head = head.next
            last.next = None
            prarr.append(temppush)
            
        if k > count:
            for v in range(k - count):
                prarr.append(None)
                
        return prarr
```
