# Solution
```
# Definition for singly-linked list.
# class ListNode:
#     def __init__(self, x):
#         self.val = x
#         self.next = None

class Solution:
    def mergeTwoLists(self, l1, l2):
        head = rt = ListNode(0)
        while l1 is not None or l2 is not None:
            temp = ListNode(2147483647)  # Max value that can be stored in Python Int variable
            check = 0
            if l1 is not None:
                if l1.val < temp.val:
                    temp.val = l1.val
                    check = 1
            if l2 is not None:
                if l2.val < temp.val:
                    temp.val = l2.val
                    check = 2

            head.next = temp
            head = head.next
            if check == 1:
                l1 = l1.next
            elif check == 2:
                l2 = l2.next

        return rt.next
```
