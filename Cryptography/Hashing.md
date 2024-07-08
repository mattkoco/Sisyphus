# Hashing ooga booga

## Hash Functions
- **Definition:** Hash functions map data of arbitrary size to fixed-size values (hash values).

### Common Hash Functions
- **MD5 (Message Digest Algorithm 5):**
  - Length: 128 bits
  - Example: `md5sum file.txt`

- **SHA-1 (Secure Hash Algorithm 1):**
  - Length: 160 bits
  - Example: `sha1sum file.txt`

- **SHA-256 (Secure Hash Algorithm 256):**
  - Length: 256 bits
  - Example: `sha256sum file.txt`

## Hash Cracking Techniques
- **Brute Force:** Trying all possible combinations until a match is found.
  - Tools: Hashcat, John the Ripper

- **Dictionary Attack:** Using a list of common passwords or words to crack hashes.
  - Tools: Hashcat, John the Ripper

- **Rainbow Tables:** Precomputed tables of hashes to quickly crack passwords.
  - Tools: RainbowCrack, Ophcrack

## Hash Types and Vulnerabilities
- **Salted Hashes:** Adding a unique salt to each password before hashing prevents rainbow table attacks.
  - Example: `sha256(salt + password)`

- **Hash Collisions:** Different inputs producing the same hash value, which can weaken security.
  - Example: MD5 collisions found in practice.

## Techniques for CTFs
- **Identifying Hash Types:** Determine the hash type (MD5, SHA-1, SHA-256) for effective cracking.
  - Example: Hash identifier tools (`hash-identifier`)

- **Online Tools:** Utilize online hash cracking services for quick results.
  - Example: CrackStation, HashKiller

- **Custom Scripts:** Write Python or Bash scripts for specific hash cracking tasks in CTF challenges.

## References
- [MD5](https://en.wikipedia.org/wiki/MD5)
- [SHA-1](https://en.wikipedia.org/wiki/SHA-1)
- [SHA-256](https://en.wikipedia.org/wiki/SHA-2)
- [Hashcat](https://hashcat.net/hashcat/)
- [John the Ripper](https://www.openwall.com/john/)
- [RainbowCrack](http://project-rainbowcrack.com/)
- [Crackstation](https://crackstation.net/)
- ![Hash Identifier](https://hashes.com/en/tools/hash_identifier)
