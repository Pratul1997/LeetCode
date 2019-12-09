# Solution
 ```
# Definition for singly-linked list.
# class ListNode(object):
#     def __init__(self, x):
#         self.val = x
#         self.next = None

class Solution(object):
    def middleNode(self, head):
        count = 0
        dummy = head
        while dummy is not None:
            count += 1
            dummy = dummy.next
            
        if count % 2 == 1:
            count = (count + 1) // 2
        else:
            count = count // 2 + 1
            
        limit = 1
        while limit < count:
            head = head.next
            limit += 1
        return head
 ```
