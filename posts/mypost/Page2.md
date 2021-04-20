---
title: "First Os build"
date: 2021-04-18T16:50:48+05:00
default: false


---
This is my first Os build.It took us only 1 week to make even when all of the code was available online.I was faced with 3 different errors which took a long time to debug.Learned how to use git,github,Hugo,Docker and qemu.


# Os: 
This is a 64-bit operating system which is is made in C and assembly.

# Main Components:
- # DockerFile
    This is a file which creates a sort of environment to build our Os.It brings packages like NASM and Grub to the access of Os which are required at startup
- # Main.asm
    This contains the main assembly code for the os.It includes the manipulation of registers and so on.The data structures such as the main stack are defined here.At starting One Megabyte of memory is reserved for stack.
    Different modes such as Long mode,multiboot are defined here.Global Descriptor table is also defined.
- # Makefile
    This is the most high level file in the whole Os.This is where the build commands are present which build the os from assembly code and the display it.
- # Grub 
    This file is for multiboot and making new files from low level files.

# Errors:
Faced a lot of errors in this project such as

- #  Unable to find docker image:
    This was an issue where the instance of the Os created in docker refused to run.
    [Error](https://github.com/Umairius/umair.github.io/blob/main/Error%201.jpeg)
    
- #  WSL installation:
    This was an error where we had to install Windows subsystem for linux
    [Error](https://github.com/Umairius/umair.github.io/blob/main/Error%202.jpeg)
- #  Could not load PC BIOS:
    This was an error where we had to go go inside pc bios,enable virtualization and then enable hyperV in windows.After that we had to give docker and Vs go admin rights
    [Error]([Error](https://github.com/Umairius/umair.github.io/blob/main/Error%202.jpeg))



