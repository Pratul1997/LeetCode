# Solution  
```
class Solution:
    def uniqueMorseRepresentations(self, words):
        apha = [
            'a',
            'b',
            'c',
            'd',
            'e',
            'f',
            'g',
            'h',
            'i',
            'j',
            'k',
            'l',
            'm',
            'n',
            'o',
            'p',
            'q',
            'r',
            's',
            't',
            'u',
            'v',
            'w',
            'x',
            'y',
            'z',
            ]
        mor = [
            '.-',
            '-...',
            '-.-.',
            '-..',
            '.',
            '..-.',
            '--.',
            '....',
            '..',
            '.---',
            '-.-',
            '.-..',
            '--',
            '-.',
            '---',
            '.--.',
            '--.-',
            '.-.',
            '...',
            '-',
            '..-',
            '...-',
            '.--',
            '-..-',
            '-.--',
            '--..',
            ]
        ot = []
        for wd in words:
            st = ''
            for x in range(len(wd)):
                st = st + mor[apha.index(wd[x])]
            if st not in ot:
                ot.append(st)
        return len(ot)

```
