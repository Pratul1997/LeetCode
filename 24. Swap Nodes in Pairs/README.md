# Solution
```
# Definition for singly-linked list.
# class ListNode(object):
#     def __init__(self, x):
#         self.val = x
#         self.next = None

class Solution(object):
    def swapPairs(self, head):
        if head is None:
            return head
        elif head.next is None:
            return head
        else:
            retval = head
            count = 0
            hprev = head
            while head is not None:
                if head.next is not None:
                    temp = head
                    temp1 = head.next
                    temp.next = head.next.next
                    temp1.next = temp
                    head = head.next
                    if count == 0:
                        count += 1
                        retval = temp1
                    else:
                        hprev.next = temp1
                        
                    hprev = temp
                else:
                    break
            return retval
```
