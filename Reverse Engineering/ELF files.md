# ELF Files

## Introduction
ELF (Executable Linking Format) files are the most common method of packaging executables on UNIX systems. If you're used to Windows, you can think of it as the Linux equivalent of a ``.exe`` file. In most of the CTF competitions you'll encounter them in, ELFs will be compiled C code or occasionally bash.

## Recognizing an ELF
* Usually have no file extension
* The ``file`` command will respond with some variant of ``ELF data``
* Opening the raw data in a text editor will turn up the string "ELF" in the header of the file

## Reverse Engineering an ELF

### Initial Understanding
- **Ghidra**
	- Ghidra is the main tool you'll use for reverse engineering
	- A full guide to the tool ought to be created somewhere besides here; for now, this guide assumes you know the basics of its usage
	- This guide also assumes the ELF is compiled C and that you can read it
- **Shape of the File**
  - Open the file in Ghidra
  - Go to the ``Functions`` tab and look at the ``main`` function
  - Read what the file is meant to do when it's opened
  - Read any other functions called by ``main``
- **Exploiting**
	- After you have a good idea of what the file does, i'll write this bit later
