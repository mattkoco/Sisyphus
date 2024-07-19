# ELF Files

## Introduction
ELF (Executable Linking Format) files are the most common method of packaging executables on UNIX systems. If you're used to Windows, you can think of it as the Linux equivalent of a ``.exe`` file. In most of the CTF competitions you'll encounter them in, ELFs will be compiled C code or occasionally bash.

### Reverse Engineering an ELF

## Initial Understanding
- **Ghidra**
	- Ghidra is one of the many tools you can use. it is good for static analysis and getting an idea of the code. 
	- A full guide to the tool ought to be created somewhere besides here; for now, this guide assumes you know the basics of its usage
- **Using Ghidra**
  	- Open your file and choose to analyze it
  	- Use the menus on the side to view the function tree then look through to find where the first function is.
  	- Once you find a vulnerable funciton, you can bring it into a dynamic complier like gdb and look through
- **Exploiting**
	- After you have a good idea of what the file does, i'll write this bit later
