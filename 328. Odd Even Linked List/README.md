# Solution
```
# Definition for singly-linked list.
# class ListNode:
#     def __init__(self, x):
#         self.val = x
#         self.next = None

class Solution:
    def oddEvenList(self, head):
        count = 1
        odd_rec = odd = ListNode(0)
        even_rec = even = ListNode(0)
        while head is not None:
            temp = ListNode(head.val)
            remove = head
            head = head.next
            remove.next = None
            if count % 2 == 1:
                odd.next = temp
                odd = odd.next
            else:
                even.next = temp
                even = even.next
            count += 1
        odd.next = even_rec.next
        return odd_rec.next
```
