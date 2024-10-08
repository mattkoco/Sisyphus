# RSA 4 Dummies
I hope you paid attention in math class

## Key Generation
- **Step 1: Choose two large prime numbers, p and q**
  - Example: p = 61, q = 53

- **Step 2: Compute n = p * q**
  - Example: n = 61 * 53 = 3233

- **Step 3: Compute Euler's totient function, φ(n) = (p-1) * (q-1)**
  - Example: φ(3233) = 60 * 52 = 3120

- **Step 4: Choose an integer e such that 1 < e < φ(n) and gcd(e, φ(n)) = 1**
  - Example: e = 17 (common choice)

- **Step 5: Compute d, the modular multiplicative inverse of e mod φ(n)**
  - Example: d = 2753 (calculated using extended Euclidean algorithm)

- **Public Key (e, n):** (17, 3233)
- **Private Key (d, n):** (2753, 3233)

## Encryption
- **Plaintext message:** M (where 0 ≤ M < n)
  - Example: M = 1234

- **Cipher text calculation:** C ≡ M^e (mod n)
  - Example: C ≡ 1234^17 (mod 3233) = 855

- **Encrypted message:** C = 855

## Decryption
- **Cipher text:** C
  - Example: C = 855

- **Decrypted message calculation:** M ≡ C^d (mod n)
  - Example: M ≡ 855^2753 (mod 3233) = 1234

- **Decrypted message:** M = 1234

## Common Pitfalls
- **Small primes:** Choosing small primes makes the RSA vulnerable to factorization attacks.
- **Common modulus attack:** Reusing n across different keys makes the encryption insecure.

## Tools
- **RsaCtfTool:** A Python script for RSA encryption/decryption in CTF challenges.
- **openssl:** Command-line tool for RSA key generation, encryption, and decryption.

## References
- [RSA Algorithm](https://en.wikipedia.org/wiki/RSA_(cryptosystem))
- [RsaCtfTool](https://github.com/Ganapati/RsaCtfTool)

