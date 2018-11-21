# Solution
```
class Solution:
    def numUniqueEmails(self, emails):
        past = dict()
        for email in emails:
            (lname, dname) = email.split('@')
            lname = lname.split('+')[0]
            while '.' in lname:
                lname = lname.replace('.', '')
            if not past.get(lname + dname):
                past[lname + dname] = 1
        return len(past)
```
