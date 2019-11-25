---
layout: default_cryptopals
---

## Challenge 2: Fixed XOR
<br>

Second challenge of the set, asks to write a function that takes two equal-length buffers and produces their XOR combination.

Given string:
```
1c0111001f010100061a024b53535009181c
```
XOR with:
```
686974207468652062756c6c277320657965
```
Should produce:
```
746865206b696420646f6e277420706c6179
```

Solution:

_challenge2.py_
```
def xorSS(string1, string2):
    return ''.join(chr(ord(a) ^ ord(b)) for a,b in zip(string1,string2))

def hexToString(hexString):
    try:
        return bytes.fromhex(hexString).decode('utf-8')
    except Exception as e:
        return "";

input1 = "1c0111001f010100061a024b53535009181c"
input2 = "686974207468652062756c6c277320657965"

result = xorSS(hexToString(input1), hexToString(input2))

print(result)
print(result.encode('utf-8').hex())

```

Output:
```
the kid don't play
746865206b696420646f6e277420706c6179
```
