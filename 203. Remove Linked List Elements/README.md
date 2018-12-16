# Solution
```
# Definition for singly-linked list.
# class ListNode:
#     def __init__(self, x):
#         self.val = x
#         self.next = None

class Solution:
    def removeElements(self, head, val):
        if head is None:
            return head
        elif head.next is None:
            if head.val == val:
                return []
            else:
                return head
        hhd = head
        while head.next is not None:
            if head.next.val == val:
                head.next = head.next.next
                continue
            head = head.next
        if hhd.val == val:
            return hhd.next
        else:
            return hhd
```
