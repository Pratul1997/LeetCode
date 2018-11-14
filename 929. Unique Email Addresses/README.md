# Solution
```
class Solution:
    def numUniqueEmails(self, emails):
        past=[]
        for email in emails:
            lname,dname = email.split('@')
            lname=lname.split('+')[0]
            while '.' in lname:
                lname = lname.replace(".", "")
            if not((lname+dname) in past):
                past.append((lname+dname))
        return len(past)
```
