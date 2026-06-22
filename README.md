# Encryption/Decryption Using XOR

## Secret Message and Key

Message: **code**
Key: **key1**

## ASCII and Binary

| Character | ASCII | Binary   |
| --------- | ----: | -------- |
| c         |    99 | 01100011 |
| o         |   111 | 01101111 |
| d         |   100 | 01100100 |
| e         |   101 | 01100101 |

| Key Character | ASCII | Binary   |
| ------------- | ----: | -------- |
| k             |   107 | 01101011 |
| e             |   101 | 01100101 |
| y             |   121 | 01111001 |
| 1             |    49 | 00110001 |

## Encryption Using XOR

01100011 XOR 01101011 = 00001000
01101111 XOR 01100101 = 00001010
01100100 XOR 01111001 = 00011101
01100101 XOR 00110001 = 01010100

Encrypted Binary:

00001000 00001010 00011101 01010100

Encrypted Hexadecimal:

08 0A 1D 54

## Decryption Using XOR

00001000 XOR 01101011 = 01100011 = c
00001010 XOR 01100101 = 01101111 = o
00011101 XOR 01111001 = 01100100 = d
01010100 XOR 00110001 = 01100101 = e

Decrypted Message: **code**

## Different Length Plaintext and Key

If the plaintext and key are different lengths, the key can be repeated until it matches the length of the message. For example, if the message is longer than the key, the key starts over from the beginning. This allows every character in the message to be XORed with a key character.

## Flowchart

Start
↓
Choose message and key
↓
Convert message to ASCII and binary
↓
Convert key to ASCII and binary
↓
Apply XOR to each binary pair
↓
Convert encrypted binary to hexadecimal
↓
XOR encrypted binary with key again
↓
Confirm original message is recovered
↓
End

## Challenges

One challenge was making sure each character was converted into the correct 8-bit binary ASCII value. Another challenge was carefully applying the XOR rule, because one small mistake in a bit could change the encrypted result. I also had to make sure the same key was used again during decryption so the original message could be recovered correctly.
