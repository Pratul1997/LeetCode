# Solution
```
# Definition for singly-linked list.
# class ListNode(object):
#     def __init__(self, x):
#         self.val = x
#         self.next = None

class Solution(object):
    def detectCycle(self, head):
        rec = dict()
        count = 0
        while head is not None:
            if str(head)[-15:] in rec:
                return rec[str(head)[-15:]]
            else:
                rec[str(head)[-15:]] = head
            count += 1
            head = head.next
        return None
```
