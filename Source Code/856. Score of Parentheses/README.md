# Solution
```
class Solution:
    def scoreOfParentheses(self, S):
        st = []
        for x in range(len(S)):
            if S[x] == '(':
                st.append(S[x])
            elif S[x] == ')':
                if st[-1] == '(':
                    st.pop()
                    st.append(1)
                elif st[-1] != '(':
                    k = st.pop()
                    st.pop()
                    st.append(2 * k)
            if len(st) > 1:
                if type(st[-1]) == int and type(st[-2]) == int:
                    k1 = st.pop()
                    k2 = st.pop()
                    st.append(k1 + k2)

        return st[0]
```
