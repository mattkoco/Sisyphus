# General Ciphers and Encoding

## Ciphers Overview

### Substitution Ciphers
- **Caesar Cipher:**
  - Description: Shifts each letter by a fixed number of positions down the alphabet.
  - Example: Shift of 3 → A -> D, B -> E, ..., Z -> C
  - Tools: Online Caesar cipher tools

- **ROT13:**
  - Description: A specific case of the Caesar cipher where each letter is shifted 13 places.
  - Example: "HELLO" -> "URYYB"
  - Tools: Online ROT13 converters

- **Vigenère Cipher:**
  - Description: Uses a keyword to shift letters in plaintext cyclically.
  - Encryption: C[i] = (M[i] + K[i % len(K)]) % 26
  - Decryption: M[i] = (C[i] - K[i % len(K)]) % 26
  - Tools: CryptoPals Vigenère tool

### Transposition Ciphers
- **Rail Fence Cipher:**
  - Description: Writes plaintext diagonally on successive "rails" of an imaginary fence, then reads off ciphertext row by row.
  - Tools: Online Rail Fence cipher tools

- **Columnar Transposition:**
  - Description: Rearranges plaintext letters according to a sequence of integers derived from a keyword.
  - Tools: Online Columnar Transposition cipher tools

### Stream Ciphers
- **XOR Cipher:**
  - Description: Encrypts plaintext by bitwise XOR operation with a key stream.
  - Example: `C[i] = M[i] ^ K[i % len(K)]`
  - Tools: Custom scripts or online XOR calculators

## Encoding Schemes

### Base Encoding
- **Base64:**
  - Description: Converts binary data into ASCII characters for transmission.
  - Example: `echo -n "Hello, World!" | base64`
  - Tools: Command-line utilities (base64), online converters

- **URL Encoding:**
  - Description: Converts special characters into a format that can be transmitted over the Internet.
  - Example: `%20` for space
  - Tools: Online URL encoding tools

### Miscellaneous
- **Binary and Hexadecimal:**
  - Description: Representing data in binary (base-2) or hexadecimal (base-16) formats.
  - Example: `0x41` for 'A'
  - Tools: Calculator apps, programming languages

## Tools
- **CyberChef:**
  - Description: Web app for analyzing and decoding data using various ciphers and encodings.
  - Link: [CyberChef](https://gchq.github.io/CyberChef/)

- **Cryptii:**
  - Description: Online conversion tool supporting various ciphers and encodings.
  - Link: [Cryptii](https://cryptii.com/)
 
- **Dcode**
  - Description: Identify and crack almost any type of cipher out there. My personal fav.
  - Link: [Dcode](https://www.dcode.fr/en)

## References
- [Caesar Cipher](https://en.wikipedia.org/wiki/Caesar_cipher)
- [Vigenère Cipher](https://en.wikipedia.org/wiki/Vigenère_cipher)
- [Base64](https://en.wikipedia.org/wiki/Base64)
- [CyberChef](https://gchq.github.io/CyberChef/)
- [Cryptii](https://cryptii.com/)
- [Dcode](https://www.dcode.fr/en)


