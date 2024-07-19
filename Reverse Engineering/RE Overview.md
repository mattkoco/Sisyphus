# Reverse Engineering Overview

## Introduction
- **Definition:** Reverse engineering involves taking a program, binary, or script produced by some external source and analyzing it to figure out how it works. In a CTF context, you then have to reverse the file by writing a script that reverses whatever the file did to find the decrypted flag.

## RE Tips (in no particular order)
- **Deobfuscate:**
  - Many reverse engineering challenges will use confusing function names and variables, as well as "dead code" that does nothing, to make it hard to read
    - Use find-and-replace in a text editor to replace them with more readable names
  - Online code beautifiers can help
    - https://beautifier.io/ is a good one for JS

- **Decompile:**
  - Compiled code won't be readable to you
  - Use a tool to decompile it
    - Ghidra
    - x64 debugger
    - https://dogbolt.org/ remotely hosts a ton of tools

- **Translate the code:**
  - If the code is in a language you don't know, translate it line-by-line into a language you do know
  - Google is your friend here
  - You'll probably get a basic understanding of the new language as you do this

- **Understanding the code:**
  - Read through it line-by-line
  - Understand what every for/while loop does
    - I like to visualize it on paper
  - Use print statements
  - Step through it with a debugger
 
# GOOGLE IS YOUR FRIEND
seriously if you don't know what you're doing google does
