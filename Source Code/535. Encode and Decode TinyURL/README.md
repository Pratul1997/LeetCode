# Solution
```
from random import randint
dt = {}

class Codec:
    def encode(self, longUrl):
        st = ''
        while 1:
            for x in range(6):
                ch = randint(1, 3)
                if ch == 1:
                    vl = randint(1, 26)
                    st = st + chr(96 + vl)
                elif ch == 2:
                    vl = randint(1, 26)
                    st = st + chr(64 + vl)
                else:
                    vl = randint(0, 9)
                    st = st + chr(48 + vl)
            if dt.get(st) == None:
                dt[st] = longUrl
                break
        return 'http://tinyurl.com/' + st

    def decode(self, shortUrl):
        vl = shortUrl[-6:]
        if dt.get(vl) == None:
            return 'No Value'
        else:
            return dt.get(vl)


# Your Codec object will be instantiated and called as such:
# codec = Codec()
# codec.decode(codec.encode(url))
```
