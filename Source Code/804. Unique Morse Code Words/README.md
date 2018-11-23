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
        ot = dict()
        for wd in words:
            st = ''
            for x in range(len(wd)):
                st = st + mor[apha.index(wd[x])]
            if not ot.get(st):
                ot[st] = 1
        return len(ot)
```
