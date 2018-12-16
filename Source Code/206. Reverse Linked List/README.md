# Solution
```
# Definition for singly-linked list.
# class ListNode(object):
#     def __init__(self, x):
#         self.val = x
#         self.next = None

class Solution(object):
    def reverseList(self, head):
        rtl = ListNode(0)
        while head is not None:
            temp = ListNode(0)
            rtl.val = head.val
            temp.next = rtl
            rtl = temp
            head = head.next
        return rtl.next
```
