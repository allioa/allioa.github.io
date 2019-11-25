---
layout: default_cryptopals
---

## Challenge 1: Convert hex to base64

<br>

First challenge of the set, asks to a given hex string, to convert it in a base64 string.

Given string:
```
49276d206b696c6c696e6720796f757220627261696e206c696b65206120706f69736f6e6f7573206d757368726f6f6d
```
Should produce:
```
SSdtIGtpbGxpbmcgeW91ciBicmFpbiBsaWtlIGEgcG9pc29ub3VzIG11c2hyb29t
```
<br>
#### Solution:
<br>

_challenge1.py_
```
import base64

input = "49276d206b696c6c696e6720796f757220627261696e206c696b65206120706f69736f6e6f7573206d757368726f6f6d"
def hexToBase64(hexString):
    return base64.b64encode(bytes.fromhex(hexString))

print(hexToBase64(input).decode("utf-8"))
```
Output:
```
SSdtIGtpbGxpbmcgeW91ciBicmFpbiBsaWtlIGEgcG9pc29ub3VzIG11c2hyb29t
```
