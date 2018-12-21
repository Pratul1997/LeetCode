# Solution
```
# Definition for singly-linked list.
# class ListNode:
#     def __init__(self, x):
#         self.val = x
#         self.next = None

class Solution:
    def reverseKGroup(self, head, k):
        if head is None:
            return head
        elif head.next is None:
            return head
        else:
            clen = head
            count = 0
            while clen is not None:
                count += 1
                clen = clen.next
            rllret = rll = ListNode(0)
            i = 1
            while k * i <= count:
                arr = []
                for x in range(k):
                    temp = head
                    head = head.next
                    arr.append(temp.val)
                    temp.next = None
                for y in range(k):
                    temp = ListNode(arr[k - y - 1])
                    rll.next = temp
                    rll = rll.next
                i = i + 1
            if head is not None:
                rll.next = head
            return rllret.next
```
