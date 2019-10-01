# Solution
```
class Solution:
    def deckRevealedIncreasing(self, deck):
        deck.sort()
        out = []
        out.append(deck[len(deck) - 1])
        for x in range(1, len(deck)):
            i = len(deck) - 1 - x
            out = [deck[i]] + [out[-1]] + out[:len(out) - 1]
        return out
```
