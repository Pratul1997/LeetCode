# Solution
```
# Definition for singly-linked list.
# class ListNode:
#     def __init__(self, x):
#         self.val = x
#         self.next = None

class Solution:
    def removeNthFromEnd(self, head, n):
        dummy = remove = head
        count = i = 0
        if head.next is None:
            return []
        else:
            while dummy is not None:
                count += 1
                dummy = dummy.next

            if count == n:
                return head.next

            last = ListNode(0)
            while i < count - n:
                last = remove
                remove = remove.next
                i += 1
            last.next = remove.next
            return head
```
